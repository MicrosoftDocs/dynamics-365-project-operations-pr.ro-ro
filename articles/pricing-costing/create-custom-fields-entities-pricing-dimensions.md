---
title: Crearea de entități și câmpuri particularizate ca dimensiuni de preț
description: Acest subiect oferă informații despre cum să creați seturi de opțiuni personalizate sau entități.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275643"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="3f178-103">Crearea de entități și câmpuri particularizate ca dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="3f178-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="3f178-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="3f178-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3f178-105">Parcurgeți pașii următori când doriți să creați un set de opțiuni sau o entitate particularizat(ă) pentru a o utiliza drept dimensiune de preț.</span><span class="sxs-lookup"><span data-stu-id="3f178-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="3f178-106">Pentru mai multe informații, consultați [Prezentare generală a dimensiunii de preț](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3f178-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3f178-107">Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată.</span><span class="sxs-lookup"><span data-stu-id="3f178-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="3f178-108">Această bună practică importantă oferă flexibilitate în viitor pentru actualizarea sau eliminarea modificărilor, după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="3f178-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="3f178-109">Acest lucru vă va ajuta, de asemenea, la reutilizarea muncii dvs. și va facilita portarea acestor modificări într-o altă instanță După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurarea prețurilor.</span><span class="sxs-lookup"><span data-stu-id="3f178-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="3f178-110">Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="3f178-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="3f178-111">O dimensiune de tarifare poate fi un set de opțiuni sau o entitate.</span><span class="sxs-lookup"><span data-stu-id="3f178-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="3f178-112">Ambele trebuie să fie create în soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="3f178-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="3f178-113">Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="3f178-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="3f178-114">Dimensiuni bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="3f178-114">Entity-based dimensions</span></span>
<span data-ttu-id="3f178-115">Pentru a crea dimensiuni bazate pe entități, urmați acești pași:</span><span class="sxs-lookup"><span data-stu-id="3f178-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="3f178-116">Accesați **Setări** > **Soluții**, apoi faceți dublu clic pe **\<your organization name> dimensiunile prețurilor**.</span><span class="sxs-lookup"><span data-stu-id="3f178-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="3f178-117">În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.</span><span class="sxs-lookup"><span data-stu-id="3f178-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="3f178-118">Selectați **Nou** pentru a crea o nouă entitate denumită **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="3f178-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="3f178-119">Introduceți restul de informații solicitate și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="3f178-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definiție entitate titlu standard](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="3f178-121">Dimensiuni bazate pe seturi de opțiuni</span><span class="sxs-lookup"><span data-stu-id="3f178-121">Option set-based dimensions</span></span> 
<span data-ttu-id="3f178-122">Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="3f178-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="3f178-123">Utilizați **Locația de lucru a resurselor** pentru a urmări locația de lucru **Acasă** și **La fața locului**.</span><span class="sxs-lookup"><span data-stu-id="3f178-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="3f178-124">Utilizați **Resurse Program de lucru** cu valori **Regulat** și **Ore suplimentare** pentru a aplica un adaos când lucrarea este finalizată.</span><span class="sxs-lookup"><span data-stu-id="3f178-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="3f178-125">Următorul grafic oferă o vizualizare a dimensiunii **Locația de lucru a resurselor**.</span><span class="sxs-lookup"><span data-stu-id="3f178-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Locația de lucru resursă](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="3f178-127">Următorul grafic oferă o vizualizare a dimensiunii **Ore de lucru resursă**.</span><span class="sxs-lookup"><span data-stu-id="3f178-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensiunea de tarifare bazată pe set de opțiuni denumită Ore de lucru resursă](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="3f178-129">Accesați **Setări** > **Soluții**, apoi faceți dublu clic pe  **\<your organization name> dimensiunile prețurilor**.</span><span class="sxs-lookup"><span data-stu-id="3f178-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3f178-130">În Explorator soluții, în panoul de navigare din stânga, selectați  **Seturi de opțiuni**.</span><span class="sxs-lookup"><span data-stu-id="3f178-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="3f178-131">Selectați **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="3f178-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="3f178-132">Crearea de date pentru dimensiunile bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="3f178-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="3f178-133">Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3f178-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="3f178-134">Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="3f178-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="3f178-135">Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.</span><span class="sxs-lookup"><span data-stu-id="3f178-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="3f178-136">Selectați **Găsire complexă**.</span><span class="sxs-lookup"><span data-stu-id="3f178-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="3f178-137">Selectați entitatea **Titlu standard**, apoi selectați **Rezultate**.</span><span class="sxs-lookup"><span data-stu-id="3f178-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="3f178-138">Toate rândurile din entitatea **Titlu standard** vor fi afișate.</span><span class="sxs-lookup"><span data-stu-id="3f178-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="3f178-139">Selectați **Nou** și pe câmpul **Nume**, introduceți „Inginer de sistem” și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="3f178-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="3f178-140">Închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="3f178-140">Close the page.</span></span> 
5. <span data-ttu-id="3f178-141">Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.</span><span class="sxs-lookup"><span data-stu-id="3f178-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Date eșantion pentru entitatea Titlu standard](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]