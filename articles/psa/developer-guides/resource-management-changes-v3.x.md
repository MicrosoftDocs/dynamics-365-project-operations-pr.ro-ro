---
title: Modificări în gestionarea resurselor (Project Service Automation) 3.x
description: Acest subiect furnizează informații despre modificările din zona de gestionare a resurselor.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148658"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="af7f3-103">Modificări în gestionarea resurselor (Project Service Automation) 3.x</span><span class="sxs-lookup"><span data-stu-id="af7f3-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="af7f3-104">Secțiunile acestui subiect furnizează informații despre modificările efectuate în zona de gestionare a resurselor din Dynamics 365 Project Service Automation versiunea 3. x.</span><span class="sxs-lookup"><span data-stu-id="af7f3-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="af7f3-105">Estimări de proiect</span><span class="sxs-lookup"><span data-stu-id="af7f3-105">Project estimates</span></span>

<span data-ttu-id="af7f3-106">În loc să se bazeze pe entitatea **msdyn\_projecttask** (**Activitate proiect**), estimările proiectului se bazează pe entitatea **msdyn\_resourceassignment** (**Atribuire resurse**).</span><span class="sxs-lookup"><span data-stu-id="af7f3-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="af7f3-107">Atribuirile de resurse au devenit „sursa adevărului" pentru programarea și prețul sarcinilor.</span><span class="sxs-lookup"><span data-stu-id="af7f3-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="af7f3-108">Activități de linie</span><span class="sxs-lookup"><span data-stu-id="af7f3-108">Line tasks</span></span>

<span data-ttu-id="af7f3-109">În PSA 3. x, activitățile de linie sunt învechite (perimate).</span><span class="sxs-lookup"><span data-stu-id="af7f3-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="af7f3-110">Atribuirile indică acum întreaga activitate în locul activităților de linie.</span><span class="sxs-lookup"><span data-stu-id="af7f3-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="af7f3-111">Următorul exemplu arată cum este atribuită o activitate denumită „Activitate test” membrilor echipei A și B în versiunile anterioare de PSA și în PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="af7f3-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="af7f3-112">**Înainte de PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="af7f3-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="af7f3-113">Activitate test</span><span class="sxs-lookup"><span data-stu-id="af7f3-113">Test task</span></span>

        - <span data-ttu-id="af7f3-114">Activitate test – Activitate linie 1</span><span class="sxs-lookup"><span data-stu-id="af7f3-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="af7f3-115">Atribuire la A</span><span class="sxs-lookup"><span data-stu-id="af7f3-115">Assignment to A</span></span>

        - <span data-ttu-id="af7f3-116">Activitate test – Activitate linie 2</span><span class="sxs-lookup"><span data-stu-id="af7f3-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="af7f3-117">Atribuire la B</span><span class="sxs-lookup"><span data-stu-id="af7f3-117">Assignment to B</span></span>

- <span data-ttu-id="af7f3-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="af7f3-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="af7f3-119">Activitate test</span><span class="sxs-lookup"><span data-stu-id="af7f3-119">Test task</span></span>

        - <span data-ttu-id="af7f3-120">Atribuire la A</span><span class="sxs-lookup"><span data-stu-id="af7f3-120">Assignment to A</span></span>
        - <span data-ttu-id="af7f3-121">Atribuire la B</span><span class="sxs-lookup"><span data-stu-id="af7f3-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="af7f3-122">Atribuire neatribuită</span><span class="sxs-lookup"><span data-stu-id="af7f3-122">Unassigned assignment</span></span>

<span data-ttu-id="af7f3-123">În PSA 3.x, o atribuire neatribuită este o atribuire care este atribuită unui membru de echipă **NULL** și unei resurse **NULL**.</span><span class="sxs-lookup"><span data-stu-id="af7f3-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="af7f3-124">Atribuirile neatribuite pot apărea în câteva scenarii:</span><span class="sxs-lookup"><span data-stu-id="af7f3-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="af7f3-125">Dacă s-a creat o activitate, dar nu a fost încă atribuită niciunui membru al echipei, se creează întotdeauna o atribuire neatribuită.</span><span class="sxs-lookup"><span data-stu-id="af7f3-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="af7f3-126">Dacă sunt eliminate toate persoanele alocate pe o activitate, o atribuire neatribuit este re-creată pentru această activitate.</span><span class="sxs-lookup"><span data-stu-id="af7f3-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="af7f3-127">Programarea câmpurilor din entitatea Activitate proiect</span><span class="sxs-lookup"><span data-stu-id="af7f3-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="af7f3-128">Câmpurile din entitatea **msdyn\_projecttask** au fost perimate sau mutate la entitatea **msdyn\_resourceassignment**, sau acum se face referire la ele din entitatea **msdyn\_projectteam** (**Membru echipă proiect**).</span><span class="sxs-lookup"><span data-stu-id="af7f3-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="af7f3-129">Câmp perimat pe msdyn\_proiecttask (Activitate proiect)</span><span class="sxs-lookup"><span data-stu-id="af7f3-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="af7f3-130">Câmp nou pe msdyn\_resourarmistialocare (Atribuire resurse)</span><span class="sxs-lookup"><span data-stu-id="af7f3-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="af7f3-131">Comentariu</span><span class="sxs-lookup"><span data-stu-id="af7f3-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="af7f3-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="af7f3-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="af7f3-133">Niciunul</span><span class="sxs-lookup"><span data-stu-id="af7f3-133">None</span></span> | |
| <span data-ttu-id="af7f3-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="af7f3-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="af7f3-135">Niciunul</span><span class="sxs-lookup"><span data-stu-id="af7f3-135">None</span></span> | |
| <span data-ttu-id="af7f3-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="af7f3-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="af7f3-137">Niciunul</span><span class="sxs-lookup"><span data-stu-id="af7f3-137">None</span></span> | |
| <span data-ttu-id="af7f3-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="af7f3-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="af7f3-139">Niciunul</span><span class="sxs-lookup"><span data-stu-id="af7f3-139">None</span></span> | |
| <span data-ttu-id="af7f3-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="af7f3-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="af7f3-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="af7f3-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="af7f3-142">Formatul de structură de date JavaScript Object Notation (JSON) care este stocat în câmp a fost modificat.</span><span class="sxs-lookup"><span data-stu-id="af7f3-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="af7f3-143">Contur planificare</span><span class="sxs-lookup"><span data-stu-id="af7f3-143">Schedule contour</span></span>

<span data-ttu-id="af7f3-144">Conturul de planificare este stocat în câmpul **Lucrări planificate** (**msdyn\_plannedwork**) din fiecare entitate de **Atribuire resurse** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="af7f3-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="af7f3-145">Structură</span><span class="sxs-lookup"><span data-stu-id="af7f3-145">Structure</span></span>

<span data-ttu-id="af7f3-146">Noua structură a conturului planificării constă în felii de timp flexibile care sunt definite pentru fiecare zi a planificării.</span><span class="sxs-lookup"><span data-stu-id="af7f3-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="af7f3-147">Fiecare felie de timp are următoarele proprietăți:</span><span class="sxs-lookup"><span data-stu-id="af7f3-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="af7f3-148">**Start** - Începutul orelor de lucru pentru a ziua respectivă, în conformitate cu calendarul proiectului.</span><span class="sxs-lookup"><span data-stu-id="af7f3-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="af7f3-149">**Sfârșit** - Finalul orelor de lucru pentru a ziua respectivă, în conformitate cu calendarul proiectului.</span><span class="sxs-lookup"><span data-stu-id="af7f3-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="af7f3-150">**Ore** – Numărul de ore atribuite în ziua respectivă.</span><span class="sxs-lookup"><span data-stu-id="af7f3-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="af7f3-151">**Exemplu**</span><span class="sxs-lookup"><span data-stu-id="af7f3-151">**Example**</span></span>

<span data-ttu-id="af7f3-152">Acest exemplu utilizează un calendar de proiect în care ziua de lucru este de la 09:00 la 17:00 pe fusul orar UTC-8.</span><span class="sxs-lookup"><span data-stu-id="af7f3-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="af7f3-153">Planificarea automată și planificarea manuală</span><span class="sxs-lookup"><span data-stu-id="af7f3-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="af7f3-154">Dacă o activitate este planificată automat, orele sunt încărcate frontal și durata activității poate fi redusă.</span><span class="sxs-lookup"><span data-stu-id="af7f3-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="af7f3-155">**Exemplu**</span><span class="sxs-lookup"><span data-stu-id="af7f3-155">**Example**</span></span>

<span data-ttu-id="af7f3-156">Următoarea sarcină este planificată automat timp de 18 ore pe trei zile (3 decembrie, 2018, până la 5 decembrie 2018).</span><span class="sxs-lookup"><span data-stu-id="af7f3-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="af7f3-157">Dacă o activitate este planificată manual, orele sunt distribuite uniform la toate datele.</span><span class="sxs-lookup"><span data-stu-id="af7f3-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="af7f3-158">**Exemplu**</span><span class="sxs-lookup"><span data-stu-id="af7f3-158">**Example**</span></span>

<span data-ttu-id="af7f3-159">Următoarea sarcină este planificată manual timp de 18 ore pe trei zile (3 decembrie, 2018, până la 5 decembrie 2018).</span><span class="sxs-lookup"><span data-stu-id="af7f3-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="af7f3-160">Unitate de atribuire</span><span class="sxs-lookup"><span data-stu-id="af7f3-160">Assignment unit</span></span>

<span data-ttu-id="af7f3-161">Unitatea de atribuire a fost perimată în PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="af7f3-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="af7f3-162">Orele de efort de activitate sunt acum împărțite în mod egal, pe zi, între toate resursele alocate.</span><span class="sxs-lookup"><span data-stu-id="af7f3-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="af7f3-163">**Exemplu**</span><span class="sxs-lookup"><span data-stu-id="af7f3-163">**Example**</span></span>

<span data-ttu-id="af7f3-164">În acest exemplu, pentru sarcină sunt atribuite două resurse și este planificată automat pentru 36 de ore pe trei zile (3 decembrie, 2018, la 5 decembrie 2018).</span><span class="sxs-lookup"><span data-stu-id="af7f3-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="af7f3-165">Atribuire 1:</span><span class="sxs-lookup"><span data-stu-id="af7f3-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="af7f3-166">Atribuire 2:</span><span class="sxs-lookup"><span data-stu-id="af7f3-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="af7f3-167">Dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="af7f3-167">Pricing dimensions</span></span>

<span data-ttu-id="af7f3-168">În PSA 3.x, câmpurile de dimensiune a prețului specifice resurselor (cum ar fi **Rol** și **Unitate organizațională**) au fost eliminate din entitatea **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="af7f3-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="af7f3-169">Aceste câmpuri pot fi preluate de la membrul echipei de proiect corespunzător (**msdyn\_proiectteam**) al atribuirii resursei **(msdyn\_resourceassignment**) când sunt generate estimările de proiect.</span><span class="sxs-lookup"><span data-stu-id="af7f3-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="af7f3-170">Un câmp nou, **msdyn\_organizationalunit**, a fost adăugat la entitatea **msdyn\_projectteam** .</span><span class="sxs-lookup"><span data-stu-id="af7f3-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="af7f3-171">Câmp perimat pe msdyn\_proiecttask (Activitate proiect)</span><span class="sxs-lookup"><span data-stu-id="af7f3-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="af7f3-172">Câmp din msdyn\_projectteam (membru al echipei de proiect) care este utilizat în schimb</span><span class="sxs-lookup"><span data-stu-id="af7f3-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="af7f3-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="af7f3-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="af7f3-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="af7f3-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="af7f3-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="af7f3-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="af7f3-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="af7f3-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="af7f3-177">Contururi</span><span class="sxs-lookup"><span data-stu-id="af7f3-177">Contours</span></span>

<span data-ttu-id="af7f3-178">Câmpurile de contur de stabilire și de estimare a prețurilor au fost perimate pe entitatea **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="af7f3-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="af7f3-179">Acestea au fost mutate în entitatea **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="af7f3-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="af7f3-180">Câmp perimat pe msdyn\_proiecttask (Activitate proiect)</span><span class="sxs-lookup"><span data-stu-id="af7f3-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="af7f3-181">Câmp nou pe msdyn\_resourarmistialocare (Atribuire resurse)</span><span class="sxs-lookup"><span data-stu-id="af7f3-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="af7f3-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="af7f3-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="af7f3-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="af7f3-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="af7f3-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="af7f3-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="af7f3-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="af7f3-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="af7f3-186">Următoarele câmpuri au fost adăugate la entitatea **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="af7f3-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="af7f3-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="af7f3-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="af7f3-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="af7f3-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="af7f3-189">Următoarele câmpuri pentru costurile și vânzările planificate, reale și rămase sunt neschimbate pe entitatea de **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="af7f3-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="af7f3-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="af7f3-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="af7f3-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="af7f3-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="af7f3-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="af7f3-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="af7f3-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="af7f3-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="af7f3-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="af7f3-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="af7f3-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="af7f3-195">msdyn\_remainingsales</span></span>
