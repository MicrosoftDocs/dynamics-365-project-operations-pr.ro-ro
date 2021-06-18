---
title: Definirea calendarelor de proiect
description: Acest subiect oferă informații despre cum se aplică un șablon de calendar unui proiect pentru a urmări planificarea proiectului.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999011"
---
# <a name="define-project-calendars"></a><span data-ttu-id="1d941-103">Definirea calendarelor de proiect</span><span class="sxs-lookup"><span data-stu-id="1d941-103">Define project calendars</span></span>

<span data-ttu-id="1d941-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="1d941-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d941-105">Pentru a crea și gestiona un proiect, trebuie să aplicați un șablon de calendar de proiect.</span><span class="sxs-lookup"><span data-stu-id="1d941-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="1d941-106">Șablonul de calendar definește următoarele atribute de proiect:</span><span class="sxs-lookup"><span data-stu-id="1d941-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="1d941-107">Programul de lucru, inclusiv ora de început și sfârșit</span><span class="sxs-lookup"><span data-stu-id="1d941-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="1d941-108">Zile de lucru</span><span class="sxs-lookup"><span data-stu-id="1d941-108">Working days</span></span>
- <span data-ttu-id="1d941-109">Excepții din calendar, cum ar fi zilele nelucrătoare</span><span class="sxs-lookup"><span data-stu-id="1d941-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="1d941-110">Șablonul de calendar aplicat unui proiect este o copie a șablonului calendarului definit în setările organizației dvs.</span><span class="sxs-lookup"><span data-stu-id="1d941-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="1d941-111">Dacă modificați șablonul de calendar, aceste modificări nu se propagă la planificarea de lucru a proiectului.</span><span class="sxs-lookup"><span data-stu-id="1d941-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="1d941-112">Pentru a schimba planificarea de lucru a proiectului, trebuie aplicat un nou șablon.</span><span class="sxs-lookup"><span data-stu-id="1d941-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="1d941-113">Pentru a crea un șablon de calendar pentru organizația dvs., există două cerințe principale:</span><span class="sxs-lookup"><span data-stu-id="1d941-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="1d941-114">Definiți orele de lucru dorite ale șablonului utilizând o resursă rezervabilă nouă sau existentă.</span><span class="sxs-lookup"><span data-stu-id="1d941-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="1d941-115">Creați un nou șablon de calendar și asociați șablonul cu resursa rezervabilă.</span><span class="sxs-lookup"><span data-stu-id="1d941-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="1d941-116">**Definiți orele de lucru ale șablonului**</span><span class="sxs-lookup"><span data-stu-id="1d941-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="1d941-117">Accesați **Resurse** \> **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="1d941-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="1d941-118">Creați o nouă resursă pentru a face referință în șablonul calendarului sau selectați o resursă existentă.</span><span class="sxs-lookup"><span data-stu-id="1d941-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="1d941-119">Selectați fila **Ore de lucru** a resursei și completați instrucțiunile din [Setarea orelor de lucru pentru o resursă](/dynamics365/field-service/set-work-hours-resource.md) pentru a configura regulile calendarului.</span><span class="sxs-lookup"><span data-stu-id="1d941-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="1d941-120">**Creați un șablon nou de calendar**</span><span class="sxs-lookup"><span data-stu-id="1d941-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="1d941-121">Accesați **Setări** \> **Șabloane de calendar**.</span><span class="sxs-lookup"><span data-stu-id="1d941-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="1d941-122">Selectați **Nou** și introduceți un nume, o descriere și o resursă șablon.</span><span class="sxs-lookup"><span data-stu-id="1d941-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="1d941-123">Când se face referire la o resursă într-un șablon de calendar, o copie a calendarului resursei este asociată cu șablonul de calendar.</span><span class="sxs-lookup"><span data-stu-id="1d941-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="1d941-124">Dacă modificați orele de lucru ale șablonului copiat, aceste modificări nu se propagă în șablonul de calendar.</span><span class="sxs-lookup"><span data-stu-id="1d941-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="1d941-125">Acum aveți posibilitatea să asociați șablonul de lucru cu un șablon de calendar de proiect.</span><span class="sxs-lookup"><span data-stu-id="1d941-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

