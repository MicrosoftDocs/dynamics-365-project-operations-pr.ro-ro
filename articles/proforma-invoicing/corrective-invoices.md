---
title: Facturi corectate
description: Acest subiect oferă informații despre facturi corectate.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082964"
---
# <a name="corrected-invoices"></a><span data-ttu-id="6bc5f-103">Facturi corectate</span><span class="sxs-lookup"><span data-stu-id="6bc5f-103">Corrected invoices</span></span>

<span data-ttu-id="6bc5f-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="6bc5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6bc5f-105">Facturile PSA confirmate pot fi editate.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="6bc5f-106">Când editați o factură confirmată, se creează o schiță a facturii corectate.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="6bc5f-107">Întrucât ipoteza este că doriți să inversați toate tranzacțiile și cantitățile din factura originală, această factură corectată include toate tranzacțiile din factura originală și toate cantitățile de aici sunt zero (0).</span><span class="sxs-lookup"><span data-stu-id="6bc5f-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="6bc5f-108">Când tranzacțiile nu necesită corecție, puteți să le eliminați din proiectul de factură rectificativă.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="6bc5f-109">Pentru a inversa sau returna numai o cantitate parțială, puteți să editați câmpul Cantitate în detaliul liniei.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="6bc5f-110">Dacă deschideți detaliul de linie factură, puteți să vedeți cantitatea inițială de factură.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="6bc5f-111">Aveți posibilitatea să editați apoi cantitatea curentă de factură, astfel încât să fie mai mică sau mai mare decât cantitatea inițială de factură.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="6bc5f-112">Când confirmați o factură rectificativă, valoarea reală a vânzărilor inițiale facturate este inversată și se creează o nouă valoare reală de vânzări facturate.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="6bc5f-113">În cazul în care cantitatea a fost redusă, diferența va provoca o nouă valoare reală de vânzări nefacturate pentru a fi create.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="6bc5f-114">De exemplu, dacă vânzarea facturată inițial a fost de opt ore și detaliile liniei de factură corectate are o cantitate redusă de șase ore, liniile facturate origniale sunt inversate și sunt create două noi valori reale:</span><span class="sxs-lookup"><span data-stu-id="6bc5f-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="6bc5f-115">O valoare reală de vânzări facturate timp de șase ore.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="6bc5f-116">O valoare reală de vânzări nefacturate pentru restul de două ore.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="6bc5f-117">Această tranzacție poate fi facturată ulterior sau poate fi marcată ca netaxabilă, în funcție de negocierile cu clientul.</span><span class="sxs-lookup"><span data-stu-id="6bc5f-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
