---
title: Extinderea intrărilor de timp
description: Acest articol oferă informații despre modul în care dezvoltatorii pot extinde controlul intrării de timp.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914785"
---
# <a name="extending-time-entries"></a>Extinderea intrărilor de timp

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations include un control personalizat pentru introducerea timpului extensibil. Acest control include următoarele caracteristici:

- Introduceți orizontal timp de o săptămână
- Totaluri pe zi, rând sau săptămână
- Copiați rânduri sau săptămâni
- Intrarea de timp prin HH:mm sau HH.hh (se convertește automat la HH.hh)
- Importați din atribuiri, rezervări sau întâlniri

Extinderea intrărilor de timp este posibilă în două domenii:
- [Adăugați intrări de timp personalizate pentru propria dvs. utilizare](#add)
- [Particularizați controlul săptămânal de control cronometru](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Adăugați intrări de timp particularizate pentru propria dvs. utilizare

Intrările de timp sunt o entitate de bază utilizată în mai multe scenarii. În valul 1 de lansare din aprilie 2020, a fost introdusă soluția de bază TESA. TESA oferă o entitate **Setări** și un nou rol de securitate **Utilizator de intrare de timp**. Noile câmpuri, **msdyn_start** și **msdyn_end** care au o relație directă cu **msdyn_duration**, au fost, de asemenea, incluse. Noua entitate, rol de securitate, și câmpurile permit o abordare mai unitară a timpului pe mai multe produse.


### <a name="time-source-entity"></a>Entitate sursă de timp
| Câmp | Descriere | 
|-------|------------|
| Nume  | Numele intrării Sursă timp utilizată ca valoare de selecție la crearea intrărilor de timp. |
| Sursă de timp implicită [Sursă de timp: isdefault] | În mod implicit, o singură sursă de timp poate fi marcată în mod implicit. Aceasta permite ca intrările să fie implicite la o sursă de timp dacă una nu este specificată. |
|Tipul sursei de timp [Sursa de timp: sourcetype] | Tipul de sursă este o opțiune (Time Entry Type Source) care permite asocierea sursei de timp la o aplicație. Microsoft rezervă valori mai mari decât 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Intrări de timp și entitatea sursă de timp
Fiecare intrare de timp este asociată cu o înregistrare a sursei de timp. Această înregistrare determină cum și ce aplicații ar trebui să proceseze intrarea de timp.

Intrările de timp sunt întotdeauna un bloc contiguu de timp cu începutul, sfârșitul și durata legate.

Logica va actualiza automat înregistrarea introducerii timpului în următoarele situații:

- Dacă sunt furnizate două din cele trei câmpuri următoare, al treilea este calculat automat: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Câmpurile **msdyn_start** și **msdyn_end** țin cont de fusul orar.
- Intrări de timp create numai cu **msdyn_date** și **msdyn_duration** specificate va începe la miezul nopții. Câmpurile, **msdyn_start** și **msdyn_end** se vor actualiza în consecință.

#### <a name="time-entry-types"></a>Tipuri de intrări de timp

Înregistrările de introducere a timpului au un tip asociat care definește comportamentul în fluxul de trimitere pentru aplicația asociată.

|Etichetă | Valoare|
|-----|-----|
|În pauză   |192,355,000|
|Călătorie | 192,355,001|
|Ore suplimentare   | 192,354,320|
|Lucru   | 192,350,000|
|Absență    | 192,350,001|
|Vacanță   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Particularizați controlul săptămânal de intrare de timp
Dezvoltatorii pot adăuga câmpuri și căutări suplimentare la alte entități și pot implementa reguli de afaceri personalizate pentru a-și susține scenariile de afaceri.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Adăugați câmpuri particularizate cu căutări la alte entități
Există trei pași principali pentru adăugarea unui câmp particularizat la grila de intrare de timp săptămânală.

1. Adăugați câmpul particularizat la caseta de dialog **Creare rapidă**.
2. Configurați grila pentru a afișa câmpul particularizat.
3. Adăugați câmpul particularizat la pagina **Editare rând** sau **Editare intrare de timp**, după caz.

Asigurați-vă că noul câmp are validările necesare pe pagina **Editare rând** sau **Editare intrare de timp**. Ca parte a acestei sarcini, blocați câmpul, în funcție de starea intrării de timp.

Când adăugați un câmp personalizat la grila **Intrare de timp** și apoi creați intrări de timp direct în grilă, câmpul personalizat pentru acele intrări este setat automat astfel încât să se potrivească cu rândul. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adăugați câmpul particularizat la caseta de dialog Creare rapidă
Adăugați câmpul particularizat la caseta de dialog **Creare rapidă: Creare intrare de timp**. Utilizatorii pot apoi introduce o valoare atunci când adaugă intrări de timp selectând **Nou**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurați grila pentru a afișa câmpul particularizat
Există două modalități pentru adăugarea unui câmp particularizat la grila **Intrare de timp săptămânală**.

- Particularizați vizualizarea **Intrările mele de timp săptămânale** și adăugați câmpul particularizat la aceasta. Aveți posibilitatea să specificați poziția și dimensiunea câmpului particularizat din grilă editând proprietățile în vizualizare.
- Creați o nouă vizualizare de intrare de timp personalizată și setați-o ca vizualizare implicită. Această vizualizare ar trebui să conțină câmpurile **Descriere** și **Comentarii externe** în plus față de coloanele pe care doriți să le includeți în grilă. Puteți specifica poziția, dimensiunea și ordinea implicită de sortare a grilei editând proprietățile în vizualizare. Apoi, configurați controlul particularizat pentru această vizualizare, astfel încât să fie un control **Grilă introducere timp**. Adăugați controlul la vizualizare și selectați-l pentru **Web**, **Telefon** și **Tabletă**. Apoi, configurați parametrii pentru grila de **Intrare de timp săptămânală**. Setați câmpul **Dată începere** la **msdyn\_date**, setați câmpul **Durată** la **msdyn\_duration** și setați câmpul **Stare** la **msdyn\_entrystatus**. Câmpul **Listă de stare numai pentru citire** este setat la **192350002 (Aprobat)**, **192350003 (Trimis)** sau **192350004 (Retragere solicitată)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Adăugați câmpul particularizat la pagina de editare corespunzătoare
Paginile care sunt folosite pentru a edita o intrare de timp sau un rând de intrări de timp pot fi găsite sub **Formulare**. Butonul **Editare intrare** din grilă deschide pagina **Editare intrare**, iar butonul **Editare rând** deschide pagina **Editare rând**. Puteți edita aceste pagini astfel încât să includă câmpuri personalizate.

Ambele opțiuni elimină unele filtrări predefinite de pe entitățile **Proiect** și **Sarcină proiect** astfel încât toate vizualizările de căutare pentru entități sunt vizibile. În mod implicit, numai vizualizările de căutare relevante sunt vizibile.

Trebuie să determinați pagina corespunzătoare pentru câmpul particularizat. Cel mai probabil, dacă ați adăugat câmpul la grilă, acesta ar trebui să ajungă pe pagina **Editare rând** care este utilizată pentru câmpurile care se aplică la întregul rând de intrări de timp. Dacă câmpul personalizat are o valoare unică în rând în fiecare zi (de exemplu, dacă este un câmp personalizat pentru ora de încheiere), acesta ar trebui să ajungă pe pagina **Intrare de timp**.

Pentru a adăuga câmpul particularizat lao pagină, glisați un element **Câmp** în poziția corespunzătoare de pe pagină, apoi setați-i proprietățile.

### <a name="add-new-option-set-values"></a>Adăugați noi valori set de opțiuni
Pentru a adăuga valori ale setului de opțiuni la un câmp predefinit, urmați acești pași.

1. Deschideți pagina de editare pentru câmp, apoi, sub **Tip**, selectați **Editare** lângă setul de opțiuni.
2. Adăugați o nouă opțiune care are o etichetă și o culoare particularizate. Dacă doriți să adăugați o nouă stare de intrare de timp, câmpul predefinit este numit **Stare intrare**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Desemnați o nouă stare de înregistrare de timp ca doar în citire
Pentru a desemna o nouă stare de înregistrare de timp ca doar în citire, adăugați noua valoare de intrare de timp la proprietatea **Listă de stare doar în citire**. Asigurați-vă că adăugați numărul, nu eticheta. Partea editabilă a grilei de intrare de timp va fi acum blocată pentru rândurile care au starea nouă. Pentru a seta proprietatea **Listă de stare numai pentru citire** în mod diferit pentru diferite vizualizări **Intrare de timp**, adăugați grila **Intrare de timp** într-o secțiune a vizualizării **Controale personalizate** și configurați corespunzător parametrii.

Apoi, adăugați reguli de afaceri pentru a bloca toate câmpurile de pe paginile **Editare rând** și **Editare intrare de timp**. Pentru a accesa regulile de afaceri pentru aceste pagini, deschideți editorul de formulare pentru fiecare pagină, apoi selectați **Reguli de afaceri**. Aveți posibilitatea să adăugați starea nouă la condiția din regulile de business existente sau să adăugați o nouă regulă de business pentru noua stare.

### <a name="add-custom-validation-rules"></a>Adăugarea de reguli de validare particularizate
Puteți adăuga două tipuri de reguli de validare pentru experiența grilei **Intrare de timp săptămânală**.

- Reguli de afaceri la nivel de client care funcționează pe pagini
- Validări de inserturi pe parte de server care se aplică tuturor actualizărilor de intrare de timp

#### <a name="client-side-business-rules"></a>Reguli de afaceri pe parte de client
Utilizați reguli de business pentru a bloca și debloca câmpuri, pentru a introduce valori implicite în câmpuri și pentru a defini validări care necesită informații numai din înregistrarea de intrare de timp curentă. Pentru a accesa regulile de afaceri pentru o pagină, deschideți editorul de formulare și apoi selectați **Reguli de afaceri**. Aveți posibilitatea să editați regulile de business existente sau să adăugați o nouă regulă de business.

#### <a name="server-side-plug-in-validations"></a>Validări de inserturi pe parte de server
Ar trebui să utilizați validările de insert pentru orice validări care necesită mai mult context decât este disponibil într-o singură înregistrare de intrare de timp. De asemenea, ar trebui să le utilizați pentru orice validări pe care doriți să le executați pentru actualizările în linie din grilă. Pentru a finaliza validările, creați un insert particularizat pe entitatea de **Intrare de timp**.

### <a name="limits"></a>Limite
În prezent, grila **Intrarede timp** are o limită de dimensiune de 500 de rânduri. Dacă există mai mult de 500 de rânduri, rândurile în exces nu vor fi afișate. Nu există nicio modalitate de a crește această limită de dimensiune.

### <a name="copying-time-entries"></a>Copiere intrări de timp
Utilizați vizualizarea **Copiere coloane intrări de timp** pentru a defini lista câmpurilor de copiat în timpul introducerii timpului. **Data** și **Durata** sunt câmpuri obligatorii și nu trebuie eliminate din vizualizare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
