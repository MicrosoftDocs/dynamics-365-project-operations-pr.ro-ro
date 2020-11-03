---
title: Crearea de entități și câmpuri particularizate ca dimensiuni de preț
description: Acest subiect oferă informații despre cum să creați seturi de opțiuni personalizate sau entități.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082834"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="015e6-103">Crearea de entități și câmpuri particularizate ca dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="015e6-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="015e6-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="015e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="015e6-105">Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă).</span><span class="sxs-lookup"><span data-stu-id="015e6-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="015e6-106">Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată.</span><span class="sxs-lookup"><span data-stu-id="015e6-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="015e6-107">Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță.</span><span class="sxs-lookup"><span data-stu-id="015e6-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="015e6-108">După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="015e6-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="015e6-109">Crearea unei soluții particularizate pentru dimensiunile de tarifare</span><span class="sxs-lookup"><span data-stu-id="015e6-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="015e6-110">Accesați **Setări** > **Soluții** și apoi selectați **Nou** pentru a crea o soluție nouă.</span><span class="sxs-lookup"><span data-stu-id="015e6-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="015e6-111">Denumiți soluția, **\<your organization name> dimensiunile de preț** , introduceți informațiile necesare rămase și apoi selectați **Salvați**.</span><span class="sxs-lookup"><span data-stu-id="015e6-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="015e6-112">Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="015e6-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="015e6-113">O dimensiune de tarifare poate fi un set de opțiuni sau o entitate.</span><span class="sxs-lookup"><span data-stu-id="015e6-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="015e6-114">Ambele trebuie să fie create în soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="015e6-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="015e6-115">Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="015e6-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="015e6-116">Dimensiuni bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="015e6-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="015e6-117">Accesați **Setări** > **Soluții** , apoi faceți dublu clic pe **\<your organization name> dimensiunile prețurilor**.</span><span class="sxs-lookup"><span data-stu-id="015e6-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="015e6-118">În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.</span><span class="sxs-lookup"><span data-stu-id="015e6-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="015e6-119">Selectați **Nou** pentru a crea o nouă entitate denumită **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="015e6-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="015e6-120">Introduceți restul de informații solicitate și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="015e6-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="015e6-121">Dimensiuni bazate pe seturi de opțiuni</span><span class="sxs-lookup"><span data-stu-id="015e6-121">Option set-based dimensions</span></span> 
<span data-ttu-id="015e6-122">Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="015e6-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="015e6-123">Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.</span><span class="sxs-lookup"><span data-stu-id="015e6-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="015e6-124">Accesați **Setări** > **Soluții** , apoi faceți dublu clic pe  **\<your organization name> dimensiunile prețurilor**.</span><span class="sxs-lookup"><span data-stu-id="015e6-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="015e6-125">În Explorator soluții, în panoul de navigare din stânga, selectați **Seturi de opțiuni**.</span><span class="sxs-lookup"><span data-stu-id="015e6-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="015e6-126">Selectați **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="015e6-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="015e6-127">Crearea de date pentru dimensiunile bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="015e6-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="015e6-128">Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="015e6-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="015e6-129">Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="015e6-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="015e6-130">Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.</span><span class="sxs-lookup"><span data-stu-id="015e6-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="015e6-131">Selectați **Găsire avansată** , selectați entitatea **Titlu standard** , apoi selectați **Rezultate**.</span><span class="sxs-lookup"><span data-stu-id="015e6-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="015e6-132">Toate rândurile din entitatea **Titlu standard** vor fi afișate.</span><span class="sxs-lookup"><span data-stu-id="015e6-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="015e6-133">Selectați **Nou** și pe câmpul **Nume** , introduceți „Inginer de sistem” și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="015e6-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="015e6-134">Închideți formularul.</span><span class="sxs-lookup"><span data-stu-id="015e6-134">Close the form.</span></span> 
4. <span data-ttu-id="015e6-135">Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.</span><span class="sxs-lookup"><span data-stu-id="015e6-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="015e6-136">Adăugați toate entitățile necesare și componentele corelate la Soluția de dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="015e6-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="015e6-137">Va trebui să adăugați următoarele entități la soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="015e6-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="015e6-138">Utilizați pașii din această procedură pentru a face unele modificări importante ale schemei în soluția de tarifare, astfel încât entitățile să devină conștiente de noile dimensiuni de tarifare.</span><span class="sxs-lookup"><span data-stu-id="015e6-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="015e6-139">Selectați **Setări** > **Soluții** și faceți clic dublu pe **\<your organization name> dimensiuni de preț**.</span><span class="sxs-lookup"><span data-stu-id="015e6-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="015e6-140">În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.</span><span class="sxs-lookup"><span data-stu-id="015e6-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="015e6-141">În caseta de dialog **Componente soluție** , selectați următoarele entități:</span><span class="sxs-lookup"><span data-stu-id="015e6-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="015e6-142">Real</span><span class="sxs-lookup"><span data-stu-id="015e6-142">Actual</span></span>
  - <span data-ttu-id="015e6-143">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="015e6-143">Bookable Resource</span></span>
  - <span data-ttu-id="015e6-144">Linie estimată</span><span class="sxs-lookup"><span data-stu-id="015e6-144">Estimate Line</span></span>
  - <span data-ttu-id="015e6-145">Detaliu linie factură</span><span class="sxs-lookup"><span data-stu-id="015e6-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="015e6-146">Linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="015e6-146">Journal Line</span></span>
  - <span data-ttu-id="015e6-147">Detaliu linie contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="015e6-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="015e6-148">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="015e6-148">Project Team Member</span></span>
  - <span data-ttu-id="015e6-149">Detaliu linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="015e6-149">Quote Line Detail</span></span>
  - <span data-ttu-id="015e6-150">Adaos de preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="015e6-150">Role Price Markup</span></span>
  - <span data-ttu-id="015e6-151">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="015e6-151">Role Price</span></span> 
  - <span data-ttu-id="015e6-152">Intrare de timp</span><span class="sxs-lookup"><span data-stu-id="015e6-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="015e6-153">Asigurați-vă că includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.</span><span class="sxs-lookup"><span data-stu-id="015e6-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="015e6-154">Când vi se solicită să includeți orice entități dependente pentru entitățile selectate mai sus, selectați **Nu**.</span><span class="sxs-lookup"><span data-stu-id="015e6-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

