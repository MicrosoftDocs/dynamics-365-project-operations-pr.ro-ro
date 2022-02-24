---
title: Prezentare generală a reconcilierii resurselor
description: Acest subiect oferă informații care vă vor ajuta să vă asigurați că rezervările de resurse și alocările pentru proiecte sunt armonizate.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8723cfad1e7cd07774e37023c5427b0a5833a554
ms.sourcegitcommit: cffc84187007b34211c90babef8af5152d4d92ea
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/12/2021
ms.locfileid: "4849639"
---
# <a name="resource-reconciliation-overview"></a>Prezentare generală a reconcilierii resurselor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pentru membrii echipei, rezervările și atribuirile sunt cuplate lejer. Cu alte cuvinte, resursele pot avea misiuni, dar nu rezervări, sau pot avea rezervări, dar nu misiuni. În mod ideal, rezervările și atribuirile ar trebui aliniate, astfel încât resursele au o capacitate angajată de a realiza activitățile atribuite. Cu toate acestea, rezervările s-ar putea să se bazeze pe disponibilitate, iar timpii de activitate s-ar putea modifica pe măsură ce proiectul continuă. Prin urmare, cuplarea lejeră a rezervărilor și atribuirilor furnizează flexibilitate.

Fila **Reconciliere** de pe pagina **Proiecte** le permite managerilor de proiect să reconcilieze rezervările membrilor echipei și misiunile lor pentru echipele de proiect.

Fila **Reconciliere** afișează rezervările și atribuirile până la nivelul atribuirii individuale a activității pentru fiecare membru al echipei. Orele sunt arătate în celule, care reprezintă perioade de luni până la zile. Fila afișează, de asemenea, un total net global pentru proiect, împreună cu o coloană de **Total**.

Pentru fiecare resursă, fila **Reconciliere** calculează diferența dintre rezervările unui membru al echipei și un cumulul al atribuirilor de activități ale acelui membru al echipei. În mod ideal, această diferență ar trebui să fie 0 (zero). Cu alte cuvinte, nu ar trebui să existe nicio diferență între rezervări și atribuiri. Diferențele sunt colorate și umbrite pentru a atrage atenția asupra a două condiții:

- **Deficit de rezervare** - un deficit de rezervare apare atunci când o resursă are mai multe atribuiri decât rezervări. Deoarece capacitatea nu a fost rezervată, managerul de proiect ar putea dori să corecteze această condiție extinzând rezervările resursei pentru a acoperi deficitul.
- **Rezervări în exces** – rezervările în exces apar atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților. Această condiție ar putea fi acceptabilă în cazurile în care resursa a fost rezervată la proiect înainte să aibă loc atribuirea sarcinii. Cu toate acestea, în alte cazuri, în care nu există un plan de atribuire a resursei la sarcini, managerul de proiect ar trebui să ia în considerare anularea rezervărilor pentru resursă. În acest fel, capacitatea poate fi utilizată pentru un alt proiect.

În unele cazuri, când vizualizați timpul la un nivel mai înalt decât nivelul zilei (de exemplu, nivelul lunii), este posibil să vedeți o diferență netă de zero pentru o resursă (cu alte cuvinte, rezervări egale cu misiuni). Cu toate acestea, dacă vă uitați la nivel de săptămână, este posibil să vedeți că există atribuiri de zero ore și rezervări de 40 ore în prima săptămână, dar atribuiri de 40 ore și rezervări de zero ore în a doua săptămână. În general, rezervările și atribuirile sunt reconciliate, dar acestea diferă de la o săptămână la alta.

Când vizualizați timpul la nivele mai înalte, celulele de pe fila **Reconciliere** au un indicator pentru a vă informa că sunt diferențe la niveluri mai joase. Apăsând de două ori sau făcând dublu clic într-o celulă, aveți posibilitatea să măriți pentru a vizualiza diferența. Apoi puteți selecta și ține apăsat (sau clic dreapta) pentru a micșora. Selectând o resursă și apoi utilizând comanda **Următoarea diferență** pe bara de instrumente a grilei, puteți trece la următoarea diferență dintre rezervări și atribuiri pentru acea resursă. Apoi puteți utiliza controlul **Diferenței anterioare** pentru a reveni. De asemenea, puteți dezactiva indicatorul de diferență și comportamentul de navigare sub **Setări**.

DAcă aveți atribuiri de activități pentru o resursă dar nu rezervări, selectați deficitul de rezervare pe fila **Reconciliere** de pe pagina **Proiecte**, apoi selectați **Extindeți rezervarea**. Caseta de dialog **Extindere rezervare** care apare afișează rezervarea care este necesară pentru a aborda deficitul resursei. Caseta de dialog arată și rezervările existente ale resursei în toate proiectele sau alte entități care pot fi planificate. Dacă selectați **OK** pentru a crea rezervarea pentru resursă, indiferent de disponibilitatea acelei resurse, este posibil să cauzați o suprarezervare.

Rezervările care sunt create prin acțiunea **Extindeți rezervarea** sunt asociate cu cerința principală a proiectului. Când este inițiată o extensie, cerința specifică care trebuie extinsă nu poate fi determinată, deoarece resursa ar putea fi asociată cu mai mult de o cerință pentru proiect.

Managerul de proiect sau managerul de resurse poate utiliza apoi Panoul de planificare pentru a gestiona orice situații în care o resursă este suprarezervată peste capacitate.
