---
title: Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare
description: Acest subiect oferă informații și exemple pentru utilizarea API-urilor de Planificare.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116812"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="56802-103">Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare</span><span class="sxs-lookup"><span data-stu-id="56802-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="56802-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="56802-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="56802-105">O parte sau toate funcționalitățile notate în acest subiect sunt disponibile ca parte a ediției de previzualizare.</span><span class="sxs-lookup"><span data-stu-id="56802-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="56802-106">Conținutul și funcționalitățile pot fi modificate.</span><span class="sxs-lookup"><span data-stu-id="56802-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="56802-107">Entități de planificare</span><span class="sxs-lookup"><span data-stu-id="56802-107">Scheduling entities</span></span>

<span data-ttu-id="56802-108">API-urile de programare oferă posibilitatea de a efectua operațiuni de creare, actualizare și ștergere cu **Entități de planificare**.</span><span class="sxs-lookup"><span data-stu-id="56802-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="56802-109">Aceste entități sunt gestionate prin intermediul motorului de planificare în Proiect pentru web.</span><span class="sxs-lookup"><span data-stu-id="56802-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="56802-110">Creați, actualizați și ștergeți operațiuni cu **Entități de planificare** au fost restricționate în versiuni mai timpurii ale Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="56802-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="56802-111">Următorul tabel oferă o listă completă a **Entităților de planificare**.</span><span class="sxs-lookup"><span data-stu-id="56802-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="56802-112">Nume de entitate</span><span class="sxs-lookup"><span data-stu-id="56802-112">Entity name</span></span>  | <span data-ttu-id="56802-113">Numele logic al entității</span><span class="sxs-lookup"><span data-stu-id="56802-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="56802-114">Project</span><span class="sxs-lookup"><span data-stu-id="56802-114">Project</span></span> | <span data-ttu-id="56802-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="56802-115">msdyn_project</span></span> |
| <span data-ttu-id="56802-116">Activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-116">Project Task</span></span>  | <span data-ttu-id="56802-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="56802-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="56802-118">Dependență de activitate proiect</span><span class="sxs-lookup"><span data-stu-id="56802-118">Project Task Dependency</span></span>  | <span data-ttu-id="56802-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="56802-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="56802-120">Atribuire de resurse</span><span class="sxs-lookup"><span data-stu-id="56802-120">Resource Assignment</span></span> | <span data-ttu-id="56802-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="56802-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="56802-122">Pachet de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-122">Project Bucket</span></span>  | <span data-ttu-id="56802-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="56802-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="56802-124">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-124">Project Team Member</span></span> | <span data-ttu-id="56802-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="56802-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="56802-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="56802-126">OperationSet</span></span>

<span data-ttu-id="56802-127">OperationSet este un model de unitate de lucru care poate fi utilizat atunci când mai multe cereri care afectează planificarea trebuie procesate în cadrul unei tranzacții.</span><span class="sxs-lookup"><span data-stu-id="56802-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="56802-128">Planificați API-urile</span><span class="sxs-lookup"><span data-stu-id="56802-128">Schedule APIs</span></span>

<span data-ttu-id="56802-129">Următoarea este o listă a API-urilor curente de planificare.</span><span class="sxs-lookup"><span data-stu-id="56802-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="56802-130">**msdyn_CreateProjectV1**: Acest API poate fi folosit pentru a crea un proiect.</span><span class="sxs-lookup"><span data-stu-id="56802-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="56802-131">Proiectul și pachetul de proiect implicit sunt create imediat.</span><span class="sxs-lookup"><span data-stu-id="56802-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="56802-132">**msdyn_CreateTeamMemberV1**: Acest API poate fi utilizat pentru a crea un membru al echipei de proiect.</span><span class="sxs-lookup"><span data-stu-id="56802-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="56802-133">Înregistrarea membrilor echipei este creată imediat.</span><span class="sxs-lookup"><span data-stu-id="56802-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="56802-134">**msdyn_CreateOperationSetV1**: Acest API poate fi utilizat pentru a programa mai multe solicitări care trebuie efectuate în cadrul unei tranzacții.</span><span class="sxs-lookup"><span data-stu-id="56802-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="56802-135">**msdyn_PSSCreateV1**: Acest API poate fi utilizat pentru a crea o entitate.</span><span class="sxs-lookup"><span data-stu-id="56802-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="56802-136">Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de creare.</span><span class="sxs-lookup"><span data-stu-id="56802-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="56802-137">**msdyn_PSSUpdateV1**: acest API poate fi utilizat pentru a actualiza o entitate.</span><span class="sxs-lookup"><span data-stu-id="56802-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="56802-138">Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de actualizare.</span><span class="sxs-lookup"><span data-stu-id="56802-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="56802-139">**msdyn_PSSDeleteV1**: acest API poate fi utilizat pentru a șterge o entitate.</span><span class="sxs-lookup"><span data-stu-id="56802-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="56802-140">Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de ștergere.</span><span class="sxs-lookup"><span data-stu-id="56802-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="56802-141">**msdyn_ExecuteOperationSetV1**: Acest API este utilizat pentru a executa toate operațiunile din cadrul setului de operații date.</span><span class="sxs-lookup"><span data-stu-id="56802-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="56802-142">Utilizarea API-urilor de programare cu OperationSet</span><span class="sxs-lookup"><span data-stu-id="56802-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="56802-143">Pentru că înregistrează cu amândouă **CreateProjectV1** și **CreateTeamMemberV1** sunt create imediat, aceste API-uri nu pot fi utilizate în **OperationSet** direct.</span><span class="sxs-lookup"><span data-stu-id="56802-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="56802-144">Cu toate acestea, puteți utiliza API-ul pentru a crea înregistrări necesare, pentru a crea un **OperationSet**, și apoi utilizați aceste înregistrări pre-create în **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="56802-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="56802-145">Operațiuni acceptate</span><span class="sxs-lookup"><span data-stu-id="56802-145">Supported operations</span></span>

| <span data-ttu-id="56802-146">Entitate de planificare</span><span class="sxs-lookup"><span data-stu-id="56802-146">Scheduling entity</span></span> | <span data-ttu-id="56802-147">Creați</span><span class="sxs-lookup"><span data-stu-id="56802-147">Create</span></span> | <span data-ttu-id="56802-148">Actualizați</span><span class="sxs-lookup"><span data-stu-id="56802-148">Update</span></span> | <span data-ttu-id="56802-149">Delete</span><span class="sxs-lookup"><span data-stu-id="56802-149">Delete</span></span> | <span data-ttu-id="56802-150">Considerații importante</span><span class="sxs-lookup"><span data-stu-id="56802-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="56802-151">Activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-151">Project task</span></span> | <span data-ttu-id="56802-152">Da</span><span class="sxs-lookup"><span data-stu-id="56802-152">Yes</span></span> | <span data-ttu-id="56802-153">Da</span><span class="sxs-lookup"><span data-stu-id="56802-153">Yes</span></span> | <span data-ttu-id="56802-154">Da</span><span class="sxs-lookup"><span data-stu-id="56802-154">Yes</span></span> | <span data-ttu-id="56802-155">Fără</span><span class="sxs-lookup"><span data-stu-id="56802-155">None</span></span> |
| <span data-ttu-id="56802-156">Dependență de activitate proiect</span><span class="sxs-lookup"><span data-stu-id="56802-156">Project task dependency</span></span> | <span data-ttu-id="56802-157">Da</span><span class="sxs-lookup"><span data-stu-id="56802-157">Yes</span></span> | <span data-ttu-id="56802-158">Da</span><span class="sxs-lookup"><span data-stu-id="56802-158">Yes</span></span> | | <span data-ttu-id="56802-159">Înregistrările de dependență ale sarcinii de proiect nu sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="56802-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="56802-160">În schimb, o înregistrare veche poate fi ștearsă și o nouă înregistrare poate fi creată.</span><span class="sxs-lookup"><span data-stu-id="56802-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="56802-161">Atribuire de resurse</span><span class="sxs-lookup"><span data-stu-id="56802-161">Resource assignment</span></span> | <span data-ttu-id="56802-162">Da</span><span class="sxs-lookup"><span data-stu-id="56802-162">Yes</span></span> | <span data-ttu-id="56802-163">Da</span><span class="sxs-lookup"><span data-stu-id="56802-163">Yes</span></span> | | <span data-ttu-id="56802-164">Operațiile cu următoarele câmpuri nu sunt acceptate: **BookableResourceID**, **Efort**, **EfortCompletat**, **EfortRămânând**, și **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="56802-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="56802-165">Înregistrările de alocare a resurselor nu sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="56802-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="56802-166">În schimb, înregistrarea veche poate fi ștearsă și o nouă înregistrare poate fi creată.</span><span class="sxs-lookup"><span data-stu-id="56802-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="56802-167">Pachet de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-167">Project bucket</span></span> | <span data-ttu-id="56802-168">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56802-168">N/A</span></span> | <span data-ttu-id="56802-169">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56802-169">N/A</span></span> | <span data-ttu-id="56802-170">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56802-170">N/A</span></span> | <span data-ttu-id="56802-171">Pachetul implicit este creat folosind API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="56802-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="56802-172">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-172">Project team member</span></span> | <span data-ttu-id="56802-173">Da</span><span class="sxs-lookup"><span data-stu-id="56802-173">Yes</span></span> | <span data-ttu-id="56802-174">Da</span><span class="sxs-lookup"><span data-stu-id="56802-174">Yes</span></span> | <span data-ttu-id="56802-175">Da</span><span class="sxs-lookup"><span data-stu-id="56802-175">Yes</span></span> | <span data-ttu-id="56802-176">Pentru operația de creare, utilizați API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="56802-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="56802-177">Project</span><span class="sxs-lookup"><span data-stu-id="56802-177">Project</span></span> | <span data-ttu-id="56802-178">Da</span><span class="sxs-lookup"><span data-stu-id="56802-178">Yes</span></span> | <span data-ttu-id="56802-179">Da</span><span class="sxs-lookup"><span data-stu-id="56802-179">Yes</span></span> | <span data-ttu-id="56802-180">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56802-180">N/A</span></span> | <span data-ttu-id="56802-181">Operațiunile cu următoarele câmpuri nu sunt acceptate: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Efort**, **EfortCompletat**, **EfortRămânând**, **Progres**, **Finalizare**, **TaskEarliestStart** și **Durată**.</span><span class="sxs-lookup"><span data-stu-id="56802-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="56802-182">Aceste API-uri pot fi apelate cu obiecte de entitate care includ câmpuri personalizate.</span><span class="sxs-lookup"><span data-stu-id="56802-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="56802-183">Proprietatea ID este opțională.</span><span class="sxs-lookup"><span data-stu-id="56802-183">The ID property is optional.</span></span> <span data-ttu-id="56802-184">Dacă este furnizat, sistemul încearcă să-l folosească și aruncă o excepție dacă nu poate fi folosit.</span><span class="sxs-lookup"><span data-stu-id="56802-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="56802-185">Dacă nu este furnizat, sistemul îl va genera.</span><span class="sxs-lookup"><span data-stu-id="56802-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="56802-186">Câmpuri restricționate</span><span class="sxs-lookup"><span data-stu-id="56802-186">Restricted fields</span></span>

<span data-ttu-id="56802-187">Următoarele tabele definesc câmpurile care sunt restricționate din **Creare** și **Editare.**</span><span class="sxs-lookup"><span data-stu-id="56802-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="56802-188">Activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-188">Project task</span></span>

| <span data-ttu-id="56802-189">**Nume logic**</span><span class="sxs-lookup"><span data-stu-id="56802-189">**Logical name**</span></span>                       | <span data-ttu-id="56802-190">**Poate crea**</span><span class="sxs-lookup"><span data-stu-id="56802-190">**Can create**</span></span> | <span data-ttu-id="56802-191">**Poate edita**</span><span class="sxs-lookup"><span data-stu-id="56802-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="56802-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="56802-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="56802-193">nu</span><span class="sxs-lookup"><span data-stu-id="56802-193">no</span></span>             | <span data-ttu-id="56802-194">nu</span><span class="sxs-lookup"><span data-stu-id="56802-194">no</span></span>               |
| <span data-ttu-id="56802-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="56802-196">nu</span><span class="sxs-lookup"><span data-stu-id="56802-196">no</span></span>             | <span data-ttu-id="56802-197">nu</span><span class="sxs-lookup"><span data-stu-id="56802-197">no</span></span>               |
| <span data-ttu-id="56802-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="56802-198">msdyn_actualend</span></span>                        | <span data-ttu-id="56802-199">nu</span><span class="sxs-lookup"><span data-stu-id="56802-199">no</span></span>             | <span data-ttu-id="56802-200">nu</span><span class="sxs-lookup"><span data-stu-id="56802-200">no</span></span>               |
| <span data-ttu-id="56802-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="56802-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="56802-202">nu</span><span class="sxs-lookup"><span data-stu-id="56802-202">no</span></span>             | <span data-ttu-id="56802-203">nu</span><span class="sxs-lookup"><span data-stu-id="56802-203">no</span></span>               |
| <span data-ttu-id="56802-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="56802-205">nu</span><span class="sxs-lookup"><span data-stu-id="56802-205">no</span></span>             | <span data-ttu-id="56802-206">nu</span><span class="sxs-lookup"><span data-stu-id="56802-206">no</span></span>               |
| <span data-ttu-id="56802-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="56802-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="56802-208">nu</span><span class="sxs-lookup"><span data-stu-id="56802-208">no</span></span>             | <span data-ttu-id="56802-209">nu</span><span class="sxs-lookup"><span data-stu-id="56802-209">no</span></span>               |
| <span data-ttu-id="56802-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="56802-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="56802-211">nu</span><span class="sxs-lookup"><span data-stu-id="56802-211">no</span></span>             | <span data-ttu-id="56802-212">nu</span><span class="sxs-lookup"><span data-stu-id="56802-212">no</span></span>               |
| <span data-ttu-id="56802-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="56802-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="56802-214">nu</span><span class="sxs-lookup"><span data-stu-id="56802-214">no</span></span>             | <span data-ttu-id="56802-215">nu</span><span class="sxs-lookup"><span data-stu-id="56802-215">no</span></span>               |
| <span data-ttu-id="56802-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="56802-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="56802-217">nu</span><span class="sxs-lookup"><span data-stu-id="56802-217">no</span></span>             | <span data-ttu-id="56802-218">nu</span><span class="sxs-lookup"><span data-stu-id="56802-218">no</span></span>               |
| <span data-ttu-id="56802-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="56802-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="56802-220">nu</span><span class="sxs-lookup"><span data-stu-id="56802-220">no</span></span>             | <span data-ttu-id="56802-221">nu</span><span class="sxs-lookup"><span data-stu-id="56802-221">no</span></span>               |
| <span data-ttu-id="56802-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="56802-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="56802-223">nu</span><span class="sxs-lookup"><span data-stu-id="56802-223">no</span></span>             | <span data-ttu-id="56802-224">nu</span><span class="sxs-lookup"><span data-stu-id="56802-224">no</span></span>               |
| <span data-ttu-id="56802-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="56802-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="56802-226">nu</span><span class="sxs-lookup"><span data-stu-id="56802-226">no</span></span>             | <span data-ttu-id="56802-227">nu</span><span class="sxs-lookup"><span data-stu-id="56802-227">no</span></span>               |
| <span data-ttu-id="56802-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="56802-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="56802-229">nu</span><span class="sxs-lookup"><span data-stu-id="56802-229">no</span></span>             | <span data-ttu-id="56802-230">nu</span><span class="sxs-lookup"><span data-stu-id="56802-230">no</span></span>               |
| <span data-ttu-id="56802-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="56802-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="56802-232">nu</span><span class="sxs-lookup"><span data-stu-id="56802-232">no</span></span>             | <span data-ttu-id="56802-233">nu</span><span class="sxs-lookup"><span data-stu-id="56802-233">no</span></span>               |
| <span data-ttu-id="56802-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="56802-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="56802-235">nu</span><span class="sxs-lookup"><span data-stu-id="56802-235">no</span></span>             | <span data-ttu-id="56802-236">nu</span><span class="sxs-lookup"><span data-stu-id="56802-236">no</span></span>               |
| <span data-ttu-id="56802-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="56802-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="56802-238">nu</span><span class="sxs-lookup"><span data-stu-id="56802-238">no</span></span>             | <span data-ttu-id="56802-239">nu</span><span class="sxs-lookup"><span data-stu-id="56802-239">no</span></span>               |
| <span data-ttu-id="56802-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="56802-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="56802-241">nu</span><span class="sxs-lookup"><span data-stu-id="56802-241">no</span></span>             | <span data-ttu-id="56802-242">nu</span><span class="sxs-lookup"><span data-stu-id="56802-242">no</span></span>               |
| <span data-ttu-id="56802-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="56802-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="56802-244">nu</span><span class="sxs-lookup"><span data-stu-id="56802-244">no</span></span>             | <span data-ttu-id="56802-245">nu</span><span class="sxs-lookup"><span data-stu-id="56802-245">no</span></span>               |
| <span data-ttu-id="56802-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="56802-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="56802-247">nu</span><span class="sxs-lookup"><span data-stu-id="56802-247">no</span></span>             | <span data-ttu-id="56802-248">nu</span><span class="sxs-lookup"><span data-stu-id="56802-248">no</span></span>               |
| <span data-ttu-id="56802-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="56802-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="56802-250">nu</span><span class="sxs-lookup"><span data-stu-id="56802-250">no</span></span>             | <span data-ttu-id="56802-251">nu</span><span class="sxs-lookup"><span data-stu-id="56802-251">no</span></span>               |
| <span data-ttu-id="56802-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="56802-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="56802-253">nu</span><span class="sxs-lookup"><span data-stu-id="56802-253">no</span></span>             | <span data-ttu-id="56802-254">nu</span><span class="sxs-lookup"><span data-stu-id="56802-254">no</span></span>               |
| <span data-ttu-id="56802-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="56802-256">nu</span><span class="sxs-lookup"><span data-stu-id="56802-256">no</span></span>             | <span data-ttu-id="56802-257">nu</span><span class="sxs-lookup"><span data-stu-id="56802-257">no</span></span>               |
| <span data-ttu-id="56802-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="56802-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="56802-259">nu</span><span class="sxs-lookup"><span data-stu-id="56802-259">no</span></span>             | <span data-ttu-id="56802-260">nu</span><span class="sxs-lookup"><span data-stu-id="56802-260">no</span></span>               |
| <span data-ttu-id="56802-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="56802-262">nu</span><span class="sxs-lookup"><span data-stu-id="56802-262">no</span></span>             | <span data-ttu-id="56802-263">nu</span><span class="sxs-lookup"><span data-stu-id="56802-263">no</span></span>               |
| <span data-ttu-id="56802-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="56802-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="56802-265">nu</span><span class="sxs-lookup"><span data-stu-id="56802-265">no</span></span>             | <span data-ttu-id="56802-266">nu</span><span class="sxs-lookup"><span data-stu-id="56802-266">no</span></span>               |
| <span data-ttu-id="56802-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="56802-267">msdyn_progress</span></span>                         | <span data-ttu-id="56802-268">nu</span><span class="sxs-lookup"><span data-stu-id="56802-268">no</span></span>             | <span data-ttu-id="56802-269">nu (da pentru P4W)</span><span class="sxs-lookup"><span data-stu-id="56802-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="56802-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="56802-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="56802-271">nu</span><span class="sxs-lookup"><span data-stu-id="56802-271">no</span></span>             | <span data-ttu-id="56802-272">nu</span><span class="sxs-lookup"><span data-stu-id="56802-272">no</span></span>               |
| <span data-ttu-id="56802-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="56802-274">nu</span><span class="sxs-lookup"><span data-stu-id="56802-274">no</span></span>             | <span data-ttu-id="56802-275">nu</span><span class="sxs-lookup"><span data-stu-id="56802-275">no</span></span>               |
| <span data-ttu-id="56802-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="56802-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="56802-277">nu</span><span class="sxs-lookup"><span data-stu-id="56802-277">no</span></span>             | <span data-ttu-id="56802-278">nu</span><span class="sxs-lookup"><span data-stu-id="56802-278">no</span></span>               |
| <span data-ttu-id="56802-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="56802-280">nu</span><span class="sxs-lookup"><span data-stu-id="56802-280">no</span></span>             | <span data-ttu-id="56802-281">nu</span><span class="sxs-lookup"><span data-stu-id="56802-281">no</span></span>               |
| <span data-ttu-id="56802-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="56802-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="56802-283">nu</span><span class="sxs-lookup"><span data-stu-id="56802-283">no</span></span>             | <span data-ttu-id="56802-284">nu</span><span class="sxs-lookup"><span data-stu-id="56802-284">no</span></span>               |
| <span data-ttu-id="56802-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="56802-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="56802-286">nu</span><span class="sxs-lookup"><span data-stu-id="56802-286">no</span></span>             | <span data-ttu-id="56802-287">nu</span><span class="sxs-lookup"><span data-stu-id="56802-287">no</span></span>               |
| <span data-ttu-id="56802-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="56802-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="56802-289">nu</span><span class="sxs-lookup"><span data-stu-id="56802-289">no</span></span>             | <span data-ttu-id="56802-290">nu</span><span class="sxs-lookup"><span data-stu-id="56802-290">no</span></span>               |
| <span data-ttu-id="56802-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="56802-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="56802-292">nu</span><span class="sxs-lookup"><span data-stu-id="56802-292">no</span></span>             | <span data-ttu-id="56802-293">nu</span><span class="sxs-lookup"><span data-stu-id="56802-293">no</span></span>               |
| <span data-ttu-id="56802-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="56802-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="56802-295">nu</span><span class="sxs-lookup"><span data-stu-id="56802-295">no</span></span>             | <span data-ttu-id="56802-296">nu</span><span class="sxs-lookup"><span data-stu-id="56802-296">no</span></span>               |
| <span data-ttu-id="56802-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="56802-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="56802-298">nu</span><span class="sxs-lookup"><span data-stu-id="56802-298">no</span></span>             | <span data-ttu-id="56802-299">nu</span><span class="sxs-lookup"><span data-stu-id="56802-299">no</span></span>               |
| <span data-ttu-id="56802-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="56802-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="56802-301">nu</span><span class="sxs-lookup"><span data-stu-id="56802-301">no</span></span>             | <span data-ttu-id="56802-302">nu</span><span class="sxs-lookup"><span data-stu-id="56802-302">no</span></span>               |
| <span data-ttu-id="56802-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="56802-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="56802-304">nu</span><span class="sxs-lookup"><span data-stu-id="56802-304">no</span></span>             | <span data-ttu-id="56802-305">nu</span><span class="sxs-lookup"><span data-stu-id="56802-305">no</span></span>               |
| <span data-ttu-id="56802-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="56802-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="56802-307">nu</span><span class="sxs-lookup"><span data-stu-id="56802-307">no</span></span>             | <span data-ttu-id="56802-308">nu</span><span class="sxs-lookup"><span data-stu-id="56802-308">no</span></span>               |
| <span data-ttu-id="56802-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="56802-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="56802-310">nu</span><span class="sxs-lookup"><span data-stu-id="56802-310">no</span></span>             | <span data-ttu-id="56802-311">nu</span><span class="sxs-lookup"><span data-stu-id="56802-311">no</span></span>               |
| <span data-ttu-id="56802-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="56802-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="56802-313">nu</span><span class="sxs-lookup"><span data-stu-id="56802-313">no</span></span>             | <span data-ttu-id="56802-314">nu</span><span class="sxs-lookup"><span data-stu-id="56802-314">no</span></span>               |
| <span data-ttu-id="56802-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="56802-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="56802-316">nu</span><span class="sxs-lookup"><span data-stu-id="56802-316">no</span></span>             | <span data-ttu-id="56802-317">nu</span><span class="sxs-lookup"><span data-stu-id="56802-317">no</span></span>               |
| <span data-ttu-id="56802-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="56802-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="56802-319">nu</span><span class="sxs-lookup"><span data-stu-id="56802-319">no</span></span>             | <span data-ttu-id="56802-320">nu</span><span class="sxs-lookup"><span data-stu-id="56802-320">no</span></span>               |
| <span data-ttu-id="56802-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="56802-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="56802-322">nu</span><span class="sxs-lookup"><span data-stu-id="56802-322">no</span></span>             | <span data-ttu-id="56802-323">nu</span><span class="sxs-lookup"><span data-stu-id="56802-323">no</span></span>               |
| <span data-ttu-id="56802-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="56802-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="56802-325">nu</span><span class="sxs-lookup"><span data-stu-id="56802-325">no</span></span>             | <span data-ttu-id="56802-326">nu</span><span class="sxs-lookup"><span data-stu-id="56802-326">no</span></span>               |
| <span data-ttu-id="56802-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="56802-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="56802-328">nu</span><span class="sxs-lookup"><span data-stu-id="56802-328">no</span></span>             | <span data-ttu-id="56802-329">nu</span><span class="sxs-lookup"><span data-stu-id="56802-329">no</span></span>               |
| <span data-ttu-id="56802-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="56802-330">msdyn_summary</span></span>                          | <span data-ttu-id="56802-331">nu</span><span class="sxs-lookup"><span data-stu-id="56802-331">no</span></span>             | <span data-ttu-id="56802-332">nu</span><span class="sxs-lookup"><span data-stu-id="56802-332">no</span></span>               |
| <span data-ttu-id="56802-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="56802-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="56802-334">nu</span><span class="sxs-lookup"><span data-stu-id="56802-334">no</span></span>             | <span data-ttu-id="56802-335">nu</span><span class="sxs-lookup"><span data-stu-id="56802-335">no</span></span>               |
| <span data-ttu-id="56802-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="56802-337">nu</span><span class="sxs-lookup"><span data-stu-id="56802-337">no</span></span>             | <span data-ttu-id="56802-338">nu</span><span class="sxs-lookup"><span data-stu-id="56802-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="56802-339">Dependență de activitate proiect</span><span class="sxs-lookup"><span data-stu-id="56802-339">Project task dependency</span></span>

| <span data-ttu-id="56802-340">**Nume logic**</span><span class="sxs-lookup"><span data-stu-id="56802-340">**Logical name**</span></span>              | <span data-ttu-id="56802-341">**Poate crea**</span><span class="sxs-lookup"><span data-stu-id="56802-341">**Can create**</span></span> | <span data-ttu-id="56802-342">**Poate edita**</span><span class="sxs-lookup"><span data-stu-id="56802-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="56802-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="56802-343">msdyn_linktype</span></span>                | <span data-ttu-id="56802-344">nu</span><span class="sxs-lookup"><span data-stu-id="56802-344">no</span></span>             | <span data-ttu-id="56802-345">nu</span><span class="sxs-lookup"><span data-stu-id="56802-345">no</span></span>           |
| <span data-ttu-id="56802-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="56802-346">msdyn_linktypename</span></span>            | <span data-ttu-id="56802-347">nu</span><span class="sxs-lookup"><span data-stu-id="56802-347">no</span></span>             | <span data-ttu-id="56802-348">nu</span><span class="sxs-lookup"><span data-stu-id="56802-348">no</span></span>           |
| <span data-ttu-id="56802-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="56802-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="56802-350">da</span><span class="sxs-lookup"><span data-stu-id="56802-350">yes</span></span>            | <span data-ttu-id="56802-351">nu</span><span class="sxs-lookup"><span data-stu-id="56802-351">no</span></span>           |
| <span data-ttu-id="56802-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="56802-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="56802-353">da</span><span class="sxs-lookup"><span data-stu-id="56802-353">yes</span></span>            | <span data-ttu-id="56802-354">nu</span><span class="sxs-lookup"><span data-stu-id="56802-354">no</span></span>           |
| <span data-ttu-id="56802-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="56802-355">msdyn_project</span></span>                 | <span data-ttu-id="56802-356">da</span><span class="sxs-lookup"><span data-stu-id="56802-356">yes</span></span>            | <span data-ttu-id="56802-357">nu</span><span class="sxs-lookup"><span data-stu-id="56802-357">no</span></span>           |
| <span data-ttu-id="56802-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="56802-358">msdyn_projectname</span></span>             | <span data-ttu-id="56802-359">da</span><span class="sxs-lookup"><span data-stu-id="56802-359">yes</span></span>            | <span data-ttu-id="56802-360">nu</span><span class="sxs-lookup"><span data-stu-id="56802-360">no</span></span>           |
| <span data-ttu-id="56802-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="56802-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="56802-362">da</span><span class="sxs-lookup"><span data-stu-id="56802-362">yes</span></span>            | <span data-ttu-id="56802-363">nu</span><span class="sxs-lookup"><span data-stu-id="56802-363">no</span></span>           |
| <span data-ttu-id="56802-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="56802-364">msdyn_successortask</span></span>           | <span data-ttu-id="56802-365">da</span><span class="sxs-lookup"><span data-stu-id="56802-365">yes</span></span>            | <span data-ttu-id="56802-366">nu</span><span class="sxs-lookup"><span data-stu-id="56802-366">no</span></span>           |
| <span data-ttu-id="56802-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="56802-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="56802-368">da</span><span class="sxs-lookup"><span data-stu-id="56802-368">yes</span></span>            | <span data-ttu-id="56802-369">nu</span><span class="sxs-lookup"><span data-stu-id="56802-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="56802-370">Atribuire de resurse</span><span class="sxs-lookup"><span data-stu-id="56802-370">Resource assignment</span></span>

| <span data-ttu-id="56802-371">**Nume logic**</span><span class="sxs-lookup"><span data-stu-id="56802-371">**Logical name**</span></span>             | <span data-ttu-id="56802-372">**Poate crea**</span><span class="sxs-lookup"><span data-stu-id="56802-372">**Can create**</span></span> | <span data-ttu-id="56802-373">**Poate edita**</span><span class="sxs-lookup"><span data-stu-id="56802-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="56802-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="56802-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="56802-375">da</span><span class="sxs-lookup"><span data-stu-id="56802-375">yes</span></span>            | <span data-ttu-id="56802-376">nu</span><span class="sxs-lookup"><span data-stu-id="56802-376">no</span></span>           |
| <span data-ttu-id="56802-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="56802-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="56802-378">da</span><span class="sxs-lookup"><span data-stu-id="56802-378">yes</span></span>            | <span data-ttu-id="56802-379">nu</span><span class="sxs-lookup"><span data-stu-id="56802-379">no</span></span>           |
| <span data-ttu-id="56802-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="56802-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="56802-381">nu</span><span class="sxs-lookup"><span data-stu-id="56802-381">no</span></span>             | <span data-ttu-id="56802-382">nu</span><span class="sxs-lookup"><span data-stu-id="56802-382">no</span></span>           |
| <span data-ttu-id="56802-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="56802-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="56802-384">nu</span><span class="sxs-lookup"><span data-stu-id="56802-384">no</span></span>             | <span data-ttu-id="56802-385">nu</span><span class="sxs-lookup"><span data-stu-id="56802-385">no</span></span>           |
| <span data-ttu-id="56802-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="56802-386">msdyn_committype</span></span>             | <span data-ttu-id="56802-387">nu</span><span class="sxs-lookup"><span data-stu-id="56802-387">no</span></span>             | <span data-ttu-id="56802-388">nu</span><span class="sxs-lookup"><span data-stu-id="56802-388">no</span></span>           |
| <span data-ttu-id="56802-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="56802-389">msdyn_committypename</span></span>         | <span data-ttu-id="56802-390">nu</span><span class="sxs-lookup"><span data-stu-id="56802-390">no</span></span>             | <span data-ttu-id="56802-391">nu</span><span class="sxs-lookup"><span data-stu-id="56802-391">no</span></span>           |
| <span data-ttu-id="56802-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="56802-392">msdyn_effort</span></span>                 | <span data-ttu-id="56802-393">nu</span><span class="sxs-lookup"><span data-stu-id="56802-393">no</span></span>             | <span data-ttu-id="56802-394">nu</span><span class="sxs-lookup"><span data-stu-id="56802-394">no</span></span>           |
| <span data-ttu-id="56802-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="56802-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="56802-396">nu</span><span class="sxs-lookup"><span data-stu-id="56802-396">no</span></span>             | <span data-ttu-id="56802-397">nu</span><span class="sxs-lookup"><span data-stu-id="56802-397">no</span></span>           |
| <span data-ttu-id="56802-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="56802-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="56802-399">nu</span><span class="sxs-lookup"><span data-stu-id="56802-399">no</span></span>             | <span data-ttu-id="56802-400">nu</span><span class="sxs-lookup"><span data-stu-id="56802-400">no</span></span>           |
| <span data-ttu-id="56802-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="56802-401">msdyn_finish</span></span>                 | <span data-ttu-id="56802-402">nu</span><span class="sxs-lookup"><span data-stu-id="56802-402">no</span></span>             | <span data-ttu-id="56802-403">nu</span><span class="sxs-lookup"><span data-stu-id="56802-403">no</span></span>           |
| <span data-ttu-id="56802-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="56802-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="56802-405">nu</span><span class="sxs-lookup"><span data-stu-id="56802-405">no</span></span>             | <span data-ttu-id="56802-406">nu</span><span class="sxs-lookup"><span data-stu-id="56802-406">no</span></span>           |
| <span data-ttu-id="56802-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="56802-408">nu</span><span class="sxs-lookup"><span data-stu-id="56802-408">no</span></span>             | <span data-ttu-id="56802-409">nu</span><span class="sxs-lookup"><span data-stu-id="56802-409">no</span></span>           |
| <span data-ttu-id="56802-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="56802-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="56802-411">nu</span><span class="sxs-lookup"><span data-stu-id="56802-411">no</span></span>             | <span data-ttu-id="56802-412">nu</span><span class="sxs-lookup"><span data-stu-id="56802-412">no</span></span>           |
| <span data-ttu-id="56802-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="56802-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="56802-414">nu</span><span class="sxs-lookup"><span data-stu-id="56802-414">no</span></span>             | <span data-ttu-id="56802-415">nu</span><span class="sxs-lookup"><span data-stu-id="56802-415">no</span></span>           |
| <span data-ttu-id="56802-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="56802-417">nu</span><span class="sxs-lookup"><span data-stu-id="56802-417">no</span></span>             | <span data-ttu-id="56802-418">nu</span><span class="sxs-lookup"><span data-stu-id="56802-418">no</span></span>           |
| <span data-ttu-id="56802-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="56802-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="56802-420">nu</span><span class="sxs-lookup"><span data-stu-id="56802-420">no</span></span>             | <span data-ttu-id="56802-421">nu</span><span class="sxs-lookup"><span data-stu-id="56802-421">no</span></span>           |
| <span data-ttu-id="56802-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="56802-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="56802-423">nu</span><span class="sxs-lookup"><span data-stu-id="56802-423">no</span></span>             | <span data-ttu-id="56802-424">nu</span><span class="sxs-lookup"><span data-stu-id="56802-424">no</span></span>           |
| <span data-ttu-id="56802-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="56802-425">msdyn_projectid</span></span>              | <span data-ttu-id="56802-426">da</span><span class="sxs-lookup"><span data-stu-id="56802-426">yes</span></span>            | <span data-ttu-id="56802-427">nu</span><span class="sxs-lookup"><span data-stu-id="56802-427">no</span></span>           |
| <span data-ttu-id="56802-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="56802-428">msdyn_projectidname</span></span>          | <span data-ttu-id="56802-429">nu</span><span class="sxs-lookup"><span data-stu-id="56802-429">no</span></span>             | <span data-ttu-id="56802-430">nu</span><span class="sxs-lookup"><span data-stu-id="56802-430">no</span></span>           |
| <span data-ttu-id="56802-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="56802-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="56802-432">nu</span><span class="sxs-lookup"><span data-stu-id="56802-432">no</span></span>             | <span data-ttu-id="56802-433">nu</span><span class="sxs-lookup"><span data-stu-id="56802-433">no</span></span>           |
| <span data-ttu-id="56802-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="56802-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="56802-435">nu</span><span class="sxs-lookup"><span data-stu-id="56802-435">no</span></span>             | <span data-ttu-id="56802-436">nu</span><span class="sxs-lookup"><span data-stu-id="56802-436">no</span></span>           |
| <span data-ttu-id="56802-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="56802-437">msdyn_start</span></span>                  | <span data-ttu-id="56802-438">nu</span><span class="sxs-lookup"><span data-stu-id="56802-438">no</span></span>             | <span data-ttu-id="56802-439">nu</span><span class="sxs-lookup"><span data-stu-id="56802-439">no</span></span>           |
| <span data-ttu-id="56802-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="56802-440">msdyn_taskid</span></span>                 | <span data-ttu-id="56802-441">nu</span><span class="sxs-lookup"><span data-stu-id="56802-441">no</span></span>             | <span data-ttu-id="56802-442">nu</span><span class="sxs-lookup"><span data-stu-id="56802-442">no</span></span>           |
| <span data-ttu-id="56802-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="56802-443">msdyn_taskidname</span></span>             | <span data-ttu-id="56802-444">nu</span><span class="sxs-lookup"><span data-stu-id="56802-444">no</span></span>             | <span data-ttu-id="56802-445">nu</span><span class="sxs-lookup"><span data-stu-id="56802-445">no</span></span>           |
| <span data-ttu-id="56802-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="56802-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="56802-447">nu</span><span class="sxs-lookup"><span data-stu-id="56802-447">no</span></span>             | <span data-ttu-id="56802-448">nu</span><span class="sxs-lookup"><span data-stu-id="56802-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="56802-449">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="56802-449">Project team member</span></span>

| <span data-ttu-id="56802-450">**Nume logic**</span><span class="sxs-lookup"><span data-stu-id="56802-450">**Logical name**</span></span>                                 | <span data-ttu-id="56802-451">**Poate crea**</span><span class="sxs-lookup"><span data-stu-id="56802-451">**Can create**</span></span> | <span data-ttu-id="56802-452">**Poate edita**</span><span class="sxs-lookup"><span data-stu-id="56802-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="56802-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="56802-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="56802-454">nu</span><span class="sxs-lookup"><span data-stu-id="56802-454">no</span></span>             | <span data-ttu-id="56802-455">nu</span><span class="sxs-lookup"><span data-stu-id="56802-455">no</span></span>           |
| <span data-ttu-id="56802-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="56802-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="56802-457">nu</span><span class="sxs-lookup"><span data-stu-id="56802-457">no</span></span>             | <span data-ttu-id="56802-458">nu</span><span class="sxs-lookup"><span data-stu-id="56802-458">no</span></span>           |
| <span data-ttu-id="56802-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="56802-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="56802-460">nu</span><span class="sxs-lookup"><span data-stu-id="56802-460">no</span></span>             | <span data-ttu-id="56802-461">nu</span><span class="sxs-lookup"><span data-stu-id="56802-461">no</span></span>           |
| <span data-ttu-id="56802-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="56802-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="56802-463">nu</span><span class="sxs-lookup"><span data-stu-id="56802-463">no</span></span>             | <span data-ttu-id="56802-464">nu</span><span class="sxs-lookup"><span data-stu-id="56802-464">no</span></span>           |
| <span data-ttu-id="56802-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="56802-465">msdyn_effort</span></span>                                     | <span data-ttu-id="56802-466">nu</span><span class="sxs-lookup"><span data-stu-id="56802-466">no</span></span>             | <span data-ttu-id="56802-467">nu</span><span class="sxs-lookup"><span data-stu-id="56802-467">no</span></span>           |
| <span data-ttu-id="56802-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="56802-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="56802-469">nu</span><span class="sxs-lookup"><span data-stu-id="56802-469">no</span></span>             | <span data-ttu-id="56802-470">nu</span><span class="sxs-lookup"><span data-stu-id="56802-470">no</span></span>           |
| <span data-ttu-id="56802-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="56802-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="56802-472">nu</span><span class="sxs-lookup"><span data-stu-id="56802-472">no</span></span>             | <span data-ttu-id="56802-473">nu</span><span class="sxs-lookup"><span data-stu-id="56802-473">no</span></span>           |
| <span data-ttu-id="56802-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="56802-474">msdyn_finish</span></span>                                     | <span data-ttu-id="56802-475">nu</span><span class="sxs-lookup"><span data-stu-id="56802-475">no</span></span>             | <span data-ttu-id="56802-476">nu</span><span class="sxs-lookup"><span data-stu-id="56802-476">no</span></span>           |
| <span data-ttu-id="56802-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="56802-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="56802-478">nu</span><span class="sxs-lookup"><span data-stu-id="56802-478">no</span></span>             | <span data-ttu-id="56802-479">nu</span><span class="sxs-lookup"><span data-stu-id="56802-479">no</span></span>           |
| <span data-ttu-id="56802-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="56802-480">msdyn_hours</span></span>                                      | <span data-ttu-id="56802-481">nu</span><span class="sxs-lookup"><span data-stu-id="56802-481">no</span></span>             | <span data-ttu-id="56802-482">nu</span><span class="sxs-lookup"><span data-stu-id="56802-482">no</span></span>           |
| <span data-ttu-id="56802-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="56802-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="56802-484">nu</span><span class="sxs-lookup"><span data-stu-id="56802-484">no</span></span>             | <span data-ttu-id="56802-485">nu</span><span class="sxs-lookup"><span data-stu-id="56802-485">no</span></span>           |
| <span data-ttu-id="56802-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="56802-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="56802-487">nu</span><span class="sxs-lookup"><span data-stu-id="56802-487">no</span></span>             | <span data-ttu-id="56802-488">nu</span><span class="sxs-lookup"><span data-stu-id="56802-488">no</span></span>           |
| <span data-ttu-id="56802-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="56802-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="56802-490">nu</span><span class="sxs-lookup"><span data-stu-id="56802-490">no</span></span>             | <span data-ttu-id="56802-491">nu</span><span class="sxs-lookup"><span data-stu-id="56802-491">no</span></span>           |
| <span data-ttu-id="56802-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="56802-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="56802-493">nu</span><span class="sxs-lookup"><span data-stu-id="56802-493">no</span></span>             | <span data-ttu-id="56802-494">nu</span><span class="sxs-lookup"><span data-stu-id="56802-494">no</span></span>           |
| <span data-ttu-id="56802-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="56802-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="56802-496">nu</span><span class="sxs-lookup"><span data-stu-id="56802-496">no</span></span>             | <span data-ttu-id="56802-497">nu</span><span class="sxs-lookup"><span data-stu-id="56802-497">no</span></span>           |
| <span data-ttu-id="56802-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="56802-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="56802-499">nu</span><span class="sxs-lookup"><span data-stu-id="56802-499">no</span></span>             | <span data-ttu-id="56802-500">nu</span><span class="sxs-lookup"><span data-stu-id="56802-500">no</span></span>           |
| <span data-ttu-id="56802-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="56802-501">msdyn_start</span></span>                                      | <span data-ttu-id="56802-502">nu</span><span class="sxs-lookup"><span data-stu-id="56802-502">no</span></span>             | <span data-ttu-id="56802-503">nu</span><span class="sxs-lookup"><span data-stu-id="56802-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="56802-504">Project</span><span class="sxs-lookup"><span data-stu-id="56802-504">Project</span></span>

| <span data-ttu-id="56802-505">**Nume logic**</span><span class="sxs-lookup"><span data-stu-id="56802-505">**Logical name**</span></span>                       | <span data-ttu-id="56802-506">**Poate crea**</span><span class="sxs-lookup"><span data-stu-id="56802-506">**Can create**</span></span> | <span data-ttu-id="56802-507">**Poate edita**</span><span class="sxs-lookup"><span data-stu-id="56802-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="56802-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="56802-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="56802-509">nu</span><span class="sxs-lookup"><span data-stu-id="56802-509">no</span></span>             | <span data-ttu-id="56802-510">nu</span><span class="sxs-lookup"><span data-stu-id="56802-510">no</span></span>           |
| <span data-ttu-id="56802-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="56802-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="56802-512">nu</span><span class="sxs-lookup"><span data-stu-id="56802-512">no</span></span>             | <span data-ttu-id="56802-513">nu</span><span class="sxs-lookup"><span data-stu-id="56802-513">no</span></span>           |
| <span data-ttu-id="56802-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="56802-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="56802-515">nu</span><span class="sxs-lookup"><span data-stu-id="56802-515">no</span></span>             | <span data-ttu-id="56802-516">nu</span><span class="sxs-lookup"><span data-stu-id="56802-516">no</span></span>           |
| <span data-ttu-id="56802-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="56802-518">nu</span><span class="sxs-lookup"><span data-stu-id="56802-518">no</span></span>             | <span data-ttu-id="56802-519">nu</span><span class="sxs-lookup"><span data-stu-id="56802-519">no</span></span>           |
| <span data-ttu-id="56802-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="56802-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="56802-521">nu</span><span class="sxs-lookup"><span data-stu-id="56802-521">no</span></span>             | <span data-ttu-id="56802-522">nu</span><span class="sxs-lookup"><span data-stu-id="56802-522">no</span></span>           |
| <span data-ttu-id="56802-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="56802-524">nu</span><span class="sxs-lookup"><span data-stu-id="56802-524">no</span></span>             | <span data-ttu-id="56802-525">nu</span><span class="sxs-lookup"><span data-stu-id="56802-525">no</span></span>           |
| <span data-ttu-id="56802-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="56802-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="56802-527">da</span><span class="sxs-lookup"><span data-stu-id="56802-527">yes</span></span>            | <span data-ttu-id="56802-528">nu</span><span class="sxs-lookup"><span data-stu-id="56802-528">no</span></span>           |
| <span data-ttu-id="56802-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="56802-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="56802-530">da</span><span class="sxs-lookup"><span data-stu-id="56802-530">yes</span></span>            | <span data-ttu-id="56802-531">nu</span><span class="sxs-lookup"><span data-stu-id="56802-531">no</span></span>           |
| <span data-ttu-id="56802-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="56802-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="56802-533">da</span><span class="sxs-lookup"><span data-stu-id="56802-533">yes</span></span>            | <span data-ttu-id="56802-534">nu</span><span class="sxs-lookup"><span data-stu-id="56802-534">no</span></span>           |
| <span data-ttu-id="56802-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="56802-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="56802-536">nu</span><span class="sxs-lookup"><span data-stu-id="56802-536">no</span></span>             | <span data-ttu-id="56802-537">nu</span><span class="sxs-lookup"><span data-stu-id="56802-537">no</span></span>           |
| <span data-ttu-id="56802-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="56802-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="56802-539">nu</span><span class="sxs-lookup"><span data-stu-id="56802-539">no</span></span>             | <span data-ttu-id="56802-540">nu</span><span class="sxs-lookup"><span data-stu-id="56802-540">no</span></span>           |
| <span data-ttu-id="56802-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="56802-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="56802-542">nu</span><span class="sxs-lookup"><span data-stu-id="56802-542">no</span></span>             | <span data-ttu-id="56802-543">nu</span><span class="sxs-lookup"><span data-stu-id="56802-543">no</span></span>           |
| <span data-ttu-id="56802-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="56802-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="56802-545">nu</span><span class="sxs-lookup"><span data-stu-id="56802-545">no</span></span>             | <span data-ttu-id="56802-546">nu</span><span class="sxs-lookup"><span data-stu-id="56802-546">no</span></span>           |
| <span data-ttu-id="56802-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="56802-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="56802-548">nu</span><span class="sxs-lookup"><span data-stu-id="56802-548">no</span></span>             | <span data-ttu-id="56802-549">nu</span><span class="sxs-lookup"><span data-stu-id="56802-549">no</span></span>           |
| <span data-ttu-id="56802-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="56802-550">msdyn_duration</span></span>                         | <span data-ttu-id="56802-551">nu</span><span class="sxs-lookup"><span data-stu-id="56802-551">no</span></span>             | <span data-ttu-id="56802-552">nu</span><span class="sxs-lookup"><span data-stu-id="56802-552">no</span></span>           |
| <span data-ttu-id="56802-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="56802-553">msdyn_effort</span></span>                           | <span data-ttu-id="56802-554">nu</span><span class="sxs-lookup"><span data-stu-id="56802-554">no</span></span>             | <span data-ttu-id="56802-555">nu</span><span class="sxs-lookup"><span data-stu-id="56802-555">no</span></span>           |
| <span data-ttu-id="56802-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="56802-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="56802-557">nu</span><span class="sxs-lookup"><span data-stu-id="56802-557">no</span></span>             | <span data-ttu-id="56802-558">nu</span><span class="sxs-lookup"><span data-stu-id="56802-558">no</span></span>           |
| <span data-ttu-id="56802-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="56802-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="56802-560">nu</span><span class="sxs-lookup"><span data-stu-id="56802-560">no</span></span>             | <span data-ttu-id="56802-561">nu</span><span class="sxs-lookup"><span data-stu-id="56802-561">no</span></span>           |
| <span data-ttu-id="56802-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="56802-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="56802-563">nu</span><span class="sxs-lookup"><span data-stu-id="56802-563">no</span></span>             | <span data-ttu-id="56802-564">nu</span><span class="sxs-lookup"><span data-stu-id="56802-564">no</span></span>           |
| <span data-ttu-id="56802-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="56802-565">msdyn_finish</span></span>                           | <span data-ttu-id="56802-566">da</span><span class="sxs-lookup"><span data-stu-id="56802-566">yes</span></span>            | <span data-ttu-id="56802-567">da</span><span class="sxs-lookup"><span data-stu-id="56802-567">yes</span></span>          |
| <span data-ttu-id="56802-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="56802-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="56802-569">nu</span><span class="sxs-lookup"><span data-stu-id="56802-569">no</span></span>             | <span data-ttu-id="56802-570">nu</span><span class="sxs-lookup"><span data-stu-id="56802-570">no</span></span>           |
| <span data-ttu-id="56802-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="56802-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="56802-572">nu</span><span class="sxs-lookup"><span data-stu-id="56802-572">no</span></span>             | <span data-ttu-id="56802-573">nu</span><span class="sxs-lookup"><span data-stu-id="56802-573">no</span></span>           |
| <span data-ttu-id="56802-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="56802-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="56802-575">nu</span><span class="sxs-lookup"><span data-stu-id="56802-575">no</span></span>             | <span data-ttu-id="56802-576">nu</span><span class="sxs-lookup"><span data-stu-id="56802-576">no</span></span>           |
| <span data-ttu-id="56802-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="56802-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="56802-578">nu</span><span class="sxs-lookup"><span data-stu-id="56802-578">no</span></span>             | <span data-ttu-id="56802-579">nu</span><span class="sxs-lookup"><span data-stu-id="56802-579">no</span></span>           |
| <span data-ttu-id="56802-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="56802-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="56802-581">nu</span><span class="sxs-lookup"><span data-stu-id="56802-581">no</span></span>             | <span data-ttu-id="56802-582">nu</span><span class="sxs-lookup"><span data-stu-id="56802-582">no</span></span>           |
| <span data-ttu-id="56802-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="56802-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="56802-584">nu</span><span class="sxs-lookup"><span data-stu-id="56802-584">no</span></span>             | <span data-ttu-id="56802-585">nu</span><span class="sxs-lookup"><span data-stu-id="56802-585">no</span></span>           |
| <span data-ttu-id="56802-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="56802-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="56802-587">nu</span><span class="sxs-lookup"><span data-stu-id="56802-587">no</span></span>             | <span data-ttu-id="56802-588">nu</span><span class="sxs-lookup"><span data-stu-id="56802-588">no</span></span>           |
| <span data-ttu-id="56802-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="56802-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="56802-590">nu</span><span class="sxs-lookup"><span data-stu-id="56802-590">no</span></span>             | <span data-ttu-id="56802-591">nu</span><span class="sxs-lookup"><span data-stu-id="56802-591">no</span></span>           |
| <span data-ttu-id="56802-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="56802-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="56802-593">nu</span><span class="sxs-lookup"><span data-stu-id="56802-593">no</span></span>             | <span data-ttu-id="56802-594">nu</span><span class="sxs-lookup"><span data-stu-id="56802-594">no</span></span>           |
| <span data-ttu-id="56802-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="56802-596">nu</span><span class="sxs-lookup"><span data-stu-id="56802-596">no</span></span>             | <span data-ttu-id="56802-597">nu</span><span class="sxs-lookup"><span data-stu-id="56802-597">no</span></span>           |
| <span data-ttu-id="56802-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="56802-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="56802-599">nu</span><span class="sxs-lookup"><span data-stu-id="56802-599">no</span></span>             | <span data-ttu-id="56802-600">nu</span><span class="sxs-lookup"><span data-stu-id="56802-600">no</span></span>           |
| <span data-ttu-id="56802-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="56802-602">nu</span><span class="sxs-lookup"><span data-stu-id="56802-602">no</span></span>             | <span data-ttu-id="56802-603">nu</span><span class="sxs-lookup"><span data-stu-id="56802-603">no</span></span>           |
| <span data-ttu-id="56802-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="56802-604">msdyn_progress</span></span>                         | <span data-ttu-id="56802-605">nu</span><span class="sxs-lookup"><span data-stu-id="56802-605">no</span></span>             | <span data-ttu-id="56802-606">nu</span><span class="sxs-lookup"><span data-stu-id="56802-606">no</span></span>           |
| <span data-ttu-id="56802-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="56802-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="56802-608">nu</span><span class="sxs-lookup"><span data-stu-id="56802-608">no</span></span>             | <span data-ttu-id="56802-609">nu</span><span class="sxs-lookup"><span data-stu-id="56802-609">no</span></span>           |
| <span data-ttu-id="56802-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="56802-611">nu</span><span class="sxs-lookup"><span data-stu-id="56802-611">no</span></span>             | <span data-ttu-id="56802-612">nu</span><span class="sxs-lookup"><span data-stu-id="56802-612">no</span></span>           |
| <span data-ttu-id="56802-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="56802-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="56802-614">nu</span><span class="sxs-lookup"><span data-stu-id="56802-614">no</span></span>             | <span data-ttu-id="56802-615">nu</span><span class="sxs-lookup"><span data-stu-id="56802-615">no</span></span>           |
| <span data-ttu-id="56802-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="56802-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="56802-617">nu</span><span class="sxs-lookup"><span data-stu-id="56802-617">no</span></span>             | <span data-ttu-id="56802-618">nu</span><span class="sxs-lookup"><span data-stu-id="56802-618">no</span></span>           |
| <span data-ttu-id="56802-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="56802-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="56802-620">nu</span><span class="sxs-lookup"><span data-stu-id="56802-620">no</span></span>             | <span data-ttu-id="56802-621">nu</span><span class="sxs-lookup"><span data-stu-id="56802-621">no</span></span>           |
| <span data-ttu-id="56802-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="56802-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="56802-623">nu</span><span class="sxs-lookup"><span data-stu-id="56802-623">no</span></span>             | <span data-ttu-id="56802-624">nu</span><span class="sxs-lookup"><span data-stu-id="56802-624">no</span></span>           |
| <span data-ttu-id="56802-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="56802-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="56802-626">nu</span><span class="sxs-lookup"><span data-stu-id="56802-626">no</span></span>             | <span data-ttu-id="56802-627">nu</span><span class="sxs-lookup"><span data-stu-id="56802-627">no</span></span>           |
| <span data-ttu-id="56802-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="56802-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="56802-629">nu</span><span class="sxs-lookup"><span data-stu-id="56802-629">no</span></span>             | <span data-ttu-id="56802-630">nu</span><span class="sxs-lookup"><span data-stu-id="56802-630">no</span></span>           |
| <span data-ttu-id="56802-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="56802-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="56802-632">nu</span><span class="sxs-lookup"><span data-stu-id="56802-632">no</span></span>             | <span data-ttu-id="56802-633">nu</span><span class="sxs-lookup"><span data-stu-id="56802-633">no</span></span>           |
| <span data-ttu-id="56802-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="56802-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="56802-635">nu</span><span class="sxs-lookup"><span data-stu-id="56802-635">no</span></span>             | <span data-ttu-id="56802-636">nu</span><span class="sxs-lookup"><span data-stu-id="56802-636">no</span></span>           |
| <span data-ttu-id="56802-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="56802-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="56802-638">nu</span><span class="sxs-lookup"><span data-stu-id="56802-638">no</span></span>             | <span data-ttu-id="56802-639">nu</span><span class="sxs-lookup"><span data-stu-id="56802-639">no</span></span>           |
| <span data-ttu-id="56802-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="56802-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="56802-641">nu</span><span class="sxs-lookup"><span data-stu-id="56802-641">no</span></span>             | <span data-ttu-id="56802-642">nu</span><span class="sxs-lookup"><span data-stu-id="56802-642">no</span></span>           |
| <span data-ttu-id="56802-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="56802-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="56802-644">nu</span><span class="sxs-lookup"><span data-stu-id="56802-644">no</span></span>             | <span data-ttu-id="56802-645">nu</span><span class="sxs-lookup"><span data-stu-id="56802-645">no</span></span>           |
| <span data-ttu-id="56802-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="56802-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="56802-647">nu</span><span class="sxs-lookup"><span data-stu-id="56802-647">no</span></span>             | <span data-ttu-id="56802-648">nu</span><span class="sxs-lookup"><span data-stu-id="56802-648">no</span></span>           |
| <span data-ttu-id="56802-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="56802-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="56802-650">nu</span><span class="sxs-lookup"><span data-stu-id="56802-650">no</span></span>             | <span data-ttu-id="56802-651">nu</span><span class="sxs-lookup"><span data-stu-id="56802-651">no</span></span>           |
| <span data-ttu-id="56802-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="56802-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="56802-653">nu</span><span class="sxs-lookup"><span data-stu-id="56802-653">no</span></span>             | <span data-ttu-id="56802-654">nu</span><span class="sxs-lookup"><span data-stu-id="56802-654">no</span></span>           |
| <span data-ttu-id="56802-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="56802-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="56802-656">nu</span><span class="sxs-lookup"><span data-stu-id="56802-656">no</span></span>             | <span data-ttu-id="56802-657">nu</span><span class="sxs-lookup"><span data-stu-id="56802-657">no</span></span>           |
| <span data-ttu-id="56802-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="56802-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="56802-659">nu</span><span class="sxs-lookup"><span data-stu-id="56802-659">no</span></span>             | <span data-ttu-id="56802-660">nu</span><span class="sxs-lookup"><span data-stu-id="56802-660">no</span></span>           |
| <span data-ttu-id="56802-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="56802-662">nu</span><span class="sxs-lookup"><span data-stu-id="56802-662">no</span></span>             | <span data-ttu-id="56802-663">nu</span><span class="sxs-lookup"><span data-stu-id="56802-663">no</span></span>           |
| <span data-ttu-id="56802-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="56802-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="56802-665">nu</span><span class="sxs-lookup"><span data-stu-id="56802-665">no</span></span>             | <span data-ttu-id="56802-666">nu</span><span class="sxs-lookup"><span data-stu-id="56802-666">no</span></span>           |
| <span data-ttu-id="56802-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="56802-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="56802-668">nu</span><span class="sxs-lookup"><span data-stu-id="56802-668">no</span></span>             | <span data-ttu-id="56802-669">nu</span><span class="sxs-lookup"><span data-stu-id="56802-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="56802-670">Limitări și probleme cunoscute</span><span class="sxs-lookup"><span data-stu-id="56802-670">Limitations and known issues</span></span>
<span data-ttu-id="56802-671">Următoarea este o listă de limitări și probleme cunoscute:</span><span class="sxs-lookup"><span data-stu-id="56802-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="56802-672">API-urile de programare pot fi utilizate numai de **Utilizatori cu licență Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="56802-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="56802-673">Nu pot fi utilizate de:</span><span class="sxs-lookup"><span data-stu-id="56802-673">They can't be used by:</span></span>
    - <span data-ttu-id="56802-674">Utilizatori aplicație</span><span class="sxs-lookup"><span data-stu-id="56802-674">Application users</span></span>
    - <span data-ttu-id="56802-675">Utilizatori de sistem</span><span class="sxs-lookup"><span data-stu-id="56802-675">System users</span></span>
    - <span data-ttu-id="56802-676">Utilizatori de integrare</span><span class="sxs-lookup"><span data-stu-id="56802-676">Integration users</span></span>
    - <span data-ttu-id="56802-677">Alți utilizatori care nu au licența necesară</span><span class="sxs-lookup"><span data-stu-id="56802-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="56802-678">Fiecare **OperationSet** poate efectua doar maximum 100 de operații.</span><span class="sxs-lookup"><span data-stu-id="56802-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="56802-679">Fiecare utilizator poate avea doar un maximum de 10 **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="56802-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="56802-680">Project Operations acceptă în prezent maximum 500 de sarcini totale pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="56802-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="56802-681">**OperationSet** starea de eroare și jurnalele de erori nu sunt disponibile momentan.</span><span class="sxs-lookup"><span data-stu-id="56802-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="56802-682">Limite și restricții pentru proiecte și sarcini</span><span class="sxs-lookup"><span data-stu-id="56802-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="56802-683">Eroare de tratare</span><span class="sxs-lookup"><span data-stu-id="56802-683">Error handling</span></span>

   - <span data-ttu-id="56802-684">Pentru a revizui erorile generate din seturile de operații, accesați **Setări** \> **Integrarea planificării** \> **Seturi de operații**.</span><span class="sxs-lookup"><span data-stu-id="56802-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="56802-685">Pentru a examina erorile generate de serviciul de planificare a proiectelor, accesați **Setări** \> **Integrarea planificării** \> **Jurnalele de erori PSS**.</span><span class="sxs-lookup"><span data-stu-id="56802-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="56802-686">Eșantion de scenariu</span><span class="sxs-lookup"><span data-stu-id="56802-686">Sample scenario</span></span>

<span data-ttu-id="56802-687">În acest scenariu, veți crea un proiect, un membru al echipei, patru sarcini și două alocări de resurse.</span><span class="sxs-lookup"><span data-stu-id="56802-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="56802-688">Apoi, veți actualiza o sarcină, actualizați proiectul, ștergeți o sarcină, ștergeți o atribuire de resurse și creați o dependență de sarcină.</span><span class="sxs-lookup"><span data-stu-id="56802-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="56802-689">Eșantioane suplimentare</span><span class="sxs-lookup"><span data-stu-id="56802-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
