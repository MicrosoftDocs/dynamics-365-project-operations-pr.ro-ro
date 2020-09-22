---
title: Configurați facturarea proiectelor între companii
description: Acest subiect arată cum să configurați facturarea proiectului între două companii din organizația dvs.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754704"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="e7272-103">Configurați facturarea proiectelor între companii</span><span class="sxs-lookup"><span data-stu-id="e7272-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7272-104">Acest subiect arată cum să configurați facturarea proiectului între două companii din organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="e7272-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="e7272-105">Această sarcină utilizează setul de date USSI.</span><span class="sxs-lookup"><span data-stu-id="e7272-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e7272-106">În panoul de navigare, accesați **Module > Conturi furnizori > Furnizori > Toți furnizorii**.</span><span class="sxs-lookup"><span data-stu-id="e7272-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="e7272-107">În lista **Toți furnizorii**, găsiți și selectați înregistrarea dorită.</span><span class="sxs-lookup"><span data-stu-id="e7272-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="e7272-108">În panoul de acțiuni, selectați **General**.</span><span class="sxs-lookup"><span data-stu-id="e7272-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="e7272-109">Selectați **Între companii**.</span><span class="sxs-lookup"><span data-stu-id="e7272-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="e7272-110">Configurați **Activ** la **Da** pentru a permite tranzacționarea între companii.</span><span class="sxs-lookup"><span data-stu-id="e7272-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="e7272-111">În câmpul **Compania clientului**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="e7272-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="e7272-112">În câmpul **Contul meu**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="e7272-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="e7272-113">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="e7272-113">Select **Save**.</span></span>
9. <span data-ttu-id="e7272-114">Închideți paginile pentru a reveni la pagina principală.</span><span class="sxs-lookup"><span data-stu-id="e7272-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="e7272-115">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Parametrii pentru managementul proiectelor și contabilitate**.</span><span class="sxs-lookup"><span data-stu-id="e7272-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="e7272-116">Selectați fila **Între companii**.</span><span class="sxs-lookup"><span data-stu-id="e7272-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="e7272-117">Mutați glisorul la **Da** pentru a permite planificarea resurselor între companii și foi de pontaj.</span><span class="sxs-lookup"><span data-stu-id="e7272-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="e7272-118">În listă, marcați rândul selectat.</span><span class="sxs-lookup"><span data-stu-id="e7272-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e7272-119">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="e7272-119">Select **New**.</span></span>
15. <span data-ttu-id="e7272-120">În câmpul **Persoană juridică care împrumută**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="e7272-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="e7272-121">Selectați caseta de selectare **Venituri acumulate**.</span><span class="sxs-lookup"><span data-stu-id="e7272-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="e7272-122">În câmpul **Categorie implicită a foii de pontaj**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="e7272-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="e7272-123">În câmpul **Categorie implicită de cheltuieli**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="e7272-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="e7272-124">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="e7272-124">Select **Save**.</span></span>
20. <span data-ttu-id="e7272-125">Închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="e7272-125">Close the page.</span></span>
21. <span data-ttu-id="e7272-126">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Publicare > Configurare publicare registru**.</span><span class="sxs-lookup"><span data-stu-id="e7272-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="e7272-127">În câmpul **Tipuri de conturi registru** selectați o opțiune.</span><span class="sxs-lookup"><span data-stu-id="e7272-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="e7272-128">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="e7272-128">Select **New**.</span></span>
24. <span data-ttu-id="e7272-129">În câmpul **Contul principal** din noul rând, specificați valorile dorite.</span><span class="sxs-lookup"><span data-stu-id="e7272-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="e7272-130">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="e7272-130">Select **Save**.</span></span>
26. <span data-ttu-id="e7272-131">Închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="e7272-131">Close the page.</span></span>
27. <span data-ttu-id="e7272-132">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Prețul de transfer**.</span><span class="sxs-lookup"><span data-stu-id="e7272-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="e7272-133">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="e7272-133">Select **New**.</span></span>
29. <span data-ttu-id="e7272-134">În câmpul **Data efectivă**, introduceți o dată.</span><span class="sxs-lookup"><span data-stu-id="e7272-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="e7272-135">În câmpul **Persoană juridică care împrumută**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="e7272-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="e7272-136">În câmpul **Modelul prețului de transfer** selectați o opțiune.</span><span class="sxs-lookup"><span data-stu-id="e7272-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="e7272-137">În câmpul **Preț**, introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="e7272-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="e7272-138">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="e7272-138">Select **Save**.</span></span>

