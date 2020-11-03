---
title: Prezentare generală a reconcilierii resurselor
description: Acest subiect oferă informații despre asigurarea că rezervările de resurse și atribuirile proiectelor sunt aliniate.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082738"
---
# <a name="resource-reconciliation-overview"></a>Prezentare generală a reconcilierii resurselor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pentru membrii echipei, rezervările și atribuirile sunt cuplate lejer. Cu alte cuvinte, resursele pot avea misiuni, dar nu rezervări, sau pot avea rezervări, dar nu atribuiri. În mod ideal, rezervările și atribuirile ar trebui aliniate, astfel încât resursele au o capacitate angajată de a realiza activitățile atribuite. Cu toate acestea, rezervările s-ar putea să se bazeze pe disponibilitate, iar timpii de activitate s-ar putea modifica pe măsură ce proiectul continuă. Prin urmare, cuplarea lejeră a rezervărilor și atribuirilor furnizează flexibilitate.

Fila **Reconciliere** de pe formularul **Proiect** care permite managerilor de proiect să reconcilieze rezervările membrilor echipei și atribuirile lor pentru echipele de proiect.

Fila **Reconciliere** afișează și rezervările și atribuirile până la nivelul atribuirii individuale a activității pentru fiecare membru al echipei. Orele sunt afișate în celule care pot reprezenta perioade de timp de la luni până la zile.

Fila afișează, de asemenea, un total net global pentru proiect, împreună cu o coloană de **Total**.

Pentru fiecare resursă, fila calculează diferența dintre rezervările membrului echipei pe proiect și un cumulul al atribuirilor de activități ale acelui membru al echipei. În mod ideal, această diferență ar trebui să fie 0 (zero). Cu alte cuvinte, nu ar trebui să existe nicio diferență între rezervări și atribuiri. Diferențele sunt colorate și umbrite pentru a atrage atenția asupra a două condiții:

- **Deficit de rezervare** - un deficit de rezervare apare atunci când o resursă are mai multe atribuiri decât rezervări. Deoarece această capacitate nu a fost rezervată, un manager de proiect ar putea vrea să corecteze această condiție extinzând rezervările resursei pentru a acoperi deficitul.
- **Rezervări în exces** – rezervările în exces apar atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților. Această condiție ar putea fi acceptabilă în cazurile în care resursa a fost rezervată la proiect înainte să aibă loc atribuirea activității. Cu toate acestea, în alte cazuri, resursa nu este planificată să fie atribuită activităților. În aceste cazuri, managerul de proiect ar trebui să ia în considerare anularea rezervările resursei, astfel încât capacitatea să poată fi utilizată pentru un alt proiect.

În unele cazuri, când vizualizați timpul la un nivel mai înalt decât nivelul zilei (de exemplu, nivelul lunii), este posibil să vedeți o diferență netă de zero pentru o resursă (cu alte cuvinte, rezervări = misiuni). Cu toate acestea, dacă vă uitați la nivel de săptămână, este posibil să vedeți că există atribuiri de zero ore și rezervări de 40 ore în prima săptămână, dar atribuiri de 40 ore și rezervări de zero ore în a doua săptămână. În general, rezervările și atribuirile sunt reconciliate, dar acestea diferă de la o săptămână la alta.

Când vizualizați timpul la nivele mai înalte, celulele din fila **Reconciliere** au un indicator pentru a vă informa că sunt diferențe la niveluri mai joase. Făcând dublu clic într-o celulă, aveți posibilitatea să măriți pentru a vizualiza diferența. Apoi puteți face clic dreapta pentru a micșora. Selectând o resursă și apoi utilizând controlul **Următoarea diferență** pe grila barei de instrumente, puteți trece la următoarea diferență dintre rezervări și atribuiri pentru acea resursă. Apoi puteți utiliza controlul **Diferenței anterioare** pentru a reveni. De asemenea, puteți dezactiva indicatorul de diferență și comportamentul de navigare sub **Setări**.


DAcă aveți atribuiri de activități pentru o resursă dar nu rezervări pe pagina **Proiecte** , pe fila **Reconciliere** , selectați deficitul de rezervare și apoi selectați **Extindeți rezervarea**. Apare caseta de dialog **Extindere rezervare** și afișează rezervarea necesară pentru a aborda deficitul resursei. De asemenea, arată rezervările existente ale resursei în toate proiectele sau alte entități care pot fi planificate. Dacă selectați **OK** pentru a crea rezervarea pentru resursă, indiferent de disponibilitatea acelei resurse, este posibil să cauzați o suprarezervare.

Managerul de proiect sau managerul de resurse pot utiliza apoi Panoul de planificare pentru a gestiona orice situații în care o resursă este suprarezervată peste capacitate.

