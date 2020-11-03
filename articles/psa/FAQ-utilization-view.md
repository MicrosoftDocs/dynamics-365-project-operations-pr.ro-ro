---
title: Vizualizați utilizarea taxabilă pentru o resursă
description: Acest subiect furnizează informații despre vizualizarea utilizării resurselor.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082818"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="0ab08-103">Vizualizați utilizarea taxabilă pentru o resursă</span><span class="sxs-lookup"><span data-stu-id="0ab08-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="0ab08-104">**Vizualizarea utilizării** pe pagina **Utilizarea resurselor Project Service** afișează utilizarea taxabilă pentru fiecare resursă care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="0ab08-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="0ab08-105">Întrucât vizualizarea se bazează pe tabloul de planificare, astfel încât veți găsi multe din aceleași funcții.</span><span class="sxs-lookup"><span data-stu-id="0ab08-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Captură ecran pentru Vizualizarea utilizării](media/FAQ-utilization-1.png)
 

<span data-ttu-id="0ab08-107">Calculul de utilizare taxabilă funcționează după cum urmează:</span><span class="sxs-lookup"><span data-stu-id="0ab08-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="0ab08-108">Utilizare taxabilă = (ore efective taxabile)/(capacitate resursă)</span><span class="sxs-lookup"><span data-stu-id="0ab08-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="0ab08-109">Celulele reprezintă utilizarea taxabilă calculată pentru perioada selectată (zile, săptămâni sau luni).</span><span class="sxs-lookup"><span data-stu-id="0ab08-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="0ab08-110">Culorile din fiecare celulă arată utilizarea taxabilă pentru o resursă în comparație cu utilizarea taxabilă țintă a acestora.</span><span class="sxs-lookup"><span data-stu-id="0ab08-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="0ab08-111">Utilizarea țintă poate fi setată fie pe rolul implicit al resursei, fie pe resursa individuală în sine.</span><span class="sxs-lookup"><span data-stu-id="0ab08-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="0ab08-112">Calculul privește individual mai întâi ținta, apoi rolul implicit al resursei.</span><span class="sxs-lookup"><span data-stu-id="0ab08-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="0ab08-113">Setați țintă pe o resursă</span><span class="sxs-lookup"><span data-stu-id="0ab08-113">Set target on a resource</span></span>

1. <span data-ttu-id="0ab08-114">Accesați **Resurse**\> **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="0ab08-115">Selectați o resursă pentru a deschide înregistrarea.</span><span class="sxs-lookup"><span data-stu-id="0ab08-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="0ab08-116">În fila **Project Service** , puteți seta utilizarea țintă a resursei.</span><span class="sxs-lookup"><span data-stu-id="0ab08-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Captură de ecran a utilizării filei Project Service pentru a seta utilizarea țintă](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="0ab08-118">Setați utilizarea țintă pe un rol</span><span class="sxs-lookup"><span data-stu-id="0ab08-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="0ab08-119">Accesați **Resurse** \> **Roluri de resursă**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="0ab08-120">Selectați un rol și deschideți înregistrarea.</span><span class="sxs-lookup"><span data-stu-id="0ab08-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="0ab08-121">Setați utilizarea țintei pentru rol.</span><span class="sxs-lookup"><span data-stu-id="0ab08-121">Set the target utilization for the role.</span></span>

> ![Captură de ecran a utilizării Rolurilor resursei pentru a seta utilizarea țintă](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="0ab08-123">Calculați utilizarea taxabilă pentru o resursă</span><span class="sxs-lookup"><span data-stu-id="0ab08-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="0ab08-124">Pentru a calcula utilizarea taxabilă pentru o resursă, va trebui să întruniți câteva cerințe preliminare.</span><span class="sxs-lookup"><span data-stu-id="0ab08-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="0ab08-125">Setați rolul implicit pentru resursa individuală</span><span class="sxs-lookup"><span data-stu-id="0ab08-125">Set default role for individual resource</span></span>

<span data-ttu-id="0ab08-126">În primul rând, utilizarea țintă trebuie să fi setată fie pe resursa individuală, fie pe rolurile resursei.</span><span class="sxs-lookup"><span data-stu-id="0ab08-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="0ab08-127">Dacă utilizați rolurile resursei pentru obiective, fiecare resursă individuală trebuie să aibă un rol implicit.</span><span class="sxs-lookup"><span data-stu-id="0ab08-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="0ab08-128">Pentru a seta acest lucru, accesați **Resurse** \> **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="0ab08-129">Selectați o resursă, deschideți înregistrarea, apoi selectați fila **Project service**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="0ab08-130">În grila **Rol resursă** , asigurați-vă că există un rol pentru resursă și **Este implicit** este setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="0ab08-131">Modificați tipul de facturare pentru rolul de resursă</span><span class="sxs-lookup"><span data-stu-id="0ab08-131">Change billing type for resource role</span></span>

<span data-ttu-id="0ab08-132">Rolurile de resursă trebuie setate pentru a avea un tip de facturare **Taxabil**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="0ab08-133">Accesați **Resurse** \> **Roluri de resursă**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="0ab08-134">Deschideți înregistrarea pe care doriți să o acualizați, apoi setați implicit tipul de facturare pe **Taxabil**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="0ab08-135">Setați orele lucrătroare pentru rolul resursei</span><span class="sxs-lookup"><span data-stu-id="0ab08-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="0ab08-136">Resursa trebuie să aibă ore de lucru pentru capacitatea de calcul.</span><span class="sxs-lookup"><span data-stu-id="0ab08-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="0ab08-137">Accesați **Resurse**\> **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="0ab08-138">Selectați o resursă pentru a deschide înregistrarea, apoi selectați **Afișați orele de lucru**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="0ab08-139">Puteți actualiza în bloc lista de resurse aplicând un **șablon de ore de lucru** din vizualizarea **Listă de resurse**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="0ab08-140">Depanarea orelor efective taxabile</span><span class="sxs-lookup"><span data-stu-id="0ab08-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="0ab08-141">Orele efective taxabile provin din entitatea **Valori reale**.</span><span class="sxs-lookup"><span data-stu-id="0ab08-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="0ab08-142">Valorile reale cu un tip de facturare **Taxabil** sunt incluse în calcul și din acest motiv trebuie să aveți proiecte în cazul în care valorile reale sunt taxabile.</span><span class="sxs-lookup"><span data-stu-id="0ab08-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="0ab08-143">Dacă nu vedeți utilizarea taxabilă, aici sunt câteva aspecte care pot fi verificate:</span><span class="sxs-lookup"><span data-stu-id="0ab08-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="0ab08-144">Resursa are ore de lucru definite pentru capacitate.</span><span class="sxs-lookup"><span data-stu-id="0ab08-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="0ab08-145">Resursa are fie o țintă de utilizare definită individual, fie un rol implicit atribuit.</span><span class="sxs-lookup"><span data-stu-id="0ab08-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="0ab08-146">Rolul are o țintă de utilizare definită pentru el.</span><span class="sxs-lookup"><span data-stu-id="0ab08-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="0ab08-147">Valorile reale au un tip de facturare **Taxabil** pentru perioada pentru care estimați un calcul de utilizare.</span><span class="sxs-lookup"><span data-stu-id="0ab08-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="0ab08-148">Verificați următoarele dacă vedeți valorile actuale cu alte tipuri de facturare decât contra cost:</span><span class="sxs-lookup"><span data-stu-id="0ab08-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="0ab08-149">Rolul utilizat pe valorile reale are un tip de facturare implicit sau altul decât facturabil.</span><span class="sxs-lookup"><span data-stu-id="0ab08-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="0ab08-150">Rolul din linia contractului subadiacentă proiectului a fost setat pe non-taxabil.</span><span class="sxs-lookup"><span data-stu-id="0ab08-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="0ab08-151">Proiectul nu are o linie a contractului asociată.</span><span class="sxs-lookup"><span data-stu-id="0ab08-151">The project does not have an associated contract line.</span></span>

