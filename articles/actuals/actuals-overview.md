---
title: Date reale
description: Acest subiect oferă informații despre cum să lucrați cu date reale în Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126330"
---
# <a name="actuals"></a><span data-ttu-id="7aceb-103">Date reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-103">Actuals</span></span> 

<span data-ttu-id="7aceb-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="7aceb-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7aceb-105">Valorile reale reprezintă volumul de lucru care a fost finalizat pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="7aceb-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="7aceb-106">Acestea sunt create ca urmare a intrărilor de timp și a cheltuielilor, a înregistrărilor din jurnal și a facturilor.</span><span class="sxs-lookup"><span data-stu-id="7aceb-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="7aceb-107">Liniile de jurnal și remiteri de timp</span><span class="sxs-lookup"><span data-stu-id="7aceb-107">Journal lines and time submission</span></span>

<span data-ttu-id="7aceb-108">Pentru mai multe informații despre remiteri de timp, consultați [Prezentare generală a intrării de timp](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7aceb-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="7aceb-109">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="7aceb-109">Time and materials</span></span>

<span data-ttu-id="7aceb-110">Atunci când o intrare de timp care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="7aceb-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="7aceb-111">Preț fix</span><span class="sxs-lookup"><span data-stu-id="7aceb-111">Fixed price</span></span>

<span data-ttu-id="7aceb-112">Atunci când o intrare de timp care este remisă este legată de un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.</span><span class="sxs-lookup"><span data-stu-id="7aceb-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="7aceb-113">Tarifare implicită</span><span class="sxs-lookup"><span data-stu-id="7aceb-113">Default pricing</span></span>

<span data-ttu-id="7aceb-114">Logica pentru crearea prețurilor implicite se află pe linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="7aceb-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="7aceb-115">Valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="7aceb-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="7aceb-116">Aceste valori includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="7aceb-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="7aceb-117">Câmpurile care afectează tarifarea implicită, cum ar fi **Rol** și **Unitate organizațională**, sunt utilizate pentru a determina prețul corespunzător pe linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="7aceb-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="7aceb-118">Puteți adăuga un câmp personalizat la intrarea în timp.</span><span class="sxs-lookup"><span data-stu-id="7aceb-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="7aceb-119">Dacă doriți ca valoarea câmpului să fie propagată în valorile reale, creați câmpul în entitatea Valori reale și utilizați mapări de câmp pentru a copia câmpul din intrarea de timp în valoarea reală.</span><span class="sxs-lookup"><span data-stu-id="7aceb-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="7aceb-120">Liniile de jurnal și remiterea cheltuielilor de bază</span><span class="sxs-lookup"><span data-stu-id="7aceb-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="7aceb-121">Pentru mai multe informații despre intrări de cheltuială [Prezentare generală a cheltuielii](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7aceb-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="7aceb-122">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="7aceb-122">Time and materials</span></span>

<span data-ttu-id="7aceb-123">Atunci când o intrare de cheltuială de bază care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="7aceb-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="7aceb-124">Preț fix</span><span class="sxs-lookup"><span data-stu-id="7aceb-124">Fixed price</span></span>

<span data-ttu-id="7aceb-125">Atunci când o intrare de cheltuială de bază care este remisă este legată de un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.</span><span class="sxs-lookup"><span data-stu-id="7aceb-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="7aceb-126">Tarifare implicită</span><span class="sxs-lookup"><span data-stu-id="7aceb-126">Default pricing</span></span>

<span data-ttu-id="7aceb-127">Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="7aceb-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="7aceb-128">Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="7aceb-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="7aceb-129">Cu toate acestea, în mod implicit, suma care este introdusă pentru prețul în sine este setată direct pe liniile de jurnal de cheltuieli corelate pentru cost și vânzări.</span><span class="sxs-lookup"><span data-stu-id="7aceb-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="7aceb-130">Intrarea pe categorii a unor prețuri implicite per unitate pe intrările de cheltuieli nu este disponibilă.</span><span class="sxs-lookup"><span data-stu-id="7aceb-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="7aceb-131">Utilizați intrările de jurnal pentru a înregistra costurilr</span><span class="sxs-lookup"><span data-stu-id="7aceb-131">Use entry journals to record costs</span></span>

<span data-ttu-id="7aceb-132">Puteți utiliza intrările de jurnal pentru a înregistra costul sau venitul în material, tarif, timp, cheltuieli sau clase de taxe de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="7aceb-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="7aceb-133">Jurnalele pot fi utilizate în următoarele scopuri:</span><span class="sxs-lookup"><span data-stu-id="7aceb-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="7aceb-134">Înregistrați costul real al materialelor și vânzărilor pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="7aceb-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="7aceb-135">Mutați valorile reale ale tranzacțiile din alt sistem la Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7aceb-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="7aceb-136">Înregistrați costurile care au avut loc într-un alt sistem.</span><span class="sxs-lookup"><span data-stu-id="7aceb-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="7aceb-137">Aceste costuri pot include costuri de achiziție sau subcontractare.</span><span class="sxs-lookup"><span data-stu-id="7aceb-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7aceb-138">Aplicația nu validează tipul liniei jurnalului sau prețurile aferente care sunt introduse pe linia jurnalului.</span><span class="sxs-lookup"><span data-stu-id="7aceb-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="7aceb-139">Prin urmare, numai un utilizator care este pe deplin conștient de impactul contabil pe care îl au efectele reale asupra proiectului ar trebui să utilizeze jurnale de intrare pentru a crea date reale.</span><span class="sxs-lookup"><span data-stu-id="7aceb-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="7aceb-140">Datorită impactului acestui tip de jurnal, ar trebui să alegeți cu atenție cine are acces pentru a crea jurnale de intrare.</span><span class="sxs-lookup"><span data-stu-id="7aceb-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="7aceb-141">Înregistrați valorile reale pe baza evenimentelor proiectului</span><span class="sxs-lookup"><span data-stu-id="7aceb-141">Record actuals based on project events</span></span>

<span data-ttu-id="7aceb-142">Project Operations înregistrează tranzacțiile financiare care apar în timpul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="7aceb-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="7aceb-143">Aceste tranzacții sunt înregistrate ca valori reale.</span><span class="sxs-lookup"><span data-stu-id="7aceb-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="7aceb-144">Tabelele următoare arată diferitele tipuri de valori reale care sunt create, în funcție de faptul dacă proiectul este un proiect pe bază de timp și materiale sau un proiect cu preț fix, este în etapa de prevânzare sau este un proiect intern.</span><span class="sxs-lookup"><span data-stu-id="7aceb-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="7aceb-145">Resursa aparține aceleiași unități organizatorice ca și unitatea contractantă a proiectului</span><span class="sxs-lookup"><span data-stu-id="7aceb-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="7aceb-146">Eveniment</span><span class="sxs-lookup"><span data-stu-id="7aceb-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="7aceb-147">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="7aceb-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="7aceb-148">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="7aceb-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="7aceb-149">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="7aceb-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="7aceb-150">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="7aceb-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="7aceb-151">Preț fix</span><span class="sxs-lookup"><span data-stu-id="7aceb-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7aceb-152">Reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-152">Actuals</span></span></th>
<th><span data-ttu-id="7aceb-153">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="7aceb-153">Transaction currency</span></span></th>
<th><span data-ttu-id="7aceb-154">Preț fix</span><span class="sxs-lookup"><span data-stu-id="7aceb-154">Fixed price</span></span></th>
<th><span data-ttu-id="7aceb-155">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="7aceb-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7aceb-156">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="7aceb-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="7aceb-157">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-158">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="7aceb-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="7aceb-159">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7aceb-160">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7aceb-161">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-161">Cost actual</span></span></td>
<td><span data-ttu-id="7aceb-162">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-163">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-164">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="7aceb-165">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-166">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-167">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="7aceb-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="7aceb-168">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7aceb-169">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7aceb-170">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-170">Cost actual</span></span></td>
<td><span data-ttu-id="7aceb-171">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-172">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-173">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-174">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-175">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-176">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="7aceb-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7aceb-177">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-178">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="7aceb-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7aceb-179">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7aceb-180">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7aceb-181">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7aceb-182">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-183">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="7aceb-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-184">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-185">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-186">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-187">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-187">Billed sales</span></span></td>
<td><span data-ttu-id="7aceb-188">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7aceb-189">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7aceb-190">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7aceb-191">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-192">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-193">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-194">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-195">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-196">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="7aceb-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7aceb-197">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-198">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="7aceb-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7aceb-199">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7aceb-200">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="7aceb-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7aceb-201">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="7aceb-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7aceb-202">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="7aceb-203">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="7aceb-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="7aceb-204">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="7aceb-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="7aceb-205">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-206">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-207">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-208">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-208">Billed sales</span></span></td>
<td><span data-ttu-id="7aceb-209">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7aceb-210">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="7aceb-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7aceb-211">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="7aceb-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7aceb-212">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-213">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="7aceb-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="7aceb-214">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-215">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="7aceb-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="7aceb-216">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="7aceb-217">Resursa aparține unei unități organizatorice care diferă de unitatea contractantă a proiectului</span><span class="sxs-lookup"><span data-stu-id="7aceb-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="7aceb-218">Eveniment</span><span class="sxs-lookup"><span data-stu-id="7aceb-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="7aceb-219">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="7aceb-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="7aceb-220">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="7aceb-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="7aceb-221">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="7aceb-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="7aceb-222">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="7aceb-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="7aceb-223">Preț fix</span><span class="sxs-lookup"><span data-stu-id="7aceb-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7aceb-224">Reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-224">Actuals</span></span></th>
<th><span data-ttu-id="7aceb-225">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="7aceb-225">Transaction currency</span></span></th>
<th><span data-ttu-id="7aceb-226">Preț fix</span><span class="sxs-lookup"><span data-stu-id="7aceb-226">Fixed price</span></span></th>
<th><span data-ttu-id="7aceb-227">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="7aceb-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7aceb-228">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="7aceb-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="7aceb-229">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-230">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="7aceb-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="7aceb-231">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="7aceb-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="7aceb-232">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7aceb-233">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-233">Cost actual</span></span></td>
<td><span data-ttu-id="7aceb-234">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="7aceb-235">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="7aceb-236">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="7aceb-237">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="7aceb-238">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-239">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="7aceb-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="7aceb-240">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-241">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="7aceb-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="7aceb-242">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="7aceb-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-243">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="7aceb-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="7aceb-244">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="7aceb-245">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="7aceb-246">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-246">Cost actual</span></span></td>
<td><span data-ttu-id="7aceb-247">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-248">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-249">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-250">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-251">Cost real</span><span class="sxs-lookup"><span data-stu-id="7aceb-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-252">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="7aceb-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="7aceb-253">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="7aceb-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-254">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="7aceb-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="7aceb-255">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="7aceb-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-256">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="7aceb-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7aceb-257">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-258">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="7aceb-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7aceb-259">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7aceb-260">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7aceb-261">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7aceb-262">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-263">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="7aceb-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-264">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-265">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="7aceb-266">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-267">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-267">Billed sales</span></span></td>
<td><span data-ttu-id="7aceb-268">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7aceb-269">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="7aceb-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="7aceb-270">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="7aceb-271">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-272">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-273">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-274">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="7aceb-275">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-276">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="7aceb-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="7aceb-277">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-278">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="7aceb-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="7aceb-279">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="7aceb-280">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="7aceb-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7aceb-281">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="7aceb-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7aceb-282">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="7aceb-283">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="7aceb-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="7aceb-284">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="7aceb-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="7aceb-285">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-286">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="7aceb-287">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="7aceb-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-288">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="7aceb-288">Billed sales</span></span></td>
<td><span data-ttu-id="7aceb-289">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="7aceb-290">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="7aceb-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="7aceb-291">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="7aceb-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="7aceb-292">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-293">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="7aceb-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="7aceb-294">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7aceb-295">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="7aceb-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="7aceb-296">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="7aceb-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
