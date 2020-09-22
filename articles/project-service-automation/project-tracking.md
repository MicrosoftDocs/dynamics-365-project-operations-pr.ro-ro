---
title: Progresul și costurile în curs ale proiectului
description: Acest subiect furnizează informații despre să urmăriți progresul proiectului și consumul de costuri.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754804"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="1cb70-103">Progresul și costurile în curs ale proiectului</span><span class="sxs-lookup"><span data-stu-id="1cb70-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1cb70-104">Necesitatea de a urmări progresele în raport cu o planificare variază în funcție de industrie.</span><span class="sxs-lookup"><span data-stu-id="1cb70-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="1cb70-105">Unele industrii urmăresc la un nivel granular, în timp ce alte industrii urmăresc la un nivel mai înalt.</span><span class="sxs-lookup"><span data-stu-id="1cb70-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="1cb70-106">Acest subiect arată cum să planificați pentru a îndeplini cerințele organizației dvs.</span><span class="sxs-lookup"><span data-stu-id="1cb70-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="1cb70-107">Vizualizarea Urmărire efort</span><span class="sxs-lookup"><span data-stu-id="1cb70-107">Effort tracking view</span></span>

<span data-ttu-id="1cb70-108">Vizualizarea **Urmărire efort** urmărește progresul activităților în planificare.</span><span class="sxs-lookup"><span data-stu-id="1cb70-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="1cb70-109">Aceasta compară orele de efort real care au fost petrecute pe o activitate cu orele de efort planificate pentru acea activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="1cb70-110">PSA utilizează următoarele formule pentru a calcula măsurătorile de urmărire:</span><span class="sxs-lookup"><span data-stu-id="1cb70-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="1cb70-111">Procentaj de progres = efort efectiv cheltuit până în prezent ÷ efortul planificat pentru activitate</span><span class="sxs-lookup"><span data-stu-id="1cb70-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="1cb70-112">Estimare pentru a finaliza (ETC) = efortul planificat - efortul real petrecut până în prezent</span><span class="sxs-lookup"><span data-stu-id="1cb70-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="1cb70-113">Estimare la (EAC) finalizat = efortul rămas + efortul real petrecut până în prezent</span><span class="sxs-lookup"><span data-stu-id="1cb70-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="1cb70-114">Varianța preconizată a efortului = efortul planificat – EAC</span><span class="sxs-lookup"><span data-stu-id="1cb70-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="1cb70-115">PSA prezintă o proiecție a varianței efortului pe activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="1cb70-116">În cazul în care EAC este mai mult decât efortul planificat, activitatea este proiectată să dureze mai mult timp decât a fost planificat inițial.</span><span class="sxs-lookup"><span data-stu-id="1cb70-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="1cb70-117">Prin urmare, este în urma planificării.</span><span class="sxs-lookup"><span data-stu-id="1cb70-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="1cb70-118">În cazul în care EAC este mai puțin decât efortul planificat, activitatea este proiectată să dureze mai puțin timp decât a fost planificat inițial.</span><span class="sxs-lookup"><span data-stu-id="1cb70-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="1cb70-119">Prin urmare, este înaintea planificării.</span><span class="sxs-lookup"><span data-stu-id="1cb70-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="1cb70-120">Reproiectarea efortului</span><span class="sxs-lookup"><span data-stu-id="1cb70-120">Re-projecting effort</span></span>

<span data-ttu-id="1cb70-121">Este un lucru obișnuit ca un manager de proiect să revizuiască estimările inițiale ale unei activități.</span><span class="sxs-lookup"><span data-stu-id="1cb70-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="1cb70-122">Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind stadiul actual al proiectului.</span><span class="sxs-lookup"><span data-stu-id="1cb70-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="1cb70-123">Cu toate acestea, nu recomandăm ca managerii de proiect să modifice numerele de referință, pentru că referința proiectului reprezintă sursa stabilită de adevăr pentru planificarea proiectului și estimarea de cost și toți participanții direct interesați ai proiectului s-au pus de acord în această privință.</span><span class="sxs-lookup"><span data-stu-id="1cb70-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="1cb70-124">Există două modalități prin care un manager de proiect poate reproiecta efortul asupra activităților:</span><span class="sxs-lookup"><span data-stu-id="1cb70-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="1cb70-125">Suprascrie ETC-ul implicit cu o nouă estimare a efortului efectiv rămase pe activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="1cb70-126">Suprascrie procentul progresului implicit cu o nouă estimare a progresului real asupra activității.</span><span class="sxs-lookup"><span data-stu-id="1cb70-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="1cb70-127">Fiecare dintre aceste abordări cauzează o recalculare a activității ETC, EAC și procentajul de progres, precum și varianța de efort proiectată pentru o activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="1cb70-128">EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.</span><span class="sxs-lookup"><span data-stu-id="1cb70-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="1cb70-129">Reproiectarea efortului asupra activităților rezumat</span><span class="sxs-lookup"><span data-stu-id="1cb70-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="1cb70-130">Efortul pe sarcini rezumat sau sarcini container poate fi reproiectat.</span><span class="sxs-lookup"><span data-stu-id="1cb70-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="1cb70-131">Indiferent dacă utilizatorul reproiectează utilizând efortul rămas sau procentul de progres pe activitățile rezumat, începe următorul set de calcule:</span><span class="sxs-lookup"><span data-stu-id="1cb70-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="1cb70-132">Se calculează EAC, ETC. și procentajul de progres al activității.</span><span class="sxs-lookup"><span data-stu-id="1cb70-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="1cb70-133">Noul EAC este distribuit în jos, activităților secundare în aceeași proporție cum a fost EAC-ul original pe activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="1cb70-134">Se calculează noul EAC pe fiecare dintre sarcinile individuale până la activitățile de nod frunză.</span><span class="sxs-lookup"><span data-stu-id="1cb70-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="1cb70-135">Activitățile secundare afectate până la nodurile frunză au ETC și procentajul de progres recalculate pe baza valorii EAC.</span><span class="sxs-lookup"><span data-stu-id="1cb70-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="1cb70-136">Acest lucru duce la o nouă proiecție pentru varianța efortului de activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="1cb70-137">Sunt recalculate EAC-uri de sarcini rezumat până la nodul rădăcină.</span><span class="sxs-lookup"><span data-stu-id="1cb70-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="1cb70-138">Vizualizare urmărire cost</span><span class="sxs-lookup"><span data-stu-id="1cb70-138">Cost tracking view</span></span> 

<span data-ttu-id="1cb70-139">Vizualizarea **Urmărirea costurilor** compară costul real care a fost cheltuit pe o activitate cu costul planificat pentru o activitate.</span><span class="sxs-lookup"><span data-stu-id="1cb70-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="1cb70-140">Această vizualizare afișează numai costurile cu munca și nu include costurile din estimările de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="1cb70-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="1cb70-141">PSA utilizează următoarele formule pentru a calcula măsurătorile de urmărire:</span><span class="sxs-lookup"><span data-stu-id="1cb70-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="1cb70-142">Procent din costul consumat = cost real cheltuit până în prezent ÷ costul planificat pentru activitate</span><span class="sxs-lookup"><span data-stu-id="1cb70-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="1cb70-143">Cost pentru a finaliza (CTC) = cost planificat - cost real cheltuit până în prezent</span><span class="sxs-lookup"><span data-stu-id="1cb70-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="1cb70-144">EAC = CTC + costul real cheltuit până în prezent</span><span class="sxs-lookup"><span data-stu-id="1cb70-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="1cb70-145">Varianța costurilor proiectate = cost planificat – EAC</span><span class="sxs-lookup"><span data-stu-id="1cb70-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="1cb70-146">Pe activitate este afișată o proiecție a variației de cost.</span><span class="sxs-lookup"><span data-stu-id="1cb70-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="1cb70-147">În cazul în care EAC este mai mult decât costul planificat, activitatea este proiectată să coste mai mult timp decât a fost planificat inițial.</span><span class="sxs-lookup"><span data-stu-id="1cb70-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="1cb70-148">Prin urmare, este în tendință peste buget.</span><span class="sxs-lookup"><span data-stu-id="1cb70-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="1cb70-149">În cazul în care EAC este mai puțin decât costul planificat, activitatea este proiectată să coste mai puțin decât a fost planificat inițial.</span><span class="sxs-lookup"><span data-stu-id="1cb70-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="1cb70-150">Prin urmare, este în tendință sub buget.</span><span class="sxs-lookup"><span data-stu-id="1cb70-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="1cb70-151">Reproiectarea costului a managerului de proiect</span><span class="sxs-lookup"><span data-stu-id="1cb70-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="1cb70-152">Când efortul este reproiectat, CTC, EAC, procentul de cost consumat și varianța costurilor proiectate sunt recalculate în vizualizarea de **Urmărirea costurilor**.</span><span class="sxs-lookup"><span data-stu-id="1cb70-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="1cb70-153">Rezumat stare de proiect</span><span class="sxs-lookup"><span data-stu-id="1cb70-153">Project status summary</span></span>

<span data-ttu-id="1cb70-154">Urmărirea datelor din vizualizările de **Urmărire a efortului** și **Urmărirea costului** arată progresul și consumul de cost la nodul rădăcină de proiect, activități de sinteză și niveluri de activități nod frunză.</span><span class="sxs-lookup"><span data-stu-id="1cb70-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="1cb70-155">Secțiunea **Stare** a paginii **Entitate de proiect** afișează un rezumat al stării nivelului de proiect.</span><span class="sxs-lookup"><span data-stu-id="1cb70-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="1cb70-156">Câmpuri rezumat stare</span><span class="sxs-lookup"><span data-stu-id="1cb70-156">Status summary fields</span></span>

<span data-ttu-id="1cb70-157">Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="1cb70-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="1cb70-158">Acesta utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere.</span><span class="sxs-lookup"><span data-stu-id="1cb70-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="1cb70-159">Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut.</span><span class="sxs-lookup"><span data-stu-id="1cb70-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="1cb70-160">Câmpul **Stare actualizată pe** nu este editabil și valoarea este un marcaj temporal care indică când a fost actualizată starea ultima dată.</span><span class="sxs-lookup"><span data-stu-id="1cb70-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="1cb70-161">Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din data de urmărire.</span><span class="sxs-lookup"><span data-stu-id="1cb70-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="1cb70-162">Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, puteți seta aceste câmpuri la **Avans.**</span><span class="sxs-lookup"><span data-stu-id="1cb70-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="1cb70-163">Când programul și varianța costului pentru nodul rădăcină sunt negative, le puteți seta în **În urmă**.</span><span class="sxs-lookup"><span data-stu-id="1cb70-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
