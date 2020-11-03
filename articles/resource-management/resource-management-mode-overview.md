---
title: Prezentare generală a modurilor de gestionare a resurselor
description: Acest subiect oferă informații despre funcționalitatea gestionării resurselor în Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082684"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="e0bcf-103">Prezentare generală a modurilor de gestionare a resurselor</span><span class="sxs-lookup"><span data-stu-id="e0bcf-103">Resource management modes overview</span></span>

<span data-ttu-id="e0bcf-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="e0bcf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e0bcf-105">Dynamics 365 Project Operations acceptă două moduri pentru a putea executa fluxul general de rezervare.</span><span class="sxs-lookup"><span data-stu-id="e0bcf-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="e0bcf-106">Modul de gestionare este definit ca un parametru de proiect și poate fi modificat dacă afacerea dvs. are nevoie de schimbări.</span><span class="sxs-lookup"><span data-stu-id="e0bcf-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="e0bcf-107">Mod central</span><span class="sxs-lookup"><span data-stu-id="e0bcf-107">Central mode</span></span>
<span data-ttu-id="e0bcf-108">Pentru organizațiile care centralizează alocarea resurselor pentru proiecte, modul Central oferă o modalitate de a se asigura că managerii de proiect pot defini cerințele de resurse la nivelul proiectului.</span><span class="sxs-lookup"><span data-stu-id="e0bcf-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="e0bcf-109">Îndeplinirea cerințelor de resurse este delegată unui manager de resurse.</span><span class="sxs-lookup"><span data-stu-id="e0bcf-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="e0bcf-110">Managerii de proiect pot accepta sau respinge resursele propuse de managerul de resurse.</span><span class="sxs-lookup"><span data-stu-id="e0bcf-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Mod central](./media/resource-management-central.png)

<span data-ttu-id="e0bcf-112">Pentru a gestiona resursele cu modul Central, consultați:</span><span class="sxs-lookup"><span data-stu-id="e0bcf-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="e0bcf-113">Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse</span><span class="sxs-lookup"><span data-stu-id="e0bcf-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e0bcf-114">Rezervarea anumitor resurse din cerințele de resurse</span><span class="sxs-lookup"><span data-stu-id="e0bcf-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="e0bcf-115">Remiterea unei solicitări de resursă</span><span class="sxs-lookup"><span data-stu-id="e0bcf-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="e0bcf-116">Îndepliniți o solicitare de resurse</span><span class="sxs-lookup"><span data-stu-id="e0bcf-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="e0bcf-117">Acceptați sau respingeți o resursă de proiect propusă dintr-o solicitare de resursă</span><span class="sxs-lookup"><span data-stu-id="e0bcf-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="e0bcf-118">Mod hibrid</span><span class="sxs-lookup"><span data-stu-id="e0bcf-118">Hybrid mode</span></span>
<span data-ttu-id="e0bcf-119">Pentru organizațiile care necesită flexibilitate în alocarea resurselor, modul hibrid permite atât managerilor de proiect, cât și managerilor de resurse capacitatea de a rezerva resurse.</span><span class="sxs-lookup"><span data-stu-id="e0bcf-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Mod hibrid](./media/resource-management-hybrid.png)

<span data-ttu-id="e0bcf-121">În plus față de procesul de modul central acceptat, consultați următoarele subiecte pentru a gestiona toate celelalte fluxuri de rezervare acceptate în modul hibrid:</span><span class="sxs-lookup"><span data-stu-id="e0bcf-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="e0bcf-122">Rezervați o resursă direct unui proiect:</span><span class="sxs-lookup"><span data-stu-id="e0bcf-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="e0bcf-123">Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini</span><span class="sxs-lookup"><span data-stu-id="e0bcf-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="e0bcf-124">Rezervați o resursă dintr-o cerință de resurse:</span><span class="sxs-lookup"><span data-stu-id="e0bcf-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="e0bcf-125">Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse</span><span class="sxs-lookup"><span data-stu-id="e0bcf-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="e0bcf-126">Rezervarea anumitor resurse din cerințele de resurse</span><span class="sxs-lookup"><span data-stu-id="e0bcf-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
