---
title: Propuneți resurse de proiect
description: Acest subiect furnizează informații despre modul de propunere a resurselor de proiect.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754824"
---
# <a name="propose-project-resources"></a><span data-ttu-id="c63c1-103">Propuneți resurse de proiect</span><span class="sxs-lookup"><span data-stu-id="c63c1-103">Propose project resources</span></span>

<span data-ttu-id="c63c1-104">Managerii de resurse pot propune o resursă către managerul de proiect utilizând o solicitare de resurse.</span><span class="sxs-lookup"><span data-stu-id="c63c1-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="c63c1-105">Din grila de solicitări sau din cererea în sine,selectați **Găsire resurse**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="c63c1-106">În pagina **Asistent planificare**, selectați resursa, apoi, în panoul **Creare rezervare resursă**, în câmpul **Stare rezervare**, selectați **Rezervare.**</span><span class="sxs-lookup"><span data-stu-id="c63c1-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Resursa propusă selectată.](media/Resource-Management-image62.png)

<span data-ttu-id="c63c1-108">Apar următoarele actualizări de stare:</span><span class="sxs-lookup"><span data-stu-id="c63c1-108">The following status updates occur:</span></span>

- <span data-ttu-id="c63c1-109">În pagina **Asistent programare**, indicatorii de stare sunt actualizați pentru a indica faptul că rezervarea este propusă, nu rezervată ferm.</span><span class="sxs-lookup"><span data-stu-id="c63c1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicatori de stare pentru rezervarea propusă pe pagina Asistent programări](media/Resource-Management-image63.png)

- <span data-ttu-id="c63c1-111">La solicitarea de resurse, starea se modifică la **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Starea solicitării de resurse se modifică la Necesită revizuire.](media/Resource-Management-image64.png)

- <span data-ttu-id="c63c1-113">În fila **Echipă** a proiectului, valoarea de **Stare solicitare** a membrului generic al echipei este schimbată la **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Starea de solicitare a membrului generic al echipei este schimbată la Necesită revizuire pe fila Echipă.](media/Resource-Management-image48.png)

<span data-ttu-id="c63c1-115">Managerul de proiect poate accepta sau respinge propunerea.</span><span class="sxs-lookup"><span data-stu-id="c63c1-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="c63c1-116">Atunci când managerii de resurse procesează solicitările de resurse, pot utiliza oricare dintre următoarele abordări:</span><span class="sxs-lookup"><span data-stu-id="c63c1-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="c63c1-117">Propun mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a îndeplini orele necesare.</span><span class="sxs-lookup"><span data-stu-id="c63c1-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="c63c1-118">Orele propuse sunt apoi împărțite între mai multe resurse care pot satisface orele necesare.</span><span class="sxs-lookup"><span data-stu-id="c63c1-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="c63c1-119">În acest scenariu, orele nu se pot suprapune.</span><span class="sxs-lookup"><span data-stu-id="c63c1-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="c63c1-120">Propun mai puține resurse decât sunt necesare.</span><span class="sxs-lookup"><span data-stu-id="c63c1-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="c63c1-121">În acest scenariu, capacitatea de resurse propusă este mai mică decât orele necesare pe care le-a indicat solicitantul.</span><span class="sxs-lookup"><span data-stu-id="c63c1-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="c63c1-122">Prin urmare, atunci când solicitantul acceptă resursele propuse, este creată o cerință de resursă neîndeplinită pentru a captura cererea rămasă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="c63c1-123">Rezervă mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a finaliza lucrarea.</span><span class="sxs-lookup"><span data-stu-id="c63c1-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="c63c1-124">Rezervă mai puține resurse decât sunt necesare.</span><span class="sxs-lookup"><span data-stu-id="c63c1-124">Book fewer resources than are required.</span></span> <span data-ttu-id="c63c1-125">În acest scenariu, orele rezervate sunt mai puține decât orele necesare.</span><span class="sxs-lookup"><span data-stu-id="c63c1-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="c63c1-126">Sistemul vă ghidează să propuneți resurse în loc de rezervări, astfel încât solicitantul să poată verifica și urmări cererea rămasă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="c63c1-127">Utilizarea facturabilă</span><span class="sxs-lookup"><span data-stu-id="c63c1-127">Billable utilization</span></span>

<span data-ttu-id="c63c1-128">Resursele pot avea o utilizare facturabilă țintă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="c63c1-129">Această utilizare țintă este fie definită ca un atribut al rolului implicit al unei resurse, fie setat pe înregistrarea resursei individuale care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="c63c1-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="c63c1-130">Calculele de utilizare se bazează pe orele efective pe care le-au raportat resursele utilizând intrările de timp aprobate.</span><span class="sxs-lookup"><span data-stu-id="c63c1-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="c63c1-131">Următoarele formule sunt utilizate pentru a calcula utilizarea:</span><span class="sxs-lookup"><span data-stu-id="c63c1-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="c63c1-132">Utilizare facturabilă = Ore efective taxabile ÷  Capacitate resursă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="c63c1-133">Utilizare non-facturabilă = Timp real cu ID-ul de facturare = non-exigibil, Complementar sau Indisponibil ÷ capacitate resursă</span><span class="sxs-lookup"><span data-stu-id="c63c1-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="c63c1-134">Intern = Timp real fără contract de vânzare ÷ Capacitate resursă</span><span class="sxs-lookup"><span data-stu-id="c63c1-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="c63c1-135">Capacitate resursă = Ore de lucru resursă – Absent de la birou – zile nelucrătoare</span><span class="sxs-lookup"><span data-stu-id="c63c1-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="c63c1-136">Puteți găsi vizualizarea de **Utilizare resurse** în panoul **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Vizualizarea utilizării resurselor](media/Resource-Management-image65.png)

<span data-ttu-id="c63c1-138">Fiecare celulă din grilă reprezintă procentul de utilizare facturabil al resursei într-o perioadă, cum ar fi o zi, o săptămână sau o lună.</span><span class="sxs-lookup"><span data-stu-id="c63c1-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="c63c1-139">Următoarele formule sunt utilizate pentru a colora celulele:</span><span class="sxs-lookup"><span data-stu-id="c63c1-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="c63c1-140">**Verde:** Utilizare facturabilă \>= Utilizarea țintă a resursei.</span><span class="sxs-lookup"><span data-stu-id="c63c1-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="c63c1-141">**Galben:** Utilizare țintă – 20 \<= Utilizare facturabilă \< Utilizare țintă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="c63c1-142">**Roșu:** Utilizare facturabilă \< utilizare țintă – 20.</span><span class="sxs-lookup"><span data-stu-id="c63c1-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="c63c1-143">Deoarece vizualizarea **Utilizare resurse** se bazează pe tabloul de planificare, aveți posibilitatea să utilizați capacitățile de filtrare ale tabloului de planificare pentru a filtra rezultatele.</span><span class="sxs-lookup"><span data-stu-id="c63c1-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="c63c1-144">Grila necesită să setați o utilizare țintă fie pe rol, fie pe resursa individuală.</span><span class="sxs-lookup"><span data-stu-id="c63c1-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="c63c1-145">Pentru a face această configurare, accesați **Resurse**\> **Roluri resurse**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="c63c1-146">În plus, un rol implicit trebuie să fie atribuit fiecărei resurse care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="c63c1-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="c63c1-147">Accesați **Resurse**\> **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="c63c1-148">În fila **Project Service**, verificați că este definit un rol de resursă și că câmpul **Este implicit** pentru acesta este setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="c63c1-149">Aveți posibilitatea să adăugați roluri suplimentare acolo unde **Este implicit = Nu**.</span><span class="sxs-lookup"><span data-stu-id="c63c1-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="c63c1-150">Rolul în care **Este implicit = da** este utilizat pentru a evalua utilizarea resursei față de obiectivul pentru rolul respectiv.</span><span class="sxs-lookup"><span data-stu-id="c63c1-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Set de roluri implicite](media/Resource-Management-image67.png)

<span data-ttu-id="c63c1-152">În fila **Project Service**, puteți seta, de asemenea, o utilizare țintă individuală pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="c63c1-153">Calculul utilizării folosește apoi acea utilizare țintă pentru a evalua ținta resursei în locul țintei rolului implicit al resursei.</span><span class="sxs-lookup"><span data-stu-id="c63c1-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="c63c1-154">Utilizarea este afișată pentru o resursă numai în cazul în care resursa are aprobat timp taxabil în perioada afișată în grilă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="c63c1-155">Disponibilitatea resursei</span><span class="sxs-lookup"><span data-stu-id="c63c1-155">Resource availability</span></span>

<span data-ttu-id="c63c1-156">Este esențial ca managerii de resurse să poată vizualiza disponibilitatea resurselor și să actualizeze rezervările.</span><span class="sxs-lookup"><span data-stu-id="c63c1-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="c63c1-157">în unele cazuri, nu există nicio cerere formală (cerere de resurse), dar un manager de resurse trebuie să răspundă la o cerere neplanificată care vine prin canale, cum ar fi un e-mail, apel telefonic sau mesaj instant.</span><span class="sxs-lookup"><span data-stu-id="c63c1-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="c63c1-158">Managerii de resurse utilizează tabloul de planificare pentru a actualiza resursele și rezervările.</span><span class="sxs-lookup"><span data-stu-id="c63c1-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="c63c1-159">Programul de lucru al resurselor se utilizează ca bază pentru calcularea disponibilității unei resurse.</span><span class="sxs-lookup"><span data-stu-id="c63c1-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="c63c1-160">Rezervările de resurse consumă capacitatea resurselor.</span><span class="sxs-lookup"><span data-stu-id="c63c1-160">Resource bookings consume the capacity of the resources.</span></span>

![Bord de planificare](media/Resource-Management-image68.png)

<span data-ttu-id="c63c1-162">Consiliul de planificare utilizează culori și umbrire pentru a afișa rezervările, disponibilitatea și rezervările excedentare și, de asemenea, starea rezervărilor.</span><span class="sxs-lookup"><span data-stu-id="c63c1-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="c63c1-163">O setare din setările panoului de planificare vă permite să afișați o legendă.</span><span class="sxs-lookup"><span data-stu-id="c63c1-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="c63c1-164">În cazul în care o săgeată orientată spre dreapta apare lângă o resursă individuală care se poate rezerva în tabloul de planificare, resursa poate fi extinsă pentru a afișa detalii despre activitatea pe care este rezervată resursa.</span><span class="sxs-lookup"><span data-stu-id="c63c1-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Resursă care poate fi rezervată extinsă în panoul de planificare](media/Resource-Management-image69.png)

<span data-ttu-id="c63c1-166">Deoarece Dynamics 365 Project Service Automation utilizează motorul Universal Resource Scheduling, dacă aveți instalat și Dynamics 365 Field Service, puteți vizualiza detaliile rezervărilor de resurse pentru proiecte, comenzi de lucru și orice alte entități la care ați extins programarea.</span><span class="sxs-lookup"><span data-stu-id="c63c1-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalii privind rezervările de resurse pentru proiecte și comenzi de lucru](media/Resource-Management-image70.png)

<span data-ttu-id="c63c1-168">Pentru a vizualiza mai multe detalii despre o resursă individuală, faceți clic cu butonul din dreapta pe acesta pentru a deschide fișa resursei.</span><span class="sxs-lookup"><span data-stu-id="c63c1-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Cardul de resurse](media/Resource-Management-image71.png)