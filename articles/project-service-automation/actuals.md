---
title: Reale
description: Acest subiect oferă informații despre valorile reale ale proiectului.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754808"
---
# <a name="actuals"></a><span data-ttu-id="1180a-103">Reale</span><span class="sxs-lookup"><span data-stu-id="1180a-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1180a-104">Valorile reale reprezintă volumul de lucru care a fost finalizat pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="1180a-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="1180a-105">Valorile reale ale proiectului pot fi urmărite înapoi la documentele lor sursă.</span><span class="sxs-lookup"><span data-stu-id="1180a-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="1180a-106">Aceste documente sursă includ intrările de timp, intrările cu cheltuieli și intrările în jurnal și, de asemenea, facturile.</span><span class="sxs-lookup"><span data-stu-id="1180a-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cum sunt urmărite valorile reale ale proiectului la documentele sursă](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="1180a-108">Remiterea unei intrări de timp</span><span class="sxs-lookup"><span data-stu-id="1180a-108">Submitting a time entry</span></span>

<span data-ttu-id="1180a-109">În PSA, atunci când o intrare de timp este remisă pentru un proiect care este mapat la o linie de contract pentru timp și materiale, se creează două linii de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1180a-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="1180a-110">O linie este pentru cost, iar cealaltă linie este pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="1180a-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="1180a-111">Atunci când o intrare de timp este remisă pentru un proiect care este mapat la o linie de contract cu preț fix, se creează o linie de jurnal doar pentru cost.</span><span class="sxs-lookup"><span data-stu-id="1180a-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="1180a-112">Logica pentru introducerea prețurilor implicite se află în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1180a-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="1180a-113">Toate valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1180a-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="1180a-114">Aceste câmpuri includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="1180a-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="1180a-115">Câmpurile care afectează prețurile implicite, cum ar fi **Rol** și **Unitate organizațională**, determină introducerea implicită a unui preț corespunzător în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1180a-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="1180a-116">Dacă adăugați un câmp particularizat în intrarea de timp și doriți ca valoarea câmpului să fie propagată în valorile reale, creați câmpul în entitatea Valori reale și utilizați mapări de câmp pentru a copia câmpul din intrarea de timp în valoarea reală.</span><span class="sxs-lookup"><span data-stu-id="1180a-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="1180a-117">Remiterea unei intrări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="1180a-117">Submitting an expense entry</span></span>

<span data-ttu-id="1180a-118">În PSA, atunci când o intrare de cheltuieli este remisă pentru un proiect care este mapat la o linie de contract pentru timp și materiale, se creează două linii de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1180a-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="1180a-119">O linie este pentru cost, iar cealaltă linie este pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="1180a-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="1180a-120">Atunci când o intrare de cheltuieli este remisă pentru un proiect care este mapat la o linie de contract cu preț fix, se creează o linie de jurnal doar pentru cost.</span><span class="sxs-lookup"><span data-stu-id="1180a-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="1180a-121">Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli care este selectată în pagina **Intrare cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="1180a-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="1180a-122">Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="1180a-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1180a-123">Cu toate acestea, pentru prețul în sine, suma pe care utilizatorul a introdus-o este setată direct pe liniile de jurnal de cheltuieli corelate pentru cost și vânzări în mod implicit.</span><span class="sxs-lookup"><span data-stu-id="1180a-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="1180a-124">În versiunea curentă de PSA, introducerea pe categorii a unor prețuri implicite per unitate pe intrările de cheltuieli nu este disponibilă.</span><span class="sxs-lookup"><span data-stu-id="1180a-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="1180a-125">Utilizarea jurnalelor pentru înregistrarea costurilor</span><span class="sxs-lookup"><span data-stu-id="1180a-125">Using journals to record costs</span></span>

<span data-ttu-id="1180a-126">În PSA, jurnalele vă permit să înregistrați costuri sau venituri în clasele de tranzacții Materiale, Tarife, Timp, Cheltuieli sau Taxe.</span><span class="sxs-lookup"><span data-stu-id="1180a-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="1180a-127">Un jurnal are un antet, linii și o acțiune **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="1180a-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="1180a-128">Iată câteva scenarii în care este posibil să utilizați un jurnal:</span><span class="sxs-lookup"><span data-stu-id="1180a-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="1180a-129">Trebuie să înregistrați costurile reale ale materialelor și vânzările pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="1180a-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="1180a-130">Trebuie să mutați valori reale privind tranzacțiile dintr-un alt sistem în PSA.</span><span class="sxs-lookup"><span data-stu-id="1180a-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="1180a-131">Trebuie să înregistrați costuri care au avut loc în alt sistem, cum ar fi costurile de achiziție sau subcontractare.</span><span class="sxs-lookup"><span data-stu-id="1180a-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="1180a-132">Înregistrarea valorilor reale pe baza evenimentelor proiectului</span><span class="sxs-lookup"><span data-stu-id="1180a-132">Recording actuals based on project events</span></span>

<span data-ttu-id="1180a-133">PSA înregistrează tranzacțiile financiare care apar în timpul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="1180a-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="1180a-134">Aceste tranzacții sunt înregistrate ca **valori reale**.</span><span class="sxs-lookup"><span data-stu-id="1180a-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="1180a-135">Tabelele următoare arată diferitele tipuri de valori reale care sunt create, în funcție de faptul dacă proiectul este un proiect pe bază de timp și materiale sau un proiect cu preț fix, este în etapa de prevânzare sau este un proiect intern.</span><span class="sxs-lookup"><span data-stu-id="1180a-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="1180a-136">**Resursa aparține aceleiași unități organizatorice ca și unitatea contractantă a proiectului**</span><span class="sxs-lookup"><span data-stu-id="1180a-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1180a-137">Eveniment</span><span class="sxs-lookup"><span data-stu-id="1180a-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1180a-138">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="1180a-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1180a-139">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="1180a-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1180a-140">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="1180a-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1180a-141">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="1180a-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1180a-142">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1180a-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1180a-143">Reale</span><span class="sxs-lookup"><span data-stu-id="1180a-143">Actuals</span></span></th>
<th><span data-ttu-id="1180a-144">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1180a-144">Transaction currency</span></span></th>
<th><span data-ttu-id="1180a-145">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1180a-145">Fixed price</span></span></th>
<th><span data-ttu-id="1180a-146">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1180a-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1180a-147">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1180a-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1180a-148">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1180a-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-149">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1180a-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1180a-150">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1180a-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1180a-151">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1180a-152">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-152">Cost actual</span></span></td>
<td><span data-ttu-id="1180a-153">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-154">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-155">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="1180a-156">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-157">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-158">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="1180a-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1180a-159">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1180a-160">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1180a-161">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-161">Cost actual</span></span></td>
<td><span data-ttu-id="1180a-162">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-163">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-164">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-165">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-166">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-167">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1180a-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1180a-168">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-169">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1180a-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1180a-170">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1180a-171">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1180a-172">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1180a-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1180a-173">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-174">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1180a-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-175">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-176">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-177">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-178">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1180a-178">Billed sales</span></span></td>
<td><span data-ttu-id="1180a-179">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1180a-180">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1180a-181">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1180a-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1180a-182">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-183">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-184">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-185">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-186">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-187">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1180a-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1180a-188">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-189">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1180a-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1180a-190">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1180a-191">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1180a-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1180a-192">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1180a-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1180a-193">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1180a-194">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1180a-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1180a-195">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="1180a-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1180a-196">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-197">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-198">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-199">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1180a-199">Billed sales</span></span></td>
<td><span data-ttu-id="1180a-200">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1180a-201">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1180a-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1180a-202">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1180a-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1180a-203">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-204">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1180a-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1180a-205">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-206">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1180a-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1180a-207">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1180a-208">**Resursa aparține unei unități organizatorice care diferă de unitatea contractantă a proiectului**</span><span class="sxs-lookup"><span data-stu-id="1180a-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1180a-209">Eveniment</span><span class="sxs-lookup"><span data-stu-id="1180a-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1180a-210">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="1180a-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1180a-211">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="1180a-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1180a-212">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="1180a-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1180a-213">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="1180a-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1180a-214">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1180a-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1180a-215">Reale</span><span class="sxs-lookup"><span data-stu-id="1180a-215">Actuals</span></span></th>
<th><span data-ttu-id="1180a-216">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1180a-216">Transaction currency</span></span></th>
<th><span data-ttu-id="1180a-217">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1180a-217">Fixed price</span></span></th>
<th><span data-ttu-id="1180a-218">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1180a-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1180a-219">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1180a-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1180a-220">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1180a-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-221">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1180a-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1180a-222">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1180a-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1180a-223">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1180a-224">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-224">Cost actual</span></span></td>
<td><span data-ttu-id="1180a-225">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1180a-226">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1180a-227">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1180a-228">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1180a-229">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-230">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="1180a-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1180a-231">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-232">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1180a-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1180a-233">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1180a-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-234">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="1180a-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1180a-235">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1180a-236">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1180a-237">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-237">Cost actual</span></span></td>
<td><span data-ttu-id="1180a-238">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-239">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-240">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-241">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-242">Cost real</span><span class="sxs-lookup"><span data-stu-id="1180a-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-243">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1180a-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1180a-244">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1180a-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-245">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="1180a-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1180a-246">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1180a-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-247">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1180a-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1180a-248">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-249">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1180a-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1180a-250">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1180a-251">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1180a-252">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1180a-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1180a-253">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-254">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1180a-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-255">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-256">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1180a-257">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-258">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1180a-258">Billed sales</span></span></td>
<td><span data-ttu-id="1180a-259">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1180a-260">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1180a-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1180a-261">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1180a-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1180a-262">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-263">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-264">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-265">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1180a-266">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-267">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1180a-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1180a-268">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-269">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1180a-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1180a-270">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1180a-271">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1180a-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1180a-272">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1180a-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1180a-273">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1180a-274">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1180a-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1180a-275">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="1180a-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1180a-276">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-277">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1180a-278">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1180a-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-279">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1180a-279">Billed sales</span></span></td>
<td><span data-ttu-id="1180a-280">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1180a-281">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1180a-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1180a-282">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1180a-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1180a-283">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-284">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1180a-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1180a-285">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1180a-286">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1180a-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1180a-287">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1180a-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
