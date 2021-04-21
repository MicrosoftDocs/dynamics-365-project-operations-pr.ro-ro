---
title: Configurarea componentelor tarifabile ale unei linii de ofertă
description: Acest subiect oferă informații despre configurarea componentelor taxabile și netaxabile pe o linie de ofertă bazată pe proiect.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858308"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="26140-103">Configurarea componentelor tarifabile ale unei linii de ofertă</span><span class="sxs-lookup"><span data-stu-id="26140-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="26140-104">_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_</span><span class="sxs-lookup"><span data-stu-id="26140-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="26140-105">O linie de ofertă bazată pe proiecte are conceptul de componente *incluse* și componente *taxabile*.</span><span class="sxs-lookup"><span data-stu-id="26140-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="26140-106">Componentele incluse sunt supuse la:</span><span class="sxs-lookup"><span data-stu-id="26140-106">Included components are subject to:</span></span>

  - <span data-ttu-id="26140-107">Metoda de facturare și împărțirea clienților</span><span class="sxs-lookup"><span data-stu-id="26140-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="26140-108">Limite de nedepășire</span><span class="sxs-lookup"><span data-stu-id="26140-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="26140-109">Setările frecvenței facturilor definite pe linia de ofertă bazată pe proiect</span><span class="sxs-lookup"><span data-stu-id="26140-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="26140-110">Un subset al componentelor incluse poate fi marcat ca taxabil folosind câmpul **Tip de facturare**.</span><span class="sxs-lookup"><span data-stu-id="26140-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="26140-111">Câmpul **Tip de facturare** este un set de opțiuni care permite următoarele valori în contextul unei linii de ofertă:</span><span class="sxs-lookup"><span data-stu-id="26140-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="26140-112">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-112">Chargeable</span></span>
  - <span data-ttu-id="26140-113">Netaxabil</span><span class="sxs-lookup"><span data-stu-id="26140-113">Non-chargeable</span></span>

<span data-ttu-id="26140-114">Componentele taxabile pot fi definite pe sarcini, roluri și categorii de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="26140-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="26140-115">Taxabilitatea este definită pentru sarcinile pentru linia de ofertă și se aplică tuturor claselor de tranzacții incluse pe acea linie.</span><span class="sxs-lookup"><span data-stu-id="26140-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="26140-116">Dacă câmpul **Includeți activități** este setat la **Întregul proiect** sau este necompletat, fila **Sarcini taxabile** nu este disponibilă.</span><span class="sxs-lookup"><span data-stu-id="26140-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="26140-117">Taxabilitatea este definită pe roluri pentru o linie de ofertă și se aplică numai pentru clasa tranzacției **Timp**.</span><span class="sxs-lookup"><span data-stu-id="26140-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="26140-118">Dacă câmpul **Includeți timpul** de pe o linie de ofertă de contract este setat la **Nu**, fila **Roluri tarifabile** nu este disponibilă.</span><span class="sxs-lookup"><span data-stu-id="26140-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="26140-119">Taxabilitatea este definită pe categorii de tranzacții pentru o linie de ofertă și se aplică numai pentru clasa tranzacției **Cheltuială**.</span><span class="sxs-lookup"><span data-stu-id="26140-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="26140-120">Dacă câmpul **Includeți cheltuieli** de pe o linie de ofertă de contract este setat la **Nu**, fila **Categorii tarifabile** nu este disponibilă.</span><span class="sxs-lookup"><span data-stu-id="26140-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="26140-121">Actualizați o sarcină de proiect pentru a fi taxabilă sau netaxabilă</span><span class="sxs-lookup"><span data-stu-id="26140-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="26140-122">O sarcină de proiect poate fi taxabilă sau netaxabilă în contextul unei linii specifice de ofertă bazate pe proiect, ceea ce face posibilă următoarea configurare.</span><span class="sxs-lookup"><span data-stu-id="26140-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="26140-123">Dacă o linie de ofertă bazată pe proiect include **Timp** și sarcina **T1**, sarcina este asociată liniei de ofertă ca taxabilă.</span><span class="sxs-lookup"><span data-stu-id="26140-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="26140-124">Dacă există o a doua linie de ofertă care include **Cheltuieli**, puteți asocia sarcina **T1** pe linia de ofertă ca netaxabilă.</span><span class="sxs-lookup"><span data-stu-id="26140-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="26140-125">Rezultatul este că tot timpul înregistrat în sarcină este taxabil și toate cheltuielile înregistrate în sarcină sunt netaxabile.</span><span class="sxs-lookup"><span data-stu-id="26140-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="26140-126">Un tip de facturare al activității poate fi configurat pe fila **Activități facturabile** al unei linii de ofertă bazată pe proiect actualizând câmpul **Tip de facturare** pe subgrila **Activități de linie de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="26140-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="26140-127">Alternativ, puteți actualiza tipul de facturare pentru o activitate de proiect în câmpul **Tip de facturare** pe subgrila activității de configurare a facturării unui proiect care arată liniile ofertei asociate unei activități.</span><span class="sxs-lookup"><span data-stu-id="26140-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="26140-128">Actualizați un rol pentru a fi taxabil sau netaxabil</span><span class="sxs-lookup"><span data-stu-id="26140-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="26140-129">Un rol poate fi taxabil sau netaxabil în contextul unei linii specifice de ofertă pe bază de proiect.</span><span class="sxs-lookup"><span data-stu-id="26140-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="26140-130">Tipul de facturare al unui rol poate fi configurat pe fila **Roluri facturabile** al unei linii de ofertă bazată pe proiect actualizând câmpul **Tip de facturare** pe subgrila **Roluri facturabile**.</span><span class="sxs-lookup"><span data-stu-id="26140-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="26140-131">Actualizați o categorie de tranzacții pentru a fi taxabilă sau netaxabilă</span><span class="sxs-lookup"><span data-stu-id="26140-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="26140-132">O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="26140-133">Tipul de facturare al unei tranzacții poate fi configurat pe fila **Categorii facturabile** al unei linii de ofertă actualizând câmpul **Tip de facturare** pe subgrila **Categorii facturabile**.</span><span class="sxs-lookup"><span data-stu-id="26140-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="26140-134">Rezolvați taxarea</span><span class="sxs-lookup"><span data-stu-id="26140-134">Resolve chargeability</span></span>
<span data-ttu-id="26140-135">O estimare sau o valoare reală creată pentru timp va fi considerată taxabilă numai dacă:</span><span class="sxs-lookup"><span data-stu-id="26140-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="26140-136">**Timp** este inclus pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="26140-137">**Rol** este configurat ca taxabil pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="26140-138">**Sarcini incluse** este setat la **Sarcini selectate** pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="26140-139">Dacă aceste trei lucruri sunt adevărate, **Sarcină** este, de asemenea, configurat ca taxabil.</span><span class="sxs-lookup"><span data-stu-id="26140-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="26140-140">O estimare sau o valoare reală creată pentru cheltuieli este considerată taxabilă numai dacă:</span><span class="sxs-lookup"><span data-stu-id="26140-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="26140-141">**Cheltuieli** este inclus pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="26140-142">**Categoria tranzacției** este configurat ca taxabil pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="26140-143">**Sarcini incluse** este setat la **Sarcini selectate** pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="26140-144">Dacă aceste trei lucruri sunt adevărate, **Sarcină** este, de asemenea, configurat ca taxabil.</span><span class="sxs-lookup"><span data-stu-id="26140-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="26140-145">O estimare sau o valoare reală creată pentru material va fi considerată taxabilă numai dacă:</span><span class="sxs-lookup"><span data-stu-id="26140-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="26140-146">**Materiale** este inclus pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="26140-147">**Sarcini incluse** este setat la **Sarcini selectate** pe linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="26140-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="26140-148">Dacă aceste două lucruri sunt adevărate, **Sarcină** ar trebui să fie configurat tot ca taxabil.</span><span class="sxs-lookup"><span data-stu-id="26140-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-149">
                    <strong>Include timpul</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="26140-150">
                    <strong>Include cheltuielile</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="26140-151">
                    <strong>Includere Materiale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="26140-152">
                    <strong>Activități incluse</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-153">
                    <strong>Rol</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-154">
                    <strong>Categorie</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-155">
                    <strong>Activitate</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="26140-156">
                    <strong>Impactul taxării</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-157">Da</span><span class="sxs-lookup"><span data-stu-id="26140-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-158">Da</span><span class="sxs-lookup"><span data-stu-id="26140-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-159">Da</span><span class="sxs-lookup"><span data-stu-id="26140-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-160">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-161">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-162">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-163">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-164">Facturare la un timp real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-165">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-166">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-167">Da</span><span class="sxs-lookup"><span data-stu-id="26140-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-168">Da</span><span class="sxs-lookup"><span data-stu-id="26140-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-169">Da</span><span class="sxs-lookup"><span data-stu-id="26140-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-170">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="26140-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-171">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-172">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-173">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-174">Facturare la un timp real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-175">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-176">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-177">Da</span><span class="sxs-lookup"><span data-stu-id="26140-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-178">Da</span><span class="sxs-lookup"><span data-stu-id="26140-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-179">Da</span><span class="sxs-lookup"><span data-stu-id="26140-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-180">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="26140-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-181">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-182">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-183">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-184">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-185">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-186">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-187">Da</span><span class="sxs-lookup"><span data-stu-id="26140-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-188">Da</span><span class="sxs-lookup"><span data-stu-id="26140-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-189">Da</span><span class="sxs-lookup"><span data-stu-id="26140-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-190">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="26140-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-191">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-192">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-193">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-194">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-195">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-196">Tip de facturare pe materiale reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-197">Da</span><span class="sxs-lookup"><span data-stu-id="26140-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-198">Da</span><span class="sxs-lookup"><span data-stu-id="26140-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-199">Da</span><span class="sxs-lookup"><span data-stu-id="26140-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-200">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="26140-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-201">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-202">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-203">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-204">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-205">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-206">Tip de facturare pe materiale reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-207">Da</span><span class="sxs-lookup"><span data-stu-id="26140-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-208">Da</span><span class="sxs-lookup"><span data-stu-id="26140-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-209">Da</span><span class="sxs-lookup"><span data-stu-id="26140-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-210">Numai activități selectate</span><span class="sxs-lookup"><span data-stu-id="26140-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-211">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-212">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-213">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-214">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-215">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-216">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-218">Da</span><span class="sxs-lookup"><span data-stu-id="26140-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-219">Da</span><span class="sxs-lookup"><span data-stu-id="26140-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-220">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-221">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-222">
                    <strong>Taxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-223">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-224">Facturare pe un timp real: <strong>Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-225">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-226">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-228">Da</span><span class="sxs-lookup"><span data-stu-id="26140-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-229">Da</span><span class="sxs-lookup"><span data-stu-id="26140-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-230">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-231">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-232">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-233">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-234">Facturare pe un timp real: <strong>Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-235">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-236">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-237">Da</span><span class="sxs-lookup"><span data-stu-id="26140-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="26140-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-239">Da</span><span class="sxs-lookup"><span data-stu-id="26140-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-240">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-241">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-242">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-243">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-244">Facturare la un timp real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-245">Tipul de facturare pe cheltuieli reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-246">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-247">Da</span><span class="sxs-lookup"><span data-stu-id="26140-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="26140-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="26140-249">Da</span><span class="sxs-lookup"><span data-stu-id="26140-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-250">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-251">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-252">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-253">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-254">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-255">Tipul de facturare pe cheltuieli reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-256">Tipul de facturare pentru materialul real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-257">Da</span><span class="sxs-lookup"><span data-stu-id="26140-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-258">Da</span><span class="sxs-lookup"><span data-stu-id="26140-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="26140-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-260">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-261">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-262">Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-263">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-264">Facturare la un timp real: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-265">Tipul de facturare pentru cheltuieli reale: Taxabil</span><span class="sxs-lookup"><span data-stu-id="26140-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="26140-266">Tipul de facturare pe materiale reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="26140-267">Da</span><span class="sxs-lookup"><span data-stu-id="26140-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="26140-268">Da</span><span class="sxs-lookup"><span data-stu-id="26140-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="26140-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="26140-270">Întregul proiect</span><span class="sxs-lookup"><span data-stu-id="26140-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="26140-271">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="26140-272">
                    <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="26140-273">Nu poate fi setat</span><span class="sxs-lookup"><span data-stu-id="26140-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="26140-274">Facturare la un timp real: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-275">Tip de facturare pe cheltuieli reale: <strong>Netaxabil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="26140-276">Tipul de facturare pe materiale reale:<strong> Indisponibil</strong>
                </span><span class="sxs-lookup"><span data-stu-id="26140-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
