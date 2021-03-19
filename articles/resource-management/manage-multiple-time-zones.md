---
title: Gestionarea fusurilor orare
description: Când este creat un proiect, fusul orar al acestuia se bazează pe fusul orar definit în șablonul de oră de lucru aplicat.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e0cf24a9916f7ceedee0e9d6fa9399a88c3e4b91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279558"
---
# <a name="manage-time-zones"></a><span data-ttu-id="9f454-103">Gestionarea fusurilor orare</span><span class="sxs-lookup"><span data-stu-id="9f454-103">Manage time zones</span></span>

<span data-ttu-id="9f454-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="9f454-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="9f454-105">Proiecte</span><span class="sxs-lookup"><span data-stu-id="9f454-105">Projects</span></span>

<span data-ttu-id="9f454-106">Când este creat un proiect, fusul orar al acestuia se bazează pe fusul orar definit în șablonul de oră de lucru aplicat.</span><span class="sxs-lookup"><span data-stu-id="9f454-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="9f454-107">Pe **Proiectul** datele sunt întotdeauna relative la fusul orar al utilizatorului care este conectat la fiecare filă, cu excepția filei **Activitate**. Când vizualizați structura detaliată a proiectului, datele vor fi întotdeauna afișate în fusul orar al proiectului.</span><span class="sxs-lookup"><span data-stu-id="9f454-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="9f454-108">Activități</span><span class="sxs-lookup"><span data-stu-id="9f454-108">Tasks</span></span>

<span data-ttu-id="9f454-109">Când se creează o activitate, ora de începere, ora de încheiere și orele/ziua sunt controlate de programul de lucru al proiectului.</span><span class="sxs-lookup"><span data-stu-id="9f454-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="9f454-110">De exemplu, dacă o sarcină este creată cu un proiect al cărui fus orar este -8 PST și are următoarele ore de lucru: de la 9:00 la 17:00 de luni până vineri, orice sarcină creată fără o sarcină va respecta ora de început și ora de încheiere a calendarului proiectului.</span><span class="sxs-lookup"><span data-stu-id="9f454-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="9f454-111">Gestionați resursele cu fusuri orare</span><span class="sxs-lookup"><span data-stu-id="9f454-111">Manage resources with time zones</span></span>

<span data-ttu-id="9f454-112">Pentru rezultate precise și predictibile atunci când se utilizează **Extindeți rezervarea**, există două condiții prealabile cheie care trebuie îndeplinite:</span><span class="sxs-lookup"><span data-stu-id="9f454-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="9f454-113">Utilizatorul trebuie să configureze fusul orar al dispozitivului său pentru a se potrivi cu fusul orar definit în **Setările de personalizare** ale sistemului.</span><span class="sxs-lookup"><span data-stu-id="9f454-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Setările fusului orar în Windows 10](media/reconcile-assignments-03.png)

  ![Setările fusului orar în setările de personalizare](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="9f454-116">Resursa care poate fi rezervată trebuie să aibă cel puțin un minut de timp de lucru care se suprapune contururilor utilizate pentru a defini extensia solicitată.</span><span class="sxs-lookup"><span data-stu-id="9f454-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="9f454-117">De exemplu, următoarele resurse cu program de lucru care se încadrează între orele 9:00 și 19:00.</span><span class="sxs-lookup"><span data-stu-id="9f454-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparația contururilor resurselor](media/reconcile-assignments-05.png)

<span data-ttu-id="9f454-119">Tabelul următor afișează:</span><span class="sxs-lookup"><span data-stu-id="9f454-119">The following table shows:</span></span>

- <span data-ttu-id="9f454-120">Un șablon de calendar de proiect</span><span class="sxs-lookup"><span data-stu-id="9f454-120">A project calendar template</span></span>
- <span data-ttu-id="9f454-121">Resursa A: Această resursă are același calendar și se află în același fus orar cu proiectul.</span><span class="sxs-lookup"><span data-stu-id="9f454-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="9f454-122">Ora de început a rezervărilor va fi ora 9:00.</span><span class="sxs-lookup"><span data-stu-id="9f454-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="9f454-123">Resursa B: această resursă se află într-un alt fus orar decât proiectul și începe la ora 7:00 în fusul orar al acestora.</span><span class="sxs-lookup"><span data-stu-id="9f454-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="9f454-124">Cu toate acestea, rezervările vor începe la ora 9:00, deoarece aceasta este cea mai timpurie perioadă de începere a conturului misiunii.</span><span class="sxs-lookup"><span data-stu-id="9f454-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="9f454-125">Resursele C și D: resursele sunt situate în diferite fusuri orare, ambele diferite între ele și de proiect, iar rezervările lor încep nu mai devreme decât orele lor de început disponibile.</span><span class="sxs-lookup"><span data-stu-id="9f454-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="9f454-126">Entitate</span><span class="sxs-lookup"><span data-stu-id="9f454-126">Entity</span></span>  |<span data-ttu-id="9f454-127">Calendar</span><span class="sxs-lookup"><span data-stu-id="9f454-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="9f454-128">Șablon de calendar de proiect</span><span class="sxs-lookup"><span data-stu-id="9f454-128">Project calendar template</span></span>   | ![calendarul proiectului](media/reconcile-assignments-06.png) |
|<span data-ttu-id="9f454-130">Resursă A</span><span class="sxs-lookup"><span data-stu-id="9f454-130">Resource A</span></span>  | ![Calendar resursa A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="9f454-132">Resursă B</span><span class="sxs-lookup"><span data-stu-id="9f454-132">Resource B</span></span>  |  ![Calendar resursa B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="9f454-134">Resursă C</span><span class="sxs-lookup"><span data-stu-id="9f454-134">Resource C</span></span>  |  ![Calendar resursa C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="9f454-136">Resursă D</span><span class="sxs-lookup"><span data-stu-id="9f454-136">Resource D</span></span>  | ![Calendar resursa D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="9f454-138">Când navigați la vizualizarea **Reconciliere**, sunt afișate alocările de resurse și lipsa de rezervare asociată.</span><span class="sxs-lookup"><span data-stu-id="9f454-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vedere de reconciliere înainte de extensie](media/reconcile-assignments-10.png)

<span data-ttu-id="9f454-140">După ce funcționalitatea de rezervare extinsă a fost utilizată pentru fiecare resursă, rezervările sunt extinse cu succes pentru fiecare resursă, deoarece orele de lucru ale fiecărei resurse s-au suprapus cu contururile deficitului.</span><span class="sxs-lookup"><span data-stu-id="9f454-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vizualizare de reconciliere după extinderea rezervării](media/reconcile-assignments-11.png) 

<span data-ttu-id="9f454-142">Observați că o privire mai atentă asupra detaliilor rezervărilor arată diferențe în momentul începerii rezervărilor.</span><span class="sxs-lookup"><span data-stu-id="9f454-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="9f454-143">Rezervările încep nu mai devreme de ora de începere a conturului de atribuire și nici mai devreme de ora de începere disponibilă a resursei.</span><span class="sxs-lookup"><span data-stu-id="9f454-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Rezervări noi ale resurselor din tabloul de bord](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]