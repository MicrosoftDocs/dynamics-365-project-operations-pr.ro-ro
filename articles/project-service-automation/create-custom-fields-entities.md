---
title: Crearea câmpurilor și entităților particularizate
description: Acest subiect explică modul de creare a seturilor de opțiuni și a entităților în soluția proprie în platforma Power Apps platform.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754811"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c54ae-103">Crearea câmpurilor și entităților particularizate</span><span class="sxs-lookup"><span data-stu-id="c54ae-103">Create custom fields and entities</span></span> 

<span data-ttu-id="c54ae-104">Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă) pe platforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c54ae-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c54ae-105">Procedurile din acest subiect trebuie parcurse folosind interfața web a Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="c54ae-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c54ae-106">Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată.</span><span class="sxs-lookup"><span data-stu-id="c54ae-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c54ae-107">Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță.</span><span class="sxs-lookup"><span data-stu-id="c54ae-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c54ae-108">După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c54ae-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="c54ae-109">Crearea unei soluții particularizate pentru dimensiunile de tarifare</span><span class="sxs-lookup"><span data-stu-id="c54ae-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="c54ae-110">În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți clic pe **Nou** pentru a crea o soluție nouă.</span><span class="sxs-lookup"><span data-stu-id="c54ae-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="c54ae-111">Denumiți soluția, **\<numele organizației dvs. > dimensiuni de tarifare**, introduceți restul de informații solicitate, apoi faceți clic pe **Salvare.**</span><span class="sxs-lookup"><span data-stu-id="c54ae-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Crearea unei soluții particularizate pentru dimensiunile de tarifare](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c54ae-113">Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="c54ae-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c54ae-114">O dimensiune de tarifare poate fi un set de opțiuni sau o entitate.</span><span class="sxs-lookup"><span data-stu-id="c54ae-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c54ae-115">Ambele trebuie să fie create în soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c54ae-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c54ae-116">Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="c54ae-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c54ae-117">Dimensiuni bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="c54ae-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="c54ae-118">În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți dublu clic pe **\<numele organizației dvs.> dimensiunile prețurilor**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c54ae-119">În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c54ae-120">Faceți clic pe **Nou** pentru a crea o nouă entitate denumită **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c54ae-121">Introduceți restul de informații solicitate și apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definiție entitate titlu standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c54ae-123">Dimensiuni bazate pe seturi de opțiuni</span><span class="sxs-lookup"><span data-stu-id="c54ae-123">Option set-based dimensions</span></span> 
<span data-ttu-id="c54ae-124">Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="c54ae-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c54ae-125">Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.</span><span class="sxs-lookup"><span data-stu-id="c54ae-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c54ae-126">În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți dublu clic pe **\<numele organizației dvs. > dimensiuni de tarifare**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c54ae-127">În Explorator soluții, în panoul de navigare din stânga, selectați **Seturi de opțiuni**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c54ae-128">Faceți clic pe **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c54ae-129">Dimensiunea de tarifare bazată pe set de opțiuni denumită Locația de lucru resursă</span><span class="sxs-lookup"><span data-stu-id="c54ae-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c54ae-130">Dimensiunea de tarifare bazată pe set de opțiuni denumită Ore de lucru resursă</span><span class="sxs-lookup"><span data-stu-id="c54ae-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c54ae-131">Crearea de date pentru dimensiunile bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="c54ae-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c54ae-132">Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c54ae-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c54ae-133">Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c54ae-134">Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.</span><span class="sxs-lookup"><span data-stu-id="c54ae-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c54ae-135">În PSA, faceți clic pe **Găsire complexă**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c54ae-136">Selectați entitatea **Titlu standard**, apoi faceți clic pe **Rezultate**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c54ae-137">Toate rândurile din entitatea **Titlu standard** vor fi afișate.</span><span class="sxs-lookup"><span data-stu-id="c54ae-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c54ae-138">Faceți clic pe **Nou**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-138">Click **New**.</span></span> <span data-ttu-id="c54ae-139">În câmpul **Nume**, introduceți „Inginer sisteme” și apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c54ae-140">Închideţi formularul.</span><span class="sxs-lookup"><span data-stu-id="c54ae-140">Close the form.</span></span> 
4. <span data-ttu-id="c54ae-141">Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.</span><span class="sxs-lookup"><span data-stu-id="c54ae-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c54ae-142">Date eșantion pentru entitatea Titlu standard</span><span class="sxs-lookup"><span data-stu-id="c54ae-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c54ae-143">Adăugați toate entitățile PSA necesare și componentele corelate la Soluția de dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="c54ae-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="c54ae-144">Va trebui să adăugați următoarele entități Project Service la soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c54ae-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="c54ae-145">Utilizați pașii din această procedură pentru a face unele modificări importante ale schemei în soluția de tarifare, astfel încât entitățile să devină conștiente de noile dimensiuni de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c54ae-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c54ae-146">În PSA, faceți clic pe **Setări** > **Soluții**, apoi faceți dublu clic pe **\<numele organizației dvs.> dimensiunile prețurilor**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c54ae-147">În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c54ae-148">În caseta de dialog **Componente soluție**, selectați următoarele entități:</span><span class="sxs-lookup"><span data-stu-id="c54ae-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="c54ae-149">Real</span><span class="sxs-lookup"><span data-stu-id="c54ae-149">Actual</span></span>
- <span data-ttu-id="c54ae-150">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="c54ae-150">Bookable Resource</span></span>
- <span data-ttu-id="c54ae-151">Linie estimată</span><span class="sxs-lookup"><span data-stu-id="c54ae-151">Estimate Line</span></span>
- <span data-ttu-id="c54ae-152">Detaliu linie factură</span><span class="sxs-lookup"><span data-stu-id="c54ae-152">Invoice Line Detail</span></span>
- <span data-ttu-id="c54ae-153">Linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="c54ae-153">Journal Line</span></span>
- <span data-ttu-id="c54ae-154">Detaliu linie contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="c54ae-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="c54ae-155">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="c54ae-155">Project Team Member</span></span>
- <span data-ttu-id="c54ae-156">Detaliu linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="c54ae-156">Quote Line Detail</span></span>
- <span data-ttu-id="c54ae-157">Adaos de preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="c54ae-157">Role Price Markup</span></span>
- <span data-ttu-id="c54ae-158">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="c54ae-158">Role Price</span></span> 
- <span data-ttu-id="c54ae-159">Intrare de timp</span><span class="sxs-lookup"><span data-stu-id="c54ae-159">Time Entry</span></span> 

> ![Adăugați entități existente la soluția de dimensiuni de tarifare](media/Existing-entities-to-PD-solution.png)

> ![Selectare componente soluție](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="c54ae-162">Asigurați-vă că includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.</span><span class="sxs-lookup"><span data-stu-id="c54ae-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c54ae-163">Când vi se solicită să includeți orice entități dependente pentru entitățile selectate mai sus, faceți clic pe **Nu**.</span><span class="sxs-lookup"><span data-stu-id="c54ae-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Nu includeți toate componentele corelate](media/Do-not-include-required.png)


