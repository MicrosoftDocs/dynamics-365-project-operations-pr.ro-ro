---
title: Rezervați resurse denumite din cerințele de resurse
description: Acest subiect furnizează informații despre rezervarea de resurse denumite pentru o cerință de resurse generice.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 83ac2056-313e-4f90-8297-238fd4d25ef9
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eab280cd1a670cc2a6ed0ae02cde7ba9bf7d601d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754707"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="72d60-103">Rezervați resurse denumite din cerințele de resurse</span><span class="sxs-lookup"><span data-stu-id="72d60-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="72d60-104">Aveți posibilitatea să rezervați o resursă denumită pentru a înlocui resursa generică care are o cerință de resurse.</span><span class="sxs-lookup"><span data-stu-id="72d60-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="72d60-105">În Project Service Automation (PSA), pe pagina **Proiecte**, faceți clic pe fila **Echipă**.</span><span class="sxs-lookup"><span data-stu-id="72d60-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="72d60-106">Selectați resursa generică care are o cerință de resurse din listă și apoi faceți clic pe **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="72d60-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="72d60-107">Sau, deschideți cerința de resurse și apoi faceți clic pe **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="72d60-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezervarea unui membru generic al echipei](media/RM-how-to-14.png)


3. <span data-ttu-id="72d60-109">În pagina **Asistent de planificare**, selectați o resursă denumită pentru a rezerva în echipa de proiect și apoi faceți clic pe **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="72d60-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezervarea unui membru generic al echipei folosind Asistentul de planificare](media/RM-how-to-15.png)

<span data-ttu-id="72d60-111">Când rezervarea este finalizată și îndeplinită de o resursă denumită, resursa generică este înlocuită cu resursa denumită.</span><span class="sxs-lookup"><span data-stu-id="72d60-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Membru al echipei denumit înlocuind un membru generic al echipei](media/RM-how-to-16.png)

<span data-ttu-id="72d60-113">Atribuirile din planificare sunt actualizate și cu resursa denumită.</span><span class="sxs-lookup"><span data-stu-id="72d60-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membru al echipei denumit atribuit la activități de proiect](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="72d60-115">Îndeplinirea unei resurse generice cu mai multe resurse denumite</span><span class="sxs-lookup"><span data-stu-id="72d60-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="72d60-116">Îndeplinirea unei cerințe pentru o resursă generică cu mai multe resurse denumite este similară cu atribuirea unei singure resurse denumite.</span><span class="sxs-lookup"><span data-stu-id="72d60-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="72d60-117">De exemplu, există o activitate cu o durată de cinci zile și 120 de ore de efort.</span><span class="sxs-lookup"><span data-stu-id="72d60-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="72d60-118">Această activitate nu poate fi finalizată de către o singură resursă care lucrează o zi tipică de opt ore, cinci zile pe săptămână.</span><span class="sxs-lookup"><span data-stu-id="72d60-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![O activitate care are nevoie de 120 de ore de efort de peste cinci zile](media/RM-how-to-21.png)

<span data-ttu-id="72d60-120">Cerința este de 120 de ore de inginerie robotică timp de cinci zile, ceea ce înseamnă 24 de ore pe zi.</span><span class="sxs-lookup"><span data-stu-id="72d60-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Cerință pe zi](media/RM-how-to-22.png)

<span data-ttu-id="72d60-122">Acesta este un exemplu de moment în care sunt necesare mai multe resurse denumite pentru a îndeplini o solicitare de resurse generice.</span><span class="sxs-lookup"><span data-stu-id="72d60-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="72d60-123">Va trebui să rezervați mai multe resurse pentru a îndeplini cerința.</span><span class="sxs-lookup"><span data-stu-id="72d60-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezervarea mai multor resurse pentru a îndeplini cerința](media/RM-how-to-23.png)

<span data-ttu-id="72d60-125">Diferența principală în acest scenariu este că resursa generică rămâne pe echipa atribuită activității și membrii echipei de resurse denumiți rezervați nu sunt atribuiți ca parte a poziției.</span><span class="sxs-lookup"><span data-stu-id="72d60-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="72d60-126">Managerul de proiect poate atribui lucrul după cum este adecvat către resursele denumite.</span><span class="sxs-lookup"><span data-stu-id="72d60-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="72d60-127">Vizualizarea **Reconciliere** poate ajuta un manager de proiect la defalcarea rezervărilor în mai multe resurse pentru atribuiri de activități.</span><span class="sxs-lookup"><span data-stu-id="72d60-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="72d60-128">Acest lucru nu se face în mod automat, deoarece în orice scenariu mai complicat decât exemplul simplu de mai sus, cum ar fi în cazul în care aveți un pachet de activități care alcătuiesc cerința, intenția modului în care managerul de proiect vrea să atribuie trebuie să fie asumată de sistem.</span><span class="sxs-lookup"><span data-stu-id="72d60-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="72d60-129">Deoarece sistemul nu poate înțelege intenția, sunt șanse ca ipotezele să fie diferite de cele preconizate și să se producă un rezultat incorect sau imprevizibil.</span><span class="sxs-lookup"><span data-stu-id="72d60-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="72d60-130">Rezultatul previzibil este că resursa generică rămâne atribuită până când managerul de proiect creează în mod deliberat atribuiri, utilizând vizualizarea **Reconciliere**.</span><span class="sxs-lookup"><span data-stu-id="72d60-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>

