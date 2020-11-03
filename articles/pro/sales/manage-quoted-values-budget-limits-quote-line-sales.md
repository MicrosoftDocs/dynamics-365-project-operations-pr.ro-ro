---
title: Linii de oferte bazate pe proiect (Pro)
description: Acest subiect oferă informații despre utilizarea liniilor de ofertă bazate pe proiecte pentru lucrările de proiect. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082726"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="21161-104">Linii de oferte bazate pe proiect (Pro)</span><span class="sxs-lookup"><span data-stu-id="21161-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="21161-105">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="21161-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="21161-106">Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament.</span><span class="sxs-lookup"><span data-stu-id="21161-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="21161-107">Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:</span><span class="sxs-lookup"><span data-stu-id="21161-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="21161-108">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="21161-108">Billing Method</span></span>
- <span data-ttu-id="21161-109">Mapare de proiect și activități</span><span class="sxs-lookup"><span data-stu-id="21161-109">Project and Task Mapping</span></span>
- <span data-ttu-id="21161-110">Clase de tranzacții incluse</span><span class="sxs-lookup"><span data-stu-id="21161-110">Included Transaction classes</span></span>
- <span data-ttu-id="21161-111">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="21161-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="21161-112">Configurare posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="21161-112">Chargeability setup</span></span>
- <span data-ttu-id="21161-113">Estimare folosind Detaliile liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="21161-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="21161-114">Clienți de linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="21161-114">Quote line Customers</span></span>

<span data-ttu-id="21161-115">Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="21161-116">Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="21161-117">**Câmp**</span><span class="sxs-lookup"><span data-stu-id="21161-117">**Field**</span></span> | <span data-ttu-id="21161-118">**Relevanță, scop și îndrumare**</span><span class="sxs-lookup"><span data-stu-id="21161-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="21161-119">**Impactul din aval**</span><span class="sxs-lookup"><span data-stu-id="21161-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="21161-120">Nume</span><span class="sxs-lookup"><span data-stu-id="21161-120">Name</span></span> | <span data-ttu-id="21161-121">Numele liniei de cotație care ar trebui să vă ajute să identificați componenta discretă a cotației care este estimată.</span><span class="sxs-lookup"><span data-stu-id="21161-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="21161-122">Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-123">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="21161-123">Billing Method</span></span> | <span data-ttu-id="21161-124">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="21161-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="21161-125">Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="21161-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="21161-126">- Preț fix</span><span class="sxs-lookup"><span data-stu-id="21161-126">- Fixed price</span></span></br><span data-ttu-id="21161-127">- Timp și material.</span><span class="sxs-lookup"><span data-stu-id="21161-127">- Time and material.</span></span>| <span data-ttu-id="21161-128">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-129">Project</span><span class="sxs-lookup"><span data-stu-id="21161-129">Project</span></span> | <span data-ttu-id="21161-130">Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament.</span><span class="sxs-lookup"><span data-stu-id="21161-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="21161-131">Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare.</span><span class="sxs-lookup"><span data-stu-id="21161-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="21161-132">Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="21161-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="21161-133">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="21161-134">Activități incluse</span><span class="sxs-lookup"><span data-stu-id="21161-134">Included Tasks</span></span> | <span data-ttu-id="21161-135">Indică dacă această linie de cotație este utilizată pentru toate sau unele dintre sarcinile proiectului pentru proiectul selectat.</span><span class="sxs-lookup"><span data-stu-id="21161-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="21161-136">Acest câmp are următoarele valori posibile:</span><span class="sxs-lookup"><span data-stu-id="21161-136">This field has the following possible values:</span></span></br><span data-ttu-id="21161-137">- Toate activitățile de proiect</span><span class="sxs-lookup"><span data-stu-id="21161-137">- All project tasks</span></span></br><span data-ttu-id="21161-138">- Numai activități de proiect selectate</span><span class="sxs-lookup"><span data-stu-id="21161-138">- Selected project tasks only</span></span></br><span data-ttu-id="21161-139">O valoare necompletată în acest câmp este echivalentă cu opțiunea **Toate sarcinile proiectului**.</span><span class="sxs-lookup"><span data-stu-id="21161-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="21161-140">Când **Numai sarcini de proiect selectate** este selectat apoi pe pagina de proiect, fila **Configurarea activității de facturare** vă permite să selectați activități specifice pentru a le asocia la această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="21161-141">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-142">Includeți timpul</span><span class="sxs-lookup"><span data-stu-id="21161-142">Include Time</span></span> | <span data-ttu-id="21161-143">Un semnalizator **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="21161-144">O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="21161-145">O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="21161-146">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-147">Includeți cheltuielile</span><span class="sxs-lookup"><span data-stu-id="21161-147">Include Expense</span></span> | <span data-ttu-id="21161-148">Un semnalizator **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="21161-149">O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="21161-150">O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="21161-151">Această valoare de câmp este copiată peste linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-152">Includeți tariful</span><span class="sxs-lookup"><span data-stu-id="21161-152">Include Fee</span></span> | <span data-ttu-id="21161-153">Un semnalizator **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="21161-154">O valoare de semnalizator **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="21161-155">O valoare de semnalizator **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="21161-156">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-157">Valoare cotă</span><span class="sxs-lookup"><span data-stu-id="21161-157">Quoted Amount</span></span> | <span data-ttu-id="21161-158">Aceasta este suma care va fi cotată clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="21161-159">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="21161-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="21161-160">Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="21161-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="21161-161">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-162">Impozit estimat</span><span class="sxs-lookup"><span data-stu-id="21161-162">Estimated Tax</span></span> | <span data-ttu-id="21161-163">Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="21161-164">Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="21161-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="21161-165">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-166">Valoare ofertată după taxe</span><span class="sxs-lookup"><span data-stu-id="21161-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="21161-167">Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire.</span><span class="sxs-lookup"><span data-stu-id="21161-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="21161-168">Suma din acest câmp este calculată ca *Suma oferită + Taxe*.</span><span class="sxs-lookup"><span data-stu-id="21161-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="21161-169">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-170">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="21161-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="21161-171">Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**.</span><span class="sxs-lookup"><span data-stu-id="21161-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="21161-172">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="21161-173">Buget client</span><span class="sxs-lookup"><span data-stu-id="21161-173">Customer Budget</span></span> | <span data-ttu-id="21161-174">Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="21161-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="21161-175">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="21161-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="21161-176">Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="21161-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="21161-177">**Regula 1** : Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului** , un proiect este inclus în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="21161-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="21161-178">**Regula 2** : Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului** , un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o singură linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="21161-179">**Regula 3** : Dacă câmpul **Sarcini incluse** este setat la **Doar activitățile de proiect selectate** , un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de ofertă multiplă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="21161-180">**Regula 4** : Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="21161-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="21161-181">**Regula 5** : Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="21161-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="21161-182">
                    <strong>Oportunitate</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="21161-183">
                    <strong>Ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="21161-184">
                    <strong>Linie de ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="21161-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="21161-186">
                    <strong>Activități incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="21161-187">
                    <strong>Includeți timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="21161-188">
                    <strong>Includeți cheltuielile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="21161-189">
                    <strong>Includere</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="21161-190">
                    <strong>Taxă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="21161-191">
                    <strong>Valid/nu este valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="21161-192">
                    <strong>Motiv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="21161-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-193">O1</span><span class="sxs-lookup"><span data-stu-id="21161-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-194">T1</span><span class="sxs-lookup"><span data-stu-id="21161-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-195">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-196">P1</span><span class="sxs-lookup"><span data-stu-id="21161-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-197">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-198">Da</span><span class="sxs-lookup"><span data-stu-id="21161-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-199">Da</span><span class="sxs-lookup"><span data-stu-id="21161-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-200">Da</span><span class="sxs-lookup"><span data-stu-id="21161-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-201">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="21161-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-202">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="21161-202">Violation of Rule #2.</span></span> <span data-ttu-id="21161-203">Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="21161-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-204">O1</span><span class="sxs-lookup"><span data-stu-id="21161-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-205">T1</span><span class="sxs-lookup"><span data-stu-id="21161-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-206">QL2</span><span class="sxs-lookup"><span data-stu-id="21161-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-207">P1</span><span class="sxs-lookup"><span data-stu-id="21161-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-208">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-209">Da</span><span class="sxs-lookup"><span data-stu-id="21161-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-210">Da</span><span class="sxs-lookup"><span data-stu-id="21161-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-211">Da</span><span class="sxs-lookup"><span data-stu-id="21161-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="21161-212">O1</span><span class="sxs-lookup"><span data-stu-id="21161-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-213">T1</span><span class="sxs-lookup"><span data-stu-id="21161-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-214">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-215">P1</span><span class="sxs-lookup"><span data-stu-id="21161-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-216">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-217">Da</span><span class="sxs-lookup"><span data-stu-id="21161-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-218">Nicio</span><span class="sxs-lookup"><span data-stu-id="21161-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-219">Da</span><span class="sxs-lookup"><span data-stu-id="21161-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-220">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="21161-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-221">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="21161-221">Violation of Rule #2.</span></span> <span data-ttu-id="21161-222">Timpul și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="21161-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-223">O1</span><span class="sxs-lookup"><span data-stu-id="21161-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-224">T1</span><span class="sxs-lookup"><span data-stu-id="21161-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-225">QL2</span><span class="sxs-lookup"><span data-stu-id="21161-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-226">P1</span><span class="sxs-lookup"><span data-stu-id="21161-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-227">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-228">Da</span><span class="sxs-lookup"><span data-stu-id="21161-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-229">Da</span><span class="sxs-lookup"><span data-stu-id="21161-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-230">Da</span><span class="sxs-lookup"><span data-stu-id="21161-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-231">O1</span><span class="sxs-lookup"><span data-stu-id="21161-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-232">T1</span><span class="sxs-lookup"><span data-stu-id="21161-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-233">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-234">P1</span><span class="sxs-lookup"><span data-stu-id="21161-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-235">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-236">Da</span><span class="sxs-lookup"><span data-stu-id="21161-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-237">Nicio</span><span class="sxs-lookup"><span data-stu-id="21161-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-238">Da</span><span class="sxs-lookup"><span data-stu-id="21161-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-239">Valid</span><span class="sxs-lookup"><span data-stu-id="21161-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="21161-240">Timpul și taxele pentru proiectul P1 sunt incluse pe QL1.</span><span class="sxs-lookup"><span data-stu-id="21161-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="21161-241">Cheltuielile pentru proiectul P1 sunt incluse în QL2.</span><span class="sxs-lookup"><span data-stu-id="21161-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="21161-242">Nu există o suprapunere în ceea ce este inclus pe fiecare linie de ofertă și este valabilă.</span><span class="sxs-lookup"><span data-stu-id="21161-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-243">O1</span><span class="sxs-lookup"><span data-stu-id="21161-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-244">T1</span><span class="sxs-lookup"><span data-stu-id="21161-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-245">QL2</span><span class="sxs-lookup"><span data-stu-id="21161-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-246">P1</span><span class="sxs-lookup"><span data-stu-id="21161-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-247">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-248">Nicio</span><span class="sxs-lookup"><span data-stu-id="21161-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-249">Da</span><span class="sxs-lookup"><span data-stu-id="21161-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-250">Nicio</span><span class="sxs-lookup"><span data-stu-id="21161-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="21161-251">O1</span><span class="sxs-lookup"><span data-stu-id="21161-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-252">T1</span><span class="sxs-lookup"><span data-stu-id="21161-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-253">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-254">P1</span><span class="sxs-lookup"><span data-stu-id="21161-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-255">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="21161-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-256">Da</span><span class="sxs-lookup"><span data-stu-id="21161-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-257">Da</span><span class="sxs-lookup"><span data-stu-id="21161-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-258">Da</span><span class="sxs-lookup"><span data-stu-id="21161-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-259">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="21161-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-260">Încălcarea regulii #2 de mai sus</span><span class="sxs-lookup"><span data-stu-id="21161-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="21161-261">Q1 include timp, cheltuieli și taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="21161-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="21161-262">QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și se suprapune cu ceea ce este inclus în Q1.</span><span class="sxs-lookup"><span data-stu-id="21161-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-263">O1</span><span class="sxs-lookup"><span data-stu-id="21161-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-264">T1</span><span class="sxs-lookup"><span data-stu-id="21161-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-265">QL2</span><span class="sxs-lookup"><span data-stu-id="21161-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-266">P1</span><span class="sxs-lookup"><span data-stu-id="21161-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-267">Necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-268">Da</span><span class="sxs-lookup"><span data-stu-id="21161-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-269">Da</span><span class="sxs-lookup"><span data-stu-id="21161-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-270">Da</span><span class="sxs-lookup"><span data-stu-id="21161-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-271">O1</span><span class="sxs-lookup"><span data-stu-id="21161-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-272">T1</span><span class="sxs-lookup"><span data-stu-id="21161-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-273">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-274">P1</span><span class="sxs-lookup"><span data-stu-id="21161-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-275">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="21161-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-276">Da</span><span class="sxs-lookup"><span data-stu-id="21161-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-277">Da</span><span class="sxs-lookup"><span data-stu-id="21161-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-278">Da</span><span class="sxs-lookup"><span data-stu-id="21161-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-279">Valid</span><span class="sxs-lookup"><span data-stu-id="21161-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-280">În conformitate cu regula #3 de mai sus,</span><span class="sxs-lookup"><span data-stu-id="21161-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="21161-281">Q1 include timp, cheltuieli și taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="21161-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="21161-282">QL2 include timp, cheltuieli și taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="21161-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="21161-283">Singura validare suplimentară este în jurul subsetului de activități de pe QL1, care sunt diferite de subsetul de activități de pe QL2.</span><span class="sxs-lookup"><span data-stu-id="21161-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="21161-284">Acest lucru asigură că nu există suprapuneri.</span><span class="sxs-lookup"><span data-stu-id="21161-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="21161-285">Acest lucru este realizat de sistem atunci când sarcinile sunt asociate.</span><span class="sxs-lookup"><span data-stu-id="21161-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-286">O1</span><span class="sxs-lookup"><span data-stu-id="21161-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-287">T1</span><span class="sxs-lookup"><span data-stu-id="21161-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-288">QL2</span><span class="sxs-lookup"><span data-stu-id="21161-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-289">P1</span><span class="sxs-lookup"><span data-stu-id="21161-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-290">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="21161-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-291">Da</span><span class="sxs-lookup"><span data-stu-id="21161-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-292">Da</span><span class="sxs-lookup"><span data-stu-id="21161-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-293">Da</span><span class="sxs-lookup"><span data-stu-id="21161-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="21161-294">O1</span><span class="sxs-lookup"><span data-stu-id="21161-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-295">T1</span><span class="sxs-lookup"><span data-stu-id="21161-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-296">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-297">P1</span><span class="sxs-lookup"><span data-stu-id="21161-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-298">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-299">Da</span><span class="sxs-lookup"><span data-stu-id="21161-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-300">Da</span><span class="sxs-lookup"><span data-stu-id="21161-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-301">Da</span><span class="sxs-lookup"><span data-stu-id="21161-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="21161-302">Valid</span><span class="sxs-lookup"><span data-stu-id="21161-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-303">Pe baza regulii #5, Q1 și Q2 sunt două citate cu aceeași oportunitate, astfel încât ambele pot estima pentru aceleași componente ale unui proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-304">O1</span><span class="sxs-lookup"><span data-stu-id="21161-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-305">T2</span><span class="sxs-lookup"><span data-stu-id="21161-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-306">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-307">P1</span><span class="sxs-lookup"><span data-stu-id="21161-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-308">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-309">Da</span><span class="sxs-lookup"><span data-stu-id="21161-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-310">Da</span><span class="sxs-lookup"><span data-stu-id="21161-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-311">Da</span><span class="sxs-lookup"><span data-stu-id="21161-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="21161-312">O1</span><span class="sxs-lookup"><span data-stu-id="21161-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-313">T1</span><span class="sxs-lookup"><span data-stu-id="21161-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-314">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-315">P1</span><span class="sxs-lookup"><span data-stu-id="21161-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-316">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-317">Da</span><span class="sxs-lookup"><span data-stu-id="21161-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-318">Da</span><span class="sxs-lookup"><span data-stu-id="21161-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-319">Da</span><span class="sxs-lookup"><span data-stu-id="21161-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="21161-320">Valid</span><span class="sxs-lookup"><span data-stu-id="21161-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="21161-321">Pe baza regulii #4, Q1 și Q2 sunt două citate cu oportunități diferite, astfel încât ambele nu pot estima pentru aceleași componente ale aceluiași proiect.</span><span class="sxs-lookup"><span data-stu-id="21161-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="21161-322">O2</span><span class="sxs-lookup"><span data-stu-id="21161-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="21161-323">T1</span><span class="sxs-lookup"><span data-stu-id="21161-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-324">QL1</span><span class="sxs-lookup"><span data-stu-id="21161-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-325">P1</span><span class="sxs-lookup"><span data-stu-id="21161-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="21161-326">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="21161-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-327">Da</span><span class="sxs-lookup"><span data-stu-id="21161-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="21161-328">Da</span><span class="sxs-lookup"><span data-stu-id="21161-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="21161-329">Da</span><span class="sxs-lookup"><span data-stu-id="21161-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="21161-330">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="21161-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

