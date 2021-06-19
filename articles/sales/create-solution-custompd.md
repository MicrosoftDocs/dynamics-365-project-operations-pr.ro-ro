---
title: Crearea unei soluții pentru dimensiunile de tarifare particularizate
description: Acest subiect oferă informații despre cum să creați soluții pentru dimensiuni de preț particularizate.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010351"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="7b0f4-103">Crearea unei soluții pentru dimensiunile de tarifare particularizate</span><span class="sxs-lookup"><span data-stu-id="7b0f4-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="7b0f4-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="7b0f4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="7b0f4-105">Toate modificările dimensiunii de preț personalizate ar trebui să fie într-o soluție separată.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="7b0f4-106">Această bună practică importantă permite flexibilitatea de a actualiza sau elimina modificările după este necesar, ajută la reutilizarea activității dvs. și facilitează portarea acestor modificări în alte instanțe.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="7b0f4-107">După ce faceți toate modificările necesare, exportați această soluție ca soluție **Gestionată** și apoi importați-o în alte instanțe pentru reutilizare.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="7b0f4-108">Crearea unei soluții pentru dimensiunile de tarifare particularizate</span><span class="sxs-lookup"><span data-stu-id="7b0f4-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="7b0f4-109">Selectați **Setări** > **Soluții**, apoi selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="7b0f4-110">Denumiți soluția, *<your organization name> dimensiunile prețurilor*.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="7b0f4-111">Introduceți restul de informații solicitate și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Crearea de soluții pentru dimensiunea de preț particularizată](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="7b0f4-113">Adăugați toate entitățile necesare și componentele corelate la Soluția de dimensiune de preț</span><span class="sxs-lookup"><span data-stu-id="7b0f4-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="7b0f4-114">Adăugați următoarele entități Project Service la soluția dvs. de stabilire a prețurilor pentru a efectua modificări importante ale schemei în soluția de stabilire a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="7b0f4-115">După ce ați finalizat această procedură, entitățile vor recunoaște noile dimensiuni de stabilire a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="7b0f4-116">Selectați **Setări** > **Soluții** și apoi faceți dublu clic pe **<*numele organizației dvs.*> dimensiuni de tarifare**.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="7b0f4-117">În Explorator soluții, în panoul de navigare din stânga, selectați **Adăugare existentă** > **Entități**.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="7b0f4-118">În caseta de dialog **Componente soluție**, selectați următoarele entități:</span><span class="sxs-lookup"><span data-stu-id="7b0f4-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="7b0f4-119">**Real**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-119">**Actual**</span></span>
   - <span data-ttu-id="7b0f4-120">**Resursă ce se poate rezerva**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="7b0f4-121">**Linie estimată**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-121">**Estimate Line**</span></span>
   - <span data-ttu-id="7b0f4-122">**Activitate de proiect**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-122">**Project Task**</span></span>
   - <span data-ttu-id="7b0f4-123">**Detaliu linie factură**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="7b0f4-124">**Linie de jurnal**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-124">**Journal Line**</span></span>
   - <span data-ttu-id="7b0f4-125">**Detaliu linie contract pentru proiect**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="7b0f4-126">**Membru echipă de proiect**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-126">**Project Team Member**</span></span>
   - <span data-ttu-id="7b0f4-127">**Detaliu linie de ofertă**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="7b0f4-128">**Adaos de preț pentru rol**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="7b0f4-129">**Preț pentru rol**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-129">**Role Price**</span></span>
   - <span data-ttu-id="7b0f4-130">**Intrare de timp**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-130">**Time Entry**</span></span>
 
   ![Adăugați entități existente soluția de dimensiuni de tarifare particularizată](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="7b0f4-132">Pentru fiecare entitate, revedeți componentele care se adaugă și lista finală a activelor entității pentru fiecare entitate.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="7b0f4-133">Includeți toate formularele și vizualizările pentru fiecare dintre entitățile selectate.</span><span class="sxs-lookup"><span data-stu-id="7b0f4-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entități adăugate](./media/solution-component-selection.png)


5.  <span data-ttu-id="7b0f4-135">Când vi se solicită să includeți entități dependente pentru entitățile selectate, selectați **Nu, nu includeți componentele necesare.**</span><span class="sxs-lookup"><span data-stu-id="7b0f4-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inclusiv entități dependente](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]