---
title: Date reale
description: Acest subiect oferă informații despre cum să lucrați cu cifrele reale în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996626"
---
# <a name="actuals"></a><span data-ttu-id="f0a56-103">Date reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-103">Actuals</span></span> 

<span data-ttu-id="f0a56-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="f0a56-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0a56-105">Valorile reale reprezintă progresul financiar revizuit și aprobat și evoluția planificată a unui proiect.</span><span class="sxs-lookup"><span data-stu-id="f0a56-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="f0a56-106">Acestea sunt create ca urmare a aprobării timpului, cheltuielilor, înregistrărilor de utilizare a materialelor, înregistrărilor din jurnal și facturilor.</span><span class="sxs-lookup"><span data-stu-id="f0a56-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="f0a56-107">Liniile de jurnal și remiteri de timp</span><span class="sxs-lookup"><span data-stu-id="f0a56-107">Journal lines and time submission</span></span>

<span data-ttu-id="f0a56-108">Pentru mai multe informații despre remiteri de timp, consultați [Prezentare generală a intrării de timp](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0a56-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f0a56-109">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="f0a56-109">Time and materials</span></span>

<span data-ttu-id="f0a56-110">Atunci când o intrare de timp care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="f0a56-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f0a56-111">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-111">Fixed price</span></span>

<span data-ttu-id="f0a56-112">Atunci când o intrare de timp care este remisă este legată de un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.</span><span class="sxs-lookup"><span data-stu-id="f0a56-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f0a56-113">Tarifare implicită</span><span class="sxs-lookup"><span data-stu-id="f0a56-113">Default pricing</span></span>

<span data-ttu-id="f0a56-114">Logica pentru crearea prețurilor implicite se află pe linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="f0a56-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="f0a56-115">Valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="f0a56-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="f0a56-116">Aceste valori includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="f0a56-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="f0a56-117">Câmpurile care afectează stabilirea implicită a prețurilor, cum ar fi **Rol** și **Unitate de resurse**, sunt utilizate pentru a determina prețul adecvat în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="f0a56-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f0a56-118">Puteți adăuga un câmp personalizat la intrarea în timp.</span><span class="sxs-lookup"><span data-stu-id="f0a56-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="f0a56-119">Dacă doriți ca valoarea câmpului să fie propagată la valorile reale, creați câmpul în tabelele **Valori reale** și **Linie de jurnal**.</span><span class="sxs-lookup"><span data-stu-id="f0a56-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f0a56-120">Utilizați codul personalizat pentru a propaga valoarea câmpului selectat de la introducerea timpului la valori efective prin linia jurnal folosind originile tranzacției.</span><span class="sxs-lookup"><span data-stu-id="f0a56-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f0a56-121">Pentru mai multe informații despre originile tranzacțiilor și conexiuni, consultați [Conectarea valorilor reale la înregistrările originale](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f0a56-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="f0a56-122">Liniile de jurnal și remiterea cheltuielilor de bază</span><span class="sxs-lookup"><span data-stu-id="f0a56-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="f0a56-123">Pentru mai multe informații despre intrări de cheltuială [Prezentare generală a cheltuielii](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0a56-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f0a56-124">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="f0a56-124">Time and materials</span></span>

<span data-ttu-id="f0a56-125">Atunci când o intrare de cheltuială de bază care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="f0a56-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f0a56-126">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-126">Fixed price</span></span>

<span data-ttu-id="f0a56-127">Atunci când o intrare de cheltuieli de bază remisă este legată la un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.</span><span class="sxs-lookup"><span data-stu-id="f0a56-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f0a56-128">Tarifare implicită</span><span class="sxs-lookup"><span data-stu-id="f0a56-128">Default pricing</span></span>

<span data-ttu-id="f0a56-129">Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="f0a56-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="f0a56-130">Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="f0a56-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f0a56-131">Câmpurile care afectează stabilirea implicită a prețurilor, cum ar fi **Categoria tranzacției** și **Unitate**, sunt utilizate pentru a determina prețul adecvat în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="f0a56-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f0a56-132">Cu toate acestea, acest lucru funcționează numai atunci când metoda de stabilire a prețurilor din lista de prețuri este **Preț unitar**.</span><span class="sxs-lookup"><span data-stu-id="f0a56-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="f0a56-133">Dacă metoda de stabilire a prețurilor este **La cost** sau **Adaos peste cost**, prețul introdus la crearea înregistrării de cheltuieli este utilizat pentru cost și prețul de pe linia jurnalului de vânzări este calculat pe baza metodei de stabilire a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="f0a56-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="f0a56-134">Puteți adăuga un câmp personalizat la intrarea de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="f0a56-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="f0a56-135">Dacă doriți ca valoarea câmpului să fie propagată la valorile reale, creați câmpul în tabelele **Valori reale** și **Linie de jurnal**.</span><span class="sxs-lookup"><span data-stu-id="f0a56-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f0a56-136">Utilizați codul personalizat pentru a propaga valoarea câmpului selectat de la introducerea timpului la valori efective prin linia jurnal folosind originile tranzacției.</span><span class="sxs-lookup"><span data-stu-id="f0a56-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f0a56-137">Pentru mai multe informații despre originile tranzacțiilor și conexiuni, consultați [Conectarea valorilor reale la înregistrările originale](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f0a56-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="f0a56-138">Liniile jurnalului și trimiterea jurnalului de utilizare a materialelor</span><span class="sxs-lookup"><span data-stu-id="f0a56-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="f0a56-139">Pentru mai multe informații despre introducerea cheltuielilor, consultați [Jurnal de utilizare a materialelor](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="f0a56-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f0a56-140">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="f0a56-140">Time and materials</span></span>

<span data-ttu-id="f0a56-141">Atunci când o înregistrare de utilizare a materialului trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.</span><span class="sxs-lookup"><span data-stu-id="f0a56-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f0a56-142">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-142">Fixed price</span></span>

<span data-ttu-id="f0a56-143">Atunci când o intrare remisă de jurnal de utilizare de material este legată de un proiect mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.</span><span class="sxs-lookup"><span data-stu-id="f0a56-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f0a56-144">Tarifare implicită</span><span class="sxs-lookup"><span data-stu-id="f0a56-144">Default pricing</span></span>

<span data-ttu-id="f0a56-145">Logica pentru introducerea prețurilor implicite pentru material se bazează pe combinația de produse și unități.</span><span class="sxs-lookup"><span data-stu-id="f0a56-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="f0a56-146">Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="f0a56-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f0a56-147">Câmpurile care afectează stabilirea implicită a prețurilor, cum ar fi **ID produs** și **Unitate**, sunt utilizate pentru a determina prețul adecvat în linia de jurnal.</span><span class="sxs-lookup"><span data-stu-id="f0a56-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f0a56-148">Cu toate acestea, acest lucru funcționează numai pentru produsele din catalog.</span><span class="sxs-lookup"><span data-stu-id="f0a56-148">However, this only works for catalog products.</span></span> <span data-ttu-id="f0a56-149">Pentru produsele din afara catalogului, prețul introdus la crearea înregistrării jurnalului de utilizare a materialului este utilizat pentru cost și prețul de vânzare pe liniile jurnalului.</span><span class="sxs-lookup"><span data-stu-id="f0a56-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="f0a56-150">Puteți adăuga un câmp personalizat la intrarea **Jurnal de utilizare materiale**.</span><span class="sxs-lookup"><span data-stu-id="f0a56-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="f0a56-151">Dacă doriți ca valoarea câmpului să fie propagată la valorile reale, creați câmpul în tabelele **Valori reale** și **Linie de jurnal**.</span><span class="sxs-lookup"><span data-stu-id="f0a56-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f0a56-152">Utilizați codul personalizat pentru a propaga valoarea câmpului selectat de la introducerea timpului la valori efective prin linia jurnal folosind originile tranzacției.</span><span class="sxs-lookup"><span data-stu-id="f0a56-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f0a56-153">Pentru mai multe informații despre originile tranzacțiilor și conexiuni, consultați [Conectarea valorilor reale la înregistrările originale](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f0a56-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="f0a56-154">Utilizați intrările de jurnal pentru a înregistra costurilr</span><span class="sxs-lookup"><span data-stu-id="f0a56-154">Use entry journals to record costs</span></span>

<span data-ttu-id="f0a56-155">Puteți utiliza intrările de jurnal pentru a înregistra costul sau venitul în material, tarif, timp, cheltuieli sau clase de taxe de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="f0a56-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f0a56-156">Jurnalele pot fi utilizate în următoarele scopuri:</span><span class="sxs-lookup"><span data-stu-id="f0a56-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="f0a56-157">Mutați valorile reale privind tranzacțiile dintr-un alt sistem în Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f0a56-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="f0a56-158">Înregistrați costurile care au avut loc într-un alt sistem.</span><span class="sxs-lookup"><span data-stu-id="f0a56-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="f0a56-159">Aceste costuri pot include costuri de achiziție sau subcontractare.</span><span class="sxs-lookup"><span data-stu-id="f0a56-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0a56-160">Aplicația nu validează tipul liniei jurnalului sau prețurile aferente care sunt introduse pe linia jurnalului.</span><span class="sxs-lookup"><span data-stu-id="f0a56-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="f0a56-161">Prin urmare, numai un utilizator care este pe deplin conștient de impactul contabil pe care îl au efectele reale asupra proiectului ar trebui să utilizeze jurnale de intrare pentru a crea date reale.</span><span class="sxs-lookup"><span data-stu-id="f0a56-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="f0a56-162">Datorită impactului acestui tip de jurnal, ar trebui să alegeți cu atenție cine are acces pentru a crea jurnale de intrare.</span><span class="sxs-lookup"><span data-stu-id="f0a56-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="f0a56-163">Înregistrați valorile reale pe baza evenimentelor proiectului</span><span class="sxs-lookup"><span data-stu-id="f0a56-163">Record actuals based on project events</span></span>

<span data-ttu-id="f0a56-164">Project Operations înregistrează tranzacțiile financiare care apar în timpul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="f0a56-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f0a56-165">Aceste tranzacții sunt înregistrate ca valori reale.</span><span class="sxs-lookup"><span data-stu-id="f0a56-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="f0a56-166">Tabelele următoare arată diferitele tipuri de valori reale care sunt create, în funcție de faptul dacă proiectul este un proiect pe bază de timp și materiale sau un proiect cu preț fix, este în etapa de prevânzare sau este un proiect intern.</span><span class="sxs-lookup"><span data-stu-id="f0a56-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="f0a56-167">Resursa aparține aceleiași unități organizatorice ca și unitatea contractantă a proiectului</span><span class="sxs-lookup"><span data-stu-id="f0a56-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f0a56-168">Eveniment</span><span class="sxs-lookup"><span data-stu-id="f0a56-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f0a56-169">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="f0a56-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f0a56-170">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="f0a56-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f0a56-171">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="f0a56-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f0a56-172">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="f0a56-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f0a56-173">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f0a56-174">Reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-174">Actuals</span></span></th>
<th><span data-ttu-id="f0a56-175">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="f0a56-175">Transaction currency</span></span></th>
<th><span data-ttu-id="f0a56-176">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-176">Fixed price</span></span></th>
<th><span data-ttu-id="f0a56-177">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="f0a56-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f0a56-178">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="f0a56-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f0a56-179">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-180">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="f0a56-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f0a56-181">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f0a56-182">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f0a56-183">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-183">Cost actual</span></span></td>
<td><span data-ttu-id="f0a56-184">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-185">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-186">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f0a56-187">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-188">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-189">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="f0a56-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f0a56-190">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f0a56-191">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f0a56-192">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-192">Cost actual</span></span></td>
<td><span data-ttu-id="f0a56-193">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-194">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-195">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-196">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-197">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-198">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="f0a56-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f0a56-199">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-200">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="f0a56-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f0a56-201">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f0a56-202">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f0a56-203">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f0a56-204">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-205">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="f0a56-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-206">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-207">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-208">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-209">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-209">Billed sales</span></span></td>
<td><span data-ttu-id="f0a56-210">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f0a56-211">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f0a56-212">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f0a56-213">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-214">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-215">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-216">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-217">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-218">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="f0a56-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f0a56-219">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-220">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="f0a56-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f0a56-221">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f0a56-222">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="f0a56-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f0a56-223">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="f0a56-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f0a56-224">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f0a56-225">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="f0a56-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f0a56-226">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="f0a56-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f0a56-227">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-228">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-229">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-230">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-230">Billed sales</span></span></td>
<td><span data-ttu-id="f0a56-231">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f0a56-232">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="f0a56-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f0a56-233">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="f0a56-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f0a56-234">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-235">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="f0a56-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f0a56-236">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-237">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="f0a56-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f0a56-238">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="f0a56-239">Resursa aparține unei unități organizatorice care diferă de unitatea contractantă a proiectului</span><span class="sxs-lookup"><span data-stu-id="f0a56-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f0a56-240">Eveniment</span><span class="sxs-lookup"><span data-stu-id="f0a56-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f0a56-241">Proiect facturabil sau vândut</span><span class="sxs-lookup"><span data-stu-id="f0a56-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f0a56-242">Proiect în etapa de prevânzare</span><span class="sxs-lookup"><span data-stu-id="f0a56-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f0a56-243">Proiect intern</span><span class="sxs-lookup"><span data-stu-id="f0a56-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f0a56-244">Timp și materiale</span><span class="sxs-lookup"><span data-stu-id="f0a56-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f0a56-245">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f0a56-246">Reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-246">Actuals</span></span></th>
<th><span data-ttu-id="f0a56-247">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="f0a56-247">Transaction currency</span></span></th>
<th><span data-ttu-id="f0a56-248">Preț fix</span><span class="sxs-lookup"><span data-stu-id="f0a56-248">Fixed price</span></span></th>
<th><span data-ttu-id="f0a56-249">Monedă de tranzacționare</span><span class="sxs-lookup"><span data-stu-id="f0a56-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f0a56-250">Este creată o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="f0a56-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f0a56-251">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-252">Este remisă o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="f0a56-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f0a56-253">Nicio activitate în entitatea Valori reale</span><span class="sxs-lookup"><span data-stu-id="f0a56-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f0a56-254">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f0a56-255">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-255">Cost actual</span></span></td>
<td><span data-ttu-id="f0a56-256">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f0a56-257">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f0a56-258">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f0a56-259">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f0a56-260">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-261">Valoare reală vânzări nefacturate – taxabilă</span><span class="sxs-lookup"><span data-stu-id="f0a56-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f0a56-262">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-263">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="f0a56-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f0a56-264">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="f0a56-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-265">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="f0a56-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f0a56-266">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f0a56-267">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f0a56-268">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-268">Cost actual</span></span></td>
<td><span data-ttu-id="f0a56-269">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-270">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-271">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-272">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-273">Cost real</span><span class="sxs-lookup"><span data-stu-id="f0a56-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-274">Cost de unitate resursă</span><span class="sxs-lookup"><span data-stu-id="f0a56-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f0a56-275">Monedă unitate resursă</span><span class="sxs-lookup"><span data-stu-id="f0a56-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-276">Vânzări inter-organizaționale</span><span class="sxs-lookup"><span data-stu-id="f0a56-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f0a56-277">Moneda unității contractante</span><span class="sxs-lookup"><span data-stu-id="f0a56-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-278">Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="f0a56-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f0a56-279">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-280">Valoare reală vânzări nefacturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="f0a56-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f0a56-281">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f0a56-282">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f0a56-283">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f0a56-284">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-285">Vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="f0a56-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-286">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-287">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f0a56-288">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-289">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-289">Billed sales</span></span></td>
<td><span data-ttu-id="f0a56-290">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f0a56-291">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</span><span class="sxs-lookup"><span data-stu-id="f0a56-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f0a56-292">Inversare vânzări nefacturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f0a56-293">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-294">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-295">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-296">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f0a56-297">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-298">Vânzări facturate – taxabile pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="f0a56-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f0a56-299">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-300">Vânzări facturate – netaxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="f0a56-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f0a56-301">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f0a56-302">O factură este corectată pentru a mări cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="f0a56-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f0a56-303">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="f0a56-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f0a56-304">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f0a56-305">Inversare vânzări facturate pentru jalon</span><span class="sxs-lookup"><span data-stu-id="f0a56-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f0a56-306">Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></span><span class="sxs-lookup"><span data-stu-id="f0a56-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f0a56-307">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-308">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f0a56-309">Nu se aplică</span><span class="sxs-lookup"><span data-stu-id="f0a56-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-310">Vânzări facturate</span><span class="sxs-lookup"><span data-stu-id="f0a56-310">Billed sales</span></span></td>
<td><span data-ttu-id="f0a56-311">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f0a56-312">O factură este corectată pentru a micșora cantitatea tarifabilă.</span><span class="sxs-lookup"><span data-stu-id="f0a56-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f0a56-313">Vânzări facturate – inversare</span><span class="sxs-lookup"><span data-stu-id="f0a56-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f0a56-314">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-315">Vânzări facturate pentru noua cantitate</span><span class="sxs-lookup"><span data-stu-id="f0a56-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f0a56-316">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f0a56-317">Vânzări nefacturate – taxabile pentru diferență</span><span class="sxs-lookup"><span data-stu-id="f0a56-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f0a56-318">Monedă contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f0a56-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
