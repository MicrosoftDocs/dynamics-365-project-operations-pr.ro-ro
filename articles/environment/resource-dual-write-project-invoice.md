---
title: Integrarea de facturi pentru proiect
description: Acest articol oferă informații despre integrarea cu scriere duală pentru facturarea clientului în Project Operations.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029039"
---
# <a name="project-invoice-integration"></a>Integrarea de facturi pentru proiect

Acest articol oferă informații despre integrarea cu scriere duală pentru facturarea clientului în Project Operations.

În Project Operations, managerul de proiect gestionează restanțele de facturare ale proiectului și creează o factură proformă pentru client în Microsoft Dataverse. Pe baza acestei facturi proforma, funcționarul de creanțe sau contabilul de proiect creează o factură orientată către client. Integrarea cu scriere duală asigură sincronizarea cu detaliile facturii proformă în aplicațiile pentru finanțe și operațiuni. După ce se postează factura către client, sistemul actualizează datele relevante ale proiectului în Dataverse cu acest detaliu contabil. Următorul grafic oferă o imagine de ansamblu conceptuală la nivel înalt asupra acestei integrări.

   ![Integrarea de facturi pentru proiect.](./media/DW5Invoicing.png)

După ce Managerul de proiect confirmă factura proformă în Dataverse, informațiile antetului facturii proforme se sincronizează cu aplicațiile pentru finanțe și operațiuni care utilizează harta tabelului cu scriere duală **Propunere de facturare pentru proiectul V2 (facturi)**. Aceasta este o integrare unidirecțională de la Dataverse la aplicațiile pentru finanțe și operațiuni. Crearea sau ștergerea Propunerilor de facturare ale proiectului direct în aplicațiile pentru finanțe și operațiuni nu este acceptată.

Confirmarea facturii în Dataverse declanșează, de asemenea, logica de afaceri pentru a crea înregistrări legate de facturare în entitatea **Actualități**. Aceste înregistrări sunt sincronizate cu aplciațiile pentru finanțe și operațiuni folosind harta de tabel cu scriere duală, **Integrare valori reale Project Operations (msdyn\_actuals).** Pentru mai multe informații, consultați [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md). 

Liniile de propunere de factură de proiect sunt create prin procesul periodic, **Importați etapizarea formularului**. Acest proces se bazează pe detaliile reale ale vânzărilor facturate în tabelul **Etapizarea valorilor reale**. Pentru mai multe informații, consultați [Gestionarea propunerilor de facturi pentru proiect](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
