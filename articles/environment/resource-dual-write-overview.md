---
title: Integrare cu scriere duală a Project Operations
description: Acest articol oferă o prezentare generală a integrării cu scriere duală a Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927987"
---
# <a name="project-operations-dual-write-integration-overview"></a>Prezentare generală pentru Integrare cu scriere duală a Project Operations

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Project Operations utilizează [capabilități de scriere duală](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) pentru a sincroniza datele din Microsoft Dataverse și Dynamics 365 Finance.

Următoarea ilustrație arată cum sunt sincronizate datele ca parte a acestei integrări între Dataverse și Finanțe.

![Prezentare generală a fluxurilor de date Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations pe Dataverse oferă o interfață de utilizator modernă (UI) și o extensibilitate ușoară fără cod/cod scăzut folosind capacități Power Platform . Managerii de proiect, managerii de resurse, membrii echipei de proiect și alte persoane din front-office își desfășoară activitățile în Project Operations pe Dataverse.

Project Operations în Finanțe asigură contabilitatea proiectelor și suport pentru recunoașterea veniturilor. Project Operations se conectează la cadrul financiar din Finanțe pentru calcularea impozitului pe vânzări, ratele de schimb valutar, raportarea dimensiunii financiare și multe altele. Experiențele contabilului de proiect se bazează în cea mai mare parte pe Finanțe.

Integrarea Project Operations constă din următoarea integrare a componentelor:


- [Configurarea Project Operations și integrarea datelor de configurare](resource-dual-write-setup-integration.md) 
- [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md)
- [Facturi proiect](resource-dual-write-project-invoice.md)
- [Gestionarea cheltuielilor](resource-dual-write-expense.md)
- [Factură furnizor](resource-dual-write-vendor-invoice.md)
