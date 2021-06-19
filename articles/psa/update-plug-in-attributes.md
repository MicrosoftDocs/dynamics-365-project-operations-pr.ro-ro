---
title: Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare
description: Acest subiect furnizează informații despre actualizarea atributelor inserturilor pentru dimensiunile de tarifare.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
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
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012826"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="231b2-103">Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare</span><span class="sxs-lookup"><span data-stu-id="231b2-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="231b2-104">Dacă nu utilizați funcțiile de ofertare și contractare Project Service Automation (PSA), puteți sări peste acest subiect.</span><span class="sxs-lookup"><span data-stu-id="231b2-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="231b2-105">Acest subiect presupune că ați finalizat procedurile din subiectele [Crearea de câmpuri și entități particularizate](create-custom-fields-entities.md), [Adăugarea de câmpuri particularizate la parametrizare preț și entități tranzacționale](field-references.md) și [Configurare câmpuri particularizate ca dimensiuni de tarifare](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="231b2-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="231b2-106">Dacă nu ați finalizat aceste proceduri, reveniți și completați-le și apoi reveniți la acest subiect.</span><span class="sxs-lookup"><span data-stu-id="231b2-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="231b2-107">Când se creează un detaliu al liniei de ofertă în pagina **linie ofertă** pentru o linie de ofertă de proiect, sistemul creează două linii de estimare în fundal -- o linie pentru partea de cost a estimării și una pentru partea de vânzări.</span><span class="sxs-lookup"><span data-stu-id="231b2-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="231b2-108">Acest lucru este la fel pentru liniile de contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="231b2-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="231b2-109">Când efectuați o modificare a cantității sau a unui câmp pa partea de cost, acea modificare este propagată pe partea de vânzare.</span><span class="sxs-lookup"><span data-stu-id="231b2-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="231b2-110">Asta este posibil din cauza următoarele inserturi care trebuie să fie re-înregistrate după o modificare a dimensiunilor de tarifare.</span><span class="sxs-lookup"><span data-stu-id="231b2-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="231b2-111">PreOperationContractLineDetailUpdate - Actualizări **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="231b2-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="231b2-112">PreOperationQuoteLineDetailUpdate - Actualizări **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="231b2-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="231b2-113">Următorii pași vă explică procesul de înregistrare a inserturilor.</span><span class="sxs-lookup"><span data-stu-id="231b2-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="231b2-114">Deschideți **PluginRegistrationTool** și conectați-vă la instanța dvs. online.</span><span class="sxs-lookup"><span data-stu-id="231b2-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="231b2-115">Faceți clic pe **Căutare** și căutați insertul de actualizat.</span><span class="sxs-lookup"><span data-stu-id="231b2-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Captură de ecran a arborelui de căutare](media/PRT-1.png)

3. <span data-ttu-id="231b2-117">După ce se găsește insertul, selectați-l și apoi faceți clic pe **Selectați în formularul principal**.</span><span class="sxs-lookup"><span data-stu-id="231b2-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="231b2-118">Selectați pasul insertului de actualizat, faceți clic dreapta, iar apoi selectați **Actualizare**.</span><span class="sxs-lookup"><span data-stu-id="231b2-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Captură de ecran cu insertul de actualizat](media/PRT-2.png)
 
5. <span data-ttu-id="231b2-120">În fereastra de actualizare, faceți clic pe puncte de suspensie (**...**) în atributele de filtrare.</span><span class="sxs-lookup"><span data-stu-id="231b2-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Captură de ecran a informațiilor de configurare Actualizare pas existent](media/PRT-3.png)
 
6. <span data-ttu-id="231b2-122">Selectați casetele de validare a atributului de tarifare.</span><span class="sxs-lookup"><span data-stu-id="231b2-122">Select the pricing attribute check boxes.</span></span>

 ![Captură de ecran care arată selectarea casetei de validare pentru atributele de tarifare](media/PRT-4.png)

7. <span data-ttu-id="231b2-124">Faceți clic pe **OK** pentru a închide pagina, apoi selectați **Actualizare pas**.</span><span class="sxs-lookup"><span data-stu-id="231b2-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Captură de ecran cu butonul „Actualizare pas"](media/PRT-5.png)
 
8. <span data-ttu-id="231b2-126">Repetați acest proces pentru al doilea insert, **PreOperationQuoteLineDetail - Actualizare msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="231b2-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="231b2-127">Închideți instrumentul de înregistrare inserturi.</span><span class="sxs-lookup"><span data-stu-id="231b2-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]