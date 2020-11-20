---
title: Estimări de resurse
description: Acest subiect furnizează informații despre cum sunt calculate estimările de resurse în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127390"
---
# <a name="resource-estimates"></a><span data-ttu-id="06fe6-103">Estimări de resurse</span><span class="sxs-lookup"><span data-stu-id="06fe6-103">Resource estimates</span></span>

<span data-ttu-id="06fe6-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="06fe6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06fe6-105">Estimările resurselor provin din eforturi în etape temporale care sunt definite în structura detaliată a proiectului împreună cu dimensiunile de preț aplicabile.</span><span class="sxs-lookup"><span data-stu-id="06fe6-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="06fe6-106">De obicei, calculul este **rata/oră pentru fiecare rol x ore.**</span><span class="sxs-lookup"><span data-stu-id="06fe6-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="06fe6-107">Efortul pe etape pentru fiecare resursă este stocat în înregistrarea de alocare a resurselor.</span><span class="sxs-lookup"><span data-stu-id="06fe6-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="06fe6-108">Prețul este stocat într-o listă de prețuri predefinită.</span><span class="sxs-lookup"><span data-stu-id="06fe6-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="06fe6-109">Conversia unității se aplică pe baza listei de prețuri aplicabile.</span><span class="sxs-lookup"><span data-stu-id="06fe6-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimări de resursă](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="06fe6-111">Prețul de cost implicit și valuta de cost</span><span class="sxs-lookup"><span data-stu-id="06fe6-111">Default cost price and cost currency</span></span>

<span data-ttu-id="06fe6-112">Prețurile de cost sunt implicite din Unitatea Organizațională.</span><span class="sxs-lookup"><span data-stu-id="06fe6-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="06fe6-113">Rata de facturare implicită și moneda de vânzare</span><span class="sxs-lookup"><span data-stu-id="06fe6-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="06fe6-114">Prețurile de vânzare se aplică o dată pe tranzacție.</span><span class="sxs-lookup"><span data-stu-id="06fe6-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="06fe6-115">Ierarhia pentru lista de prețuri de vânzare implicită este următoarea:</span><span class="sxs-lookup"><span data-stu-id="06fe6-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="06fe6-116">Organizație</span><span class="sxs-lookup"><span data-stu-id="06fe6-116">Organization</span></span>
2. <span data-ttu-id="06fe6-117">Client</span><span class="sxs-lookup"><span data-stu-id="06fe6-117">Customer</span></span>
3. <span data-ttu-id="06fe6-118">Ofertă/contract</span><span class="sxs-lookup"><span data-stu-id="06fe6-118">Quote/contract</span></span>
