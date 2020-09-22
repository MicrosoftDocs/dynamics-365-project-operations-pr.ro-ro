---
title: Primiți articole din comanda de achiziție din cerința articolului
description: Acest subiect explică modul de primire a articolelor dintr-o comandă de achiziție dintr-o cerință de articol.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754681"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="27463-103">Primiți articole din comanda de achiziție din cerința articolului</span><span class="sxs-lookup"><span data-stu-id="27463-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27463-104">Acest subiect explică modul de primire a articolelor dintr-o comandă de achiziție dintr-o cerință de articol.</span><span class="sxs-lookup"><span data-stu-id="27463-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="27463-105">Utilizând o cerință de articol în loc de o tranzacție de articol, puteți planifica livrarea chiar înainte ca articolul să fie utilizat efectiv, să creați o comandă de achiziție, să includeți articolul în cadrul acordului comercial și să includeți cerința articolului în planificarea producției.</span><span class="sxs-lookup"><span data-stu-id="27463-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="27463-106">Această sarcină utilizează setul de date USSI.</span><span class="sxs-lookup"><span data-stu-id="27463-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="27463-107">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Proiecte > Toate proiectele**.</span><span class="sxs-lookup"><span data-stu-id="27463-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="27463-108">În listă, selectați linkul din rândul doriți.</span><span class="sxs-lookup"><span data-stu-id="27463-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="27463-109">În panoul de acțiuni, selectați **Plan**.</span><span class="sxs-lookup"><span data-stu-id="27463-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="27463-110">Selectați **Cerințele articolului**.</span><span class="sxs-lookup"><span data-stu-id="27463-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="27463-111">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="27463-111">Select **New**.</span></span>
6. <span data-ttu-id="27463-112">În noul rând, introduceți sau selectați o valoare în câmpul **Numărul de articol**.</span><span class="sxs-lookup"><span data-stu-id="27463-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="27463-113">În câmpul **Cantitate**, introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="27463-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="27463-114">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="27463-114">Select **Save**.</span></span>
9. <span data-ttu-id="27463-115">În panoul de acțiuni, selectați **Gestionare**.</span><span class="sxs-lookup"><span data-stu-id="27463-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="27463-116">Selectați **Funcții**.</span><span class="sxs-lookup"><span data-stu-id="27463-116">Select **Functions**.</span></span>
11. <span data-ttu-id="27463-117">Selectați **Creați comanda de achiziție**.</span><span class="sxs-lookup"><span data-stu-id="27463-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="27463-118">Selectați caseta de selectare **Includeți tot**.</span><span class="sxs-lookup"><span data-stu-id="27463-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="27463-119">În câmpul **Cont distribuitor**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="27463-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="27463-120">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="27463-120">Select **OK**.</span></span>
15. <span data-ttu-id="27463-121">În panoul de navigare, selectați **Module > Conturi furnizori > Comenzi de achiziție > Toate comenzile de achiziție**.</span><span class="sxs-lookup"><span data-stu-id="27463-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="27463-122">În listă, selectați linkul din rândul doriți.</span><span class="sxs-lookup"><span data-stu-id="27463-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="27463-123">În panoul de acțiuni, selectați **Achiziție**.</span><span class="sxs-lookup"><span data-stu-id="27463-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="27463-124">Selectați **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="27463-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="27463-125">În panoul de acțiuni, selectați **Primiți**.</span><span class="sxs-lookup"><span data-stu-id="27463-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="27463-126">Selectați **Chitanță de produs**.</span><span class="sxs-lookup"><span data-stu-id="27463-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="27463-127">În câmpul **Chitanță de produs**, tastați o valoare.</span><span class="sxs-lookup"><span data-stu-id="27463-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="27463-128">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="27463-128">Select **OK**.</span></span>

