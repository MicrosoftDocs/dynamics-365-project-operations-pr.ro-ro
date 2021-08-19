---
title: Prognoze și bugete de proiect
description: Microsoft Dynamics 365 Finance oferă prognozele proiectului și bugetele proiectului pentru a vă gestiona și controla proiectele.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47ea4c49a76a2bb0a1855fce2e9a874b4044e429d963c08392ec0ab471f89329
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988081"
---
# <a name="project-forecasts-and-budgets"></a>Prognoze și bugete de proiect

[!include [banner](../includes/banner.md)]

Există două modalități de a vă gestiona și controla proiectele: prognozele proiectului și bugetele proiectului. 

Utilizați prognozele proiectului dacă organizația dvs. are o perspectivă operațională, dacă și se concentrează pe veniturile și costurile care sunt derivate din tranzacții specifice. Folosiți alocarea bugetului proiectului dacă organizația dvs. se concentrează mai mult pe sume financiare. 

Atât prognozele de proiect, cât și bugetele de proiect utilizează modele de prognoză pentru a reține sumele tranzacției proiectate. 

Fiecare metodă are avantajele sale. Trebuie să luați în considerare următoarele puncte înainte de a selecta o metodă pentru organizația dvs.

|   Metodă de alocare       |           Prognoza proiectului            |        Bugetul proiectului                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Alocarea perioadei**     | Nu puteți aloca în mod explicit tranzacțiile pentru o perioadă fiscală. În schimb, prognoza și controlul prognozei se bazează pe durata proiectului. Deoarece prognozele se bazează pe o anumită dată, trebuie să deduceți perioada din data respectivă. | Nu puteți aloca tranzacțiile pentru tot proiectul sau o perioadă fiscală. Dacă alocați pentru o perioadă, puteți transfera sumele neutilizate înainte la următoarea perioadă fiscală. |
| **Vizualizarea tranzacțiilor**  | Puteți vizualiza tranzacțiile în formularele de prognoză, unde vedeți prognozele pentru întreaga companie și pentru toate proiectele, indiferent de ierarhie. Pentru a vă concentra asupra unui anumit proiect, trebuie să filtrați datele.                                       | Puteți vizualiza tranzacții bugetate pentru o singură ierarhie de proiect. Prin urmare, puteți vizualiza detaliile tranzacției pentru un proiect principal sau pentru subproiectele acestuia.                 |
| **Variabile de tranzacție** | Când introduceți tranzacții prognozate, puteți utiliza fiecare atribut care există pentru o tranzacție reală. Acest lucru permite detalii mai mari în prognoză. De exemplu, puteți introduce detalii pentru cantități, angajați, articole sau proprietăți de linie.         | Când introduceți detalii despre buget, puteți utiliza numai sume, categorii și activități.                    |
| **Securitate**              | Prognoza se bazează pe tranzacțiile pe care le introduceți în formularele de prognoză și nu implică niciun mecanism de control al procesului. Orice angajat care are permisiuni pentru un formular de prognoză poate revizui informațiile fără aprobare.                                        | Stabilirea bugetului utilizează sistemul fluxului de lucru, care permite gestionarea modificărilor și vă permite să păstrați un istoric al reviziilor.         |
| **Tipuri de intrări**           | Intrările de tranzacție din prognoză se bazează pe numărul de unități, și pe prețurile unitare de cost și vânzare.  | Detaliile bugetului se bazează pe sume, care sunt împărțite între costuri și venituri.                                          |
| **Modele de prognoză**       | Deoarece fiecare prognoză trebuie să fie asociată cu un model, puteți crea mai multe modele de prognoză și puteți configura și submodele.           | Stabilirea bugetului proiectului limitează modelele de prognoză care sunt utilizate pentru bugetare. Mai puține modele de prognoză pot contribui la creșterea consecvenței în proiecții.                           |
| **Depășiri de costuri**         | Puteți doar permite sau interzice introducerea tranzacțiilor care vor provoca o depășire a costurilor.   | Stabilirea bugetului proiectului oferă opțiuni suplimentare de control pentru utilizatori. Puteți permite avertismente și depășiri.                    |
| **Control**               | Controlul prognozei se realizează utilizând reducerea prognozei. Sumele efective sunt scăzute din soldurile tranzacțiilor prognozate fără niciun jurnal de audit. Acest lucru poate face mai dificilă urmărirea locului în care au avut loc tranzacțiile reale.                   | În controlul bugetului proiectului, sumele efective sunt scăzute din sumele din bugetul rămas. Acest lucru permite un jurnal de audit mai clar.                                   |

## <a name="project-forecasts"></a>Prognozele proiectului
Când utilizați prognoza de proiect, puteți introduce tranzacțiile de prognoză în formularele de prognoză pentru fiecare tip de tranzacție. Fiecare atribut ce este disponibil pentru o tranzacție reală poate fi utilizat pentru o tranzacție prognozată - de exemplu, profitabilitatea liniei, atributele liniei, angajații sau descrierile. De asemenea, puteți proiecta la cât timp după ce suportați un cost, veți factura un client. 

Tranzacțiile de prognozare a proiectelor se bazează pe unități și sume. 

Trebuie să asociați fiecare prognoză de proiect cu un model de prognoză. Când introduceți o tranzacție de prognoză, este sugerat automat un model de prognoză. Modelul de prognoză acționează ca un container pentru tranzacțiile prognozate. 

Puteți desemna modele de prognoză ca submodele pentru un model. Acest lucru vă permite să prognozați în funcție de regiune, perioadă de timp sau departament. Puteți copia tranzacțiile prognozate într-un model pentru a crea un model nou și puteți, de asemenea, să transferați tranzacțiile în registrul general. Deoarece există o relație unu-la-unu între o prognoză și un model, fiecare model de prognoză alcătuiește un buget separat pentru un proiect. 

Modelele de prognoză pot utiliza reducerea prognozei ca mecanism de control pentru proiecte. În reducerea prognozei, tranzacțiile reale reduc soldurile tranzacțiilor prognozate. Cu toate acestea, deoarece reducerea prognozei se aplică celui mai înalt proiect din ierarhie, aceasta oferă o imagine limitată a modificărilor din prognoză. De exemplu, dacă un angajat este asociat cu un subproiect, tranzacțiile reale pentru angajat sunt înregistrate în proiectul principal. Acest lucru poate face dificilă urmărirea modificărilor, deoarece nu puteți determina cu ușurință ce tranzacție și în care subproiect a cauzat o reducere a sumei prognozate. Prin urmare, este o idee bună să creați o copie a unui model de prognoză pentru a fi utilizat de reducerea prognozei. Puteți utiliza apoi rapoarte pentru a vizualiza ceea ce a fost prognozat inițial. 

Puteți să revizuiți, copiați, ștergeți sau să transferați prognozele de proiect într-un buget de registru general. Cu toate acestea, nu există un control al procesului. Orice angajat care are permisiunea pentru un formular de prognoză poate efectua revizii fără recenzie.

-   **Revizuire** - Puteți revizui o tranzacție prognozată în aceleași formulare în care au fost făcute intrările originale.
-   **Copiere sau ștergere** - Când copiați tranzacțiile de prognoză, copiați liniile de tranzacție ale unui model de prognoză pe un alt model de prognoză. Când ștergeți o prognoză, ștergeți tranzacțiile de prognoză dintr-un model de prognoză. Pentru a limita tranzacțiile prognozate care sunt copiate sau șterse, selectați anumite tipuri de tranzacții și date. Aceasta vă permite să copiați sau să ștergeți numai anumite părți ale unei prognoze.
-   **Transfer** - Când transferați o prognoză de proiect către un buget de registru general, transferați tranzacțiile de prognoză ale unui model de prognoză către un buget de registru general. Puteți suprascrie orice tranzacții transferate anterior în bugetul de registru general în care transferați prognoza de proiect.

## <a name="project-budgets"></a>Bugete de proiect
Stabilirea bugetului proiectelor este o metodă mai simplă decât prognozarea, deși se integrează cu modelele de prognoză. Folosește un singur formular de intrare pentru detalii și revizuiri originale ale bugetului și permite proiecții care se bazează numai pe sumă, categorie sau activitate. 

În stabilirea bugetului proiectului, toate bugetele și reviziile originale trebuie trimise către un flux de lucru al proiectului pentru aprobare. Fluxurile de lucru vă oferă un control sporit asupra procesului și creează o înregistrare a istoricului modificărilor. 

Stabilirea bugetului proiectului seamănă cu bugetul registrului general, dar este mai rapidă și mai ușor de configurat. Multe dintre opțiunile din bugetul registrului general, cum ar fi secvențele numerice sau moneda, nu trebuie să fie configurate separat pentru proiecte.

Bugetele proiectului sunt asociate automat cu două modele de prognoză, unul pentru bugetul inițial și unul pentru bugetul rămas. Prin urmare, rapoartele care se bazează pe modele de prognoză pot utiliza date bugetare. Atunci când un buget de proiect este angajat, sistemul creează tranzacții prognozate pe baza modelelor asociate, care sunt utilizate în scopuri de raportare și control.

## <a name="forecast-models"></a>Modele de prognoză
Modelele de prognoză au o ierarhie cu un singur strat. Aceasta înseamnă că un proiect de prognoză trebuie asociat cu un singur model de prognoză.

Dacă utilizați prognozarea proiectului, puteți identifica modelele ca submodele. Puteți apoi să creați prognoze în funcție de departament, perioadă de timp sau regiune. De exemplu, puteți crea un model de prognoză pentru un an și apoi puteți crea submodele pentru previziunile regionale de nord-est, sud-est, nord-vest și sud-vest pe care le transmit șefii regionali. Selectând diferite opțiuni în rapoartele disponibile, puteți vizualiza informații în funcție de prognoza totală sau de submodel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]