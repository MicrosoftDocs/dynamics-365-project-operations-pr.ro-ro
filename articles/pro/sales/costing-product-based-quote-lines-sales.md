---
title: Linii de oferte bazate pe produs de cost
description: Acest subiect oferă informații despre aplicarea unui preț de cost unei linii de ofertă pe bază de produs.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c08ac3b0f24dda19489bad6e667a50b67b8ce3ec
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273663"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="1f9aa-103">Linii de oferte bazate pe produs de cost</span><span class="sxs-lookup"><span data-stu-id="1f9aa-103">Costing product-based quote lines</span></span>

<span data-ttu-id="1f9aa-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="1f9aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1f9aa-105">Linii de ofertă bazate pe produse din Dynamics 365 Project Operations au și un câmp **Preț de cost**.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="1f9aa-106">Acest câmp este utilizat pentru a urmări prețul de cost al produsului pe linia de ofertă și pentru calculele de profitabilitate din aval.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="1f9aa-107">Atunci când se creează o linie de ofertă bazată pe produs pentru un produs din catalog, costul liniei de ofertă bazată pe produs este implicit de la **Cost standard** din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="1f9aa-108">Câmpul de cost standard din catalogul de produse este configurat în moneda de bază a Organizației.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="1f9aa-109">Costul unitar implicit pe linia de cotare bazată pe produs este convertit în moneda de vânzare din cotare.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="1f9aa-110">Costul unitar pe o linie de ofertă pe bază de produs</span><span class="sxs-lookup"><span data-stu-id="1f9aa-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="1f9aa-111">Scopul de a avea un cost unitar pe o linie de ofertă bazată pe produs este de a permite costuri diferite pentru un produs pentru fiecare vânzare.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="1f9aa-112">Acesta nu este un scenariu tipic, dar uneori costul produsului poate fi redus de furnizor, în funcție de clientul vânzării finale.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="1f9aa-113">De exemplu:</span><span class="sxs-lookup"><span data-stu-id="1f9aa-113">For example:</span></span>

<span data-ttu-id="1f9aa-114">Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="1f9aa-115">Fabrikam oferă servicii de instalare, dar brațele robotizate sunt achiziționate de la robotica Trey.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="1f9aa-116">Dacă instalarea brațelor robotizate la A Datum Corporation deschide o nouă verticală a industriei pentru brațele robotizate ale lui Trey, Trey ar putea acorda Fabrikam o reducere specială pentru această ofertă.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="1f9aa-117">În acest caz, Fabrikam va crea o linie de cotare bazată pe produse pentru Robotic Arms și va introduce un cost unitar special pentru acest preț.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="1f9aa-118">Acest cost este diferit de costul standard al Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="1f9aa-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]