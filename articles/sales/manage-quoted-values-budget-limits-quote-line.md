---
title: Prezentare generală a liniilor de oferte ale proiectului
description: Acest subiect oferă informații despre utilizarea de linii de ofertă de proiect pentru lucrul la un proiect.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858047"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="23998-103">Prezentare generală a liniilor de oferte ale proiectului</span><span class="sxs-lookup"><span data-stu-id="23998-103">Project quote lines overview</span></span>

<span data-ttu-id="23998-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="23998-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="23998-105">Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament.</span><span class="sxs-lookup"><span data-stu-id="23998-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="23998-106">Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:</span><span class="sxs-lookup"><span data-stu-id="23998-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="23998-107">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="23998-107">Billing Method</span></span>
- <span data-ttu-id="23998-108">Maparea proiectului</span><span class="sxs-lookup"><span data-stu-id="23998-108">Project Mapping</span></span>
- <span data-ttu-id="23998-109">Clase de tranzacții incluse</span><span class="sxs-lookup"><span data-stu-id="23998-109">Included Transaction classes</span></span>
- <span data-ttu-id="23998-110">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="23998-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="23998-111">Configurare posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="23998-111">Chargeability setup</span></span>
- <span data-ttu-id="23998-112">Estimare folosind Detaliile liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="23998-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="23998-113">Clienți de linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="23998-113">Quote line Customers</span></span>

<span data-ttu-id="23998-114">Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="23998-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="23998-115">Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.</span><span class="sxs-lookup"><span data-stu-id="23998-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="23998-116">**Câmp**</span><span class="sxs-lookup"><span data-stu-id="23998-116">**Field**</span></span> | <span data-ttu-id="23998-117">**Descriere**</span><span class="sxs-lookup"><span data-stu-id="23998-117">**Description**</span></span> | <span data-ttu-id="23998-118">**Impactul din aval**</span><span class="sxs-lookup"><span data-stu-id="23998-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="23998-119">Nume</span><span class="sxs-lookup"><span data-stu-id="23998-119">Name</span></span> | <span data-ttu-id="23998-120">Numele liniei de cotație care ar trebui să vă ajute să identificați componenta discretă a cotației care este estimată.</span><span class="sxs-lookup"><span data-stu-id="23998-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="23998-121">Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-122">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="23998-122">Billing Method</span></span> | <span data-ttu-id="23998-123">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="23998-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="23998-124">Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="23998-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="23998-125">- Preț fix</span><span class="sxs-lookup"><span data-stu-id="23998-125">- Fixed price</span></span></br><span data-ttu-id="23998-126">- Timp și material.</span><span class="sxs-lookup"><span data-stu-id="23998-126">- Time and material.</span></span>| <span data-ttu-id="23998-127">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-128">Project</span><span class="sxs-lookup"><span data-stu-id="23998-128">Project</span></span> | <span data-ttu-id="23998-129">Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament.</span><span class="sxs-lookup"><span data-stu-id="23998-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="23998-130">Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare.</span><span class="sxs-lookup"><span data-stu-id="23998-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="23998-131">Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="23998-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="23998-132">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-133">Includeți timpul</span><span class="sxs-lookup"><span data-stu-id="23998-133">Include Time</span></span> | <span data-ttu-id="23998-134">Un semnalizator **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23998-135">O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23998-136">O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23998-137">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-138">Includeți cheltuielile</span><span class="sxs-lookup"><span data-stu-id="23998-138">Include Expense</span></span> | <span data-ttu-id="23998-139">Un semnalizator **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23998-140">O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23998-141">O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23998-142">Această valoare de câmp este copiată peste linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-143">Includeți tariful</span><span class="sxs-lookup"><span data-stu-id="23998-143">Include Fee</span></span> | <span data-ttu-id="23998-144">Un semnalizator **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="23998-145">O valoare de semnalizator **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="23998-146">O valoare de semnalizator **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="23998-147">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-148">Valoare cotă</span><span class="sxs-lookup"><span data-stu-id="23998-148">Quoted Amount</span></span> | <span data-ttu-id="23998-149">Aceasta este suma care va fi cotată clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="23998-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="23998-150">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="23998-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="23998-151">Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="23998-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="23998-152">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-153">Impozit estimat</span><span class="sxs-lookup"><span data-stu-id="23998-153">Estimated Tax</span></span> | <span data-ttu-id="23998-154">Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="23998-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="23998-155">Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="23998-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="23998-156">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-157">Valoare ofertată după taxe</span><span class="sxs-lookup"><span data-stu-id="23998-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="23998-158">Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire.</span><span class="sxs-lookup"><span data-stu-id="23998-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="23998-159">Suma din acest câmp este calculată ca *Suma oferită + Taxe*.</span><span class="sxs-lookup"><span data-stu-id="23998-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="23998-160">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-161">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="23998-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="23998-162">Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**.</span><span class="sxs-lookup"><span data-stu-id="23998-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="23998-163">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="23998-164">Buget client</span><span class="sxs-lookup"><span data-stu-id="23998-164">Customer Budget</span></span> | <span data-ttu-id="23998-165">Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="23998-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="23998-166">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="23998-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="23998-167">Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="23998-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="23998-168">**Regula 1**: O anumită clasă de tranzacție pentru proiectul selectat poate fi inclusă numai pe o singură linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="23998-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="23998-169">**Regula 2**: Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="23998-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="23998-170">**Regula 3**: Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="23998-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="23998-171">
                    <strong>Oportunitate</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="23998-172">
                    <strong>Ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="23998-173">
                    <strong>Linie de ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="23998-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="23998-175">
                    <strong>Includeți timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="23998-176">
                    <strong>Includeți cheltuielile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="23998-177">
                    <strong>Includere</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="23998-178">
                    <strong>taxă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="23998-179">
                    <strong>Valid/nu este valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="23998-180">
                    <strong>Motiv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="23998-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-181">O1</span><span class="sxs-lookup"><span data-stu-id="23998-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-182">T1</span><span class="sxs-lookup"><span data-stu-id="23998-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-183">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-184">P1</span><span class="sxs-lookup"><span data-stu-id="23998-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-185">Da</span><span class="sxs-lookup"><span data-stu-id="23998-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-186">Da</span><span class="sxs-lookup"><span data-stu-id="23998-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-187">Da</span><span class="sxs-lookup"><span data-stu-id="23998-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-188">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="23998-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-189">Încălcarea regulii #1.</span><span class="sxs-lookup"><span data-stu-id="23998-189">Violation of Rule #1.</span></span> <span data-ttu-id="23998-190">Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe ambele linii de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="23998-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-191">O1</span><span class="sxs-lookup"><span data-stu-id="23998-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-192">T1</span><span class="sxs-lookup"><span data-stu-id="23998-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-193">QL2</span><span class="sxs-lookup"><span data-stu-id="23998-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-194">P1</span><span class="sxs-lookup"><span data-stu-id="23998-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-195">Da</span><span class="sxs-lookup"><span data-stu-id="23998-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-196">Da</span><span class="sxs-lookup"><span data-stu-id="23998-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-197">Da</span><span class="sxs-lookup"><span data-stu-id="23998-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-198">O1</span><span class="sxs-lookup"><span data-stu-id="23998-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-199">T1</span><span class="sxs-lookup"><span data-stu-id="23998-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-200">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-201">P1</span><span class="sxs-lookup"><span data-stu-id="23998-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-202">Da</span><span class="sxs-lookup"><span data-stu-id="23998-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-203">Nicio</span><span class="sxs-lookup"><span data-stu-id="23998-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-204">Da</span><span class="sxs-lookup"><span data-stu-id="23998-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-205">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="23998-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-206">Încălcarea regulii #1.</span><span class="sxs-lookup"><span data-stu-id="23998-206">Violation of Rule #1.</span></span> <span data-ttu-id="23998-207">Timpul și taxele pentru proiectul P1 sunt incluse pe ambele linii de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="23998-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-208">O1</span><span class="sxs-lookup"><span data-stu-id="23998-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-209">T1</span><span class="sxs-lookup"><span data-stu-id="23998-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-210">QL2</span><span class="sxs-lookup"><span data-stu-id="23998-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-211">P1</span><span class="sxs-lookup"><span data-stu-id="23998-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-212">Da</span><span class="sxs-lookup"><span data-stu-id="23998-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-213">Da</span><span class="sxs-lookup"><span data-stu-id="23998-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-214">Da</span><span class="sxs-lookup"><span data-stu-id="23998-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-215">O1</span><span class="sxs-lookup"><span data-stu-id="23998-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-216">T1</span><span class="sxs-lookup"><span data-stu-id="23998-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-217">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-218">P1</span><span class="sxs-lookup"><span data-stu-id="23998-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-219">Da</span><span class="sxs-lookup"><span data-stu-id="23998-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-220">Nicio</span><span class="sxs-lookup"><span data-stu-id="23998-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-221">Da</span><span class="sxs-lookup"><span data-stu-id="23998-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-222">Valid</span><span class="sxs-lookup"><span data-stu-id="23998-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="23998-223">Timpul și taxele pentru proiectul P1 sunt incluse pe QL1.</span><span class="sxs-lookup"><span data-stu-id="23998-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="23998-224">Cheltuielile pentru proiectul P1 sunt incluse în QL2.</span><span class="sxs-lookup"><span data-stu-id="23998-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="23998-225">Nu există o suprapunere în ceea ce este inclus pe fiecare linie de cotare, deci este valabilă.</span><span class="sxs-lookup"><span data-stu-id="23998-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-226">O1</span><span class="sxs-lookup"><span data-stu-id="23998-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-227">T1</span><span class="sxs-lookup"><span data-stu-id="23998-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-228">QL2</span><span class="sxs-lookup"><span data-stu-id="23998-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-229">P1</span><span class="sxs-lookup"><span data-stu-id="23998-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-230">Nicio</span><span class="sxs-lookup"><span data-stu-id="23998-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-231">Da</span><span class="sxs-lookup"><span data-stu-id="23998-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-232">Nicio</span><span class="sxs-lookup"><span data-stu-id="23998-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-233">O1</span><span class="sxs-lookup"><span data-stu-id="23998-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-234">T1</span><span class="sxs-lookup"><span data-stu-id="23998-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-235">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-236">P1</span><span class="sxs-lookup"><span data-stu-id="23998-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-237">Da</span><span class="sxs-lookup"><span data-stu-id="23998-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-238">Da</span><span class="sxs-lookup"><span data-stu-id="23998-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-239">Da</span><span class="sxs-lookup"><span data-stu-id="23998-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-240">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="23998-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-241">Încălcarea regulii #1 de mai sus</span><span class="sxs-lookup"><span data-stu-id="23998-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="23998-242">Q1 include timp, cheltuieli și taxe pentru întregul proiect P1.</span><span class="sxs-lookup"><span data-stu-id="23998-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="23998-243">QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și se suprapune cu ceea ce este inclus în Q1.</span><span class="sxs-lookup"><span data-stu-id="23998-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-244">O1</span><span class="sxs-lookup"><span data-stu-id="23998-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-245">T1</span><span class="sxs-lookup"><span data-stu-id="23998-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-246">QL2</span><span class="sxs-lookup"><span data-stu-id="23998-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-247">P1</span><span class="sxs-lookup"><span data-stu-id="23998-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-248">Da</span><span class="sxs-lookup"><span data-stu-id="23998-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-249">Da</span><span class="sxs-lookup"><span data-stu-id="23998-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-250">Da</span><span class="sxs-lookup"><span data-stu-id="23998-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-251">O1</span><span class="sxs-lookup"><span data-stu-id="23998-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-252">T1</span><span class="sxs-lookup"><span data-stu-id="23998-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-253">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-254">P1</span><span class="sxs-lookup"><span data-stu-id="23998-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-255">Da</span><span class="sxs-lookup"><span data-stu-id="23998-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-256">Da</span><span class="sxs-lookup"><span data-stu-id="23998-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-257">Da</span><span class="sxs-lookup"><span data-stu-id="23998-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="23998-258">Valid</span><span class="sxs-lookup"><span data-stu-id="23998-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-259">Pe baza regulii #2, Q1 și Q2 sunt două citate cu aceeași oportunitate, astfel încât ambele pot estima pentru aceleași componente ale unui proiect.</span><span class="sxs-lookup"><span data-stu-id="23998-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-260">O1</span><span class="sxs-lookup"><span data-stu-id="23998-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-261">T2</span><span class="sxs-lookup"><span data-stu-id="23998-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-262">QL1 pe Q2</span><span class="sxs-lookup"><span data-stu-id="23998-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-263">P1</span><span class="sxs-lookup"><span data-stu-id="23998-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-264">Da</span><span class="sxs-lookup"><span data-stu-id="23998-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-265">Da</span><span class="sxs-lookup"><span data-stu-id="23998-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-266">Da</span><span class="sxs-lookup"><span data-stu-id="23998-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-267">O1</span><span class="sxs-lookup"><span data-stu-id="23998-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-268">T1</span><span class="sxs-lookup"><span data-stu-id="23998-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-269">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-270">P1</span><span class="sxs-lookup"><span data-stu-id="23998-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-271">Da</span><span class="sxs-lookup"><span data-stu-id="23998-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-272">Da</span><span class="sxs-lookup"><span data-stu-id="23998-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-273">Da</span><span class="sxs-lookup"><span data-stu-id="23998-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="23998-274">Valid</span><span class="sxs-lookup"><span data-stu-id="23998-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="23998-275">Pe baza regulii #3, Q1 și Q2 sunt două citate cu oportunități diferite, astfel încât ambele nu pot estima pentru aceleași componente ale aceluiași proiect.</span><span class="sxs-lookup"><span data-stu-id="23998-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="23998-276">O2</span><span class="sxs-lookup"><span data-stu-id="23998-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="23998-277">T1</span><span class="sxs-lookup"><span data-stu-id="23998-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-278">QL1</span><span class="sxs-lookup"><span data-stu-id="23998-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-279">P1</span><span class="sxs-lookup"><span data-stu-id="23998-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-280">Da</span><span class="sxs-lookup"><span data-stu-id="23998-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="23998-281">Da</span><span class="sxs-lookup"><span data-stu-id="23998-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="23998-282">Da</span><span class="sxs-lookup"><span data-stu-id="23998-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="23998-283">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="23998-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
