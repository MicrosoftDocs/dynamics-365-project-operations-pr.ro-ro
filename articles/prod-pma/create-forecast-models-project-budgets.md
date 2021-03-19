---
title: Crearea unor modele de prognoză pentru bugetele proiectului
description: Acest subiect descrie cum să creați un model de prognoză pentru bugetele rămase.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271053"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="a71de-103">Crearea unor modele de prognoză pentru bugetele proiectului</span><span class="sxs-lookup"><span data-stu-id="a71de-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a71de-104">Acest subiect descrie cum să creați un model de prognoză pentru bugetele rămase.</span><span class="sxs-lookup"><span data-stu-id="a71de-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="a71de-105">Un proiect care este supus controlului bugetar utilizează două tipuri de bugete: original și rămas.</span><span class="sxs-lookup"><span data-stu-id="a71de-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="a71de-106">Când creați un buget de proiect, trebuie să specificați modelele de prognoză de buget inițiale și rămase care au fost create în pagina **Modele de prognoză**.</span><span class="sxs-lookup"><span data-stu-id="a71de-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="a71de-107">Bugetele proiectului pe baza modelelor specificate sunt create atunci când vă angajați la bugetul proiectului.</span><span class="sxs-lookup"><span data-stu-id="a71de-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="a71de-108">Un model de prognoză care este utilizat pentru controlul bugetului nu poate avea un submodel sau nu poate fi folosit ca submodel.</span><span class="sxs-lookup"><span data-stu-id="a71de-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="a71de-109">Selectați **Management de proiect și contabilitate** > **Configurare** > **Prognoze**  > **Modele de prognoză**.</span><span class="sxs-lookup"><span data-stu-id="a71de-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="a71de-110">Selectați **Nou** pentru a crea un nou model de prognoză, apoi introduceți un număr de ID de model și un nume pentru noul model.</span><span class="sxs-lookup"><span data-stu-id="a71de-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="a71de-111">Setați opțiunea **Oprit** pentru **Da** pentru a preveni orice modificare a liniilor de prognoză pentru modelul de prognoză.</span><span class="sxs-lookup"><span data-stu-id="a71de-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="a71de-112">Dacă liniile de prognoză cu care este asociat modelul ar trebui să genereze previziuni ale fluxului de numerar în registrul general, setați **Includeți în previziunile fluxurilor de numerar** la **Da.**</span><span class="sxs-lookup"><span data-stu-id="a71de-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="a71de-113">Pentru a utiliza data proiectului ca dată a facturii, setați **Data facturii cu prognoză** la **Da**.</span><span class="sxs-lookup"><span data-stu-id="a71de-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="a71de-114">În **Tipul bugetului**, selectați unul dintre următoarele tipuri de modele:</span><span class="sxs-lookup"><span data-stu-id="a71de-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="a71de-115">**Bugetul original**: Utilizați sumele inițiale ale bugetului care sunt angajate atunci când bugetul inițial este creat și aprobat.</span><span class="sxs-lookup"><span data-stu-id="a71de-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="a71de-116">**Buget rămas**: Utilizați sumele bugetare rămase pe durata proiectului.</span><span class="sxs-lookup"><span data-stu-id="a71de-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="a71de-117">Soldurile din acest model de prognoză sunt reduse prin tranzacții reale și crescute sau diminuate prin revizuiri bugetare.</span><span class="sxs-lookup"><span data-stu-id="a71de-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="a71de-118">**Reportare**: Utilizați sumele din bugetul de reportare pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="a71de-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="a71de-119">Reportarea este un proces opțional care poate fi rulat pentru a transfera sumele neutilizate ale bugetului de la un exercițiu financiar la altul.</span><span class="sxs-lookup"><span data-stu-id="a71de-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="a71de-120">Setați următoarele opțiuni, după cum este necesar:</span><span class="sxs-lookup"><span data-stu-id="a71de-120">Set the following options as required:</span></span>

   - <span data-ttu-id="a71de-121">Activați **Data facturii cu prognoză** pentru a utiliza data proiectului ca dată a facturii.</span><span class="sxs-lookup"><span data-stu-id="a71de-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="a71de-122">Activați **Prognoza cu WIP** pentru a prognoza pe baza lucrărilor în curs (WIP), apoi selectați tipul de WIP.</span><span class="sxs-lookup"><span data-stu-id="a71de-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="a71de-123">Puteți păstra valoarea implicită **Tipul bugetului** ca **Niciuna** sau introduceți un tip nou.</span><span class="sxs-lookup"><span data-stu-id="a71de-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="a71de-124">Tipul de buget nu poate fi modificat după ce schimbați o înregistrare.</span><span class="sxs-lookup"><span data-stu-id="a71de-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="a71de-125">Dacă modificați tipul de buget implicit, toate celelalte opțiuni nu vor fi disponibile pentru actualizări și nu puteți reutiliza acest model de prognoză.</span><span class="sxs-lookup"><span data-stu-id="a71de-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]