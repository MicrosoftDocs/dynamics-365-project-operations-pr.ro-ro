---
title: Credite și facturi corectate
description: Acest subiect furnizează informații despre facturi corectate în Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082907"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="9cdc8-103">Credite și facturi corectate</span><span class="sxs-lookup"><span data-stu-id="9cdc8-103">Credits and corrected invoices</span></span>

<span data-ttu-id="9cdc8-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="9cdc8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9cdc8-105">O factură de proiect confirmată poate fi corectată pentru a procesa modificările sau creditele negociate cu clientul și managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9cdc8-106">Pentru a face modificări la o factură confirmată, deschideți factura confirmată și selectați **Corectați această factură**.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9cdc8-107">Această selecție nu este disponibilă decât dacă se confirmă factura proiectului.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="9cdc8-108">O nouă schiță de factură este creată din factura confirmată.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9cdc8-109">Toate detaliile liniei de facturare din factura confirmată anterior sunt copiate în noua schiță.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9cdc8-110">Următoarele sunt câteva dintre punctele cheie pentru a înțelege detaliile liniei de pe noua factură corectată:</span><span class="sxs-lookup"><span data-stu-id="9cdc8-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9cdc8-111">Toate cantitățile sunt actualizate la zero.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9cdc8-112">Aplicația presupune că toate articolele facturate sunt creditate integral.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9cdc8-113">Dacă este necesar, puteți actualiza manual aceste cantități pentru a reflecta cantitatea care este facturată și nu cantitatea care este creditată.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9cdc8-114">Pe baza cantității pe care o introduceți, aplicația calculează cantitatea creditată.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9cdc8-115">Această sumă se reflectă în datele reale care se creează la confirmarea facturii corectate.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9cdc8-116">Dacă modificați valoarea impozitului, trebuie să introduceți suma corectă a impozitului și nu valoarea impozitului care este creditată.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9cdc8-117">Liniile contractuale bazate pe produse confirmate anterior nu sunt copiate.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="9cdc8-118">Procesarea corecțiilor pe o factură de proiect bazată pe produs nu este acceptată.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="9cdc8-119">Corecțiile de jalon sunt întotdeauna procesate ca credite complete.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="9cdc8-120">Sumele de onorariu sau avans pot fi corectate dacă clientul a fost facturat pentru o sumă incorectă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="9cdc8-121">Reconcilierile onorariilor și avansurilor pot fi corectate dacă a fost utilizată o sumă incorectă pentru a se concilia cu taxele de pe o factură confirmată anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cdc8-122">Detaliile liniei de facturare care sunt corecții la alte taxe deja facturate au câmpul **Corecție** setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="9cdc8-123">Facturile care au corectat detaliile liniei de facturare au un câmp numit **Are corecții** care este, de asemenea, setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="9cdc8-124">Date reale create la confirmarea unei facturi corective:</span><span class="sxs-lookup"><span data-stu-id="9cdc8-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="9cdc8-125">Mai jos sunt datele reale create de aplicație la confirmarea unei corecții pe baza operațiunilor efectuate pe proiectul de factură corectivă înainte de confirmare.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9cdc8-126">
                    <strong>Scenariu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9cdc8-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9cdc8-127">
                    <strong>Date reale create la confirmare</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9cdc8-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9cdc8-128">Confirmați corectarea unui avans sau a unui onorariu facturat.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9cdc8-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-129">O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9cdc8-130">Această sumă este pozitivă deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-131">Se creează o inversare a datelor reale ale vânzărilor facturate pentru suma din onorariu sau avans pentru a inversa vânzările facturate inițial.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-132">Se creează o nouă vânzare facturată actuală pentru suma corectată de pe onorariu sau linia de factură corectată pe bază de avans.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-133">O valoare reală de vânzări nefacturate cu sumă negativă a onorariului sau a liniei de factură corectate pe bază de avans, care va fi utilizată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9cdc8-134">O confirmare a corectării unui onorariu sau a unui avans reconciliat anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-135">O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9cdc8-136">Această sumă este pozitivă și este menită să anuleze negativul care a fost creat atunci când a avut loc reconcilierea anterioară.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-137">O valoare reală de inversare a vânzărilor facturate pentru suma de pe factura anterioară.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-138">O nouă valoare reală a vânzărilor facturate pentru suma de onorariu corectată care se aplică pe factura corectată.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-139">O valoare reală de vânzări nefacturate cu o sumă negativă din onorariul sau avansul rămas corectat, care va fi utilizată pentru reconciliere pe facturile ulterioare.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cdc8-140">Facturarea creditului integral al unei tranzacții temporare facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-141">O inversare a vânzărilor facturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-142">O nouă valoare reală a vânzărilor nefacturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9cdc8-143">Facturarea creditului parțial pe o tranzacție temporală.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-144">O inversare a vânzărilor facturate pentru orele și suma facturate din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-145">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-146">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cdc8-147">Facturarea creditului integral al unei tranzacții de cheltuială facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-148">O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-149">O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9cdc8-150">Facturarea creditului parțial al unei tranzacții de cheltuială facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-151">O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru o cheltuială.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-152">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corectate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-153">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cdc8-154">Facturarea creditului integral al taxei unei tranzacții facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-155">O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-156">O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9cdc8-157">Facturarea creditului parțial al taxei unei tranzacții facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-158">O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-159">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corective modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9cdc8-160">Facturarea creditului integral al jalonului facturat anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-161">O inversare a vânzărilor facturate pentru suma din detaliile liniei de facturare inițiale pentru jalon.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9cdc8-162">Factura de jalon sau starea de facturare pe linia contractului de proiect este actualizată la **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9cdc8-163">Facturarea creditului parțial al jalonului facturat anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-164">Neacceptat</span><span class="sxs-lookup"><span data-stu-id="9cdc8-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9cdc8-165">Credite și corecții ale unei linii contractuale bazate pe produse facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="9cdc8-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9cdc8-166">Neacceptat</span><span class="sxs-lookup"><span data-stu-id="9cdc8-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
