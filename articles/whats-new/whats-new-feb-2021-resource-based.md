---
title: Ce este nou în februarie 2021 - Project Operations pentru scenarii bazate pe resurse/ne-stocate
description: Acest subiect oferă informații despre actualizările de calitate disponibile în lansarea din februarie 2021 a Project Operations pentru scenarii bazate pe resurse/ne-stocate.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 12708a9b847f1f87ee0f5f45688adf48638d709f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291904"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în februarie 2021 - Project Operations pentru scenarii bazate pe resurse/ne-stocate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Project Operations pe mediu Dataverse 4.7.0.95
- Management de proiect și contabilitate în Dynamics 365 Finance versiunea mediului 10.0.16 

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| **Facturare și stabilirea prețurilor** | 2053736 | Detaliile liniei facturii sunt acum accesibile prin accesarea secțiunii **Factură** > **Informații conexe**. |
| **Facturare și stabilirea prețurilor** | 2122613 | Acțiunile **Activați** și **Dezactivați** au fost eliminate din entități de asociere **Listă de prețuri**. |
| **Facturare și stabilirea prețurilor** | 2128606 | S-a rezolvat problema cu **ullExcepțieReferință** în insertul **ObținețiEstimăriPentruProiect**. |
| **Implementare și configurare** | 2139346 | S-a rezolvat problema cu proces de importare a unei soluții negestionate **Dynamics365ProjectOperationsDualWrite**. |
| **Implementare și configurare** | 2140569 | Soluția proiectului nu trebuie instalată în mediile Dataverse Teams. |
| **Implementare și configurare** | 2086991 | Localizare de personalizare restricționată a resurselor web. |
| **Managementul oportunităților** | 2136794 | Afișați mesajul corect de eroare când procesele **Confirmați factura** sau **Marcați factura ca plătită** eșuează. |
| **Managementul oportunităților** | 2139330 | Schimbarea managerului de proiect în cadrul unui proiect nu trebuie să reseteze compania deținătoare la valoarea implicită. |
| **Managementul oportunităților** | 2146376 | Valoarea impozitului corectată la valorile reale neimpozabile este creată din confirmarea facturii. |
| **Planificarea și urmărirea proiectului** | 2099879 | Implementarea mediului Dataverse trebuie să creeze o categorie de tranzacții implicită cu un ID static și să nu genereze unul în mod aleatoriu per mediu. |
| **Planificarea și urmărirea proiectului** | 2128577 | S-au remediat privilegiile utilizatorului pentru Project Service pentru a actualiza categoria de tranzacții la o alocare de resurse. |
| **Planificarea și urmărirea proiectului** | 2164035 | S-au rezolvat problemele cu funcția **Copiați proiect**. |
| **Intrare de timp** | 2129161 | Se aplică restricții mai stricte pentru a garanta că utilizatorii nu pot modifica și actualiza o intrare de timp care a fost trimisă sau aprobată. |
| **Intrare de timp** | 2103572 | Aprobarea timpului pentru intrările de timp care nu fac parte din proiect nu trebuie să caute rolul de aprobator al proiectului. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance 

Pentru mai multe informații despre managementul proiectului și contabilitate în Dynamics 365 Finance, consultați [Ce este nou ianuarie 2021 - Project Operations scenarii bazate pe resurse/ne-stocate](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Actualizări de reglementare

Pentru informații despre actualizările de reglementare pentru aplicații Finance and Operations, vezi [Actualizări de reglementare](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). O altă modalitate de a afla despre actualizările de reglementare este să vă conectați la Lifecycle Services (LCS) și să vizualizați actualizările de reglementare planificate folosind instrumentul de căutare a problemelor. Căutarea problemelor vă permite să căutați în funcție de țară, tipul de funcție și eliberare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]