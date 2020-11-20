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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129198"
---
# <a name="configure-project-service"></a><span data-ttu-id="6296a-103">Configurarea Project Service</span><span class="sxs-lookup"><span data-stu-id="6296a-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6296a-104">Înainte de a putea utiliza capacitățile de automatizare [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] în [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pentru a vă gestiona conturile, proiectele și resursele, trebuie să finalizați câțiva pași de configurare pentru a vă asigura vă soluția de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] corespunde necesităților organizației.</span><span class="sxs-lookup"><span data-stu-id="6296a-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="6296a-105">Acești pași includ:</span><span class="sxs-lookup"><span data-stu-id="6296a-105">These steps include:</span></span>  
  
-   <span data-ttu-id="6296a-106">[Configurați unitățile de timp](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="6296a-107">Configurați unități de timp în catalogul de produse pe care îl veți utiliza ca bază pentru programarea si facturarea proiectelor.</span><span class="sxs-lookup"><span data-stu-id="6296a-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="6296a-108">[Configurați valutele și cursul valutar](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="6296a-109">Configurați monedele pe care le veți utiliza pentru proiectele dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="6296a-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="6296a-110">[Creați unități organizaționale](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="6296a-111">Setați grupurile pe care le utilizează compania dumneavoastră pentru a-și împărți afacerile, după geografie, după funcția de afaceri sau după altă diviziune logică.</span><span class="sxs-lookup"><span data-stu-id="6296a-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="6296a-112">[Configurați frecvențele de facturare](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="6296a-113">Setați perioadele pe care doriți să le utilizați pentru facturarea clienților.</span><span class="sxs-lookup"><span data-stu-id="6296a-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="6296a-114">[Configurați categoriile de tranzacții](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="6296a-115">Configurați categorii de tranzacții la care să își poată modifica cheltuielile cu sau fără factură consultanții.</span><span class="sxs-lookup"><span data-stu-id="6296a-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="6296a-116">[Configurați categoriile de cheltuieli](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="6296a-117">Configurați categoriile la care să își poată modifica cheltuielile cu sau fără factură consultanții.</span><span class="sxs-lookup"><span data-stu-id="6296a-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="6296a-118">[Creați elemente din catalogul de produse](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="6296a-119">Adăugați produsele pe care le vindeți, cum ar fi licențele de software, la catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="6296a-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="6296a-120">[Crearea unei liste de prețuri](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="6296a-121">Configurați liste de prețuri diferite, în funcție de cât de mult doriți să vă taxați clienții pentru fiecare rol de care are nevoie proiectul lor.</span><span class="sxs-lookup"><span data-stu-id="6296a-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="6296a-122">[Configurați resursele](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="6296a-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="6296a-123">Adăugați abilități, competențe, roluri de resurse și alte informații despre resurse de care veți avea nevoie pentru proiectele dumneavoastră.</span><span class="sxs-lookup"><span data-stu-id="6296a-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6296a-124">Consultați și</span><span class="sxs-lookup"><span data-stu-id="6296a-124">See Also</span></span>  
 <span data-ttu-id="6296a-125">[Prezentare generală a Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="6296a-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="6296a-126">[Configurați Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="6296a-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="6296a-127">[Ghidul Managerului de cont](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6296a-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="6296a-128">[Ghidul Managerului de proiect](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6296a-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="6296a-129">[Ghidul Managerului de resurse](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6296a-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="6296a-130">Timp, cheltuieli și ghid de colaborare</span><span class="sxs-lookup"><span data-stu-id="6296a-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
