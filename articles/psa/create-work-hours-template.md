---
title: Crearea unui șablon de ore de lucru
description: Acest subiect descrie cum să creați un șablon de ore de lucru în Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981270"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="52e18-103">Creați un șablon de ore de lucru (Project Service)</span><span class="sxs-lookup"><span data-stu-id="52e18-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52e18-104">Pentru a crea și gestiona un proiect, trebuie să aplicați un șablon de calendar de proiect.</span><span class="sxs-lookup"><span data-stu-id="52e18-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="52e18-105">Șablonul de calendar definește următoarele atribute de proiect:</span><span class="sxs-lookup"><span data-stu-id="52e18-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="52e18-106">Programul de lucru, inclusiv ora de început și sfârșit</span><span class="sxs-lookup"><span data-stu-id="52e18-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="52e18-107">Zile de lucru</span><span class="sxs-lookup"><span data-stu-id="52e18-107">Working days</span></span>
- <span data-ttu-id="52e18-108">Excepții din calendar, cum ar fi zilele nelucrătoare</span><span class="sxs-lookup"><span data-stu-id="52e18-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="52e18-109">Șablonul de calendar aplicat unui proiect este o copie a șablonului calendarului definit în setările organizației dvs.</span><span class="sxs-lookup"><span data-stu-id="52e18-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="52e18-110">Dacă modificați șablonul de calendar, aceste modificări nu se propagă la planificarea de lucru a proiectului.</span><span class="sxs-lookup"><span data-stu-id="52e18-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="52e18-111">Pentru a schimba planificarea de lucru a proiectului, trebuie aplicat un nou șablon.</span><span class="sxs-lookup"><span data-stu-id="52e18-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="52e18-112">Pentru a crea un șablon de calendar pentru organizația dvs., există două cerințe principale:</span><span class="sxs-lookup"><span data-stu-id="52e18-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="52e18-113">Definiți orele de lucru dorite ale șablonului utilizând o resursă rezervabilă nouă sau existentă.</span><span class="sxs-lookup"><span data-stu-id="52e18-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="52e18-114">Creați un nou șablon de calendar și asociați șablonul cu resursa rezervabilă.</span><span class="sxs-lookup"><span data-stu-id="52e18-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="52e18-115">**Definiți orele de lucru ale șablonului**</span><span class="sxs-lookup"><span data-stu-id="52e18-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="52e18-116">Accesați **Resurse** \> **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="52e18-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="52e18-117">Creați o nouă resursă pentru a face referință în șablonul calendarului sau selectați o resursă existentă.</span><span class="sxs-lookup"><span data-stu-id="52e18-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="52e18-118">Selectați fila **Ore de lucru** a resursei și completați instrucțiunile din [Setarea orelor de lucru pentru o resursă](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) pentru a configura regulile calendarului.</span><span class="sxs-lookup"><span data-stu-id="52e18-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="52e18-119">**Creați un șablon nou de calendar**</span><span class="sxs-lookup"><span data-stu-id="52e18-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="52e18-120">Accesați **Setări** \> **Șabloane de calendar**.</span><span class="sxs-lookup"><span data-stu-id="52e18-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="52e18-121">Selectați **Nou** și introduceți un nume, o descriere și o resursă șablon.</span><span class="sxs-lookup"><span data-stu-id="52e18-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="52e18-122">Când se face referire la o resursă într-un șablon de calendar, o copie a calendarului resursei este asociată cu șablonul de calendar.</span><span class="sxs-lookup"><span data-stu-id="52e18-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="52e18-123">Dacă modificați orele de lucru ale șablonului copiat, aceste modificări nu se propagă în șablonul de calendar.</span><span class="sxs-lookup"><span data-stu-id="52e18-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="52e18-124">Consultați și</span><span class="sxs-lookup"><span data-stu-id="52e18-124">See Also</span></span>  
 [<span data-ttu-id="52e18-125">Configurarea resurselor</span><span class="sxs-lookup"><span data-stu-id="52e18-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
