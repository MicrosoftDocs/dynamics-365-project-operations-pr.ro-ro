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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286533"
---
# <a name="resource-estimates"></a><span data-ttu-id="23f6e-103">Estimări de resurse</span><span class="sxs-lookup"><span data-stu-id="23f6e-103">Resource estimates</span></span>

<span data-ttu-id="23f6e-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="23f6e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23f6e-105">Estimările resurselor provin din eforturi în etape temporale care sunt definite în structura detaliată a proiectului împreună cu dimensiunile de preț aplicabile.</span><span class="sxs-lookup"><span data-stu-id="23f6e-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="23f6e-106">De obicei, calculul este **rata/oră pentru fiecare rol x ore.**</span><span class="sxs-lookup"><span data-stu-id="23f6e-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="23f6e-107">Efortul pe etape pentru fiecare resursă este stocat în înregistrarea de alocare a resurselor.</span><span class="sxs-lookup"><span data-stu-id="23f6e-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="23f6e-108">Prețul este stocat într-o listă de prețuri predefinită.</span><span class="sxs-lookup"><span data-stu-id="23f6e-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="23f6e-109">Conversia unității se aplică pe baza listei de prețuri aplicabile.</span><span class="sxs-lookup"><span data-stu-id="23f6e-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimări de resursă](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="23f6e-111">Prețul de cost implicit și valuta de cost</span><span class="sxs-lookup"><span data-stu-id="23f6e-111">Default cost price and cost currency</span></span>

<span data-ttu-id="23f6e-112">Prețurile de cost sunt implicite din Unitatea Organizațională.</span><span class="sxs-lookup"><span data-stu-id="23f6e-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="23f6e-113">Rata de facturare implicită și moneda de vânzare</span><span class="sxs-lookup"><span data-stu-id="23f6e-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="23f6e-114">Prețurile de vânzare se aplică o dată pe tranzacție.</span><span class="sxs-lookup"><span data-stu-id="23f6e-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="23f6e-115">Ierarhia pentru lista de prețuri de vânzare implicită este următoarea:</span><span class="sxs-lookup"><span data-stu-id="23f6e-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="23f6e-116">Organizație</span><span class="sxs-lookup"><span data-stu-id="23f6e-116">Organization</span></span>
2. <span data-ttu-id="23f6e-117">Client</span><span class="sxs-lookup"><span data-stu-id="23f6e-117">Customer</span></span>
3. <span data-ttu-id="23f6e-118">Ofertă/contract</span><span class="sxs-lookup"><span data-stu-id="23f6e-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]