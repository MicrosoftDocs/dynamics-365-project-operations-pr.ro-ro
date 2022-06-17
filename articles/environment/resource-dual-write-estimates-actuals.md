---
title: Estimări de proiect și integrarea reală
description: Acest articol oferă informații despre integrarea cu dublă scriere a Project Operations pentru estimări și valori reale ale proiectului.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 43c868b051bf141cfc3211669c0a44333b4b2c65
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914601"
---
# <a name="project-estimates-and-actuals-integration"></a>Estimări de proiect și integrarea reală

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol oferă informații despre integrarea cu dublă scriere a Project Operations pentru estimări și valori reale ale proiectului.

## <a name="project-estimates"></a>Estimări de proiect

Estimările privind forța de muncă, cheltuielile și materialele din proiect sunt create și menținute în Microsoft Dataverse și sincronizat cu aplicațiile Finanțe și Operațiuni în scopuri contabile. Operațiunile de creare, actualizare și ștergere nu sunt acceptate prin aplicațiile Finanțe și Operațiuni.

Crearea estimărilor necesită o configurație contabilă validă de proiect. Proiectele care sunt asociate cu liniile contractuale trebuie să aibă un profil valid de cost și venituri de proiect definit în regulile profilului de cost și de venit al proiectului. Pentru mai multe informații, consultați [Configurarea contabilității pentru proiectele facturabile](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimări ale forței de muncă

Estimările de forță de muncă sunt create de managerul de proiect sau de managerul de resurse care atribuie, de asemenea, o resursă generică sau denumită sarcinii proiectului. Înregistrările de alocare a resurselor pot fi revizuite pe fila **Atribuiri de resurse** de pe pagina **detaliile proiectului** în Dataverse. Alocarea resurselor înregistrează în Dataverse creați înregistrări de prognoză oră în aplicațiile Finanțe și Operațiuni folosind **Entitate de integrare Project Operations pentru estimări de oră (msdyn\_ alocări de resurse)**.

   ![Integrarea estimărilor de manoperă.](./Media/DW4LaborEstimates.png)

Scrierea duală sincronizează înregistrările de alocare a resurselor la tabelul de etapizare (**ProjCDSEstimateHoursImport**) și apoi folosește logica de business pentru a crea și actualiza înregistrările de estimări orare (**ProjForecastEmpl**).

Contabilul proiectului examinează înregistrările orelor de prognoză create în aplicațiile Finanțe și operațiuni accesând **Management de proiect si contabilitate** > **Toate proiectele** > **Plan** > **Prognoze orare**.

## <a name="expense-estimates"></a>Estimări de cheltuieli

Estimările cheltuielilor sunt create de managerul de proiect pe fila **Estimări de cheltuieli** de pe pagina **Detalii proiect** în Dataverse. Înregistrările de estimare a cheltuielilor sunt stocate în entitatea **Linie estimată** în Dataverse. Aceste înregistrări de estimare au clasa de tranzacție, **Cheltuiala** și sunt sincronizate cu înregistrările de prognoză a cheltuielilor din aplicațiile Finanțe și Operațiuni folosind **Entitate de integrare Project Operations pentru estimări de cheltuieli (msdyn\_ estimări)**.

   ![Integrarea estimărilor cheltuielilor.](./Media/DW4ExpenseEstimates.png)

Scrierea duală sincronizează înregistrările de estimări ale cheltuielilor la tabelul de etapizare, **ProjCDSEstimateExpenseImport** și apoi folosește logica de business pentru a crea și actualiza înregistrările de estimări de cheltuieli (**ProjForecastCost**). Liniile estimate estimează vânzările și înregistrările de estimări ale costurilor separat. Logica de afaceri din aplicațiile Finanțe și operațiuni populează o singură înregistrare de prognoză a cheltuielilor folosind acest detaliu din tabelul de punere în pas.

Contabilul de proiect poate examina înregistrările privind prognoza cheltuielilor în aplicațiile Finanțe și operațiuni, accesând **Management de proiect si contabilitate** > **Toate proiectele** > **Plan** > **Previziunile de cheltuieli**.

## <a name="material-estimates"></a>Estimări materiale

Estimările materiale sunt create de managerul de proiect pe fila **Estimări de materiale** de pe pagina **Detalii proiect** în Dataverse. Înregistrările de estimare a materialelor sunt stocate în entitatea **Linie estimată** în Dataverse. Aceste înregistrări de estimare au clasa de tranzacție, **Material** și sunt sincronizate cu înregistrările de prognoză a articolelor din aplicațiile Finance and Operations folosind **Tabel de integrare a proiectelor pentru estimări de materiale (msdyn\_ estimări)**.

   ![Integrarea estimărilor de material.](./Media/DW4MaterialEstimates.png)

Scrierea duală sincronizează înregistrările de estimări de materiale la tabelul de etapizare **ProjForecastSalesImpor**, și apoi folosește logica de business pentru a crea și actualiza înregistrările de estimări de elemente (**ForecastSales**). Liniile estimate estimează vânzările și înregistrările de estimări ale costurilor separat. Logica de afaceri din aplicațiile Finanțe și operațiuni populează o singură înregistrare de prognoză a articolului folosind acest detaliu din tabelul de punere în pas.

Contabilul de proiect poate examina înregistrările de prognoză a articolelor din aplicațiile Finanțe și operațiuni, accesând **Management de proiect si contabilitate** > **Toate proiectele** > **Plan** > **Previziunile articolului**.

## <a name="project-actuals"></a>Date reale ale proiectului

Datele reale de proiect sunt create în Dataverse, pe baza timpului, cheltuielilor, materialului și activității de facturare. Toate atributele operaționale ale acestor tranzacții, inclusiv cantitatea, prețul de cost, prețul de vânzare și proiectul sunt capturate în această entitate Dataverse. Pentru mai multe informații, [Date reale](../actuals/actuals-overview.md). Înregistrările reale sunt sincronizate cu aplicațiile Finance and Operations folosind harta tabelului cu dublă scriere **Date reale de integrare a operațiunilor de proiect (msdyn\_ reale)** pentru contabilitatea din aval.

   ![Integrarea valorilor reale.](./Media/DW4Actuals.png)

Harta de tabel **Integrare valori reale Project Operations** sincronizează toate înregistrările din entitatea **Date reale** în Dataverse, cu atributul **Omitere sincronizare (numai pentru un intern)** setat la **Fals**. Această valoare a atributului este setată automat în Dataverse la crearea înregistrării. Exemple în care acest atribut este setat la **True** sunt:

  - Valori reale ale costului de proiect pentru tranzacțiile între companii. Pentru mai multe informații, consultați [Creați tranzacții între companii](../project-accounting/create-intercompany-transactions.md). Aceste înregistrări sunt omise, deoarece sistemul recreează costul real al proiectului în aplicațiile Finanțe și operațiuni atunci când este înregistrată factura furnizorului intercompanii.
  - Înregistrări negative de vânzări nefacturate create la confirmarea facturii proforma. Aceste înregistrări sunt omise deoarece registrul secundar al proiectului din aplicațiile Finanțe și operațiuni nu inversează înregistrarea vânzărilor nefacturate la facturare, ci schimbă starea în facturare completă.

Harta de tabel cu scriere dublă sincronizează înregistrările reale cu tabelul de etapizare **ProjCDSActualsImport**. Aceste înregistrări sunt procesate prin procesul periodic **Importați din tabelul de etapizare** la crearea liniilor de jurnal de integrare Project Operations și a liniilor de propunere de factură de proiect. Pentru mai multe informații, consultați [Jurnal de integrare în Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse captează, de asemenea, legăturile dintre tranzacțiile efective de proiect în entitatea **Conexiune de tranzacție**. Pentru mai multe informații, consultați: [Conectarea datelor reale la înregistrările originale](../actuals/linkingactuals.md). Legăturile dintre tranzacțiile reale sunt, de asemenea, sincronizate cu aplicațiile Finanțe și Operațiuni folosind harta tabelului cu dublă scriere, **Entitate de integrare pentru relațiile de tranzacții ale proiectului (msdyn\_ conexiuni de tranzacție)**. Aceste înregistrări sunt utilizate prin procesul periodic, **Importați din tabelul de etapizare** la crearea liniilor de jurnal de integrare Project Operations și a liniilor de propunere de factură de proiect.

Postarea unui jurnal de integrare Project Operations și a unei propuneri de facturi pentru proiect declanșează o actualizare în înregistrările respective din tabelul de etapizare **ProjCDSActualsImport**. Sistemul captează și înregistrează următoarele atribute contabile pentru tranzacțiile reale:

- Valoarea monedei contabile
- Curs de schimb
- Număr voucher
- Valoare impozit pe vânzări

Harta tabelului **Integrare valori reale Project Operations** actualizează înregistrările de date reale respective în Dataverse cu aceste informații.
