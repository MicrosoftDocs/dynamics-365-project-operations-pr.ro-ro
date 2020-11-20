---
title: Prezentare generală a liniilor de oferte bazate pe proiect - simplificat
description: Acest subiect oferă informații despre utilizarea liniilor de ofertă bazate pe proiecte pentru lucrările de proiect. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181107"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="f0e66-104">Prezentare generală a liniilor de oferte bazate pe proiect - simplificat</span><span class="sxs-lookup"><span data-stu-id="f0e66-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="f0e66-105">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="f0e66-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0e66-106">Liniile de ofertă bazate pe proiect sunt concepute pentru a ajuta la estimarea muncii proiectului pe baza unui angajament.</span><span class="sxs-lookup"><span data-stu-id="f0e66-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="f0e66-107">Structura unei linii de ofertă bazată pe proiect este extinsă pentru estimările proiectului cu următoarele concepte:</span><span class="sxs-lookup"><span data-stu-id="f0e66-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="f0e66-108">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="f0e66-108">Billing Method</span></span>
- <span data-ttu-id="f0e66-109">Mapare de proiect și activități</span><span class="sxs-lookup"><span data-stu-id="f0e66-109">Project and Task Mapping</span></span>
- <span data-ttu-id="f0e66-110">Clase de tranzacții incluse</span><span class="sxs-lookup"><span data-stu-id="f0e66-110">Included Transaction classes</span></span>
- <span data-ttu-id="f0e66-111">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="f0e66-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="f0e66-112">Configurare posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="f0e66-112">Chargeability setup</span></span>
- <span data-ttu-id="f0e66-113">Estimare folosind Detaliile liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="f0e66-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="f0e66-114">Clienți de linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="f0e66-114">Quote line Customers</span></span>

<span data-ttu-id="f0e66-115">Următorul tabel oferă informații despre câmpurile de pe fila **General** a liniei de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="f0e66-116">Aceste câmpuri ajută la stabilirea bazei unei estimări detaliate, fundamentate pentru lucrările de proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="f0e66-117">**Câmp**</span><span class="sxs-lookup"><span data-stu-id="f0e66-117">**Field**</span></span> | <span data-ttu-id="f0e66-118">**Descriere**</span><span class="sxs-lookup"><span data-stu-id="f0e66-118">**Description**</span></span> | <span data-ttu-id="f0e66-119">**Impactul din aval**</span><span class="sxs-lookup"><span data-stu-id="f0e66-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f0e66-120">Nume</span><span class="sxs-lookup"><span data-stu-id="f0e66-120">Name</span></span> | <span data-ttu-id="f0e66-121">Numele liniei de cotație care ar trebui să vă ajute să identificați componenta discretă a cotației care este estimată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="f0e66-122">Copiat pe linia contractului de proiect care este creată din această linie de cotație atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-123">Metodă de facturare</span><span class="sxs-lookup"><span data-stu-id="f0e66-123">Billing Method</span></span> | <span data-ttu-id="f0e66-124">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul corespunzător de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="f0e66-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="f0e66-125">Acest câmp include cele două modele principale de contractare acceptate de Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="f0e66-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="f0e66-126">- Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0e66-126">- Fixed price</span></span></br><span data-ttu-id="f0e66-127">- Timp și material.</span><span class="sxs-lookup"><span data-stu-id="f0e66-127">- Time and material.</span></span>| <span data-ttu-id="f0e66-128">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-129">Project</span><span class="sxs-lookup"><span data-stu-id="f0e66-129">Project</span></span> | <span data-ttu-id="f0e66-130">Utilizați acest câmp opțional pentru a identifica proiectul care va fi utilizat pentru a furniza lucrările la acest angajament.</span><span class="sxs-lookup"><span data-stu-id="f0e66-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="f0e66-131">Atunci când un proiect este mapat la o linie de ofertă, ajută la configurarea sarcinilor cu taxă și, de asemenea, la introducerea unei estimări bazate pe proiect la linia de estimare ca detalii despre linia de estimare.</span><span class="sxs-lookup"><span data-stu-id="f0e66-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="f0e66-132">Atunci când un proiect nu este mapat la o linie de ofertă bazată pe proiect, devizul trebuie creat manual prin crearea fiecărui detaliu al liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="f0e66-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="f0e66-133">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="f0e66-134">Activități incluse</span><span class="sxs-lookup"><span data-stu-id="f0e66-134">Included Tasks</span></span> | <span data-ttu-id="f0e66-135">Indică dacă această linie de cotație este utilizată pentru toate sau unele dintre sarcinile proiectului pentru proiectul selectat.</span><span class="sxs-lookup"><span data-stu-id="f0e66-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="f0e66-136">Acest câmp are următoarele valori posibile:</span><span class="sxs-lookup"><span data-stu-id="f0e66-136">This field has the following possible values:</span></span></br><span data-ttu-id="f0e66-137">- Toate activitățile de proiect</span><span class="sxs-lookup"><span data-stu-id="f0e66-137">- All project tasks</span></span></br><span data-ttu-id="f0e66-138">- Numai activități de proiect selectate</span><span class="sxs-lookup"><span data-stu-id="f0e66-138">- Selected project tasks only</span></span></br><span data-ttu-id="f0e66-139">O valoare necompletată în acest câmp este echivalentă cu opțiunea **Toate sarcinile proiectului**.</span><span class="sxs-lookup"><span data-stu-id="f0e66-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="f0e66-140">Când **Numai sarcini de proiect selectate** este selectat apoi pe pagina de proiect, fila **Configurarea activității de facturare** vă permite să selectați activități specifice pentru a le asocia la această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="f0e66-141">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-142">Includeți timpul</span><span class="sxs-lookup"><span data-stu-id="f0e66-142">Include Time</span></span> | <span data-ttu-id="f0e66-143">Un semnalizator **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f0e66-144">O valoare de semnalizator **Nu** indică faptul că tranzacțiile de timp sau costul cu forța de muncă nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f0e66-145">O valoare de semnalizator **Da** indică faptul că tranzacțiile de timp sau costul cu forța de muncă vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f0e66-146">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-147">Includeți cheltuielile</span><span class="sxs-lookup"><span data-stu-id="f0e66-147">Include Expense</span></span> | <span data-ttu-id="f0e66-148">Un semnalizator **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f0e66-149">O valoare de semnalizator **Nu** indică faptul că costurile de cheltuieli nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f0e66-150">O valoare de semnalizator **Da** indică faptul că costurile de cheltuieli vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f0e66-151">Această valoare de câmp este copiată peste linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-152">Includeți tariful</span><span class="sxs-lookup"><span data-stu-id="f0e66-152">Include Fee</span></span> | <span data-ttu-id="f0e66-153">Un semnalizator **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în estimarea de pe această linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="f0e66-154">O valoare de semnalizator **Nu** indică faptul că taxele nu vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="f0e66-155">O valoare de semnalizator **Da** indică faptul că taxele vor fi incluse în estimarea acestei linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="f0e66-156">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-157">Valoare cotă</span><span class="sxs-lookup"><span data-stu-id="f0e66-157">Quoted Amount</span></span> | <span data-ttu-id="f0e66-158">Aceasta este suma care va fi cotată clientului pentru toate lucrările prognozate pe această linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="f0e66-159">Pe o ofertă creată dintr-o oportunitate, această valoare este copiată din câmpul **Buget de client** de pe linia de oportunitate.</span><span class="sxs-lookup"><span data-stu-id="f0e66-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="f0e66-160">Când linia de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="f0e66-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="f0e66-161">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-162">Impozit estimat</span><span class="sxs-lookup"><span data-stu-id="f0e66-162">Estimated Tax</span></span> | <span data-ttu-id="f0e66-163">Acesta este un câmp editabil pentru ca utilizatorul să adauge suma fiscală estimată pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="f0e66-164">Când o linie de estimare bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de estimare.</span><span class="sxs-lookup"><span data-stu-id="f0e66-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="f0e66-165">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-166">Valoare ofertată după taxe</span><span class="sxs-lookup"><span data-stu-id="f0e66-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="f0e66-167">Acest câmp reprezintă suma liniei de cotare după impozitare și este doar în citire.</span><span class="sxs-lookup"><span data-stu-id="f0e66-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="f0e66-168">Suma din acest câmp este calculată ca *Suma oferită + Taxe*.</span><span class="sxs-lookup"><span data-stu-id="f0e66-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="f0e66-169">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-170">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="f0e66-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="f0e66-171">Acest câmp este editabil și este disponibil numai pe liniile de cotație bazate pe proiecte care au o metodă de facturare **Timp și material**.</span><span class="sxs-lookup"><span data-stu-id="f0e66-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="f0e66-172">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="f0e66-173">Buget client</span><span class="sxs-lookup"><span data-stu-id="f0e66-173">Customer Budget</span></span> | <span data-ttu-id="f0e66-174">Acest câmp se poate edita și este copiat din câmpul corespunzător de pe linia de oportunitate dacă oferta a fost creată dintr-o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="f0e66-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="f0e66-175">Această valoare de câmp este copiată pe linia de contract de proiect care este creată din această linie de ofertă atunci când oferta este câștigată.</span><span class="sxs-lookup"><span data-stu-id="f0e66-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="f0e66-176">Reguli de validare pentru câmpurile din fila General a liniilor de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="f0e66-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="f0e66-177">**Regula 1**: Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului**, un proiect este inclus în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="f0e66-178">**Regula 2**: Dacă câmpul **Sarcini incluse** este necompletat sau dacă este setat la **Toate sarcinile proiectului**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o singură linie de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="f0e66-179">**Regula 3**: Dacă câmpul **Sarcini incluse** este setat la **Doar activitățile de proiect selectate**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de ofertă multiplă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="f0e66-180">**Regula 4**: Dacă o oportunitate are mai multe ghilimele, pot exista linii de ofertă din oferte diferite care fac referire la același proiect și includ aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="f0e66-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="f0e66-181">**Regula 5**: Dacă ofertele nu aparțin aceleiași oportunități, nu pot include același proiect și aceeași clasă de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="f0e66-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="f0e66-182">
                    <strong>Oportunitate</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="f0e66-183">
                    <strong>Ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f0e66-184">
                    <strong>Linie de ofertă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f0e66-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="f0e66-186">
                    <strong>Activități incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="f0e66-187">
                    <strong>Includeți timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="f0e66-188">
                    <strong>Includeți cheltuielile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="f0e66-189">
                    <strong>Includere</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="f0e66-190">
                    <strong>Taxă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="f0e66-191">
                    <strong>Valid/nu este valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="f0e66-192">
                    <strong>Motiv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f0e66-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-193">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-194">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-195">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-196">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-197">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-198">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-199">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-200">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-201">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-202">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="f0e66-202">Violation of Rule #2.</span></span> <span data-ttu-id="f0e66-203">Timpul, cheltuielile și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="f0e66-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-204">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-205">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-206">QL2</span><span class="sxs-lookup"><span data-stu-id="f0e66-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-207">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-208">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-209">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-210">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-211">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-211">Yes</span></span> </p>
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
<span data-ttu-id="f0e66-212">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-213">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-214">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-215">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-216">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-217">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-218">Nicio</span><span class="sxs-lookup"><span data-stu-id="f0e66-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-219">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-220">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-221">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="f0e66-221">Violation of Rule #2.</span></span> <span data-ttu-id="f0e66-222">Timpul și taxele pentru proiectul P1 sunt incluse pe liniile de ofertă, QL1 și QL2.</span><span class="sxs-lookup"><span data-stu-id="f0e66-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-223">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-224">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-225">QL2</span><span class="sxs-lookup"><span data-stu-id="f0e66-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-226">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-227">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-228">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-229">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-230">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-230">Yes</span></span> </p>
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
<span data-ttu-id="f0e66-231">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-232">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-233">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-234">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-235">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-236">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-237">Nicio</span><span class="sxs-lookup"><span data-stu-id="f0e66-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-238">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-239">Valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="f0e66-240">Timpul și taxele pentru proiectul P1 sunt incluse pe QL1.</span><span class="sxs-lookup"><span data-stu-id="f0e66-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="f0e66-241">Cheltuielile pentru proiectul P1 sunt incluse în QL2.</span><span class="sxs-lookup"><span data-stu-id="f0e66-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="f0e66-242">Nu există o suprapunere în ceea ce este inclus pe fiecare linie de ofertă și este valabilă.</span><span class="sxs-lookup"><span data-stu-id="f0e66-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-243">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-244">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-245">QL2</span><span class="sxs-lookup"><span data-stu-id="f0e66-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-246">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-247">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-248">Nicio</span><span class="sxs-lookup"><span data-stu-id="f0e66-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-249">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-250">Nicio</span><span class="sxs-lookup"><span data-stu-id="f0e66-250">No</span></span> </p>
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
<span data-ttu-id="f0e66-251">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-252">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-253">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-254">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-255">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="f0e66-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-256">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-257">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-258">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-259">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-260">Încălcarea regulii #2 de mai sus</span><span class="sxs-lookup"><span data-stu-id="f0e66-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="f0e66-261">Q1 include timp, cheltuieli și taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="f0e66-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f0e66-262">QL2 include timp, cheltuieli și taxe pentru întregul proiect P1 și se suprapune cu ceea ce este inclus în Q1.</span><span class="sxs-lookup"><span data-stu-id="f0e66-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-263">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-264">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-265">QL2</span><span class="sxs-lookup"><span data-stu-id="f0e66-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-266">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-267">Necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-268">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-269">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-270">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-270">Yes</span></span> </p>
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
<span data-ttu-id="f0e66-271">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-272">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-273">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-274">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-275">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="f0e66-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-276">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-277">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-278">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-279">Valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-280">În conformitate cu regula #3 de mai sus,</span><span class="sxs-lookup"><span data-stu-id="f0e66-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="f0e66-281">Q1 include timp, cheltuieli și taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="f0e66-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f0e66-282">QL2 include timp, cheltuieli și taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="f0e66-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="f0e66-283">Singura validare suplimentară este în jurul subsetului de activități de pe QL1, care sunt diferite de subsetul de activități de pe QL2.</span><span class="sxs-lookup"><span data-stu-id="f0e66-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="f0e66-284">Acest lucru asigură că nu există suprapuneri.</span><span class="sxs-lookup"><span data-stu-id="f0e66-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="f0e66-285">Acest lucru este realizat de sistem atunci când sarcinile sunt asociate.</span><span class="sxs-lookup"><span data-stu-id="f0e66-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-286">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-287">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-288">QL2</span><span class="sxs-lookup"><span data-stu-id="f0e66-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-289">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-290">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="f0e66-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-291">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-292">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-293">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-293">Yes</span></span> </p>
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
<span data-ttu-id="f0e66-294">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-295">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-296">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-297">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-298">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-299">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-300">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-301">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="f0e66-302">Valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-303">Pe baza regulii #5, Q1 și Q2 sunt două citate cu aceeași oportunitate, astfel încât ambele pot estima pentru aceleași componente ale unui proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-304">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-305">T2</span><span class="sxs-lookup"><span data-stu-id="f0e66-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-306">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-307">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-308">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-309">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-310">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-311">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-311">Yes</span></span> </p>
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
<span data-ttu-id="f0e66-312">O1</span><span class="sxs-lookup"><span data-stu-id="f0e66-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-313">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-314">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-315">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-316">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-317">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-318">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-319">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="f0e66-320">Valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="f0e66-321">Pe baza regulii #4, Q1 și Q2 sunt două citate cu oportunități diferite, astfel încât ambele nu pot estima pentru aceleași componente ale aceluiași proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e66-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="f0e66-322">O2</span><span class="sxs-lookup"><span data-stu-id="f0e66-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="f0e66-323">T1</span><span class="sxs-lookup"><span data-stu-id="f0e66-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-324">QL1</span><span class="sxs-lookup"><span data-stu-id="f0e66-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-325">P1</span><span class="sxs-lookup"><span data-stu-id="f0e66-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="f0e66-326">Toate activitățile de proiect sau necompletat</span><span class="sxs-lookup"><span data-stu-id="f0e66-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-327">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="f0e66-328">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="f0e66-329">Da</span><span class="sxs-lookup"><span data-stu-id="f0e66-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="f0e66-330">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="f0e66-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

