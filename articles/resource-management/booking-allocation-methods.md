---
title: Metode de alocare a rezervării
description: Acest subiect oferă informații despre cum funcționează metodele de alocare a rezervării în Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897691"
---
# <a name="booking-allocation-methods"></a>Metode de alocare a rezervării

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Indiferent dacă adăugați un membru al echipei direct la un proiect pe fila **Echipă** sau dacă rezervați o resursă la un proiect sau o cerință din tabloul de planificare există câteva metode de alocare a rezervărilor diferite pe care le puteți utiliza. Acest subiect explică modul în care funcționează fiecare metodă și ce metode ar putea duce la suprarezervarea de resurse.

## <a name="booking-allocation-methods"></a>Metode de alocare a rezervării

Există șase metode de alocare a rezervării pe care le puteți utiliza:

- [Capacitate completă](#full)
- [Capacitate rămasă](#remaining)
- [Capacitate procentaj](#percentage)
- [Distribuiți uniform orele](#evenly)
- [Ore de încărcare frontală](#front)
- [Niciunul](#none)

### <a name="full-capacity"></a><a name="full"></a>Capacitate completă 
Metoda Capacitate completă rezervă întreaga capacitate a resursei pentru datele de pornire și finalizare indicate. De exemplu, în cazul în care o resursă are un calendar setat să lucreze 8 ore pe zi, 5 zile pe săptămână, stabilirea unei date de început și de sfârșit care acoperă 5 zile lucrătoare rezervă resursa pentru 40 de ore. Rezervarea se face indiferent de capacitatea rămasă a resursei. În cazul în care o resursă este deja rezervată pe alte proiecte în această perioadă, cele 40 de ore sunt rezervate ca ore suplimentare, ceea ce ar putea duce la suprarezervări.

### <a name="remaining-capacity"></a><a name="remaining"></a>Capacitate rămasă
Metoda Capacitate rămasă este disponibilă numai atunci când rezervați direct un proiect utilizând Tabloul de planificare. Această metodă rezervă capacitatea disponibilă a resursei în intervalul de date specificat. De exemplu, în cazul în care o resursă are o capacitate de 40 de ore pe săptămână și a fost deja rezervată pentru 10 ore, rezervarea pentru aceeași săptămână are drept rezultat o rezervare pentru restul de 30 de ore de capacitate pentru săptămâna respectivă.

### <a name="percentage-capacity"></a><a name="percentage"></a>Capacitate procentaj
Metoda Procentaj capacitate rezervă resursa pentru un procent din capacitatea pentru datele de pornire și finalizare indicate. De exemplu, în cazul în care o resursă are un calendar setat să lucreze opt ore pe zi, cinci zile pe săptămână, stabilirea unei date de început și de sfârșit care acoperă cinci zile lucrătoare și la o capacitate de 50% va rezerva resursa pentru 20 de ore. Rezervările individuale pe zi sunt repartizate în mod egal pe întreaga perioadă, de exemplu patru ore pe zi, în acest exemplu. Rezervarea se face indiferent de capacitatea rămasă a resursei. În cazul în care o resursă este deja rezervată pe alte proiecte în această perioadă, cele 20 de ore sunt rezervate ca ore suplimentare, ceea ce ar putea duce la suprarezervări.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Ore distribuite uniform
Metoda Distribuirea uniformă a orelor rezervă resursa pentru un anumit număr de ore, distribuind timpul uniform pe zi între datele de început și sfârșit indicate. De exemplu, în cazul în care rezervați o resursă pentru 20 de ore pe o perioadă de cinci zile, această metodă distribuie cele 20 de ore în mod egal, cu câte patru ore pe zi. Rezervarea se face indiferent de capacitatea rămasă a resursei. În cazul în care o resursă este deja rezervată pe alte proiecte în această perioadă, cele 20 de ore sunt rezervate ca ore suplimentare, ceea ce ar putea duce la suprarezervări.

### <a name="front-load-hours"></a><a name="front"></a>Ore de încărcare frontală
Metoda Încărcare frontală a orelor rezervă resursa pentru un anumit număr de ore, încărcând frontal timpul pe zi între datele de început și sfârșit indicate. Încărcarea frontală consumă capacitatea disponibilă a resursei într-o ordine „primul venit, primul consumat". De exemplu, în cazul în care programul de lucru al resursei este de opt ore pe zi, cinci zile pe săptămână și aceasta nu are nicio rezervare curentă, rezervarea resursei pentru 20 de ore pe o perioadă de 5 zile lucrătoare duce la următorul model de rezervare zilnic: 

|                           |    Ziua 1    |    Ziua 2    |    Ziua 3    |    Ziua 4    |    Ziua 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Rezervări existente**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Rezervare nouă**          |    8        |    8        |    4        |    0        |    0        |    20       |

Metoda de încărcare frontală ia în considerare rezervările existente și capacitatea disponibilă. De exemplu, în cazul în care aceeași resursă are deja 20 de ore de rezervări în săptămâna de lucru, rezervările noi consumă capacitatea rămasă după cum urmează:

|                     | Ziua 1 | Ziua 2 | Ziua 3 | Ziua 4 | Ziua 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Rezervări existente** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Rezervare nouă**       | 0     | 0     | 4     | 8     | 8     | 20    |

Deoarece este luată în calcul capacitatea disponibilă, este posibil să primiți un mesaj de eroare dacă resursa nu mai are capacitate rămasă care să poată fi absorbită de rezervare. Cu această metodă, nu puteți face suprarezervări.

### <a name="none"></a><a name="none"></a>Niciunul
Metoda Niciunul este disponibilă numai atunci când rezervați din fila **Echipă** din cadrul unui proiect. Această metodă adaugă resursa ca membru al echipei la proiect, dar nu creează rezervări care să absoarbă capacitatea resursei. Această metodă este utilizată atunci când se adaugă membrul echipei care este managerul implicit de proiect atunci când este creat un proiect. Utilizatorul managerului de proiect care a creat proiectul se adaugă în mod implicit la proiect, astfel încât înregistrarea entității proiectului are un proprietar și există o persoană care aprobă pe proiect. Întrucât acest utilizator nu are rezervări, dacă doriți să rezervați resursa puteți fie să o ștergeți și apoi să o adăugați din nou folosind o metodă de alocare diferită, fie să adăugați resursa la sarcini și apoi să utilizați **Extinde rezervările** de pe fila **Reconciliere** pentru a crea rezervări pentru atribuiri.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metode de alocare care duc la suprarezervare
În concluzie, următoarele metode de alocare duc la suprarezervare dacă resursa este deja angajată în alte proiecte (sau pentru alte comenzi de lucru sau entități care pot fi planificate):

- Capacitate completă
- Capacitate procentaj
- Distribuire uniformă a orelor

Când utilizați una dintre aceste trei metode de alocare, nu veți fi notificat cu privire la faptul că resursa este suprarezervată. Pentru a corecta suprarezervarea trebuie să utilizați Tabloul de planificare.
