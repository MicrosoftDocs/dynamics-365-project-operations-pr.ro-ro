---
title: Linii de contract bazate pe produs de cost - simplificat
description: Acest subiect oferă informații despre creare
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764474"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="a6e30-103">Linii de contract bazate pe produs de cost - simplificat</span><span class="sxs-lookup"><span data-stu-id="a6e30-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="a6e30-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="a6e30-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a6e30-105">Liniile contractuale pe bază de produse în Dynamics 365 Project Operations includ câmpul **Preț de cost**, care stochează prețul de cost al produsului pentru calculele de profitabilitate din aval.</span><span class="sxs-lookup"><span data-stu-id="a6e30-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="a6e30-106">Când se creează o linie contractuală bazată pe produs pentru un produs de catalog, costul liniei reiese implicit din câmpul **Cost standard** din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="a6e30-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="a6e30-107">Câmpul **Cost standard** din catalogul de produse este configurat în moneda de bază a Organizației.</span><span class="sxs-lookup"><span data-stu-id="a6e30-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="a6e30-108">Când costul unitar este implicit pe linia contractului, acesta este convertit în moneda de vânzare din contract.</span><span class="sxs-lookup"><span data-stu-id="a6e30-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="a6e30-109">Costul unitar pe o linie de contract pe bază de produs</span><span class="sxs-lookup"><span data-stu-id="a6e30-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="a6e30-110">Având un cost unitar pe o linie de contract bazată pe produse, vă permite a avea costuri diferite ale produsului pentru fiecare vânzare a unei unități.</span><span class="sxs-lookup"><span data-stu-id="a6e30-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="a6e30-111">Deși nu sunt întotdeauna necesare, există anumite scenarii în care costul produsului poate fi redus pentru client de către furnizor.</span><span class="sxs-lookup"><span data-stu-id="a6e30-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="a6e30-112">Luați în considerare următorul scenariu:</span><span class="sxs-lookup"><span data-stu-id="a6e30-112">Consider the following scenario:</span></span>

<span data-ttu-id="a6e30-113">Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="a6e30-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="a6e30-114">Fabrikam oferă servicii de instalare, dar brațele robotice provin de la Trey Research.</span><span class="sxs-lookup"><span data-stu-id="a6e30-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="a6e30-115">Dacă instalarea brațelor robotizate la Adatum Corporation deschide o nouă verticală a industriei pentru brațele de la Trey Research, aceștia ar putea acorda Fabrikam o reducere specială pentru această ofertă.</span><span class="sxs-lookup"><span data-stu-id="a6e30-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="a6e30-116">În acest caz, Fabrikam creează o linie contractuală bazată pe produse pentru Brațe robotice.</span><span class="sxs-lookup"><span data-stu-id="a6e30-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="a6e30-117">Pentru acest contract se introduce un cost pe unitate.</span><span class="sxs-lookup"><span data-stu-id="a6e30-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="a6e30-118">Costul este diferit de costul brațelor robotice de la Trey Research.</span><span class="sxs-lookup"><span data-stu-id="a6e30-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
