---
title: Actualizarea atributelor inserturilor cu noile dimensiuni de preț
description: Acest subiect furnizează informații despre cum să actualizați atributele inserturilor pentru dimensiunile de tarifare.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643233"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="c4884-103">Actualizați atributele inserturilor cu noile dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="c4884-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="c4884-104">Acest subiect furnizează informații despre cum să actualizați atributele inserturilor pentru dimensiunile de tarifare.</span><span class="sxs-lookup"><span data-stu-id="c4884-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="c4884-105">Acest subiect se aplică numai caracteristicilor de ofertă și contract în Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c4884-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c4884-106">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="c4884-106">Prerequisites</span></span>
<span data-ttu-id="c4884-107">Înainte de a finaliza pașii din acest subiect, trebuie să fi finalizat procedurile din următoarele subiecte:</span><span class="sxs-lookup"><span data-stu-id="c4884-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="c4884-108">Crearea câmpurilor și entităților particularizate</span><span class="sxs-lookup"><span data-stu-id="c4884-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="c4884-109">Adăugarea câmpurilor particularizate la configurarea prețurilor și la entitățile tranzacționale </span><span class="sxs-lookup"><span data-stu-id="c4884-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="c4884-110">[Configurarea câmpurilor particularizate ca dimensiuni de preț](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="c4884-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="c4884-111">Dacă nu ați finalizat aceste proceduri, completați-le și apoi reveniți la acest subiect.</span><span class="sxs-lookup"><span data-stu-id="c4884-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="c4884-112">Înregistrați un insert</span><span class="sxs-lookup"><span data-stu-id="c4884-112">Register a plug-in</span></span>
<span data-ttu-id="c4884-113">Când se creează un detaliu de linie de ofertă pe pagina **Linie de ofertă** pentru o linie de ofertă de proiect, sistemul creează două linii de estimare.</span><span class="sxs-lookup"><span data-stu-id="c4884-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="c4884-114">O linie este pentru partea de cost a estimării, iar cealaltă linie este pentru partea de vânzări.</span><span class="sxs-lookup"><span data-stu-id="c4884-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="c4884-115">Acest lucru este la fel pentru liniile de contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="c4884-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="c4884-116">Când efectuați o modificare a cantității sau a unui câmp pe partea de cost, acea modificare este propagată și pe partea de vânzare.</span><span class="sxs-lookup"><span data-stu-id="c4884-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="c4884-117">Acest lucru este posibil deoarece pluginurile PreOperation de pe entitățile de detalii Quotelinedetail și contractline conectează atribute specifice din partea costurilor cu partea de vânzări a tranzacției.</span><span class="sxs-lookup"><span data-stu-id="c4884-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="c4884-118">Dacă aveți nevoie de modificări ale valorilor dimensiunii prețurilor din partea vânzărilor, care trebuie făcute și din partea costurilor, următoarele inserturi trebuie să fie reînregistrate după efectuarea modificărilor la dimensiunea prețurilor.</span><span class="sxs-lookup"><span data-stu-id="c4884-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="c4884-119">Acestea sunt inserturile pentru actualizare și reînregistrare:</span><span class="sxs-lookup"><span data-stu-id="c4884-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="c4884-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="c4884-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="c4884-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="c4884-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="c4884-122">Parcurgeți pașii următori pentru a actualiza și a înregistra din nou inserturile.</span><span class="sxs-lookup"><span data-stu-id="c4884-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="c4884-123">Deschideți **PluginRegistrationTool** și conectați-vă la mediul dvs. Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c4884-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="c4884-124">Selectați **Căutare** și tastați primele litere ale insertului care urmează să fie actualizat.</span><span class="sxs-lookup"><span data-stu-id="c4884-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="c4884-125">După ce se găsește insertul, selectați-l și apoi selectați **Selectați pe formularul principal**.</span><span class="sxs-lookup"><span data-stu-id="c4884-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="c4884-126">Selectați pasul **Actualizați msdyn_orderlinetransaction**, faceți clic dreapta și apoi selectați **Actualizați**.</span><span class="sxs-lookup"><span data-stu-id="c4884-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="c4884-127">În caseta de dialog **Actualizare** selectați elipsa (**...**) în atributele de filtrare.</span><span class="sxs-lookup"><span data-stu-id="c4884-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="c4884-128">Fereastra de atribute de filtrare se deschide și oferă o listă cu toate atributele din entitate și dimensiunile de stabilire a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="c4884-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="c4884-129">Bifați casetele de selectare pentru atributele dimensiunii de preț.</span><span class="sxs-lookup"><span data-stu-id="c4884-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="c4884-130">Selectați **OK** pentru a închide pagina, apoi selectați **Actualizare pas**.</span><span class="sxs-lookup"><span data-stu-id="c4884-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="c4884-131">Repetați pașii 2-7 pentru al doilea insert, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="c4884-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="c4884-132">Pentru acest insert, trebuie să actualizați pasul **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="c4884-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="c4884-133">Închideți **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="c4884-133">Close **PluginRegistrationTool**.</span></span>
