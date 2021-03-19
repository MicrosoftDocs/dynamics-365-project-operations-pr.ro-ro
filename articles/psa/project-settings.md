---
title: Setări de proiect
description: Acest subiect furnizează informații despre setările de management de proiect.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c55d0f4c8f8db231a995d91a46a582bca2e1e6e3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283743"
---
# <a name="project-settings"></a><span data-ttu-id="6c740-103">Setări de proiect</span><span class="sxs-lookup"><span data-stu-id="6c740-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6c740-104">Utilizați următoarele setări pentru a accesa caracteristicile de planificare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="6c740-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="6c740-105">Șablon de lucru</span><span class="sxs-lookup"><span data-stu-id="6c740-105">Work template</span></span>

<span data-ttu-id="6c740-106">Pentru a crea o planificare de proiect, creați un șablon de calendar de proiect care definește numărul de ore de lucru pe zi și orice închideri de firmă.</span><span class="sxs-lookup"><span data-stu-id="6c740-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="6c740-107">Pentru a crea un șablon de calendar de proiect, asociați un șablon de lucru cu câmpul **Șablon de calendar** pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="6c740-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="6c740-108">Urmați acești pași pentru a crea un șablon de lucru.</span><span class="sxs-lookup"><span data-stu-id="6c740-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="6c740-109">În PSA, în panoul de navigare din stânga, faceți clic pe **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="6c740-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="6c740-110">Pe pagina listei **Resurse**, deschideți o înregistrare de utilizator și apoi selectați **Afișați ore de lucru**.</span><span class="sxs-lookup"><span data-stu-id="6c740-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="6c740-111">Asigurați-vă că permiteți ferestrele pop-up pe pagina browserului.</span><span class="sxs-lookup"><span data-stu-id="6c740-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="6c740-112">Acest lucru vă permite să vedeți orele de lucru setate pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="6c740-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="6c740-113">Pe fila **Vizualizare lunară**, faceți clic pe **Configurați**.</span><span class="sxs-lookup"><span data-stu-id="6c740-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="6c740-114">Apare o listă cu trei opțiuni:</span><span class="sxs-lookup"><span data-stu-id="6c740-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="6c740-115">Planificare săptămânală nouă</span><span class="sxs-lookup"><span data-stu-id="6c740-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="6c740-116">Planificare lucru pentru o zi</span><span class="sxs-lookup"><span data-stu-id="6c740-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="6c740-117">Întrerupere</span><span class="sxs-lookup"><span data-stu-id="6c740-117">Time Off</span></span>

> ![Configurați opțiuni](media/project-13.png)

4. <span data-ttu-id="6c740-119">Selectați **Programul săptămânal nou**, apoi setați opțiunile pentru această planificare de resurse.</span><span class="sxs-lookup"><span data-stu-id="6c740-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="6c740-120">Puteți seta o planificare săptămânală recurentă, parametri de oră pe zi, închideri de afaceri și multe altele.</span><span class="sxs-lookup"><span data-stu-id="6c740-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="6c740-121">Setați intervalul de date, selectați **Salvare**, apoi faceți clic pe **Închidere**.</span><span class="sxs-lookup"><span data-stu-id="6c740-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="6c740-122">Reveniți la pagina listă **Resurse** și selectați resursa pentru care setați orele de lucru.</span><span class="sxs-lookup"><span data-stu-id="6c740-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="6c740-123">Selectați **Configurați calendarul ca** pentru a seta șablonul de lucru.</span><span class="sxs-lookup"><span data-stu-id="6c740-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="6c740-124">În caseta de dialog **Șablon de lucru**, introduceți un nume pentru șablonul de lucru și apoi selectați **Aplicați**.</span><span class="sxs-lookup"><span data-stu-id="6c740-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="6c740-125">Acum aveți posibilitatea să asociați șablonul de lucru cu un șablon de calendar de proiect.</span><span class="sxs-lookup"><span data-stu-id="6c740-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="6c740-126">Roluri de resursă</span><span class="sxs-lookup"><span data-stu-id="6c740-126">Resource roles</span></span>

<span data-ttu-id="6c740-127">Termenul *rol de resursă* se referă la setul de aptitudini, competențe și certificări pe care o persoană trebuie să le aibă pentru a efectua un anumit set de activități într-un proiect.</span><span class="sxs-lookup"><span data-stu-id="6c740-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="6c740-128">PSA vă permite să stabiliți costul și să facturați timpul unei resurse pe baza rolului cu care este asociată o resursă.</span><span class="sxs-lookup"><span data-stu-id="6c740-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="6c740-129">Fiecare organizație trebuie să configureze aceste roluri utilizând navigarea din partea stângă a meniului **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="6c740-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="6c740-130">Fiecare organizație trebuie să configureze aceste roluri pe pagina **Categorii resursă activă**.</span><span class="sxs-lookup"><span data-stu-id="6c740-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="6c740-131">Pentru a deschide această pagină, în panoul de navigare din stânga, selectați **Roluri resursă**.</span><span class="sxs-lookup"><span data-stu-id="6c740-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="6c740-132">Liste de prețuri</span><span class="sxs-lookup"><span data-stu-id="6c740-132">Price lists</span></span>

<span data-ttu-id="6c740-133">Listele de prețuri vă permit să configurați costurile și prețurile de vânzări pentru rolurile de resurse, categoriile de cheltuieli, produse și alte elemente dintr-o organizație.</span><span class="sxs-lookup"><span data-stu-id="6c740-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="6c740-134">Înainte să configurați estimări financiare pentru lucrul care trebuie livrat pentru un proiect, ar trebui să creați un cost de rezervă și o listă de prețuri de vânzări.</span><span class="sxs-lookup"><span data-stu-id="6c740-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="6c740-135">În secțiunea parametri, ar trebui să configurați, de asemenea, un cost implicit și lista de prețuri de vânzări care se aplică tuturor proiectelor care sunt create în organizație.</span><span class="sxs-lookup"><span data-stu-id="6c740-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="6c740-136">Pe pagina **Parametri proiect activi**, asigurați-vă că configurați un cost implicit și o listă de prețuri de vânzări.</span><span class="sxs-lookup"><span data-stu-id="6c740-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]