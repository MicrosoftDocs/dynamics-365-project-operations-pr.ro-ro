---
title: Contracte de proiect
description: Acest subiect oferă exemple de contracte de proiect pe care le puteți crea pentru diferite tipuri de proiecte și surse de finanțare și modul în care puteți gestiona contracte și factura clienții proiectului.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53eb6ff3f98e7efc3d6b997cd4d877025225936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289564"
---
# <a name="project-contracts"></a><span data-ttu-id="2f6b9-103">Contracte de proiect</span><span class="sxs-lookup"><span data-stu-id="2f6b9-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f6b9-104">Acest articol furnizează exemple de contracte de proiect pe care le puteți crea pentru diferite tipuri de proiecte și surse de finanțare și modul în care puteți gestiona contracte și factura clienții proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="2f6b9-105">Tipul de proiect pe care îl creați pentru un contract de proiect determină metoda utilizată pentru a factura clienții proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="2f6b9-106">Puteți modifica un contract de proiect și proiectul aferent, dar nu puteți modifica tipul de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="2f6b9-107">Utilizând un contract de proiect, puteți factura unul sau mai multe proiecte în același timp.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="2f6b9-108">De asemenea, contractul de proiect garantează o procedură de facturare consecventă pentru fiecare subproiect dintr-o structură de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="2f6b9-109">Fiecare proiect care va fi facturat trebuie să fie asociat cu un contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="2f6b9-110">Setările pentru un contract de proiect se aplică tuturor proiectelor și subproiectelor care sunt asociate cu acel contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="2f6b9-111">Un contract de proiect poate specifica una sau mai multe surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="2f6b9-112">Prin urmare, puteți împărți facturarea între mai mulți finanțatori, setați limite de finanțare astfel încât sursele de finanțare să nu fie facturate mai mult decât o sumă specificată și să configurați reguli de finanțare pentru perceperea cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="2f6b9-113">Finanțarea contractelor de proiect</span><span class="sxs-lookup"><span data-stu-id="2f6b9-113">Funding for project contracts</span></span>
<span data-ttu-id="2f6b9-114">Unele contracte de proiect specifică faptul că mai multe părți împart responsabilitatea pentru finanțarea costurilor proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="2f6b9-115">Iată câteva exemple:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-115">Here are some examples:</span></span>

-   <span data-ttu-id="2f6b9-116">Un client mare care are mai multe divizii solicită ca finanțarea unui proiect să fie împărțită pe divizii.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="2f6b9-117">Compania dvs. împarte costurile unui proiect mare cu o organizație externă.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="2f6b9-118">Un proiect rutier este cofinanțat de două municipalități.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="2f6b9-119">Un proiect de pod este finanțat de o subvenție guvernamentală și de o corporație privată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="2f6b9-120">În Dynamics 365 Finance, puteți împărți facturarea pentru o singură tranzacție sau un întreg proiect între mai mulți clienți, subvenții sau organizații.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="2f6b9-121">În proiectele care au mai mulți finanțatori, toate părțile care contribuie la finanțarea unui proiect avansat de finanțare sunt numite surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="2f6b9-122">După ce un client, o organizație sau o bursă este definit ca sursă de finanțare, acesta poate fi atribuit uneia sau mai multor reguli de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="2f6b9-123">Regulile de finanțare conțin criteriile care determină modul în care taxele sunt alocate diferitelor surse de finanțare pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="2f6b9-124">Deoarece articolele stocate, cum ar fi cele care apar în cererile de achiziție și comenzile de cumpărare, nu pot fi împărțite, suma costului nu poate fi împărțită între mai multe surse de finanțare în momentul distribuției.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="2f6b9-125">Prin urmare, valoarea sursei de finanțare rămâne 0 (zero) până la publicarea emisiunii de inventar.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="2f6b9-126">Când este înregistrată problema inventarului, suma costului este distribuită conform regulilor de distribuire a contului pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="2f6b9-127">Iată câțiva pași pe care îi puteți face pentru a facilita împărțirea facturării între mai multe surse de finanțare:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="2f6b9-128">Specificați că toate tranzacțiile introduse pentru un proiect utilizează aceeași monedă de vânzare ca și contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="2f6b9-129">Stabiliți limite de finanțare, astfel încât o sursă de finanțare să nu fie facturată mai mult decât o sumă specificată pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="2f6b9-130">Configurați regulile de finanțare și limitele de finanțare pentru fiecare lucrător, articol, categorie, grup de categorii și tip de tranzacție (sau pentru toate tipurile de tranzacții).</span><span class="sxs-lookup"><span data-stu-id="2f6b9-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="2f6b9-131">Selectați datele opționale de începere și de încheiere pentru a defini perioada în care fiecare regulă de finanțare este valabilă.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="2f6b9-132">Specificați procentul de care este responsabilă fiecare sursă de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="2f6b9-133">Specificați ce sursă de finanțare este responsabilă pentru rotunjirea diferențelor cauzate de calculele alocării finanțării.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="2f6b9-134">Stabiliți reguli care determină modul în care costurile proiectului sunt facturate clienților externi și taxate către organizațiile interne.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="2f6b9-135">Înregistrați tranzacțiile într-un cont de finanțare în așteptare până când se poate obține finanțare suplimentară sau până când decideți să suportați costurile pe plan intern.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="2f6b9-136">Pentru a determina ce grup fiscal se asociază cu o tranzacție, proiectul este căutat pentru o atribuire de grup fiscal.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="2f6b9-137">Dacă nu a fost efectuată nicio atribuire de grup fiscal la nivelul proiectului, se caută contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="2f6b9-138">Exemplu: mai multe surse de finanțare (simple)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="2f6b9-139">Tabelul următor oferă scenarii pentru gestionarea alocării finanțării între mai multe surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="2f6b9-140">Aceste scenarii se bazează pe următoarele ipoteze:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="2f6b9-141">Setările prioritare sunt luate în considerare în alocarea fondurilor înainte de aplicarea altor criterii de regulă de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="2f6b9-142">Nu a fost specificat niciun interval de date pentru a defini perioada când regula de finanțare este valabilă.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f6b9-143"><strong>Scenariu</strong></span><span class="sxs-lookup"><span data-stu-id="2f6b9-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="2f6b9-144"><strong>Sursă de finanțare</strong></span><span class="sxs-lookup"><span data-stu-id="2f6b9-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="2f6b9-145"><strong>Procentul de alocare</strong></span><span class="sxs-lookup"><span data-stu-id="2f6b9-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="2f6b9-146"><strong>Prioritate de alocare</strong></span><span class="sxs-lookup"><span data-stu-id="2f6b9-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f6b9-147">Doriți să alocați costurile unei surse de finanțare până la epuizarea fondurilor sale, alocați costurile unei a doua surse de finanțare până la epuizarea fondurilor sale și, în cele din urmă, alocați costurile rămase la o a treia sursă de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-148">Sursă de　finanțare　1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="2f6b9-149">Sursă de　finanțare　2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="2f6b9-150">Sursă de　finanțare　3</span><span class="sxs-lookup"><span data-stu-id="2f6b9-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-151">100%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-151">100%</span></span></li>
<li><span data-ttu-id="2f6b9-152">100%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-152">100%</span></span></li>
<li><span data-ttu-id="2f6b9-153">100%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-154">1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-154">1</span></span></li>
<li><span data-ttu-id="2f6b9-155">2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-155">2</span></span></li>
<li><span data-ttu-id="2f6b9-156">3</span><span class="sxs-lookup"><span data-stu-id="2f6b9-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f6b9-157">Doriți să alocați 75% din costuri unei surse de finanțare și 25% unei alte surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="2f6b9-158">Când oricare dintre aceste surse de finanțare este epuizată, doriți să plătiți costurile rămase dintr-o a treia sursă de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-159">Sursă de　finanțare　1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="2f6b9-160">Sursă de　finanțare　2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="2f6b9-161">Sursă de　finanțare　3</span><span class="sxs-lookup"><span data-stu-id="2f6b9-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-162">75%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-162">75%</span></span></li>
<li><span data-ttu-id="2f6b9-163">25%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-163">25%</span></span></li>
<li><span data-ttu-id="2f6b9-164">100%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-165">1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-165">1</span></span></li>
<li><span data-ttu-id="2f6b9-166">1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-166">1</span></span></li>
<li><span data-ttu-id="2f6b9-167">2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f6b9-168">Doriți să alocați 75% din costuri unei surse de finanțare și 25% unei alte surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="2f6b9-169">Când oricare dintre aceste surse de finanțare este epuizată, doriți să împărțiți costurile rămase între o a treia sursă de finanțare și o a patra sursă de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-170">Sursă de　finanțare　1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="2f6b9-171">Sursă de　finanțare　2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="2f6b9-172">Sursă de　finanțare　3</span><span class="sxs-lookup"><span data-stu-id="2f6b9-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="2f6b9-173">Sursă de　finanțare　4</span><span class="sxs-lookup"><span data-stu-id="2f6b9-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-174">75%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-174">75%</span></span></li>
<li><span data-ttu-id="2f6b9-175">25%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-175">25%</span></span></li>
<li><span data-ttu-id="2f6b9-176">50%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-176">50%</span></span></li>
<li><span data-ttu-id="2f6b9-177">50%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-178">1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-178">1</span></span></li>
<li><span data-ttu-id="2f6b9-179">1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-179">1</span></span></li>
<li><span data-ttu-id="2f6b9-180">2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-180">2</span></span></li>
<li><span data-ttu-id="2f6b9-181">2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f6b9-182">Doriți să alocați primii 25% din costuri unei surse de finanțare și restul unei a doua surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-183">Sursă de　finanțare　1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="2f6b9-184">Sursă de　finanțare　2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-185">25%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-185">25%</span></span></li>
<li><span data-ttu-id="2f6b9-186">100%</span><span class="sxs-lookup"><span data-stu-id="2f6b9-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2f6b9-187">1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-187">1</span></span></li>
<li><span data-ttu-id="2f6b9-188">2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="2f6b9-189">Exemplu: mai multe surse de finanțare (complexe)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="2f6b9-190">Aveți trei surse de finanțare pe care doriți să le utilizați în următoarea ordine:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="2f6b9-191">Utilizați sursa de finanțare 2 și sursa de finanțare 3 în mod egal până când sursa de finanțare 2 este epuizată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="2f6b9-192">Continuați să utilizați sursa de finanțare 3 până când aceasta este epuizată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="2f6b9-193">Utilizați sursa de finanțare 1 după ce sursa de finanțare 3 este epuizată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="2f6b9-194">Pentru a realiza acest obiectiv, trebuie să faceți următoarele:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="2f6b9-195">Stabiliți limite de finanțare pentru sursa de finanțare 2 și sursa de finanțare 3, pentru sumele respective.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="2f6b9-196">Creați următoarele reguli de finanțare:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="2f6b9-197">Regula 1 (Prioritatea1): Alocați 50% din tranzacții la sursa de finanțare 2 și 50% la sursa de finanțare 3.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="2f6b9-198">Regula 2 (Prioritatea 2): Alocați 100% din tranzacții sursei de finanțare 3.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="2f6b9-199">Regula 3 (Prioritatea 3): Alocați 100% din tranzacții sursei de finanțare 1.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="2f6b9-200">Această configurare funcționează deoarece tranzacțiile sunt verificate în raport cu regulile și limitele pentru a determina dacă oricare dintre acestea se aplică tranzacției.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="2f6b9-201">Dacă nu se aplică reguli sau limite specifice tranzacției, se aplică regula Toate tranzacțiile.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="2f6b9-202">Regula Toate tranzacțiile corespunde tuturor tranzacțiilor.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="2f6b9-203">Dacă se găsește o regulă care se potrivește cu o tranzacție, procentul care a fost alocat în regula respectivă se aplică mai întâi, dar numai după ce meciurile sunt verificate în raport cu orice limite care au fost stabilite.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="2f6b9-204">Dacă a fost atinsă o limită și fondurile unei surse de finanțare sunt epuizate, regula de finanțare care este asociată cu limita de finanțare este ignorată, iar programul verifică următoarea regulă care se aplică.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="2f6b9-205">În unele cazuri, numai o parte a unei tranzacții poate fi alocată conform unei reguli.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="2f6b9-206">Acest lucru se poate întâmpla deoarece o limită este atinsă atunci când tranzacția este alocată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="2f6b9-207">În acest caz, numai o anumită sumă este alocată în conformitate cu regula respectivă, cum ar fi 50 la sută pentru fiecare sursă de finanțare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="2f6b9-208">Acesta este cazul în regula 1, care este descrisă mai devreme în această secțiune.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="2f6b9-209">Restul este alocat în conformitate cu următoarea regulă din secvență.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="2f6b9-210">Tabelul următor examinează acest scenariu în detaliu.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2f6b9-211"><strong>Focus</strong></span><span class="sxs-lookup"><span data-stu-id="2f6b9-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="2f6b9-212"><strong>Detalii</strong></span><span class="sxs-lookup"><span data-stu-id="2f6b9-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f6b9-213">Reguli de finanțare</span><span class="sxs-lookup"><span data-stu-id="2f6b9-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-214">Regula 1 (Prioritatea 1): Toate tranzacțiile.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="2f6b9-215">Alocați sursa de finanțare 2 la 50% și sursa de finanțare 3 la 50%.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="2f6b9-216">Regula 2 (Prioritatea 2): Toate tranzacțiile.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="2f6b9-217">Alocați sursa de finanțare 3 la 100%.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="2f6b9-218">Regula 3 (Prioritatea 2): Toate tranzacțiile.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="2f6b9-219">Alocați sursa de finanțare 1 la 100%.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f6b9-220">Limite de finanțare</span><span class="sxs-lookup"><span data-stu-id="2f6b9-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-221">Sursa de finanțare 1 limită = 10.000</span><span class="sxs-lookup"><span data-stu-id="2f6b9-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="2f6b9-222">Limita sursei 2 de finanțare = 500.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="2f6b9-223">Limita sursei 3 de finanțare = 750.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f6b9-224">Tranzacție 1</span><span class="sxs-lookup"><span data-stu-id="2f6b9-224">Transaction 1</span></span></td>
<td><span data-ttu-id="2f6b9-225"><strong>Suma tranzacției:</strong> 100.00<strong>Finanțare:</strong> Tranzacția este plătită numai conform regulii 1, deoarece tranzacția este plătită integral după aplicarea regulii 1.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="2f6b9-226">Tranzacția este finanțată în mod egal între sursa de finanțare 2 și sursa de finanțare 3.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="2f6b9-227">Sursa de finanțare 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="2f6b9-228">Sursa de finanțare 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2f6b9-229">Tranzacție 2</span><span class="sxs-lookup"><span data-stu-id="2f6b9-229">Transaction 2</span></span></td>
<td><span data-ttu-id="2f6b9-230"><strong>Suma tranzacției:</strong> 5.000.00<strong>Finanțare:</strong> Tranzacția este plătită în conformitate cu toate cele trei reguli.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="2f6b9-231"><strong>Regula 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="2f6b9-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="2f6b9-232">Sursa de finanțare 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="2f6b9-233">Sursa de finanțare 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="2f6b9-234">
<strong>Regula 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="2f6b9-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="2f6b9-235">Sursa de finanțare 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="2f6b9-236">
<strong>Regula 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="2f6b9-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="2f6b9-237">Sursă de finanțare 1: 3.850.00 (= 5.000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2f6b9-238">Totalul fondurilor distribuite pentru fiecare sursă de finanțare</span><span class="sxs-lookup"><span data-stu-id="2f6b9-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="2f6b9-239">Sursa de finanțare 1: 3.850.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="2f6b9-240">Sursa de finanțare 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="2f6b9-241">Sursa de finanțare 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="2f6b9-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="2f6b9-242">Regulile de facturare</span><span class="sxs-lookup"><span data-stu-id="2f6b9-242">Billing rules</span></span>
<span data-ttu-id="2f6b9-243">Când negociați un contract de proiect cu un client, definiți cum și când puteți factura clientul pentru munca la un proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="2f6b9-244">După ce configurați contractul de proiect și proiectul, puteți seta reguli de facturare pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="2f6b9-245">Regulile de facturare se bazează pe termenii proiectului specificați în contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="2f6b9-246">Regulile de facturare pe care le puteți crea depind de termenii contractului de proiect și de tipul de proiect, cum ar fi Timpul și materialul sau Prețul fix, pe care le asociați cu regula de facturare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="2f6b9-247">Puteți crea mai multe reguli de facturare pentru un contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="2f6b9-248">De asemenea, puteți atribui o regulă de facturare mai multor proiecte care sunt asociate cu același contract de proiect și care au condiții de facturare similare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="2f6b9-249">Puteți configura următoarele tipuri de reguli de facturare:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="2f6b9-250">**Unitatea de livrare** - Facturați un client atunci când finalizați o unitate de livrare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="2f6b9-251">Definiți unitățile de livrare în contract.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="2f6b9-252">**Progres** - Facturați un client atunci când finalizați un procent specificat din proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="2f6b9-253">Puteți configura o regulă de facturare pentru a calcula automat procentul de muncă finalizată sau puteți calcula manual procentul de muncă finalizată și suma de facturare a clientului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="2f6b9-254">**Jalon** - Facturați un client pentru suma totală a unui proiect de referință la atingerea acestuia.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="2f6b9-255">**Taxă** - Facturați un client pentru serviciile dvs. plus o taxă de administrare, care este de obicei un procent din costul serviciilor.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="2f6b9-256">**Timp și material** - Facturați un client pentru valoarea timpului și a materialelor utilizate pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="2f6b9-257">Pentru toate tipurile de reguli de facturare, puteți specifica un procent de păstrare care se deduce din facturile clienților până când un proiect ajunge la o etapă convenită.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="2f6b9-258">Procentul de păstrare a plăților este specificat în contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="2f6b9-259">Suma se calculează pe baza și se scade din valoarea totală a liniilor dintr-o factură de client.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="2f6b9-260">Pentru regulile de facturare **Timp și material** și **Progres**, puteți atribui categorii taxabile.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="2f6b9-261">Categoriile taxabile indică tranzacțiile care ar trebui incluse în facturile clienților.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="2f6b9-262">Când sunteți gata să facturați clientul, suma de facturat pentru proiect este calculată pe baza regulilor de facturare și se generează o propunere de facturare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="2f6b9-263">Următoarele secțiuni oferă exemple care arată cum să configurați și să gestionați regulile de facturare pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="2f6b9-264">Exemplu: creați o regulă de facturare care se bazează pe numărul de unități livrate</span><span class="sxs-lookup"><span data-stu-id="2f6b9-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="2f6b9-265">Organizația dvs. încheie un acord pentru a furniza în total cinci sesiuni de instruire angajaților unui client la un cost de 10.000 pe sesiune de instruire.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="2f6b9-266">Facturați clientul după fiecare sesiune de instruire.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="2f6b9-267">Când configurați regulile de facturare pentru contract, utilizați următoarele valori:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="2f6b9-268">Unitatea de livrare este o sesiune de antrenament.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="2f6b9-269">Prețul unitar este de 10.000 pe sesiune de antrenament.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="2f6b9-270">Numărul total de unități este de cinci sesiuni de antrenament.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="2f6b9-271">După ce ați finalizat o sesiune de instruire, puteți crea o factură pentru 10.000, pentru prima unitate care a fost livrată și puteți trimite factura către client.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="2f6b9-272">Exemplu: creați o regulă de facturare care se bazează pe un procent specificat de finalizare a proiectului (calcul manual)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="2f6b9-273">Organizația dvs., o firmă de consultanță software, încheie un acord cu un client pentru a dezvolta o parte a unui produs pe care acesta îl dezvoltă.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="2f6b9-274">Organizația dvs. este de acord să livreze codul software pe o perioadă de șase luni.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="2f6b9-275">Clientul este de acord să plătească organizației dvs. un total de 100.000 pentru lucrări.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="2f6b9-276">Creați o regulă de facturare pentru a factura clientul pe baza procentajului de muncă finalizat pe proiect, așa cum se specifică în contract.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="2f6b9-277">La sfârșitul primei luni, vă întâlniți cu clientul pentru a determina procentul de muncă finalizată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="2f6b9-278">După ce dvs. și clientul examinați proiectul, decideți că proiectul este finalizat cu 15%.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="2f6b9-279">Creați o factură pentru 15.000 (15 la sută din 100.000) și o trimiteți clientului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="2f6b9-280">Exemplu: creați o regulă de facturare care se bazează pe un procent specificat de finalizare a proiectului (calcul automat)</span><span class="sxs-lookup"><span data-stu-id="2f6b9-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="2f6b9-281">Organizația dvs., o firmă de dezvoltare software, este de acord să dezvolte un pachet de contabilitate a salariilor pentru un client pentru 30.000.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="2f6b9-282">Clientul este de acord să plătească organizației dvs. pe baza procentului de lucru finalizat.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="2f6b9-283">Estimați că costurile proiectului sunt de 20.000.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="2f6b9-284">Contractul de proiect specifică categoriile de lucrări pe care le utilizați în procesul de facturare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="2f6b9-285">Configurați reguli de facturare care calculează automat sumele facturii pentru procentul de muncă finalizat pentru fiecare categorie.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="2f6b9-286">Configurați un buget pentru fiecare categorie:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="2f6b9-287">**Dezvoltare** - Cost de 15.000 și venituri de 20.000</span><span class="sxs-lookup"><span data-stu-id="2f6b9-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="2f6b9-288">**Instalare** - Cost de 5.000 și venituri de 10.000</span><span class="sxs-lookup"><span data-stu-id="2f6b9-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="2f6b9-289">Când creați o factură pentru client pentru prima dată, suma facturii este calculată automat pe baza următoarelor informații:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="2f6b9-290">După o lună, lucrătorul din proiect transmite o foaie de timp pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="2f6b9-291">Costul orelor lucrătorului este de 5.000 pentru dezvoltare și 1.000 pentru instalare.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="2f6b9-292">Lucrările de dezvoltare sunt finalizate cu 33% (5.000 de costuri reale/15.000 de costuri bugetare), iar lucrările de instalare sunt finalizate cu 20% (1.000 de costuri reale/5.000 de costuri bugetare).</span><span class="sxs-lookup"><span data-stu-id="2f6b9-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="2f6b9-293">Suma facturii de 8.667 este calculată automat (33% din 20.000 + 20% din 10.000).</span><span class="sxs-lookup"><span data-stu-id="2f6b9-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="2f6b9-294">Creați o factură pentru 8.667 și o trimiteți clientului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="2f6b9-295">Exemplu: creați o regulă de facturare bazată pe repere convenite</span><span class="sxs-lookup"><span data-stu-id="2f6b9-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="2f6b9-296">Organizația dvs., o firmă de consultanță în management, este de acord să efectueze cercetări de piață pentru un produs de consum pe care clientul intenționează să îl vândă.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="2f6b9-297">Clientul este de acord să utilizeze serviciile dvs. pentru o perioadă de trei luni, începând cu luna martie, și este de acord să plătească organizației dvs. 50.000.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="2f6b9-298">Proiectul are trei jaloane:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-298">The project has three milestones:</span></span>

-   <span data-ttu-id="2f6b9-299">Etapa 1: Colectați date despre consumatori - 31 martie</span><span class="sxs-lookup"><span data-stu-id="2f6b9-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="2f6b9-300">Etapa 2: Analizați datele consumatorilor - 30 aprilie</span><span class="sxs-lookup"><span data-stu-id="2f6b9-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="2f6b9-301">Etapa 3: Prezentați o propunere de viabilitate a produsului - 31 mai</span><span class="sxs-lookup"><span data-stu-id="2f6b9-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="2f6b9-302">Clientul este de acord să plătească organizației dvs. 10.000 pentru primul jalon, 20.000 pentru al doilea jalon și 20.000 pentru al treilea jalon.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="2f6b9-303">Când configurați contractul de proiect, sunteți de acord să facturați clientul pe baza etapei care a fost finalizată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="2f6b9-304">Configurarea regulii de facturare include următorii pași:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="2f6b9-305">Definiți etapele proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-305">Define the project milestones.</span></span>
-   <span data-ttu-id="2f6b9-306">Definiți suma de facturat clientului la finalizarea fiecărei etape.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="2f6b9-307">Când prima etapă este finalizată la 31 martie, marcați etapa ca fiind finalizată, apoi creați o factură pentru 10.000 și o trimiteți clientului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="2f6b9-308">Nu puteți crea o factură pentru o etapă de referință până când nu ați marcat această etapă ca fiind finalizată.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="2f6b9-309">Exemplu: creați o regulă de facturare care se bazează pe servicii plus o taxă de administrare</span><span class="sxs-lookup"><span data-stu-id="2f6b9-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="2f6b9-310">Organizația dvs., o firmă de consultanță în management, este de acord să efectueze studii de piață pentru a evalua viabilitatea unui produs pe care clientul, o companie de retail, îl dezvoltă.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="2f6b9-311">Termenii acordului specifică faptul că veți furniza serviciile primilor dvs. trei consultanți în management, care vor efectua cercetările în funcție de timp și materiale.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="2f6b9-312">Clientul este de acord să plătească 100 pe oră, plus o taxă de administrare de 10% pentru orele de consultanță care sunt taxate pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="2f6b9-313">Când configurați contractul de proiect, creați o regulă de facturare pentru a adăuga o taxă de administrare de 10% la orele de consultanță care sunt taxate proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="2f6b9-314">Atunci când creați o factură pentru client, clientul primește o taxă de administrare de 10% plus costul orelor de consultanță.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="2f6b9-315">De exemplu, dacă cei trei consultanți au lucrat în total 200 de ore la proiect, se creează o factură pentru 22.000 pe baza următorului calcul:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="2f6b9-316">200 de ore la 100 pe oră = 20.000</span><span class="sxs-lookup"><span data-stu-id="2f6b9-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="2f6b9-317">10% comision de administrare = 2.000</span><span class="sxs-lookup"><span data-stu-id="2f6b9-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="2f6b9-318">Suma totală a facturii = 22.000</span><span class="sxs-lookup"><span data-stu-id="2f6b9-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="2f6b9-319">Dacă taxele sunt impozabile pentru un client și selectați un grup de taxe pe vânzări în contractul de proiect, grupul de taxe pe vânzări este introdus automat într-o regulă de facturare pentru taxe.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="2f6b9-320">Exemplu: creați o regulă de facturare pentru valoarea timpului și a materialelor</span><span class="sxs-lookup"><span data-stu-id="2f6b9-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="2f6b9-321">Organizația dvs., o firmă de consultanță software, este de acord să ofere cinci consultanți tehnici pentru a lucra la un proiect de dezvoltare software pentru un client pentru următoarele șase luni.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="2f6b9-322">Clientul este de acord să plătească 150 pentru fiecare oră de consultanță, plus costul materialelor de birou.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="2f6b9-323">Organizația dvs. trimite o factură către client la sfârșitul fiecărei luni.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="2f6b9-324">Când stabiliți contractul de proiect, sunteți de acord să facturați lunar clientului timpul și materialele aferente proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="2f6b9-325">Creați o regulă de facturare care include următoarele informații:</span><span class="sxs-lookup"><span data-stu-id="2f6b9-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="2f6b9-326">Perioada contractului este de șase luni.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-326">The contract period is six months.</span></span>
-   <span data-ttu-id="2f6b9-327">Timpul de consultare este calculat la o rată de 150 pe oră.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="2f6b9-328">Materialele de birou sunt facturate la cost, iar costul total al proiectului nu trebuie să depășească 10.000.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="2f6b9-329">Creați o factură pentru client la sfârșitul fiecărei luni calendaristice în timpul proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="2f6b9-330">În prima lună, în total 800 de ore sunt înregistrate de consultanți în cadrul proiectului.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="2f6b9-331">Costul materialelor de birou care sunt taxate pentru proiect este de 2.000.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="2f6b9-332">Prin urmare, la sfârșitul lunii, creați o factură pentru 122.000, care este calculată ca 800 de ore la 150 pe oră, plus 2.000 pentru rechizite de birou.</span><span class="sxs-lookup"><span data-stu-id="2f6b9-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]