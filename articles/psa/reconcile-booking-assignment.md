---
title: Reconciliați rezervări și atribuiri
description: Acest subiect oferă informații despre valorile reale.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 9528bd983e6e18197138f0720abccdc6d6fa1ed5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147938"
---
# <a name="reconcile-bookings-and-assignments"></a>Reconciliați rezervări și atribuiri

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Rezervările de proiect ale unui membru al echipei de proiect și atribuirile de sarcini de proiect sunt cuplate lejer. De aceea, o resursă poate avea atribuirile de activități care nu corespund rezervărilor și rezervări care nu corespund atribuirilor de activități. În mod ideal, rezervările de proiect și atribuirile sunt aliniate, astfel încât resursele au angajată capacitatea de a-și efectua atribuirile de sarcini. Cu toate acestea, realitatea este că rezervările pot apărea în funcție de disponibilitate, iar timpii de activitate se pot schimba pe măsură ce proiectul continuă prin ciclul său de viață. Prin urmare, cuplarea lejeră permite flexibilitate.

Din cauza cuplării lejere a rezervărilor de proiect și a atribuirilor de activități, în entitatea Proiect este inclusă o filă de **Reconciliere**. Această filă îi ajută managerii de proiect să reconcilieze rezervările membrilor echipei și sarcinile lor pentru echipa lor de proiect.

Pentru fiecare membru al echipei numit, fila **Reconciliere** afișează rezervările și atribuirile până la atribuirea sarcinilor individuale. Acesta arată ore în celule, care pot reprezenta perioade de luni până la zile.

În câmpul **Scală de timp**, aveți posibilitatea să selectați **Lună**, **Săptămână** sau **Zi**. **Săptămână** este selectat în mod implicit. Cu toate acestea, aveți posibilitatea să modificați valoarea implicită selectând butonul **Setări**. Când se deschide fila **Reconciliere**, aceasta afișează data curentă, dar se poate utiliza controlul calendarului pentru a avansa sau a merge înapoi în timp. Când un proiect are o dată de începere care se află în viitor, fila afișează acea dată când este deschisă. Controlul calendarului are, de asemenea, opțiuni care vă permit să mergeți la datele de început și de sfârșit ale proiectului.

Puteți utiliza controalele de extindere pentru fiecare resursă pentru a afișa detaliile rezervărilor acelei resurse. De asemenea, aveți posibilitatea să extindeți atribuirile fiecărei resurse la nivelul activității individuale.

Partea de jos a filei **Reconciliere** afișează un total net global pentru proiect și fila include, de asemenea, o coloană totală. Pentru fiecare resursă, fila ia diferența dintre rezervările unui membru al echipei pe proiect și cumulul de misiuni de activitate ale acelui membru al echipei. În mod ideal, diferența ar trebui să fie 0 (zero). Cu alte cuvinte, nu ar trebui să existe nicio diferență între rezervările resursei și sarcinile sale de activitate. Orice diferențe sunt indicate prin culoare și umbrire pentru a apela două condiții:

- **Deficit de rezervare** – deficitul de rezervare apare atunci când o resursă are mai multe atribuiri decât rezervări. Deoarece această capacitate nu a fost rezervată, un manager de proiect poate corecta această condiție extinzând rezervările resursei pentru a acoperi deficitul.
- **Rezervări în exces** – rezervările în exces apar atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților. Această condiție poate fi acceptabilă dacă, de exemplu, resursa a fost rezervată înainte să apară atribuirea de activități. Cu toate acestea, în alte cazuri, resursa ar putea să nu fie planificată pentru a fi atribuită. În aceste cazuri, managerul de proiect ar trebui să ia în considerare anularea rezervările resursei, astfel încât capacitatea să poată fi utilizată pentru un alt proiect.

> [!NOTE]
> Legenda pentru aceste condiții ar putea fi ascunsă pentru a lăsa mai mult spațiu pentru grilă. În acest caz, puteți face legenda vizibilă selectând butonul **Setări**.

În unele cazuri, atunci când câmpul **Scală timp** este setat la un nivel care este mai mare decât **Zi**, diferențele pot fi calculate ca 0 (zero). De exemplu, la nivel de **Lună**, diferența netă pentru o resursă ar putea fi 0 (zero) pentru a indica faptul că rezervările sunt egale cu atribuirile. Cu toate acestea, dacă vă uitați la nivel de **Săptămână**, este posibil să vedeți că există atribuiri de 0 (zero) ore și rezervări de 40 ore în prima săptămână a lunii, și misiuni de 40 ore și rezervări de 0 (zero) ore în a doua săptămână a lunii. Deși totalul rezervărilor și atribuirile pentru lună sunt egale, acestea diferă prin săptămână.

Când vizualizați niveluri mai mari de timp, fila **Reconciliere** afișează un indicator de celulă pentru a vă notifica că există diferențe la nivelurile mai mici de timp. De exemplu, în următoarea ilustrație, un indicator de celulă apare în celula pentru luna octombrie 2018 pentru resursa denumită Ileana Grasu. Prin urmare, puteți vedea că, chiar dacă rezervările și atribuirile resursei sunt egale atunci când acestea sunt agregate la nivel de **Lună**, ele nu se potrivesc la niveluri mai mici.

![Rezervări și atribuiri nepotrivite la nivel lunar](media/reconcile-assignments-01.JPG)

Faceți dublu clic pe o celulă pentru a mări la următorul nivel inferior și a vedea diferența. De exemplu, dacă faceți dublu clic pe diferența din octombrie 2018 pentru Ileana Grasu, detaliați până la nivel de **Săptămână**. Puteți vedea apoi că resursa are rezervări de 16 ore, dar nu atribuiri în primele două săptămâni din octombrie, și 16 de ore de atribuiri, dar nu rezervări în a treia săptămână a lui octombrie.

![Rezervări și atribuiri nepotrivite la nivel săptămânal](media/reconcile-assignments-02.JPG)

Aveți posibilitatea să faceți clic dreapta pe o celulă pentru a micșora următorul nivel superior. De asemenea, puteți dezactiva indicatorul celulei selectând butonul **Setări**. 

De asemenea, puteți utiliza butoanele **Anterior** și **Următor** de deasupra grilei pentru a vă deplasa prin orice diferențe din proiect. Pentru a utiliza aceste butoane, trebuie mai întâi să selectați o resursă. Selectați **Următorul** pentru a merge la următoarea diferență între rezervările și atribuirile pentru acea resursă. Selectați **Anterior** pentru a trece la diferența anterioară.

În situațiile în care aveți atribuiri de activități pentru o resursă, dar fără rezervări, aveți posibilitatea să selectați deficitul de rezervare și apoi să selectați **Extindere rezervare**. Puteți vedea apoi rezervarea necesară pentru a aborda deficitul resursei. De asemenea, puteți vizualiza rezervările resursei în proiectul curent și în alte proiecte. Selectați **OK** pentru a crea rezervarea resursei fără a ține cont de disponibilitatea curentă. Managerul de proiect sau managerul de resurse pot utiliza apoi panoul de planificare pentru a gestiona situațiile în care o resursă a devenit supra-rezervată peste capacitate, deoarece rezervările sale s-au extins.

## <a name="managing-with-time-zones"></a>Gestionarea cu fusuri orare
Pentru a asigura rezultate precise și previzibile atunci când utilizați Extend Booking, există două premise-cheie care trebuie îndeplinite:  

- Utilizatorul trebuie să configureze fusul orar al dispozitivului pentru a se potrivi cu fusul orar definit în Setările de personalizare ale sistemului.
 
  ![Setările fusului orar în Windows 10](media/reconcile-assignments-03.png)

  ![Setările fusului orar în setările de personalizare](media/reconcile-assignments-04.png)
 
- Resursa rezervabilă trebuie să aibă cel puțin un minut de timp de lucru care se suprapune contururilor utilizate pentru a defini extensia solicitată. De exemplu, următorul exemplu arată resursele de revizuire cu ore de lucru care se încadrează între 9:00 AM și 19:00. 

  ![Comparația contururilor resurselor](media/reconcile-assignments-05.png)

Tabelul următor afișează:

- Un șablon de calendar de proiect.
- Resursa A: Această resursă are același calendar și se află în același fus orar cu proiectul. Ora de început a rezervărilor va fi ora 9:00.
- Resurse B: Această resursă este localizată într-un alt fus orar decât proiectul și, prin urmare, începe la ora 7:00 în fusul lor orar. Cu toate acestea, rezervările vor începe la ora 9:00, deoarece aceasta este cea mai timpurie perioadă de începere a conturului misiunii.
- Resurse C și D: Resursele sunt, de asemenea, amplasate în zone de timp diferite, ambele diferite între ele și proiect, iar rezervările lor încep nu mai devreme decât orele de pornire disponibile.

|Entitate  |Calendar  |
|-|-|
|Șablon de calendar de proiect   | ![calendarul proiectului](media/reconcile-assignments-06.png) |
|Resursă A  | ![Calendar resursa A](media/reconcile-assignments-06.png) |
|Resursă B  |  ![Calendar resursa B](media/reconcile-assignments-07.png) |
|Resursă C  |  ![Calendar resursa C](media/reconcile-assignments-08.png) |
|Resursă D  | ![Calendar resursa D](media/reconcile-assignments-09.png)  |
 
Când navigați la vizualizarea de reconciliere, vor fi afișate alocările de resurse și deficiențele de rezervare asociate.
 ![Vedere de reconciliere înainte de extensie](media/reconcile-assignments-10.png)

După ce funcționalitatea Extind Booking este executată pe fiecare resursă, rezervările sunt extinse cu succes pentru fiecare resursă. Acest lucru se datorează faptului că orele de lucru ale fiecărei resurse s-au suprapus cu contururile deficitului.
 ![Vizualizare de reconciliere după extinderea rezervării](media/reconcile-assignments-11.png) 

Cu toate acestea, o privire mai atentă la detaliile rezervărilor arată diferențe în ora de început a rezervărilor. Rezervările vor începe nu mai devreme decât ora de început a conturului misiunii și nu mai devreme decât ora de pornire disponibilă a resursei.
 ![Rezervări noi ale resurselor din tabloul de bord](media/reconcile-assignments-12.png)
