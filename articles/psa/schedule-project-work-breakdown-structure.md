---
title: Planificarea unui proiect cu o structură detaliată a proiectului
description: Cum să planificați un proiect cu o structură detaliată a proiectului în Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082978"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="f2246-103">Planificarea unui proiect cu o structură detaliată a proiectului (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f2246-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f2246-104">O planificare de proiect comunică ce lucru trebuie să fie efectuat, ce resurse vor efectua lucrul și intervalul de timp în care trebuie să fie efectuat lucrul.</span><span class="sxs-lookup"><span data-stu-id="f2246-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="f2246-105">Planificarea proiectului reflectă tot lucrul asociat cu livrarea proiectului la timp.</span><span class="sxs-lookup"><span data-stu-id="f2246-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="f2246-106">Unul dintre primii pași din faza de inițiere a proiectului este livrarea unei planificări de proiect.</span><span class="sxs-lookup"><span data-stu-id="f2246-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="f2246-107">Pentru a stabili o planificare de proiect, trebuie să creați o structură detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="f2246-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="f2246-108">Creați o structură de proiect cu o structură detaliată a proiectului, care vă ajută să:</span><span class="sxs-lookup"><span data-stu-id="f2246-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="f2246-109">Scindați lucrul în activități gestionabile</span><span class="sxs-lookup"><span data-stu-id="f2246-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="f2246-110">Estimați timpul necesar pentru a finaliza o activitate</span><span class="sxs-lookup"><span data-stu-id="f2246-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="f2246-111">Setați dependențele pentru activități și durata activităților</span><span class="sxs-lookup"><span data-stu-id="f2246-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="f2246-112">Determinați rolurile necesare pentru finalizarea fiecărei activități</span><span class="sxs-lookup"><span data-stu-id="f2246-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="f2246-113">Planificarea proiectului în structura detaliată a proiectului are un aspect și un stil familiar, completat cu o diagramă Gantt interactivă.</span><span class="sxs-lookup"><span data-stu-id="f2246-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="f2246-114">Creați o structură detaliată a proiectului pentru un proiect</span><span class="sxs-lookup"><span data-stu-id="f2246-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="f2246-115">Creați o structură detaliată a proiectului pentru a reprezenta secvența de activități dintr-un proiect.</span><span class="sxs-lookup"><span data-stu-id="f2246-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="f2246-116">Structură detaliată a proiectului include activitățile, cerințele pentru fiecare activitate și informațiile despre venituri și costuri.</span><span class="sxs-lookup"><span data-stu-id="f2246-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="f2246-117">În structură detaliată a proiectului, aveți posibilitatea să adăugați:</span><span class="sxs-lookup"><span data-stu-id="f2246-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="f2246-118">Succesiunea de activități dintr-o ierarhie</span><span class="sxs-lookup"><span data-stu-id="f2246-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="f2246-119">Alte activități, dacă există, care trebuie să fie finalizate înainte de începerea activității</span><span class="sxs-lookup"><span data-stu-id="f2246-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="f2246-120">Data de început, data de sfârșit și durata unei activități</span><span class="sxs-lookup"><span data-stu-id="f2246-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="f2246-121">Numărul de ore necesare pentru o activitate</span><span class="sxs-lookup"><span data-stu-id="f2246-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="f2246-122">Orice abilități și educația necesare pentru un angajat</span><span class="sxs-lookup"><span data-stu-id="f2246-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="f2246-123">Angajații cărora li s-a atribuit o activitate</span><span class="sxs-lookup"><span data-stu-id="f2246-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="f2246-124">Venitul și costurile estimate</span><span class="sxs-lookup"><span data-stu-id="f2246-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="f2246-125">Tipuri de activitate</span><span class="sxs-lookup"><span data-stu-id="f2246-125">Task types</span></span>  
<span data-ttu-id="f2246-126">Veți utiliza următoarele tipuri de activități atunci când creați structura detaliată a proiectului:</span><span class="sxs-lookup"><span data-stu-id="f2246-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="f2246-127">**Nodul rădăcină al proiectului**</span><span class="sxs-lookup"><span data-stu-id="f2246-127">**Project root node**</span></span> | <span data-ttu-id="f2246-128">Activitatea rezumat de nivel superior pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="f2246-128">The top-level summary task for the project.</span></span> <span data-ttu-id="f2246-129">Toate celelalte activități de proiect create în cadrul acestuia.</span><span class="sxs-lookup"><span data-stu-id="f2246-129">All other project tasks are created under it.</span></span> <span data-ttu-id="f2246-130">Numele activității rădăcină este numele proiectului.</span><span class="sxs-lookup"><span data-stu-id="f2246-130">The name of the root task is the project name.</span></span> <span data-ttu-id="f2246-131">Efortul, datele și durata nodului rădăcină se bazează pe valorile din ierarhia de sub acesta.</span><span class="sxs-lookup"><span data-stu-id="f2246-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="f2246-132">Nu puteți edita proprietățile nodului rădăcină sau șterge nodul rădăcină.</span><span class="sxs-lookup"><span data-stu-id="f2246-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="f2246-133">**Activități rezumat sau container**</span><span class="sxs-lookup"><span data-stu-id="f2246-133">**Summary or container tasks**</span></span> | <span data-ttu-id="f2246-134">O activitate rezumat este o activitate care are subactivități.</span><span class="sxs-lookup"><span data-stu-id="f2246-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="f2246-135">O activitate rezumat nu are niciun efort de lucru sau cost propriu.</span><span class="sxs-lookup"><span data-stu-id="f2246-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="f2246-136">Efortul său de lucru și costurile sunt un cumul al subactivităților.</span><span class="sxs-lookup"><span data-stu-id="f2246-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="f2246-137">Puteți schimba numele unei activități de rezumat, dar nu puteți modifica efortul, datele sau durata, deoarece acestea sunt calculate automat.</span><span class="sxs-lookup"><span data-stu-id="f2246-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="f2246-138">Ștergerea unei activități de rezumat șterge activitatea și toate subactivitățile ei.</span><span class="sxs-lookup"><span data-stu-id="f2246-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="f2246-139">**Activitățile nodului frunză**</span><span class="sxs-lookup"><span data-stu-id="f2246-139">**Leaf node tasks**</span></span> | <span data-ttu-id="f2246-140">O activitate nod frunză reprezintă lucrul cel mai detaliat la proiect.</span><span class="sxs-lookup"><span data-stu-id="f2246-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="f2246-141">Include o estimare a efortului, un număr de resurse planificate, datele de început și de sfârșit planificate și o durată.</span><span class="sxs-lookup"><span data-stu-id="f2246-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="f2246-142">Ierarhia de activități</span><span class="sxs-lookup"><span data-stu-id="f2246-142">Task hierarchy</span></span>  
 <span data-ttu-id="f2246-143">Aveți următoarele opțiuni atunci când creați o ierarhie de activități:</span><span class="sxs-lookup"><span data-stu-id="f2246-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="f2246-144">**Adăugați activitatea**.</span><span class="sxs-lookup"><span data-stu-id="f2246-144">**Add task**.</span></span>   <span data-ttu-id="f2246-145">Puteți adăuga o activitate la o poziție pe care o alegeți în ierarhia de activități.</span><span class="sxs-lookup"><span data-stu-id="f2246-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="f2246-146">Dacă nu selectați o poziție, activitatea nouă apare la sfârșit.</span><span class="sxs-lookup"><span data-stu-id="f2246-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="f2246-147">**Indentați activitatea**.</span><span class="sxs-lookup"><span data-stu-id="f2246-147">**Indent task**.</span></span>   <span data-ttu-id="f2246-148">Indentați o activitate pentru a o face subordonată activității aflate direct deasupra ei.</span><span class="sxs-lookup"><span data-stu-id="f2246-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="f2246-149">**Indentați negativ activitatea**.</span><span class="sxs-lookup"><span data-stu-id="f2246-149">**Outdent task**.</span></span>   <span data-ttu-id="f2246-150">Indentați negativ o activitate, ca să nu mai fie subactivitate a activității sale părinte inițiale.</span><span class="sxs-lookup"><span data-stu-id="f2246-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="f2246-151">**Mutați în sus și în jos**.</span><span class="sxs-lookup"><span data-stu-id="f2246-151">**Move up and Move down**.</span></span>   <span data-ttu-id="f2246-152">Mutați activitățile în sus și în jos în ierarhia lor părinte.</span><span class="sxs-lookup"><span data-stu-id="f2246-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="f2246-153">Mutarea unei activități în sus sau în jos nu are niciun efect asupra efortului, costurilor, datelor sau duratei.</span><span class="sxs-lookup"><span data-stu-id="f2246-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="f2246-154">Atributele activității</span><span class="sxs-lookup"><span data-stu-id="f2246-154">Task attributes</span></span>  
 <span data-ttu-id="f2246-155">Numele unei activități descrie lucrul care trebuie să fie finalizat.</span><span class="sxs-lookup"><span data-stu-id="f2246-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="f2246-156">Utilizați diverse atribute de sarcină activități pentru a descrie cerințele de planificare și personal pentru activitate.</span><span class="sxs-lookup"><span data-stu-id="f2246-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="f2246-157">Planificare atribute</span><span class="sxs-lookup"><span data-stu-id="f2246-157">Schedule attributes</span></span>

 - <span data-ttu-id="f2246-158">Atribuiți valori pentru **Ore de efort** , **Număr de resurse** , **Data de început** , **Data de sfârșit** și **Durată** pentru a stabili planificarea pentru activitate.</span><span class="sxs-lookup"><span data-stu-id="f2246-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="f2246-159">**Efortul** este o estimare a orelor necesare pentru a finaliza activitata.</span><span class="sxs-lookup"><span data-stu-id="f2246-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="f2246-160">**Număr de resurse** este o estimare efectuată de managerul proiectului în activitate, pentru a ajuta la realizarea celui mai bun program posibil.</span><span class="sxs-lookup"><span data-stu-id="f2246-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="f2246-161">**Duraăa** (în zile) indică numărul de zile de lucru necesare pentru a finaliza activitatea.</span><span class="sxs-lookup"><span data-stu-id="f2246-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="f2246-162">Atribute de personal</span><span class="sxs-lookup"><span data-stu-id="f2246-162">Staffing attributes</span></span>

 - <span data-ttu-id="f2246-163">**Rol** , **Unitate organizațională de resurse** , **Număr de resurse** și **Resurse** descriu cerințele de personal pentru activitate.</span><span class="sxs-lookup"><span data-stu-id="f2246-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="f2246-164">**Rol** descrie tipul de resurse necesare pentru a îndeplini activitatea.</span><span class="sxs-lookup"><span data-stu-id="f2246-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="f2246-165">**Unitate organizațională de resurse** indică unitatea organizațională din care ar trebui să fie recrutate resurse pentru această activitate; de asemenea, acest lucru afectează estimarea de costuri și vânzări pentru activitate, deoarece este contabilizat atunci când se stabilește prețul de vânzare unitar pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="f2246-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="f2246-166">**Resurse** înseamnă o resursă generică sau o resursă denumită, atunci când este găsită una.</span><span class="sxs-lookup"><span data-stu-id="f2246-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="f2246-167">Dependențe de activitate</span><span class="sxs-lookup"><span data-stu-id="f2246-167">Task dependencies</span></span>  
 <span data-ttu-id="f2246-168">Aveți posibilitatea să creați relații de precedare între una sau mai multe activități în structură detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="f2246-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="f2246-169">Puteți seta una sau mai multe valori pentru câmpul predecesor în activități, care să indice activitățile de care va depinde.</span><span class="sxs-lookup"><span data-stu-id="f2246-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="f2246-170">Când asociați o valoare de predecesor la o activitate, activitatea poate începe numai atunci când s-au terminat toate activitățile predecesoare.</span><span class="sxs-lookup"><span data-stu-id="f2246-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="f2246-171">Stabilirea acestei dependențe pentru o activitate va avea drept consecință recalcularea datei de început planificate a activității ca cea mai recentă dată de sfârșit a tuturor predecesorilor săi.</span><span class="sxs-lookup"><span data-stu-id="f2246-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="f2246-172">Impactul legat de predecesor pentru o planificare nu este limitat de modul de activitate definit pentru activitate.</span><span class="sxs-lookup"><span data-stu-id="f2246-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="f2246-173">Mod de activitate</span><span class="sxs-lookup"><span data-stu-id="f2246-173">Task mode</span></span>  
 <span data-ttu-id="f2246-174">Modul de activitate este unul dintre factorii importanți care determină planificarea activităților de nod frunză.</span><span class="sxs-lookup"><span data-stu-id="f2246-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="f2246-175">Există două moduri de activitate pentru fiecare activitate: modul de planificare automată și modul de planificare manuală.</span><span class="sxs-lookup"><span data-stu-id="f2246-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="f2246-176">**Planificare automată**.</span><span class="sxs-lookup"><span data-stu-id="f2246-176">**Auto scheduling**.</span></span>   <span data-ttu-id="f2246-177">Când setați modul de activitate la Planificat automat, motorul de planificare a activităților utilizează regulile de planificare pentru următoarele atribute de activitate, pentru a determina planificarea pentru activitate:</span><span class="sxs-lookup"><span data-stu-id="f2246-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="f2246-178">Predecesori</span><span class="sxs-lookup"><span data-stu-id="f2246-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="f2246-179">Efort</span><span class="sxs-lookup"><span data-stu-id="f2246-179">Effort</span></span>  
  
    -   <span data-ttu-id="f2246-180">Număr de resurse</span><span class="sxs-lookup"><span data-stu-id="f2246-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="f2246-181">Datele de sfârșit și de început</span><span class="sxs-lookup"><span data-stu-id="f2246-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="f2246-182">**Regulile mele de planificare**.</span><span class="sxs-lookup"><span data-stu-id="f2246-182">**Scheduling rules**.</span></span>   <span data-ttu-id="f2246-183">Data de început a unei activități nod frunză care nu are predecesori impliciți pentru data de început a planificării proiectului.</span><span class="sxs-lookup"><span data-stu-id="f2246-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="f2246-184">Durata unei activități nod frunză se calculează întotdeauna ca numărul de zile lucrătoare dintre datele sale de început și de sfârșit.</span><span class="sxs-lookup"><span data-stu-id="f2246-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="f2246-185">Când o activitate este planificată automat, motorul de planificare urmează regulile de mai jos:</span><span class="sxs-lookup"><span data-stu-id="f2246-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="f2246-186">Datele de început și de sfârșit ale unei activități trebuie să fie întotdeauna zile lucratoare, conform calendarului de planificare a proiectului</span><span class="sxs-lookup"><span data-stu-id="f2246-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="f2246-187">Data de început a unei activități care are predecesori devine implicit cea mai recentă dată de sfârșit a predecesorilor săi</span><span class="sxs-lookup"><span data-stu-id="f2246-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="f2246-188">Efort = numărul de persoane \* durata \* orele dintr-o zi de lucru standard din calendarul proiectului</span><span class="sxs-lookup"><span data-stu-id="f2246-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="f2246-189">**Planificare manuală**.</span><span class="sxs-lookup"><span data-stu-id="f2246-189">**Manual scheduling**.</span></span>   <span data-ttu-id="f2246-190">În unele cazuri, ați putea dori să vă abateți de la aceste reguli.</span><span class="sxs-lookup"><span data-stu-id="f2246-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="f2246-191">În aceste cazuri, puteți seta modul de activitate pentru activitatea care va fi planificată manual.</span><span class="sxs-lookup"><span data-stu-id="f2246-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="f2246-192">Aceasta oprește ca motorul de planificare să calculeze valorile pentru alte atribute de planificare.</span><span class="sxs-lookup"><span data-stu-id="f2246-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="f2246-193">Setarea de predecesori pentru activități afectează întotdeauna data de început a activității dependente.</span><span class="sxs-lookup"><span data-stu-id="f2246-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="f2246-194">Creați o structură detaliată a proiectului</span><span class="sxs-lookup"><span data-stu-id="f2246-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="f2246-195">Accesați **Project Service > Proiecte**.</span><span class="sxs-lookup"><span data-stu-id="f2246-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="f2246-196">Faceți clic pe proiectul la care doriți să lucrați.</span><span class="sxs-lookup"><span data-stu-id="f2246-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="f2246-197">În bara din partea de sus a ecranului, selectați săgeata în jos de lângă numele proiectului, apoi faceți clic pe Structură detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="f2246-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="f2246-198">Pentru a adăuga o activitate, faceți clic pe **Adăugare activitate**.</span><span class="sxs-lookup"><span data-stu-id="f2246-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="f2246-199">Completați câmpurile pentru activitate, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="f2246-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="f2246-200">Continuați să adăugați activități până când se finalizează structură detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="f2246-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="f2246-201">În timp ce creați structură detaliată a proiectului, puteți face următoarele pentru a vă organiza activitățile:</span><span class="sxs-lookup"><span data-stu-id="f2246-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="f2246-202">Selectați o activitate și faceți clic pe **Indentare** pentru a o muta sub o altă activitate sau faceți clic pe Indentare negativă pentru a o muta în afară cu un nivel.</span><span class="sxs-lookup"><span data-stu-id="f2246-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="f2246-203">Selectați o activitate și faceți clic pe **Mutare în sus** sau pe **Mutare în jos** pentru a o muta în sus sau în jos în listă.</span><span class="sxs-lookup"><span data-stu-id="f2246-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="f2246-204">Faceți clic pe **Ascundere Gantt** pentru a ascunde diagrama Gantt și faceți clic pe **Afișare Gantt** pentru a o afișa din nou.</span><span class="sxs-lookup"><span data-stu-id="f2246-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="f2246-205">Selectați o perioadă diferită pentru diagrama Gantt în **Scară de timp**.</span><span class="sxs-lookup"><span data-stu-id="f2246-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="f2246-206">Pentru a adăuga rolurile specificate în structura detaliată a proiectului pentru membrii echipei proiectului dvs., faceți clic pe **Generare echipă de proiect**.</span><span class="sxs-lookup"><span data-stu-id="f2246-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="f2246-207">Faceți clic pe **Salvare** în colțul din dreapta jos al ecranului după ce ați terminat de efectuat modificările.</span><span class="sxs-lookup"><span data-stu-id="f2246-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f2246-208">Consultați și</span><span class="sxs-lookup"><span data-stu-id="f2246-208">See Also</span></span>  
 [<span data-ttu-id="f2246-209">Ghidul managerului de proiect</span><span class="sxs-lookup"><span data-stu-id="f2246-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
