---
title: Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare
description: Acest subiect oferă informații și exemple pentru utilizarea API-urilor de Planificare.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868144"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="56d3e-103">Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare</span><span class="sxs-lookup"><span data-stu-id="56d3e-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="56d3e-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="56d3e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="56d3e-105">O parte sau toate funcționalitățile notate în acest subiect sunt disponibile ca parte a ediției de previzualizare.</span><span class="sxs-lookup"><span data-stu-id="56d3e-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="56d3e-106">Conținutul și funcționalitățile pot fi modificate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="56d3e-107">Entități de planificare</span><span class="sxs-lookup"><span data-stu-id="56d3e-107">Scheduling entities</span></span>

<span data-ttu-id="56d3e-108">API-urile de programare oferă posibilitatea de a efectua operațiuni de creare, actualizare și ștergere cu **Entități de planificare**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="56d3e-109">Aceste entități sunt gestionate prin intermediul motorului de planificare în Proiect pentru web.</span><span class="sxs-lookup"><span data-stu-id="56d3e-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="56d3e-110">Creați, actualizați și ștergeți operațiuni cu **Entități de planificare** au fost restricționate în versiuni mai timpurii ale Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="56d3e-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="56d3e-111">Următorul tabel oferă o listă completă a **Entităților de planificare**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="56d3e-112">Nume de entitate</span><span class="sxs-lookup"><span data-stu-id="56d3e-112">Entity name</span></span>  | <span data-ttu-id="56d3e-113">Numele logic al entității</span><span class="sxs-lookup"><span data-stu-id="56d3e-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="56d3e-114">Project</span><span class="sxs-lookup"><span data-stu-id="56d3e-114">Project</span></span> | <span data-ttu-id="56d3e-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="56d3e-115">msdyn_project</span></span> |
| <span data-ttu-id="56d3e-116">Activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-116">Project Task</span></span>  | <span data-ttu-id="56d3e-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="56d3e-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="56d3e-118">Dependență de activitate proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-118">Project Task Dependency</span></span>  | <span data-ttu-id="56d3e-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="56d3e-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="56d3e-120">Atribuire de resurse</span><span class="sxs-lookup"><span data-stu-id="56d3e-120">Resource Assignment</span></span> | <span data-ttu-id="56d3e-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="56d3e-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="56d3e-122">Pachet de proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-122">Project Bucket</span></span>  | <span data-ttu-id="56d3e-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="56d3e-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="56d3e-124">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-124">Project Team Member</span></span> | <span data-ttu-id="56d3e-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="56d3e-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="56d3e-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="56d3e-126">OperationSet</span></span>

<span data-ttu-id="56d3e-127">OperationSet este un model de unitate de lucru care poate fi utilizat atunci când mai multe cereri care afectează planificarea trebuie procesate în cadrul unei tranzacții.</span><span class="sxs-lookup"><span data-stu-id="56d3e-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="56d3e-128">Planificați API-urile</span><span class="sxs-lookup"><span data-stu-id="56d3e-128">Schedule APIs</span></span>

<span data-ttu-id="56d3e-129">Următoarea este o listă a API-urilor curente de planificare.</span><span class="sxs-lookup"><span data-stu-id="56d3e-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="56d3e-130">**msdyn_CreateProjectV1**: Acest API poate fi folosit pentru a crea un proiect.</span><span class="sxs-lookup"><span data-stu-id="56d3e-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="56d3e-131">Proiectul și pachetul de proiect implicit sunt create imediat.</span><span class="sxs-lookup"><span data-stu-id="56d3e-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="56d3e-132">**msdyn_CreateTeamMemberV1**: Acest API poate fi utilizat pentru a crea un membru al echipei de proiect.</span><span class="sxs-lookup"><span data-stu-id="56d3e-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="56d3e-133">Înregistrarea membrilor echipei este creată imediat.</span><span class="sxs-lookup"><span data-stu-id="56d3e-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="56d3e-134">**msdyn_CreateOperationSetV1**: Acest API poate fi utilizat pentru a programa mai multe solicitări care trebuie efectuate în cadrul unei tranzacții.</span><span class="sxs-lookup"><span data-stu-id="56d3e-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="56d3e-135">**msdyn_PSSCreateV1**: Acest API poate fi utilizat pentru a crea o entitate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="56d3e-136">Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de creare.</span><span class="sxs-lookup"><span data-stu-id="56d3e-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="56d3e-137">**msdyn_PSSUpdateV1**: acest API poate fi utilizat pentru a actualiza o entitate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="56d3e-138">Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de actualizare.</span><span class="sxs-lookup"><span data-stu-id="56d3e-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="56d3e-139">**msdyn_PSSDeleteV1**: acest API poate fi utilizat pentru a șterge o entitate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="56d3e-140">Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de ștergere.</span><span class="sxs-lookup"><span data-stu-id="56d3e-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="56d3e-141">**msdyn_ExecuteOperationSetV1**: Acest API este utilizat pentru a executa toate operațiunile din cadrul setului de operații date.</span><span class="sxs-lookup"><span data-stu-id="56d3e-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="56d3e-142">Utilizarea API-urilor de programare cu OperationSet</span><span class="sxs-lookup"><span data-stu-id="56d3e-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="56d3e-143">Pentru că înregistrează cu amândouă **CreateProjectV1** și **CreateTeamMemberV1** sunt create imediat, aceste API-uri nu pot fi utilizate în **OperationSet** direct.</span><span class="sxs-lookup"><span data-stu-id="56d3e-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="56d3e-144">Cu toate acestea, puteți utiliza API-ul pentru a crea înregistrări necesare, pentru a crea un **OperationSet**, și apoi utilizați aceste înregistrări pre-create în **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="56d3e-145">Operațiuni acceptate</span><span class="sxs-lookup"><span data-stu-id="56d3e-145">Supported operations</span></span>

| <span data-ttu-id="56d3e-146">Entitate de planificare</span><span class="sxs-lookup"><span data-stu-id="56d3e-146">Scheduling entity</span></span> | <span data-ttu-id="56d3e-147">Creați</span><span class="sxs-lookup"><span data-stu-id="56d3e-147">Create</span></span> | <span data-ttu-id="56d3e-148">Actualizați</span><span class="sxs-lookup"><span data-stu-id="56d3e-148">Update</span></span> | <span data-ttu-id="56d3e-149">Delete</span><span class="sxs-lookup"><span data-stu-id="56d3e-149">Delete</span></span> | <span data-ttu-id="56d3e-150">Considerații importante</span><span class="sxs-lookup"><span data-stu-id="56d3e-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="56d3e-151">Activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-151">Project task</span></span> | <span data-ttu-id="56d3e-152">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-152">Yes</span></span> | <span data-ttu-id="56d3e-153">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-153">Yes</span></span> | <span data-ttu-id="56d3e-154">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-154">Yes</span></span> | <span data-ttu-id="56d3e-155">Fără</span><span class="sxs-lookup"><span data-stu-id="56d3e-155">None</span></span> |
| <span data-ttu-id="56d3e-156">Dependență de activitate proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-156">Project task dependency</span></span> | <span data-ttu-id="56d3e-157">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-157">Yes</span></span> | <span data-ttu-id="56d3e-158">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-158">Yes</span></span> | | <span data-ttu-id="56d3e-159">Înregistrările de dependență ale sarcinii de proiect nu sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="56d3e-160">În schimb, o înregistrare veche poate fi ștearsă și o nouă înregistrare poate fi creată.</span><span class="sxs-lookup"><span data-stu-id="56d3e-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="56d3e-161">Atribuire de resurse</span><span class="sxs-lookup"><span data-stu-id="56d3e-161">Resource assignment</span></span> | <span data-ttu-id="56d3e-162">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-162">Yes</span></span> | <span data-ttu-id="56d3e-163">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-163">Yes</span></span> | | <span data-ttu-id="56d3e-164">Operațiile cu următoarele câmpuri nu sunt acceptate: **BookableResourceID**, **Efort**, **EfortCompletat**, **EfortRămânând**, și **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="56d3e-165">Înregistrările de alocare a resurselor nu sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="56d3e-166">În schimb, înregistrarea veche poate fi ștearsă și o nouă înregistrare poate fi creată.</span><span class="sxs-lookup"><span data-stu-id="56d3e-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="56d3e-167">Pachet de proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-167">Project bucket</span></span> | <span data-ttu-id="56d3e-168">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56d3e-168">N/A</span></span> | <span data-ttu-id="56d3e-169">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56d3e-169">N/A</span></span> | <span data-ttu-id="56d3e-170">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56d3e-170">N/A</span></span> | <span data-ttu-id="56d3e-171">Pachetul implicit este creat folosind API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="56d3e-172">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="56d3e-172">Project team member</span></span> | <span data-ttu-id="56d3e-173">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-173">Yes</span></span> | <span data-ttu-id="56d3e-174">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-174">Yes</span></span> | <span data-ttu-id="56d3e-175">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-175">Yes</span></span> | <span data-ttu-id="56d3e-176">Pentru operația de creare, utilizați API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="56d3e-177">Project</span><span class="sxs-lookup"><span data-stu-id="56d3e-177">Project</span></span> | <span data-ttu-id="56d3e-178">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-178">Yes</span></span> | <span data-ttu-id="56d3e-179">Da</span><span class="sxs-lookup"><span data-stu-id="56d3e-179">Yes</span></span> | <span data-ttu-id="56d3e-180">Nedisponibil</span><span class="sxs-lookup"><span data-stu-id="56d3e-180">N/A</span></span> | <span data-ttu-id="56d3e-181">Operațiunile cu următoarele câmpuri nu sunt acceptate: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Efort**, **EfortCompletat**, **EfortRămânând**, **Progres**, **Finalizare**, **TaskEarliestStart** și **Durată**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="56d3e-182">Aceste API-uri pot fi apelate cu obiecte de entitate care includ câmpuri personalizate.</span><span class="sxs-lookup"><span data-stu-id="56d3e-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="56d3e-183">Proprietatea ID este opțională.</span><span class="sxs-lookup"><span data-stu-id="56d3e-183">The ID property is optional.</span></span> <span data-ttu-id="56d3e-184">Dacă este furnizat, sistemul încearcă să-l folosească și aruncă o excepție dacă nu poate fi folosit.</span><span class="sxs-lookup"><span data-stu-id="56d3e-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="56d3e-185">Dacă nu este furnizat, sistemul îl va genera.</span><span class="sxs-lookup"><span data-stu-id="56d3e-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="56d3e-186">Limitări și probleme cunoscute</span><span class="sxs-lookup"><span data-stu-id="56d3e-186">Limitations and known issues</span></span>
<span data-ttu-id="56d3e-187">Următoarea este o listă de limitări și probleme cunoscute:</span><span class="sxs-lookup"><span data-stu-id="56d3e-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="56d3e-188">API-urile de programare pot fi utilizate numai de **Utilizatori cu licență Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="56d3e-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="56d3e-189">Nu pot fi utilizate de:</span><span class="sxs-lookup"><span data-stu-id="56d3e-189">They can't be used by:</span></span>
    - <span data-ttu-id="56d3e-190">Utilizatori aplicație</span><span class="sxs-lookup"><span data-stu-id="56d3e-190">Application users</span></span>
    - <span data-ttu-id="56d3e-191">Utilizatori de sistem</span><span class="sxs-lookup"><span data-stu-id="56d3e-191">System users</span></span>
    - <span data-ttu-id="56d3e-192">Utilizatori de integrare</span><span class="sxs-lookup"><span data-stu-id="56d3e-192">Integration users</span></span>
    - <span data-ttu-id="56d3e-193">Alți utilizatori care nu au licența necesară</span><span class="sxs-lookup"><span data-stu-id="56d3e-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="56d3e-194">Fiecare **OperationSet** poate efectua doar maximum 100 de operații.</span><span class="sxs-lookup"><span data-stu-id="56d3e-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="56d3e-195">Fiecare utilizator poate avea doar un maximum de 10 **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="56d3e-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="56d3e-196">Project Operations acceptă în prezent maximum 500 de sarcini totale pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="56d3e-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="56d3e-197">**OperationSet** starea de eroare și jurnalele de erori nu sunt disponibile momentan.</span><span class="sxs-lookup"><span data-stu-id="56d3e-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="56d3e-198">Planificarea API-urilor sunt în versiune preliminară publică.</span><span class="sxs-lookup"><span data-stu-id="56d3e-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="56d3e-199">Utilizarea acestor API-uri într-un mediu de producție nu este acceptată de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="56d3e-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="56d3e-200">Eșantion de scenariu</span><span class="sxs-lookup"><span data-stu-id="56d3e-200">Sample scenario</span></span>

<span data-ttu-id="56d3e-201">În acest scenariu, veți crea un proiect, un membru al echipei, patru sarcini și două alocări de resurse.</span><span class="sxs-lookup"><span data-stu-id="56d3e-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="56d3e-202">Apoi, veți actualiza o sarcină, actualizați proiectul, ștergeți o sarcină, ștergeți o atribuire de resurse și creați o dependență de sarcină.</span><span class="sxs-lookup"><span data-stu-id="56d3e-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="56d3e-203">Eșantioane suplimentare</span><span class="sxs-lookup"><span data-stu-id="56d3e-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
