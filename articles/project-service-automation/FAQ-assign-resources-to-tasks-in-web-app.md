---
title: Cum atribui o resursă care se poate rezerva unei activități în aplicația web
description: Prezentare generală a modurilor în care puteți atribui resurse care pot fi rezervate.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754842"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="5a1cf-103">Cum atribui o resursă care se poate rezerva unei sarcină în aplicația web (aplicația Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="5a1cf-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="5a1cf-104">Există două modalități de a atribui o resursă unei sarcini în Project Service.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="5a1cf-105">Puteți rezerva o resursă ca un membru al echipei și apoi să o atribuiți la o sarcină.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="5a1cf-106">Sau puteți că creați un membru al echipei generic prin intermediul atribuirii rolurilor pe sarcini, să generați o echipă și apoi să îndepliniți cerințele subiacente cu o resursă desemnată.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="5a1cf-107">Rețineți că dacă doriți să atribuiți o resursă care se poate rezerva la o sarcină, membrul echipei de resurse care se poate rezerva trebuie să aibă rezervări suficiente disponibile.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="5a1cf-108">Starea rezervării trebuie să fie Tip comitere Rezervare fermă și Stare Comisă.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="5a1cf-109">În cazul în care nu există suficiente rezervări pentru resursă, Project Service elimină alocarea și afișează următorul mesaj de eroare:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="5a1cf-110">*Imposibil de alocat resursa la sarcină - Următoarea/ următoarele resurse nu are/au suficiente ore rezervate pe proiect*</span><span class="sxs-lookup"><span data-stu-id="5a1cf-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="5a1cf-111">Rezervați o resursă ca un membru al echipei și apoi atribuiți resursa la o sarcină.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="5a1cf-112">Cu această metodă adăugați o resursă la echipa proiectului și apoi atribuiți sarcini resursei în planificarea proiectului.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="5a1cf-113">Iată cum se face:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="5a1cf-114">Pe grila de membru echipă, adăugați un nou membru al echipei selectând **Nou**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="5a1cf-115">Pe ecranul Creare rapidă membru echipă, selectați numele resursei care se poate rezerva și setați un rol.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="5a1cf-116">Selectați datele **De la** și **Până la**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="5a1cf-117">![Captura de ecran a adăugării membrilor echipei](media/FAQ-Resources-to-Tasks2-1.png "Captura de ecran a adăugării membrilor echipei")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="5a1cf-118">Selectați una dintre următoarele metode de alocare pentru a rezerva resursa:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="5a1cf-119">**Capacitate completă** rezervă întreaga capacitate a resursei pentru datele de pornire și finalizare indicate.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="5a1cf-120">**Capacitate procentaj** rezervă resursa pentru un procent din capacitatea resursei pentru datele de pornire și finalizare indicate.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="5a1cf-121">**După ore - Distribuiți uniform** rezervă resursa pentru un anumit număr de ore, distribuind-o uniform pe zi intre datele de început și sfârșit indicate.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="5a1cf-122">**După ore - Încărcare frontală** rezervă resursa pentru un anumit număr de ore, încărcând frontal timpul pe zi între datele de început și sfârșit indicate.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="5a1cf-123">Nu selectați **Niciuna**, deoarece acest lucru adaugă resursa la echipă, dar nu creează rezervări care să absoarbă capacitatea resursei.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="5a1cf-124">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-124">Select **Save**.</span></span>

    <span data-ttu-id="5a1cf-125">Rețineți că orele rezervării trebuie să fie suficiente pentru a acoperi orele de efort si intervalele de dată de ale sarcinilor pentru care atribuiți această resursă.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="5a1cf-126">În cazul în care acestea nu sunt aliniate, nu puteți asocia resursa la sarcină.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="5a1cf-127">Pentru structura detaliată a proiectului (WBS) pentru sarcină, faceți clic pe lista verticală din celula resursei.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="5a1cf-128">Apoi:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-128">Then:</span></span> 

    1. <span data-ttu-id="5a1cf-129">Selectați **Adăugare**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-129">Select **Add**.</span></span>
    2. <span data-ttu-id="5a1cf-130">Selectați lista derulantă de sub **Resurse** și selectați membrul de echipă adăugat anterior.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="5a1cf-131">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-131">Select **OK**.</span></span> <span data-ttu-id="5a1cf-132">Membrul echipei este acum atribuit la sarcină.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="5a1cf-133">![Screenshot de adăugare a resurselor cu WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot de adăugare a resurselor cu WBS")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="5a1cf-134">Pe grila de membru echipă, veți vedea totalul orelor atribuite ale resursei, sub Ore alocate.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="5a1cf-135">Acesta va fi mai mic sau egal cu orele rezervate pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5a1cf-136">![Captură de ecran cu ore alocate pentru o resursă](media/FAQ-Resources-to-Tasks2-3.png "Captură de ecran cu ore alocate pentru o resursă")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="5a1cf-137">În cazul în care sarcina pe care încercați să o atribuiți resursei începe după data de sfârșit a rezervărilor pentru de resursă, resursa nu va apărea în lista derulantă.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="5a1cf-138">Rețineți că aveți posibilitatea să îi atribuiți unei resurse mai multe ore decât orele lor rezervate dacă resursa are capacitate rămasă neatribuită.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="5a1cf-139">În acest caz resursa va doar fi parțial atribuită, în funcție de rezervări.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="5a1cf-140">Puteți vedea aceste ore de sarcini rămase neatribuite prin adăugarea coloanei Ore neacoperite de personal la structura detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="5a1cf-141">În cazul în care resursele sunt atribuite la orele lor rezervate (orele lor rezervate sunt egale cu orele lor atribuite), veți vedea următorul mesaj de eroare atunci când încercați să le atribuiți alte sarcini:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="5a1cf-142">*Imposibil de alocat resursa la sarcină - Următoarea/ următoarele resurse nu are/au suficiente ore rezervate pe proiect.*</span><span class="sxs-lookup"><span data-stu-id="5a1cf-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="5a1cf-143">În plus, membrul echipei care este managerul implicit de proiect care este adăugat la echipă atunci când creați proiectul este adăugat fără rezervări și nu îi pot fi atribuite sarcini.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="5a1cf-144">Aceștia nu apar în lista verticală de resurse pentru sarcini.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="5a1cf-145">În cazul în care doriți să atribuiți această resursă, trebuie să le scoateți din echipă și apoi să le adăugați din nou cu o metodă de alocare diferită de Niciuna.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="5a1cf-146">Motivul pentru care acestea sunt adăugate la echipă atunci când este creat proiectul este ca fiecare proiect să aibă cel puțin o persoană implicită care face aprobarea.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="5a1cf-147">Creați un membru generic al echipei prin atribuirea de roluri pe sarcini</span><span class="sxs-lookup"><span data-stu-id="5a1cf-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="5a1cf-148">Această metodă asigură că resursele au suficiente rezervări pentru sarcini.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="5a1cf-149">Mai întâi, creați un substituent sau o resursă generică care descrie caracteristicile resursei care doriți să lucreze la final pe sarcini, prin generarea unei echipe după atribuirea rolurilor la sarcini.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="5a1cf-150">Iată cum se face:</span><span class="sxs-lookup"><span data-stu-id="5a1cf-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="5a1cf-151">Selectați o sarcină pe structura detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="5a1cf-152">Selectați pictograma derulantă **Rol atribuit** din celula resursei.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="5a1cf-153">Selectați lista derulantă **Rol** și selectați rolul pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="5a1cf-154">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="5a1cf-155">![Captură de ecran a utilizării WBS pentru a adăuga o resursă](media/FAQ-Resources-to-Tasks2-4.png "Captură de ecran a utilizării WBS pentru a adăuga o resursă")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="5a1cf-156">Odată ce ați completat atribuirea de roluri la sarcini în WBS, selectați **Generare echipă de proiect**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="5a1cf-157">Project Service creează numărul minim de membri ai echipei generice pe baza rolurilor, a unităților organizaționale din care provin resursele și a calendarului de proiect prin agregarea atribuirilor de sarcini.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5a1cf-158">![Captură de ecran a echipei de generare a proiectului](media/FAQ-Resources-to-Tasks2-5.png "Captură de ecran a echipei de generare a proiectului")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="5a1cf-159">Pr grila de Membru al echipei, veți vedea resursele de tip Resursă generică cu rolul și numele poziției.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="5a1cf-160">În cazul în care sunt necesare două resurse pentru un rol pentru a finaliza lucrările, caracteristica Generare echipă creează doi membri ai echipei și utilizează numele poziției pentru a-i diferenția.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5a1cf-161">![Captură de ecran cu adăugarea a două resurse generice](media/FAQ-Resources-to-Tasks2-6.png "Captură de ecran cu adăugarea a două resurse generice")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="5a1cf-162">Puteți deschide cerința de resurse subiacente pentru membrul generic de echipă prin selectarea link-ul de la Cerință de resurse.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="5a1cf-163">![Captură de ecran cu cerința de deschidere de resurse subiacente](media/FAQ-Resources-to-Tasks2-7.png "Captură de ecran cu cerința de deschidere de resurse subiacente")</span><span class="sxs-lookup"><span data-stu-id="5a1cf-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="5a1cf-164">Selectați **Rezervare** pentru resursa generică și apoi puteți folosi tabloul de planificare pentru a găsi și rezerva o resursă reală.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="5a1cf-165">Puteți trimite solicitarea de realizare de către un manager de resurse, selectând **Remite solicitare**.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="5a1cf-166">Când resursa generică este îndeplinită cu o anumită resursă, resursa generică este scoasă din echipă și atribuirile de sarcini pentru resursa generică sunt atribuite resursei indicate care a îndeplinit cerința de resurse a resursei generice.</span><span class="sxs-lookup"><span data-stu-id="5a1cf-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

