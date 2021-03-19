---
title: Navigarea în interfața cu utilizatorul
description: Acest subiect oferă informații despre gestionarea proiectului în Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286758"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="96fbd-103">Navigarea în interfața cu utilizatorul</span><span class="sxs-lookup"><span data-stu-id="96fbd-103">Navigating the user interface</span></span>

<span data-ttu-id="96fbd-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="96fbd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="96fbd-105">Prezentare generală</span><span class="sxs-lookup"><span data-stu-id="96fbd-105">Overview</span></span>

<span data-ttu-id="96fbd-106">Formularul principal al proiectului este separat în mai multe file.</span><span class="sxs-lookup"><span data-stu-id="96fbd-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="96fbd-107">Fiecare filă reprezintă un nivel diferit de detaliu în cadrul proiectului.</span><span class="sxs-lookup"><span data-stu-id="96fbd-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="96fbd-108">**Rezumat**: furnizează o descriere a proiectului și cumulează atât performanța planificată, cât și cea reală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="96fbd-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Fila și câmpurile Rezumat](media/navigation7.png)

- <span data-ttu-id="96fbd-110">**Activități**: furnizează detalii cu privire la structura detaliată a proiectului reprezentată de o vizualizare grilă, vizualizare panou și un gantt.</span><span class="sxs-lookup"><span data-stu-id="96fbd-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Fila și câmpurile activitate](media/navigation8.png)

- <span data-ttu-id="96fbd-112">**Echipă**: Oferă detalii cu privire la participanții la proiect.</span><span class="sxs-lookup"><span data-stu-id="96fbd-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="96fbd-113">Efortul atribuit fiecărui membru al echipei este, de asemenea, rezumat în acest punct de vedere.</span><span class="sxs-lookup"><span data-stu-id="96fbd-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Fila și câmpurile echipă](media/navigation9.png)

- <span data-ttu-id="96fbd-115">**Alocări de resurse**: Oferă o imagine în timp a efortului pentru fiecare resursă a unui proiect.</span><span class="sxs-lookup"><span data-stu-id="96fbd-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Fila și câmpurile de alocare a resurselor](media/navigation10.png)

- <span data-ttu-id="96fbd-117">**Reconcilierea resurselor**: Oferă o vedere în etape temporale a diferențelor dintre atribuțiile fiecărei resurse denumite și rezervările acestora.</span><span class="sxs-lookup"><span data-stu-id="96fbd-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Fila și câmpurile de reconciliere resursă](media/navigation11.png)

- <span data-ttu-id="96fbd-119">**Estimări**: Oferă o vizualizare pe etape a costurilor și estimărilor de vânzări ale unui proiect.</span><span class="sxs-lookup"><span data-stu-id="96fbd-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Fila și câmpurile estimări](media/navigation12.png)

- <span data-ttu-id="96fbd-121">**Urmărirea**: Oferă o vizualizare care arată progresul sarcinilor în structura detaliată a proiectului pentru efort, cost și vânzări.</span><span class="sxs-lookup"><span data-stu-id="96fbd-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Fila și câmpurile urmărire](media/navigation13.png)

- <span data-ttu-id="96fbd-123">**Vânzări**: Oferă legături profunde către ofertele și contractele asociate proiectului.</span><span class="sxs-lookup"><span data-stu-id="96fbd-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="96fbd-124">**Estimări de cheltuieli**: Oferă o grilă care definește cheltuielile proiectului pe baza categoriilor de cheltuieli organizaționale.</span><span class="sxs-lookup"><span data-stu-id="96fbd-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Fila și câmpurile estimări de cheltuieli](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="96fbd-126">Comenzi ale grilei</span><span class="sxs-lookup"><span data-stu-id="96fbd-126">Grid controls</span></span>

<span data-ttu-id="96fbd-127">Următorul este o scurtă prezentare generală a controalelor tipice găsite în diferitele file de planificare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="96fbd-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="96fbd-128">Reîmprospătați</span><span class="sxs-lookup"><span data-stu-id="96fbd-128">Refresh</span></span>

<span data-ttu-id="96fbd-129">**Reîmprospătare**: regăsește cele mai recente date de pe server dacă s-au produs modificări după încărcarea grilei.</span><span class="sxs-lookup"><span data-stu-id="96fbd-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Butonul Reîmprospătare](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="96fbd-131">Grupare după</span><span class="sxs-lookup"><span data-stu-id="96fbd-131">Group by</span></span>

<span data-ttu-id="96fbd-132">**Grupare după**: actualizează gruparea rândurilor din grilă pentru a reflecta resursele, rolurile sau categoriile pe baza nevoilor utilizatorului.</span><span class="sxs-lookup"><span data-stu-id="96fbd-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Grupare după butoane](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="96fbd-134">Anteriorul/următorul</span><span class="sxs-lookup"><span data-stu-id="96fbd-134">Previous/Next</span></span>

<span data-ttu-id="96fbd-135">**Anterior**/**Următorul**: Actualizați perioadele de timp vizibile pe grilele cu etape temporale.</span><span class="sxs-lookup"><span data-stu-id="96fbd-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Butoanele Anterior și Următorul](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="96fbd-137">Scală timp</span><span class="sxs-lookup"><span data-stu-id="96fbd-137">Timescale</span></span>

<span data-ttu-id="96fbd-138">**Scală timp**: Modificați agregarea datelor pe etape între zile, săptămâni, luni și ani.</span><span class="sxs-lookup"><span data-stu-id="96fbd-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Buton Scală timp](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="96fbd-140">Extindeți</span><span class="sxs-lookup"><span data-stu-id="96fbd-140">Expand</span></span>

<span data-ttu-id="96fbd-141">**Extinde**: Redați grila vizibilă pe ecran complet oferind mai multă capacitate de a vedea roluri suplimentare.</span><span class="sxs-lookup"><span data-stu-id="96fbd-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Buton Extindere](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="96fbd-143">Scală timp după</span><span class="sxs-lookup"><span data-stu-id="96fbd-143">Time-phase by</span></span>

<span data-ttu-id="96fbd-144">**Etapare după**: Actualizați gruparea rândurilor din grilă pentru a reflecta estimările de cost pentru estimările vânzărilor.</span><span class="sxs-lookup"><span data-stu-id="96fbd-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="96fbd-145">Acest control se aplică și scriptului estimativ și grilei de urmărire.</span><span class="sxs-lookup"><span data-stu-id="96fbd-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Buton de etapare după](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="96fbd-147">Adăugare coloană</span><span class="sxs-lookup"><span data-stu-id="96fbd-147">Add column</span></span>

<span data-ttu-id="96fbd-148">**Adăugați coloană**: Permite utilizatorului să definească coloanele vizibile din grilă.</span><span class="sxs-lookup"><span data-stu-id="96fbd-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="96fbd-149">Doar coloanele care nu sunt disponibile pot fi adăugate la grilele din formularul **Planificarea proiectului**.</span><span class="sxs-lookup"><span data-stu-id="96fbd-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Adăugați buton de coloană](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]