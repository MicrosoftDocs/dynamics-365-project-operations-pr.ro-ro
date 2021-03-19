---
title: Îndeplinirea cerințelor de resurse generice
description: Acest subiect furnizează informații despre cum să rezervați resurse denumite pentru o cerință de resurse generice.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279603"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="4309d-103">Îndeplinirea cerințelor de resurse generice</span><span class="sxs-lookup"><span data-stu-id="4309d-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="4309d-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="4309d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4309d-105">Aveți posibilitatea să rezervați o resursă denumită pentru a înlocui resursa generică care are o cerință de resurse.</span><span class="sxs-lookup"><span data-stu-id="4309d-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="4309d-106">Pe pagina **Proiecte**, selectați fila **Echipă**.</span><span class="sxs-lookup"><span data-stu-id="4309d-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="4309d-107">Selectați resursa generică care are o cerință de resurse din listă și apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="4309d-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="4309d-108">Sau, deschideți cerința de resurse și apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="4309d-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="4309d-109">În pagina **Asistent de planificare**, selectați o resursă denumită pentru a rezerva în echipa de proiect și apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="4309d-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="4309d-110">Când rezervarea este finalizată și îndeplinită de o resursă denumită, resursa generică este înlocuită cu resursa denumită.</span><span class="sxs-lookup"><span data-stu-id="4309d-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="4309d-111">Atribuirile din planificare sunt actualizate și cu resursa denumită.</span><span class="sxs-lookup"><span data-stu-id="4309d-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="4309d-112">Îndeplinirea unei resurse generice cu mai multe resurse denumite</span><span class="sxs-lookup"><span data-stu-id="4309d-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="4309d-113">Îndeplinirea unei cerințe pentru o resursă generică cu mai multe resurse denumite este similară cu atribuirea unei singure resurse denumite.</span><span class="sxs-lookup"><span data-stu-id="4309d-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="4309d-114">De exemplu, există o activitate cu o durată de cinci zile și 120 de ore de efort.</span><span class="sxs-lookup"><span data-stu-id="4309d-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="4309d-115">Această activitate nu poate fi finalizată de către o singură resursă care lucrează o zi tipică de opt ore, cinci zile pe săptămână.</span><span class="sxs-lookup"><span data-stu-id="4309d-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="4309d-116">Cerința este de 120 de ore de inginerie robotică timp de cinci zile, ceea ce înseamnă 24 de ore pe zi.</span><span class="sxs-lookup"><span data-stu-id="4309d-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="4309d-117">Acesta este un exemplu de moment în care sunt necesare mai multe resurse denumite pentru a îndeplini o solicitare de resurse generice.</span><span class="sxs-lookup"><span data-stu-id="4309d-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="4309d-118">Va trebui să rezervați mai multe resurse pentru a îndeplini cerința.</span><span class="sxs-lookup"><span data-stu-id="4309d-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="4309d-119">Diferența principală în acest scenariu este că resursa generică rămâne pe echipa atribuită activității și membrii echipei de resurse denumiți rezervați nu sunt atribuiți ca parte a poziției.</span><span class="sxs-lookup"><span data-stu-id="4309d-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="4309d-120">Managerul de proiect poate atribui lucrul după cum este adecvat către resursele denumite.</span><span class="sxs-lookup"><span data-stu-id="4309d-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="4309d-121">Vizualizarea **Reconciliere** poate ajuta un manager de proiect la defalcarea rezervărilor în mai multe resurse pentru atribuiri de activități.</span><span class="sxs-lookup"><span data-stu-id="4309d-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="4309d-122">Acest lucru nu se face în mod automat, deoarece în orice scenariu mai complicat decât exemplul simplu de mai sus, cum ar fi în cazul în care aveți un pachet de activități care alcătuiesc cerința sau intenția modului în care managerul de proiect vrea să atribuie trebuie să fie asumată de sistem.</span><span class="sxs-lookup"><span data-stu-id="4309d-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="4309d-123">Deoarece sistemul nu poate înțelege intenția, este posibil ca ipotezele să fie diferite de cele preconizate și se va produce un rezultat incorect sau imprevizibil.</span><span class="sxs-lookup"><span data-stu-id="4309d-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="4309d-124">Rezultatul previzibil este că resursa generică rămâne atribuită până când managerul de proiect creează în mod deliberat atribuiri, utilizând vizualizarea **Reconciliere**.</span><span class="sxs-lookup"><span data-stu-id="4309d-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]