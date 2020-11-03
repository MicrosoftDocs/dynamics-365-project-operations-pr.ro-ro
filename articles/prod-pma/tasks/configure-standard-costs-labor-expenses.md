---
title: Configurați costurile standard pentru forța de muncă și cheltuieli
description: Acest subiect explică modul de stabilire a costurilor standard pentru forța de muncă și pentru cheltuielile unui proiect.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082853"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="578ca-103">Configurați costurile standard pentru forța de muncă și cheltuieli</span><span class="sxs-lookup"><span data-stu-id="578ca-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="578ca-104">Acest subiect explică modul de stabilire a costurilor standard pentru forța de muncă și pentru cheltuielile unui proiect.</span><span class="sxs-lookup"><span data-stu-id="578ca-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="578ca-105">Această sarcină utilizează setul de date USSI.</span><span class="sxs-lookup"><span data-stu-id="578ca-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="578ca-106">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Preț de cost (oră)**.</span><span class="sxs-lookup"><span data-stu-id="578ca-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="578ca-107">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="578ca-107">Select **New**.</span></span>
3. <span data-ttu-id="578ca-108">În câmpul **Data efectivă** , introduceți o dată.</span><span class="sxs-lookup"><span data-stu-id="578ca-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="578ca-109">În câmpul **Preț de cost** , introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="578ca-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="578ca-110">Puteți seta un preț de cost standard pentru categoria de proiect sau puteți seta un preț de cost în funcție de numărul lucrătorului, numărul proiectului, categoria, data sau orice combinație a acestora.</span><span class="sxs-lookup"><span data-stu-id="578ca-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="578ca-111">Prețul de cost aplicat este prețul de cost cu cel mai înalt nivel de detaliere.</span><span class="sxs-lookup"><span data-stu-id="578ca-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="578ca-112">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="578ca-112">Select **Save**.</span></span>
6. <span data-ttu-id="578ca-113">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Prețul de vânzări (oră)**.</span><span class="sxs-lookup"><span data-stu-id="578ca-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="578ca-114">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="578ca-114">Select **New**.</span></span>
8. <span data-ttu-id="578ca-115">În câmpul **Data efectivă** , introduceți o dată.</span><span class="sxs-lookup"><span data-stu-id="578ca-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="578ca-116">În câmpul **Valid pentru** , selectați o opțiune.</span><span class="sxs-lookup"><span data-stu-id="578ca-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="578ca-117">În câmpul **Preț** , introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="578ca-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="578ca-118">Puteți configura un preț de vânzare standard pentru tranzacțiile per oră sau pentru o categorie de proiect.</span><span class="sxs-lookup"><span data-stu-id="578ca-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="578ca-119">De asemenea, puteți seta prețurile de vânzare după numărul lucrătorului, numărul proiectului, categoria, data tranzacției sau orice combinație a acestora.</span><span class="sxs-lookup"><span data-stu-id="578ca-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="578ca-120">Prețul real de vânzare, care se aplică atunci când un lucrător introduce o tranzacție în jurnalul pe oră, este prețul de vânzare cu cel mai înalt nivel de detaliere.</span><span class="sxs-lookup"><span data-stu-id="578ca-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="578ca-121">De exemplu, dacă sunt stabilite atât un preț general de vânzare, cât și un preț de vânzare specific lucrătorului, se folosește prețul de vânzare specific lucrătorului.</span><span class="sxs-lookup"><span data-stu-id="578ca-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="578ca-122">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="578ca-122">Select **Save**.</span></span>
12. <span data-ttu-id="578ca-123">Închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="578ca-123">Close the page.</span></span>
13. <span data-ttu-id="578ca-124">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Preț de cost (cheltuieli)**.</span><span class="sxs-lookup"><span data-stu-id="578ca-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="578ca-125">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="578ca-125">Select **New**.</span></span>
15. <span data-ttu-id="578ca-126">În câmpul **Data efectivă** , introduceți o dată.</span><span class="sxs-lookup"><span data-stu-id="578ca-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="578ca-127">În câmpul **Preț de cost** , introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="578ca-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="578ca-128">Pot fi completate mai multe câmpuri, dar acesta este minimul necesar pentru salvarea înregistrării.</span><span class="sxs-lookup"><span data-stu-id="578ca-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="578ca-129">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="578ca-129">Select **Save**.</span></span>
18. <span data-ttu-id="578ca-130">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Configurare > Prețuri > Prețul de vânzări (cheltuieli)**.</span><span class="sxs-lookup"><span data-stu-id="578ca-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="578ca-131">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="578ca-131">Select **New**.</span></span>
20. <span data-ttu-id="578ca-132">În câmpul **Data efectivă** , introduceți o dată.</span><span class="sxs-lookup"><span data-stu-id="578ca-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="578ca-133">În câmpul **Valid pentru** , selectați o opțiune.</span><span class="sxs-lookup"><span data-stu-id="578ca-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="578ca-134">În câmpul **Preț** , introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="578ca-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="578ca-135">Prețul real de vânzare, care se aplică atunci când un lucrător introduce tranzacții în jurnalul de cheltuieli, este prețul de vânzare cu cel mai înalt nivel de detaliere.</span><span class="sxs-lookup"><span data-stu-id="578ca-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="578ca-136">De exemplu, dacă sunt stabilite atât un preț general de vânzare, cât și un preț de vânzare specific lucrătorului, se folosește prețul de vânzare specific lucrătorului.</span><span class="sxs-lookup"><span data-stu-id="578ca-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="578ca-137">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="578ca-137">Select **Save**.</span></span>

