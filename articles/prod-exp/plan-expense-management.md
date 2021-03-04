---
title: Configurați gestionarea cheltuielilor
description: Acest articol descrie considerațiile și deciziile pe care trebuie să le luați în timpul procesului de planificare înainte de a configura gestionarea cheltuielilor în Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960352"
---
# <a name="configure-expense-management"></a><span data-ttu-id="604ca-103">Configurați gestionarea cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="604ca-103">Configure expense management</span></span>

<span data-ttu-id="604ca-104">Acest subiect descrie considerațiile și deciziile pe care trebuie să le luați în timpul procesului de planificare înainte de a configura gestionarea cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="604ca-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="604ca-105">În Gestionarea cheltuielilor, puteți stoca informații despre metodele de plată, cererile de călătorie, rapoartele de cheltuieli, politicile și așa mai departe.</span><span class="sxs-lookup"><span data-stu-id="604ca-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="604ca-106">Deoarece multe dintre deciziile pe care le luați atunci când vă planificați configurația pentru gestionarea cheltuielilor se bazează pe ierarhia și structura financiară a organizației dvs., trebuie să consultați documentele de planificare pentru acele domenii.</span><span class="sxs-lookup"><span data-stu-id="604ca-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="604ca-107">Cheltuieli între companii</span><span class="sxs-lookup"><span data-stu-id="604ca-107">Intercompany expenses</span></span>

<span data-ttu-id="604ca-108">Când activați cheltuielile între companii, permiteți persoanelor juridice și angajaților să suporte cheltuieli în numele altei persoane juridice și să colecteze plata de la entitatea juridică de angajare din cadrul organizației dvs.</span><span class="sxs-lookup"><span data-stu-id="604ca-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="604ca-109">De exemplu, un angajat al persoanei juridice A finalizează un proiect pentru persoana juridică B, iar proiectul suportă cheltuieli legate de călătorie.</span><span class="sxs-lookup"><span data-stu-id="604ca-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="604ca-110">Dacă sunt activate cheltuielile între companii, angajatul poate depune apoi un raport de cheltuieli care va înregistra cheltuielile către persoana juridică B, iar cheltuielile trebuie apoi plătite de persoana juridică A. Dacă organizația dvs. nu are mai multe persoane juridice, nu aveți nu trebuie să permită cheltuielile între companii.</span><span class="sxs-lookup"><span data-stu-id="604ca-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="604ca-111">**Decizie:** Doriți să activați cheltuielile între companii?</span><span class="sxs-lookup"><span data-stu-id="604ca-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="604ca-112">Gestiune financiară</span><span class="sxs-lookup"><span data-stu-id="604ca-112">Financial management</span></span>

<span data-ttu-id="604ca-113">Managementul cheltuielilor este strâns integrat cu managementul financiar al organizației dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="604ca-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="604ca-114">O mulțime de configurații pentru gestionarea cheltuielilor se vor baza pe deciziile pe care le-ați luat cu privire la finanțele organizației dvs.</span><span class="sxs-lookup"><span data-stu-id="604ca-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="604ca-115">Următoarele secțiuni descriu diferitele domenii care necesită planificare și decizii, pe baza deciziilor financiare și a îndrumărilor organizației dvs. din partea echipei de conducere.</span><span class="sxs-lookup"><span data-stu-id="604ca-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="604ca-116">Diurne</span><span class="sxs-lookup"><span data-stu-id="604ca-116">Per diems</span></span>

<span data-ttu-id="604ca-117">Trebuie să definiți dietele angajaților pe care le oferă organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="604ca-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="604ca-118">Deoarece diurnele sunt utilizate în mod obișnuit pentru acoperirea cheltuielilor, cum ar fi mesele, cazarea și alte cheltuieli accidentale, puteți crea reguli pentru indemnizațiile per diem pe care le oferă organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="604ca-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="604ca-119">ratele diurnei se pot baza pe perioada anului, locația călătoriei sau ambele.</span><span class="sxs-lookup"><span data-stu-id="604ca-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="604ca-120">Când definiți o regulă de diurnă, puteți specifica că un procent din rata diemului va fi reținut dacă un lucrător primește mese sau servicii gratuite.</span><span class="sxs-lookup"><span data-stu-id="604ca-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="604ca-121">De asemenea, puteți defini nivelurile de rate de diurnă pentru a configura numărul minim și maxim de ore pentru care poate fi aplicat diurnei pentru călătoria unui lucrător.</span><span class="sxs-lookup"><span data-stu-id="604ca-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="604ca-122">**Decizii**</span><span class="sxs-lookup"><span data-stu-id="604ca-122">**Decisions:**</span></span>

- <span data-ttu-id="604ca-123">Reguli implicite pentru diurnă pentru prima și ultima zi:</span><span class="sxs-lookup"><span data-stu-id="604ca-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="604ca-124">Care este numărul minim de ore pe care un angajat îl poate solicita pentru o zi și totuși primește o diurnă?</span><span class="sxs-lookup"><span data-stu-id="604ca-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="604ca-125">Există o reducere a sumei oferite pentru mesele din prima zi și ultima zi?</span><span class="sxs-lookup"><span data-stu-id="604ca-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="604ca-126">Dacă există o reducere, care este procentul reducerii?</span><span class="sxs-lookup"><span data-stu-id="604ca-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="604ca-127">Există o reducere a sumei oferite pentru un hotel pentru prima zi și ultima zi?</span><span class="sxs-lookup"><span data-stu-id="604ca-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="604ca-128">Dacă există o reducere, care este procentul reducerii?</span><span class="sxs-lookup"><span data-stu-id="604ca-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="604ca-129">Există o reducere a sumei oferite pentru alte cheltuieli care sunt percepute pentru prima zi și ultima zi?</span><span class="sxs-lookup"><span data-stu-id="604ca-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="604ca-130">Dacă există o reducere, care este procentul reducerii?</span><span class="sxs-lookup"><span data-stu-id="604ca-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="604ca-131">Reguli implicite de dirună:</span><span class="sxs-lookup"><span data-stu-id="604ca-131">Default per diem rules:</span></span>

    - <span data-ttu-id="604ca-132">Există o reducere procentuală a indemnizației per diem pentru fiecare masă dacă, de exemplu, masa este gratuită?</span><span class="sxs-lookup"><span data-stu-id="604ca-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="604ca-133">Dacă există o reducere, care este procentul reducerii pentru fiecare masă?</span><span class="sxs-lookup"><span data-stu-id="604ca-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="604ca-134">Reducerea meselor este calculată pe zi, pe călătorie sau în funcție de numărul de mese pe zi?</span><span class="sxs-lookup"><span data-stu-id="604ca-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="604ca-135">Sumele diurnelor trebuie rotunjite în mod obișnuit sau rotunjite în sus?</span><span class="sxs-lookup"><span data-stu-id="604ca-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="604ca-136">Sunt diurnele calculate pe o perioadă de 24 de ore sau într-o zi calendaristică?</span><span class="sxs-lookup"><span data-stu-id="604ca-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="604ca-137">Regulile de diurnă care se bazează pe locație:</span><span class="sxs-lookup"><span data-stu-id="604ca-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="604ca-138">Tarifele diurnei variază în funcție de locație?</span><span class="sxs-lookup"><span data-stu-id="604ca-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="604ca-139">Ce locații sunt incluse?</span><span class="sxs-lookup"><span data-stu-id="604ca-139">What locations are included?</span></span>
    - <span data-ttu-id="604ca-140">Dacă tarifele diurnei variază în funcție de locație, pentru fiecare locație, ce procentaj este prevăzut pentru următoarele tipuri de cheltuieli:</span><span class="sxs-lookup"><span data-stu-id="604ca-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="604ca-141">Mese</span><span class="sxs-lookup"><span data-stu-id="604ca-141">Meals</span></span>
        - <span data-ttu-id="604ca-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="604ca-142">Hotel</span></span>
        - <span data-ttu-id="604ca-143">Alte cheltuieli</span><span class="sxs-lookup"><span data-stu-id="604ca-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="604ca-144">Jurnalele și conturile de gestionare a cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="604ca-144">Expense management journals and accounts</span></span>

<span data-ttu-id="604ca-145">Gestionarea cheltuielilor necesită utilizarea mai multor jurnale și conturi.</span><span class="sxs-lookup"><span data-stu-id="604ca-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="604ca-146">Trebuie să decideți, de exemplu, dacă același cont este utilizat pentru avansuri de numerar și litigii legate de cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="604ca-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="604ca-147">**Decizii**</span><span class="sxs-lookup"><span data-stu-id="604ca-147">**Decisions:**</span></span>

- <span data-ttu-id="604ca-148">În ce jurnal contabil sunt afișate rapoartele de cheltuieli aprobate?</span><span class="sxs-lookup"><span data-stu-id="604ca-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="604ca-149">Ce cont este utilizat pentru avansuri de numerar?</span><span class="sxs-lookup"><span data-stu-id="604ca-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="604ca-150">Ar trebui ca avansurile de numerar să fie înregistrate imediat?</span><span class="sxs-lookup"><span data-stu-id="604ca-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="604ca-151">Metode de plată</span><span class="sxs-lookup"><span data-stu-id="604ca-151">Payment methods</span></span>

<span data-ttu-id="604ca-152">Atunci când permiteți angajaților să suporte cheltuieli în numele afacerii dvs., trebuie să definiți metodele de plată pe care angajații au voie să le folosească.</span><span class="sxs-lookup"><span data-stu-id="604ca-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="604ca-153">De exemplu, puteți permite angajaților să folosească numerar sau un card de credit corporativ.</span><span class="sxs-lookup"><span data-stu-id="604ca-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="604ca-154">De asemenea, puteți permite angajaților să utilizeze carduri de credit personale și apoi să le rambursați angajaților.</span><span class="sxs-lookup"><span data-stu-id="604ca-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="604ca-155">Trebuie să luați următoarele decizii pentru fiecare metodă de plată pe care o permiteți.</span><span class="sxs-lookup"><span data-stu-id="604ca-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="604ca-156">**Decizii**</span><span class="sxs-lookup"><span data-stu-id="604ca-156">**Decisions:**</span></span>

- <span data-ttu-id="604ca-157">Ce metode de plată sunt permise?</span><span class="sxs-lookup"><span data-stu-id="604ca-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="604ca-158">Cine deține cheltuielile cu metoda de plată?</span><span class="sxs-lookup"><span data-stu-id="604ca-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="604ca-159">Există un tip de cont compensat?</span><span class="sxs-lookup"><span data-stu-id="604ca-159">Is there an offset account type?</span></span> <span data-ttu-id="604ca-160">Dacă există un tip de cont compensat, ce este?</span><span class="sxs-lookup"><span data-stu-id="604ca-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="604ca-161">Dacă există un tip de cont compensat, care este contul?</span><span class="sxs-lookup"><span data-stu-id="604ca-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="604ca-162">Dacă metoda de plată este un card de credit, metoda de plată ar trebui utilizată numai cu tranzacțiile importate?</span><span class="sxs-lookup"><span data-stu-id="604ca-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="604ca-163">Categorii de cheltuieli și categorii partajate</span><span class="sxs-lookup"><span data-stu-id="604ca-163">Expense categories and shared categories</span></span>

<span data-ttu-id="604ca-164">Când angajații creează un raport de cheltuieli, fiecare cheltuială pe care o înregistrează trebuie să fie asociată unei categorii de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="604ca-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="604ca-165">Categoriile de cheltuieli sunt derivate din categorii comune care pot fi partajate între entitățile juridice din organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="604ca-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="604ca-166">Aceste categorii pot fi, de asemenea, partajate în managementul de proiect și contabilitate, în funcție de modul în care este definită organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="604ca-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="604ca-167">Pe baza definiției organizației dvs. și a îndrumărilor din partea echipei de implementare, trebuie să determinați dacă categoriile care sunt utilizate în gestionarea cheltuielilor vor fi utilizate numai în gestionarea cheltuielilor sau dacă ar trebui să fie partajate între Gestionarea proiectului și contabilitate și Gestionarea cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="604ca-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="604ca-168">Rețineți că aceste categorii pot fi împărțite între Proiect și Cheltuială sau Proiect și Producție, dar nu între Cheltuială și Producție.</span><span class="sxs-lookup"><span data-stu-id="604ca-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="604ca-169">Trebuie să luați următoarele decizii pentru fiecare categorie de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="604ca-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="604ca-170">**Decizii**</span><span class="sxs-lookup"><span data-stu-id="604ca-170">**Decisions:**</span></span>

- <span data-ttu-id="604ca-171">Care este categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-171">What is the expense category?</span></span> <span data-ttu-id="604ca-172">Exemplele includ categorii pentru zboruri, hotel sau kilometraj.</span><span class="sxs-lookup"><span data-stu-id="604ca-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="604ca-173">Categoria de cheltuieli poate fi utilizată și în managementul proiectelor și contabilitate?</span><span class="sxs-lookup"><span data-stu-id="604ca-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="604ca-174">Care este tipul de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-174">What is the expense type?</span></span>
- <span data-ttu-id="604ca-175">Care este metoda de plată implicită pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="604ca-176">Cheltuielile din categoria cheltuielilor trebuie să fie detaliate?</span><span class="sxs-lookup"><span data-stu-id="604ca-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="604ca-177">Care este contul principal implicit pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="604ca-178">Care este grupul implicit de impozitare pe vânzări pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="604ca-179">Sunt permise metode de plată suplimentare pentru categoria de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="604ca-180">Dacă sunt permise metode de plată suplimentare, care sunt acestea?</span><span class="sxs-lookup"><span data-stu-id="604ca-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="604ca-181">Există subcategorii în această categorie de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="604ca-182">Dacă sunt subcategorii, trebuie să luați și următoarele decizii:</span><span class="sxs-lookup"><span data-stu-id="604ca-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="604ca-183">Există vreuna dintre subcategoriile excluse din recuperarea impozitelor?</span><span class="sxs-lookup"><span data-stu-id="604ca-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="604ca-184">Care este grupul de taxe pe vânzări de articole din subcategorii?</span><span class="sxs-lookup"><span data-stu-id="604ca-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="604ca-185">Dacă categoria de cheltuieli este utilizată și în managementul de proiect și contabilitate, răspundeți la întrebările rămase.</span><span class="sxs-lookup"><span data-stu-id="604ca-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="604ca-186">În caz contrar, treceți la secțiunea următoare.</span><span class="sxs-lookup"><span data-stu-id="604ca-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="604ca-187">Ce conturi de costuri vor fi utilizate pentru următoarele cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="604ca-188">Cost</span><span class="sxs-lookup"><span data-stu-id="604ca-188">Cost</span></span>
    - <span data-ttu-id="604ca-189">Alocare stat de plată</span><span class="sxs-lookup"><span data-stu-id="604ca-189">Payroll allocation</span></span>
    - <span data-ttu-id="604ca-190">WIP-valoare de cost</span><span class="sxs-lookup"><span data-stu-id="604ca-190">WIP-cost value</span></span>
    - <span data-ttu-id="604ca-191">Cost-element</span><span class="sxs-lookup"><span data-stu-id="604ca-191">Cost-item</span></span>
    - <span data-ttu-id="604ca-192">WIP-valoare de cost-element</span><span class="sxs-lookup"><span data-stu-id="604ca-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="604ca-193">Pierderi acumulate</span><span class="sxs-lookup"><span data-stu-id="604ca-193">Accrued loss</span></span>
    - <span data-ttu-id="604ca-194">WIP-pierderi acumulate</span><span class="sxs-lookup"><span data-stu-id="604ca-194">WIP-accrued loss</span></span>

- <span data-ttu-id="604ca-195">Ce conturi de venituri vor fi utilizate pentru următoarele?</span><span class="sxs-lookup"><span data-stu-id="604ca-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="604ca-196">Venituri facturate</span><span class="sxs-lookup"><span data-stu-id="604ca-196">Invoiced revenue</span></span>
    - <span data-ttu-id="604ca-197">Venit acumulat-valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="604ca-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="604ca-198">WIP-valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="604ca-198">WIP-sales value</span></span>
    - <span data-ttu-id="604ca-199">Producție de venituri acumulate</span><span class="sxs-lookup"><span data-stu-id="604ca-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="604ca-200">WIP-producție</span><span class="sxs-lookup"><span data-stu-id="604ca-200">WIP-production</span></span>
    - <span data-ttu-id="604ca-201">Venituri acumulate-profit</span><span class="sxs-lookup"><span data-stu-id="604ca-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="604ca-202">WIP-profit</span><span class="sxs-lookup"><span data-stu-id="604ca-202">WIP-profit</span></span>
    - <span data-ttu-id="604ca-203">Venituri acumulate-abonament</span><span class="sxs-lookup"><span data-stu-id="604ca-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="604ca-204">WIP-abonament</span><span class="sxs-lookup"><span data-stu-id="604ca-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="604ca-205">Impozite</span><span class="sxs-lookup"><span data-stu-id="604ca-205">Taxes</span></span>

<span data-ttu-id="604ca-206">Pentru taxele legate de cheltuieli, trebuie să determinați ce este inclus sau activat în rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="604ca-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="604ca-207">**Decizii**</span><span class="sxs-lookup"><span data-stu-id="604ca-207">**Decisions:**</span></span>

- <span data-ttu-id="604ca-208">Impozitul pe vânzări este inclus în sumele cheltuielilor?</span><span class="sxs-lookup"><span data-stu-id="604ca-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="604ca-209">Ar trebui să se permită recuperarea impozitelor la cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="604ca-210">Când planificați registrul general, dacă ați decis să aplicați impozitul pe vânzări în SUA și să utilizați regulile fiscale, nu puteți activa recuperarea impozitului pe cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="604ca-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="604ca-211">(Pentru a aplica impozitul pe vânzări în SUA și a utiliza regulile fiscale, setați opțiunea **Aplicați regulile privind impozitarea pe vânzări** la **Da**.)</span><span class="sxs-lookup"><span data-stu-id="604ca-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="604ca-212">Politici</span><span class="sxs-lookup"><span data-stu-id="604ca-212">Policies</span></span>

<span data-ttu-id="604ca-213">Prin crearea politicilor de raportare a cheltuielilor, vă puteți ajuta organizația să economisească timp și bani atunci când angajații suportă cheltuieli în numele acesteia.</span><span class="sxs-lookup"><span data-stu-id="604ca-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="604ca-214">Politicile contribuie la garantarea faptului că angajații rămân în buget, furnizează toate informațiile necesare și cheltuiesc bani numai după cum au nevoie.</span><span class="sxs-lookup"><span data-stu-id="604ca-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="604ca-215">Trebuie să luați următoarele decizii pentru fiecare politică de raportare a cheltuielilor și pentru fiecare politică de aprobare a raportului de cheltuieli pe care o creați.</span><span class="sxs-lookup"><span data-stu-id="604ca-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="604ca-216">**Decizii**</span><span class="sxs-lookup"><span data-stu-id="604ca-216">**Decisions:**</span></span>

- <span data-ttu-id="604ca-217">Care este numele politicii?</span><span class="sxs-lookup"><span data-stu-id="604ca-217">What is the name of the policy?</span></span>
- <span data-ttu-id="604ca-218">Pentru ce este politica de cheltuieli?</span><span class="sxs-lookup"><span data-stu-id="604ca-218">What is the expense policy for?</span></span>
- <span data-ttu-id="604ca-219">Dacă ați decis anterior să activați cheltuielile între companii, la ce companii din organizația dvs. se va aplica această politică?</span><span class="sxs-lookup"><span data-stu-id="604ca-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="604ca-220">Când devine eficientă politica?</span><span class="sxs-lookup"><span data-stu-id="604ca-220">When does the policy become effective?</span></span>
- <span data-ttu-id="604ca-221">Când expiră politica?</span><span class="sxs-lookup"><span data-stu-id="604ca-221">When does the policy expire?</span></span>
- <span data-ttu-id="604ca-222">Care este regula politicii?</span><span class="sxs-lookup"><span data-stu-id="604ca-222">What is the policy rule?</span></span>
- <span data-ttu-id="604ca-223">Care este rezultatul regulii politicii?</span><span class="sxs-lookup"><span data-stu-id="604ca-223">What is the outcome of the policy rule?</span></span>
