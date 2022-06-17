---
title: Integrarea de facturi pentru furnizor
description: Acest articol oferă informații despre integrarea facturii furnizorului în Operațiuni de proiect.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d1e41638b6fe827e9e577860a78a84a9948053e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912071"
---
# <a name="vendor-invoice-integration"></a>Integrarea de facturi pentru furnizor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Achizițiile aferente proiectului în Dynamics 365 Project Operations pot fi înregistrate accesând **Conturi furnizori** > **Facturi** > **Facturi de furnizor neachitate** și utilizând un document de factură neachitată a furnizorului. Pentru mai multe informații, consultați [Achiziții de materiale care nu există pe stoc utilizând o factură de furnizor neachitată](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Înainte de a utiliza funcționalitatea descrisă în acest articol, revizuiți și aplicați configurațiile necesare. Pentru mai multe informații, consultați [Activarea materialelor care nu există pe stoc și a facturilor de la furnizori neachitate](../procurement/configure-materials-nonstocked.md).

În Project Operations, facturile de furnizor legate de proiect sunt înregistrate folosind reguli speciale de publicare:

- Costul aferent proiectului (inclusiv impozitul nerecuperabil) nu este înregistrat imediat în contul de cost al proiectului din registrul general. În schimb, costul este înregistrat în **Cont de integrare a achizițiilor**. Acest cont este configurat în **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametrii contabili**, pe fila **Project Operations pe Dynamics 365 Customer engagement**.
- Scrierea duală sincronizează detaliile facturii de furnizor la Microsoft Dataverse folosind următoarele hărți de tabel:

     - **Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices)**: Această hartă de tabel sincronizează informațiile antetului facturii de furnizor. Doar facturile de furnizor cu cel puțin o linie care conține un ID de proiect sunt sincronizate la Dataverse.
     - **Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn_projectvendorinvoicelines)**: Această hartă de tabel sincronizează informațiile liniei facturii de furnizor. Doar liniile care conțin un ID de proiect sunt sincronizate cu Dataverse.

     > [!NOTE]
     > Detaliile facturii de furnizor în Dataverse nu sunt editabile.

Registrul fiscal secundar, registrul secundar al furnizorului și alte înregistrări financiare sunt înregistrate după caz în Dynamics 365 Finance atunci când factura de furnizor este înregistrată.

![Integrarea facturilor pentru furnizor.](media/DW7VendorInvoice.png)

Când înregistrările sunt scrise către o entitate **Factura de furnizor** în Dataverse începe un proces automat de aprobare a înregistrărilor. Dacă este necesar, starea procesului de aprobare automată poate fi revizuită în Dataverse accesând **Setări avansate** > **Sistem** > **Procese de sistem**. După finalizarea aprobării, sistemul creează înregistrări de clase de tranzacții materiale în entitatea **Actualități**.

Datele reale legate de materiale sunt apoi procesate utilizând harta tabelului cu scriere duală **Valori reale privind integrarea în Project Operations (msdyn_actuals)**. Pentru mai multe informații, consultați [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md).

Procesul periodic, **Import din etapă** creează linii de jurnal legate de factura de furnizor în jurnalul de integrare Project Operations. Contul compensat este implicit cu contul de integrare al achizițiilor. Când este înregistrat jurnalul de integrare, soldul contului este eliminat pentru tranzacția cu factura de furnizor și suma liniei este mutată în contul de cost de proiecti. Tranzacțiile subregistru de proiect sunt create, de asemenea, în scopuri de facturare în aval și de recunoaștere a veniturilor.
