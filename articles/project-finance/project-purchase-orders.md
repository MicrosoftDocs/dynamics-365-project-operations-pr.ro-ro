---
title: Comenzi de achiziție pentru un proiect
description: Acest articol descrie diferitele metode pe care le puteți utiliza pentru a crea comenzi de achiziție pentru un proiect. Metoda pe care o utilizați depinde de scopul comenzii de cumpărare, și de când sunt consumate și taxate într-un proiect articolele achiziționate.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754733"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="8518b-104">Comenzi de achiziție pentru un proiect</span><span class="sxs-lookup"><span data-stu-id="8518b-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8518b-105">Acest articol descrie diferitele metode pe care le puteți utiliza pentru a crea comenzi de achiziție pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="8518b-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="8518b-106">Metoda pe care o utilizați depinde de scopul comenzii de cumpărare, și de când sunt consumate și taxate într-un proiect articolele achiziționate.</span><span class="sxs-lookup"><span data-stu-id="8518b-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="8518b-107">Metode de creare a unei comenzi de achiziție</span><span class="sxs-lookup"><span data-stu-id="8518b-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="8518b-108">Puteți utiliza una dintre următoarele metode pentru a crea o comandă de achiziție în managementul de proiect și contabilitate.</span><span class="sxs-lookup"><span data-stu-id="8518b-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="8518b-109">Scopul comenzii de achiziție determină când este consumată comanda de achiziție și, prin urmare, când sunt taxate articolele către un proiect.</span><span class="sxs-lookup"><span data-stu-id="8518b-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8518b-110">Metodă</span><span class="sxs-lookup"><span data-stu-id="8518b-110">Method</span></span></th>
<th><span data-ttu-id="8518b-111">Scop</span><span class="sxs-lookup"><span data-stu-id="8518b-111">Purpose</span></span></th>
<th><span data-ttu-id="8518b-112">Consumul de articole</span><span class="sxs-lookup"><span data-stu-id="8518b-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8518b-113">Creați o comandă de achiziție direct dintr-un proiect.</span><span class="sxs-lookup"><span data-stu-id="8518b-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="8518b-114">Utilizați această metodă pentru a achiziționa articole de la un furnizor extern pentru consum în cadrul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="8518b-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="8518b-115">Puteți crea comanda de cumpărare în două moduri:</span><span class="sxs-lookup"><span data-stu-id="8518b-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="8518b-116">Din proiectul în sine.</span><span class="sxs-lookup"><span data-stu-id="8518b-116">From the project itself.</span></span> <span data-ttu-id="8518b-117">În acest caz, proiectul este deja definit pentru comanda de cumpărare.</span><span class="sxs-lookup"><span data-stu-id="8518b-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="8518b-118">Navigând la comanda de achiziție a proiectului.</span><span class="sxs-lookup"><span data-stu-id="8518b-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="8518b-119">Trebuie să selectați atât furnizorul, cât și proiectul pentru a crea comanda de achiziție.</span><span class="sxs-lookup"><span data-stu-id="8518b-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="8518b-120">Articolele sunt consumate atunci când factura furnizorului este actualizată.</span><span class="sxs-lookup"><span data-stu-id="8518b-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8518b-121">Creați o comandă de cumpărare dintr-o comandă de vânzare.</span><span class="sxs-lookup"><span data-stu-id="8518b-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="8518b-122">Utilizați această metodă pentru a achiziționa articole atunci când creați o comandă de vânzare dintr-un proiect.</span><span class="sxs-lookup"><span data-stu-id="8518b-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="8518b-123">Articolele sunt consumate atunci când comanda de vânzare este facturată către client.</span><span class="sxs-lookup"><span data-stu-id="8518b-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8518b-124">Creați o comandă de cumpărare dintr-o cerință de articol.</span><span class="sxs-lookup"><span data-stu-id="8518b-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="8518b-125">Utilizați această metodă pentru a achiziționa articole atunci când creați o cerință de articol dintr-un proiect.</span><span class="sxs-lookup"><span data-stu-id="8518b-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="8518b-126">Articolele sunt consumate la actualizarea bonului de ambalare pentru cerința articolului.</span><span class="sxs-lookup"><span data-stu-id="8518b-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="8518b-127">Când actualizați factura furnizorului sau bonul de ambalare, vi se solicită să actualizați bonul de ambalare pentru cerința articolului.</span><span class="sxs-lookup"><span data-stu-id="8518b-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="8518b-128">Pentru mai multe informații, consultați [Primiți articole din comanda de achiziție din cerința articolului](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="8518b-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

