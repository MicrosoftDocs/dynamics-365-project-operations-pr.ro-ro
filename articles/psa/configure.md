---
title: Configurați Project Service Automation
description: Pași pentru configurarea Project Service
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
ms.openlocfilehash: ec5381f91b1fe5198bd93ac8d6015b1fea38738d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146948"
---
# <a name="configure-project-service"></a><span data-ttu-id="d247f-103">Configurarea Project Service</span><span class="sxs-lookup"><span data-stu-id="d247f-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d247f-104">Înainte de a putea utiliza capacitățile de automatizare [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] în [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pentru a vă gestiona conturile, proiectele și resursele, trebuie să finalizați câțiva pași de configurare pentru a vă asigura vă soluția de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] corespunde necesităților organizației.</span><span class="sxs-lookup"><span data-stu-id="d247f-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="d247f-105">Acești pași includ:</span><span class="sxs-lookup"><span data-stu-id="d247f-105">These steps include:</span></span>  
  
-   <span data-ttu-id="d247f-106">[Configurați unitățile de timp](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="d247f-107">Configurați unități de timp în catalogul de produse pe care îl veți utiliza ca bază pentru programarea si facturarea proiectelor.</span><span class="sxs-lookup"><span data-stu-id="d247f-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="d247f-108">[Configurați valutele și cursul valutar](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="d247f-109">Configurați monedele pe care le veți utiliza pentru proiectele dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="d247f-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="d247f-110">[Creați unități organizaționale](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="d247f-111">Setați grupurile pe care le utilizează compania dumneavoastră pentru a-și împărți afacerile, după geografie, după funcția de afaceri sau după altă diviziune logică.</span><span class="sxs-lookup"><span data-stu-id="d247f-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="d247f-112">[Configurați frecvențele de facturare](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="d247f-113">Setați perioadele pe care doriți să le utilizați pentru facturarea clienților.</span><span class="sxs-lookup"><span data-stu-id="d247f-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="d247f-114">[Configurați categoriile de tranzacții](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="d247f-115">Configurați categorii de tranzacții la care să își poată modifica cheltuielile cu sau fără factură consultanții.</span><span class="sxs-lookup"><span data-stu-id="d247f-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="d247f-116">[Configurați categoriile de cheltuieli](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="d247f-117">Configurați categoriile la care să își poată modifica cheltuielile cu sau fără factură consultanții.</span><span class="sxs-lookup"><span data-stu-id="d247f-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="d247f-118">[Creați elemente din catalogul de produse](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="d247f-119">Adăugați produsele pe care le vindeți, cum ar fi licențele de software, la catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="d247f-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="d247f-120">[Crearea unei liste de prețuri](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="d247f-121">Configurați liste de prețuri diferite, în funcție de cât de mult doriți să vă taxați clienții pentru fiecare rol de care are nevoie proiectul lor.</span><span class="sxs-lookup"><span data-stu-id="d247f-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="d247f-122">[Configurați resursele](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d247f-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="d247f-123">Adăugați abilități, competențe, roluri de resurse și alte informații despre resurse de care veți avea nevoie pentru proiectele dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="d247f-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d247f-124">Consultați și</span><span class="sxs-lookup"><span data-stu-id="d247f-124">See Also</span></span>  
 <span data-ttu-id="d247f-125">[Prezentare generală a Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="d247f-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="d247f-126">[Configurați Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="d247f-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="d247f-127">[Ghidul Managerului de cont](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d247f-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="d247f-128">[Ghidul Managerului de proiect](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d247f-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="d247f-129">[Ghidul Managerului de resurse](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d247f-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="d247f-130">Timp, cheltuieli și ghid de colaborare</span><span class="sxs-lookup"><span data-stu-id="d247f-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
