---
title: Configurarea resurselor proiectului
description: Acest subiect furnizează informații despre configurarea sau solicitarea resurselor de proiect.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082968"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="9aaa4-103">Configurarea resurselor proiectului</span><span class="sxs-lookup"><span data-stu-id="9aaa4-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9aaa4-104">Trebuie să configurați un calendar și să îl asociați cu un angajat sau cu un lucrător.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="9aaa4-105">Calendarul este folosit pentru a planifica proiectul și timpul de lucru al resurselor rezervate pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="9aaa4-106">În timpul configurării calendarului, managerii de proiect pot realiza nivelarea resurselor ca parte a optimizării resurselor.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="9aaa4-107">Pe baza planificării calendaristice, pot fi impuse restricții asupra resurselor.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="9aaa4-108">Puteți configura un calendar din pagina **Calendare**.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="9aaa4-109">Când configurați un angajat ca resursă a proiectului, puteți selecta dintre angajații care lucrează în compania pentru care configurați resursele.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="9aaa4-110">Alternativ, puteți selecta angajați din alte companii din organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="9aaa4-111">Acești angajați sunt cunoscuți ca resurse între companii.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="9aaa4-112">Următoarele proceduri explică cum să configurați un angajat ca o resursă de proiect în compania dvs. și cum să configurați o resursă de proiect între companii.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="9aaa4-113">Configurați un angajat ca resursă a proiectului</span><span class="sxs-lookup"><span data-stu-id="9aaa4-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="9aaa4-114">Din pagina **Angajați** , în lista **Angajați** , selectați angajatul pe care îl adăugați ca resursă a proiectului și deschideți înregistrarea angajatului.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="9aaa4-115">În panoul de acțiuni, selectați **Proiect** &gt; **Configurare** &gt; **Configurarea proiectului**.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="9aaa4-116">Selectați un calendar, apoi închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="9aaa4-117">De asemenea, puteți specifica proiecte implicite pentru o resursă ca un tip de pre-atribuire.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="9aaa4-118">Pre-atribuirile pot fi utilizate atunci când managerul de resurse sau managerul de proiect știe în avans la ce proiecte va lucra resursa.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="9aaa4-119">Pre-atribuirile se pot baza și pe cererea unui sponsor de proiect sau a unui client.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="9aaa4-120">Pentru a pre-atribui un proiect, din pagina **Atribuire proiecte** , în fila **Proiecte** , în lista **Proiecte rămase** , selectați proiectul corespunzător.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="9aaa4-121">Configurați o resursă între companii</span><span class="sxs-lookup"><span data-stu-id="9aaa4-121">Set up an intercompany resource</span></span>

<span data-ttu-id="9aaa4-122">Când configurați un angajat ca resursă între companii, trebuie să finalizați configurarea atât în compania sursă, cât și în cea țintă.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="9aaa4-123">În compania sursă</span><span class="sxs-lookup"><span data-stu-id="9aaa4-123">In the lending company</span></span>

1. <span data-ttu-id="9aaa4-124">În Finanțe, verificați dacă este selectată compania sursă, apoi finalizați procedura din secțiunea anterioară „Configurați un angajat ca resursă a proiectului”.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="9aaa4-125">În pagina **Contabilitate între companii** , selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="9aaa4-126">În câmpul **ID-ul entității juridice** , selectați compania sursă.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="9aaa4-127">Completați corespunzător câmpurile rămase, și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="9aaa4-128">În pagina **Preț de transfer** , selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="9aaa4-129">În câmpul **Entitate juridică țintă** , selectați compania adecvată.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="9aaa4-130">Pentru a împrumuta companiei țintă numai resursa pe care ați creat-o la începutul acestei secțiuni, în câmpul **Resursă** , selectați numele resursei pe care ați creat-o.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="9aaa4-131">Pentru a pune la dispoziția companiei țintă toate resursele din compania sursă, lăsați câmpul **Resursă** necompletat.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="9aaa4-132">Din pagina **Managementul proiectului și parametri contabili** , în fila **Între companii** , setați opțiunea **Activați planificarea resurselor și foilor de pontaj între companii** la **Da**.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="9aaa4-133">În compania țintă</span><span class="sxs-lookup"><span data-stu-id="9aaa4-133">In the borrowing company</span></span>

- <span data-ttu-id="9aaa4-134">Din pagina **Lista resurselor** , în filtrul de căutare, introduceți numele resursei pe care ați creat-o pentru compania sursă, pentru a verifica dacă numele este inclus în lista de resurse pentru compania țintă.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="9aaa4-135">Solicitați resurse de proiect</span><span class="sxs-lookup"><span data-stu-id="9aaa4-135">Request project resources</span></span>
<span data-ttu-id="9aaa4-136">Funcționalitatea pentru planificarea resurselor proiectului permite doar managerilor de resurse să distribuie resursele de personal pe implicări sau proiecte.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="9aaa4-137">Pentru a activa această funcționalitate, finalizați următoarele activități sau verificați dacă acestea au fost finalizate:</span><span class="sxs-lookup"><span data-stu-id="9aaa4-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="9aaa4-138">Configurare secvențe numerice.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-138">Set up number sequences.</span></span>
- <span data-ttu-id="9aaa4-139">Configurare fluxuri de lucru de management de proiect și contabilitate.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="9aaa4-140">Activare fluxuri de lucru de solicitare a resurselor.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-140">Enable resource request workflows.</span></span>

<span data-ttu-id="9aaa4-141">După finalizarea sarcinilor precedente, puteți finaliza următoarele sarcini după necesități:</span><span class="sxs-lookup"><span data-stu-id="9aaa4-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="9aaa4-142">Crearea unei solicitări de resursă dintr-o resursă de personal cu rezervare provizorie.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="9aaa4-143">Monitorizarea solicitărilor de resurse.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-143">Monitor resource requests.</span></span>
- <span data-ttu-id="9aaa4-144">Completarea solicitărilor de resurse.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="9aaa4-145">Solicitarea unei resurse de personal de la o WBS.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="9aaa4-146">Rezervarea de resurse la un proiect fără a avea o solicitare pentru o resursă de personal.</span><span class="sxs-lookup"><span data-stu-id="9aaa4-146">Book resources to a project without having a request for a staffed resource.</span></span>
