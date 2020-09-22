---
title: Dezactivarea unei dimensiuni de tarifare
description: Acest subiect arată cum se configurează dimensiunile de tarifare în soluția Project service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754784"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="c8546-103">Dezactivarea unei dimensiuni de tarifare</span><span class="sxs-lookup"><span data-stu-id="c8546-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="c8546-104">Poate fi necesar să revizuiți și să actualizați strategia de tarifare la fiecare câțiva ani.</span><span class="sxs-lookup"><span data-stu-id="c8546-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="c8546-105">Orice actualizări pe care le efectuați pot necesita dezactivarea unei dimensiuni de tarifare existente și crearea uneia noi.</span><span class="sxs-lookup"><span data-stu-id="c8546-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="c8546-106">De exemplu, este posibil să fi tarifat în trecut în funcție de **Rol**, dar acum ați decis să tarifați în funcție de **Experiența de lucru**.</span><span class="sxs-lookup"><span data-stu-id="c8546-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="c8546-107">Acest lucru vă poate solicita să dezactivați **Rol** ca dimensiune de tarifare și să creați **Experiență de lucru** ca noua dimensiune de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c8546-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="c8546-108">Dezactivarea unei dimensiuni de tarifare, indiferent dacă este predefinită sau personalizată, se poate face prin setarea câmpurilor **Aplicabil la costuri** și **Aplicabil la vânzări** ale dimensiunii de tarifare la **Nu**.</span><span class="sxs-lookup"><span data-stu-id="c8546-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="c8546-109">Cu toate acestea, atunci când procedați astfel, este posibil să primiți următorul mesaj de eroare.</span><span class="sxs-lookup"><span data-stu-id="c8546-109">However, when you do this, you might receive the following error message.</span></span>

![Eroare de proces de business probabil atunci când dezactivați o dimensiune de tarifare](media/Business-Process-Error.png)


<span data-ttu-id="c8546-111">Acest mesaj de eroare indică faptul că există înregistrări de preț care au fost parametrizate anterior pentru dimensiunea care este dezactivată.</span><span class="sxs-lookup"><span data-stu-id="c8546-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="c8546-112">Toate înregistrările **Preț rol** și **Adaos preț rol** care se referă la o dimensiune trebuie șterse înainte ca aplicabilitatea dimensiunii să fie setată la **Nu**.</span><span class="sxs-lookup"><span data-stu-id="c8546-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="c8546-113">Această regulă se aplică atât dimensiunilor de tarifare predefinite, cât și oricăror dimensiuni de preț particularizate pe care le-ați creat.</span><span class="sxs-lookup"><span data-stu-id="c8546-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="c8546-114">Motivul pentru această validare se datorează faptului că Project service are o constrângere că fiecare înregistrare de **Preț de rol** trebuie să aibă o combinație unică de dimensiuni.</span><span class="sxs-lookup"><span data-stu-id="c8546-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="c8546-115">De exemplu, pe o listă de prețuri numită **Rate de cost SUA 2018**, aveți următoarele rânduri de **Preț rol**.</span><span class="sxs-lookup"><span data-stu-id="c8546-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="c8546-116">Titlu standard</span><span class="sxs-lookup"><span data-stu-id="c8546-116">Standard Title</span></span>         | <span data-ttu-id="c8546-117">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="c8546-117">Org Unit</span></span>    |<span data-ttu-id="c8546-118">Unitate</span><span class="sxs-lookup"><span data-stu-id="c8546-118">Unit</span></span>   |<span data-ttu-id="c8546-119">Preț</span><span class="sxs-lookup"><span data-stu-id="c8546-119">Price</span></span>  |<span data-ttu-id="c8546-120">Monedă</span><span class="sxs-lookup"><span data-stu-id="c8546-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="c8546-121">Inginer sisteme</span><span class="sxs-lookup"><span data-stu-id="c8546-121">Systems Engineer</span></span>|<span data-ttu-id="c8546-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="c8546-122">Contoso US</span></span>|<span data-ttu-id="c8546-123">Hour</span><span class="sxs-lookup"><span data-stu-id="c8546-123">Hour</span></span>| <span data-ttu-id="c8546-124">100</span><span class="sxs-lookup"><span data-stu-id="c8546-124">100</span></span>|<span data-ttu-id="c8546-125">USD</span><span class="sxs-lookup"><span data-stu-id="c8546-125">USD</span></span>|
| <span data-ttu-id="c8546-126">Inginer sisteme senior</span><span class="sxs-lookup"><span data-stu-id="c8546-126">Senior Systems Engineer</span></span>|<span data-ttu-id="c8546-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="c8546-127">Contoso US</span></span>|<span data-ttu-id="c8546-128">Hour</span><span class="sxs-lookup"><span data-stu-id="c8546-128">Hour</span></span>| <span data-ttu-id="c8546-129">150</span><span class="sxs-lookup"><span data-stu-id="c8546-129">150</span></span>| <span data-ttu-id="c8546-130">USD</span><span class="sxs-lookup"><span data-stu-id="c8546-130">USD</span></span>|


<span data-ttu-id="c8546-131">Când dezactivați **Titlu standard** ca dimensiunea de tarifare, iar motorul de tarifare Project Service caută un preț, acesta va utiliza numai valoarea **Unității organizaționale** din contextul de intrare.</span><span class="sxs-lookup"><span data-stu-id="c8546-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="c8546-132">Dacă **Unitatea organizațională** din contextul de intrare este „Contoso US", rezultatul va fi non-determinist, deoarece ambele rânduri se vor potrivi.</span><span class="sxs-lookup"><span data-stu-id="c8546-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="c8546-133">Pentru a evita acest scenariu, atunci când creați înregistrări de **Preț de rol**, Project Service validează unicitatea combinației de dimensiuni.</span><span class="sxs-lookup"><span data-stu-id="c8546-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="c8546-134">Dacă dimensiunea este dezactivată după crearea înregistrărilor de **Preț de rol**, această restricție poate fi încălcată.</span><span class="sxs-lookup"><span data-stu-id="c8546-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="c8546-135">Prin urmare, este necesar ca înainte de a dezactiva o dimensiune să ștergeți toate rândurile **Preț rol** și **Adaos preț rol** care au această valoare de dimensiune populată.</span><span class="sxs-lookup"><span data-stu-id="c8546-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

