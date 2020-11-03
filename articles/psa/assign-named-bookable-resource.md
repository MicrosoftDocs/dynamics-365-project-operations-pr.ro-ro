---
title: Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini
description: Acest subiect oferă informații despre cum să rezervați resurse numite pentru echipe de proiect și despre atribuirea lor către activități.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082915"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="1688c-103">Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini</span><span class="sxs-lookup"><span data-stu-id="1688c-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1688c-104">Puteți adăuga o resursă numită echipei dvs. de proiect, rezervând-o direct pe echipă.</span><span class="sxs-lookup"><span data-stu-id="1688c-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="1688c-105">Pentru a face acest lucru, efectuați următorii pași.</span><span class="sxs-lookup"><span data-stu-id="1688c-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="1688c-106">În Project Service Automation, accesați **Proiecte** și selectați și deschideți proiectul pentru care faceți rezervarea.</span><span class="sxs-lookup"><span data-stu-id="1688c-106">In  Project Service Automation, go to **Projects** , and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="1688c-107">Pe pagina **Proiect** , în fila **Echipă** , faceți clic pe **Nou**.</span><span class="sxs-lookup"><span data-stu-id="1688c-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Adăugarea unui membru al echipei din fila echipă](media/RM-how-to-1.png)

3. <span data-ttu-id="1688c-109">În caseta de dialog **Creare rapidă membru echipă proiect** , selectați resursa care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="1688c-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="1688c-110">Câmpul **Rol** se va popula cu rolul implicit al resursei, dacă aceasta are unul atribuit.</span><span class="sxs-lookup"><span data-stu-id="1688c-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="1688c-111">Aveți posibilitatea să schimbați rolul, dacă este necesar.</span><span class="sxs-lookup"><span data-stu-id="1688c-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="1688c-112">Selectați datele de la și până la care resursa va fi necesară și selectați metoda de alocare a capacității resursei.</span><span class="sxs-lookup"><span data-stu-id="1688c-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="1688c-113">Dacă doriți ca membrul echipei să fie un aprobator de proiect, selectați **Da** în câmpul **Aprobator proiect**.</span><span class="sxs-lookup"><span data-stu-id="1688c-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="1688c-114">Acest lucru va însemna că membrul echipei poate aproba intrările de timp și cheltuieli remise pentru acest proiect.</span><span class="sxs-lookup"><span data-stu-id="1688c-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="1688c-115">Faceţi clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="1688c-115">Click **Save**.</span></span>

![Adăugarea unui membru al echipei în formularul de creare rapidă](media/RM-how-to-2.png)


<span data-ttu-id="1688c-117">Acum aveți posibilitatea să atribuiți resursa rezervată activităților din proiect.</span><span class="sxs-lookup"><span data-stu-id="1688c-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="1688c-118">Pe pagina **Proiect** , faceți clic pe fila **Planificare** pentru a atribui activități la noua resursă.</span><span class="sxs-lookup"><span data-stu-id="1688c-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="1688c-119">Selectorul de resurse care este lansat din câmpul **Resurse** din grila de activități va afișa membrii echipei pe care îi puteți selecta.</span><span class="sxs-lookup"><span data-stu-id="1688c-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Atribuirea unui membru al echipei la o activitate din fila planificare](media/RM-how-to-3.png)

<span data-ttu-id="1688c-121">În versiunea 3 pentru Project Service Automation (PSA), rezervările de resurse și atribuirile de activități nu sunt strâns cuplate.</span><span class="sxs-lookup"><span data-stu-id="1688c-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="1688c-122">Aceasta înseamnă că atunci când utilizați selectorul de resurse din planificare, aveți posibilitatea să atribuiți activități membrilor echipei pentru mai multe ore decât acoperă rezervările lor pe proiect.</span><span class="sxs-lookup"><span data-stu-id="1688c-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="1688c-123">Puteți vedea diferențele dintre rezervările membrilor echipei și atribuiri în fila **Echipă** sau în fila **Reconciliere resurse**. De asemenea, aveți posibilitatea să reconciliați diferențele dintre rezervări și atribuiri pentru resurse la un nivel mai detaliat.</span><span class="sxs-lookup"><span data-stu-id="1688c-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Fila Reconciliere resurse](media/RM-how-to-4.png)

<span data-ttu-id="1688c-125">De asemenea, puteți utiliza selectorul de resurse în fila **Planificare** pentru a căuta și selecta resurse rezervabile care nu fac deja parte din echipa de proiect.</span><span class="sxs-lookup"><span data-stu-id="1688c-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="1688c-126">Acestea sunt afișate în selectorul de resurse ca **Alte resurse**.</span><span class="sxs-lookup"><span data-stu-id="1688c-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Atribuirea unei resurse de membru non-echipă la o activitate](media/RM-how-to-5.png)

<span data-ttu-id="1688c-128">Când faceți acest lucru, resursa este adăugată la echipa de proiect și atribuită sarcinii, dar nu sunt generate rezervări.</span><span class="sxs-lookup"><span data-stu-id="1688c-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membru al echipei cu atribuiri și fără rezervări](media/RM-how-to-6.png)

<span data-ttu-id="1688c-130">Aveți posibilitatea să utilizați capacitatea Extindere rezervare a filei **Reconciliere** sau **Tablou de planificare** pentru a rezerva capacitatea resursei la proiect.</span><span class="sxs-lookup"><span data-stu-id="1688c-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Extinderea rezervărilor pentru un membru al echipei în fila reconciliere resurse](media/RM-how-to-7.png)

<span data-ttu-id="1688c-132">După ce un membru al echipei este rezervat în cadrul proiectului dvs., aveți posibilitatea să utilizați Menține rezervările sau să utilizați direct Tabloul de planificare pentru a gestiona rezervările acestuia.</span><span class="sxs-lookup"><span data-stu-id="1688c-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
