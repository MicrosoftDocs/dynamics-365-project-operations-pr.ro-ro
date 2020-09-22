---
title: Sincronizați sarcinile proiectului direct din Project Service Automation în Finance and Operations
description: Acest subiect descrie șablonul și sarcina de desfășurare care sunt utilizate pentru a sincroniza sarcinile de proiect direct de la Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754810"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="fbb83-103">Sincronizați sarcinile proiectului direct din Project Service Automation în Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fbb83-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fbb83-104">Acest subiect descrie șablonul și sarcina de desfășurare care sunt utilizate pentru a sincroniza sarcinile de proiect direct de la Dynamics 365 Project Service Automation la Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb83-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="fbb83-105">Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.</span><span class="sxs-lookup"><span data-stu-id="fbb83-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="fbb83-106">Dacă utilizați Enterprise edition 7.3.0, după ce instalați KB 4132657 și KB 4132660, veți putea utiliza șabloanele pentru a integra sarcinile proiectului, categoriile de tranzacții de cheltuieli, estimările orelor, estimările cheltuielilor și datele reale și pentru a configura blocarea funcționalității.</span><span class="sxs-lookup"><span data-stu-id="fbb83-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="fbb83-107">Dacă trebuie să resetați distribuțiile contabile, vă recomandăm să instalați și KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="fbb83-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="fbb83-108">Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.</span><span class="sxs-lookup"><span data-stu-id="fbb83-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="fbb83-109">Fluxul de date pentru Project Service Automation la Finanțe</span><span class="sxs-lookup"><span data-stu-id="fbb83-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="fbb83-110">Soluția de integrare Project Service Automation la Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb83-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="fbb83-111">Șablonul de integrare disponibil cu funcția de integrare a datelor permite fluxul de date despre sarcinile proiectului de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb83-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fbb83-112">Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb83-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="fbb83-113">[![Fluxul de date pentru integrarea Project Service Automation cu Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="fbb83-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="fbb83-114">Șablon și sarcină</span><span class="sxs-lookup"><span data-stu-id="fbb83-114">Template and task</span></span>

<span data-ttu-id="fbb83-115">Pentru a accesa șablonul, în centrul de administrare Microsoft Power Apps, selectați **Proiecte**, apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.</span><span class="sxs-lookup"><span data-stu-id="fbb83-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fbb83-116">Următorul șablon și sarcina de desfășurare sunt utilizate pentru a sincroniza sarcini de proiect de la Project Service Automation la Finance:</span><span class="sxs-lookup"><span data-stu-id="fbb83-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="fbb83-117">**Numele șablonului în Integrarea datelor:** Sarcini de proiect (PSA la Fin și Ops)</span><span class="sxs-lookup"><span data-stu-id="fbb83-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="fbb83-118">**Numele sarcinii din proiect:** Sarcini de proiect</span><span class="sxs-lookup"><span data-stu-id="fbb83-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="fbb83-119">Înainte de a putea avea loc sincronizarea sarcinilor proiectului, trebuie să sincronizați contractele și proiectele proiectului.</span><span class="sxs-lookup"><span data-stu-id="fbb83-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="fbb83-120">Entitate setată</span><span class="sxs-lookup"><span data-stu-id="fbb83-120">Entity set</span></span>

| <span data-ttu-id="fbb83-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fbb83-121">Project Service Automation</span></span> | <span data-ttu-id="fbb83-122">Finanțe</span><span class="sxs-lookup"><span data-stu-id="fbb83-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="fbb83-123">Activități de proiect</span><span class="sxs-lookup"><span data-stu-id="fbb83-123">Project Tasks</span></span>              | <span data-ttu-id="fbb83-124">Entitate de integrare pentru sarcina proiectului</span><span class="sxs-lookup"><span data-stu-id="fbb83-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="fbb83-125">Fluxul de entități</span><span class="sxs-lookup"><span data-stu-id="fbb83-125">Entity flow</span></span>

<span data-ttu-id="fbb83-126">Sarcinile proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu Finanțarea ca activități de proiect.</span><span class="sxs-lookup"><span data-stu-id="fbb83-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="fbb83-127">Cerințe preliminare și configurare a mapării</span><span class="sxs-lookup"><span data-stu-id="fbb83-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="fbb83-128">Înainte de a putea avea loc sincronizarea sarcinilor proiectului, trebuie să sincronizați contractele și proiectele proiectului.</span><span class="sxs-lookup"><span data-stu-id="fbb83-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="fbb83-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="fbb83-129">Power Query</span></span>

<span data-ttu-id="fbb83-130">Trebuie să utilizați Microsoft Power Query pentru Excel pentru a filtra datele dacă această condiție este îndeplinită:</span><span class="sxs-lookup"><span data-stu-id="fbb83-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="fbb83-131">Aveți înregistrări specifice resurselor într-o sarcină de proiect.</span><span class="sxs-lookup"><span data-stu-id="fbb83-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="fbb83-132">Dacă trebuie să utilizați Power Query, urmați acest ghid:</span><span class="sxs-lookup"><span data-stu-id="fbb83-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="fbb83-133">Șablonul Sarcini de proiect (PSA la Fin și Ops) are un filtru implicit care exclude înregistrările specifice resurselor dintr-o sarcină de proiect prin setarea filtrului pe **IsLineTask** la **Fals**.</span><span class="sxs-lookup"><span data-stu-id="fbb83-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="fbb83-134">Dacă vă creați propriul șablon, trebuie să adăugați acest filtru.</span><span class="sxs-lookup"><span data-stu-id="fbb83-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fbb83-135">Maparea șabloanelor în integrarea datelor</span><span class="sxs-lookup"><span data-stu-id="fbb83-135">Template mapping in Data integration</span></span>

<span data-ttu-id="fbb83-136">Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor.</span><span class="sxs-lookup"><span data-stu-id="fbb83-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="fbb83-137">Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb83-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="fbb83-138">[![Maparea șabloanelor](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="fbb83-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
