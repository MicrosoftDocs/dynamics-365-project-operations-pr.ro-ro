---
title: Integrarea de facturi pentru proiect
description: Acest articol oferă informații despre integrarea cu scriere duală a Project Operations pentru facturarea clienților.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912117"
---
# <a name="project-invoice-integration"></a>Integrarea de facturi pentru proiect

Acest articol oferă informații despre integrarea cu scriere duală a Project Operations pentru facturarea clienților.

În Project Operations, managerul de proiect gestionează restanțele de facturare ale proiectului și creează o factură proformă pentru client în Microsoft Dataverse. Pe baza acestei facturi proforma, funcționarul de creanțe sau contabilul de proiect creează o factură orientată către client. Integrarea cu dublă scriere asigură sincronizarea detaliilor facturii proforma cu aplicațiile Finance and Operations. După ce se postează factura către client, sistemul actualizează datele relevante ale proiectului în Dataverse cu acest detaliu contabil. Următorul grafic oferă o imagine de ansamblu conceptuală la nivel înalt asupra acestei integrări.

   ![Integrarea de facturi pentru proiect.](./media/DW5Invoicing.png)

După ce managerul de proiect confirmă factura proforma în Dataverse, informațiile din antetul facturii proforma se sincronizează cu aplicațiile Finance and Operations folosind harta tabelului cu scriere dublă, **Propunere de factură de proiect V2 (facturi)**. Aceasta este o integrare unidirecțională de la Dataverse la aplicațiile Finanțe și Operațiuni. Crearea sau ștergerea propunerilor de factură de proiect direct în aplicațiile Finanțe și Operațiuni nu este acceptată.

Confirmarea facturii în Dataverse declanșează, de asemenea, logica de afaceri pentru a crea înregistrări legate de facturare în entitatea **Actualități**. Aceste înregistrări sunt sincronizate cu Finanțe și Operațiuni folosind harta tabelului cu dublă scriere, **Date reale de integrare a operațiunilor de proiect (msdyn\_ actuale).** Pentru mai multe informații, consultați [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md). 

Liniile de propunere de factură de proiect sunt create prin procesul periodic, **Importați etapizarea formularului**. Acest proces se bazează pe detaliile reale ale vânzărilor facturate în tabelul **Etapizarea valorilor reale**. Pentru mai multe informații, consultați [Gestionarea propunerilor de facturi pentru proiect](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
