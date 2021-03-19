---
title: Dezactivarea unei dimensiuni de preț
description: Acest subiect oferă informații despre cum să dezactivați dimensiunile de preț.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274743"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="df6d5-103">Dezactivarea unei dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="df6d5-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="df6d5-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="df6d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="df6d5-105">Poate fi necesar să revizuiți și să actualizați strategia de tarifare la fiecare câțiva ani.</span><span class="sxs-lookup"><span data-stu-id="df6d5-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="df6d5-106">Orice actualizări pe care le efectuați pot necesita dezactivarea unei dimensiuni de tarifare existente și crearea uneia noi.</span><span class="sxs-lookup"><span data-stu-id="df6d5-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="df6d5-107">De exemplu, este posibil să fi tarifat în trecut în funcție de **Rol**, dar acum ați decis să tarifați în funcție de **Experiența de lucru**.</span><span class="sxs-lookup"><span data-stu-id="df6d5-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="df6d5-108">Acest lucru vă poate solicita să dezactivați **Rol** ca dimensiune de tarifare și să creați **Experiența de lucru** ca noua dimensiune de tarifare.</span><span class="sxs-lookup"><span data-stu-id="df6d5-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="df6d5-109">Dezactivarea unei dimensiuni de tarifare, indiferent dacă este predefinită sau personalizată, se poate face prin setarea câmpurilor **Aplicabil la costuri** și **Aplicabil la vânzări** ale dimensiunii de tarifare la **Nu**.</span><span class="sxs-lookup"><span data-stu-id="df6d5-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="df6d5-110">Cu toate acestea, atunci când faceți acest lucru, este posibil să primiți mesajul de eroare, **Dimensiunea prețurilor nu poate fi actualizată sau ștearsă dacă există înregistrări de preț asociate.**</span><span class="sxs-lookup"><span data-stu-id="df6d5-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Eroare de proces de business probabil atunci când dezactivați o dimensiune de tarifare](media/Business-Process-Error.png)

<span data-ttu-id="df6d5-112">Acest mesaj de eroare indică faptul că există înregistrări de preț care au fost parametrizate anterior pentru dimensiunea care este dezactivată.</span><span class="sxs-lookup"><span data-stu-id="df6d5-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="df6d5-113">Toate înregistrările **Preț rol** și **Adaos preț rol** care se referă la o dimensiune trebuie șterse înainte ca aplicabilitatea dimensiunii să fie setată la **Nu**.</span><span class="sxs-lookup"><span data-stu-id="df6d5-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="df6d5-114">Această regulă se aplică atât dimensiunilor de tarifare predefinite, cât și oricăror dimensiuni de preț particularizate pe care le-ați creat.</span><span class="sxs-lookup"><span data-stu-id="df6d5-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="df6d5-115">Motivul pentru această validare este pentru că înregistrarea **Rol de preț** trebuie să aibă o combinație unică de dimensiuni.</span><span class="sxs-lookup"><span data-stu-id="df6d5-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="df6d5-116">De exemplu, pe o listă de prețuri numită **Rate de cost SUA 2018**, aveți următoarele rânduri de **Preț rol**.</span><span class="sxs-lookup"><span data-stu-id="df6d5-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="df6d5-117">Titlu standard</span><span class="sxs-lookup"><span data-stu-id="df6d5-117">Standard Title</span></span>         | <span data-ttu-id="df6d5-118">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="df6d5-118">Org Unit</span></span>    |<span data-ttu-id="df6d5-119">Unitate</span><span class="sxs-lookup"><span data-stu-id="df6d5-119">Unit</span></span>   |<span data-ttu-id="df6d5-120">Preț</span><span class="sxs-lookup"><span data-stu-id="df6d5-120">Price</span></span>  |<span data-ttu-id="df6d5-121">Monedă</span><span class="sxs-lookup"><span data-stu-id="df6d5-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="df6d5-122">Inginer sisteme</span><span class="sxs-lookup"><span data-stu-id="df6d5-122">Systems Engineer</span></span>|<span data-ttu-id="df6d5-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="df6d5-123">Contoso US</span></span>|<span data-ttu-id="df6d5-124">Hour</span><span class="sxs-lookup"><span data-stu-id="df6d5-124">Hour</span></span>| <span data-ttu-id="df6d5-125">100</span><span class="sxs-lookup"><span data-stu-id="df6d5-125">100</span></span>|<span data-ttu-id="df6d5-126">USD</span><span class="sxs-lookup"><span data-stu-id="df6d5-126">USD</span></span>|
| <span data-ttu-id="df6d5-127">Inginer sisteme senior</span><span class="sxs-lookup"><span data-stu-id="df6d5-127">Senior Systems Engineer</span></span>|<span data-ttu-id="df6d5-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="df6d5-128">Contoso US</span></span>|<span data-ttu-id="df6d5-129">Hour</span><span class="sxs-lookup"><span data-stu-id="df6d5-129">Hour</span></span>| <span data-ttu-id="df6d5-130">150</span><span class="sxs-lookup"><span data-stu-id="df6d5-130">150</span></span>| <span data-ttu-id="df6d5-131">USD</span><span class="sxs-lookup"><span data-stu-id="df6d5-131">USD</span></span>|


<span data-ttu-id="df6d5-132">Când dezactivați **Titlu standard** ca dimensiunea de tarifare, iar motorul de tarifare caută un preț, acesta va utiliza numai valoarea **Unității organizaționale** din contextul de intrare.</span><span class="sxs-lookup"><span data-stu-id="df6d5-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="df6d5-133">Dacă **Unitatea organizațională** din contextul de intrare este „Contoso US", rezultatul va fi non-determinist, deoarece ambele rânduri se vor potrivi.</span><span class="sxs-lookup"><span data-stu-id="df6d5-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="df6d5-134">Pentru a evita acest scenariu, atunci când creați înregistrări de **Preț de rol**, sistemul validează unicitatea combinației de dimensiuni.</span><span class="sxs-lookup"><span data-stu-id="df6d5-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="df6d5-135">Dacă dimensiunea este dezactivată după crearea înregistrărilor de **Preț de rol**, această restricție poate fi încălcată.</span><span class="sxs-lookup"><span data-stu-id="df6d5-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="df6d5-136">Prin urmare, este necesar ca înainte de a dezactiva o dimensiune să ștergeți toate rândurile **Preț rol** și **Adaos preț rol** care au această valoare de dimensiune populată.</span><span class="sxs-lookup"><span data-stu-id="df6d5-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]