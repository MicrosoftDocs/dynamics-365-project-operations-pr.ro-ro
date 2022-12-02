---
title: Adăugarea membrilor echipei din grila de membri Echipă
description: Acest articol oferă informații despre cum puteți gestiona resursele membrului echipei.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928585"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Adăugarea membrilor echipei din grila de membri Echipă

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations include un tablou de bord al managerului de resurse care oferă o prezentare vizuală a cererii și utilizării resurselor în întreaga organizație. Puteți utiliza diagramele de pe acest tablou de bord pentru a vizualiza următoarele informații:

- **Cerere resursă**: diagrama **Solicitare de resursă activă** afișează resursele care au fost remise. Resursele sunt agregate după fiecare rol sau proiect.
- **Cerere de resurse neremise**: diagrama **Cerere de resurse neatribuite** afișează toate cerințele de resurse care nu au fost remise. Această diagramă ajută managerii de resurse să vizualizeze cererea care nu este fermă și poate fi remisă printr-o solicitare de resurse.
- **Utilizarea facturabilă pentru săptămâna trecută**: diagrama **Utilizare în funcție de rol** arată procentul utilizării efective facturabile a organizației în funcție de rolul pe care l-a avut asupra utilizării sale facturabile în funcție de rol.

    > [!NOTE]
    > Pentru a face diagrama **Utilizare după rol** disponibilă, creați o operațiune care rulează fluxul de lucru **UpdateRoleUtilization**. Această operațiune periodică se execută la fiecare șapte zile pentru a calcula utilizarea facturabilă pentru ultimele șapte zile. Rezultatele sunt agregate în funcție de rol.

## <a name="manage-project-team-members"></a>Gestionarea membrilor echipei de proiect

Managerii de proiect pot utiliza tabloul de bord al managerului de resurse pentru a gestiona resursele din proiecte. De exemplu, ele pot adăuga un membru al echipei direct la un proiect și rezerva un membru al echipei pentru a îndeplini cerințele de resurse care au fost capturate de o resursă generică.

### <a name="add-a-team-member-directly-to-a-project"></a>Adăugarea unui membru al echipei direct la un proiect

Pentru a adăuga un membru al echipei direct la un proiect, pe formularul **Proiecte**, pe fila **Echipă**, selectați **Nou**. Apare caseta de dialog **Creare rapidă:membru al echipei de proiect**. În această casetă de dialog, aveți posibilitatea să efectuați aceste activități:

- **Rezervați o resursă denumită**: în câmpul **Resursă care se poate rezerva**, selectați numele resursei. Apoi selectați rolul, setați perioada și selectați o metodă de alocare. Resursa denumită pe care ați selectat-o este adăugată la proiect utilizând metoda de alocare selectată și calendarul de resurse.
- **Adăugați o resursă generică**: lăsați câmpul **Resurse care se pot rezerva** necompletat, apoi selectați rolul, setați perioada și selectați metoda de alocare preferată. O resursă generică este adăugată echipei ca substituent. Substituentul deține modelul cererii care este utilizat pentru a rezerva resurse numite în echipă. Cerința se face în funcție de calendarul proiectului.
- **Adăugați la echipă o resursă denumită fără a consuma capacitatea de resurse**: în câmpul **Resursă care se poate rezerva**, selectați o resursă. Selectați perioada și apoi selectați **Niciuna** ca metodă de alocare. Resursa este adăugată la echipă, dar capacitatea resursei nu este consumată printr-o rezervare.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervați un membru al echipei pentru a îndeplini cerințele de resurse pentru o resursă generică

În Project Operations, puteți rezerva o resursă generică pe o echipă de proiect. De asemenea, puteți specifica rolul, capacitatea necesară și modul în care este distribuită această capacitate. Pentru cerința de resurse, aveți posibilitatea să specificați atributele care sunt asociate cu resursa generică. Aceste atribute includ aptitudinile necesare, unitatea organizațională preferată și resursele preferate.

Completați pașii următori pentru a specifica abilitățile necesare pe o resursă generică pentru un dezvoltator.

1. Pe formularul **Proiecte**, pe fila **Echipă**, selectați **Nou** pentru a rezerva o resursă generică.
2. În vizualizarea **Toți membrii echipei**, în coloana **Cerință de resursă**, selectați linkul pentru a adăuga abilitățile necesare pentru resursa generică.
3. Pe formularul **Cerință de resurse** care apare, în grila **Abilități**, selectați punctele de suspensie (**...**) și apoi selectați **Adăugați noua caracteristică de cerință** pentru a adăuga abilitățile necesare pentru dezvoltator.
4. În formularul de dialog **Creare rapidă: caracteristică cerință** care apare, în câmpul **Caracteristică**, selectați abilitatea necesară.
5. În câmpul **Valoare de evaluare**, selectați nivelul de competență pentru acea abilitate. 
6. În câmpul **Cerință de resursă**, setați cerința de resurse pentru a obține resurse din unități organizaționale sau chiar resurse numite. Când ați terminat, selectați **Salvare**.
7. Pe formularul **Cerință resursă**, selectați **Rezervare** pentru a îndeplini cerința de resurse. De asemenea, puteți selecta resursa generică în grila **Toți membrii echipei** și apoi selectați **Rezervare**.

    > [!NOTE]
    > În acest exemplu, există 40 ore necesare, dar nu ore rezervate reale, deoarece resursele generice nu au rezervări. În plus, nu există ore atribuite, deoarece resursa generică a fost adăugată direct la echipă în loc să fie adăugat utilizând atribuirea activităților.

    În formularul **Asistent de planificare**, aveți posibilitatea să filtrați resursele disponibile după cerințele specificate în cerința de resursă. Resursele sunt sortate în funcție de parametrii de sortare specificați în Tabloul de planificare.

   Unele dintre cele mai utilizate filtre sunt:

    - **Caracteristici, împreună cu o evaluare**: filtrare după abilități, certificari, și alte calități de resurse, în plus față de evaluarea de competență.
    - **Roluri**: filtrați după rolurile implicite care sunt atribuite resurselor care se pot rezerva.
    - **Unități organizaționale**: filtrați resursele care pot fi rezervate de către unitățile organizaționale la care sunt atribuite.

8. Dacă nu sunteți mulțumit de rezultatele căutării inițiale de cerințe, aveți posibilitatea să modificați criteriile de filtrare. Extindeți panoul **Vizualizare filtrare** din partea stângă, apoi selectați **Căutare** pentru a găsi resurse suplimentare. Pentru a modifica modul de sortare a rezultatelor, selectați **Sortare**.
9. Selectați resurse în funcție de cererea specificată pe cerință, așa cum este indicat în partea de sus a grilei. Puteți goli selecția celulelor din grilă și lăsați acea capacitate de resurse deschisă. Poate fi selectată drept rezervată o singură resursă pe rând.
10. Selectați **Rezervare** pentru a rezerva resursa selectată și lăsați tabloul de planificare deschis, astfel încât să puteți selecta resurse suplimentare. Alternativ, selectați **Rezervați și ieșiți** pentru a rezerva resursa selectată și închideți tabloul de planificare.
11. Reveniți la vizualizarea **Toți membrii echipei**. În grilă, observați că resursa generic a fost înlocuită de resursa denumită și 40 ore sunt listate ca rezervate pentru acea resursă.

    > [!NOTE]
    > Nu sunt afișate ore alocate, deoarece acestea au fost rezervate direct în echipă. Nu au fost rezervate prin atribuirea sarcinilor.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuiți resurse generice la activități și generați cerințe de resurse

În Project Operations, aveți posibilitatea să creați activități și apoi să le atribuiți resurse generice. Cererea de resurse poate fi reprezentată de substituenți în timp ce estimați planificarea și numerele financiare. Puteți genera apoi cerințe de resurse pentru resursele generice și să le îndepliniți.

1. Pe formularul de **Proiecte**, în fila **Planificare**, selectați **Adăugare** pentru a crea o activitate.
2. În câmpul **Resurse**, selectați simbolul **Selectorul de resurse**. Selectorul de resurse apare și afișează membrii echipei existente pentru proiect.
3. Introduceți numele resursei generice noi, apoi selectați **Creare**.
4. În caseta de dialog **Creare rapidă: membrul echipei de proiect** care apare, în câmpul **Rol**, selectați rolul pentru resursa generică. 
5. În câmpul **Unitate resursă**, selectați unitatea organizațională pentru resursa generică. Apoi selectați **Salvare**. Membrul generic al echipei este acum atribuit activității.

   În fila **Echipă**, veți vedea noul membru generic al echipei. Observați că are doar ore atribuite. Aceste ore sunt suma tuturor activităților care sunt atribuite membrului generic de echipă. Membrul generic al echipei nu are încă orele necesare sau o cerință de resurse.

6. Acum aveți posibilitatea să atribuiți membrul generic de echipă altor activități utilizând selectorul de resurse.

   După ce ați terminat asocierea resursei generice la activități, aveți posibilitatea să generați o cerință de resursă pentru resursa generică.

7. În fila **Echipă**, selectați resursa generică, apoi selectați **Generare cerință**. Când se generează cerința, membrul generic al echipei va avea ore necesare și un link pentru cerința de resurse.

  După ce rezervați o resursă denumită, resursa generică este eliminată din echipă și înlocuită de resursa denumită. În fila **Planificare**, atribuirile de resurse generice sunt eliminate și înlocuite de resursa denumită.

  > [!NOTE]
  > Acest comportament are loc numai atunci când o resursă denumită este complet rezervată pentru cerința de resurse generice. Când fie o resursă denumită înlocuiește parțial cerința de resurse generice sau mai multe resurse numite înlocuiesc cerința de resurse generice, resursa generică rămâne atribuită activității.

Project Operations nu atribuie ambele resurse activității, pentru că acel comportament ar produce o planificare mai puțin previzibilă. În acest exemplu simplu, este ușor să împărțiți orele în mod egal între două resurse. Cu toate acestea, în scenarii mai complexe care implică mai multe sarcini și mai multe resurse, PSA ar trebui să facă presupuneri despre ar trebui să aloce rezervările care sunt primite pentru mai multe resurse în mai multe activități.

Prin urmare, în aceste scenarii, managerul de proiect este responsabil pentru analizarea mai multor rezervări și atribuirea acestora după cum este necesar. Pentru a aloca rezervările, managerul de proiect atribuie activitățile din resursele generice la resursele numite și apoi utilizează vizualizarea **Reconciliere** pentru a vă asigura că alocarea funcționează cu rezervările.

### <a name="edit-a-resource-requirement"></a>Editați o cerință de resurse

După ce s-a creat o cerință de resursă, un manager de proiect sau un Manager resurse poate dori să editeze detaliile pentru a rafina criteriile de căutare atunci când se utilizează tabloul de planificare. Pentru a edita cerința de resurse, urmați acești pași.

1. Pe formularul **Proiecte**, pe fila **Echipă**, selectați linkul spre orice cerință pe o resursă generică.
2. Pe formularul **Cerința de resurse** care apare, introduceți informațiile de câmp necesare

   Pe formularul **Cerința de resurse**, managerul de proiect sau manager de resurse pot defini, de asemenea, abilități, roluri, preferințe de resurse și unitatea organizațională preferată.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualizați rezervările de resurse după ce sunt rezervate pe un proiect

După ce ați adăugat o resursă generică sau denumită într-o echipă de proiect, aveți posibilitatea să modificați rezervările resursei.

1. Pe formularul **Proiecte**, pe fila **Echipă**, selectați un membru al echipei și apoi selectați **Mențineți rezervări**.
 
   Consiliul de planificare apare și afișează rezervările membrilor echipei de proiect. Extindeți înregistrarea membrului echipei pentru a vizualiza orele care au fost rezervate împotriva acestui proiect și a altor proiecte care consumă capacitatea membrului echipei.

2. Selectați și glisați rezervarea pentru a o prelungi sau scurta. Va apărea o casetă de dialog **Creare rezervare de resursă** care vă permite să ajustați rezervarea.
3. Faceți clic dreapta pe rezervare. Apoi, puteți utiliza meniul de comenzi rapide pentru a finaliza următoarele acțiuni:

    - Modificați starea rezervării
    - Editați rezervarea
    - Înlocuiți o resursă în echipa de proiect

### <a name="change-the-booking-status"></a>Modificați starea rezervării

Aveți posibilitatea să modificați orice stare de rezervare implicită sau particularizată.

Următoarele stări sunt incluse în Project Operations:

- **Anulat**: anulează rezervarea unei resurse și eliberează capacitatea resursei.
- **Rezervare fermă**: consumă capacitatea unei resurse. O rezervare are de obicei această stare atunci când deschideți **Mențineți rezervările** din grila **Toți membrii echipei** pe formularul **Proiecte**.
- **Rezervare permisivă** – adaugă o resursă unei echipe, dar nu consumă capacitatea resursei. Această stare indică faptul că resursa a fost rezervat pentru lucru potențial, dar are încă capacitate în cazul în care este nevoie de alte procese. În vederea disponibilității globale a resurselor, rezervările provizorii au o stare diferită față de rezervările ferme.
- **Propus**: reprezintă o propunere de manager de resurse sau de manager de proiect pentru o resursă. Propunerile nu consumă capacitatea unei resurse, iar resursa nu este adăugată echipei de proiect. Pentru a rezerva ferm resursa pe echipă, managerul de proiect trebuie să accepte propunerea.

### <a name="submit-resource-requests"></a>Remiterea solicitărilor de resurse

Solicitările de resurse sunt utilizate pentru a purta cererea (solicitarea de resursă) care trebuie procesată de un manager de resurse. Pentru o resursă generică care este deja în echipă, aveți posibilitatea să remiteți direct o solicitare de resursă. O solicitare de resurse poate fi procesată în două moduri:

- Managerul de resurse procesează direct solicitarea. În acest caz, resursa generică este înlocuită de o rezervare fermă care are o resursă denumită.
- Managerul de resurse propune o resursă pentru managerul de proiect, iar managerul de proiect aprobă sau respinge resursa propusă.

#### <a name="direct-fulfillment-of-resource-requests"></a>Procesarea directă a cererilor de resurse

Atunci când se generează o cerință de resurse, un manager de proiect poate remite o solicitare de resurse pentru o resursă generică selectând resursa și apoi selectând **Remitere solicitarea**. Comentariile despre resursă pot fi furnizate managerului de resurse care procesează solicitarea. După depunerea solicitării, câmpul **Stare** pentru membrul echipei este modificat la **Remis**. Când managerul de resurse procesează solicitarea, membrul generic de echipă este înlocuit de resursa denumită în grila **Toți membrii echipei**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilizarea unei propuneri de resurse pentru solicitări de resurse

În loc să rezerve direct o resursă pe o solicitare de resurse, un manager de resurse poate propune o resursă pentru managerul de proiect. Un manager de resurse poate utiliza această opțiune atunci când nu este disponibilă o potrivire exactă pentru cerințe. Atunci când un manager de resurse propune o resursă, managerul de proiect vede că câmpul **Stare** pentru membrul generic de echipă este modificat la **Necesită revizuire**.

Puteți vizualiza resursa propusă împreună cu o vizualizare a efectului rezervării propunerii. 

1. Faceți dublu clic pe membrul echipei care are statutul de **Necesită revizuire**. 
2. Selectați fila **Resurse propuse**.
3. Selectați **Acceptați toate propunerile** pentru a accepta toate resursele propuse sau **Respingeți toate propunerile** pentru a le respinge. Dacă acceptați resursele propuse, acestea sunt ferm rezervate pe proiect ca membri ai echipei și înlocuiesc resursele generice.

> [!NOTE]
> Trebuie fie să acceptați, fie să respingeți toate resursele propuse. Nu le puteți accepta parțial sau respinge.

### <a name="substitute-a-resource-on-the-project-team"></a>Înlocuiți o resursă în echipa de proiect

Uneori, un manager de proiect trebuie să înlocuiască un membru al echipei rezervat într-un proiect.

1. Pe formularul **Proiecte**, pe fila **Echipă**, selectați resursa care are nevoie de o înlocuire și apoi selectați **Mențineți rezervări**.
2. Extindeți resursa pentru a vizualiza proiectele la care este atribuită.
3. Faceți clic dreapta pe proiect și apoi selectați **Înlocuitor resursă**.
4. Dacă cunoașteți resursa pe care doriți să o înlocuiți pentru resursa curentă, selectați sau tastați numele, apoi selectați **Reatribuire**.

Sau. Dacă trebuie să căutați o resursă, parcurgeți pașii următori.

1. Selectați **Găsire substituire**.

   Asistentul de planificare returnează o listă de înlocuitori disponibili. În Asistentul de planificare, puteți filtra și mai mult resursele disponibile pentru a găsi un substitut adecvat.

2. Pentru a înlocui resursa, selectați resursa dorită, apoi selectați **Înlocuitor**.   

   Rezervările și atribuirile sunt înlocuite cu noua resursă.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Reconciliați rezervările și atribuirile membrilor echipei

Pentru membrii echipei, rezervările și atribuirile sunt cuplate lejer. Cu alte cuvinte, resursele pot avea misiuni, dar nu rezervări, sau pot avea rezervări, dar nu atribuiri. În mod ideal, rezervările și atribuirile ar trebui aliniate, astfel încât resursele au o capacitate angajată de a realiza activitățile atribuite. Cu toate acestea, rezervările s-ar putea să se bazeze pe disponibilitate, iar timpii de activitate s-ar putea modifica pe măsură ce proiectul continuă. Prin urmare, cuplarea lejeră a rezervărilor și atribuirilor furnizează flexibilitate.

Project Operations are o filă de **Reconciliere** care permite managerilor de proiect să reconcilieze rezervările membrilor echipei și atribuirile lor pentru echipele de proiect.

Fila **Reconciliere** afișează rezervările și atribuirile până la nivelul atribuirii individuale a activității pentru fiecare membru al echipei. Acesta arată ore în celule, care pot reprezenta perioade de timp de la luni până la zile.

Fila afișează, de asemenea, un total net global pentru proiect, împreună cu o coloană totală.

Pentru fiecare resursă, fila calculează diferența dintre rezervările membrului echipei pe proiect și un cumulul al atribuirilor de activități ale acelui membru al echipei. În mod ideal, această diferență ar trebui să fie 0 (zero). Cu alte cuvinte, nu ar trebui să existe nicio diferență între rezervări și atribuiri. Diferențele sunt colorate și umbrite pentru a atrage atenția asupra a două condiții:

- **Deficit de rezervare**: apare atunci când o resursă are mai multe atribuiri decât rezervări. Deoarece această capacitate nu a fost rezervată, un manager de proiect ar putea vrea să corecteze această condiție extinzând rezervările resursei pentru a acoperi deficitul.
- **Rezervări în exces**: rezervările în exces apar atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților. Această condiție ar putea fi acceptabilă în cazurile în care resursa a fost rezervată la proiect înainte să aibă loc atribuirea activității. Cu toate acestea, în alte cazuri, resursa nu este planificată să fie atribuită activităților. În aceste cazuri, managerul de proiect ar trebui să ia în considerare anularea rezervările resursei, astfel încât capacitatea să poată fi utilizată pentru un alt proiect.

În unele cazuri, când vizualizați timpul la un nivel mai înalt decât nivelul zilei, de exemplu, nivelul lunii, este posibil să vedeți o diferență netă de zero pentru o resursă. Cu alte cuvinte, rezervări = sarcini. Cu toate acestea, dacă vă uitați la nivel de săptămână, este posibil să vedeți că există atribuiri de zero ore și rezervări de 40 ore în prima săptămână, dar atribuiri de 40 ore și rezervări de zero ore în a doua săptămână. În general, rezervările și atribuirile sunt reconciliate, dar acestea diferă de la o săptămână la alta.

Când vizualizați timpul la nivele mai înalte, celulele din fila **Reconciliere** au un indicator pentru a vă informa că sunt diferențe la niveluri mai joase. Faceți dublu clic într-o celulă, aveți posibilitatea să măriți pentru a vizualiza diferența. Apoi puteți face clic dreapta pentru a micșora. Selectând o resursă și apoi selectând **Următoarea diferență** pe grila barei de instrumente, puteți trece la următoarea diferență dintre rezervări și atribuiri pentru acea resursă. Selectați **Diferența precedentă** pentru a reveni. De asemenea, puteți dezactiva indicatorul de diferență și comportamentul de navigare sub **Setări**.

DAcă aveți atribuiri de activități pentru o resursă dar nu rezervări pe formularul **Proiecte**, pe fila **Reconciliere**, selectați deficitul de rezervare și apoi selectați **Extindeți rezervarea**. Apare caseta de dialog **Extindere rezervare** și afișează rezervarea necesară pentru a aborda deficitul resursei. Caseta de dialog arată și rezervările existente ale resursei în toate proiectele sau alte entități care pot fi planificate. Dacă selectați **OK** pentru a crea rezervarea pentru resursă, indiferent de disponibilitatea acelei resurse, este posibil să cauzați o suprarezervare.

Managerul de proiect sau managerul de resurse pot utiliza apoi Panoul de planificare pentru a gestiona orice situații în care o resursă este suprarezervată peste capacitate.


[!INCLUDE[footer-include](../includes/footer-banner.md)]