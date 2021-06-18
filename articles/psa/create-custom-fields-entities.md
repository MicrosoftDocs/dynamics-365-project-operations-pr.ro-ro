---
title: Crearea câmpurilor și entităților particularizate
description: Acest subiect explică modul de creare a seturilor de opțiuni și a entităților în soluția proprie în platforma Power Apps platform.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998966"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c74f8-103">Crearea câmpurilor și entităților particularizate</span><span class="sxs-lookup"><span data-stu-id="c74f8-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c74f8-104">Parcurgeți pașii următori în orice moment în care doriți să creați un set de opțiuni sau o entitate particularizat(ă) pe platforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c74f8-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c74f8-105">Procedurile din acest subiect trebuie parcurse folosind interfața web a Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="c74f8-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c74f8-106">Vă recomandăm să efectuați toate modificările de dimensiune de tarifare particularizate într-o soluție separată.</span><span class="sxs-lookup"><span data-stu-id="c74f8-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c74f8-107">Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță.</span><span class="sxs-lookup"><span data-stu-id="c74f8-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c74f8-108">După ce ați făcut toate modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c74f8-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c74f8-109">Creați câmpuri particularizate și seturi de opțiuni în soluția de dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="c74f8-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c74f8-110">O dimensiune de tarifare poate fi un set de opțiuni sau o entitate.</span><span class="sxs-lookup"><span data-stu-id="c74f8-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c74f8-111">Ambele trebuie să fie create în soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c74f8-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c74f8-112">Pașii din această procedură explică modul de creare a dimensiunilor bazate pe entități și a dimensiunilor bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="c74f8-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c74f8-113">Dimensiuni bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="c74f8-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="c74f8-114">În PSA, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de preț**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c74f8-115">În Explorator soluții, în panoul de navigare din stânga, selectați **Entități**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c74f8-116">Faceți clic pe **Nou** pentru a crea o nouă entitate denumită **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c74f8-117">Introduceți restul de informații solicitate și apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definiție entitate titlu standard](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c74f8-119">Dimensiuni bazate pe seturi de opțiuni</span><span class="sxs-lookup"><span data-stu-id="c74f8-119">Option set-based dimensions</span></span> 
<span data-ttu-id="c74f8-120">Aveți posibilitatea să creați două dimensiuni bazate pe seturi de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="c74f8-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c74f8-121">Utilizați **Locația de lucru resursă** pentru a urmări prețul lucrărilor cu locația **Acasă** și **Local** și utilizați **Ore de lucru resursă** cu valorile **Obișnuite** și **Ore suplimentare** pentru a aplica un marcaj la terminarea lucrărilor.</span><span class="sxs-lookup"><span data-stu-id="c74f8-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c74f8-122">În PSA, selectați **Setări** > **Soluții** și apoi faceți clic dublu pe  **\<your organization name> dimensiuni de preț**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c74f8-123">În Explorator soluții, în panoul de navigare din stânga, selectați **Seturi de opțiuni**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c74f8-124">Faceți clic pe **Nou** pentru a crea un set de opțiuni nou, introduceți restul de informații solicitate, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c74f8-125">Dimensiunea de tarifare bazată pe set de opțiuni denumită Locația de lucru resursă</span><span class="sxs-lookup"><span data-stu-id="c74f8-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c74f8-126">Dimensiunea de tarifare bazată pe set de opțiuni denumită Ore de lucru resursă</span><span class="sxs-lookup"><span data-stu-id="c74f8-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c74f8-127">Crearea de date pentru dimensiunile bazate pe entități</span><span class="sxs-lookup"><span data-stu-id="c74f8-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c74f8-128">Aveți posibilitatea să creați manual date pentru dimensiunile bazate pe entități sau utilizând apelurile de import sau de service Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c74f8-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c74f8-129">Utilizați pașii din această procedură pentru a crea două titluri standard, **Inginer sisteme** și **Inginer sisteme senior** din dimensiunea bazată pe entitate **Titlu standard**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c74f8-130">Dacă datele pe care doriți să le creați sunt mici, ca în exemplul următor, aveți posibilitatea să utilizați un formular standard.</span><span class="sxs-lookup"><span data-stu-id="c74f8-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c74f8-131">În PSA, faceți clic pe **Găsire complexă**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c74f8-132">Selectați entitatea **Titlu standard**, apoi faceți clic pe **Rezultate**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c74f8-133">Toate rândurile din entitatea **Titlu standard** vor fi afișate.</span><span class="sxs-lookup"><span data-stu-id="c74f8-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c74f8-134">Faceți clic pe **Nou**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-134">Click **New**.</span></span> <span data-ttu-id="c74f8-135">În câmpul **Nume**, introduceți „Inginer sisteme” și apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c74f8-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c74f8-136">Închideţi formularul.</span><span class="sxs-lookup"><span data-stu-id="c74f8-136">Close the form.</span></span> 
4. <span data-ttu-id="c74f8-137">Repetați pașii 1-3 pentru a crea un alt titlu standard pentru „Inginer sisteme senior”.</span><span class="sxs-lookup"><span data-stu-id="c74f8-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c74f8-138">Date eșantion pentru entitatea Titlu standard</span><span class="sxs-lookup"><span data-stu-id="c74f8-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]