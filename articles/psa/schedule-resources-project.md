---
title: Planificați resurse pentru un proiect
description: Cum se planifică resurse pentru un proiect în Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282663"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="21d4c-103">Planificați resurse pentru un proiect (Project Service)</span><span class="sxs-lookup"><span data-stu-id="21d4c-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="21d4c-104">Puteți verifica disponibilitatea resurselor pentru a obține o imagine de ansamblu a rezervării resurselor dvs., sau puteți filtra vizualizarea după competențe, echipă, locație și alte opțiuni.</span><span class="sxs-lookup"><span data-stu-id="21d4c-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="21d4c-105">Tabloul de planificare arată lista de resurse și disponibilitatea acestora.</span><span class="sxs-lookup"><span data-stu-id="21d4c-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="21d4c-106">Selectați un mod de vizualizare pentru a arăta disponibilitatea după **Ore**, **Zile**, **Săptămâni** sau **Luni**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="21d4c-107">Înainte de a utiliza panoul de planificare, este important să-l configurați.</span><span class="sxs-lookup"><span data-stu-id="21d4c-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="21d4c-108">Pentru informații suplimentare, consultați [Configurați tabloul de planificare (Field Service sau Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="21d4c-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="21d4c-109">Dacă utilizați o versiune mai veche, pentru a vedea disponibilitatea resurselor, consultați [Vedeți disponibilitatea resurselor](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="21d4c-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="21d4c-110">Pentru a utiliza funcția de rezervare a panoului de planificare, codificarea geografică și serviciile de localizare, trebuie să activați hărțile.</span><span class="sxs-lookup"><span data-stu-id="21d4c-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="21d4c-111">În meniul principal, selectați **Planificarea resurselor** > **Administrare**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="21d4c-112">Faceți clic pe **Parametri de planificare**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="21d4c-113">Deschideți înregistrarea și navigați i în jos la secțiunea **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="21d4c-114">În câmpul **Conectare la Hărți**, alegeți **Da**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="21d4c-115">Acceptați condițiile și salvați înregistrarea.</span><span class="sxs-lookup"><span data-stu-id="21d4c-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="21d4c-116">În meniul principal, selectați **Project Service** > **Panou de planificare**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="21d4c-117">De aici, există mai multe moduri de a planifica manual o cerință de rezervare.</span><span class="sxs-lookup"><span data-stu-id="21d4c-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="21d4c-118">Alegeți metoda care funcționează pentru dvs.</span><span class="sxs-lookup"><span data-stu-id="21d4c-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="21d4c-119">Găsiți resurse disponibile</span><span class="sxs-lookup"><span data-stu-id="21d4c-119">Find available resources</span></span>

1.  <span data-ttu-id="21d4c-120">Din lista **Cerință de rezervare**, faceți clic dreapta pe o rezervare neprogramată și alegeți una dintre următoarele:</span><span class="sxs-lookup"><span data-stu-id="21d4c-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="21d4c-121">Alegeți **Găsiți disponibilitatea - Resurse curente** pentru a găsi o resursă disponibilă din lista de pe panoul de planificare.</span><span class="sxs-lookup"><span data-stu-id="21d4c-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="21d4c-122">Alegeți **Găsiți disponibilitatea - Toate resursele** pentru a găsi o resursă disponibilă din cele din sistem</span><span class="sxs-lookup"><span data-stu-id="21d4c-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="21d4c-123">Când faceți acest lucru, filtrele vor arăta opțiuni pentru cerința de rezervare selectată.</span><span class="sxs-lookup"><span data-stu-id="21d4c-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="21d4c-124">Atunci când vedeți un slot disponibil, faceți clic dreapta pe intervalul de timp de pe tabloul de planificare și alegeți **Rezervați aici**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="21d4c-125">Sau glisați și fixați cerința de rezervare în slotul de timp disponibil.</span><span class="sxs-lookup"><span data-stu-id="21d4c-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="21d4c-126">Rezervați o resursă utilizând vizualizarea zilnică și vedeți cine nu este rezervat</span><span class="sxs-lookup"><span data-stu-id="21d4c-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="21d4c-127">Pe panoul de planificare, selectați **Modul de vizualizare** și selectați **Zile**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="21d4c-128">Acest lucru arată o vizualizare grilă a numărului de ore rezervate pentru o resursă pe zi și prezintă zilele libere.</span><span class="sxs-lookup"><span data-stu-id="21d4c-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="21d4c-129">Faceți clic pe numele resursei pe care doriți s-o rezervați, apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="21d4c-130">În caseta de dialog **Rezervare de resurse (creare)**, alege proiectul pentru care doriți să rezervați resursa, metoda de rezervare și timpii de începere sau de încheiere.</span><span class="sxs-lookup"><span data-stu-id="21d4c-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="21d4c-131">Când ați terminat, selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="21d4c-132">Vizualizați tabloul de planificare</span><span class="sxs-lookup"><span data-stu-id="21d4c-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="21d4c-133">Selectați o cerință de rezervare neplanificată din lista din partea de jos.</span><span class="sxs-lookup"><span data-stu-id="21d4c-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="21d4c-134">Glisați cerința de rezervare într-un slot de resurse/timp din panoul de planificare.</span><span class="sxs-lookup"><span data-stu-id="21d4c-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="21d4c-135">Când ați terminat, selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="21d4c-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="21d4c-136">Resurse suplimentare</span><span class="sxs-lookup"><span data-stu-id="21d4c-136">Additional resources</span></span>  
 [<span data-ttu-id="21d4c-137">Ghidul managerului de resurse</span><span class="sxs-lookup"><span data-stu-id="21d4c-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]