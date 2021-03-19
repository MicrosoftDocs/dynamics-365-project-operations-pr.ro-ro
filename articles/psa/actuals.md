---
title: Prezentare date reale
description: Acest subiect oferă informații despre valorile reale ale proiectului.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285633"
---
# <a name="actuals-overview"></a><span data-ttu-id="1ee2e-103">Prezentare date reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1ee2e-104">Valorile reale reprezintă volumul de lucru care a fost finalizat pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="1ee2e-105">Valorile reale ale proiectului pot fi urmărite înapoi la documentele lor sursă.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="1ee2e-106">Aceste documente sursă includ intrările de timp, intrările cu cheltuieli și intrările în jurnal și, de asemenea, facturile.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cum sunt urmărite valorile reale ale proiectului la documentele sursă](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="1ee2e-108">Remiterea unei intrări de timp</span><span class="sxs-lookup"><span data-stu-id="1ee2e-108">Submitting a time entry</span></span>

<span data-ttu-id="1ee2e-109">În PSA, atunci când o intrare de timp este remisă pentru un proiect care este mapat la o linie de contract pentru timp și materiale, se creează două linii de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="1ee2e-110">O linie este pentru cost, iar cealaltă linie este pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="1ee2e-111">Atunci când o intrare de timp este remisă pentru un proiect care este mapat la o linie de contract cu preț fix, se creează o linie de jurnal doar pentru cost.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="1ee2e-112">Logica pentru introducerea prețurilor implicite se află în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="1ee2e-113">Toate valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="1ee2e-114">Aceste câmpuri includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="1ee2e-115">Câmpurile care afectează prețurile implicite, cum ar fi **Rol** și **Unitate organizațională**, determină introducerea implicită a unui preț corespunzător în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="1ee2e-116">Dacă adăugați un câmp particularizat în intrarea de timp și doriți ca valoarea câmpului să fie propagată în valorile reale, creați câmpul în entitatea Valori reale și utilizați mapări de câmp pentru a copia câmpul din intrarea de timp în valoarea reală.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="1ee2e-117">Remiterea unei intrări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="1ee2e-117">Submitting an expense entry</span></span>

<span data-ttu-id="1ee2e-118">În PSA, atunci când o intrare de cheltuieli este remisă pentru un proiect care este mapat la o linie de contract pentru timp și materiale, se creează două linii de jurnal.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="1ee2e-119">O linie este pentru cost, iar cealaltă linie este pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="1ee2e-120">Atunci când o intrare de cheltuieli este remisă pentru un proiect care este mapat la o linie de contract cu preț fix, se creează o linie de jurnal doar pentru cost.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="1ee2e-121">Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli care este selectată în pagina **Intrare cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="1ee2e-122">Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="1ee2e-123">Cu toate acestea, pentru prețul în sine, suma pe care utilizatorul a introdus-o este setată direct pe liniile de jurnal de cheltuieli corelate pentru cost și vânzări în mod implicit.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="1ee2e-124">În versiunea curentă de PSA, introducerea pe categorii a unor prețuri implicite per unitate pe intrările de cheltuieli nu este disponibilă.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="1ee2e-125">Utilizarea jurnalelor de intrări pentru înregistrarea costurilor</span><span class="sxs-lookup"><span data-stu-id="1ee2e-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="1ee2e-126">În PSA, jurnalele de intare vă permit să înregistrați costul sau venitul în clasele de tranzacții Materiale, Tarife, Timp, Cheltuieli sau Taxe.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="1ee2e-127">Un jurnal are un antet, linii și o acțiune **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="1ee2e-128">Iată câteva scenarii în care este posibil să utilizați un jurnal:</span><span class="sxs-lookup"><span data-stu-id="1ee2e-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="1ee2e-129">Trebuie să înregistrați costurile reale ale materialelor și vânzările pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="1ee2e-130">Trebuie să mutați valori reale privind tranzacțiile dintr-un alt sistem în PSA.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="1ee2e-131">Trebuie să înregistrați costuri care au avut loc în alt sistem, cum ar fi costurile de achiziție sau subcontractare.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ee2e-132">Utilizarea jurnalelor de intrare pentru a crea actualități ar trebui să fie făcută doar de către un utilizator care este pe deplin conștient de impactul contabil pe care efectivele îl au asupra proiectului.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="1ee2e-133">Acest lucru se datorează faptului că aplicația nu validează tipul liniei de jurnal sau prețurile aferente care sunt introduse pe linia jurnalului.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="1ee2e-134">Din cauza impactului acestui tip de jurnal, trebuie să aveți precauție adecvată pentru cine are acces la crearea jurnalelor de intrare.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="1ee2e-135">Înregistrarea valorilor reale pe baza evenimentelor proiectului</span><span class="sxs-lookup"><span data-stu-id="1ee2e-135">Recording actuals based on project events</span></span>

<span data-ttu-id="1ee2e-136">PSA înregistrează tranzacțiile financiare care apar în timpul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="1ee2e-137">Aceste tranzacții sunt înregistrate ca **valori reale**.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="1ee2e-138">Tabelele următoare arată diferitele tipuri de valori reale care sunt create, în funcție de faptul dacă proiectul este un proiect pe bază de timp și materiale sau un proiect cu preț fix, este în etapa de prevânzare sau este un proiect intern.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="1ee2e-139">**Resursa aparține aceleiași unități organizatorice ca și unitatea contractantă a proiectului**</span><span class="sxs-lookup"><span data-stu-id="1ee2e-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1ee2e-140">Eveniment</span><span class="sxs-lookup"><span data-stu-id="1ee2e-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1ee2e-141">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="1ee2e-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1ee2e-142">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1ee2e-143">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="1ee2e-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1ee2e-144">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1ee2e-145">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1ee2e-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1ee2e-146">Reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-146">Actuals</span></span></th>
<th><span data-ttu-id="1ee2e-147">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-147">Transaction currency</span></span></th>
<th><span data-ttu-id="1ee2e-148">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1ee2e-148">Fixed price</span></span></th>
<th><span data-ttu-id="1ee2e-149">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ee2e-150">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1ee2e-151">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-152">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1ee2e-153">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ee2e-154">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ee2e-155">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-155">Cost actual</span></span></td>
<td><span data-ttu-id="1ee2e-156">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-157">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-158">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="1ee2e-159">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-160">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-161">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="1ee2e-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1ee2e-162">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ee2e-163">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ee2e-164">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-164">Cost actual</span></span></td>
<td><span data-ttu-id="1ee2e-165">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-166">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-167">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-168">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-169">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-170">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ee2e-171">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-172">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1ee2e-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ee2e-173">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ee2e-174">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ee2e-175">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ee2e-176">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-177">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1ee2e-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-178">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-179">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-180">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-181">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-181">Billed sales</span></span></td>
<td><span data-ttu-id="1ee2e-182">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ee2e-183">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ee2e-184">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ee2e-185">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-186">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-187">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-188">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-189">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-190">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ee2e-191">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-192">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1ee2e-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ee2e-193">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ee2e-194">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ee2e-195">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ee2e-196">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1ee2e-197">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1ee2e-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1ee2e-198">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="1ee2e-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1ee2e-199">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-200">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-201">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-202">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-202">Billed sales</span></span></td>
<td><span data-ttu-id="1ee2e-203">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ee2e-204">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ee2e-205">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ee2e-206">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-207">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1ee2e-208">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-209">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1ee2e-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ee2e-210">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1ee2e-211">**Resursa aparține unei unități organizatorice care diferă de unitatea contractantă a proiectului**</span><span class="sxs-lookup"><span data-stu-id="1ee2e-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="1ee2e-212">Eveniment</span><span class="sxs-lookup"><span data-stu-id="1ee2e-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="1ee2e-213">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="1ee2e-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="1ee2e-214">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="1ee2e-215">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="1ee2e-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="1ee2e-216">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="1ee2e-217">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1ee2e-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1ee2e-218">Reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-218">Actuals</span></span></th>
<th><span data-ttu-id="1ee2e-219">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-219">Transaction currency</span></span></th>
<th><span data-ttu-id="1ee2e-220">Preț fix</span><span class="sxs-lookup"><span data-stu-id="1ee2e-220">Fixed price</span></span></th>
<th><span data-ttu-id="1ee2e-221">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ee2e-222">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="1ee2e-223">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-224">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="1ee2e-225">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1ee2e-226">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ee2e-227">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-227">Cost actual</span></span></td>
<td><span data-ttu-id="1ee2e-228">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1ee2e-229">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1ee2e-230">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="1ee2e-231">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="1ee2e-232">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-233">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="1ee2e-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="1ee2e-234">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-235">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1ee2e-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1ee2e-236">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1ee2e-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-237">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1ee2e-238">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1ee2e-239">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="1ee2e-240">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-240">Cost actual</span></span></td>
<td><span data-ttu-id="1ee2e-241">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-242">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-243">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-244">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-245">Cost real</span><span class="sxs-lookup"><span data-stu-id="1ee2e-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-246">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1ee2e-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="1ee2e-247">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="1ee2e-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-248">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="1ee2e-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="1ee2e-249">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="1ee2e-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-250">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ee2e-251">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-252">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1ee2e-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ee2e-253">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ee2e-254">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ee2e-255">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ee2e-256">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-257">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1ee2e-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-258">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-259">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="1ee2e-260">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-261">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-261">Billed sales</span></span></td>
<td><span data-ttu-id="1ee2e-262">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ee2e-263">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="1ee2e-264">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="1ee2e-265">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-266">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-267">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-268">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1ee2e-269">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-270">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="1ee2e-271">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-272">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1ee2e-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ee2e-273">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1ee2e-274">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ee2e-275">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ee2e-276">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="1ee2e-277">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="1ee2e-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="1ee2e-278">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="1ee2e-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="1ee2e-279">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-280">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="1ee2e-281">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="1ee2e-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-282">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-282">Billed sales</span></span></td>
<td><span data-ttu-id="1ee2e-283">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1ee2e-284">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="1ee2e-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="1ee2e-285">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="1ee2e-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="1ee2e-286">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-287">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="1ee2e-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="1ee2e-288">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ee2e-289">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="1ee2e-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="1ee2e-290">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="1ee2e-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]