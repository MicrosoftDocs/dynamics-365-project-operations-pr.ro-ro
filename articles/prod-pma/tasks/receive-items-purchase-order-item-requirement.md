---
title: Primiți articole din comanda de achiziție din cerința articolului
description: Acest subiect explică modul de primire a articolelor dintr-o comandă de achiziție dintr-o cerință de articol.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011701"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="13fea-103">Primiți articole din comanda de achiziție din cerința articolului</span><span class="sxs-lookup"><span data-stu-id="13fea-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13fea-104">Acest subiect explică modul de primire a articolelor dintr-o comandă de achiziție dintr-o cerință de articol.</span><span class="sxs-lookup"><span data-stu-id="13fea-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="13fea-105">Utilizând o cerință de articol în loc de o tranzacție de articol, puteți planifica livrarea chiar înainte ca articolul să fie utilizat efectiv, să creați o comandă de achiziție, să includeți articolul în cadrul acordului comercial și să includeți cerința articolului în planificarea producției.</span><span class="sxs-lookup"><span data-stu-id="13fea-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="13fea-106">Această sarcină utilizează setul de date USSI.</span><span class="sxs-lookup"><span data-stu-id="13fea-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="13fea-107">În panoul de navigare, accesați **Module > Management de proiect și contabilitate > Proiecte > Toate proiectele**.</span><span class="sxs-lookup"><span data-stu-id="13fea-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="13fea-108">În listă, selectați linkul din rândul doriți.</span><span class="sxs-lookup"><span data-stu-id="13fea-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="13fea-109">În panoul de acțiuni, selectați **Plan**.</span><span class="sxs-lookup"><span data-stu-id="13fea-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="13fea-110">Selectați **Cerințele articolului**.</span><span class="sxs-lookup"><span data-stu-id="13fea-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="13fea-111">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="13fea-111">Select **New**.</span></span>
6. <span data-ttu-id="13fea-112">În noul rând, introduceți sau selectați o valoare în câmpul **Numărul de articol**.</span><span class="sxs-lookup"><span data-stu-id="13fea-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="13fea-113">În câmpul **Cantitate**, introduceți un număr.</span><span class="sxs-lookup"><span data-stu-id="13fea-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="13fea-114">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="13fea-114">Select **Save**.</span></span>
9. <span data-ttu-id="13fea-115">În panoul de acțiuni, selectați **Gestionare**.</span><span class="sxs-lookup"><span data-stu-id="13fea-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="13fea-116">Selectați **Funcții**.</span><span class="sxs-lookup"><span data-stu-id="13fea-116">Select **Functions**.</span></span>
11. <span data-ttu-id="13fea-117">Selectați **Creați comanda de achiziție**.</span><span class="sxs-lookup"><span data-stu-id="13fea-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="13fea-118">Selectați caseta de selectare **Includeți tot**.</span><span class="sxs-lookup"><span data-stu-id="13fea-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="13fea-119">În câmpul **Cont distribuitor**, introduceți sau selectați o valoare.</span><span class="sxs-lookup"><span data-stu-id="13fea-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="13fea-120">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="13fea-120">Select **OK**.</span></span>
15. <span data-ttu-id="13fea-121">În panoul de navigare, selectați **Module > Conturi furnizori > Comenzi de achiziție > Toate comenzile de achiziție**.</span><span class="sxs-lookup"><span data-stu-id="13fea-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="13fea-122">În listă, selectați linkul din rândul doriți.</span><span class="sxs-lookup"><span data-stu-id="13fea-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="13fea-123">În panoul de acțiuni, selectați **Achiziție**.</span><span class="sxs-lookup"><span data-stu-id="13fea-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="13fea-124">Selectați **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="13fea-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="13fea-125">În panoul de acțiuni, selectați **Primiți**.</span><span class="sxs-lookup"><span data-stu-id="13fea-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="13fea-126">Selectați **Chitanță de produs**.</span><span class="sxs-lookup"><span data-stu-id="13fea-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="13fea-127">În câmpul **Chitanță de produs**, tastați o valoare.</span><span class="sxs-lookup"><span data-stu-id="13fea-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="13fea-128">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="13fea-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]