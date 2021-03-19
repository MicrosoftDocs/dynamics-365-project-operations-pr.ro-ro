---
title: Atribuirea de resurse generice rezervabile unei activități și unei echipe de proiect
description: Acest subiect oferă informații despre rezervarea resurselor generice pentru activități și echipe de proiect.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291409"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="5f54d-103">Atribuiți resurse generice care se pot rezerva unei activități și generați cerințe de resurse</span><span class="sxs-lookup"><span data-stu-id="5f54d-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f54d-104">Pe lângă rezervarea și atribuirea resurselor denumite sau reale proiectului dvs., aveți posibilitatea să atribuiți resurse generice activităților de proiect.</span><span class="sxs-lookup"><span data-stu-id="5f54d-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="5f54d-105">Aceste resurse pot servi ca substituenți pentru resursele numite până când sunteți gata să alocați ca personal pentru proiectul dvs. resurse numite.</span><span class="sxs-lookup"><span data-stu-id="5f54d-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="5f54d-106">În Project Service Automation (PSA), deschideți pagina **Proiect** și în fila **Planificare**, introduceți numele de poziție al resursei generice în celula **Resursă** a planificării.</span><span class="sxs-lookup"><span data-stu-id="5f54d-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="5f54d-107">Sau, aveți posibilitatea să faceți clic pe pictograma **Resursă** din celulă pentru a deschide selectorul de resurse, apoi introduceți numele resursei generice pe care doriți să o creați.</span><span class="sxs-lookup"><span data-stu-id="5f54d-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Crearea și atribuirea unui membru al echipei generice](media/RM-how-to-9.png)

<span data-ttu-id="5f54d-109">Acest lucru va deschide panoul **Creare rapidă: membru al echipei de proiect**.</span><span class="sxs-lookup"><span data-stu-id="5f54d-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="5f54d-110">Introduceți rolul și unitatea organizațională a membrului echipei de resurse generice și apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="5f54d-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Creare rapidă membru al echipei generice](media/RM-how-to-10.png)

3. <span data-ttu-id="5f54d-112">După ce ați creat noul membru al echipei de resurse generice, acesta este atribuit activității.</span><span class="sxs-lookup"><span data-stu-id="5f54d-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="5f54d-113">Aveți posibilitatea să continuați să atribuiți acea resursă generică altor activități din planificarea activităților.</span><span class="sxs-lookup"><span data-stu-id="5f54d-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Atribuirea membrului de echipă generic existent la activități](media/RM-how-to-11.png)

4. <span data-ttu-id="5f54d-115">După ce ați atribuit resursa generică, aveți posibilitatea să generați o cerință de resursă și să o îndepliniți prin rezervarea directă sau prin trimiterea unei solicitări de resurse către un manager de resurse.</span><span class="sxs-lookup"><span data-stu-id="5f54d-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generarea unei cerințe pentru un membru al echipei generice](media/RM-how-to-12.png)

<span data-ttu-id="5f54d-117">În grila de membru al echipei, pe lângă posibilitatea de a utiliza selectorul de resurse așa s-a menționat mai sus, puteți adăuga direct resurse generice.</span><span class="sxs-lookup"><span data-stu-id="5f54d-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="5f54d-118">Resursele sunt adăugate cu o cerință de resurse care se bazează pe datele de început/sfârșit și pe metoda de alocare specificată în panoul **Creare rapidă: membru al echipei de proiect**.</span><span class="sxs-lookup"><span data-stu-id="5f54d-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="5f54d-119">Puteți vedea o diferență dacă adăugați direct membrul echipei generice și apoi atribuiți resursei generice mai multe activități decât numărul de ore de care aceasta dispune pentru a le acoperi.</span><span class="sxs-lookup"><span data-stu-id="5f54d-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="5f54d-120">Faceți clic pe **Generare cerință** pentru a regenera cerința, în scopul de a echilibra orele necesare și atribuirile.</span><span class="sxs-lookup"><span data-stu-id="5f54d-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="5f54d-121">De asemenea, puteți face clic pe linkul **Cerință resursă** din grila de echipă pentru a deschide cerința și a adăuga competențe, resurse preferate etc.</span><span class="sxs-lookup"><span data-stu-id="5f54d-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Cerință resursă](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]