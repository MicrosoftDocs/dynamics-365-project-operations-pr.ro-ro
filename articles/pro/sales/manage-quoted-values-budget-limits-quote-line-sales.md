---
title: 'Prezentare generală linii de oferte bazate pe proiect '
description: Acest subiect oferă informații despre utilizarea liniilor de ofertă bazate pe proiecte pentru lucrările de proiect.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994871"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="73e3c-103">Prezentare generală a liniilor de oferte bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="73e3c-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="73e3c-104">_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_</span><span class="sxs-lookup"><span data-stu-id="73e3c-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="73e3c-105">Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament.</span><span class="sxs-lookup"><span data-stu-id="73e3c-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="73e3c-106">Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:</span><span class="sxs-lookup"><span data-stu-id="73e3c-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="73e3c-107">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="73e3c-107">Billing Method</span></span>
- <span data-ttu-id="73e3c-108">Mapare de proiect și activități</span><span class="sxs-lookup"><span data-stu-id="73e3c-108">Project and Task Mapping</span></span>
- <span data-ttu-id="73e3c-109">Clase de tranzacții incluse</span><span class="sxs-lookup"><span data-stu-id="73e3c-109">Included Transaction classes</span></span>
- <span data-ttu-id="73e3c-110">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="73e3c-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="73e3c-111">Configurare posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="73e3c-111">Chargeability setup</span></span>
- <span data-ttu-id="73e3c-112">Estimare folosind Detaliile liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="73e3c-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="73e3c-113">Clienți de linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="73e3c-113">Quote line Customers</span></span>

<span data-ttu-id="73e3c-114">Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="73e3c-115">Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="73e3c-116">**Câmp**</span><span class="sxs-lookup"><span data-stu-id="73e3c-116">**Field**</span></span> | <span data-ttu-id="73e3c-117">**Descriere**</span><span class="sxs-lookup"><span data-stu-id="73e3c-117">**Description**</span></span> | <span data-ttu-id="73e3c-118">**Impactul din aval**</span><span class="sxs-lookup"><span data-stu-id="73e3c-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="73e3c-119">Nume</span><span class="sxs-lookup"><span data-stu-id="73e3c-119">Name</span></span> | <span data-ttu-id="73e3c-120">Numele liniei de ofertă care vă ajută să identificați componenta discretă a ofertei care este estimată.</span><span class="sxs-lookup"><span data-stu-id="73e3c-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="73e3c-121">Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="73e3c-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-122">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="73e3c-122">Billing Method</span></span> | <span data-ttu-id="73e3c-123">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="73e3c-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="73e3c-124">Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="73e3c-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="73e3c-125">- Preț fix</span><span class="sxs-lookup"><span data-stu-id="73e3c-125">- Fixed price</span></span></br><span data-ttu-id="73e3c-126">- Timp și material.</span><span class="sxs-lookup"><span data-stu-id="73e3c-126">- Time and material.</span></span>| <span data-ttu-id="73e3c-127">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-128">Project</span><span class="sxs-lookup"><span data-stu-id="73e3c-128">Project</span></span> | <span data-ttu-id="73e3c-129">Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament.</span><span class="sxs-lookup"><span data-stu-id="73e3c-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="73e3c-130">Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare.</span><span class="sxs-lookup"><span data-stu-id="73e3c-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="73e3c-131">Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="73e3c-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="73e3c-132">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="73e3c-133">Activități incluse</span><span class="sxs-lookup"><span data-stu-id="73e3c-133">Included Tasks</span></span> | <span data-ttu-id="73e3c-134">Indică dacă această linie de cotație este utilizată pentru toate sau unele dintre sarcinile proiectului pentru proiectul selectat.</span><span class="sxs-lookup"><span data-stu-id="73e3c-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="73e3c-135">Acest câmp are următoarele valori posibile:</span><span class="sxs-lookup"><span data-stu-id="73e3c-135">This field has the following possible values:</span></span></br><span data-ttu-id="73e3c-136">- Toate activitățile de proiect</span><span class="sxs-lookup"><span data-stu-id="73e3c-136">- All project tasks</span></span></br><span data-ttu-id="73e3c-137">- Numai activități de proiect selectate</span><span class="sxs-lookup"><span data-stu-id="73e3c-137">- Selected project tasks only</span></span></br><span data-ttu-id="73e3c-138">O valoare necompletată în acest câmp este echivalentă cu opțiunea **Toate sarcinile proiectului**.</span><span class="sxs-lookup"><span data-stu-id="73e3c-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="73e3c-139">Când este selectat **Numai sarcini de proiect selectate** pe pagina proiectului, fila **Configurarea activității de facturare** vă permite să selectați sarcini specifice pentru a le asocia la această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="73e3c-140">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-141">Includeți timpul</span><span class="sxs-lookup"><span data-stu-id="73e3c-141">Include Time</span></span> | <span data-ttu-id="73e3c-142">O valoare **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-143">O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-144">O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="73e3c-145">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-146">Includeți cheltuielile</span><span class="sxs-lookup"><span data-stu-id="73e3c-146">Include Expense</span></span> | <span data-ttu-id="73e3c-147">O valoare **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-148">O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-149">O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="73e3c-150">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-151">Includeți materialele</span><span class="sxs-lookup"><span data-stu-id="73e3c-151">Include Material</span></span> | <span data-ttu-id="73e3c-152">O valoare **Da**/**Nu** indică dacă costurile cu materiale pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-153">O valoare **Nu** indică că costurile cu materiale pentru proiectul selectat nu vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-154">O valoare **Da** indică că costurile cu materiale pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="73e3c-155">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-156">Includeți tariful</span><span class="sxs-lookup"><span data-stu-id="73e3c-156">Include Fee</span></span> | <span data-ttu-id="73e3c-157">O valoare **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-158">O valoare **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="73e3c-159">O valoare **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="73e3c-160">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-161">Valoare cotă</span><span class="sxs-lookup"><span data-stu-id="73e3c-161">Quoted Amount</span></span> | <span data-ttu-id="73e3c-162">Aceasta este suma care va fi oferită clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="73e3c-163">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="73e3c-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="73e3c-164">Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="73e3c-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="73e3c-165">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-166">Impozit estimat</span><span class="sxs-lookup"><span data-stu-id="73e3c-166">Estimated Tax</span></span> | <span data-ttu-id="73e3c-167">Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="73e3c-168">Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="73e3c-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="73e3c-169">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-170">Valoare ofertată după taxe</span><span class="sxs-lookup"><span data-stu-id="73e3c-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="73e3c-171">Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire.</span><span class="sxs-lookup"><span data-stu-id="73e3c-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="73e3c-172">Suma din acest câmp este calculată ca *Suma oferită + Taxe*.</span><span class="sxs-lookup"><span data-stu-id="73e3c-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="73e3c-173">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-174">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="73e3c-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="73e3c-175">Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**.</span><span class="sxs-lookup"><span data-stu-id="73e3c-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="73e3c-176">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="73e3c-177">Buget client</span><span class="sxs-lookup"><span data-stu-id="73e3c-177">Customer Budget</span></span> | <span data-ttu-id="73e3c-178">Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="73e3c-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="73e3c-179">Această valoare este copiată pe linia contractului de proiect care este creată din această linie de ofertă atunci când este câștigată oferta.</span><span class="sxs-lookup"><span data-stu-id="73e3c-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="73e3c-180">Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="73e3c-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="73e3c-181">**Regula 1**: Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului**, un proiect este inclus în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="73e3c-182">**Regula 2**: Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o singură linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="73e3c-183">**Regula 3**: Dacă câmpul **Sarcini incluse** este setat la **Doar activitățile de proiect selectate**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de ofertă multiplă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="73e3c-184">**Regula 4**: Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="73e3c-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="73e3c-185">**Regula 5**: Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="73e3c-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="73e3c-186">
                    <strong>Oportunitate</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="73e3c-187">
                    <strong>Ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="73e3c-188">
                    <strong>Linie de ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="73e3c-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="73e3c-190">
                    <strong>Activități incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="73e3c-191">
                    <strong>Includeți timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="73e3c-192">
                    <strong>Includeți cheltuielile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="73e3c-193">
                    <strong>Includeți materialele</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="73e3c-194">
                    <strong>Includere</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="73e3c-195">
                    <strong>Taxă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="73e3c-196">
                    <strong>Valid/nu este valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="73e3c-197">
                    <strong>Motiv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="73e3c-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-198">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-199">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-200">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-201">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-202">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-203">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-204">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-205">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-206">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-207">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-208">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="73e3c-208">Violation of Rule #2.</span></span> <span data-ttu-id="73e3c-209">Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-210">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-211">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-212">QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-213">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-214">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-215">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-216">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-217">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-218">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-219">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-220">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-221">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-222">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-223">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-224">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-225">No</span><span class="sxs-lookup"><span data-stu-id="73e3c-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-226">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-227">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-228">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-229">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="73e3c-229">Violation of Rule #2.</span></span> <span data-ttu-id="73e3c-230">Timpul, materialele și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-231">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-232">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-233">QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-234">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-235">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-236">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-237">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-238">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-239">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-240">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-241">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-242">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-243">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-244">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-245">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-246">No</span><span class="sxs-lookup"><span data-stu-id="73e3c-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-247">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-248">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-249">Valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-250">Timpul, materialele și taxele pentru proiectul P1 sunt incluse pe QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="73e3c-251">Cheltuielile pentru proiectul P1 sunt incluse în QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="73e3c-252">Nicio suprapunere în ceea ce este inclus pe fiecare linie de ofertă și, prin urmare, este valabilă.</span><span class="sxs-lookup"><span data-stu-id="73e3c-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-253">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-254">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-255">QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-256">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-257">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-258">No</span><span class="sxs-lookup"><span data-stu-id="73e3c-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-259">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-260">No</span><span class="sxs-lookup"><span data-stu-id="73e3c-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-261">No</span><span class="sxs-lookup"><span data-stu-id="73e3c-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-262">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-263">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-264">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-265">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-266">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="73e3c-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-267">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-268">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-269">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-270">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-271">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-272">Încălcarea regulii #2</span><span class="sxs-lookup"><span data-stu-id="73e3c-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="73e3c-273">Q1 include Timp, Material, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="73e3c-274">QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și, prin urmare, se suprapune cu ceea ce este inclus pe Q1.</span><span class="sxs-lookup"><span data-stu-id="73e3c-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-275">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-276">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-277">QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-278">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-279">Necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-280">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-281">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-282">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-283">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-284">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-285">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-286">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-287">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-288">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="73e3c-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-289">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-290">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-291">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-292">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-293">Valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-294">Conform regulii nr. 3,</span><span class="sxs-lookup"><span data-stu-id="73e3c-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="73e3c-295">Q1 include Timp, Material, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="73e3c-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="73e3c-296">QL2 include Timp, Material, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="73e3c-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="73e3c-297">Singura validare suplimentară este în jurul subsetului de activități de pe QL1, care este diferit de subsetul de activități de pe QL2 pentru a se asigura că nu există suprapuneri.</span><span class="sxs-lookup"><span data-stu-id="73e3c-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="73e3c-298">Acest lucru este realizat de sistem atunci când sarcinile sunt asociate.</span><span class="sxs-lookup"><span data-stu-id="73e3c-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-299">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-300">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-301">QL2</span><span class="sxs-lookup"><span data-stu-id="73e3c-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-302">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-303">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="73e3c-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-304">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-305">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-306">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-307">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-308">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-309">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-310">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-311">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-312">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-313">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-314">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-315">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-316">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-317">Valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-318">Conform regulii # 5, Q1 și Q2 sunt două oferte cu aceeași oportunitate, deci ambele pot estima pentru aceleași componente ale unui proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-319">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-320">T2</span><span class="sxs-lookup"><span data-stu-id="73e3c-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-321">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-322">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-323">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-324">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-325">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-326">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-327">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-328">O1</span><span class="sxs-lookup"><span data-stu-id="73e3c-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-329">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-330">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-331">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-332">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-333">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-334">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-335">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-336">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-337">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="73e3c-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="73e3c-338">Conform regulii # 4, Q1 și Q2 sunt două oferte pe oportunități diferite, deci nu pot estima pentru aceleași componente ale aceluiași proiect.</span><span class="sxs-lookup"><span data-stu-id="73e3c-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="73e3c-339">O2</span><span class="sxs-lookup"><span data-stu-id="73e3c-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="73e3c-340">T1</span><span class="sxs-lookup"><span data-stu-id="73e3c-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="73e3c-341">QL1</span><span class="sxs-lookup"><span data-stu-id="73e3c-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-342">P1</span><span class="sxs-lookup"><span data-stu-id="73e3c-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="73e3c-343">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="73e3c-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="73e3c-344">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="73e3c-345">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="73e3c-346">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="73e3c-347">Da</span><span class="sxs-lookup"><span data-stu-id="73e3c-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
