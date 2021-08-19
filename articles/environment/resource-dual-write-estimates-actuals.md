---
title: Estimări de proiect și integrarea reală
description: Acest subiect oferă informații despre integrarea cu scriere duală a Project Operations pentru estimări și date reale ale proiectului.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006306"
---
# <a name="project-estimates-and-actuals-integration"></a>Estimări de proiect și integrarea reală

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect oferă informații despre integrarea cu scriere duală a Project Operations pentru estimări și date reale ale proiectului.

## <a name="project-estimates"></a>Estimări de proiect

Munca pe proiect, cheltuielile și estimările materiale sunt create și menținute în Microsoft Dataverse și sincronizate cu aplicații Finance and Operations în scopuri contabile. Operațiile de creare, actualizare și ștergere nu sunt acceptate prin aplicații Finance and Operations.

Crearea estimărilor necesită o configurație contabilă validă de proiect. Proiectele care sunt asociate cu liniile contractuale trebuie să aibă un profil valid de cost și venituri de proiect definit în regulile profilului de cost și de venit al proiectului. Pentru mai multe informații, consultați [Configurarea contabilității pentru proiectele facturabile](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimări ale forței de muncă

Estimările de forță de muncă sunt create de managerul de proiect sau de managerul de resurse care atribuie, de asemenea, o resursă generică sau denumită sarcinii proiectului. Înregistrările de alocare a resurselor pot fi revizuite pe fila **Atribuiri de resurse** de pe pagina **detaliile proiectului** în Dataverse. Înregistrările de alocare a resurselor în Dataverse creează înregistrări de estimări orare în aplicații Finance and Operations folosind **Entitate de integrare Project Operations pentru estimări orare (msdyn\_resourceassignments)**.

   ![Integrarea estimărilor de manoperă.](./Media/DW4LaborEstimates.png)

Scrierea duală sincronizează înregistrările de alocare a resurselor la tabelul de etapizare (**ProjCDSEstimateHoursImport**) și apoi folosește logica de business pentru a crea și actualiza înregistrările de estimări orare (**ProjForecastEmpl**).

Contabilul de proiect analizează înregistrările estimărilor orare create în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Toate proiectele** > **Plan** > **Estimări orare**.

## <a name="expense-estimates"></a>Estimări de cheltuieli

Estimările cheltuielilor sunt create de managerul de proiect pe fila **Estimări de cheltuieli** de pe pagina **Detalii proiect** în Dataverse. Înregistrările de estimare a cheltuielilor sunt stocate în entitatea **Linie estimată** în Dataverse. Aceste înregistrări estimative au clasa de tranzacție **Cheltuieli** și sunt sincronizate cu înregistrările de estimare a cheltuielilor în aplicații Finance and Operations utilizând **Entitate de integrare Project Operations pentru estimări de cheltuieli (msdyn\_estimatelines)**.

   ![Integrarea estimărilor cheltuielilor.](./Media/DW4ExpenseEstimates.png)

Scrierea duală sincronizează înregistrările de estimări ale cheltuielilor la tabelul de etapizare, **ProjCDSEstimateExpenseImport** și apoi folosește logica de business pentru a crea și actualiza înregistrările de estimări de cheltuieli (**ProjForecastCost**). Liniile estimate estimează vânzările și înregistrările de estimări ale costurilor separat. Logica de afaceri în aplicații Finance and Operations completează o singură înregistrare de estimare a cheltuielilor utilizând acest detaliu în tabelul de etapizare.

Contabilul de proiect poate analiza înregistrările de cheltuieli orare create în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Toate proiectele** > **Plan** > **Estimări cheltuieli**.

## <a name="material-estimates"></a>Estimări materiale

Estimările materiale sunt create de managerul de proiect pe fila **Estimări de materiale** de pe pagina **Detalii proiect** în Dataverse. Înregistrările de estimare a materialelor sunt stocate în entitatea **Linie estimată** în Dataverse. Aceste înregistrări estimative au clasa de tranzacție **Material** și sunt sincronizate cu înregistrările de estimare a elementelor în aplicații Finance and Operations utilizând **Tabelul de integrare de proiect pentru estimări de materiale (msdyn\_estimatelines)**.

   ![Integrarea estimărilor de material.](./Media/DW4MaterialEstimates.png)

Scrierea duală sincronizează înregistrările de estimări de materiale la tabelul de etapizare **ProjForecastSalesImpor**, și apoi folosește logica de business pentru a crea și actualiza înregistrările de estimări de elemente (**ForecastSales**). Liniile estimate estimează vânzările și înregistrările de estimări ale costurilor separat. Logica de afaceri în aplicații Finance and Operations completează o singură înregistrare de estimare de elemente utilizând acest detaliu în tabelul de etapizare.

Contabilul de proiect poate analiza înregistrările de elemente orare create în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Toate proiectele** > **Plan** > **Estimări elemente**.

## <a name="project-actuals"></a>Date reale ale proiectului

Datele reale de proiect sunt create în Dataverse, pe baza timpului, cheltuielilor, materialului și activității de facturare. Toate atributele operaționale ale acestor tranzacții, inclusiv cantitatea, prețul de cost, prețul de vânzare și proiectul sunt capturate în această entitate Dataverse. Pentru mai multe informații, [Date reale](../actuals/actuals-overview.md). Înregistrările reale sunt sincronizate cu aplicații Finance and Operations folosind harta de tabel cu scriere duală **Integrare valori reale Project Operations (msdyn\_actuals)** pentru contabilitatea din aval.

   ![Integrarea valorilor reale.](./Media/DW4Actuals.png)

Harta de tabel **Integrare valori reale Project Operations** sincronizează toate înregistrările din entitatea **Date reale** în Dataverse, cu atributul **Omitere sincronizare (numai pentru un intern)** setat la **Fals**. Această valoare a atributului este setată automat în Dataverse la crearea înregistrării. Exemple în care acest atribut este setat la **True** sunt:

  - Valori reale ale costului de proiect pentru tranzacțiile între companii. Pentru mai multe informații, consultați [Creați tranzacții între companii](../project-accounting/create-intercompany-transactions.md). Aceste înregistrări sunt omise deoarece sistemul recreează costul real de proiect în aplicații Finance and Operations atunci când este postată factura furnizorului între companii.
  - Înregistrări negative de vânzări nefacturate create la confirmarea facturii proforma. Aceste înregistrări sunt omise, deoarece subregistrul proiectului în aplicații Finance and Operations nu inversează înregistrarea de vânzări nefacturate la facturare, dar schimbă starea în facturare completă.

Harta de tabel cu scriere dublă sincronizează înregistrările reale cu tabelul de etapizare **ProjCDSActualsImport**. Aceste înregistrări sunt procesate prin procesul periodic **Importați din tabelul de etapizare** la crearea liniilor de jurnal de integrare Project Operations și a liniilor de propunere de factură de proiect. Pentru mai multe informații, consultați [Jurnal de integrare în Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse captează, de asemenea, legăturile dintre tranzacțiile efective de proiect în entitatea **Conexiune de tranzacție**. Pentru mai multe informații, consultați: [Conectarea datelor reale la înregistrările originale](../actuals/linkingactuals.md). Legăturile dintre tranzacțiile reale sunt, de asemenea, sincronizate cu aplicații Finance and Operations care utilizează harta tabelului cu scriere duală, **Entitate de integrare pentru relațiile de tranzacție de proiect (msdyn\_transactionconnections)**. Aceste înregistrări sunt utilizate prin procesul periodic, **Importați din tabelul de etapizare** la crearea liniilor de jurnal de integrare Project Operations și a liniilor de propunere de factură de proiect.

Postarea unui jurnal de integrare Project Operations și a unei propuneri de facturi pentru proiect declanșează o actualizare în înregistrările respective din tabelul de etapizare **ProjCDSActualsImport**. Sistemul captează și înregistrează următoarele atribute contabile pentru tranzacțiile reale:

- Valoarea monedei contabile
- Curs de schimb
- Număr voucher
- Valoare impozit pe vânzări

Harta tabelului **Integrare valori reale Project Operations** actualizează înregistrările de date reale respective în Dataverse cu aceste informații.
