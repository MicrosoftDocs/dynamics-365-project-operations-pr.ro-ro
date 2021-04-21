---
title: Facturi corective bazate pe proiect
description: Acest subiect oferă informații despre cum să creați și să confirmați facturi corective bazate pe proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867056"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="121a2-103">Facturi corective bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="121a2-103">Corrective project-based invoices</span></span>

<span data-ttu-id="121a2-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="121a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="121a2-105">O factură de proiect confirmată poate fi corectată pentru a procesa modificările sau creditele negociate cu clientul și managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="121a2-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="121a2-106">Pentru a face modificări la o factură confirmată, deschideți factura confirmată și selectați **Corectați această factură**.</span><span class="sxs-lookup"><span data-stu-id="121a2-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="121a2-107">Această selecție nu este disponibilă decât dacă o factură de proiect este confirmată sau dacă factura bazată pe proiect are avansuri sau rețineri sau reconcilieri de avansuri sau de rețineri.</span><span class="sxs-lookup"><span data-stu-id="121a2-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="121a2-108">O nouă schiță de factură este creată din factura confirmată.</span><span class="sxs-lookup"><span data-stu-id="121a2-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="121a2-109">Toate detaliile liniei de facturare din factura confirmată anterior sunt copiate în noua schiță.</span><span class="sxs-lookup"><span data-stu-id="121a2-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="121a2-110">Următoarele sunt câteva dintre punctele cheie pentru a înțelege detaliile liniei de pe noua factură corectată:</span><span class="sxs-lookup"><span data-stu-id="121a2-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="121a2-111">Toate cantitățile sunt actualizate la zero.</span><span class="sxs-lookup"><span data-stu-id="121a2-111">All quantities are updated to zero.</span></span> <span data-ttu-id="121a2-112">Dynamics 365 Project Operations presupune că toate articolele facturate sunt creditate integral.</span><span class="sxs-lookup"><span data-stu-id="121a2-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="121a2-113">Dacă este necesar, puteți actualiza manual aceste cantități pentru a reflecta cantitatea care este facturată și nu cantitatea care este creditată.</span><span class="sxs-lookup"><span data-stu-id="121a2-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="121a2-114">Pe baza cantității pe care o introduceți, aplicația calculează cantitatea creditată.</span><span class="sxs-lookup"><span data-stu-id="121a2-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="121a2-115">Această sumă se reflectă în datele reale care se creează la confirmarea facturii corectate.</span><span class="sxs-lookup"><span data-stu-id="121a2-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="121a2-116">Dacă modificați valoarea impozitului, trebuie să introduceți suma corectă a impozitului și nu valoarea impozitului care este creditată.</span><span class="sxs-lookup"><span data-stu-id="121a2-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="121a2-117">Corecțiile de jalon sunt întotdeauna procesate ca credite complete.</span><span class="sxs-lookup"><span data-stu-id="121a2-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="121a2-118">Pentru detaliile liniei de facturare care sunt corecții la alte taxe deja facturate, câmpul **Corecție** este setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="121a2-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="121a2-119">Pentru facturile care au detalii ale liniei de facturare corectate, câmpul **Are corecții** este setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="121a2-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="121a2-120">Date reale create când se confirmă o factură corectivă</span><span class="sxs-lookup"><span data-stu-id="121a2-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="121a2-121">Următorul tabel listează valorile reale care sunt create la confirmarea unei facturi corective.</span><span class="sxs-lookup"><span data-stu-id="121a2-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="121a2-122">
                    <strong>Scenariu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="121a2-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="121a2-123">
                    <strong>Date reale create la confirmare</strong>
                </span><span class="sxs-lookup"><span data-stu-id="121a2-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="121a2-124">Facturarea creditului integral al unei tranzacții temporare facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-125">O inversare a vânzărilor facturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="121a2-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-126">O nouă valoare reală a vânzărilor nefacturate pentru orele și suma din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="121a2-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="121a2-127">Facturarea creditului parțial pe o tranzacție temporală.</span><span class="sxs-lookup"><span data-stu-id="121a2-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-128">O inversare a vânzărilor facturate pentru orele și suma facturate din detaliile liniei de facturare inițiale pentru timp.</span><span class="sxs-lookup"><span data-stu-id="121a2-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-129">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma din detaliile modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="121a2-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-130">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru orele și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="121a2-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="121a2-131">Facturarea creditului integral al unei tranzacții de cheltuială facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-132">O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.</span><span class="sxs-lookup"><span data-stu-id="121a2-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-133">O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru cheltuială.</span><span class="sxs-lookup"><span data-stu-id="121a2-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="121a2-134">Facturarea creditului parțial al unei tranzacții de cheltuială facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-135">O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru o cheltuială.</span><span class="sxs-lookup"><span data-stu-id="121a2-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-136">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corectate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="121a2-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-137">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="121a2-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="121a2-138">Facturarea creditului integral al unei tranzacții de materiale facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-139">O inversare facturată a vânzărilor pentru cantitatea și suma din detaliile liniei inițiale de facturare pentru material.</span><span class="sxs-lookup"><span data-stu-id="121a2-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-140">O valoare reală nefacturată nouă a vânzărilor pentru cantitatea și suma din detaliile liniei inițiale de facturare pentru material.</span><span class="sxs-lookup"><span data-stu-id="121a2-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="121a2-141">Facturarea creditului parțial pentru o tranzacție de materiale.</span><span class="sxs-lookup"><span data-stu-id="121a2-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-142">O inversare de factură de vânzări pentru cantitatea și suma facturate pe detaliile liniei inițiale a facturii pentru material.</span><span class="sxs-lookup"><span data-stu-id="121a2-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-143">O nouă valoare reală a vânzărilor nefacturate care este taxabilă pentru cantitatea și suma din detaliile editate ale liniei de facturare, o inversare a acesteia și o valoare reală echivalentă a vânzărilor facturate.</span><span class="sxs-lookup"><span data-stu-id="121a2-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-144">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma rămasă după deducerea cifrelor corectate pe detaliile liniei de facturare.</span><span class="sxs-lookup"><span data-stu-id="121a2-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="121a2-145">Facturarea creditului integral al taxei unei tranzacții facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-146">O inversare a vânzărilor facturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="121a2-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-147">O nouă valoare reală a vânzărilor nefacturate pentru cantitatea și suma din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="121a2-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="121a2-148">Facturarea creditului parțial al taxei unei tranzacții facturate anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-149">O inversare a vânzărilor facturate pentru cantitatea și suma facturată din detaliile liniei de facturare inițiale pentru taxă.</span><span class="sxs-lookup"><span data-stu-id="121a2-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-150">O nouă valoare reală a vânzărilor nefacturate care se taxează pentru cantitatea și suma din detaliile corective modificate ale liniei de facturare, o inversare a acestora și o facturare echivalentă efectivă.</span><span class="sxs-lookup"><span data-stu-id="121a2-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="121a2-151">Facturarea creditului integral al jalonului facturat anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-152">O inversare a vânzărilor facturate pentru suma din detaliile liniei de facturare inițiale pentru jalon.</span><span class="sxs-lookup"><span data-stu-id="121a2-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="121a2-153">Starea facturii pentru reper este actualizată din <b>Factură client postată</b> în <b>Gata de facturare</b>.</span><span class="sxs-lookup"><span data-stu-id="121a2-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="121a2-154">Facturarea creditului parțial al jalonului facturat anterior.</span><span class="sxs-lookup"><span data-stu-id="121a2-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="121a2-155">Acest scenariu nu este acceptat.</span><span class="sxs-lookup"><span data-stu-id="121a2-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
