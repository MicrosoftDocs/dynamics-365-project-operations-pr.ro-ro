---
title: Integrarea de facturi pentru proiect
description: Acest subiect oferă informații despre integrarea scriere duală pentru facturarea clientului în Project Operations.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993256"
---
# <a name="project-invoice-integration"></a>Integrarea de facturi pentru proiect

Acest subiect oferă informații despre integrarea scriere duală pentru facturarea clientului în Project Operations.

În Project Operations, managerul de proiect gestionează restanțele de facturare ale proiectului și creează o factură proformă pentru client în Microsoft Dataverse. Pe baza acestei facturi proforma, funcționarul de creanțe sau contabilul de proiect creează o factură orientată către client. Integrarea cu scriere duală asigură sincronizarea cu detaliile facturii proforma în aplicații Finance and Operations. După ce se postează factura către client, sistemul actualizează datele relevante ale proiectului în Dataverse cu acest detaliu contabil. Următorul grafic oferă o imagine de ansamblu conceptuală la nivel înalt asupra acestei integrări.

   ![Integrarea de facturi pentru proiect.](./media/DW5Invoicing.png)

După ce managerul de proiect confirmă factura proforma în Dataverse, informațiile antetului facturii proforma se sincronizează cu aplicații Finance and Operations care utilizează harta tabelului cu scriere duală **Propunere de facturi pentru proiect V2 (facturi)**. Aceasta este o integrare unidirecțională de la Dataverse la aplicații Finance and Operations. Crearea sau ștergerea propunerilor de facturi ale proiectului direct în aplicațiile Finance and Operations nu este acceptată.

Confirmarea facturii în Dataverse declanșează, de asemenea, logica de afaceri pentru a crea înregistrări legate de facturare în entitatea **Actualități**. Aceste înregistrări reale sunt sincronizate cu Finance and Operations folosind harta de tabel cu scriere duală, **Integrare valori reale Project Operations (msdyn\_actuals).** Pentru mai multe informații, consultați [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md). 

Liniile de propunere de factură de proiect sunt create prin procesul periodic, **Importați etapizarea formularului**. Acest proces se bazează pe detaliile reale ale vânzărilor facturate în tabelul **Etapizarea valorilor reale**. Pentru mai multe informații, consultați [Gestionarea propunerilor de facturi pentru proiect](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
