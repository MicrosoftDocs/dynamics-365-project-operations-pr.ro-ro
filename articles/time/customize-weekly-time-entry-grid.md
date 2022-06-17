---
title: Extinderea intrărilor de timp
description: Acest articol oferă informații despre modul în care dezvoltatorii pot extinde controlul introducerii timpului.
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
Fiecare intrare de timp este asociată cu o înregistrare a sursei de timp. Această înregistrare determină ce aplicații ar trebui să proceseze introducerea orei și cum.

Intrările de timp sunt întotdeauna un bloc contiguu de timp cu începutul, sfârșitul și durata legate.

Logica va actualiza automat înregistrarea introducerii timpului în următoarele situații:

- Dacă sunt furnizate două din cele trei câmpuri următoare, al treilea este calculat automat: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- The **msdyn_start** și **msdyn_end** câmpurile sunt conștiente de fusul orar.
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

1. Adăugați câmpul personalizat la **Creare rapidă** căsuță de dialog.
2. Configurați grila pentru a afișa câmpul particularizat.
3. Adăugați câmpul personalizat la **Editare rând** sau **Editare intrare timp** pagina, după caz.

Asigurați-vă că noul câmp are validările necesare pe **Editare rând** sau **Editare intrare timp** pagină. Ca parte a acestei sarcini, blocați câmpul, în funcție de starea intrării de timp.

Când adăugați un câmp personalizat la **Intrarea timpului** grilă și apoi creați intrări de timp direct în grilă, câmpul personalizat pentru acele intrări este setat automat astfel încât să se potrivească cu rândul. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adăugați câmpul personalizat în caseta de dialog Creare rapidă
Adăugați câmpul personalizat la **Creare rapidă: Creați intrare de timp** căsuță de dialog. Utilizatorii pot apoi introduce o valoare atunci când adaugă intrări de timp selectând **Nou**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurați grila pentru a afișa câmpul particularizat
Există două modalități de a adăuga un câmp personalizat la **Intrare săptămânală a timpului** grilă.

- Personalizați **Înregistrările mele săptămânale de timp** vizualizare și adăugați câmpul personalizat la acesta. Puteți specifica poziția și dimensiunea câmpului personalizat în grilă prin editarea proprietăților din vizualizare.
- Creați o nouă vizualizare personalizată pentru introducerea orei și setați-o ca vizualizare implicită. Această vedere ar trebui să conțină **Descriere** și **Comentarii externe** câmpuri în plus față de coloanele pe care doriți să le includă grila. Puteți specifica poziția, dimensiunea și ordinea implicită de sortare a grilei prin editarea proprietăților din vizualizare. Apoi, configurați controlul particularizat pentru această vizualizare, astfel încât să fie un control **Grilă introducere timp**. Adăugați controlul la vizualizare și selectați-l pentru **Web**, **·**, și **Comprimat**. Apoi, configurați parametrii pentru **Intrare săptămânală a timpului** grilă. Seteaza **Data de început** câmp la **msdyn\_ Data**, Seteaza **Durată** câmp la **msdyn\_ durată**, și setați **stare** câmp la **msdyn\_ starea de intrare**. The **Listă de stare numai pentru citire** câmpul este setat la **192350002 (Aprobat)**, **(Trimis)**, sau **192350004 (rechemare solicitată)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Adăugați câmpul personalizat la pagina de editare corespunzătoare
Paginile care sunt folosite pentru a edita o intrare de timp sau un rând de intrări de timp pot fi găsite sub **Forme**. The **Editați intrarea** butonul din grilă deschide **Editați intrarea** pagina, iar **Editați rândul** butonul deschide **Editare rând** pagină. Puteți edita aceste pagini astfel încât să includă câmpuri personalizate.

Ambele opțiuni elimină unele filtre out-of-box activate **Proiect** și **Sarcina proiectului** entități, astfel încât toate vizualizările de căutare pentru entități să fie vizibile. În mod implicit, numai vizualizările de căutare relevante sunt vizibile.

Trebuie să determinați pagina corespunzătoare pentru câmpul personalizat. Cel mai probabil, dacă ați adăugat câmpul la grilă, acesta ar trebui să meargă pe **Editare rând** pagină care este utilizată pentru câmpurile care se aplică întregului rând de intrări de timp. Dacă câmpul personalizat are o valoare unică în rând în fiecare zi (de exemplu, dacă este un câmp personalizat pentru ora de încheiere), acesta ar trebui să meargă pe **Editare intrare timp** pagină.

Pentru a adăuga câmpul personalizat la o pagină, trageți a **Camp** element în poziția corespunzătoare pe pagină și apoi setați proprietățile acestuia.

### <a name="add-new-option-set-values"></a>Adăugați noi valori set de opțiuni
Pentru a adăuga valori set de opțiuni într-un câmp neconform, urmați acești pași.

1. Deschideți pagina de editare a câmpului, apoi sub **Tip**, Selectați **Editați | ×** lângă set de opțiuni.
2. Adăugați o nouă opțiune care are o etichetă și o culoare particularizate. Dacă doriți să adăugați o nouă stare de introducere a orei, câmpul out-of-box este numit **Stare de intrare**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Desemnați o nouă stare de înregistrare de timp ca doar în citire
Pentru a desemna o nouă stare de înregistrare de timp ca doar în citire, adăugați noua valoare de intrare de timp la proprietatea **Listă de stare doar în citire**. Asigurați-vă că adăugați numărul, nu eticheta. Partea editabilă a grilei de introducere a timpului va fi acum blocată pentru rândurile care au noua stare. Pentru a seta **Listă de stare numai pentru citire** proprietate diferit pentru diferit **Intrarea timpului** vizualizări, adăugați **Intrarea timpului** grilă într-o vedere **Controale personalizate** secțiunea și configurați parametrii după caz.

Apoi, adăugați reguli de afaceri pentru a bloca toate câmpurile din **Editare rând** și **Editare intrare timp** pagini. Pentru a accesa regulile de afaceri pentru aceste pagini, deschideți editor formular pentru fiecare pagină, apoi selectați **Reguli de afaceri**. Aveți posibilitatea să adăugați starea nouă la condiția din regulile de business existente sau să adăugați o nouă regulă de business pentru noua stare.

### <a name="add-custom-validation-rules"></a>Adăugarea de reguli de validare particularizate
Puteți adăuga două tipuri de reguli de validare pentru **Intrare săptămânală de timp** experiență grilă:

- Reguli de afaceri la nivelul clientului care funcționează pe pagini
- Validări de plug-in pe partea de server care se aplică tuturor actualizărilor de intrare de timp

#### <a name="client-side-business-rules"></a>Reguli de afaceri la nivelul clientului
Utilizați reguli de business pentru a bloca și debloca câmpuri, pentru a introduce valori implicite în câmpuri și pentru a defini validări care necesită informații numai din înregistrarea de intrare de timp curentă. Pentru a accesa regulile de afaceri pentru o pagină, deschideți editor formular, apoi selectați **Reguli de afaceri**. Aveți posibilitatea să editați regulile de business existente sau să adăugați o nouă regulă de business.

#### <a name="server-side-plug-in-validations"></a>Validări de plug-in-uri pe partea de server
Ar trebui să utilizați validări de plug-in pentru orice validări care necesită mai mult context decât este disponibil într-o singură înregistrare de timp. De asemenea, ar trebui să le utilizați pentru orice validări pe care doriți să le executați pentru actualizările inline din grilă. Pentru a finaliza validările, creați un plug-in personalizat pe **Intrarea timpului** entitate.

### <a name="limits"></a>Limite
În prezent, cel **Intrarea timpului** grila are o limită de dimensiune de 500 de rânduri. Dacă există mai mult de 500 de rânduri, rândurile în exces nu vor fi afișate. Nu există nicio modalitate de a crește această limită de dimensiune.

### <a name="copying-time-entries"></a>Copiere intrări de timp
Utilizați vizualizarea **Copiere coloane intrări de timp** pentru a defini lista câmpurilor de copiat în timpul introducerii timpului. **Data** și **Durata** sunt câmpuri obligatorii și nu trebuie eliminate din vizualizare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
