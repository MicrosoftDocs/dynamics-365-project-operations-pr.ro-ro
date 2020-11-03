---
title: Eliminarea unei estimări de proiect
description: Acest subiect oferă informații despre eliminarea unei estimări de proiect după finalizarea acestuia.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082849"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="e9892-103">Eliminarea unei estimări de proiect</span><span class="sxs-lookup"><span data-stu-id="e9892-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9892-104">Estimările proiectului furnizează perspectiva financiară a lucrului estimat și planificat pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="e9892-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="e9892-105">Pentru a lucra cu estimări pentru un proiect, trebuie să atașați proiectul la un proiect de estimare.</span><span class="sxs-lookup"><span data-stu-id="e9892-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="e9892-106">Un proiect de estimare se bazează întotdeauna pe un proiect existent, cu toate acestea, mai multe proiecte se pot referi la un singur proiect de estimare.</span><span class="sxs-lookup"><span data-stu-id="e9892-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="e9892-107">Numai proiectele cu preț fix și investițiile pot fi atașate la proiectele estimate, iar proiectele respective trebuie să aparțină aceluiași grup de proiecte ca și proiectul estimativ.</span><span class="sxs-lookup"><span data-stu-id="e9892-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="e9892-108">Pentru a elimina un proiect de estimare, acesta trebuie să fie complet.</span><span class="sxs-lookup"><span data-stu-id="e9892-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="e9892-109">Următorii pași explică modul de eliminare a unei estimări.</span><span class="sxs-lookup"><span data-stu-id="e9892-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="e9892-110">Accesați **Gestionarea proiectului și contabilitate** > **Toate proiectele** și deschideți proiectul.</span><span class="sxs-lookup"><span data-stu-id="e9892-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="e9892-111">Pe fila **Administrați** , selectați **Estimări** , și pe pagina **Estimare** selectați **Eliminare**.</span><span class="sxs-lookup"><span data-stu-id="e9892-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="e9892-112">Pe pagina **Eliminați estimarea** pe fila **General** , setați următoarele opțiuni:</span><span class="sxs-lookup"><span data-stu-id="e9892-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="e9892-113">**Codul perioadei** : Selectați codul perioadei pentru a alege proiectele estimate corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="e9892-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="e9892-114">**Data estimării** : Selectați data estimativă adecvată pentru eliminare.</span><span class="sxs-lookup"><span data-stu-id="e9892-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="e9892-115">**Eliminați cu avertismente WIP** : Activați această opțiune pentru a furniza notificări atunci când va fi eliminată o estimare asociată cu o lucrare în curs (WIP).</span><span class="sxs-lookup"><span data-stu-id="e9892-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="e9892-116">Când această opțiune nu este activată, eliminarea nu poate continua dacă există tranzacții care nu sunt estimate.</span><span class="sxs-lookup"><span data-stu-id="e9892-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="e9892-117">Această opțiune este disponibilă numai atunci când eliminarea este aplicată unui proiect estimativ.</span><span class="sxs-lookup"><span data-stu-id="e9892-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="e9892-118">Nu este disponibil dacă utilizați postări periodice.</span><span class="sxs-lookup"><span data-stu-id="e9892-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="e9892-119">Această setare funcționează cu setările de pe fila **Estimare** de pe pagina **Parametrii proiectului** , în câmpul de grup **Permiteți eliminarea atunci când există tranzacții care nu sunt estimate**.</span><span class="sxs-lookup"><span data-stu-id="e9892-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="e9892-120">**Puneți seta la Finalizat** : Activați această opțiune pentru a seta etapa proiectului estimativ la **Terminat** după ce executați eliminarea.</span><span class="sxs-lookup"><span data-stu-id="e9892-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="e9892-121">**Imprimați lista estimărilor** : Selectați informațiile care urmează să fie incluse la imprimarea listei estimative.</span><span class="sxs-lookup"><span data-stu-id="e9892-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="e9892-122">**Afișați Infolog** : Activați această opțiune pentru a afișa Infolog.</span><span class="sxs-lookup"><span data-stu-id="e9892-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="e9892-123">**Data postării** : Alegeți data de înregistrare a registrului estimativ.</span><span class="sxs-lookup"><span data-stu-id="e9892-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="e9892-124">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9892-124">Select **OK**.</span></span>
5. <span data-ttu-id="e9892-125">După finalizarea procesului de eliminare, proiectul estimat eliminat este afișat cu o valoare negativă.</span><span class="sxs-lookup"><span data-stu-id="e9892-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="e9892-126">Dacă nu ați intenționat să eliminați o estimare, puteți selecta estimarea eliminată și selectați **Eliminare inversă**.</span><span class="sxs-lookup"><span data-stu-id="e9892-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
