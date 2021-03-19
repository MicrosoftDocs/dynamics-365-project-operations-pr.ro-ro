---
title: Sincronizați categoriile de cheltuieli ale proiectului între Finance and Operations și Project Service Automation
description: Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza categoriile de cheltuieli ale proiectului între Microsoft Dynamics 365 Finance și Dynamics 365 Project Service Automation.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 4abb7fe6554825b97df4cc04ee1b02d731cb4af9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289654"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="df947-103">Sincronizați categoriile de cheltuieli ale proiectului între Finance and Operations și Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="df947-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="df947-104">Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza categoriile de cheltuieli ale proiectului între Dynamics 365 Finance și Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="df947-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="df947-105">Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.</span><span class="sxs-lookup"><span data-stu-id="df947-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="df947-106">Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.</span><span class="sxs-lookup"><span data-stu-id="df947-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="df947-107">Dacă utilizați Enterprise edition 7.3.0, după ce instalați KB 4132657 și KB 4132660, veți putea utiliza șabloanele pentru a integra sarcinile proiectului, categoriile de tranzacții de cheltuieli, estimările orelor, estimările cheltuielilor și datele reale și pentru a configura blocarea funcționalității.</span><span class="sxs-lookup"><span data-stu-id="df947-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="df947-108">Dacă trebuie să resetați distribuțiile contabile, vă recomandăm să instalați și KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="df947-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="df947-109">Fluxul de date pentru Project Service Automation și Finance</span><span class="sxs-lookup"><span data-stu-id="df947-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="df947-110">Soluția de integrare Project Service Automation și Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="df947-111">Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de date despre categoriile de cheltuieli de tranzacție ale proiectului între Finance și Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="df947-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="df947-112">Când categoriile de cheltuieli ale proiectului sunt stăpânite în Finance, fluxul de integrare este mai întâi din Finance la Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="df947-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="df947-113">ID-urile de integrare ale categoriilor de cheltuieli ale proiectului sunt apoi actualizate prin sincronizare de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="df947-114">Când categoriile de cheltuieli ale proiectului sunt stăpânite în Project Service Automation, fluxul de integrare este mai întâi din Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="df947-115">Categoriile de proiect trebuie să fie deja configurate în Finance înainte de sincronizarea din Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="df947-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="df947-116">Apoi sincronizați de la Finance înapoi la Project Service Automation și apoi iar de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="df947-117">În acest fel, garantați conectarea categoriilor și că nu sunt create duplicate.</span><span class="sxs-lookup"><span data-stu-id="df947-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="df947-118">De obicei, categoriile de cheltuieli ale proiectului sunt stăpânite în Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="df947-119">Cu toate acestea, dacă nu sunt, sau când categoriile de cheltuieli au fost deja create în Project Service Automation, trebuie mai întâi să sincronizați utilizând șablonul Categorii de tranzacții de cheltuieli ale proiectului (PSA la Fin și Ops).</span><span class="sxs-lookup"><span data-stu-id="df947-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="df947-120">Apoi sincronizați folosind șablonul categorii de tranzacții de cheltuieli ale proiectului (Fin și Ops la PSA).</span><span class="sxs-lookup"><span data-stu-id="df947-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="df947-121">Apoi, ar trebui să rulați sincronizarea de la Project Service Automation la Finance încă o dată.</span><span class="sxs-lookup"><span data-stu-id="df947-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="df947-122">Dacă vă sincronizați mai întâi de la Project Service Automation, următoarele cerințe trebuie să fie îndeplinite în Finance înainte ca sincronizarea să fie executată:</span><span class="sxs-lookup"><span data-stu-id="df947-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="df947-123">Categoria partajată care se potrivește cu categoria de proiect care este configurată în Project Service Automation trebuie să existe și trebuie activată pentru **Proiect** și pentru **Cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="df947-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="df947-124">Pentru fiecare entitate juridică din Finance cu care trebuie integrată, trebuie să existe următoarele categorii de proiecte:</span><span class="sxs-lookup"><span data-stu-id="df947-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="df947-125">**Categoria proiectului** există.</span><span class="sxs-lookup"><span data-stu-id="df947-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="df947-126">**Folosire în cheltuieli** este activat.</span><span class="sxs-lookup"><span data-stu-id="df947-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="df947-127">**Activ în jurnal** este activat.</span><span class="sxs-lookup"><span data-stu-id="df947-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="df947-128">**Tipul tranzacției** este setat la **Cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="df947-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="df947-129">Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="df947-130">[![Fluxul de date pentru integrarea Project Service Automation cu Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="df947-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="df947-131">Sincronizare categorii de cheltuieli ale proiectului între Finance și Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="df947-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="df947-132">Șablon și sarcină</span><span class="sxs-lookup"><span data-stu-id="df947-132">Template and task</span></span>

<span data-ttu-id="df947-133">Pentru a accesa șablonul, în centrul de administrare Microsoft Power Apps, selectați **Proiecte**, apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.</span><span class="sxs-lookup"><span data-stu-id="df947-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="df947-134">Următorul șablon și sarcina de desfășurare sunt utilizate pentru a sincroniza categoriile cheltuielilor proiectului de la Finance la Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="df947-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="df947-135">**Numele șablonului în Integrarea datelor:** categoriile de tranzacție ale cheltuielilor proiectului (Fin și Ops la PSA)</span><span class="sxs-lookup"><span data-stu-id="df947-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="df947-136">**Numele sarcinii din proiect:** Sincronizați categoriile cu PSA</span><span class="sxs-lookup"><span data-stu-id="df947-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="df947-137">Entitate setată</span><span class="sxs-lookup"><span data-stu-id="df947-137">Entity set</span></span>

| <span data-ttu-id="df947-138">Finanțe</span><span class="sxs-lookup"><span data-stu-id="df947-138">Finance</span></span>                           | <span data-ttu-id="df947-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="df947-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="df947-140">Entitate de integrare pentru categorii</span><span class="sxs-lookup"><span data-stu-id="df947-140">Integration entity for categories</span></span> | <span data-ttu-id="df947-141">Categorii de tranzacții</span><span class="sxs-lookup"><span data-stu-id="df947-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="df947-142">Fluxul de entități</span><span class="sxs-lookup"><span data-stu-id="df947-142">Entity flow</span></span>

<span data-ttu-id="df947-143">Categoriile cheltuielilor proiectului sunt gestionate în Finance și sunt sincronizate cu Project Service Automation ca și categorii de tranzacție.</span><span class="sxs-lookup"><span data-stu-id="df947-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="df947-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="df947-144">Power Query</span></span>

<span data-ttu-id="df947-145">Când vă sincronizați cu Project Service Automation, trebuie să utilizați Microsoft Power Query pentru Excel pentru a seta tipul de facturare în categoria tranzacției.</span><span class="sxs-lookup"><span data-stu-id="df947-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="df947-146">Șablonul categorii tranzacții de cheltuieli ale proiectului (Fin și Ops la PSA) oferă o coloană și o mapare implicite.</span><span class="sxs-lookup"><span data-stu-id="df947-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="df947-147">Dacă vă creați propriul șablon, trebuie să adăugați o coloană condițională în Power Query.</span><span class="sxs-lookup"><span data-stu-id="df947-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="df947-148">Urmați acești pași.</span><span class="sxs-lookup"><span data-stu-id="df947-148">Follow these steps.</span></span>

1. <span data-ttu-id="df947-149">Faceți clic pe săgeată pentru a deschide maparea activității categoriilor de cheltuieli de proiect în șablonul Categorii de tranzacții de cheltuieli de proiect (Fin și Ops la PSA).</span><span class="sxs-lookup"><span data-stu-id="df947-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="df947-150">Faceți clic pe linkul **Interogare și filtrare avansate** pentru a deschide Power Query.</span><span class="sxs-lookup"><span data-stu-id="df947-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="df947-151">Selectați **Adăugare coloană condițională**.</span><span class="sxs-lookup"><span data-stu-id="df947-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="df947-152">Introduceți un nume pentru noua coloană, cum ar fi **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="df947-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="df947-153">Introduceți următoarea condiție: **dacă CATEGORYID nu este egal cu nul atunci 19235001, altfel nul**.</span><span class="sxs-lookup"><span data-stu-id="df947-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="df947-154">Faceți clic pe **OK** din coloană.</span><span class="sxs-lookup"><span data-stu-id="df947-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="df947-155">Asigurați-vă că ați mapat această nouă coloană pe pagina de mapare.</span><span class="sxs-lookup"><span data-stu-id="df947-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="df947-156">Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor.</span><span class="sxs-lookup"><span data-stu-id="df947-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="df947-157">Maparea arată informațiile despre câmp care vor fi sincronizate de la Finance la Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="df947-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="df947-158">[![Maparea categoriei de cheltuieli ale proiectului la șablonul Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="df947-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="df947-159">Sincronizare categorii de cheltuieli ale proiectului între Project Service Automation și Finance</span><span class="sxs-lookup"><span data-stu-id="df947-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="df947-160">Șablon și sarcină</span><span class="sxs-lookup"><span data-stu-id="df947-160">Template and task</span></span>

<span data-ttu-id="df947-161">Următorul șablon și sarcina de desfășurare sunt utilizate pentru a sincroniza categoriile cheltuielilor proiectului de la Project Service Automation la Finance:</span><span class="sxs-lookup"><span data-stu-id="df947-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="df947-162">**Numele șablonului în Integrarea datelor:** categoriile de tranzacție ale cheltuielilor proiectului (PSA la Fin și Ops)</span><span class="sxs-lookup"><span data-stu-id="df947-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="df947-163">**Numele sarcinii din proiect:** Sincronizați categoriile cu Fin Ops</span><span class="sxs-lookup"><span data-stu-id="df947-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="df947-164">Entitate setată</span><span class="sxs-lookup"><span data-stu-id="df947-164">Entity set</span></span>

| <span data-ttu-id="df947-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="df947-165">Project Service Automation</span></span> | <span data-ttu-id="df947-166">Finanțe</span><span class="sxs-lookup"><span data-stu-id="df947-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="df947-167">Categorii de tranzacții</span><span class="sxs-lookup"><span data-stu-id="df947-167">Transaction categories</span></span>     | <span data-ttu-id="df947-168">Entitate de integrare pentru categorii</span><span class="sxs-lookup"><span data-stu-id="df947-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="df947-169">Fluxul de entități</span><span class="sxs-lookup"><span data-stu-id="df947-169">Entity flow</span></span>

<span data-ttu-id="df947-170">Categoriile cheltuielilor proiectului sunt gestionate în Finance și sunt sincronizate cu Project Service Automation ca și categorii de tranzacție.</span><span class="sxs-lookup"><span data-stu-id="df947-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="df947-171">Sincronizarea înapoi la actualizările Finance pentru categoriile proiectului din Finance cu ID de integrare de la Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="df947-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="df947-172">Maparea șabloanelor în integrarea datelor</span><span class="sxs-lookup"><span data-stu-id="df947-172">Template mapping in Data integration</span></span>

<span data-ttu-id="df947-173">Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor.</span><span class="sxs-lookup"><span data-stu-id="df947-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="df947-174">Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="df947-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="df947-175">[![Maparea șablonului Project Service Automation la Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="df947-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]