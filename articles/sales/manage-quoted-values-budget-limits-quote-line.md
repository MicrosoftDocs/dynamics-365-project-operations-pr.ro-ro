---
title: Linii de oferte bazate pe proiect
description: Acest subiect oferă informații despre utilizarea liniilor de ofertă bazate pe proiecte pentru lucrările de proiect.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906299"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="5bd77-103">Linii de oferte bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="5bd77-103">Project-based quote lines</span></span>

<span data-ttu-id="5bd77-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="5bd77-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5bd77-105">Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament.</span><span class="sxs-lookup"><span data-stu-id="5bd77-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="5bd77-106">Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:</span><span class="sxs-lookup"><span data-stu-id="5bd77-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="5bd77-107">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="5bd77-107">Billing Method</span></span>
- <span data-ttu-id="5bd77-108">Maparea proiectului</span><span class="sxs-lookup"><span data-stu-id="5bd77-108">Project Mapping</span></span>
- <span data-ttu-id="5bd77-109">Clase de tranzacții incluse</span><span class="sxs-lookup"><span data-stu-id="5bd77-109">Included Transaction classes</span></span>
- <span data-ttu-id="5bd77-110">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="5bd77-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="5bd77-111">Configurare posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="5bd77-111">Chargeability setup</span></span>
- <span data-ttu-id="5bd77-112">Estimare folosind Detaliile liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="5bd77-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="5bd77-113">Clienți de linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="5bd77-113">Quote line Customers</span></span>

<span data-ttu-id="5bd77-114">Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="5bd77-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="5bd77-115">Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.</span><span class="sxs-lookup"><span data-stu-id="5bd77-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="5bd77-116">**Câmp**</span><span class="sxs-lookup"><span data-stu-id="5bd77-116">**Field**</span></span> | <span data-ttu-id="5bd77-117">**Relevanță, scop și îndrumare**</span><span class="sxs-lookup"><span data-stu-id="5bd77-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="5bd77-118">**Impactul din aval**</span><span class="sxs-lookup"><span data-stu-id="5bd77-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5bd77-119">Nume</span><span class="sxs-lookup"><span data-stu-id="5bd77-119">Name</span></span> | <span data-ttu-id="5bd77-120">Numele liniei de cotație care ar trebui să vă ajute să identificați componenta discretă a cotației care este estimată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="5bd77-121">Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-122">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="5bd77-122">Billing Method</span></span> | <span data-ttu-id="5bd77-123">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="5bd77-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="5bd77-124">Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="5bd77-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="5bd77-125">- Preț fix</span><span class="sxs-lookup"><span data-stu-id="5bd77-125">- Fixed price</span></span></br><span data-ttu-id="5bd77-126">- Timp și material.</span><span class="sxs-lookup"><span data-stu-id="5bd77-126">- Time and material.</span></span>| <span data-ttu-id="5bd77-127">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-128">Project</span><span class="sxs-lookup"><span data-stu-id="5bd77-128">Project</span></span> | <span data-ttu-id="5bd77-129">Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament.</span><span class="sxs-lookup"><span data-stu-id="5bd77-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="5bd77-130">Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare.</span><span class="sxs-lookup"><span data-stu-id="5bd77-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="5bd77-131">Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="5bd77-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="5bd77-132">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-133">Includeți timpul</span><span class="sxs-lookup"><span data-stu-id="5bd77-133">Include Time</span></span> | <span data-ttu-id="5bd77-134">Un semnalizator **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5bd77-135">O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5bd77-136">O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5bd77-137">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-138">Includeți cheltuielile</span><span class="sxs-lookup"><span data-stu-id="5bd77-138">Include Expense</span></span> | <span data-ttu-id="5bd77-139">Un semnalizator **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5bd77-140">O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5bd77-141">O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5bd77-142">Această valoare de câmp este copiată peste linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-143">Includeți tariful</span><span class="sxs-lookup"><span data-stu-id="5bd77-143">Include Fee</span></span> | <span data-ttu-id="5bd77-144">Un semnalizator **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5bd77-145">O valoare de semnalizator **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5bd77-146">O valoare de semnalizator **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5bd77-147">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-148">Valoare cotă</span><span class="sxs-lookup"><span data-stu-id="5bd77-148">Quoted Amount</span></span> | <span data-ttu-id="5bd77-149">Aceasta este suma care va fi cotată clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="5bd77-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="5bd77-150">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="5bd77-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="5bd77-151">Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="5bd77-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="5bd77-152">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-153">Impozit estimat</span><span class="sxs-lookup"><span data-stu-id="5bd77-153">Estimated Tax</span></span> | <span data-ttu-id="5bd77-154">Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="5bd77-155">Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="5bd77-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="5bd77-156">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-157">Valoare ofertată după taxe</span><span class="sxs-lookup"><span data-stu-id="5bd77-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="5bd77-158">Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire.</span><span class="sxs-lookup"><span data-stu-id="5bd77-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="5bd77-159">Suma din acest câmp este calculată ca *Suma oferită + Taxe*.</span><span class="sxs-lookup"><span data-stu-id="5bd77-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="5bd77-160">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-161">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="5bd77-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="5bd77-162">Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**.</span><span class="sxs-lookup"><span data-stu-id="5bd77-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="5bd77-163">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5bd77-164">Buget client</span><span class="sxs-lookup"><span data-stu-id="5bd77-164">Customer Budget</span></span> | <span data-ttu-id="5bd77-165">Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="5bd77-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="5bd77-166">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="5bd77-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="5bd77-167">Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="5bd77-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="5bd77-168">**Regula 1**: O anumită clasă de tranzacție pentru proiectul selectat poate fi inclusă numai pe o singură linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="5bd77-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="5bd77-169">**Regula 2**: Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="5bd77-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="5bd77-170">**Regula 3**: Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="5bd77-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="5bd77-171">
                    <strong>Oportunitate</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5bd77-172">
                    <strong>Ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5bd77-173">
                    <strong>Linie de ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5bd77-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5bd77-175">
                    <strong>Includeți timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5bd77-176">
                    <strong>Includeți cheltuielile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5bd77-177">
                    <strong>Includere</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5bd77-178">
                    <strong>taxă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="5bd77-179">
                    <strong>Valid/nu este valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="5bd77-180">
                    <strong>Motiv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bd77-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-181">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-182">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-183">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-184">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-185">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-186">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-187">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-188">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-189">Încălcarea regulii #1.</span><span class="sxs-lookup"><span data-stu-id="5bd77-189">Violation of Rule #1.</span></span> <span data-ttu-id="5bd77-190">Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe ambele linii de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="5bd77-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-191">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-192">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-193">QL2</span><span class="sxs-lookup"><span data-stu-id="5bd77-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-194">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-195">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-196">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-197">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-197">Yes</span></span> </p>
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
<span data-ttu-id="5bd77-198">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-199">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-200">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-201">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-202">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-203">Nicio</span><span class="sxs-lookup"><span data-stu-id="5bd77-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-204">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-205">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-206">Încălcarea regulii #1.</span><span class="sxs-lookup"><span data-stu-id="5bd77-206">Violation of Rule #1.</span></span> <span data-ttu-id="5bd77-207">Timpul și taxele pentru proiectul P1 sunt incluse pe ambele linii de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="5bd77-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-208">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-209">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-210">QL2</span><span class="sxs-lookup"><span data-stu-id="5bd77-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-211">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-212">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-213">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-214">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-214">Yes</span></span> </p>
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
<span data-ttu-id="5bd77-215">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-216">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-217">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-218">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-219">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-220">Nicio</span><span class="sxs-lookup"><span data-stu-id="5bd77-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-221">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-222">Valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="5bd77-223">Timpul și taxele pentru proiectul P1 sunt incluse pe QL1.</span><span class="sxs-lookup"><span data-stu-id="5bd77-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="5bd77-224">Cheltuielile pentru proiectul P1 sunt incluse în QL2.</span><span class="sxs-lookup"><span data-stu-id="5bd77-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="5bd77-225">Nu există o suprapunere în ceea ce este inclus pe fiecare linie de cotare, deci este valabilă.</span><span class="sxs-lookup"><span data-stu-id="5bd77-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-226">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-227">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-228">QL2</span><span class="sxs-lookup"><span data-stu-id="5bd77-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-229">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-230">Nicio</span><span class="sxs-lookup"><span data-stu-id="5bd77-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-231">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-232">Nicio</span><span class="sxs-lookup"><span data-stu-id="5bd77-232">No</span></span> </p>
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
<span data-ttu-id="5bd77-233">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-234">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-235">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-236">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-237">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-238">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-239">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-240">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-241">Încălcarea regulii #1 de mai sus</span><span class="sxs-lookup"><span data-stu-id="5bd77-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="5bd77-242">Q1 include timp, cheltuieli și taxe pentru întregul proiect P1.</span><span class="sxs-lookup"><span data-stu-id="5bd77-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5bd77-243">QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și se suprapune cu ceea ce este inclus în Q1.</span><span class="sxs-lookup"><span data-stu-id="5bd77-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-244">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-245">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-246">QL2</span><span class="sxs-lookup"><span data-stu-id="5bd77-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-247">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-248">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-249">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-250">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-250">Yes</span></span> </p>
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
<span data-ttu-id="5bd77-251">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-252">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-253">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-254">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-255">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-256">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-257">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5bd77-258">Valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-259">Pe baza regulii #2, Q1 și Q2 sunt două citate cu aceeași oportunitate, astfel încât ambele pot estima pentru aceleași componente ale unui proiect.</span><span class="sxs-lookup"><span data-stu-id="5bd77-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-260">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-261">T2</span><span class="sxs-lookup"><span data-stu-id="5bd77-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-262">QL1 pe Q2</span><span class="sxs-lookup"><span data-stu-id="5bd77-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-263">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-264">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-265">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-266">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-266">Yes</span></span> </p>
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
<span data-ttu-id="5bd77-267">O1</span><span class="sxs-lookup"><span data-stu-id="5bd77-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-268">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-269">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-270">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-271">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-272">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-273">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5bd77-274">Valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bd77-275">Pe baza regulii #3, Q1 și Q2 sunt două citate cu oportunități diferite, astfel încât ambele nu pot estima pentru aceleași componente ale aceluiași proiect.</span><span class="sxs-lookup"><span data-stu-id="5bd77-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5bd77-276">O2</span><span class="sxs-lookup"><span data-stu-id="5bd77-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5bd77-277">T1</span><span class="sxs-lookup"><span data-stu-id="5bd77-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-278">QL1</span><span class="sxs-lookup"><span data-stu-id="5bd77-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-279">P1</span><span class="sxs-lookup"><span data-stu-id="5bd77-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-280">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5bd77-281">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5bd77-282">Da</span><span class="sxs-lookup"><span data-stu-id="5bd77-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5bd77-283">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="5bd77-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

