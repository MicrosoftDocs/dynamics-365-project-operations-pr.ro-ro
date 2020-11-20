---
title: Prezentare generală a asistentului de planificare
description: Acest subiect furnizează informații despre lucrul cu asistentul de planificare pentru a rezerva resurse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125643"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="a9827-103">Prezentare generală a asistentului de planificare</span><span class="sxs-lookup"><span data-stu-id="a9827-103">Schedule assistant overview</span></span>

<span data-ttu-id="a9827-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="a9827-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a9827-105">Asistentul de planificare este utilizat pentru a rezerva resurse pe baza cerințelor definite de managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="a9827-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="a9827-106">Asistentul de planificare se bazează pe parametrii furnizați în cerința resursei pentru a găsi resursa.</span><span class="sxs-lookup"><span data-stu-id="a9827-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="a9827-107">Asistentul de planificare recomandă resurse care corespund cerințelor relevante, cum ar fi ferestrele de timp sau abilitățile necesare.</span><span class="sxs-lookup"><span data-stu-id="a9827-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="a9827-108">După identificarea resurselor adecvate, resursa sau managerul de proiect poate rezerva resursa la lucrare.</span><span class="sxs-lookup"><span data-stu-id="a9827-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a9827-109">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="a9827-109">Prerequisites</span></span>

<span data-ttu-id="a9827-110">Asistentul de planificare face parte din soluția Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="a9827-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="a9827-111">Această soluție este inclusă și instalată cu Dynamics 365 Project Operations, Dynamics 365 Field Service și Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="a9827-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="a9827-112">Cerințe și resurse potrivite</span><span class="sxs-lookup"><span data-stu-id="a9827-112">Matching requirements and resources</span></span>

<span data-ttu-id="a9827-113">O cerință de resursă generată se bazează pe detalii precum:</span><span class="sxs-lookup"><span data-stu-id="a9827-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="a9827-114">Caracteristici</span><span class="sxs-lookup"><span data-stu-id="a9827-114">Characteristics</span></span>
-   <span data-ttu-id="a9827-115">Roluri</span><span class="sxs-lookup"><span data-stu-id="a9827-115">Roles</span></span>
-   <span data-ttu-id="a9827-116">Unități de business</span><span class="sxs-lookup"><span data-stu-id="a9827-116">Business units</span></span>
-   <span data-ttu-id="a9827-117">Preferințe resurse</span><span class="sxs-lookup"><span data-stu-id="a9827-117">Resource preferences</span></span>
-   <span data-ttu-id="a9827-118">Contururi de efort</span><span class="sxs-lookup"><span data-stu-id="a9827-118">Effort contours</span></span>
-   <span data-ttu-id="a9827-119">Fus orar</span><span class="sxs-lookup"><span data-stu-id="a9827-119">Time zone</span></span>

<span data-ttu-id="a9827-120">Asistentul de planificare utilizează aceste detalii pentru a filtra resursele.</span><span class="sxs-lookup"><span data-stu-id="a9827-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="a9827-121">Lansați Asistentul de planificare</span><span class="sxs-lookup"><span data-stu-id="a9827-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="a9827-122">Există două moduri în care este lansat asistentul de programare.</span><span class="sxs-lookup"><span data-stu-id="a9827-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="a9827-123">Dacă utilizați modul hibrid, în grila membrilor echipei puteți selecta orice membru al echipei cu o cerință de resurse neîndeplinită, apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="a9827-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="a9827-124">Dacă utilizați modul central, managerul de resurse găsește și selectează resursa.</span><span class="sxs-lookup"><span data-stu-id="a9827-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="a9827-125">Filtre asistent de planificare</span><span class="sxs-lookup"><span data-stu-id="a9827-125">Schedule assistant filters</span></span>

<span data-ttu-id="a9827-126">După executarea asistentului de planificare, detaliile din cerința de resurse sunt afișate ca valori filtrate în panoul din stânga.</span><span class="sxs-lookup"><span data-stu-id="a9827-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="a9827-127">Managerul de resurse sau managerul de proiect pot ajusta rezultatele ajustând filtrele pentru a satisface nevoile de planificare.</span><span class="sxs-lookup"><span data-stu-id="a9827-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="a9827-128">Panoul de filtrare prezintă opțiuni legate de muncă, inclusiv:</span><span class="sxs-lookup"><span data-stu-id="a9827-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="a9827-129">Începutul și sfârșitul lucrului</span><span class="sxs-lookup"><span data-stu-id="a9827-129">Work start and end</span></span>
-   <span data-ttu-id="a9827-130">Caracteristici</span><span class="sxs-lookup"><span data-stu-id="a9827-130">Characteristics</span></span>
-   <span data-ttu-id="a9827-131">Roluri</span><span class="sxs-lookup"><span data-stu-id="a9827-131">Roles</span></span>
-   <span data-ttu-id="a9827-132">Unități organizaționale</span><span class="sxs-lookup"><span data-stu-id="a9827-132">Organizational units</span></span>
-   <span data-ttu-id="a9827-133">Firmă de resurse</span><span class="sxs-lookup"><span data-stu-id="a9827-133">Resourcing company</span></span>
-   <span data-ttu-id="a9827-134">Tipuri de resursă</span><span class="sxs-lookup"><span data-stu-id="a9827-134">Resource types</span></span>
-   <span data-ttu-id="a9827-135">Resurse preferate</span><span class="sxs-lookup"><span data-stu-id="a9827-135">Preferred resources</span></span>
