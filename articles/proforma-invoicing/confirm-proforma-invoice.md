---
title: Confirmarea unei facturi proforma
description: Acest subiect oferă informații despre confirmarea unei facturi proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082641"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="d6709-103">Confirmarea unei facturi proforma</span><span class="sxs-lookup"><span data-stu-id="d6709-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="d6709-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="d6709-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d6709-105">După confirmarea unei facturi proforma, starea facturii proiectului se actualizează la **Confirmat**.</span><span class="sxs-lookup"><span data-stu-id="d6709-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="d6709-106">Când o factură este confirmată, aceasta devine doar în citire.</span><span class="sxs-lookup"><span data-stu-id="d6709-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="d6709-107">În continuare, factura poate fi corectată numai dacă există corecții sau credite inițiate de clienți sau când este marcată ca plătită.</span><span class="sxs-lookup"><span data-stu-id="d6709-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="d6709-108">Următorul tabel listează datele efective create de sistem.</span><span class="sxs-lookup"><span data-stu-id="d6709-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="d6709-109">Aceste date reale sunt create atunci când anumite operațiuni sunt efectuate pe schița facturii proiectului înainte de a fi confirmată.</span><span class="sxs-lookup"><span data-stu-id="d6709-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="d6709-110">
                    <strong>Scenariu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d6709-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="d6709-111">
                    <strong>Date reale create la confirmare</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d6709-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6709-112">Facturarea unei tranzacții de timp fără modificări pe schița de factură.</span><span class="sxs-lookup"><span data-stu-id="d6709-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-113">O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="d6709-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-114">O valoare reală de vânzări facturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="d6709-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d6709-115">Facturarea unei tranzacții în timp care a fost editată pentru a reduce cantitatea.</span><span class="sxs-lookup"><span data-stu-id="d6709-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-116">O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="d6709-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-117">O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="d6709-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-118">O nouă vânzare nefacturată efectivă care nu se taxează pentru orele rămase și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="d6709-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6709-119">Facturarea unei tranzacții în timp care a fost editată pentru a mări cantitatea.</span><span class="sxs-lookup"><span data-stu-id="d6709-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-120">O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="d6709-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-121">O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="d6709-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6709-122">Facturarea unei tranzacții pentru o cheltuială fără modificări pe schița de factură.</span><span class="sxs-lookup"><span data-stu-id="d6709-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-123">O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="d6709-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-124">O valoare reală de vânzări nefacturate care se taxează pentru cantitatea și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="d6709-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d6709-125">Facturarea unei tranzacții pentru o cheltuială care a fost editată pentru a reduce cantitatea.</span><span class="sxs-lookup"><span data-stu-id="d6709-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-126">O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="d6709-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-127">O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="d6709-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-128">O nouă vânzare nefacturată efectivă care nu se taxează pentru cantitatea rămasă și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și un echivalent al vânzărilor facturate efective.</span><span class="sxs-lookup"><span data-stu-id="d6709-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6709-129">Facturarea unei tranzacții pentru o cheltuială care a fost editată pentru a mări cantitatea.</span><span class="sxs-lookup"><span data-stu-id="d6709-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-130">O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="d6709-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-131">O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="d6709-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d6709-132">Facturarea unei taxe.</span><span class="sxs-lookup"><span data-stu-id="d6709-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-133">O inversare a vânzărilor nefacturate pentru valoarea taxei pe linia de jurnal originală.</span><span class="sxs-lookup"><span data-stu-id="d6709-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-134">O valoare reală de vânzări facturate pentru cantitatea și suma din linia de jurnal de taxă inițială.</span><span class="sxs-lookup"><span data-stu-id="d6709-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d6709-135">Facturarea unui jalon.</span><span class="sxs-lookup"><span data-stu-id="d6709-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d6709-136">O vânzare facturată efectivă pentru suma de jalon de pe jalonul original de pe linia contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="d6709-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
