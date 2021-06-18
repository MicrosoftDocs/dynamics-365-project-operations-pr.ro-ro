---
title: Crearea de facturi corective bazate pe proiect
description: Acest subiect oferă informații despre facturile corective în Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001644"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="13777-103">Crearea de facturi corective bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="13777-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="13777-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="13777-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="13777-105">O factură de proiect confirmată poate fi corectată pentru a procesa modificările sau creditele negociate cu clientul și managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="13777-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="13777-106">Pentru a face modificări la o factură confirmată, deschideți factura confirmată și selectați **Corectați această factură**.</span><span class="sxs-lookup"><span data-stu-id="13777-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="13777-107">Această selecție nu este disponibilă decât dacă se confirmă factura proiectului.</span><span class="sxs-lookup"><span data-stu-id="13777-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="13777-108">O nouă schiță de factură este creată din factura confirmată.</span><span class="sxs-lookup"><span data-stu-id="13777-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="13777-109">Toate detaliile liniei de facturare din factura confirmată anterior sunt copiate în noua schiță.</span><span class="sxs-lookup"><span data-stu-id="13777-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="13777-110">Următoarele sunt câteva puncte cheie pentru a vă ajuta să înțelegeți mai multe despre detaliile liniei de pe noua factură corectată:</span><span class="sxs-lookup"><span data-stu-id="13777-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="13777-111">Toate cantitățile sunt actualizate la zero.</span><span class="sxs-lookup"><span data-stu-id="13777-111">All quantities are updated to zero.</span></span> <span data-ttu-id="13777-112">Aceasta presupune că toate articolele facturate sunt creditate integral.</span><span class="sxs-lookup"><span data-stu-id="13777-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="13777-113">Dacă este necesar, puteți actualiza manual aceste cantități pentru a reflecta cantitatea care este facturată și nu cantitatea care este creditată.</span><span class="sxs-lookup"><span data-stu-id="13777-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="13777-114">Pe baza cantității pe care o introduceți, aplicația calculează cantitatea creditată.</span><span class="sxs-lookup"><span data-stu-id="13777-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="13777-115">Această sumă se reflectă în datele reale care se creează la confirmarea facturii corectate.</span><span class="sxs-lookup"><span data-stu-id="13777-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="13777-116">Dacă modificați valoarea impozitului, trebuie să introduceți suma corectă a impozitului și nu valoarea impozitului care este creditată.</span><span class="sxs-lookup"><span data-stu-id="13777-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="13777-117">Corecțiile de jalon sunt întotdeauna procesate ca credite complete.</span><span class="sxs-lookup"><span data-stu-id="13777-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="13777-118">Sumele de onorariu sau avans pot fi corectate dacă clientul a fost facturat pentru o sumă incorectă.</span><span class="sxs-lookup"><span data-stu-id="13777-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="13777-119">Reconcilierile onorariilor și avansurilor pot fi corectate dacă a fost utilizată o sumă incorectă pentru a se concilia cu taxele de pe o factură confirmată anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13777-120">Detaliile liniei de facturare care sunt corecții la alte taxe deja facturate au câmpul **Corecție** setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="13777-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="13777-121">Facturile care au corectat detaliile liniei de facturare au un câmp numit **Are corecții** care este, de asemenea, setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="13777-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="13777-122">Date reale create la confirmarea unei facturi corective</span><span class="sxs-lookup"><span data-stu-id="13777-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="13777-123">Următorul tabel listează valorile reale care sunt create la confirmarea unei facturi corective.</span><span class="sxs-lookup"><span data-stu-id="13777-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="13777-124">
                    <strong>Scenariu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13777-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="13777-125">
                    <strong>Date reale create la confirmare</strong>
                </span><span class="sxs-lookup"><span data-stu-id="13777-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="13777-126">Confirmați corectarea unui avans sau a unui onorariu facturat.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="13777-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-127">O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="13777-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="13777-128">Această sumă este pozitivă deoarece este menită să anuleze negativul care a fost creat atunci când a fost facturat onorariul sau avansul.</span><span class="sxs-lookup"><span data-stu-id="13777-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-129">Se creează o inversare a datelor reale ale vânzărilor facturate pentru suma din onorariu sau avans pentru a inversa vânzările facturate inițial.</span><span class="sxs-lookup"><span data-stu-id="13777-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-130">Se creează o nouă vânzare facturată actuală pentru suma corectată de pe onorariu sau linia de factură corectată pe bază de avans.</span><span class="sxs-lookup"><span data-stu-id="13777-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-131">O valoare reală de vânzări nefacturate cu sumă negativă a onorariului sau a liniei de factură corectate pe bază de avans, care va fi utilizată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="13777-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="13777-132">O confirmare a corectării unui onorariu sau a unui avans reconciliat anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-133">O inversare nefacturată a vânzărilor de onorariu sau avans care a fost creată pentru reconciliere.</span><span class="sxs-lookup"><span data-stu-id="13777-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="13777-134">Această sumă este pozitivă și este menită să anuleze negativul care a fost creat atunci când a avut loc reconcilierea anterioară.</span><span class="sxs-lookup"><span data-stu-id="13777-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-135">O valoare reală de inversare a vânzărilor facturate pentru suma de pe factura anterioară.</span><span class="sxs-lookup"><span data-stu-id="13777-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-136">O nouă valoare reală a vânzărilor facturate pentru suma de onorariu corectată care se aplică pe factura corectată.</span><span class="sxs-lookup"><span data-stu-id="13777-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-137">O valoare reală de vânzări nefacturate cu o sumă negativă din onorariul sau avansul rămas corectat, care va fi utilizată pentru reconciliere pe facturile ulterioare.</span><span class="sxs-lookup"><span data-stu-id="13777-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13777-138">Facturarea creditului integral al unei tranzacții temporare facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-139">O inversare a vânzărilor facturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="13777-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-140">O nouă valoare reală a vânzărilor nefacturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="13777-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="13777-141">Facturarea creditului parțial pe o tranzacție temporală.</span><span class="sxs-lookup"><span data-stu-id="13777-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-142">O inversare a vânzărilor facturate pentru orele și suma facturate din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="13777-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-143">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="13777-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-144">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="13777-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13777-145">Facturarea creditului integral al unei tranzacții de cheltuială facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-146">O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.</span><span class="sxs-lookup"><span data-stu-id="13777-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-147">O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.</span><span class="sxs-lookup"><span data-stu-id="13777-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="13777-148">Facturarea creditului parțial al unei tranzacții de cheltuială facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-149">O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru o cheltuială.</span><span class="sxs-lookup"><span data-stu-id="13777-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-150">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corectate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="13777-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-151">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="13777-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13777-152">Facturarea creditului integral al taxei unei tranzacții facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-153">O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="13777-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-154">O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="13777-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="13777-155">Facturarea creditului parțial al taxei unei tranzacții facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-156">O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="13777-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-157">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corective modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="13777-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="13777-158">Facturarea creditului integral al jalonului facturat anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-159">O inversare a vânzărilor facturate pentru suma din detaliile liniei de facturare inițiale pentru jalon.</span><span class="sxs-lookup"><span data-stu-id="13777-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="13777-160">Starea facturii pentru reper este actualizată din <b>Factură client postată</b> în <b>Gata de facturare</b>.</span><span class="sxs-lookup"><span data-stu-id="13777-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="13777-161">Facturarea creditului parțial al jalonului facturat anterior.</span><span class="sxs-lookup"><span data-stu-id="13777-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="13777-162">Neacceptat</span><span class="sxs-lookup"><span data-stu-id="13777-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
