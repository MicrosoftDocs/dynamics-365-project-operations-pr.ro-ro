---
title: Transferarea bugetelor proiectului la sfârșitul unui exercițiu financiar
description: Acest articol oferă informații despre cum să transferați sumele bugetare rămase în anii următori și să creați detalii despre registrul bugetului.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082929"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transferarea bugetelor proiectului la sfârșitul unui exercițiu financiar

[!include [banner](../includes/banner.md)]

Când lucrați la un proiect de mai mulți ani, este posibil să aveți bugetul rămas la sfârșitul exercițiu financiar. Puteți transfera sumele bugetare rămase într-un an viitor și puteți crea detalii despre registrul bugetului pentru sumele din conturile contabile asociate. Înainte de a reporta sumele rămase, examinați și analizați sumele bugetului rămase.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Examinați și analizați sumele bugetare rămase

Parcurgeți pașii următori pentru a revizui sumele bugetare la sfârșitul anului pentru proiecte, dar nu reportați sumele.

1. Accesați **Management de proiect și contabilitate** > **Periodic** > **Bugete** > **Transferați bugete**. 
2. Pe pagina **Procesul de reportare a bugetului proiectului** , pe fila **Opțiuni de sfârșit de an** , verificați ca **Transferați sumele rămase din bugetul proiectului** să nu fie activat.
3. Pe fila **Parametrii** , în câmpul **Anul bugetar al proiectului** , selectați câmpul exercițiu financiar pentru care doriți să vedeți suma bugetului rămas. 
4. Pe câmpul **Deschiderea exercițiului financiar** selectați exercițiul financiar pentru care doriți să vedeți suma bugetului rămas. 
5. În câmpul **Din modelul de prognoză** , selectați **Buget rămas**. 
6. Pentru a include proiecte care îndeplinesc criteriile selectate și care nu au buget rămas, selectați **Arată zero rămas**.  
7. Pe fila **Selectați Bugete** , selectați **Obțineți toate bugetele** pentru a încărca toate bugetele care corespund criteriilor selectate, apoi selectați **Proces**. 
8. Pentru a proiecta o interogare de bază de date care încarcă un anumit set de bugete în panou, selectați **Preluați bugetele selectate**.

Pentru mai multe informații despre o anumită linie din panou, selectați linia, apoi selectați **Vizualizați detaliile bugetului** sau **Vizualizați conturile**.

## <a name="carry-forward-remaining-budget-amounts"></a>Transferați sumele bugetare rămase 

Când procesați sumele bugetare rămase, puteți crea tranzacții în registrul general pentru sumele pe care le reportați. Pentru a crea tranzacții contabile generale, parcurgeți pașii din secțiune, [Transferați sumele bugetare și creați tranzacții de contabilitate generală](#carry-forward). 

> [!NOTE]
> Sumele bugetare reportate sunt transferate la modelul de prognoză selectat în pagina **Modele de prognoză** ca model de prognoză de reportare.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Transferați sumele bugetare și creați tranzacții de contabilitate generală

1.  Selectați **anagement de proiect și contabilitate** > **Periodic** > **Bugete** > **Transferați bugete**. 
2. Pe pagina **Procesul de reportare a bugetului proiectului** , selectați **Sfârșit de an** , apoi activați **Transferați sumele rămase din bugetul proiectului** și **Creați înregistrări bugetare în registrul general**. 
3. Pe fila **Parametri** , în grupul de câmpuri **Parametrii proiectului** , selectați următoarele:

   - **Anul financiar al proiectului** : selectați începutul exercițiul financiar pentru care doriți să vizualizați sumele bugetului rămas. 
   - **Profit și pierdere** : creați tranzacții de profit și pierdere în registrul general. 
   -  **WIP** : Creați tranzacții Work in Progress (WIP) în registrul general.
   -  **Salarizare** : Creați tranzacții de alocare a salarizării în registrul general. 

5. În grupul de câmpuri **Registrul general** , introduceți următoarele informații: 

   - Pe câmpul **Deschiderea exercițiului financiar** selectați exercițiul financiar din care doriți să transferați sumele din bugetul rămas pentru proiecte. Valoarea implicită este la un an după valoarea din câmpul **Anul bugetar al proiectului**.
   -  În câmpul **Perioada de reportare** , selectați perioada pentru care doriți să creați detaliile registrului bugetului în registrul general. Aceasta este de obicei prima perioadă a deschiderii exercițiu financiar.

6. În grupul de câmpuri **Copiați de la/în** , introduceți următoarele informații:

   - În câmpul **Din modelul de prognoză** , selectați modelul de prognoză a bugetului proiectului asociat cu sumele bugetare rămase pe care doriți să le transferați pentru proiecte. 
   - În câmpul **La modelul registrului de buget** , selectați modelul de registru a bugetului proiectului asociat cu sumele bugetare rămase pe care doriți să le transferați în registrul general. 
   -  Selectați **Transfer valutar de vânzare** pentru a utiliza moneda de vânzări a proiectului pentru tranzacțiile din registrul general care sunt create atunci când transferați sumele bugetare pentru proiecte. Când opțiunea nu este selectată, tranzacțiile folosesc moneda contabilă. 
   -  Selectați **Arată zero rămas** pentru a include proiecte care nu au sume bugetare rămase, dar îndeplinesc celelalte criterii pe care le selectați în proiectele afișate în panoul de jos.

7. Pe fila **Selectați bugete** , selectați **Regăsiți toate bugetele** pentru a încărca toate bugetele care se potrivesc cu criteriile selectate. Dacă preferați să proiectați o interogare de bază de date care încarcă un anumit set de bugete de proiect în panou, selectați **Preluați bugetele selectate**.
8. Pentru fiecare proiect pe care doriți să îl procesați, selectați opțiunea de la începutul liniei pentru proiect.

    > [!TIP]
    > Pentru a selecta toate sau majoritatea proiectelor, selectați bifa în colțul din stânga sus al colțului. Pentru a exclude procesarea oricărui proiect, debifați bifa pentru proiectul respectiv.

9. Pentru a transfera sumele bugetului rămase pentru proiectele selectate în exercițiu financiar selectat și a crea detalii despre registrul bugetului în registrul general, selectați **Proces**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Transferați sumele bugetare fără să creați tranzacții de registru general

1. Accesați **Management de proiect și contabilitate** > **Periodic** > **Bugete** > **Transferați bugete**.
2. Pe pagina **Procesul de reportare a bugetului proiectului** , în câmpul **Opțiuni de sfârșit de an** , selectați **Transferați sumele rămase din bugetul proiectului**.
3. În grupul **Parametrii** , în câmpul **Anul bugetar al proiectului** , selectați câmpul exercițiu financiar pentru care doriți să vedeți sumele rămase în buget.
4. În grupul de câmpuri **Copiați de la/în** , furnizați următoarele informații:

   - În câmpul **Din modelul de prognoză** , selectați modelul de prognoză a bugetului proiectului care este asociat cu sumele bugetare rămase pe care doriți să le transferați pentru proiecte. 
   - Pentru a include proiecte care nu au buget rămas, dar care îndeplinesc celelalte criterii pe care le-ați selectat, selectați **Arată zero rămas**.
   - În grupul **Selectați bugete** , selectați **Regăsiți toate bugetele** pentru a încărca toate bugetele care se potrivesc cu criteriile pe care le-ați selectat. Pentru a proiecta o interogare de bază de date care încarcă un anumit set de bugete de proiect în panou, selectați **Preluați bugetele selectate**.

5. Pentru fiecare proiect pe care doriți să îl procesați, selectați opțiunea de la începutul liniei pentru proiect. 
6. Selectați **Proces** pentru a transfera sumele bugetare rămase pentru proiectele selectate în exercițiu financiar selectat.

