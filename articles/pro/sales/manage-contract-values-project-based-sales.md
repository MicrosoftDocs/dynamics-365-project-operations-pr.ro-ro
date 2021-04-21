---
title: Prezentare generală a liniilor de contract bazate pe proiect
description: Acest subiect oferă informații despre lucrul cu linii de contract bazate pe proiect.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858173"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="0dbab-103">Prezentare generală a liniilor de contract bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="0dbab-103">Project-based contract lines overview</span></span>

<span data-ttu-id="0dbab-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="0dbab-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0dbab-105">Liniile de contract bazate pe proiecte din Dynamics 365 Project Operations sunt concepute pentru a păstra acordurile de estimare și facturare pentru anumite componente ale lucrărilor de proiect într-un angajament.</span><span class="sxs-lookup"><span data-stu-id="0dbab-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="0dbab-106">Structura unei linii de contract bazate pe proiect este extinsă pentru estimări de proiect și scenarii de facturare cu următoarele concepte:</span><span class="sxs-lookup"><span data-stu-id="0dbab-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="0dbab-107">Metoda de facturare</span><span class="sxs-lookup"><span data-stu-id="0dbab-107">Billing method</span></span>
- <span data-ttu-id="0dbab-108">Mapare de proiect și activități</span><span class="sxs-lookup"><span data-stu-id="0dbab-108">Project and task mapping</span></span>
- <span data-ttu-id="0dbab-109">Clase de tranzacții incluse</span><span class="sxs-lookup"><span data-stu-id="0dbab-109">Included transaction classes</span></span>
- <span data-ttu-id="0dbab-110">Limită de nedepășire</span><span class="sxs-lookup"><span data-stu-id="0dbab-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="0dbab-111">Configurare posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="0dbab-111">Chargeability setup</span></span>
- <span data-ttu-id="0dbab-112">Estimări utilizând detaliile liniei contractului</span><span class="sxs-lookup"><span data-stu-id="0dbab-112">Estimates using contract line details</span></span>
- <span data-ttu-id="0dbab-113">Clienți de linie de contract</span><span class="sxs-lookup"><span data-stu-id="0dbab-113">Contract line customers</span></span>

<span data-ttu-id="0dbab-114">Următorul tabel include câmpurile de pe fila **General** a liniilor contractuale bazate pe proiecte care ajută la stabilirea bazei pentru o estimare detaliată și bazată pe aranjamente de facturare pentru lucrările bazate pe proiect.</span><span class="sxs-lookup"><span data-stu-id="0dbab-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="0dbab-115">Câmp</span><span class="sxs-lookup"><span data-stu-id="0dbab-115">Field</span></span> | <span data-ttu-id="0dbab-116">Descriere</span><span class="sxs-lookup"><span data-stu-id="0dbab-116">Description</span></span> | <span data-ttu-id="0dbab-117">Impactul din aval</span><span class="sxs-lookup"><span data-stu-id="0dbab-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0dbab-118">**Nume**</span><span class="sxs-lookup"><span data-stu-id="0dbab-118">**Name**</span></span> | <span data-ttu-id="0dbab-119">Numele liniei de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-119">Name of the contract line.</span></span> <span data-ttu-id="0dbab-120">Aceasta identifică componenta discretă a contractului care este estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="0dbab-121">Pentru un contract de proiect creat dintr-o ofertă, această valoare este copiată dintr-o valoare corespunzătoare a liniei de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="0dbab-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="0dbab-122">Numele copiat peste linia de facturare a proiectului care este creată din această linie de contract la crearea facturii.</span><span class="sxs-lookup"><span data-stu-id="0dbab-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="0dbab-123">**Metodă de facturare**</span><span class="sxs-lookup"><span data-stu-id="0dbab-123">**Billing Method**</span></span> | <span data-ttu-id="0dbab-124">Pe un contract de proiect creat dintr-o ofertă, această valoare este copiată din câmpul corespunzător pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="0dbab-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="0dbab-125">Acesta este un set de opțiuni care reprezintă cele două modele principale de contractare susținute de Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0dbab-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="0dbab-126">- **Preț fix**</span><span class="sxs-lookup"><span data-stu-id="0dbab-126">- **Fixed Price**</span></span></br><span data-ttu-id="0dbab-127">- **Ora și materialul**</span><span class="sxs-lookup"><span data-stu-id="0dbab-127">- **Time and Material**</span></span> | <span data-ttu-id="0dbab-128">Pe baza metodei de facturare a liniei contractuale de referință, tranzacția efectivă va fi procesată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="0dbab-129">Dacă linia contractuală la care se face referire prin real are o metodă de facturare a timpului și a materialelor, se creează un cost și înregistrări reale ale vânzărilor nefacturate.</span><span class="sxs-lookup"><span data-stu-id="0dbab-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="0dbab-130">Dacă linia contractuală la care se face referire prin actual are o metodă de facturare cu preț fix, se creează doar un cost real.</span><span class="sxs-lookup"><span data-stu-id="0dbab-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="0dbab-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="0dbab-131">**Project**</span></span> | <span data-ttu-id="0dbab-132">Utilizați acest câmp pentru a identifica proiectul care va fi utilizat pentru a realiza lucrările legate de acest angajament.</span><span class="sxs-lookup"><span data-stu-id="0dbab-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="0dbab-133">Această valoare va fi utilizată împreună cu **Sarcini incluse** și **Clase de tranzacții incluse** pentru a rezolva referința liniei de contract pe o înregistrare de linie reală sau estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="0dbab-134">**Activități incluse**</span><span class="sxs-lookup"><span data-stu-id="0dbab-134">**Included Tasks**</span></span> | <span data-ttu-id="0dbab-135">Indică dacă această linie de contract include toate sarcinile proiectului pentru proiectul selectat sau numai un subset de sarcini.</span><span class="sxs-lookup"><span data-stu-id="0dbab-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="0dbab-136">Acesta este un set de opțiuni care are următoarele valori posibile:</span><span class="sxs-lookup"><span data-stu-id="0dbab-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="0dbab-137">- **Toate activitățile de proiect**</span><span class="sxs-lookup"><span data-stu-id="0dbab-137">- **All Project Tasks**</span></span></br><span data-ttu-id="0dbab-138">- **Numai activități de proiect selectate**.</span><span class="sxs-lookup"><span data-stu-id="0dbab-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="0dbab-139">O valoare necompletată în acest câmp este egală cu selectarea **Toate activitățile proiectului**.</span><span class="sxs-lookup"><span data-stu-id="0dbab-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="0dbab-140">Dacă este selectat **Numai activități selectate**, puteți selecta anumite sarcini și le puteți asocia la această linie contractuală pe fila **Configurarea facturării sarcinilor** de pe pagina **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="0dbab-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="0dbab-141">Valoarea va fi utilizată împreună cu **Proiect** și clase de **Tranzacții incluse** pentru a rezolva referința liniei contractului pe o înregistrare de linie reală sau estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0dbab-142">**Includeți timpul**</span><span class="sxs-lookup"><span data-stu-id="0dbab-142">**Include Time**</span></span> | <span data-ttu-id="0dbab-143">O valoare **Da**/**Nu** indică dacă tranzacțiile de timp sau costurile forței de muncă pentru proiectul selectat vor fi incluse pe această linie de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0dbab-144">O valoare **Nu** indică faptul că timpul tranzacțiilor sau costurile forței de muncă nu vor fi incluse pe această linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="0dbab-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="0dbab-145">O valoare **Da** indică faptul că vor fi.</span><span class="sxs-lookup"><span data-stu-id="0dbab-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="0dbab-146">Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0dbab-147">**Includeți cheltuielile**</span><span class="sxs-lookup"><span data-stu-id="0dbab-147">**Include Expense**</span></span> | <span data-ttu-id="0dbab-148">O valoare **Da**/**Nu** indică dacă costurile de cheltuieli pentru proiectul selectat vor fi incluse în această linie de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0dbab-149">O valoare **Nu** indică faptul că costul de cheltuieli nu vor fi incluse pe această linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="0dbab-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="0dbab-150">O valoare **Da** indică faptul că va fi.</span><span class="sxs-lookup"><span data-stu-id="0dbab-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="0dbab-151">Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0dbab-152">**Includere materiale**</span><span class="sxs-lookup"><span data-stu-id="0dbab-152">**Include Materials**</span></span> | <span data-ttu-id="0dbab-153">O valoare **Da**/**Nu** indică dacă costurile de materiale pentru proiectul selectat vor fi incluse în această linie de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0dbab-154">O valoare **Nu** indică că costurile cu materiale nu vor fi incluse în această linie de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="0dbab-155">O valoare **Da** indică faptul că va fi.</span><span class="sxs-lookup"><span data-stu-id="0dbab-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="0dbab-156">Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0dbab-157">**Includeți tariful**</span><span class="sxs-lookup"><span data-stu-id="0dbab-157">**Include Fee**</span></span> | <span data-ttu-id="0dbab-158">O valoare **Da**/**Nu** indică dacă taxele pentru proiectul selectat vor fi incluse în această linie de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0dbab-159">O valoare **Nu** indică faptul că taxeel nu vor fi incluse pe această linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="0dbab-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="0dbab-160">O valoare **Da** indică faptul că vor fi.</span><span class="sxs-lookup"><span data-stu-id="0dbab-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="0dbab-161">Această valoare este utilizată împreună cu proiectul pentru a rezolva referința liniei de contract într-o înregistrare de linie reală sau estimată.</span><span class="sxs-lookup"><span data-stu-id="0dbab-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0dbab-162">**Cantitate contractată**</span><span class="sxs-lookup"><span data-stu-id="0dbab-162">**Contracted Amount**</span></span> | <span data-ttu-id="0dbab-163">Pe o linie contractuală cu preț fix, această sumă este valoarea convenită care va fi facturată clientului pentru toate componentele de lucru asociate acestei linii contractuale.</span><span class="sxs-lookup"><span data-stu-id="0dbab-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="0dbab-164">Pe o linie de contract de timp și material, această sumă este o valoare estimată a ceea ce va fi facturat clientului pentru toate componentele de lucru asociate acestei linii de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="0dbab-165">Pe un contract de proiect care este creat dintr-o ofertă, această valoare este copiată din câmpul corespunzător pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="0dbab-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="0dbab-166">Când o linie de contract bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma din detaliile liniei de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="0dbab-167">Când linia contractuală are detalii de linie, această valoare poate fi modificată prin modificarea sumelor din detaliile liniei.</span><span class="sxs-lookup"><span data-stu-id="0dbab-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="0dbab-168">Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera suma înainte de impozitare pentru etapele de facturare periodice.</span><span class="sxs-lookup"><span data-stu-id="0dbab-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="0dbab-169">**Impozit estimat**</span><span class="sxs-lookup"><span data-stu-id="0dbab-169">**Estimated Tax**</span></span> | <span data-ttu-id="0dbab-170">Utilizatorul poate edita acest câmp pentru a introduce valoarea taxei estimate pe linia contractului.</span><span class="sxs-lookup"><span data-stu-id="0dbab-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="0dbab-171">Când o linie de contract bazată pe proiect are detalii despre linie, acest câmp este blocat pentru editare și este rezumat din suma taxelor din detaliile liniei de contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="0dbab-172">Când linia contractuală are detalii de linie, această valoare poate fi modificată prin modificarea sumelor taxelor din detaliile liniei.</span><span class="sxs-lookup"><span data-stu-id="0dbab-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="0dbab-173">Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera impozitul pentru etapele de facturare periodice.</span><span class="sxs-lookup"><span data-stu-id="0dbab-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="0dbab-174">**Valoare contractată după impozitare**</span><span class="sxs-lookup"><span data-stu-id="0dbab-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="0dbab-175">Suma de pe linia de contract după impozit.</span><span class="sxs-lookup"><span data-stu-id="0dbab-175">The contract line amount after tax.</span></span> <span data-ttu-id="0dbab-176">Acest câmp este numai în citire și este calculat ca **Suma contractată + impozit**.</span><span class="sxs-lookup"><span data-stu-id="0dbab-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="0dbab-177">Pe o linie contractuală cu preț fix, această valoare este utilizată pentru a genera etapele de facturare periodice.</span><span class="sxs-lookup"><span data-stu-id="0dbab-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="0dbab-178">**Limită de nedepășire**</span><span class="sxs-lookup"><span data-stu-id="0dbab-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="0dbab-179">Utilizatorul poate edita acest câmp și este disponibil numai pe linii de contract bazate pe proiecte care au metoda de facturare setată ca timp și materiale.</span><span class="sxs-lookup"><span data-stu-id="0dbab-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="0dbab-180">Utilizatorul poate edita acest câmp.</span><span class="sxs-lookup"><span data-stu-id="0dbab-180">The user can edit this field.</span></span> <span data-ttu-id="0dbab-181">Atunci când o cheltuială de timp sau de material face referire la această linie contractuală în ceea ce privește timpul și materialul, suma reală este evaluată în raport cu limita care nu trebuie depășită pe această linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="0dbab-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="0dbab-182">Această evaluare este finalizată după contabilizarea sumelor deja cheltuite și angajate.</span><span class="sxs-lookup"><span data-stu-id="0dbab-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="0dbab-183">**Buget client**</span><span class="sxs-lookup"><span data-stu-id="0dbab-183">**Customer Budget**</span></span> | <span data-ttu-id="0dbab-184">Acest câmp este editabil și este copiat din câmpul corespondent pe linia de ofertă, dacă contractul a fost creat dintr-o ofertă.</span><span class="sxs-lookup"><span data-stu-id="0dbab-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="0dbab-185">Acest câmp este utilizat doar pentru informații și nu are nicio semnificație din aval.</span><span class="sxs-lookup"><span data-stu-id="0dbab-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="0dbab-186">Regulile de validare pentru opțiunile din fila General a liniilor contractuale bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="0dbab-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="0dbab-187">Regula 1: Dacă câmpul **Activități incluse** este necompletat sau setat la **Toate activitățile proiectului**, toate activitățile proiectului sunt incluse pe linia contractului.</span><span class="sxs-lookup"><span data-stu-id="0dbab-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="0dbab-188">Regula 2: Când câmpul **Activități incluse** este necompletat sau setat în mod explicit la **Toate activitățile proiectului**, un proiect și o anumită clasă de tranzacții pot fi incluse numai pe o linie de contract bazată pe proiect a unui contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="0dbab-189">Regula 3: Când câmpul **Activități incluse** este setat la **Doar activități de proiect selectate**, un proiect și o anumită clasă de tranzacție poate fi inclusă pe mai multe linii de contract pe bază de proiect a unui contract.</span><span class="sxs-lookup"><span data-stu-id="0dbab-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="0dbab-190">
                    <strong>Contract</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0dbab-191">
                    <strong>Linie contract</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0dbab-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="0dbab-193">
                    <strong>Activități incluse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0dbab-194">
                    <strong>Includeți timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0dbab-195">
                    <strong>Includeți cheltuielile</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0dbab-196">
                    <strong>Includere materiale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0dbab-197">
                    <strong>Includere</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0dbab-198">
                    <strong>Taxă</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="0dbab-199">
                    <strong>Valid/nu este valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="0dbab-200">
                    <strong>Motiv</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0dbab-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-201">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-202">CL1</span><span class="sxs-lookup"><span data-stu-id="0dbab-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-203">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-204">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-205">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-206">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-207">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-208">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-209">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="0dbab-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-210">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="0dbab-210">Violation of Rule #2.</span></span> <span data-ttu-id="0dbab-211">Timpul, cheltuielile, materialele și taxele pentru proiectul P1 sunt incluse în ambele linii de ofertă, CL1 și CL2.</span><span class="sxs-lookup"><span data-stu-id="0dbab-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-212">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-213">CL2</span><span class="sxs-lookup"><span data-stu-id="0dbab-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-214">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-215">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-216">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-217">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-218">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-219">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-220">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-221">CL1</span><span class="sxs-lookup"><span data-stu-id="0dbab-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-222">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-223">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-224">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-225">No</span><span class="sxs-lookup"><span data-stu-id="0dbab-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-226">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-227">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-228">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="0dbab-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-229">Încălcarea regulii #2.</span><span class="sxs-lookup"><span data-stu-id="0dbab-229">Violation of Rule #2.</span></span> <span data-ttu-id="0dbab-230">Timpul, materialele și taxele pentru proiectul P1 sunt incluse în ambele linii de ofertă, CL1 și CL2.</span><span class="sxs-lookup"><span data-stu-id="0dbab-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-231">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-232">CL2</span><span class="sxs-lookup"><span data-stu-id="0dbab-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-233">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-234">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-235">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-236">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-237">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-238">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-239">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-240">CL1</span><span class="sxs-lookup"><span data-stu-id="0dbab-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-241">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-242">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-243">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-244">No</span><span class="sxs-lookup"><span data-stu-id="0dbab-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-245">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-246">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-247">Valid</span><span class="sxs-lookup"><span data-stu-id="0dbab-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-248">Timpul, materialele și taxele pentru proiectul P1 sunt incluse pe CL1.</span><span class="sxs-lookup"><span data-stu-id="0dbab-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="0dbab-249">Cheltuielile pentru proiectul P1 sunt incluse în CL2.</span><span class="sxs-lookup"><span data-stu-id="0dbab-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="0dbab-250">Nicio suprapunere în ceea ce este inclus pe fiecare linie de contract și, prin urmare, este valabilă.</span><span class="sxs-lookup"><span data-stu-id="0dbab-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-251">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-252">CL2</span><span class="sxs-lookup"><span data-stu-id="0dbab-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-253">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-254">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-255">No</span><span class="sxs-lookup"><span data-stu-id="0dbab-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-256">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-257">No</span><span class="sxs-lookup"><span data-stu-id="0dbab-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-258">No</span><span class="sxs-lookup"><span data-stu-id="0dbab-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-259">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-260">CL1</span><span class="sxs-lookup"><span data-stu-id="0dbab-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-261">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-262">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="0dbab-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-263">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-264">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-265">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-266">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-267">Nu este valid</span><span class="sxs-lookup"><span data-stu-id="0dbab-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-268">Încălcarea regulii #2</span><span class="sxs-lookup"><span data-stu-id="0dbab-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="0dbab-269">C1 include Timp, Materiale, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="0dbab-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0dbab-270">CL2 include timp, materiale, cheltuieli și taxe pentru întregul proiect P1 și, prin urmare, se suprapune cu ceea ce este inclus pe C1.</span><span class="sxs-lookup"><span data-stu-id="0dbab-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-271">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-272">CL2</span><span class="sxs-lookup"><span data-stu-id="0dbab-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-273">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-274">Necompletat</span><span class="sxs-lookup"><span data-stu-id="0dbab-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-275">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-276">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-277">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-278">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-279">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-280">CL1</span><span class="sxs-lookup"><span data-stu-id="0dbab-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-281">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-282">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="0dbab-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-283">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-284">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-285">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-286">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-287">Valid</span><span class="sxs-lookup"><span data-stu-id="0dbab-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0dbab-288">Conform regulii nr. 3</span><span class="sxs-lookup"><span data-stu-id="0dbab-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="0dbab-289">C1 include Timp, Cheltuieli, Materiale, Cheltuieli și Taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="0dbab-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0dbab-290">CL2 include Timp, Cheltuieli, Materiale și Taxe pentru un subset de sarcini din proiectul P1.</span><span class="sxs-lookup"><span data-stu-id="0dbab-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0dbab-291">Singura validare suplimentară este în jurul subsetului de sarcini de pe CL1, care este diferit de subsetul de sarcini de pe CL2 pentru a se asigura că nu există suprapuneri acolo.</span><span class="sxs-lookup"><span data-stu-id="0dbab-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="0dbab-292">Acest lucru este realizat de sistem atunci când sarcinile sunt asociate.</span><span class="sxs-lookup"><span data-stu-id="0dbab-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0dbab-293">C1</span><span class="sxs-lookup"><span data-stu-id="0dbab-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0dbab-294">CL2</span><span class="sxs-lookup"><span data-stu-id="0dbab-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-295">P1</span><span class="sxs-lookup"><span data-stu-id="0dbab-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0dbab-296">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="0dbab-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-297">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0dbab-298">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-299">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0dbab-300">Da</span><span class="sxs-lookup"><span data-stu-id="0dbab-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
