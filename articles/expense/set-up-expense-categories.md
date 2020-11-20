---
title: Configurarea categoriilor de cheltuieli
description: Acest subiect oferă informații despre cum să configurați categoriile de cheltuieli și categoriile partajate pentru rapoartele de cheltuieli.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123798"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="36f3d-103">Configurarea categoriilor de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="36f3d-103">Set up expense categories</span></span>

<span data-ttu-id="36f3d-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="36f3d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="36f3d-105">Când angajații creează rapoarte de cheltuieli, fiecare cheltuială pe care o înregistrează trebuie să fie asociată unei categorii de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="36f3d-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="36f3d-106">Categoriile de cheltuieli sunt derivate din categorii comune care pot fi partajate între entitățile juridice din organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="36f3d-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="36f3d-107">În funcție de modul în care este definită organizația dvs., aceste categorii de cheltuieli pot fi distribuite și în alte domenii.</span><span class="sxs-lookup"><span data-stu-id="36f3d-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="36f3d-108">Pe baza definiției organizației dvs. și a îndrumărilor din partea echipei de implementare, trebuie să determinați dacă categoriile care sunt utilizate în gestionarea cheltuielilor vor fi utilizate numai în gestionarea cheltuielilor sau ar trebui să fie partajate în alte domenii.</span><span class="sxs-lookup"><span data-stu-id="36f3d-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="36f3d-109">Aceste categorii pot fi împărțite între managementul de proiect și contabilitate și managementul cheltuielilor, sau între managementul de proiect și contabilitate și producție.</span><span class="sxs-lookup"><span data-stu-id="36f3d-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="36f3d-110">Cu toate acestea, acestea nu pot fi împărțite între managementul cheltuielilor și producție.</span><span class="sxs-lookup"><span data-stu-id="36f3d-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="36f3d-111">Înainte de a putea începe procesul de configurare, trebuie luate următoarele decizii pentru fiecare categorie de cheltuieli:</span><span class="sxs-lookup"><span data-stu-id="36f3d-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="36f3d-112">Care este categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-112">What is the expense category?</span></span> <span data-ttu-id="36f3d-113">Exemplele includ categorii pentru zboruri, hotel sau kilometraj.</span><span class="sxs-lookup"><span data-stu-id="36f3d-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="36f3d-114">Categoria de cheltuieli poate fi utilizată și în managementul proiectelor și contabilitate?</span><span class="sxs-lookup"><span data-stu-id="36f3d-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="36f3d-115">Dacă poate, trebuie să luați și următoarele decizii:</span><span class="sxs-lookup"><span data-stu-id="36f3d-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="36f3d-116">Ce conturi de costuri vor fi utilizate pentru următoarele cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="36f3d-117">Cost</span><span class="sxs-lookup"><span data-stu-id="36f3d-117">Cost</span></span>
        - <span data-ttu-id="36f3d-118">Alocare stat de plată</span><span class="sxs-lookup"><span data-stu-id="36f3d-118">Payroll allocation</span></span>
        - <span data-ttu-id="36f3d-119">WIP-valoare de cost</span><span class="sxs-lookup"><span data-stu-id="36f3d-119">WIP-cost value</span></span>
        - <span data-ttu-id="36f3d-120">Cost-element</span><span class="sxs-lookup"><span data-stu-id="36f3d-120">Cost-item</span></span>
        - <span data-ttu-id="36f3d-121">WIP-valoare de cost-element</span><span class="sxs-lookup"><span data-stu-id="36f3d-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="36f3d-122">Pierderi acumulate</span><span class="sxs-lookup"><span data-stu-id="36f3d-122">Accrued loss</span></span>
        - <span data-ttu-id="36f3d-123">WIP-pierderi acumulate</span><span class="sxs-lookup"><span data-stu-id="36f3d-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="36f3d-124">Ce conturi de venituri vor fi utilizate pentru următoarele surse de venit?</span><span class="sxs-lookup"><span data-stu-id="36f3d-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="36f3d-125">Venituri facturate</span><span class="sxs-lookup"><span data-stu-id="36f3d-125">Invoiced revenue</span></span>
        - <span data-ttu-id="36f3d-126">Venit acumulat-valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="36f3d-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="36f3d-127">WIP-valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="36f3d-127">WIP-sales value</span></span>
        - <span data-ttu-id="36f3d-128">Producție de venituri acumulate</span><span class="sxs-lookup"><span data-stu-id="36f3d-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="36f3d-129">WIP-producție</span><span class="sxs-lookup"><span data-stu-id="36f3d-129">WIP-production</span></span>
        - <span data-ttu-id="36f3d-130">Venituri acumulate-profit</span><span class="sxs-lookup"><span data-stu-id="36f3d-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="36f3d-131">WIP-profit</span><span class="sxs-lookup"><span data-stu-id="36f3d-131">WIP-profit</span></span>
        - <span data-ttu-id="36f3d-132">Venituri acumulate-abonament</span><span class="sxs-lookup"><span data-stu-id="36f3d-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="36f3d-133">WIP-abonament</span><span class="sxs-lookup"><span data-stu-id="36f3d-133">WIP-subscription</span></span>

- <span data-ttu-id="36f3d-134">Care este tipul de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-134">What is the expense type?</span></span>
- <span data-ttu-id="36f3d-135">Care este metoda de plată implicită pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="36f3d-136">Cheltuielile din categoria cheltuielilor trebuie să fie detaliate?</span><span class="sxs-lookup"><span data-stu-id="36f3d-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="36f3d-137">Care este contul principal implicit pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="36f3d-138">Care este grupul implicit de impozitare pe vânzări pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="36f3d-139">Sunt permise metode de plată suplimentare pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="36f3d-140">Dacă da, care sunt acestea?</span><span class="sxs-lookup"><span data-stu-id="36f3d-140">If so, what are they?</span></span>
- <span data-ttu-id="36f3d-141">Există subcategorii în această categorie de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="36f3d-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="36f3d-142">Dacă sunt subcategorii, trebuie să luați și următoarele decizii:</span><span class="sxs-lookup"><span data-stu-id="36f3d-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="36f3d-143">Există vreuna dintre subcategoriile excluse din recuperarea impozitelor?</span><span class="sxs-lookup"><span data-stu-id="36f3d-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="36f3d-144">Care este grupul de taxe pe vânzări de articole din subcategorii?</span><span class="sxs-lookup"><span data-stu-id="36f3d-144">What is the item sales tax group of the subcategories?</span></span>
