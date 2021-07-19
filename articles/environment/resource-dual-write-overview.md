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
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="62c11-103">Prezentare generală pentru Integrare cu scriere duală a Project Operations</span><span class="sxs-lookup"><span data-stu-id="62c11-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="62c11-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="62c11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62c11-105">Utilizările Project Operations [capacități de scriere duală](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) pentru a sincroniza datele Microsoft Dataverse și Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="62c11-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="62c11-106">Următoarea ilustrație arată cum sunt sincronizate datele ca parte a acestei integrări între Dataverse și Finanțe.</span><span class="sxs-lookup"><span data-stu-id="62c11-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Prezentare generală a fluxurilor de date Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="62c11-108">Project Operations pe Dataverse oferă o interfață de utilizator modernă (UI) și o extensibilitate ușoară fără cod/cod scăzut folosind capacități Power Platform .</span><span class="sxs-lookup"><span data-stu-id="62c11-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="62c11-109">Managerii de proiect, managerii de resurse, membrii echipei de proiect și alte persoane din front-office își desfășoară activitățile în Project Operations pe Dataverse.</span><span class="sxs-lookup"><span data-stu-id="62c11-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="62c11-110">Project Operations în Finanțe asigură contabilitatea proiectelor și suport pentru recunoașterea veniturilor.</span><span class="sxs-lookup"><span data-stu-id="62c11-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="62c11-111">Project Operations se conectează la cadrul financiar din Finanțe pentru calcularea impozitului pe vânzări, ratele de schimb valutar, raportarea dimensiunii financiare și multe altele.</span><span class="sxs-lookup"><span data-stu-id="62c11-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="62c11-112">Experiențele contabilului de proiect se bazează în cea mai mare parte pe Finanțe.</span><span class="sxs-lookup"><span data-stu-id="62c11-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="62c11-113">Integrarea Project Operations constă din următoarea integrare a componentelor:</span><span class="sxs-lookup"><span data-stu-id="62c11-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="62c11-114">Configurarea Project Operations și integrarea datelor de configurare</span><span class="sxs-lookup"><span data-stu-id="62c11-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="62c11-115">Estimări de proiect și valori reale</span><span class="sxs-lookup"><span data-stu-id="62c11-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="62c11-116">Facturi proiect</span><span class="sxs-lookup"><span data-stu-id="62c11-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="62c11-117">Gestionarea cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="62c11-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="62c11-118">Factură furnizor</span><span class="sxs-lookup"><span data-stu-id="62c11-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
