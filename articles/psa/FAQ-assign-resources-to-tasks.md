---
title: Atribuiți o resursă la o activitate
description: Acest subiect furnizează informații despre modul de atribuire a resurselor la activități.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082985"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="2e9f7-103">Atribuiți o resursă la o activitate</span><span class="sxs-lookup"><span data-stu-id="2e9f7-103">Assign a resource to a task</span></span>

<span data-ttu-id="2e9f7-104">Există trei moduri de atribui o resursă la o activitate în Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="2e9f7-105">Rezervați o resursă ca un membru al echipei și apoi atribuiți resursa la o sarcină</span><span class="sxs-lookup"><span data-stu-id="2e9f7-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="2e9f7-106">Puteți adăuga o resursă la echipa proiectului și apoi puteți atribui resursa la sarcini în planificarea proiectului.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="2e9f7-107">În fila **Membru echipă** adăugați un nou membru al echipei selectând **Nou**.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="2e9f7-108">Panoul **Creare rapidă membru echipă** se deschide, unde puteți selecta numele resursei care se poate rezerva puteți seta un rol.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="2e9f7-109">Selectați una dintre următoarele metode de alocare pentru a rezerva resursa:</span><span class="sxs-lookup"><span data-stu-id="2e9f7-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="2e9f7-110">**Capacitate completă** rezervă întreaga capacitate a resursei pentru datele de pornire și finalizare indicate.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="2e9f7-111">**Capacitate procentaj** rezervă resursa pentru un procent din capacitatea resursei pentru datele de pornire și finalizare indicate.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="2e9f7-112">**După ore - Distribuiți uniform** rezervă resursa pentru un anumit număr de ore, distribuindu-le uniform pe zi între datele de început și de sfârșit indicate.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="2e9f7-113">**După ore - Încărcare frontală** rezervă resursa pentru un anumit număr de ore, încărcând frontal timpul pe zi între datele de început și sfârșit indicate.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="2e9f7-114">**Niciuna** adaugă resursa la echipă, dar nu creează rezervări care să le absoarbă capacitatea.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="2e9f7-115">Pe grila **Planificare** pentru o activitate, faceți clic pe pictograma **Resursă** în celula resursei, apoi selectați **Membrii echipei** , pe care tocmai i-ați adăugat.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="2e9f7-116">În filele **Membru echipă** și **Reconciliere** , resursa afișează orele rezervate și atribuite.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="2e9f7-117">Orele ar trebui să fie aceleași, dar nu neapărat, deoarece rezervările și atribuirile nu sunt strâns cuplate.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="2e9f7-118">Fila **Reconciliere** vă oferă detalii atunci când acestea sunt diferite, cum ar fi când atribuiți unei resurse mai multe ore decât ați rezervat.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="2e9f7-119">Dacă este necesar, puteți corecta informațiile prin extinderea rezervărilor resursei sau prin modificarea atribuirii.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="2e9f7-120">Creați un membru al echipei prin atribuirea de sarcini</span><span class="sxs-lookup"><span data-stu-id="2e9f7-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="2e9f7-121">Când creați un membru al echipei prin atribuirea de sarcini, creați un substituent sau o resursă generică care descrie caracteristicile resursei care doriți să lucreze la final pe sarcini.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="2e9f7-122">Apoi generați o solicitare (sau transmiteți o cerere folosind solicitarea) care este folosită pentru căutarea și rezervarea respectivei resurse.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="2e9f7-123">Pe grila **Planificare** pentru o activitate, faceți clic pe pictograma **Resursă** în celula resursei.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="2e9f7-124">Tastați un nume pentru a servi drept substituent pentru numele resursei.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="2e9f7-125">De exemplu „Manager de Program”.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="2e9f7-126">Selectați **Creare** , iar în câmpul **Creare rapidă membru echipă** , setați rolul pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="2e9f7-127">Puteți continua să atribuiți sarcini acestei resurse substituent prin selectarea resursei pe **Selectorul de resurse** pentru sarcină.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="2e9f7-128">Acestea sunt listate la **Membrii echipei**.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="2e9f7-129">Când ați terminat alocarea resursei generice, selectați resursa generică pe fila **Echipă** și selectați **Generare cerință** pentru a crea o cerință de resurse pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="2e9f7-130">Selectați **Rezervare** pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="2e9f7-131">Puteți utiliza Tabloul de planificare pentru a găsi și a rezerva o resursă reală.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="2e9f7-132">Puteți de asemenea remite solicitarea de realizare de către un manager de resurse.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="2e9f7-133">Când resursa generică este îndeplinită cu o anumită resursă, resursa generică este scoasă din echipă și atribuirile de sarcini pentru resursa generică sunt atribuite resursei indicate care a îndeplinit cerința de resurse a resursei generice.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="2e9f7-134">Atribuiți o resursă din lista tuturor resurselor care se pot rezerva.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="2e9f7-135">Puteți utiliza caseta de căutare în **Selectorul de resurse** pentru a căuta toate resursele care se pot rezerva și pentru a le atribui la o sarcină.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="2e9f7-136">Resursele atribuite în acest mod sunt adăugate echipei fără rezervări.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="2e9f7-137">Acest lucru este similar cu adăugarea unui membru al echipei și selectarea Niciunul ca metodă de alocare.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="2e9f7-138">Resursa este afișată în filele **Echipă** și **Reconciliere** ca resurse care au numai atribuiri și un deficit de rezervare.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="2e9f7-139">Rezervați-le dacă doriți să le utilizați disponibilitatea.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="2e9f7-140">Pe grila **Planificare** pentru o activitate, faceți clic pe pictograma **Resursă** în celula resursei.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="2e9f7-141">Începeți să tastați un nume.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-141">Start typing a name.</span></span> <span data-ttu-id="2e9f7-142">Rezultatele căutării sunt afișate în **Selectorul de resurse** în **Alte resurse**.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="2e9f7-143">Selectați resursa pe care doriți să o atribuiți activității.</span><span class="sxs-lookup"><span data-stu-id="2e9f7-143">Select the resource that you want to assign to the task.</span></span>

