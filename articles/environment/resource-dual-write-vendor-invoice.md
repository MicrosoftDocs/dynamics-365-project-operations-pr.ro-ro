---
title: Integrarea de facturi pentru furnizor
description: Acest subiect oferă informații despre integrarea facturii furnizorului în Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d4f1b0ad94b71dc4adc5b2b3423340c5fdb171eb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002295"
---
# <a name="vendor-invoice-integration"></a>Integrarea de facturi pentru furnizor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Achizițiile aferente proiectului în Dynamics 365 Project Operations pot fi înregistrate accesând **Conturi furnizori** > **Facturi** > **Facturi de furnizor neachitate** și utilizând un document de factură neachitată a furnizorului. Pentru mai multe informații, consultați [Achiziții de materiale care nu există pe stoc utilizând o factură de furnizor neachitată](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Înainte de a utiliza funcționalitatea descrisă în acest subiect, revizuiți și aplicați configurațiile necesare. Pentru mai multe informații, consultați [Activarea materialelor care nu există pe stoc și a facturilor de la furnizori neachitate](../procurement/configure-materials-nonstocked.md).

În Project Operations, facturile de furnizor legate de proiect sunt înregistrate folosind reguli speciale de publicare:

- Costul aferent proiectului (inclusiv impozitul nerecuperabil) nu este înregistrat imediat în contul de cost al proiectului din registrul general. În schimb, costul este înregistrat în **Cont de integrare a achizițiilor**. Acest cont este configurat în **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametrii contabili**, pe fila **Project Operations pe Dynamics 365 Customer engagement**.
- Scrierea duală sincronizează detaliile facturii de furnizor la Microsoft Dataverse folosind următoarele hărți de tabel:

     - **Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices)**: Această hartă de tabel sincronizează informațiile antetului facturii de furnizor. Doar facturile de furnizor cu cel puțin o linie care conține un ID de proiect sunt sincronizate la Dataverse.
     - **Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn_projectvendorinvoicelines)**: Această hartă de tabel sincronizează informațiile liniei facturii de furnizor. Doar liniile care conțin un ID de proiect sunt sincronizate cu Dataverse.

     > [!NOTE]
     > Detaliile facturii de furnizor în Dataverse nu sunt editabile.

Subregistrul de impozit, subregistrul furnizorului și alte înregistrări financiare sunt înregistrate după caz, în Dynamics 365 Finance când se postează factura de furnizor.

![Integrarea de facturi pentru furnizor](media/DW7VendorInvoice.png)

Când înregistrările sunt scrise către o entitate **Factura de furnizor** în Dataverse începe un proces automat de aprobare a înregistrărilor. Dacă este necesar, starea procesului de aprobare automată poate fi revizuită în Dataverse accesând **Setări avansate** > **Sistem** > **Procese de sistem**. După finalizarea aprobării, sistemul creează înregistrări de clase de tranzacții materiale în entitatea **Actualități**.

Datele reale legate de materiale sunt apoi procesate utilizând harta tabelului cu scriere duală **Valori reale privind integrarea în Project Operations (msdyn_actuals)**. Pentru mai multe informații, consultați [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md).

Procesul periodic, **Import din etapă** creează linii de jurnal legate de factura de furnizor în jurnalul de integrare Project Operations. Contul compensat este implicit cu contul de integrare al achizițiilor. Când este înregistrat jurnalul de integrare, soldul contului este eliminat pentru tranzacția cu factura de furnizor și suma liniei este mutată în contul de cost de proiecti. Tranzacțiile subregistru de proiect sunt create, de asemenea, în scopuri de facturare în aval și de recunoaștere a veniturilor.
