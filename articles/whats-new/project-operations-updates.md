---
title: Actualizări Project Operations
description: Acest subiect oferă informații despre dimensiunile versiunile lansate de Dynamics 365 Project Operations.
author: sigitac
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5e37bc90a74e6bc9f1bf3d3820a34c3f4c3496d
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942854"
---
# <a name="project-operations-updates"></a>Actualizări Project Operations

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/non-stoc, implementare simplificată - facturare de la ofertă la proforma și Project Operations pentru scenarii stocate/bazate pe producție_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="project-operations-components"></a>Componente Project Operations

Dynamics 365 Project Operations este format din două componente:

- Project Operations pe mediul Dataverse acoperă capabilitățile de la oportunitate la emiterea facturii proforme. Dataverse este utilizat în implementarea simplă și implementarea scenariilor de resurse/ne-stocate ale Project Operations.
- Proiect management și contabilitate în mediul Dynamics 365 Finance acoperă capabilități de gestionare a cheltuielilor, contabilitate de proiect și recunoașterea veniturilor. Mediul de aplicație Finance and Operations este utilizat în Project Operations pentru scenarii resursă/non-stoc și Project Operations pentru scenarii stocat/pe bază de producție.

## <a name="project-operations-release-notes"></a>Note de lansare pentru Project Operations
- Cele mai recente note de lansare pentru Project Operations în cazul scenariilor [Resursă/non-stoc](whats-new-dec-2021-resource-based.md).
- Cele mai recente note de lansare pentru Project Operations în cazul scenariilor [Implementare simplificată](../pro/whats-new/whats-new-dec-2021-lite.md).
- Cele mai recente note de lansare pentru Project Operations în cazul scenariilor [stocate/producție](../prod-pma/whats-new/whats-new-oct-2021-stocked.md).

## <a name="project-operations-latest-version"></a>Ultima versiune Project Operations

| Project Operations pe mediu Dataverse | Management de proiect și contabilitate în medii de aplicații Finance and Operations | 
| --- | --- |
| 4.27.0.242 | 10.0.23 |

Pentru Resursă de operațiuni de proiect/scenariu fără stoc, vă recomandăm să utilizați versiunea orchestrației cu scriere duală 2.3.1.15 sau o versiune superioară.

## <a name="release-schedule-for-project-operations-on-dataverse-environment"></a>Planificare de lansare pentru Project Operations pe mediul Dataverse

Actualizările pentru Project Operations pe mediul Dataverse sunt disponibile lunar. 

| Stație | Regiunea | Numărul versiunii curente | Actualizări automate pentru implementarea Lite | Actualizări automate pentru implementare de resurse/nestocate | Următorul număr de versiune | Următoarea versiune este disponibilă în general |
|-----------|-----------------------|-----------------|--------------------|---------------------|---------------------|---------------------|
| Stația 1 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Prima apariție         |  4.27.0.242     | Finalizare*          | Finalizare*           | TBD                 | 14 ianuarie 2022    |
| Stația 2 |   &nbsp;              |    &nbsp;       | &nbsp;             |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | America de Sud         |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 14 ianuarie 2022    |
|   &nbsp;  | Canada                |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 14 ianuarie 2022    |
|   &nbsp;  | India                 |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 14 ianuarie 2022    |
|   &nbsp;  | Franța                |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 14 ianuarie 2022    |
|   &nbsp;  | Africa de Sud          |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 14 ianuarie 2022    |
| Stația 3 |      &nbsp;           |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Japonia                 |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 21 ianuarie 2022    |
|   &nbsp;  | Asia Pacific          |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 21 ianuarie 2022    |
|   &nbsp;  | Regatul Unit         |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 21 ianuarie 2022    |
|   &nbsp;  | Oceania               |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 21 ianuarie 2022    |
|   &nbsp;  | Emiratele Arabe Unite  |  4.27.0.242     | Finalizați           | 07 ianuarie 2022    | TBD                 | 21 ianuarie 2022    |
| Stația 4 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | Europa                |  4.26.0.155     | Finalizați           | 07 ianuarie 2022    | 4.27.0.242          | 10 ianuarie 2022    |
| Stația 5 |     &nbsp;            |     &nbsp;      |     &nbsp;         |      &nbsp;         |      &nbsp;         |      &nbsp;         |
|   &nbsp;  | America de Nord         |  4.26.0.155     | 07 ianuarie 2022   | 14 ianuarie 2022    | 4.27.0.242          | 17 ianuarie 2022    |

>[!Note]
> - Complete* - Actualizări automate finalizate cu versiunea 4.27.0.195.


## <a name="release-schedule-for-project-management-and-accounting-in-the-finance-and-operations-apps-environment"></a>Planificare de lansare pentru managementul de proiect și contabilitate în mediul de aplicații Finance and Operations

Actualizările pentru managementul de proiect și contabilitate sunt publicate de opt ori pe an.

|Versiune acceptată| Disponibilitate versiune preliminară (PEAP) | Disponibil în general (auto-actualizare) | Data de începere a producției programului de actualizare automată (prin setările de actualizare LCS) |   Sfârșit de serviciu   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.23     |      15 Octombrie 2021       |        10 decembrie 2021          |                          31 decembrie 2021                           | 18 martie 2022     |
|     10.0.22     |      3 septembrie 2021      |        22 Octombrie 2021           |                          5 noiembrie 2021                            | 14 ianuarie 2022   |


Datele de lansare vizate pot fi modificate. Pentru informații suplimentare, consultați [Disponibilitate actualizare de serviciu](/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-releases?toc=%2fdynamics365%2ffinance%2ftoc.json).

|Versiune țintă | Disponibilitate versiune preliminară (PEAP) | Disponibil în general (auto-actualizare) | Data de începere a producției programului de actualizare automată (prin setările de actualizare LCS) |   Sfârșit de serviciu   |
|:---------------:|:---------------------------:|:---------------------------------:|:--------------------------------------------------------------------:|:------------------:|
|     10.0.24     |      3 decembrie 2021       |        14 ianuarie 2022           |                          4 februarie 2022                            | 15 aprilie 2022     |
|     10.0.25     |      31 ianuarie 2022       |        18 martie 2022             |                          1 aprilie 2022                               | 10 iunie 2022      |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
