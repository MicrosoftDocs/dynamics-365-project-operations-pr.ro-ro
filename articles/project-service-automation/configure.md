---
title: Configurați Project Service Automation
description: Pași pentru configurarea Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754729"
---
# <a name="configure-project-service"></a><span data-ttu-id="def0f-103">Configurarea Project Service</span><span class="sxs-lookup"><span data-stu-id="def0f-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="def0f-104">Înainte de a putea utiliza capacitățile de automatizare [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] în [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pentru a vă gestiona conturile, proiectele și resursele, trebuie să finalizați câțiva pași de configurare pentru a vă asigura vă soluția de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] corespunde necesităților organizației.</span><span class="sxs-lookup"><span data-stu-id="def0f-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="def0f-105">Acești pași includ:</span><span class="sxs-lookup"><span data-stu-id="def0f-105">These steps include:</span></span>  
  
-   <span data-ttu-id="def0f-106">[Configurați unitățile de timp](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="def0f-107">Configurați unități de timp în catalogul de produse pe care îl veți utiliza ca bază pentru programarea si facturarea proiectelor.</span><span class="sxs-lookup"><span data-stu-id="def0f-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="def0f-108">[Configurați valutele și cursul valutar](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="def0f-109">Configurați monedele pe care le veți utiliza pentru proiectele dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="def0f-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="def0f-110">[Creați unități organizaționale](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="def0f-111">Setați grupurile pe care le utilizează compania dumneavoastră pentru a-și împărți afacerile, după geografie, după funcția de afaceri sau după altă diviziune logică.</span><span class="sxs-lookup"><span data-stu-id="def0f-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="def0f-112">[Configurați frecvențele de facturare](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="def0f-113">Setați perioadele pe care doriți să le utilizați pentru facturarea clienților.</span><span class="sxs-lookup"><span data-stu-id="def0f-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="def0f-114">[Configurați categoriile de tranzacții](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="def0f-115">Configurați categorii de tranzacții la care să își poată modifica cheltuielile cu sau fără factură consultanții.</span><span class="sxs-lookup"><span data-stu-id="def0f-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="def0f-116">[Configurați categoriile de cheltuieli](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="def0f-117">Configurați categoriile la care să își poată modifica cheltuielile cu sau fără factură consultanții.</span><span class="sxs-lookup"><span data-stu-id="def0f-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="def0f-118">[Creați elemente din catalogul de produse](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="def0f-119">Adăugați produsele pe care le vindeți, cum ar fi licențele de software, la catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="def0f-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="def0f-120">[Crearea unei liste de prețuri](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="def0f-121">Configurați liste de prețuri diferite, în funcție de cât de mult doriți să vă taxați clienții pentru fiecare rol de care are nevoie proiectul lor.</span><span class="sxs-lookup"><span data-stu-id="def0f-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="def0f-122">[Configurați resursele](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="def0f-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="def0f-123">Adăugați abilități, competențe, roluri de resurse și alte informații despre resurse de care veți avea nevoie pentru proiectele dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="def0f-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="def0f-124">Consultați și</span><span class="sxs-lookup"><span data-stu-id="def0f-124">See Also</span></span>  
 <span data-ttu-id="def0f-125">[Prezentare generală a Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="def0f-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="def0f-126">[Configurați Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="def0f-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="def0f-127">[Ghidul Managerului de cont](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="def0f-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="def0f-128">[Ghidul Managerului de proiect](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="def0f-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="def0f-129">[Ghidul Managerului de resurse](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="def0f-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="def0f-130">Timp, cheltuieli și ghid de colaborare</span><span class="sxs-lookup"><span data-stu-id="def0f-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
