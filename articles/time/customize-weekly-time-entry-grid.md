---
title: Extinderea intrărilor de timp
description: Acest subiect oferă informații despre modul în care dezvoltatorii pot extinde controlul introducerii de timp.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930895"
---
# <a name="extending-time-entries"></a>Extinderea intrărilor de timp

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations includ un control personalizat pentru introducerea timpului extensibil. Acest control include următoarele caracteristici:

- Introduceți orizontal timp de o săptămână
- Totaluri pe zi, rând sau săptămână
- Copiați rânduri sau săptămâni
- Intrarea de timp prin HH:mm sau HH.hh (se convertește automat la HH.hh)
- Importați din atribuiri, rezervări sau întâlniri

Extinderea intrărilor de timp este posibilă în două domenii:
- [Adăugați intrări de timp personalizate pentru propria dvs. utilizare](#add)
- [Particularizați controlul săptămânal de control cronometru](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Adăugați intrări de timp particularizate pentru propria dvs. utilizare.

Intrările de timp sunt o entitate de bază care este concepută pentru a fi utilizată pentru mai multe scenarii. În valul 1 de lansare din aprilie 2020, a fost introdusă soluția de bază TESA, care oferă o entitate **Setări** și un nou rol de securitate **Utilizator de intrare în timp**. Noile câmpuri, **msdyn_start** și **msdyn_end** care au o relație directă cu **msdyn_duration**, au fost, de asemenea, incluse. Noua entitate, rol de securitate, și câmpurile permit o abordare mai unitară a timpului pe mai multe produse.


### <a name="time-source-entity"></a>Entitate sursă de timp
| Câmp | Descriere | 
|-------|------------|
| Nume  | Numele intrării Sursă timp utilizată ca valoare de selecție în timpul creării intrării timpului. |
| Sursă de timp implicită [Sursă de timp: isdefault] | În mod implicit, o singură sursă de timp poate fi marcată la sursa de timp implicită. Această capacitate permite ca intrările să fie implicite la o sursă de timp dacă una nu este specificată. |
|Tipul sursei de timp [Sursa de timp: sourcetype] | Tipul de sursă este o opțiune (Time Entry Type Source) care permite asocierea sursei de timp la o aplicație. La acest set de opțiuni se vor adăuga valori suplimentare pe măsură ce se adaugă aplicații suplimentare. Rețineți că Microsoft rezervă valori mai mari decât 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Intrări de timp și entitatea sursă de timp
Fiecare intrare de timp este asociată cu o înregistrare a sursei de timp. Această înregistrare determină cum și ce aplicații ar trebui să proceseze introducerea timpului.

Intrările de timp sunt întotdeauna un bloc contiguu de timp cu începutul, sfârșitul și durata legate.

Logica va actualiza automat înregistrarea introducerii timpului în următoarele situații:

- Dacă sunt furnizate două din cele trei câmpuri următoare, al treilea este calculat automat 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Câmpurile, **msdyn_start** și **msdyn_end** sunt conștienți de fusul orar.
- Intrări de timp create numai cu **msdyn_date** și **msdyn_duration** specificat va începe la miezul nopții și **msdyn_start** și **msdyn_end** va fi actualizat corespunzător.

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

- Adăugați câmpul particularizat la caseta de dialog Creare rapidă.
- Configurați grila pentru a afișa câmpul particularizat.
- Adăugați câmpul particularizat fie la rândul de flux de activități de editare, fie la fluxul de activități de editare a celulei.

De asemenea, trebuie să vă asigurați că noul câmp are validările necesare în fluxul de activitate de editare a rândului sau celulei. Ca parte a acestui pas, trebuie să blocați câmpul pe baza stării înregistrării de timp.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adăugați câmpul particularizat la caseta de dialog Creare rapidă
Trebuie să adăugați câmpul particularizat la caseta de dialog **Creați intrarea de timp creare rapidă**. Utilizatorii pot apoi introduce o valoare atunci când adaugă intrări de timp selectând **Nou**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurați grila pentru a afișa câmpul particularizat
Există două modalități pentru adăugarea unui câmp particularizat la grila de introducere de timp săptămânală:

  - Personalizați o vizualizare și adăugați un câmp personalizat
  - Creați o nouă intrare de timp implicită particularizată 


**Personalizați o vizualizare și adăugați un câmp personalizat**

Puteți particulariza vizualizarea **Vizualizarea înregistrărilor mele săptămânale de timp** și să adăugați câmpul particularizat la acesta. Aveți posibilitatea să alegeți poziția și dimensiunea câmpului particularizat din grilă editând acele proprietăți în vizualizare.

**Creați o nouă intrare de timp implicită particularizată** 

Această vizualizare ar trebui să conțină câmpurile **Descriere** și **Comentarii externe**, în plus față de coloanele pe care doriți să le aveți în grilă. 

1. Alegeți poziția, dimensiunea și ordinea implicită de sortare a grilei editând acele proprietăți în vizualizare. 
2. Configurați controlul particularizat pentru această vizualizare, astfel încât să fie un control **Grilă de introducere timp**. 
3. Adăugați acest control la vizualizare și selectați-l pentru web, telefon și tabletă. 
4. Configurați parametrii pentru grila de introducere de timp săptămânal. Setați câmpul **Data de începere** la **msdyn_date**, setați câmpul **Durată** la **msdyn_duration** și setați câmpul **Stare** la **msdyn_entrystatus**. 
5. Pentru vizualizarea implicită, câmpul **Listă de stare doar în citire** este setat la **192350002,192350003,192350004**, câmpul **Flux activitate editare rând** este setat la **msdyn_timeentryrowedit** și **Flux sarcină editare celulă** este setat la **msdyn_timeentryedit**. 
6. Aveți posibilitatea să particularizați aceste câmpuri pentru a adăuga sau elimina starea doar în citire sau pentru a utiliza o altă experiență bazată pe sarcini (TBX) pentru editarea rândului sau a celulelor. Aceste câmpuri trebuie să fie legate la o valoare statică.


> [!NOTE] 
> Ambele opțiuni vor elimina unele filtrări predefinite pe entitățile **Proiect** și **Activitate de proiect** astfel încât toate vizualizările de căutare pentru entități vor fi vizibile. În mod predefinit, numai vizualizările de căutare relevante sunt vizibile.
Trebuie să determinați fluxul de activitate corespunzător pentru câmpul particularizat. Cel mai probabil, dacă ați adăugat câmpul la grilă, acesta ar trebui să meargă fluxul de activități de editare câmp care este utilizat pentru câmpurile care se aplică la întregul rând de înregistrări de timp. În cazul în care câmpul particularizat are o valoare unică în fiecare zi, ar fi un câmp particularizat pentru **Ora de sfârșit**, acesta ar trebui să meargă în fluxul de activități de editare a celulei.

Pentru a adăuga câmpul particularizat la un flux de activitate, glisați un element **Câmp** în poziția corespunzătoare din pagină, apoi setați-i proprietățile de câmp. Setați proprietatea **Sursă** la **Înregistrare timp** și setați proprietatea **Câmp de date** la câmpul particularizat. Proprietatea **Câmp** specifică numele afișat pe pagina TBX. Selectați **Aplicare** pentru a salva modificările pe câmp, apoi selectați **Actualizați** pentru a salva modificările pe pagină.

Pentru a utiliza o nouă pagină particularizată TBX în schimb, creați un proces nou. Setați categoria la **Flux de business**, setați entitatea la **Înregistrare timp** și setați tipul de proces de afaceri la **Executare proces ca flux de activități**. Sub **Proprietăți**, proprietatea **Nume de pagină** trebuie setată la numele afișat pentru pagină. Adăugați toate câmpurile relevante la pagina TBX. Salvați și activați procesul și apoi actualizați proprietatea de control particularizat pentru fluxul de activități relevant la valoarea **Nume** în proces.

### <a name="add-new-option-set-values"></a>Adăugați noi valori set de opțiuni
Pentru a adăuga valori set de opțiuni la un câmp predefinit, deschideți pagina de editare pentru câmp, apoi, sub **Tip**, selectați **Editare** lângă setul de opțiuni. Apoi, adăugați o nouă opțiune care are o etichetă și o culoare particularizate. Dacă doriți să adăugați o nouă stare de înregistrare de timp, câmpul predefinit este **Stare înregistrare**, nu **Stare.**

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Desemnați o nouă stare de înregistrare de timp ca doar în citire
Pentru a desemna o nouă stare de înregistrare de timp ca doar în citire, adăugați noua valoare de intrare de timp la proprietatea **Listă de stare doar în citire**. Partea editabilă a grilei de înregistrare de timp va fi blocată pentru rândurile care au starea nouă.
Apoi, adăugați reguli de afaceri pentru a bloca toate câmpurile de pe paginile TBX **Editare rând introducere timp** și **Editare înregistrare timp**. Puteți accesa regulile de business pentru aceste pagini deschizând editorul flux de business pentru pagină, apoi selectând **Reguli de afaceri**. Aveți posibilitatea să adăugați starea nouă la condiția din regulile de business existente sau să adăugați o nouă regulă de business pentru noua stare.

### <a name="add-custom-validation-rules"></a>Adăugarea de reguli de validare particularizate
Există două tipuri de reguli de validare pe care le puteți adăuga pentru experiența săptămânală a grilei de introducere a timpului:

- Regulile de business din partea clientului care funcționează în casete de dialog rapide și pe pagini TBX.
- Validări de inserturi de la server care se aplică tuturor actualizărilor de intrare de timp.

#### <a name="business-rules"></a>Reguli de business
Utilizați reguli de business pentru a bloca și debloca câmpuri, pentru a introduce valori implicite în câmpuri și pentru a defini validări care necesită informații numai din înregistrarea de intrare de timp curentă. Puteți accesa regulile de business pentru o pagină TBX deschizând editorul flux de business pentru pagină, apoi selectând **Reguli de business**. Aveți posibilitatea să editați regulile de business existente sau să adăugați o nouă regulă de business. Pentru validări și mai personalizate, puteți utiliza o regulă de business pentru a executa JavaScript.

#### <a name="plug-in-validations"></a>Validări insert
Ar trebui să utilizați validările de insert pentru orice validări care necesită mai mult context decât este disponibil într-o singură înregistrare de intrare de timp sau pentru orice validări pe care doriți să executați pe actualizările inline în grilă. Pentru a finaliza validarea, creați un insert particularizat pe entitatea de **Înregistrare timp**.
