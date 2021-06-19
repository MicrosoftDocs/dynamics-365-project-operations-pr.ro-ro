---
title: Configurarea componentelor tarifabile ale unei linii de contract bazate pe proiect
description: Acest subiect oferă informații despre cum să adăugați componente taxabile la liniile contractuale în Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003736"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="975c3-103">Configurarea componentelor tarifabile ale unei linii de contract bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="975c3-104">_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_</span><span class="sxs-lookup"><span data-stu-id="975c3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="975c3-105">O linie de contract bazată pe proiecte are componente *incluse* și componente *taxabile*.</span><span class="sxs-lookup"><span data-stu-id="975c3-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="975c3-106">Componentele incluse sunt componente care fac obiectul:</span><span class="sxs-lookup"><span data-stu-id="975c3-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="975c3-107">Metoda de facturare și împărțirea clienților</span><span class="sxs-lookup"><span data-stu-id="975c3-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="975c3-108">Limite de nedepășire</span><span class="sxs-lookup"><span data-stu-id="975c3-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="975c3-109">Setările frecvenței facturilor definite pe linia de contract bazată pe proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="975c3-110">Un subset al componentelor incluse poate fi marcat ca taxabil folosind câmpul **Tip de facturare**.</span><span class="sxs-lookup"><span data-stu-id="975c3-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="975c3-111">Câmpul **Tip de facturare** este un set de opțiuni care permite următoarele valori în contextul unei linii contractuale:</span><span class="sxs-lookup"><span data-stu-id="975c3-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="975c3-112">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-112">Chargeable</span></span>
  - <span data-ttu-id="975c3-113">Netaxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-113">Non-chargeable</span></span>

<span data-ttu-id="975c3-114">Componentele taxabile pot fi definite pe sarcini, roluri și categorii de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="975c3-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="975c3-115">Taxabilitatea este definită pentru sarcinile pentru o linie de contract de proiect și se aplică tuturor claselor de tranzacții incluse pe linie.</span><span class="sxs-lookup"><span data-stu-id="975c3-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="975c3-116">Dacă câmpul **Includeți activități** de pe o linie de contract este necompletat sau setat la **Întregul proiect**, fila **Sarcini taxabile** nu va fi disponibilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="975c3-117">Taxabilitatea definită pe roluri pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Timp**.</span><span class="sxs-lookup"><span data-stu-id="975c3-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="975c3-118">Dacă câmpul **Includeți timpul** de pe o linie de contract este setat la **Nu**, fila **Roluri tarifabile** nu va fi disponibilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="975c3-119">Taxabilitatea definită pe categorii de tranzacții pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Cheltuială**.</span><span class="sxs-lookup"><span data-stu-id="975c3-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="975c3-120">Dacă câmpul **Includeți cheltuielile** este setat la **Nu**, fila **Categorii tarifabile** nu va fi disponibilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="975c3-121">Actualizați o sarcină de proiect ca fiind taxabilă sau netaxabilă</span><span class="sxs-lookup"><span data-stu-id="975c3-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="975c3-122">O sarcină de proiect poate fi taxabilă sau netaxabilă pe o anumită linie contractuală, ceea ce face posibilă următoarea configurare:</span><span class="sxs-lookup"><span data-stu-id="975c3-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="975c3-123">Dacă o linie de contract bazată pe proiect include **Timp** și o anumită sarcină, **T1** este asociat acesteia ca taxabil.</span><span class="sxs-lookup"><span data-stu-id="975c3-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="975c3-124">Dacă există o a doua linie de contract care include **Cheltuieli**, puteți asocia sarcina T1 pe linia contractului ca netaxabilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="975c3-125">Rezultatul este că tot timpul înregistrat în sarcină este taxabil și toate cheltuielile sunt netaxabile.</span><span class="sxs-lookup"><span data-stu-id="975c3-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="975c3-126">Tipul de facturare al unei activități poate fi configurat pe fila **Activități facturabile** liniei contractului prin actualizarea câmpului **Tip de facturare** pe subgrila activități linie contract.</span><span class="sxs-lookup"><span data-stu-id="975c3-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="975c3-127">Alternativ, puteți actualiza câmpul **Tip de facturare** pe subgrila sarcinii Configurarea facturării unui proiect care arată liniile contractuale asociate unei activități.</span><span class="sxs-lookup"><span data-stu-id="975c3-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="975c3-128">Actualizați un rol ca fiind taxabil sau netaxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="975c3-129">Un rol poate fi taxabil sau netaxabil pe o anumită linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="975c3-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="975c3-130">Tipul de facturare al unui rol poate fi configurat pe fila **Roluri tarifabile** al unei linii contractuale.</span><span class="sxs-lookup"><span data-stu-id="975c3-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="975c3-131">Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe subgrila **Roluri facturabile**.</span><span class="sxs-lookup"><span data-stu-id="975c3-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="975c3-132">Actualizați o categorie de tranzacții ca fiind taxabilă sau netaxabilă</span><span class="sxs-lookup"><span data-stu-id="975c3-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="975c3-133">O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="975c3-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="975c3-134">Tipul de facturare al unei tranzacții poate fi configurat pe fila **Categorii tarifabile** a unei linii de contract bazate pe proiect.</span><span class="sxs-lookup"><span data-stu-id="975c3-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="975c3-135">Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe subgrila **Categorii facturabile**.</span><span class="sxs-lookup"><span data-stu-id="975c3-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="975c3-136">Rezolvați taxarea</span><span class="sxs-lookup"><span data-stu-id="975c3-136">Resolve chargeability</span></span>

<span data-ttu-id="975c3-137">O estimare sau o valoare reală creată pentru timp este considerată taxabilă numai dacă:</span><span class="sxs-lookup"><span data-stu-id="975c3-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="975c3-138">**Timp** este inclus pe linia de contract.</span><span class="sxs-lookup"><span data-stu-id="975c3-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="975c3-139">**Rol** este configurat ca taxabil pe linia de contract.</span><span class="sxs-lookup"><span data-stu-id="975c3-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="975c3-140">**Sarcini incluse** este setat la **Sarcini selectate** pe linia de contract.</span><span class="sxs-lookup"><span data-stu-id="975c3-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="975c3-141">Dacă aceste trei lucruri sunt adevărate, sarcina este și ea configurată ca taxabilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="975c3-142">O estimare sau o valoare reală creată pentru cheltuieli este considerată taxabilă numai dacă:</span><span class="sxs-lookup"><span data-stu-id="975c3-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="975c3-143">**Cheltuieli** este inclus pe linia de contract</span><span class="sxs-lookup"><span data-stu-id="975c3-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="975c3-144">**Categoria tranzacției** este configurat ca taxabil pe linia de contract</span><span class="sxs-lookup"><span data-stu-id="975c3-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="975c3-145">**Sarcini incluse** este setat la **Sarcină selectată** pe linia de contract</span><span class="sxs-lookup"><span data-stu-id="975c3-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="975c3-146">Dacă aceste trei lucruri sunt adevărate, **Sarcină** este și ea configurată ca taxabilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="975c3-147">O estimare sau o valoare reală creată pentru materiale este considerată taxabilă numai dacă:</span><span class="sxs-lookup"><span data-stu-id="975c3-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="975c3-148">**Materiale** este inclus pe linia de contract</span><span class="sxs-lookup"><span data-stu-id="975c3-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="975c3-149">**Sarcini incluse** este setat la **Sarcini selectate** pe linia de contract</span><span class="sxs-lookup"><span data-stu-id="975c3-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="975c3-150">Dacă aceste două lucruri sunt adevărate, **Sarcină** este și ea configurată ca taxabilă.</span><span class="sxs-lookup"><span data-stu-id="975c3-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-151">
                    <strong>Include timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="975c3-152">
                    <strong>Include cheltuielile</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="975c3-153">
                    <strong>Includere Materiale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="975c3-154">
                    <strong>Activități incluse</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-155">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-156">
                    <strong>Categorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-157">
                    <strong>Activitate</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="975c3-158">
                    <strong>Impactul taxării</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-159">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-160">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-161">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-162">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-163">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-164">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-165">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-166">Facturare la un timp real: <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-167">Tipul de facturare pe cheltuieli reale: <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-168">Tipul de facturare pe materialul real: <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-169">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-170">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-171">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-172">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="975c3-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-173">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-174">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-175">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-176">Facturare la un timp real: <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-177">Tipul de facturare pe cheltuieli reale: <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-178">Tipul de facturare pe materialul real: <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-179">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-180">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-181">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-182">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="975c3-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-183">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-184">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-185">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-186">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-187">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="975c3-188">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-189">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-190">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-191">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-192">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="975c3-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-193">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-194">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-195">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-196">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-197">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-198">Tip de facturare pe materiale reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-199">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-200">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-201">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-202">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="975c3-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-203">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-204">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-205">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-206">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-207">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-208">Tip de facturare pe materiale reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-209">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-210">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-211">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-212">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="975c3-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-213">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-214">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-215">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-216">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-217">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-218">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-220">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-221">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-222">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-223">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-224">
                    <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-225">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-226">Facturare pe un timp real: <strong>Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-227">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="975c3-228">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-230">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-231">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-232">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-233">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-234">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-235">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-236">Facturare pe un timp real: <strong>Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-237">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-238">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-239">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="975c3-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-241">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-242">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-243">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-244">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-245">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-246">Facturare la un timp real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="975c3-247">Tipul de facturare pe cheltuieli reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-248">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-249">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="975c3-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="975c3-251">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-252">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-253">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-254">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-255">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-256">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-257">Tipul de facturare pe cheltuieli reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-258">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-259">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-260">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="975c3-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-262">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-263">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-264">Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-265">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-266">Facturare la un timp real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="975c3-267">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="975c3-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="975c3-268">Tipul de facturare pe materiale reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="975c3-269">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="975c3-270">Da</span><span class="sxs-lookup"><span data-stu-id="975c3-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="975c3-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="975c3-272">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="975c3-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="975c3-273">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="975c3-274">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="975c3-275">Nu se poate seta</span><span class="sxs-lookup"><span data-stu-id="975c3-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="975c3-276">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-277">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="975c3-278">Tipul de facturare pe materiale reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="975c3-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
