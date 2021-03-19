---
title: Configurarea unei liste de prețuri pentru vânzare
description: Acest subiect oferă informații despre listele de prețuri de vânzări pentru prețuri de proiect.
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
ms.openlocfilehash: 05b1c13540e902975eee7379276cf394d9fc5743
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275463"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="200e1-103">Configurarea unei liste de prețuri pentru vânzare</span><span class="sxs-lookup"><span data-stu-id="200e1-103">Set up a sales price list</span></span>

<span data-ttu-id="200e1-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="200e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="200e1-105">Pentru ofertele și contractele de proiect, o listă de prețuri de proiect are un alt model de suprascriere a prețului decât o listă de prețuri de produs.</span><span class="sxs-lookup"><span data-stu-id="200e1-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="200e1-106">Pe o linie de ofertă bazată pe catalogul de produse, aveți posibilitatea să suprascrieți prețul la roluri și categorii direct pe linia de ofertă, deoarece fiecare linie de ofertă indică exact un element de catalog.</span><span class="sxs-lookup"><span data-stu-id="200e1-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="200e1-107">Cu toate acestea, pe o linie de ofertă bazată pe proiect, nu puteți suprascrie prețul la roluri și categorii direct pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="200e1-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="200e1-108">Puteți utiliza lista de prețuri a proiectului pentru a lucra cu cele două modele de suprascriere distincte.</span><span class="sxs-lookup"><span data-stu-id="200e1-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="200e1-109">Vă recomandăm să aveți o listă de prețuri separată pentru resursele proiectului și elementele de catalog, din cauza diferențelor de comportament între cele două atunci când suprascrieți tarifarea.</span><span class="sxs-lookup"><span data-stu-id="200e1-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="200e1-110">Fiecare dintre următoarele entități poate avea una sau mai multe liste de prețuri de vânzare asociate pentru tarifarea de proiect:</span><span class="sxs-lookup"><span data-stu-id="200e1-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="200e1-111">(Cont) client</span><span class="sxs-lookup"><span data-stu-id="200e1-111">Customer (account)</span></span> 
- <span data-ttu-id="200e1-112">Oportunitate</span><span class="sxs-lookup"><span data-stu-id="200e1-112">Opportunity</span></span> 
- <span data-ttu-id="200e1-113">Ofertă</span><span class="sxs-lookup"><span data-stu-id="200e1-113">Quote</span></span> 
- <span data-ttu-id="200e1-114">Contract de proiect</span><span class="sxs-lookup"><span data-stu-id="200e1-114">Project Contract</span></span>

<span data-ttu-id="200e1-115">Asocierea acestor entități cu o listă de prețuri este indicată de listele de prețuri ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="200e1-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="200e1-116">Aveți posibilitatea să asociați una sau mai multe liste de prețuri cu entitățile de vânzări Client, Oportunitate, Ofertă și Contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="200e1-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="200e1-117">O listă de prețuri implicită a proiectului nu este introdusă automat într-o înregistrare de client.</span><span class="sxs-lookup"><span data-stu-id="200e1-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="200e1-118">Cu toate acestea, aveți posibilitatea să atașați manual o listă de prețuri de proiect la înregistrarea clientului.</span><span class="sxs-lookup"><span data-stu-id="200e1-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="200e1-119">Totuși, ar trebui să atașați manual o listă de prețuri de proiect numai atunci când aveți un acord de tarifare particularizat cu clientul.</span><span class="sxs-lookup"><span data-stu-id="200e1-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="200e1-120">Atunci când o listă de prețuri de proiect este atașată la o entitate de vânzări, următoarele informații sunt validate:</span><span class="sxs-lookup"><span data-stu-id="200e1-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="200e1-121">Lista de prețuri are un context de **Vânzări**.</span><span class="sxs-lookup"><span data-stu-id="200e1-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="200e1-122">Moneda listei de prețuri corespunde monedei clientului.</span><span class="sxs-lookup"><span data-stu-id="200e1-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="200e1-123">Pe un contract de proiect, este utilizată următoarea ordine de prioritate pentru a seta automat liste de proiect corelate:</span><span class="sxs-lookup"><span data-stu-id="200e1-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="200e1-124">Ofertă</span><span class="sxs-lookup"><span data-stu-id="200e1-124">Quote</span></span>
2. <span data-ttu-id="200e1-125">Oportunitate</span><span class="sxs-lookup"><span data-stu-id="200e1-125">Opportunity</span></span>
3. <span data-ttu-id="200e1-126">Client</span><span class="sxs-lookup"><span data-stu-id="200e1-126">Customer</span></span> 
4. <span data-ttu-id="200e1-127">Setări globale</span><span class="sxs-lookup"><span data-stu-id="200e1-127">Global settings</span></span> 

<span data-ttu-id="200e1-128">Atunci când o listă de prețuri de proiect este introdusă în mod implicit, sistemul validează că moneda se potrivește cu moneda clientului și că listele de prețuri implicite care au fost introduse au un context de **Vânzări**.</span><span class="sxs-lookup"><span data-stu-id="200e1-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="200e1-129">Aveți posibilitatea să asociați mai multe liste de prețuri cu entitățile Client, Oportunitate, Ofertă și Contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="200e1-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="200e1-130">Această capacitate acceptă prețuri implicite specifice datei pentru un contract de proiect de lungă durată, în cazul căruia este posibil să aveți nevoie de mai mult de o listă de prețuri pentru a ține cont de actualizările de preț care au loc din cauza inflației.</span><span class="sxs-lookup"><span data-stu-id="200e1-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="200e1-131">Cu toate acestea, în cazul în care listele de prețuri pe care le asociați cu entitatea Client, Oportunitate, Ofertă sau Contract de proiect au o suprapunere a efectivității datelor, prețurile implicite ar putea fi incorecte.</span><span class="sxs-lookup"><span data-stu-id="200e1-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="200e1-132">De aceea, ar trebui să vă asigurați că listele de prețuri de proiect care au o suprapunere a efectivității datelor nu sunt asociate cu aceste entități.</span><span class="sxs-lookup"><span data-stu-id="200e1-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]