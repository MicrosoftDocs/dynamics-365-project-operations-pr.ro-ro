---
title: Crearea ofertelor de proiecte din oportunități
description: Acest subiect oferă informații despre crearea unei oferte de proiect dintr-o oportunitate.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082708"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="b8fd9-103">Crearea ofertelor de proiecte din oportunități</span><span class="sxs-lookup"><span data-stu-id="b8fd9-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="b8fd9-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="b8fd9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b8fd9-105">Ofertele pot fi create din oportunități de proiect în următoarele moduri:</span><span class="sxs-lookup"><span data-stu-id="b8fd9-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="b8fd9-106">De la fila **Oferte** de pe pagina **Oportunitate proiect**</span><span class="sxs-lookup"><span data-stu-id="b8fd9-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="b8fd9-107">De la fluxul de proces oportunități de vânzări</span><span class="sxs-lookup"><span data-stu-id="b8fd9-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="b8fd9-108">Prin actualizarea referinței de oportunitate pe o ofertă existentă</span><span class="sxs-lookup"><span data-stu-id="b8fd9-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="b8fd9-109">De la fila Oferte de pe pagina Oportunitate proiect</span><span class="sxs-lookup"><span data-stu-id="b8fd9-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="b8fd9-110">Pentru a crea o ofertă de proiect dintr-o oportunitate, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="b8fd9-111">Deschideți pagina **Oportunitate proiect** și selectați fila **Oferte**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="b8fd9-112">Pe sub-grila **Oferte** , selectați **+** pentru a crea o nouă ofertă de proiect bazată pe oportunitate.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="b8fd9-113">Toate liniile de oportunități și listele de prețuri aferente proiectului sunt copiate în noua ofertă din oportunitate.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="b8fd9-114">De la fluxul de proces oportunități de vânzări</span><span class="sxs-lookup"><span data-stu-id="b8fd9-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="b8fd9-115">Pentru a crea o ofertă din fluxul de proces vânzări de oportunitate, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="b8fd9-116">Din fluxul procesului de vânzări de oportunitate, deschideți oportunitatea.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="b8fd9-117">Selectați etapa **Calificare**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="b8fd9-118">Selectați **Următorul** și apoi selectați **Creați** pentru a crea o nouă ofertă.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="b8fd9-119">Cele mai multe informații despre fila **Rezumat** pentru această ofertă nouă vor fi implicit din oportunitate.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="b8fd9-120">Introduceți toate informațiile necesare care lipsesc sau actualizați valorile implicite, după cum este necesar pe fila **Rezumat** ,</span><span class="sxs-lookup"><span data-stu-id="b8fd9-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="b8fd9-121">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-121">Select **Save**.</span></span> <span data-ttu-id="b8fd9-122">Noua ofertă este creată și asociată cu oportunitatea.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="b8fd9-123">Acum puteți vizualiza informațiile despre cotație în fila **Oferte** din pagina **Oportunitate**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="b8fd9-124">Procesul de vânzări de oportunitate trece la etapa următoare, **Propunere**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="b8fd9-125">Prin actualizarea referinței de oportunitate pe o ofertă existentă</span><span class="sxs-lookup"><span data-stu-id="b8fd9-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="b8fd9-126">O ofertă existentă poate fi legată de o oportunitate.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="b8fd9-127">Parcurgeți pașii următori pentru a actualiza informațiile despre oportunitate despre o ofertă existentă.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="b8fd9-128">Deschideți pagina **Ofertă** și selectați fila **Rezumat**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="b8fd9-129">În câmpul **Oportunitate** , selectați oportunitatea pe care doriți să o conectați la ofertă.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="b8fd9-130">Puteți vedea oferta în grila **Oferte** a oportunității.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="b8fd9-131">Folosind procesul de vânzare de oportunitate, oportunitatea poate fi mutată în etapa următoare, **Propunere**.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="b8fd9-132">Când mutați o oportunitate în această etapă, puteți selecta această ofertă dintr-o listă de oferte asociate acestei oportunități.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="b8fd9-133">Selectarea acestei oferte indică faptul că mergeți mai departe cu ea.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="b8fd9-134">Toate celelalte oferte asociate cu oportunitatea vor fi disponibile și active până când una dintre ele va fi câștigată.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="b8fd9-135">Puteți muta procesul de vânzare înapoi la etapa anterioară **Calificare** și alegeți o altă ofertă pentru a merge mai departe.</span><span class="sxs-lookup"><span data-stu-id="b8fd9-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
