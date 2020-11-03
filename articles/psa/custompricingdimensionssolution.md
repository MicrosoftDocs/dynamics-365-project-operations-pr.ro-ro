---
title: Creare soluții particularizate pentru dimensiunile de tarifare
description: Acest subiect explică cum să creați o soluție personalizată atunci când creați dimensiuni de tarifare personalizate.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082805"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="f4216-103">Creare soluții particularizate pentru dimensiunile de tarifare</span><span class="sxs-lookup"><span data-stu-id="f4216-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4216-104">Toate modificările dimensiunii de preț personalizate ar trebui să fie într-o soluție separată.</span><span class="sxs-lookup"><span data-stu-id="f4216-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="f4216-105">Această bună practică importantă oferă flexibilitate în viitor pentru a actualiza sau elimina modificările după este necesar, va ajuta la reutilizarea activității dvs. și facilitează portarea acestor modificări într-o altă instanță.</span><span class="sxs-lookup"><span data-stu-id="f4216-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="f4216-106">După ce faceți modificările necesare, exportați această soluție ca **Soluție gestionată** și importați-o în alte instanțe pentru a reutiliza configurația dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="f4216-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="f4216-107">Selectați **Setări** > **Soluții** , apoi selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="f4216-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="f4216-108">Denumiți soluția, **\<your organization name> dimensiunile de preț** , introduceți informațiile necesare rămase și apoi selectați **Salvați**.</span><span class="sxs-lookup"><span data-stu-id="f4216-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Crearea unei soluții particularizate pentru dimensiunile de tarifare](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f4216-110">Adăugați toate entitățile necesare și componentele corelate la Soluția de dimensiune de preț</span><span class="sxs-lookup"><span data-stu-id="f4216-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="f4216-111">Va trebui să adăugați următoarele entități Project Service la soluția dvs. de tarifare.</span><span class="sxs-lookup"><span data-stu-id="f4216-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="f4216-112">Completați pașii din această procedură pentru a face unele modificări importante ale schemei în soluția de tarifare, astfel încât entitățile să devină conștiente de noile dimensiuni de tarifare.</span><span class="sxs-lookup"><span data-stu-id="f4216-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="f4216-113">Selectați **Setări** > **Soluții** și apoi faceți clic dublu pe **\<your organization name> dimensiuni de preț**.</span><span class="sxs-lookup"><span data-stu-id="f4216-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f4216-114">În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.</span><span class="sxs-lookup"><span data-stu-id="f4216-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="f4216-115">În caseta de dialog **Componente soluție** , selectați următoarele entități:</span><span class="sxs-lookup"><span data-stu-id="f4216-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="f4216-116">Real</span><span class="sxs-lookup"><span data-stu-id="f4216-116">Actual</span></span>
- <span data-ttu-id="f4216-117">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="f4216-117">Bookable Resource</span></span>
- <span data-ttu-id="f4216-118">Linie estimată</span><span class="sxs-lookup"><span data-stu-id="f4216-118">Estimate Line</span></span>
- <span data-ttu-id="f4216-119">Activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="f4216-119">Project Task</span></span>
- <span data-ttu-id="f4216-120">Detaliu linie factură</span><span class="sxs-lookup"><span data-stu-id="f4216-120">Invoice Line Detail</span></span>
- <span data-ttu-id="f4216-121">Linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="f4216-121">Journal Line</span></span>
- <span data-ttu-id="f4216-122">Detaliu linie contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="f4216-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="f4216-123">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="f4216-123">Project Team Member</span></span>
- <span data-ttu-id="f4216-124">Detaliu linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="f4216-124">Quote Line Detail</span></span>
- <span data-ttu-id="f4216-125">Adaos de preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="f4216-125">Role Price Markup</span></span>
- <span data-ttu-id="f4216-126">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="f4216-126">Role Price</span></span> 
- <span data-ttu-id="f4216-127">Intrare de timp</span><span class="sxs-lookup"><span data-stu-id="f4216-127">Time Entry</span></span> 

> ![Adăugați entități existente la soluția de dimensiuni de tarifare](media/Existing-entities-to-PD-solution.png)

> ![Selectare componente soluție](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="f4216-130">Asigurați-vă că includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.</span><span class="sxs-lookup"><span data-stu-id="f4216-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="f4216-131">Când vi se solicită să includeți orice entități dependente pentru entitățile selectate, selectați **Nu**.</span><span class="sxs-lookup"><span data-stu-id="f4216-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Nu includeți toate componentele corelate](media/Do-not-include-required.png)


