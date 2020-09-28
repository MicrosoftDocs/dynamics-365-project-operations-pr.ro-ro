---
title: Considerente de actualizare pentru structura detaliată a proiectului
description: Acest subiect oferă informații despre actualizarea structurii detaliate a proiectului de la Project Service Automation 2.x la 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754782"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="dd859-103">Considerente de actualizare pentru structura detaliată a proiectului</span><span class="sxs-lookup"><span data-stu-id="dd859-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="dd859-104">Acest subiect oferă informații despre actualizarea structurii detaliate a proiectului de la Project Service Automation 2.x la 3.x.</span><span class="sxs-lookup"><span data-stu-id="dd859-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="dd859-105">Acest subiect definește starea de sănătate a unui proiect în Project Service Automation (PSA) care este necesar pentru o actualizare de succes.</span><span class="sxs-lookup"><span data-stu-id="dd859-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="dd859-106">Există, de asemenea, informații despre condițiile comune de blocare care vor duce la eșuarea actualizării.</span><span class="sxs-lookup"><span data-stu-id="dd859-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="dd859-107">Pentru mai multe informații despre definirea activităților de proiect și a funcțiilor lor în cadrul unei planificări de proiect, consultați [Planificări de proiect](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="dd859-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="dd859-108">Entități-cheie</span><span class="sxs-lookup"><span data-stu-id="dd859-108">Key entities</span></span>
<span data-ttu-id="dd859-109">Pentru o structură detaliată a proiectului deja încărcată cu resurse, sunt necesare următoarele entități:</span><span class="sxs-lookup"><span data-stu-id="dd859-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="dd859-110">Proiect</span><span class="sxs-lookup"><span data-stu-id="dd859-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="dd859-111">Echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="dd859-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="dd859-112">Sarcina proiectului</span><span class="sxs-lookup"><span data-stu-id="dd859-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="dd859-113">Atribuiri de resurse</span><span class="sxs-lookup"><span data-stu-id="dd859-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="dd859-114">Dependența sarcinii proiectului</span><span class="sxs-lookup"><span data-stu-id="dd859-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="dd859-115">Resurse ce se pot rezerva</span><span class="sxs-lookup"><span data-stu-id="dd859-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="dd859-116">Pentru a defini o resursă încărcată în structura detaliată a proiectului, trebuie să parcurgeți următorii pași:</span><span class="sxs-lookup"><span data-stu-id="dd859-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="dd859-117">Creați un nou proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-117">Create a new project.</span></span> <span data-ttu-id="dd859-118">Pentru mai multe informații despre modul de creare a unui proiect nou, consultați [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="dd859-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="dd859-119">Creați una sau mai multe activități.</span><span class="sxs-lookup"><span data-stu-id="dd859-119">Create one or more tasks.</span></span> <span data-ttu-id="dd859-120">Pentru mai multe informații despre modul de creare a unei activități, consultați [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="dd859-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="dd859-121">Definiți dependențele de activitate.</span><span class="sxs-lookup"><span data-stu-id="dd859-121">Define the task dependencies.</span></span> <span data-ttu-id="dd859-122">Pentru informații suplimentare, consultați [Dependența sarcinilor de proiect](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="dd859-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="dd859-123">Atribuiți membri de echipă de proiect la proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-123">Assign project team members to the project.</span></span> <span data-ttu-id="dd859-124">Pentru mai multe informații, consultați [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="dd859-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="dd859-125">Atribuiți membri de echipă de proiect la activități.</span><span class="sxs-lookup"><span data-stu-id="dd859-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="dd859-126">Pentru mai multe informații, consultați [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="dd859-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="dd859-127">Relații echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="dd859-127">Project team relationships</span></span>

<span data-ttu-id="dd859-128">Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:</span><span class="sxs-lookup"><span data-stu-id="dd859-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="dd859-129">Toți membrii echipei de proiect trebuie să fie asociați cu o resursă care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="dd859-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="dd859-130">Toți membrii echipei de proiect trebuie să fie asociați în cadrul aceluiași proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="dd859-131">Relații activități de proiect</span><span class="sxs-lookup"><span data-stu-id="dd859-131">Project task relationships</span></span>
<span data-ttu-id="dd859-132">Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:</span><span class="sxs-lookup"><span data-stu-id="dd859-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="dd859-133">Orice activități asociate trebuie să fie asociate cu același proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="dd859-134">Fiecare activitate de linie trebuie să aibă o activitate părinte.</span><span class="sxs-lookup"><span data-stu-id="dd859-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="dd859-135">Fiecare activitate trebuie să aibă un proiect părinte.</span><span class="sxs-lookup"><span data-stu-id="dd859-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="dd859-136">Condiții valabile</span><span class="sxs-lookup"><span data-stu-id="dd859-136">Valid conditions</span></span>

- <span data-ttu-id="dd859-137">Toate duratele activităților trebuie să fie mai mari sau egale cu (>=) o oră și mai mici de 1.800.000 minute (1.250 de zile). \*</span><span class="sxs-lookup"><span data-stu-id="dd859-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="dd859-138">Toate activitățile trebuie să aibă o dată de începere nu mai devreme de 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="dd859-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="dd859-139">Toate activitățile trebuie să aibă o dată de începere nu mai târziu de 17 ani de la data curentă.\*</span><span class="sxs-lookup"><span data-stu-id="dd859-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="dd859-140">Toate activitățile trebuie să aibă o dată de începere anterioară sau egală cu data lor de încheiere.</span><span class="sxs-lookup"><span data-stu-id="dd859-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="dd859-141">Toate tipurile de tranzacții pe clasificări (cheltuieli, materiale, taxe și timp) trebuie să aibă valori pentru **Unitatea implicită** și **Grup unități**.</span><span class="sxs-lookup"><span data-stu-id="dd859-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="dd859-142">Formatele de dată cu litere trebuie evitate.</span><span class="sxs-lookup"><span data-stu-id="dd859-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="dd859-143">Pași de atenuare potențiali</span><span class="sxs-lookup"><span data-stu-id="dd859-143">Potential mitigation steps</span></span>
- <span data-ttu-id="dd859-144">Utilizați Căutare avansată pentru a identifica sarcinile de proiect care nu conțin un ID de proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="dd859-145">Utilizați Căutare avansată pentru a identifica sarcinile proiectului în care durata programată este mai mare decât > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="dd859-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="dd859-146">Înainte de a face orice schimbare de date, ar trebui să investigați orice personalizare asociată entității care ar fi putut duce la obținerea datelor într-o stare proastă.</span><span class="sxs-lookup"><span data-stu-id="dd859-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="dd859-147">Aceste personalizări ar trebui abordate înainte de a continua cu actualizări legate de date.</span><span class="sxs-lookup"><span data-stu-id="dd859-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="dd859-148">Pentru sarcinile identificate care au rămas orfane, luați în considerare ștergerea acestor sarcini dacă nu sunt necesare sau dacă ar trebui asociate cu proiectul părinte corect.</span><span class="sxs-lookup"><span data-stu-id="dd859-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="dd859-149">Pentru orice sarcini în care durata este mai mare de 1.250 de zile, luați în considerare adăugarea mai multor sarcini pentru a reprezenta durata totală, dacă este posibil.</span><span class="sxs-lookup"><span data-stu-id="dd859-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="dd859-150">Elementele notate cu un asterisc (\*) au limite care se datorează faptului că managementul relațiilor cu clienții (CRM) suportă numai 7.320 extinderi de recurență.</span><span class="sxs-lookup"><span data-stu-id="dd859-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="dd859-151">Trebuie să vă mențineți sub această limită.</span><span class="sxs-lookup"><span data-stu-id="dd859-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="dd859-152">Relații atribuire de resurse</span><span class="sxs-lookup"><span data-stu-id="dd859-152">Resource Assignment relationships</span></span>
<span data-ttu-id="dd859-153">Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:</span><span class="sxs-lookup"><span data-stu-id="dd859-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="dd859-154">Toate atribuirile de resurse într-o structură detaliată a proiectului trebuie să fie legate de același proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="dd859-155">Toate atribuirile de resurse într-o structură detaliată a proiectului trebuie să fie asociate cu membri ai echipei de proiect din același proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="dd859-156">Pași de atenuare potențiali</span><span class="sxs-lookup"><span data-stu-id="dd859-156">Potential mitigation steps</span></span>
- <span data-ttu-id="dd859-157">Identificați toate activitățile care nu se încadrează în condițiile descrise mai sus.</span><span class="sxs-lookup"><span data-stu-id="dd859-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="dd859-158">Orice alocări de resurse care nu mai sunt valabile ar trebui să fie șterse.</span><span class="sxs-lookup"><span data-stu-id="dd859-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="dd859-159">Relațiile dependenței de activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="dd859-159">Project task dependency relationships</span></span>
<span data-ttu-id="dd859-160">Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:</span><span class="sxs-lookup"><span data-stu-id="dd859-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="dd859-161">Toate dependențele de activitate de proiect trebuie să fie corelate cu același proiect.</span><span class="sxs-lookup"><span data-stu-id="dd859-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="dd859-162">O activitate nu poate avea aceeași dependență la care se face referire de mai multe ori.</span><span class="sxs-lookup"><span data-stu-id="dd859-162">A task can't have the same dependency referenced more than once.</span></span>