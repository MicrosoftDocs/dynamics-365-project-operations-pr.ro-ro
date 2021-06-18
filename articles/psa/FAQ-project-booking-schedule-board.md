---
title: Crearea unei rezervări de proiect din Panoul de planificare
description: Acest subiect oferă informații despre modul de a crea o rezervare de proiect de la tabloul de planificare.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: d33786a5d0a2485a06d174eb7afcbaaa2f337cf6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992981"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="f1e18-103">Crearea unei rezervări de proiect din Panoul de planificare</span><span class="sxs-lookup"><span data-stu-id="f1e18-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f1e18-104">Puteți rezerva o resursă pe un proiect direct din fila **Echipă** a proiectului sau generând o cerință de resurse de la atribuirea generică a unui membru al echipei și apoi îndeplinind cerințele generate cu un membru al echipei proiectului.</span><span class="sxs-lookup"><span data-stu-id="f1e18-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="f1e18-105">Puteți rezerva, de asemenea, o resursă pe un proiect direct de la tabloul de planificare.</span><span class="sxs-lookup"><span data-stu-id="f1e18-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="f1e18-106">Există trei modalități de a face acest lucru:</span><span class="sxs-lookup"><span data-stu-id="f1e18-106">There are three ways to do this:</span></span>

- <span data-ttu-id="f1e18-107">**Rezervarea de la o cerință de resursă generată:** aveți posibilitatea să generați o cerință de resursă după ce creați o resursă generică și atribuiți activități în cadrul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="f1e18-108">**Rezervați de la cerința principală:** cerințele primare apar pe panoul de planificare pe fila **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="f1e18-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="f1e18-109">**Rezervați de la o cerință de resursă nouă:** aveți posibilitatea să creați o cerință de resursă de la zero și să o asociați cu un proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="f1e18-110">Pe tabloul de planificare, cerința de resursă apare pe fila **Deschidere cerințe**.</span><span class="sxs-lookup"><span data-stu-id="f1e18-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="f1e18-111">Rezervarea de la o cerință de resursă generată</span><span class="sxs-lookup"><span data-stu-id="f1e18-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="f1e18-112">Aveți posibilitatea să generați o cerință de resursă generică și să îi atribuiți o activitate sau mai multe activități în cadrul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="f1e18-113">Apoi puteți să generați o cerință de resursă de la membrul de echipă generic.</span><span class="sxs-lookup"><span data-stu-id="f1e18-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="f1e18-114">Pe tabloul de planificare, această resursă va apărea pe fila **Deschidere cerințe**. Este posibil să trebuiască să utilizați filtre de coloană pe grilă dacă aveți multe cerințele deschise.</span><span class="sxs-lookup"><span data-stu-id="f1e18-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="f1e18-115">![Deschideți fila Cerințe pe panoul Planificare](media/FAQ-Project-Booking-Schedule-Board-1.png "Captură de ecran tablou rezervări și atribuiri")</span><span class="sxs-lookup"><span data-stu-id="f1e18-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="f1e18-116">Selectați cerința.</span><span class="sxs-lookup"><span data-stu-id="f1e18-116">Select the requirement.</span></span> <span data-ttu-id="f1e18-117">Fila **Găsiți disponibilitatea** va apărea în partea de sus a rândului selectat.</span><span class="sxs-lookup"><span data-stu-id="f1e18-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="f1e18-118">Când selectați fila, modul Asistent de planificare al panoului de planificare se deschide și apoi filtrează resursele disponibile care întrunesc cerințele de resurse.</span><span class="sxs-lookup"><span data-stu-id="f1e18-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="f1e18-119">După aceea, puteți rezerva o resursă.</span><span class="sxs-lookup"><span data-stu-id="f1e18-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="f1e18-120">Puteți, de asemenea, să glisați și să fixați rândul selectat din partea de jos a tabloului de planificare la o celulă de resursă în grila de mai sus.</span><span class="sxs-lookup"><span data-stu-id="f1e18-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="f1e18-121">Atunci când fixați, acesta deschide panoul **Creare rezervare resursă** din partea dreaptă.</span><span class="sxs-lookup"><span data-stu-id="f1e18-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="f1e18-122">Selectând **Rezervare** se rezervă resursa pe echipa de proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panoul Creare rezervare resursă](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="f1e18-124">Rezervare de la Cerința principală</span><span class="sxs-lookup"><span data-stu-id="f1e18-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="f1e18-125">Crearea unui proiect în Project Service creează automat o cerință de resurse numită Cerință principală.</span><span class="sxs-lookup"><span data-stu-id="f1e18-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="f1e18-126">Aceasta este o cerință necompletată, care este folosită pentru a rezerva rapid o resursă cu tabloul de planificare fără a genera o cerință sau a crea una de la zero.</span><span class="sxs-lookup"><span data-stu-id="f1e18-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="f1e18-127">Întrucât cerința este necompletată, va trebui să specificați datele, precum și metoda de alocare și orele, dacă este cazul.</span><span class="sxs-lookup"><span data-stu-id="f1e18-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="f1e18-128">Pentru a rezerva o cerință cu Cerința principală, pe tabloul de planificare, selectați fila **Proiect**. Este posibil să fie nevoie să utilizați filtrul de coloană pe coloana **Proiect** dacă aveți multe proiecte.</span><span class="sxs-lookup"><span data-stu-id="f1e18-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="f1e18-129">![Filtre de coloană pe panoul de planificare](media/FAQ-Project-Booking-Schedule-Board-2.png "Captură de ecran tablou rezervări și atribuiri")</span><span class="sxs-lookup"><span data-stu-id="f1e18-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="f1e18-130">Selectați cerința care are doar numele proiectului ca denumire și are o durată de zero (0).</span><span class="sxs-lookup"><span data-stu-id="f1e18-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="f1e18-131">Selectați fila **Găsiți disponibilitatea** care apare pe rând.</span><span class="sxs-lookup"><span data-stu-id="f1e18-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="f1e18-132">Aceasta pune panoul Planificare în modul Asistent de planificare și arată resursele disponibile care pot fi rezervate în proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="f1e18-133">Întrucât o **Cerință principală** este o cerință necompletată cu durata zero (0), va trebui să setați durata pe panoul **Creare rezervare resursă** atunci când selectați și rezervați o resursă.</span><span class="sxs-lookup"><span data-stu-id="f1e18-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="f1e18-134">Puteți să selectați, de asemenea, **Cerința principală a proiectului** în partea de jos a tabloului de planificare și să o glisați și fixați pe o resursă pentru a o rezerva.</span><span class="sxs-lookup"><span data-stu-id="f1e18-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="f1e18-135">Întrucât **Cerința principală** este o cerință necompletată cu durata zero (0), va trebui să setați durata pe panoul **Creare rezervare resursă** atunci când selectați și rezervați o resursă.</span><span class="sxs-lookup"><span data-stu-id="f1e18-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="f1e18-136">Atunci când rezervați o resursă prin **Cerința principală** pe tabloul de planificare, o adăugați la echipa de proiect fără atribuiri.</span><span class="sxs-lookup"><span data-stu-id="f1e18-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="f1e18-137">Rezervați de la o cerință de resursă nouă</span><span class="sxs-lookup"><span data-stu-id="f1e18-137">Book from a new resource requirement</span></span>
<span data-ttu-id="f1e18-138">Parcurgeți pașii următori pentru a rezerva dintr-o nouă cerință de resurse.</span><span class="sxs-lookup"><span data-stu-id="f1e18-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="f1e18-139">Accesați **Cerințe resurse**, apoi selectați **Nou** pentru a crea noua cerință de resursă.</span><span class="sxs-lookup"><span data-stu-id="f1e18-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="f1e18-140">În fila **Proiect**, selectați un proiect pentru a asocia cerința la proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="f1e18-141">Pe tabloul de planificare, această cerință nouă se afișează ca **Deschidere cerință** pe care o puteți procesa.</span><span class="sxs-lookup"><span data-stu-id="f1e18-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="f1e18-142">Rezervați resursa pentru a o adăuga la echipa de proiect.</span><span class="sxs-lookup"><span data-stu-id="f1e18-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="f1e18-143">Acum, că resursa este rezervată, trebuie să atribuiți activități manual.</span><span class="sxs-lookup"><span data-stu-id="f1e18-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]