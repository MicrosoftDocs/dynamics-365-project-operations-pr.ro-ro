---
title: Definirea calendarelor de proiect
description: Acest subiect oferă informații despre utilizarea unui calendar de proiect pentru a urmări planificarea proiectului.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082970"
---
# <a name="define-project-calendars"></a><span data-ttu-id="74649-103">Definirea calendarelor de proiect</span><span class="sxs-lookup"><span data-stu-id="74649-103">Define project calendars</span></span>

<span data-ttu-id="74649-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="74649-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74649-105">Pentru a crea o planificare de proiect, creați un șablon de calendar de proiect care definește numărul de ore de lucru pe zi și orice închideri de firmă.</span><span class="sxs-lookup"><span data-stu-id="74649-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="74649-106">Pentru a crea un șablon de calendar de proiect, asociați un șablon de lucru cu câmpul **Șablon de calendar** pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="74649-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="74649-107">Urmați acești pași pentru a crea un șablon de lucru.</span><span class="sxs-lookup"><span data-stu-id="74649-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="74649-108">În panoul de navigare din stânga, selectați **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="74649-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="74649-109">Pe pagina listei **Resurse** , deschideți o înregistrare de utilizator și apoi selectați **Afișați ore de lucru**.</span><span class="sxs-lookup"><span data-stu-id="74649-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="74649-110">Asigurați-vă că permiteți ferestrele pop-up pe pagina browserului.</span><span class="sxs-lookup"><span data-stu-id="74649-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="74649-111">Acest lucru vă permite să vedeți orele de lucru setate pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="74649-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="74649-112">Pe fila **Vizualizare lunară** , selectați **Configurați**.</span><span class="sxs-lookup"><span data-stu-id="74649-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="74649-113">Apare o listă cu trei opțiuni:</span><span class="sxs-lookup"><span data-stu-id="74649-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="74649-114">Planificare săptămânală nouă</span><span class="sxs-lookup"><span data-stu-id="74649-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="74649-115">Planificare lucru pentru o zi</span><span class="sxs-lookup"><span data-stu-id="74649-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="74649-116">Indisponibilitate</span><span class="sxs-lookup"><span data-stu-id="74649-116">Time Off</span></span>

4. <span data-ttu-id="74649-117">Selectați **Programul săptămânal nou** , apoi setați opțiunile pentru această planificare de resurse.</span><span class="sxs-lookup"><span data-stu-id="74649-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="74649-118">Puteți seta o planificare săptămânală recurentă, parametri de oră pe zi, închideri de afaceri și multe altele.</span><span class="sxs-lookup"><span data-stu-id="74649-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="74649-119">Setați intervalul de date, selectați **Salvare** , apoi selectați **Închidere**.</span><span class="sxs-lookup"><span data-stu-id="74649-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="74649-120">Reveniți la pagina listă **Resurse** și selectați resursa pentru care setați orele de lucru.</span><span class="sxs-lookup"><span data-stu-id="74649-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="74649-121">Selectați **Configurați calendarul ca** pentru a seta șablonul de lucru.</span><span class="sxs-lookup"><span data-stu-id="74649-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="74649-122">În caseta de dialog **Șablon de lucru** , introduceți un nume pentru șablonul de lucru și apoi selectați **Aplicați**.</span><span class="sxs-lookup"><span data-stu-id="74649-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="74649-123">Acum aveți posibilitatea să asociați șablonul de lucru cu un șablon de calendar de proiect.</span><span class="sxs-lookup"><span data-stu-id="74649-123">You can now associate the work template with a project calendar template.</span></span>
