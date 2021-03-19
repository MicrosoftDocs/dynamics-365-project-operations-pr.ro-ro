---
title: Confirmarea unei facturi proforma - simplificat
description: Acest subiect furnizează informații despre confirmarea facturilor proforma în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274293"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="42039-103">Confirmarea unei facturi proforma - simplificat</span><span class="sxs-lookup"><span data-stu-id="42039-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="42039-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="42039-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="42039-105">După confirmarea unei facturi proforma, starea facturii proiectului se actualizează la **Confirmat**.</span><span class="sxs-lookup"><span data-stu-id="42039-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="42039-106">Când o factură este confirmată, aceasta devine doar în citire.</span><span class="sxs-lookup"><span data-stu-id="42039-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="42039-107">În continuare, factura poate fi corectată numai dacă există corecții sau credite inițiate de clienți sau dacă factura este marcată ca plătită.</span><span class="sxs-lookup"><span data-stu-id="42039-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="42039-108">Următorul tabel listează datele efective create de sistem.</span><span class="sxs-lookup"><span data-stu-id="42039-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="42039-109">Aceste date reale sunt create atunci când anumite operațiuni sunt efectuate pe schița facturii proiectului înainte de a fi confirmată.</span><span class="sxs-lookup"><span data-stu-id="42039-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="42039-110">
                    <strong>Scenariu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42039-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="42039-111">
                    <strong>Date reale create la confirmare</strong>
                </span><span class="sxs-lookup"><span data-stu-id="42039-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-112">Facturarea unui avans sau onorariu</span><span class="sxs-lookup"><span data-stu-id="42039-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-113">O valoare reală de vânzări facturate de tip <strong>Onorariu</strong> este creată pentru suma de pe avans sau onorariu.</span><span class="sxs-lookup"><span data-stu-id="42039-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-114">O valoare reală de vânzări nefacturate a unei sume negative a onorariului sau avansului care urmează a fi utilizată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="42039-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-115">După reconcilierea completă a unui onorariu sau avans pe o factură.</span><span class="sxs-lookup"><span data-stu-id="42039-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-116">O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="42039-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="42039-117">Această sumă este pozitivă, deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.</span><span class="sxs-lookup"><span data-stu-id="42039-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-118">O valoare reală de vânzări facturate pentru suma de pe această factură.</span><span class="sxs-lookup"><span data-stu-id="42039-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="42039-119">După reconcilierea parțială a unui onorariu sau avans pe o factură.</span><span class="sxs-lookup"><span data-stu-id="42039-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-120">O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="42039-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="42039-121">Această sumă este pozitivă, deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.</span><span class="sxs-lookup"><span data-stu-id="42039-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-122">O valoare reală de vânzări facturate pentru suma de pe această factură.</span><span class="sxs-lookup"><span data-stu-id="42039-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-123">O valoare negativă reală de vânzări nefacturate a sumei restante a onorariului sau avansului care urmează a fi utilizată pentru reconciliere pe facturile viitoare.</span><span class="sxs-lookup"><span data-stu-id="42039-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-124">Facturarea unei tranzacții de timp fără modificări pe schița de factură.</span><span class="sxs-lookup"><span data-stu-id="42039-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-125">O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="42039-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-126">O valoare reală de vânzări facturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="42039-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="42039-127">Facturarea unei tranzacții în timp care a fost editată pentru a reduce cantitatea.</span><span class="sxs-lookup"><span data-stu-id="42039-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-128">O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="42039-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-129">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor reale și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="42039-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-130">O nouă valoare reală a vânzărilor nefacturate care nu se taxează pentru orele rămase și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor reale și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="42039-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-131">Facturarea unei tranzacții în timp care a fost editată pentru a mări cantitatea.</span><span class="sxs-lookup"><span data-stu-id="42039-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-132">O inversare a vânzărilor nefacturate pentru ore și sumă conform aprobării inițiale a timpului.</span><span class="sxs-lookup"><span data-stu-id="42039-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-133">O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="42039-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-134">Facturarea unei tranzacții pentru o cheltuială fără modificări pe schița de factură.</span><span class="sxs-lookup"><span data-stu-id="42039-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-135">O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="42039-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-136">O valoare reală de vânzări facturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii</span><span class="sxs-lookup"><span data-stu-id="42039-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="42039-137">Facturarea unei tranzacții pentru o cheltuială care a fost editată pentru a reduce cantitatea.</span><span class="sxs-lookup"><span data-stu-id="42039-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-138">O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="42039-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-139">O nouă vânzare nefacturată efectivă care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate efective și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="42039-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-140">O nouă valoare reală a vânzărilor nefacturate care nu se taxează pentru cantitatea rămasă și suma după deducerea cifrelor corectate din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate reale și un echivalent al vânzărilor facturate efective.</span><span class="sxs-lookup"><span data-stu-id="42039-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-141">Facturarea unei tranzacții pentru o cheltuială care a fost editată pentru a mări cantitatea.</span><span class="sxs-lookup"><span data-stu-id="42039-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-142">O inversare a vânzărilor nefacturate pentru cantitatea și suma conform aprobării inițiale a cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="42039-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-143">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a vânzărilor nefacturate reale și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="42039-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="42039-144">Facturarea unei taxe.</span><span class="sxs-lookup"><span data-stu-id="42039-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-145">O inversare a vânzărilor nefacturate pentru valoarea taxei pe linia de jurnal originală.</span><span class="sxs-lookup"><span data-stu-id="42039-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-146">O valoare reală de vânzări facturate pentru cantitatea și suma din linia de jurnal de taxă inițială.</span><span class="sxs-lookup"><span data-stu-id="42039-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="42039-147">Facturarea unui jalon.</span><span class="sxs-lookup"><span data-stu-id="42039-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-148">O vânzare facturată efectivă pentru suma de jalon de pe jalonul original de pe linia contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="42039-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="42039-149">Facturarea unei linii contractuale pe bază de produse.</span><span class="sxs-lookup"><span data-stu-id="42039-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="42039-150">O valoare reală de vânzări facturate pentru linia de produse cu cantitatea și suma provenite din linia de contract pe bază de produs.</span><span class="sxs-lookup"><span data-stu-id="42039-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]