---
title: Sincronizați estimările proiectului direct din Project Service Automation în Finance and Operations
description: Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza estimările orare ale proiectului și estimările cheltuielilor proiectului direct de la Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Finance.
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754734"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ab993-103">Sincronizați estimările proiectului direct din Project Service Automation în Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ab993-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab993-104">Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza estimările orare ale proiectului și estimările cheltuielilor proiectului direct de la Dynamics 365 Project Service Automation la Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ab993-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ab993-105">Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.</span><span class="sxs-lookup"><span data-stu-id="ab993-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="ab993-106">Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.</span><span class="sxs-lookup"><span data-stu-id="ab993-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="ab993-107">Fluxul de date pentru Project Service Automation la Finanțe</span><span class="sxs-lookup"><span data-stu-id="ab993-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="ab993-108">Soluția de integrare Project Service Automation la Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="ab993-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ab993-109">Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de date despre estimările orare ale proiectului și estimările cheltuielilor proiectului de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="ab993-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ab993-110">Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="ab993-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ab993-111">[![Fluxul de date pentru integrarea Project Service Automation cu Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ab993-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="ab993-112">Estimări orare de proiect</span><span class="sxs-lookup"><span data-stu-id="ab993-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ab993-113">Șabloane și sarcini</span><span class="sxs-lookup"><span data-stu-id="ab993-113">Template and tasks</span></span>

<span data-ttu-id="ab993-114">Pentru a accesa șabloanele disponibile, în centrul de administrare Microsoft Power Apps, selectați **Proiecte**, apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.</span><span class="sxs-lookup"><span data-stu-id="ab993-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ab993-115">Următorul șablon și sarcinile de desfășurare sunt utilizate pentru a sincroniza estimările orare ale proiectului de la Project Service Automation la Finance:</span><span class="sxs-lookup"><span data-stu-id="ab993-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ab993-116">**Numele șablonului în Integrarea datelor:** estimările orare ale proiectului (PSA la Fin și Ops)</span><span class="sxs-lookup"><span data-stu-id="ab993-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ab993-117">**Numele sarcinilor din proiect:**</span><span class="sxs-lookup"><span data-stu-id="ab993-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ab993-118">Relațiile de tranzacție</span><span class="sxs-lookup"><span data-stu-id="ab993-118">Transaction relationships</span></span>
    - <span data-ttu-id="ab993-119">Estimări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="ab993-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ab993-120">Entitate setată</span><span class="sxs-lookup"><span data-stu-id="ab993-120">Entity set</span></span>

| <span data-ttu-id="ab993-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab993-121">Project Service Automation</span></span> | <span data-ttu-id="ab993-122">Finanțe</span><span class="sxs-lookup"><span data-stu-id="ab993-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="ab993-123">Activitățile proiectului</span><span class="sxs-lookup"><span data-stu-id="ab993-123">Project tasks</span></span>              | <span data-ttu-id="ab993-124">Entitate de integrare pentru estimările orare ale proiectului</span><span class="sxs-lookup"><span data-stu-id="ab993-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ab993-125">Fluxul de entități</span><span class="sxs-lookup"><span data-stu-id="ab993-125">Entity flow</span></span>

<span data-ttu-id="ab993-126">Estimările orare ale proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu Finanțarea ca prognozele orare de proiect.</span><span class="sxs-lookup"><span data-stu-id="ab993-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ab993-127">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="ab993-127">Prerequisites</span></span>

<span data-ttu-id="ab993-128">Înainte de a putea avea loc sincronizarea estimărilor orare ale proiectului, trebuie să sincronizați proiectele, sarcinile proiectului și categoriile de tranzacții de cheltuieli ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="ab993-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ab993-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="ab993-129">Power Query</span></span>

<span data-ttu-id="ab993-130">În șablonul estimărilor orare ale proiectului, trebuie să utilizați Microsoft Power Query pentru Excel pentru a finaliza aceste sarcini:</span><span class="sxs-lookup"><span data-stu-id="ab993-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="ab993-131">Setați ID-ul implicit al modelului de prognoză care va fi utilizat atunci când integrarea creează prognoze orare noi.</span><span class="sxs-lookup"><span data-stu-id="ab993-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ab993-132">Filtrează orice înregistrare specifică resursei în sarcina care va eșua integrarea în prognozele orare.</span><span class="sxs-lookup"><span data-stu-id="ab993-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="ab993-133">Filtrează orice rânduri de categorii de tranzacții goale.</span><span class="sxs-lookup"><span data-stu-id="ab993-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="ab993-134">Nerespectarea completării acestei sarcini poate duce la prognoze orare incorecte.</span><span class="sxs-lookup"><span data-stu-id="ab993-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ab993-135">Setați ID-ul modelului de prognoză implicit</span><span class="sxs-lookup"><span data-stu-id="ab993-135">Set the default forecast model ID</span></span>

<span data-ttu-id="ab993-136">Pentru a actualiza ID-ul de model de prognoză implicit în șablon, faceți clic pe săgeata **Mapare** pentru a deschide maparea.</span><span class="sxs-lookup"><span data-stu-id="ab993-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ab993-137">Apoi selectați linkul **Interogare și filtrare avansate**.</span><span class="sxs-lookup"><span data-stu-id="ab993-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ab993-138">Dacă utilizați șablonul implicit estimări orare ale proiectului (PSA la Fin și Ops), selectați **Condiția inserată** în lista de **Pași aplicați**.</span><span class="sxs-lookup"><span data-stu-id="ab993-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="ab993-139">În intrarea **Funcție**, înlocuiți **O\_forecast** cu numele de ID model prognoză care ar trebui folosit cu integrarea.</span><span class="sxs-lookup"><span data-stu-id="ab993-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ab993-140">Șablonul implicit are un ID de model de prognoză din datele demonstrative.</span><span class="sxs-lookup"><span data-stu-id="ab993-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ab993-141">Când creați un șablon nou, trebuie să adăugați această coloană.</span><span class="sxs-lookup"><span data-stu-id="ab993-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ab993-142">În Power Query, selectați **Adăugare coloană condițională**, și introduceți un nume pentru coloana nouă, cum ar fi **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="ab993-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ab993-143">Introduceți condiția coloanei, unde, dacă sarcina de proiect nu este nulă, atunci \<introduceți ID-ul modelului de prognoză\>; altfel este nulă.</span><span class="sxs-lookup"><span data-stu-id="ab993-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="ab993-144">Filtrați înregistrările specifice resurselor</span><span class="sxs-lookup"><span data-stu-id="ab993-144">Filter out resource-specific records</span></span>

<span data-ttu-id="ab993-145">Șablonul estimărilor orare ale proiectului (PSA to Fin și Ops) are un filtru implicit care elimină orice înregistrare specifică resursei.</span><span class="sxs-lookup"><span data-stu-id="ab993-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="ab993-146">Dacă vă creați propriul șablon, trebuie să adăugați acest filtru.</span><span class="sxs-lookup"><span data-stu-id="ab993-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ab993-147">Selectați linkul **Interogare și filtrare avansate** pentru a filtra pe coloana **msdyn\_islinetask** astfel încât numai înregistrările **False** să fie incluse.</span><span class="sxs-lookup"><span data-stu-id="ab993-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="ab993-148">Filtrați rândurile de categorii de tranzacții goale</span><span class="sxs-lookup"><span data-stu-id="ab993-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="ab993-149">Trebuie să adăugați un filtru pentru a elimina toate rândurile care au categorii de tranzacții goale.</span><span class="sxs-lookup"><span data-stu-id="ab993-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="ab993-150">Această sarcină este necesară, indiferent dacă utilizați șablonul implicit sau creați propriul șablon.</span><span class="sxs-lookup"><span data-stu-id="ab993-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="ab993-151">Acest filtru elimină orice rânduri rezumative din Project Service Automation care ar putea determina prognozele orare în Finanțe să fie incorecte.</span><span class="sxs-lookup"><span data-stu-id="ab993-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="ab993-152">Selectați linkul **Interogare și filtrare avansate** pentru a filtra înregistrările nule în coloana **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="ab993-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ab993-153">Maparea șabloanelor în integrarea datelor</span><span class="sxs-lookup"><span data-stu-id="ab993-153">Template mapping in Data integration</span></span>

<span data-ttu-id="ab993-154">Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor.</span><span class="sxs-lookup"><span data-stu-id="ab993-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ab993-155">Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="ab993-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ab993-156">[![Maparea șabloanelor](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ab993-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="ab993-157">Estimări de cheltuieli proiect</span><span class="sxs-lookup"><span data-stu-id="ab993-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ab993-158">Șabloane și sarcini</span><span class="sxs-lookup"><span data-stu-id="ab993-158">Template and tasks</span></span>

<span data-ttu-id="ab993-159">Următorul șablon și sarcinile de desfășurare sunt utilizate pentru a sincroniza estimările cheltuielilor proiectului de la Project Service Automation la Finance:</span><span class="sxs-lookup"><span data-stu-id="ab993-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ab993-160">**Numele șablonului în Integrarea datelor:** estimările cheltuielilor proiectului (PSA la Fin și Ops)</span><span class="sxs-lookup"><span data-stu-id="ab993-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ab993-161">**Numele sarcinilor din proiect:**</span><span class="sxs-lookup"><span data-stu-id="ab993-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ab993-162">Relațiile de tranzacție</span><span class="sxs-lookup"><span data-stu-id="ab993-162">Transaction relationships</span></span> 
    - <span data-ttu-id="ab993-163">Estimări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="ab993-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ab993-164">Entitate setată</span><span class="sxs-lookup"><span data-stu-id="ab993-164">Entity set</span></span>

| <span data-ttu-id="ab993-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab993-165">Project Service Automation</span></span> | <span data-ttu-id="ab993-166">Finanțe</span><span class="sxs-lookup"><span data-stu-id="ab993-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="ab993-167">Conexiuni de tranzacție</span><span class="sxs-lookup"><span data-stu-id="ab993-167">Transaction Connections</span></span>    | <span data-ttu-id="ab993-168">Entitate de integrare pentru relațiile de tranzacție ale proiectului</span><span class="sxs-lookup"><span data-stu-id="ab993-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="ab993-169">Linii estimate</span><span class="sxs-lookup"><span data-stu-id="ab993-169">Estimate Lines</span></span>             | <span data-ttu-id="ab993-170">Entitate de integrare pentru estimările cheltuielilor proiectului</span><span class="sxs-lookup"><span data-stu-id="ab993-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="ab993-171">Fluxul de entități</span><span class="sxs-lookup"><span data-stu-id="ab993-171">Entity flow</span></span>

<span data-ttu-id="ab993-172">Estimările cheltuielilor proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu Finanțarea ca prognozele cheltuielilor de proiect.</span><span class="sxs-lookup"><span data-stu-id="ab993-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ab993-173">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="ab993-173">Prerequisites</span></span>

<span data-ttu-id="ab993-174">Înainte de a putea avea loc sincronizarea estimărilor cheltuielilor proiectului, trebuie să sincronizați proiectele, sarcinile proiectului și categoriile de tranzacții de cheltuieli ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="ab993-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ab993-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="ab993-175">Power Query</span></span>

<span data-ttu-id="ab993-176">În șablonul de actualizare a estimărilor cheltuielilor proiectului, trebuie să utilizați Power Query pentru a finaliza următoarele sarcini:</span><span class="sxs-lookup"><span data-stu-id="ab993-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="ab993-177">Filtrați pentru a include numai înregistrările de linie de estimări de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="ab993-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="ab993-178">Setați ID-ul implicit al modelului de prognoză care va fi utilizat atunci când integrarea creează prognoze orare noi.</span><span class="sxs-lookup"><span data-stu-id="ab993-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ab993-179">Transformați tipurile de facturare.</span><span class="sxs-lookup"><span data-stu-id="ab993-179">Transform the billing types.</span></span>
- <span data-ttu-id="ab993-180">Transformați tipurile de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="ab993-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="ab993-181">Filtrați pentru a include numai liniile de estimări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="ab993-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="ab993-182">Șablonul de estimare a cheltuielilor proiectului (PSA la Fin și Ops) are un filtru implicit care include numai liniile de cheltuieli în integrare.</span><span class="sxs-lookup"><span data-stu-id="ab993-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="ab993-183">Dacă vă creați propriul șablon, trebuie să adăugați acest filtru.</span><span class="sxs-lookup"><span data-stu-id="ab993-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ab993-184">Selectați sarcina **Relații de tranzacție**, apoi faceți clic pe săgeata **Mapare** pentru a deschide maparea.</span><span class="sxs-lookup"><span data-stu-id="ab993-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ab993-185">Selectați linkul **Interogare și filtrare avansate**.</span><span class="sxs-lookup"><span data-stu-id="ab993-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="ab993-186">Filtrați coloana **msdyn\_transactiontype1** astfel încât să includă numai **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="ab993-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ab993-187">Setați ID-ul modelului de prognoză implicit</span><span class="sxs-lookup"><span data-stu-id="ab993-187">Set the default forecast model ID</span></span>

<span data-ttu-id="ab993-188">Pentru a actualiza ID-ul de model de prognoză implicit în șablon, selectați sarcina **Estimări de cheltuieli**, și apoi faceți clic pe săgeata **Mapare** pentru a deschide maparea.</span><span class="sxs-lookup"><span data-stu-id="ab993-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ab993-189">Selectați linkul **Interogare și filtrare avansate**.</span><span class="sxs-lookup"><span data-stu-id="ab993-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ab993-190">Dacă utilizați șablonul implicit estimările cheltuielilor proiectului (PSA la Fin și Ops), în Power Query, selectați prima **Condiție inserată** din secțiunea **Pași aplicați**.</span><span class="sxs-lookup"><span data-stu-id="ab993-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="ab993-191">În intrarea **Funcție**, înlocuiți **O\_forecast** cu numele de ID model prognoză care ar trebui folosit cu integrarea.</span><span class="sxs-lookup"><span data-stu-id="ab993-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ab993-192">Șablonul implicit are un ID de model de prognoză din datele demonstrative.</span><span class="sxs-lookup"><span data-stu-id="ab993-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ab993-193">Când creați un șablon nou, trebuie să adăugați această coloană.</span><span class="sxs-lookup"><span data-stu-id="ab993-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ab993-194">În Power Query, selectați **Adăugare coloană condițională**, și introduceți un nume pentru coloana nouă, cum ar fi **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="ab993-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ab993-195">Introduceți condiția coloanei, unde, dacă ID linie estimare nu este nul, atunci \<introduceți ID-ul modelului de prognoză\>; altfel este nulă.</span><span class="sxs-lookup"><span data-stu-id="ab993-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="ab993-196">Transformați tipurile de facturare</span><span class="sxs-lookup"><span data-stu-id="ab993-196">Transform the billing types</span></span>

<span data-ttu-id="ab993-197">Șablonul estimare a cheltuielilor proiectului (PSA la Fin și Ops) include o coloană condițională care este utilizată pentru a transforma tipurile de facturare care sunt primite de la Project Service Automation în timpul integrării.</span><span class="sxs-lookup"><span data-stu-id="ab993-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ab993-198">Dacă vă creați propriul șablon, trebuie să adăugați această coloană condițională.</span><span class="sxs-lookup"><span data-stu-id="ab993-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ab993-199">Selectați linkul **Interogare și filtrare avansate** și apoi selectați **Adăugare coloană condițională**.</span><span class="sxs-lookup"><span data-stu-id="ab993-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ab993-200">Introduceți un nume pentru noua coloană, cum ar fi **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="ab993-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="ab993-201">Apoi, introduceți următoarea condiție:</span><span class="sxs-lookup"><span data-stu-id="ab993-201">Then enter the following condition:</span></span>

<span data-ttu-id="ab993-202">Dacă **msdyn\_billingtype** = 192350000, atunci **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="ab993-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="ab993-203">altfel dacă **msdyn\_billingtype** = 192350001, atunci **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="ab993-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="ab993-204">altfel dacă **msdyn\_billingtype** = 192350002, atunci **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="ab993-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="ab993-205">altfel **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="ab993-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="ab993-206">Transformați tipurile de tranzacții</span><span class="sxs-lookup"><span data-stu-id="ab993-206">Transform the transaction types</span></span>

<span data-ttu-id="ab993-207">Șablonul estimare a cheltuielilor proiectului (PSA la Fin și Ops) include o coloană condițională care este utilizată pentru a transforma tipurile de tranzacție care sunt primite de la Project Service Automation în timpul integrării.</span><span class="sxs-lookup"><span data-stu-id="ab993-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ab993-208">Dacă vă creați propriul șablon, trebuie să adăugați această coloană condițională.</span><span class="sxs-lookup"><span data-stu-id="ab993-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ab993-209">Selectați linkul **Interogare și filtrare avansate** și apoi selectați **Adăugare coloană condițională**.</span><span class="sxs-lookup"><span data-stu-id="ab993-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ab993-210">Introduceți un nume pentru noua coloană, cum ar fi **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="ab993-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="ab993-211">Apoi, introduceți următoarea condiție:</span><span class="sxs-lookup"><span data-stu-id="ab993-211">Then enter the following condition:</span></span>

<span data-ttu-id="ab993-212">Dacă **msdyn\_transactiontypecode** = 192350000, atunci **Cost**</span><span class="sxs-lookup"><span data-stu-id="ab993-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="ab993-213">altfel dacă **msdyn\_transactiontypecode** = 192350005, atunci **Sales**</span><span class="sxs-lookup"><span data-stu-id="ab993-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="ab993-214">altfel **null**</span><span class="sxs-lookup"><span data-stu-id="ab993-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ab993-215">Maparea șabloanelor în integrarea datelor</span><span class="sxs-lookup"><span data-stu-id="ab993-215">Template mapping in Data integration</span></span>

<span data-ttu-id="ab993-216">Următoarele ilustrații prezintă exemple de mapări ale sarcinilor șablon în Integrarea datelor.</span><span class="sxs-lookup"><span data-stu-id="ab993-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="ab993-217">Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="ab993-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ab993-218">[![Maparea șabloanelor](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ab993-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="ab993-219">[![Maparea șabloanelor](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ab993-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>