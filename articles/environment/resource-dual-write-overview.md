---
title: Integrare cu scriere duală a Project Operations
description: Acest subiect oferă o prezentare generală a integrării cu scriere duală a Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368446"
---
# <a name="project-operations-dual-write-integration-overview"></a>Prezentare generală pentru Integrare cu scriere duală a Project Operations

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Utilizările Project Operations [capacități de scriere duală](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) pentru a sincroniza datele Microsoft Dataverse și Dynamics 365 Finance.

Următoarea ilustrație arată cum sunt sincronizate datele ca parte a acestei integrări între Dataverse și Finanțe.

![Prezentare generală a fluxurilor de date Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations pe Dataverse oferă o interfață de utilizator modernă (UI) și o extensibilitate ușoară fără cod/cod scăzut folosind capacități Power Platform . Managerii de proiect, managerii de resurse, membrii echipei de proiect și alte persoane din front-office își desfășoară activitățile în Project Operations pe Dataverse.

Project Operations în Finanțe asigură contabilitatea proiectelor și suport pentru recunoașterea veniturilor. Project Operations se conectează la cadrul financiar din Finanțe pentru calcularea impozitului pe vânzări, ratele de schimb valutar, raportarea dimensiunii financiare și multe altele. Experiențele contabilului de proiect se bazează în cea mai mare parte pe Finanțe.

Integrarea Project Operations constă din următoarea integrare a componentelor:


- [Configurarea Project Operations și integrarea datelor de configurare](resource-dual-write-setup-integration.md) 
- [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md)
- [Facturi proiect](resource-dual-write-project-invoice.md)
- [Gestionarea cheltuielilor](resource-dual-write-expense.md)
- [Factură furnizor](resource-dual-write-vendor-invoice.md)
