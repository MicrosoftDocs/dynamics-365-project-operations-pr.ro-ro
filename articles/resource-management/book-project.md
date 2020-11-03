---
title: Rezervarea pentru un proiect
description: Acest subiect furnizează informații despre rezervarea unei resurse la un proiect.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082648"
---
# <a name="book-to-a-project"></a><span data-ttu-id="a9303-103">Rezervarea pentru un proiect</span><span class="sxs-lookup"><span data-stu-id="a9303-103">Book to a project</span></span>

<span data-ttu-id="a9303-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="a9303-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a9303-105">Există momente în care un manager de proiect sau un manager de resurse va trebui să aloce o resursă proiectului fără a fi definită o cerință specifică de la un membru al echipei generice.</span><span class="sxs-lookup"><span data-stu-id="a9303-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="a9303-106">Acest lucru poate fi realizat într-unul din cele trei moduri.</span><span class="sxs-lookup"><span data-stu-id="a9303-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="a9303-107">Rezervați din grila de membru de echipă</span><span class="sxs-lookup"><span data-stu-id="a9303-107">Book from the team member grid</span></span>
- <span data-ttu-id="a9303-108">Rezervarea din tabloul de planificare</span><span class="sxs-lookup"><span data-stu-id="a9303-108">Book from the schedule board</span></span>
- <span data-ttu-id="a9303-109">Rezervați din formularul **Proiect**</span><span class="sxs-lookup"><span data-stu-id="a9303-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="a9303-110">Rezervați din grila de membru de echipă</span><span class="sxs-lookup"><span data-stu-id="a9303-110">Book from the team member grid</span></span>

<span data-ttu-id="a9303-111">Dacă organizația dvs. funcționează în modul hibrid de alocare a resurselor, managerul de proiect poate rezerva o resursă direct la proiect, parcurgând pașii următori.</span><span class="sxs-lookup"><span data-stu-id="a9303-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="a9303-112">Din proiect, accesați grila membrilor echipei și selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="a9303-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="a9303-113">Definiți numele poziției și rolul resursei.</span><span class="sxs-lookup"><span data-stu-id="a9303-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="a9303-114">Selectați resursa care se poate rezerva din căutarea disponibilă.</span><span class="sxs-lookup"><span data-stu-id="a9303-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="a9303-115">După ce selectați resursa, definiți următoarele informații de câmp pentru a rezerva resursa:</span><span class="sxs-lookup"><span data-stu-id="a9303-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="a9303-116">Dată de început</span><span class="sxs-lookup"><span data-stu-id="a9303-116">Start date</span></span>
    - <span data-ttu-id="a9303-117">Data de terminare</span><span class="sxs-lookup"><span data-stu-id="a9303-117">Finish date</span></span>
    - <span data-ttu-id="a9303-118">Metodă de alocare</span><span class="sxs-lookup"><span data-stu-id="a9303-118">Allocation method</span></span>
    - <span data-ttu-id="a9303-119">Ore, dacă este cazul</span><span class="sxs-lookup"><span data-stu-id="a9303-119">Hours, if applicable</span></span>
    - <span data-ttu-id="a9303-120">Aprobator de proiect</span><span class="sxs-lookup"><span data-stu-id="a9303-120">Project approver</span></span>

6. <span data-ttu-id="a9303-121">Selectați **Salvare și închidere**</span><span class="sxs-lookup"><span data-stu-id="a9303-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="a9303-122">Rezervarea din tabloul de planificare</span><span class="sxs-lookup"><span data-stu-id="a9303-122">Book from the schedule board</span></span>

<span data-ttu-id="a9303-123">Atunci când un manager de resurse trebuie să rezerve o resursă direct la un proiect, acesta poate folosi tabloul de planificare și cerința proiectului.</span><span class="sxs-lookup"><span data-stu-id="a9303-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="a9303-124">Cerința proiectului este o cerință de resurse care este întotdeauna disponibilă pentru a fi rezervată.</span><span class="sxs-lookup"><span data-stu-id="a9303-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="a9303-125">Parcurgeți pașii următori pentru a rezerva direct la un formular de proiect din panoul de planificare.</span><span class="sxs-lookup"><span data-stu-id="a9303-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="a9303-126">Navigați la tabloul de planificare și în pagina din stânga, filtrați pentru resursele pe care le luați în considerare pentru cerință.</span><span class="sxs-lookup"><span data-stu-id="a9303-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="a9303-127">În panoul de jos, selectați fila **Proiect** pentru a vizualiza o listă cu cerințele proiectului.</span><span class="sxs-lookup"><span data-stu-id="a9303-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="a9303-128">Trageți cerința pe o resursă și definiți următoarele informații:</span><span class="sxs-lookup"><span data-stu-id="a9303-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="a9303-129">Dată de început</span><span class="sxs-lookup"><span data-stu-id="a9303-129">Start date</span></span>
    - <span data-ttu-id="a9303-130">Data de terminare</span><span class="sxs-lookup"><span data-stu-id="a9303-130">Finish date</span></span>
    - <span data-ttu-id="a9303-131">Starea rezervării</span><span class="sxs-lookup"><span data-stu-id="a9303-131">Booking status</span></span>
    - <span data-ttu-id="a9303-132">Metodă de rezervare</span><span class="sxs-lookup"><span data-stu-id="a9303-132">Booking method</span></span>
    - <span data-ttu-id="a9303-133">Durată</span><span class="sxs-lookup"><span data-stu-id="a9303-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="a9303-134">Rezervați din formularul Proiect</span><span class="sxs-lookup"><span data-stu-id="a9303-134">Book from the Project form</span></span>

<span data-ttu-id="a9303-135">În calitate de manager de proiect, este posibil să trebuiască să rezervați o resursă la un proiect, dar să cunoașteți doar criteriile, mai degrabă decât numele resursei.</span><span class="sxs-lookup"><span data-stu-id="a9303-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="a9303-136">Parcurgeți pașii următori pentru a utiliza asistentul de planificare pentru a găsi o resursă bazată pe orice atribute disponibile ale resursei.</span><span class="sxs-lookup"><span data-stu-id="a9303-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="a9303-137">Navigați la proiect și selectați **Rezervare** pentru a deschide Asistentul de planificare.</span><span class="sxs-lookup"><span data-stu-id="a9303-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="a9303-138">Folosind filtrele din partea stângă a Asistentului de planificare, restrângeți criteriile și selectați **Căutare.**</span><span class="sxs-lookup"><span data-stu-id="a9303-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="a9303-139">Pe baza resurselor returnate în rezultate, puteți rezerva o resursă.</span><span class="sxs-lookup"><span data-stu-id="a9303-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="a9303-140">Această metodă nu creează nicio rezervare pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="a9303-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="a9303-141">În schimb, adaugă resursa la echipă.</span><span class="sxs-lookup"><span data-stu-id="a9303-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="a9303-142">După ce membrul echipei a fost adăugat la proiect, managerul de proiect poate utiliza menținerea rezervărilor sau extinde rezervările pentru a adăuga rezervările necesare la resursă.</span><span class="sxs-lookup"><span data-stu-id="a9303-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
