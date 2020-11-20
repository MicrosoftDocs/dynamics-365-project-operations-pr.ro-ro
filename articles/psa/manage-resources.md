---
title: Gestionare resurse
description: Acest subiect oferă informații despre cum puteți gestiona resursele.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132348"
---
# <a name="manage-resources"></a>Gestionare resurse

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation include un tablou de bord al managerului de resurse care oferă o prezentare vizuală a cererii și utilizării resurselor în întreaga organizație. Puteți utiliza diagramele de pe acest tablou de bord pentru a vizualiza următoarele informații:

- **Cerere resursă** – diagrama **Solicitare de resursă activă** afișează resursele care au fost remise. Resursele sunt agregate după fiecare rol sau proiect.
- **Cerere de resurse neremise** - diagrama **Cerere de resurse neremise** afișează toate cerințele de resurse care nu au fost remise. Ajută managerii de resurse să vizualizeze cererea care nu este fermă și poate fi remisă printr-o solicitare de resurse.
- **Utilizarea facturabilă pentru săptămâna trecută** – diagrama **Utilizare în funcție de rol** arată procentul utilizării efective facturabile a organizației în funcție de rolul pe care l-a avut asupra utilizării sale facturabile în funcție de rol.

    > [!NOTE]
    > Pentru a face diagrama **Utilizare în funcție de rol** disponibilă, creați o operațiune care rulează fluxul de lucru UpdateRoleUtilization. Această operațiune periodică se execută la fiecare șapte zile pentru a calcula utilizarea facturabilă pentru ultimele șapte zile. Rezultatele sunt agregate în funcție de rol.

## <a name="manage-project-team-members"></a>Gestionarea membrilor echipei de proiect

Managerii de proiect pot utiliza tabloul de bord al managerului de resurse pentru a gestiona resursele din proiecte. De exemplu, ele pot adăuga un membru al echipei direct la un proiect și rezerva un membru al echipei pentru a îndeplini cerințele de resurse care au fost capturate de o resursă generică.

### <a name="add-a-team-member-directly-to-a-project"></a>Adăugarea unui membru al echipei direct la un proiect

Pentru a adăuga un membru al echipei direct la un proiect, pe pagina **Proiecte**, pe fila **Echipă**, selectați **Nou**. Apare caseta de dialog **Creare rapidă:membru al echipei de proiect**. În această casetă de dialog, aveți posibilitatea să efectuați aceste activități:

- **Rezervați o resursă denumită** - în câmpul **Resursă care se poate rezerva**, selectați numele resursei. Apoi selectați rolul, setați perioada și selectați o metodă de alocare. Resursa denumită pe care ați selectat-o este adăugată la proiect utilizând metoda de alocare selectată și calendarul de resurse.
- **Adăugați o resursă generică**- lăsați câmpul **Resurse care se pot rezerva** necompletat, apoi selectați rolul, setați perioada și selectați metoda de alocare preferată. O resursă generică este adăugată la echipă ca un substituent pentru a ține modelul cererii care este utilizat pentru a rezerva resursele numite pe echipă. Cerința se face în funcție de calendarul proiectului.
- **Adăugați la echipă o resursă denumită fără a consuma capacitatea de resurse**- în câmpul **Resursă care se poate rezerva**, selectați o resursă. Apoi selectați perioada și selectați **Niciuna** ca metodă de alocare. Resursa este adăugată la echipă, dar capacitatea resursei nu este consumată printr-o rezervare.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervați un membru al echipei pentru a îndeplini cerințele de resurse pentru o resursă generică

În PSA, aveți posibilitatea să rezervați o resursă generică într-o echipă de proiect și să specificați rolul, capacitatea necesară și modul în care este distribuită această capacitate. Pe cerința de resurse, aveți posibilitatea să specificați atributele care sunt asociate cu resursa generică. Aceste atribute includ aptitudinile necesare, unitatea organizațională preferată și resursele preferate.

Urmați acești pași pentru a specifica abilitățile necesare pe o resursă generică pentru un dezvoltator.

1. Pe pagina **Proiecte**, pe fila **Echipă**, selectați **Nou** pentru a rezerva o resursă generică.

    ![Resursă generică rezervată echipei](media/Resource-Management-image9.png)

2. În vizualizarea **Toți membrii echipei**, în coloana **Cerință de resursă**, selectați linkul pentru a adăuga abilitățile necesare pentru resursa generică.

    ![Link cerință](media/Resource-Management-image10.png)

3. Pe pagina **Cerință de resurse** care apare, în grila **Abilități**, selectați punctele de suspensie (**...**) și apoi selectați **Adăugați noua caracteristică cerință** pentru a adăuga abilitățile necesare pentru dezvoltator.

    ![Adăugați comandă nouă Caracteristică cerință](media/Resource-Management-image11.png)

4. În caseta de dialog **Creare rapidă: caracteristică cerință** care apare, în câmpul **Caracteristică**, selectați abilitatea necesară. Apoi, în câmpul **Valoare de evaluare**, selectați nivelul de competență pentru acea abilitate. În cele din urmă în câmpul **Cerință de resursă**, setați cerința de resurse pentru a obține resurse din unități organizaționale sau chiar resurse numite. Când ați terminat, selectați **Salvare**.

    ![Creare rapidă: caseta de dialog Caracteristică cerință](media/Resource-Management-image12.png)

5. Pe pagina **Cerință resursă**, selectați **Rezervare** pentru a îndeplini cerința de resurse.

    ![Buton de rezervare pe pagina Cerință de resursă](media/Resource-Management-image13.png)

    De asemenea, puteți selecta resursa generică în grila **Toți membrii echipei** și apoi selectați **Rezervare**.

    ![Butonul rezervare de deasupra grilei Toți membrii echipei](media/Resource-Management-image14.png)

    > [!NOTE]
    > În acest exemplu, există 40 ore necesare, dar nu ore rezervate reale, deoarece resursele generice nu au rezervări. În plus, nu există ore atribuite, deoarece resursa generică a fost adăugată direct la echipă. Nu s-a adăugat utilizând atribuirea sarcinilor.

    În pagina **Asistent de planificare**, aveți posibilitatea să filtrați resursele disponibile după cerințele specificate în cerința de resursă. Resursele sunt sortate în funcție de parametrii de sortare specificați în Tabloul de planificare.

    ![Pagina Asistent de planificare](media/Resource-Management-image15.png)

    Iată câteva filtre care sunt adesea utilizate:

    - **Caracteristici, împreună cu o evaluare** - filtrare după abilități, certificari, și alte calități de resurse, în plus față de evaluarea de competență.
    - **Roluri** – filtrați după rolurile implicite care sunt atribuite resurselor care se pot rezerva.
    - **Unități organizaționale** – filtrați resursele care pot fi rezervate de către unitățile organizaționale la care sunt atribuite.

6. Dacă nu sunteți mulțumit de rezultatele căutării inițiale de cerințe, aveți posibilitatea să modificați criteriile de filtrare. Extindeți panoul **Vizualizare filtrare** din partea stângă, apoi selectați **Căutare** pentru a găsi resurse suplimentare.

    ![Panou vizualizare filtrare](media/Resource-Management-image16.png)

7. Pentru a modifica modul de sortare a rezultatelor, selectați **Sortare**.

    ![Comanda sortare](media/Resource-Management-image17.png)

8. Selectați resurse în funcție de cererea specificată pe cerință, așa cum este indicat în partea de sus a grilei. Puteți goli selecția celulelor din grilă și lăsați acea capacitate de resurse deschisă. Poate fi selectată drept rezervată o singură resursă pe rând.

9. Selectați **Rezervare** pentru a rezerva resursa selectată și lăsați tabloul de planificare deschis, astfel încât să puteți selecta resurse suplimentare. Alternativ, selectați **Rezervați și ieșiți** pentru a rezerva resursa selectată și închideți tabloul de planificare.

    ![Resursă de rezervat](media/Resource-Management-image19.png)

    Primiți o notificare despre orele rezervate. Indicatorii cererii arată cât de mult cerința de rezervare este îndeplinită și cât de mult rămâne. De asemenea, puteți vedea cât de mult din capacitatea resursei selectate este consumată. Selectați **Extindeți** pentru a vizualiza mai multe detalii despre rezervările de resurse.

9. Reveniți la vizualizarea **Toți membrii echipei**. În grilă, observați că resursa generic a fost înlocuită de resursa denumită și 40 ore sunt listate ca rezervate pentru acea resursă.

    ![Actualizat grila Toți membrii echipei](media/Resource-Management-image20.png)

    > [!NOTE]
    > Nu sunt afișate ore alocate, deoarece acestea au fost rezervate direct în echipă. Nu au fost rezervate prin atribuirea sarcinilor.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuiți resurse generice la activități și generați cerințe de resurse

În PSA, aveți posibilitatea să creați activități și apoi să le atribuiți resurse generice. În acest fel, cererea de resurse poate fi reprezentată de substituenți în timp ce estimați planificarea și numerele financiare. Puteți genera apoi cerințe de resurse pentru resursele generice și să le îndepliniți.

1. Pe pagina de **Proiecte**, în fila **Planificare**, selectați **Adăugare** pentru a crea o activitate.

    ![Activitate nouă creată](media/Resource-Management-image21.png)

2. În câmpul **Resurse**, selectați simbolul **Selectorul de resurse**. Selectorul de resurse apare și afișează membrii echipei existente pentru proiect.

    ![Selector resurse](media/Resource-Management-image22.png)

3. Introduceți numele resursei generice noi, apoi selectați **Creare**.

    ![Numele unei noi resurse generice introduse](media/Resource-Management-image23.png)

4. În caseta de dialog **Creare rapidă: membrul echipei de proiect** care apare, în câmpul **Rol**, selectați rolul pentru resursa generică. În câmpul **Unitate resursă**, selectați unitatea organizațională pentru resursa generică. Apoi selectați **Salvare**.

    ![Creare rapidă: caseta de dialog Membrul echipei de proiect](media/Resource-Management-image24.png)

    Membrul generic al echipei este acum atribuit activității.

    ![Membrul generic al echipei atribuit activității](media/Resource-Management-image25.png)

    În fila **Echipă**, veți vedea noul membru generic al echipei. Observați că are doar ore atribuite. Aceste ore sunt suma tuturor activităților care sunt atribuite membrului generic de echipă. Membrul generic al echipei nu are încă orele necesare sau o cerință de resurse.

    ![Membru generic de echipă în fila Echipă](media/Resource-Management-image26.png)

5. Acum aveți posibilitatea să atribuiți membrul generic de echipă altor activități utilizând selectorul de resurse.

    ![Membru generic de echipă în selectorul de resurse](media/Resource-Management-image27.png)

    După ce ați terminat asocierea resursei generice la activități, aveți posibilitatea să generați o cerință de resursă pentru resursa generică.

5. În fila **Echipă**, selectați resursa generică, apoi selectați **Generare cerință**.

    ![Comanda Generați cerința](media/Resource-Management-image28.png)

    Când se generează cerința, membrul generic al echipei va avea ore necesare și un link pentru cerința de resurse.

    ![Link cerință de resurse](media/Resource-Management-image29.png)

    După ce rezervați o resursă denumită, resursa generică este eliminată din echipă și înlocuită de resursa denumită.

    ![Resursă generică înlocuită de resursa denumită](media/Resource-Management-image30.png)

    În fila **Planificare**, atribuirile de resurse generice sunt eliminate și înlocuite de resursa denumită.

    ![Atribuiri ale resursei generice înlocuite de resursa denumită pe fila Planificare](media/Resource-Management-image31.png)

    > [!NOTE]
    > Acest comportament are loc numai atunci când o resursă denumită este complet rezervată pentru cerința de resurse generice. Când fie o resursă denumită înlocuiește parțial cerința de resurse generice sau mai multe resurse numite înlocuiesc cerința de resurse generice, resursa generică rămâne atribuită activității.

    În ilustrația următoare, o activitate de 80 de ore a fost planificată pentru o durată de cinci zile (16 ore pe zi timp de cinci zile) și atribuită resursei generice care este numită **Funcțională**.

    ![Activitate de optzeci de ore, cinci zile, atribuită resursei generice funcționale](media/Resource-Management-image32.png)

    Când generați cerința, este de 80 de ore timp de cinci zile.

    ![Cerință generată pentru 80 ore tim de cinci zile](media/Resource-Management-image33.png)

    Deoarece resursele disponibile funcționează doar opt ore pe zi, sunt necesare două resurse pentru a îndeplini cerința.

    ![A doua resursă](media/Resource-Management-image35.png)

    În fila **Echipă**, puteți vedea acum că resursa generică nu are ore necesare, dar orele atribuite apar în continuare împreună cu cele două resurse numite care alcătuiesc procesarea.

    ![Două resurse denumite în fila Echipă](media/Resource-Management-image36.png)

    Pe fila **Planificare** resursa generică rămâne atribuită activității.

    ![Resurse generice în fila planificare](media/Resource-Management-image37.png)

PSA nu atribuie ambele resurse activității, pentru că acel comportament ar produce o planificare mai puțin previzibilă. În acest exemplu simplu, este ușor să împărțiți orele în mod egal între două resurse. Cu toate acestea, în scenarii mai complexe care implică mai multe sarcini și mai multe resurse, PSA ar trebui să facă presupuneri despre ar trebui să aloce rezervările care sunt primite pentru mai multe resurse în mai multe activități.

Prin urmare, în aceste scenarii, managerul de proiect este responsabil pentru analizarea mai multor rezervări și atribuirea acestora după cum este necesar. Pentru a aloca rezervările, managerul de proiect atribuie activitățile din resursele generice la resursele numite și apoi utilizează vizualizarea **Reconciliere** pentru a vă asigura că alocarea funcționează cu rezervările.

### <a name="edit-a-resource-requirement"></a>Editați o cerință de resurse

După ce s-a creat o cerință de resursă, un manager de proiect sau un manager de resurse poate dori să editeze detaliile pentru a rafina criteriile de căutare atunci când se utilizează tabloul de planificare. Pentru a edita cerința de resurse, urmați acești pași.

1. Pe pagina **Proiecte**, pe fila **Echipă**, selectați linkul spre orice cerință pe o resursă generică.
2. Pe pagina **Cerință de resurse** care apare, aveți posibilitatea să actualizați mai multe atribute. Iată câteva exemple:

    - Nume
    - De la data
    - Până în prezent
    - Durată
    - Tip de resursă

Pe pagina **Cerință de resurse**, managerul de proiect sau managerul de resurse poate defini, de asemenea, următoarele informații:

- Competențe
- Roluri
- Preferințe resurse
- Unitate organizațională preferată

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualizați rezervările de resurse după ce sunt rezervate pe un proiect

După ce ați adăugat o resursă generică sau denumită într-o echipă de proiect, aveți posibilitatea să modificați rezervările resursei.

1. Pe pagina **Proiecte**, pe fila **Echipă**, selectați un membru al echipei și apoi selectați **Mențineți rezervări**.

    ![Consiliul de planificare deschis pentru membrul de echipă selectat](media/Resource-Management-image40.png)

    Consiliul de planificare apare și afișează rezervările membrilor echipei de proiect. Extindeți înregistrarea membrului echipei pentru a vizualiza orele care au fost rezervate împotriva acestui proiect și a altor proiecte care consumă capacitatea membrului echipei.

2. Selectați și glisați rezervarea pentru a o prelungi sau scurta. Va apărea o casetă de dialog **Creare rezervare de resursă** care vă permite să ajustați rezervarea.

    ![Creați o casetă de dialog de Rezervare resursă](media/Resource-Management-image41.png)

3. Faceți clic dreapta pe rezervare. Apoi, puteți utiliza meniul de comenzi rapide pentru a finaliza următoarele acțiuni:

    - Modificați starea rezervării.
    - Editați rezervarea.
    - Înlocuiți o resursă în echipa de proiect.

### <a name="change-the-booking-status"></a>Modificați starea rezervării

Aveți posibilitatea să modificați orice stare de rezervare implicită sau particularizată.

![Modificați starea comenzii](media/Resource-Management-image42.png)

Următoarele stări sunt incluse în PSA:

- **Anulat** – această stare anulează rezervarea unei resurse și eliberează capacitatea resursei.
- **Rezervare fermă** - această stare consumă capacitatea unei resurse. O rezervare are de obicei această stare atunci când deschideți **Mențineți rezervările** din grila **Toți membrii echipei** pe pagina **Proiecte**.
- **Rezervare permisivă** – această stare adaugă o resursă unei echipe, dar nu consumă capacitatea resursei. Acesta indică faptul că resursa a fost rezervat pentru lucru potențial, dar are încă capacitate în cazul în care este nevoie de alte procese. În vederea disponibilității globale a resurselor, rezervările provizorii au o stare diferită față de rezervările ferme.
- **Propus** – acest statut reprezintă o propunere de manager de resurse sau de manager de proiect pentru o resursă. Propunerile nu consumă capacitatea unei resurse, iar resursa nu este adăugată echipei de proiect. Pentru a rezerva ferm resursa pe echipă, managerul de proiect trebuie să accepte propunerea.

### <a name="submit-resource-requests"></a>Trimiterea solicitărilor de resurse

Solicitările de resurse sunt utilizate pentru a purta cererea (solicitarea de resursă) care trebuie procesată de un manager de resurse. Pentru o resursă generică care este deja în echipă, aveți posibilitatea să remiteți direct o solicitare de resursă. O solicitare de resurse poate fi procesată în două moduri:

- Managerul de resurse procesează direct solicitarea. În acest caz, resursa generică este înlocuită de o rezervare fermă care are o resursă denumită.
- Managerul de resurse propune o resursă pentru managerul de proiect, iar managerul de proiect aprobă sau respinge resursa propusă.

#### <a name="direct-fulfillment-of-resource-requests"></a>Procesarea directă a cererilor de resurse

Atunci când se generează o cerință de resurse, un manager de proiect poate remite o solicitare de resurse pentru o resursă generică selectând resursa și apoi selectând **Remitere solicitarea**.

![Buton Remiteți solicitarea](media/Resource-Management-image45.png)

Comentariile despre resursă pot fi furnizate managerului de resurse care procesează solicitarea. După depunerea solicitării, câmpul **Stare** pentru membrul echipei este modificat la **Remis**.

![Introducerea comentariilor opționale](media/Resource-Management-image46.png)

Când managerul de resurse procesează solicitarea, membrul generic de echipă este înlocuit de resursa denumită în grila **Toți membrii echipei**.

![Membrul generic al echipei înlocuit de resursa denumită în grila Toți membrii echipei](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilizarea unei propuneri de resurse pentru solicitări de resurse

În loc să rezerve direct o resursă pe o solicitare de resurse, un manager de resurse poate propune o resursă pentru managerul de proiect. Un manager de resurse poate utiliza această opțiune atunci când nu este disponibilă o potrivire exactă pentru cerințe. Atunci când un manager de resurse propune o resursă, managerul de proiect vede că câmpul **Stare** pentru membrul generic de echipă este modificat la **Necesită revizuire**.

![Statutul de membru generic al echipei s-a schimbat la Necesită revizuire](media/Resource-Management-image48.png)

Pentru a vizualiza resursa propusă împreună cu o vizualizare a efectului rezervării propunerii, faceți dublu clic pe membrul echipei care are o stare de **Necesită revizuire**. Apoi selectați fila **Resurse propuse**.

![Fila Resurse propuse](media/Resource-Management-image49.png)

Selectați **Acceptați toate propunerile** pentru a accepta toate resursele propuse sau **Respingeți toate propunerile** pentru a le respinge. Dacă acceptați resursele propuse, acestea sunt ferm rezervate pe proiect ca membri ai echipei și înlocuiesc resursele generice.

> [!NOTE]
> Trebuie fie să acceptați, fie să respingeți toate resursele propuse. Nu le puteți accepta parțial sau respinge.

### <a name="substitute-a-resource-on-the-project-team"></a>Înlocuiți o resursă în echipa de proiect

Uneori, un manager de proiect trebuie să înlocuiască un membru al echipei rezervat într-un proiect.

1. Pe pagina **Proiecte**, pe fila **Echipă**, selectați resursa care are nevoie de o înlocuire și apoi selectați **Mențineți rezervări**.
2. Extindeți resursa pentru a vizualiza proiectele la care este atribuită.

    ![Resursă extinsă pentru a afișa proiectele atribuite](media/Resource-Management-image50.png)

3. Faceți clic dreapta pe proiect și apoi selectați **Înlocuitor resursă**.
4. Dacă cunoașteți resursa pe care doriți să o înlocuiți pentru resursa curentă, selectați sau tastați numele, apoi selectați **Reatribuire**.

    ![Specificarea unui substituent de resursă](media/Resource-Management-image51.png)

    Alternativ, urmați acești pași pentru a căuta o resursă:

    1. Selectați **Găsire substituire**.

        ![Căutarea unei resurse substituent](media/Resource-Management-image52.png)

        Asistentul de planificare returnează o listă de înlocuitori disponibili. În Asistentul de planificare, puteți filtra și mai mult resursele disponibile pentru a găsi un substitut adecvat.

        ![Listă de înlocuitori disponibili](media/Resource-Management-image53.png)

    2. Pentru a înlocui resursa, selectați resursa dorită, apoi selectați **Înlocuitor**.

        ![Resursă de înlocuit selectată](media/Resource-Management-image54.png)

    Rezervările și atribuirile sunt înlocuite cu noua resursă.

    ![Rezervări și atribuiri înlocuite cu noua resursă.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Reconciliați rezervările și atribuirile membrilor echipei

Pentru membrii echipei, rezervările și atribuirile sunt cuplate lejer. Cu alte cuvinte, resursele pot avea misiuni, dar nu rezervări, sau pot avea rezervări, dar nu atribuiri. În mod ideal, rezervările și atribuirile ar trebui aliniate, astfel încât resursele au o capacitate angajată de a realiza activitățile atribuite. Cu toate acestea, rezervările s-ar putea să se bazeze pe disponibilitate, iar timpii de activitate s-ar putea modifica pe măsură ce proiectul continuă. Prin urmare, cuplarea lejeră a rezervărilor și atribuirilor furnizează flexibilitate.

PSA are o filă de **Reconciliere** care permite managerilor de proiect să reconcilieze rezervările membrilor echipei și atribuirile lor pentru echipele de proiect.

![Fila Reconciliere](media/Resource-Management-image56.png)

Fila **Reconciliere** afișează rezervările și atribuirile până la nivelul atribuirii individuale a activității pentru fiecare membru al echipei. Acesta arată ore în celule, care pot reprezenta perioade de timp de la luni până la zile.

Fila afișează, de asemenea, un total net global pentru proiect, împreună cu o coloană totală.

Pentru fiecare resursă, fila calculează diferența dintre rezervările membrului echipei pe proiect și un cumulul al atribuirilor de activități ale acelui membru al echipei. În mod ideal, această diferență ar trebui să fie 0 (zero). Cu alte cuvinte, nu ar trebui să existe nicio diferență între rezervări și atribuiri. Diferențele sunt colorate și umbrite pentru a atrage atenția asupra a două condiții:

- **Deficit de rezervare** - un deficit de rezervare apare atunci când o resursă are mai multe atribuiri decât rezervări. Deoarece această capacitate nu a fost rezervată, un manager de proiect ar putea vrea să corecteze această condiție extinzând rezervările resursei pentru a acoperi deficitul.
- **Rezervări în exces** – rezervările în exces apar atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților. Această condiție ar putea fi acceptabilă în cazurile în care resursa a fost rezervată la proiect înainte să aibă loc atribuirea activității. Cu toate acestea, în alte cazuri, resursa nu este planificată să fie atribuită activităților. În aceste cazuri, managerul de proiect ar trebui să ia în considerare anularea rezervările resursei, astfel încât capacitatea să poată fi utilizată pentru un alt proiect.

În unele cazuri, când vizualizați timpul la un nivel mai înalt decât nivelul zilei (de exemplu, nivelul lunii), este posibil să vedeți o diferență netă de zero pentru o resursă (cu alte cuvinte, rezervări = misiuni). Cu toate acestea, dacă vă uitați la nivel de săptămână, este posibil să vedeți că există atribuiri de zero ore și rezervări de 40 ore în prima săptămână, dar atribuiri de 40 ore și rezervări de zero ore în a doua săptămână. În general, rezervările și atribuirile sunt reconciliate, dar acestea diferă de la o săptămână la alta.

Când vizualizați timpul la nivele mai înalte, celulele din fila **Reconciliere** au un indicator pentru a vă informa că sunt diferențe la niveluri mai joase. Făcând dublu clic într-o celulă, aveți posibilitatea să măriți pentru a vizualiza diferența. Apoi puteți face clic dreapta pentru a micșora. Selectând o resursă și apoi utilizând controlul **Următoarea diferență** pe grila barei de instrumente, puteți trece la următoarea diferență dintre rezervări și atribuiri pentru acea resursă. Apoi puteți utiliza controlul **Diferenței anterioare** pentru a reveni. De asemenea, puteți dezactiva indicatorul de diferență și comportamentul de navigare sub **Setări**.

![Indicator diferență](media/Resource-Management-image57.png)

DAcă aveți atribuiri de activități pentru o resursă dar nu rezervări pe pagina **Proiecte**, pe fila **Reconciliere**, selectați deficitul de rezervare și apoi selectați **Extindeți rezervarea**. Apare caseta de dialog **Extindere rezervare** și afișează rezervarea necesară pentru a aborda deficitul resursei. De asemenea, arată rezervările existente ale resursei în toate proiectele sau alte entități care pot fi planificate. Dacă selectați **OK** pentru a crea rezervarea pentru resursă, indiferent de disponibilitatea acelei resurse, este posibil să cauzați o suprarezervare.

![Caseta de dialog extindere rezervare](media/Resource-Management-image58.png)

Managerul de proiect sau managerul de resurse pot utiliza apoi Panoul de planificare pentru a gestiona orice situații în care o resursă este suprarezervată peste capacitate.
