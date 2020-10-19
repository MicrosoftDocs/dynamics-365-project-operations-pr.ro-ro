---
title: Tip de implementare
description: Acest subiect oferă informații pentru a vă ajuta să determinați tipul corect de implementare a operațiunilor de proiect pentru compania dvs.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949028"
---
# <a name="deployment-types"></a><span data-ttu-id="11619-103">Tip de implementare</span><span class="sxs-lookup"><span data-stu-id="11619-103">Deployment types</span></span>

<span data-ttu-id="11619-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="11619-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11619-105">După ce ați achiziționat licența, începeți aici pentru a determina cel mai bun model de implementare a operațiunilor de proiect Dynamics 365 Project Operations folosind [Flux de instalare ghidat](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="11619-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="11619-106">După ce ați terminat fluxul de instalare ghidat, veți fi direcționat către portalul de management corect pentru a finaliza instalarea.</span><span class="sxs-lookup"><span data-stu-id="11619-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="11619-107">Consultați detaliile de implementare de mai jos pentru a finaliza instalarea.</span><span class="sxs-lookup"><span data-stu-id="11619-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="11619-108">Clienții existenți ai Dynamics utilizând Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11619-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="11619-109">Project Operations include capabilitățile livrate împreună cu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11619-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="11619-110">O cale de actualizare va fi lansată pentru acești clienți în viitor.</span><span class="sxs-lookup"><span data-stu-id="11619-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="11619-111">Clienții existenți ai Dynamics 365 Finance care utilizează managementul proiectului și contabilitatea</span><span class="sxs-lookup"><span data-stu-id="11619-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="11619-112">Clienții existenți ai Finanțelor care utilizează funcționalitatea de gestionare a proiectelor și contabilitate pot utiliza în continuare acest lucru așa cum este.</span><span class="sxs-lookup"><span data-stu-id="11619-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="11619-113">Consultați [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma).</span><span class="sxs-lookup"><span data-stu-id="11619-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="11619-114">Project Operations acceptă mai multe opțiuni de implementare pentru a se potrivi cerințelor dvs.</span><span class="sxs-lookup"><span data-stu-id="11619-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="11619-115">Indiferent dacă sunteți un client Dynamics 365 nou sau existent, Project Operations vă poate sprijini nevoile.</span><span class="sxs-lookup"><span data-stu-id="11619-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="11619-116">[Chestionarul de implementare](https://aka.ms/provisionprojectoperations) de la noi vă va ajuta să determinați implementarea corectă.</span><span class="sxs-lookup"><span data-stu-id="11619-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="11619-117">Rezultatele vă vor ghida către unul dintre următoarele tipuri de implementare:</span><span class="sxs-lookup"><span data-stu-id="11619-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="11619-118">Implementare simplificată - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="11619-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="11619-119">Project Operations pentru resurse/scenarii fără stoc</span><span class="sxs-lookup"><span data-stu-id="11619-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="11619-120">Project Operations pentru scenarii cu stocuri/comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="11619-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="11619-121">Project Operations acceptă scenarii de stocare/comandă de producție și scenarii ne-stocate/bazate pe resurse în același mediu prin configurații la nivel de entitate juridică.</span><span class="sxs-lookup"><span data-stu-id="11619-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="11619-122">De exemplu, Contoso poate valorifica capacitățile de stocare/comandă de producție din unitatea de producție din SUA (entitate juridică = Contoso Manufacturing United States) și capacitățile ne-stocate/bazate pe resurse în unitatea de service Contoso Robotics Arms din Regatul Unit (entitate juridică = Contoso Robotics Regatul Unit).</span><span class="sxs-lookup"><span data-stu-id="11619-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="11619-123"><a name="lite"><a/>Implementare simplificată - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="11619-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="11619-124">Implementarea simplă include următoarele funcții:</span><span class="sxs-lookup"><span data-stu-id="11619-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="11619-125">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="11619-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="11619-126">Prețuri multidimensionale</span><span class="sxs-lookup"><span data-stu-id="11619-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="11619-127">Gestionare unificată a resurselor</span><span class="sxs-lookup"><span data-stu-id="11619-127">Unified Resource Management</span></span>
- <span data-ttu-id="11619-128">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="11619-128">Time Tracking</span></span>
- <span data-ttu-id="11619-129">Cheltuieli de bază</span><span class="sxs-lookup"><span data-stu-id="11619-129">Basic Expense</span></span>
- <span data-ttu-id="11619-130">Propunere de factură</span><span class="sxs-lookup"><span data-stu-id="11619-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="11619-131">Pași de implementare:</span><span class="sxs-lookup"><span data-stu-id="11619-131">Deployment steps:</span></span>
<span data-ttu-id="11619-132">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="11619-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="11619-133">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](lite-preview-subscription-sign-up.md) și [Furnizarea accesului la un mediu nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="11619-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="11619-134"><a name="integrated"><a/>Project Operations pentru resurse/scenarii fără stoc</span><span class="sxs-lookup"><span data-stu-id="11619-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="11619-135">Project Operations pentru resurse/scenarii ne-stocate includ următoarele capacități:</span><span class="sxs-lookup"><span data-stu-id="11619-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="11619-136">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="11619-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="11619-137">Prețuri multidimensionale</span><span class="sxs-lookup"><span data-stu-id="11619-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="11619-138">Gestionare unificată a resurselor</span><span class="sxs-lookup"><span data-stu-id="11619-138">Unified Resource Management</span></span>
- <span data-ttu-id="11619-139">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="11619-139">Time Tracking</span></span>
- <span data-ttu-id="11619-140">Cheltuieli de bază</span><span class="sxs-lookup"><span data-stu-id="11619-140">Basic Expense</span></span>
- <span data-ttu-id="11619-141">Cheltuieli complete</span><span class="sxs-lookup"><span data-stu-id="11619-141">Full Expense</span></span>
- <span data-ttu-id="11619-142">Chitanță OCR</span><span class="sxs-lookup"><span data-stu-id="11619-142">Receipt OCR</span></span>
- <span data-ttu-id="11619-143">Facturare completă</span><span class="sxs-lookup"><span data-stu-id="11619-143">Full Invoicing</span></span>
- <span data-ttu-id="11619-144">Recunoașterea veniturilor</span><span class="sxs-lookup"><span data-stu-id="11619-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="11619-145">Pași de implementare:</span><span class="sxs-lookup"><span data-stu-id="11619-145">Deployment steps:</span></span>
<span data-ttu-id="11619-146">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="11619-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="11619-147">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](resource-sign-up-preview-subscription.md) și [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="11619-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="11619-148">Project Operations pentru scenarii cu stocuri/comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="11619-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="11619-149">Planificarea proiectelor utilizând WBS</span><span class="sxs-lookup"><span data-stu-id="11619-149">Project planning using WBS</span></span>
- <span data-ttu-id="11619-150">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="11619-150">Resource Management</span></span>
- <span data-ttu-id="11619-151">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="11619-151">Time Tracking</span></span>
- <span data-ttu-id="11619-152">Cheltuieli complete</span><span class="sxs-lookup"><span data-stu-id="11619-152">Full Expense</span></span>
- <span data-ttu-id="11619-153">Chitanță OCR</span><span class="sxs-lookup"><span data-stu-id="11619-153">Receipt OCR</span></span>
- <span data-ttu-id="11619-154">Facturare completă</span><span class="sxs-lookup"><span data-stu-id="11619-154">Full Invoicing</span></span>
- <span data-ttu-id="11619-155">Recunoașterea veniturilor</span><span class="sxs-lookup"><span data-stu-id="11619-155">Revenue Recognition</span></span>
- <span data-ttu-id="11619-156">Comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="11619-156">Production Orders</span></span>
- <span data-ttu-id="11619-157">Materiale de asistență</span><span class="sxs-lookup"><span data-stu-id="11619-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="11619-158">Pași de implementare:</span><span class="sxs-lookup"><span data-stu-id="11619-158">Deployment steps:</span></span>
<span data-ttu-id="11619-159">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="11619-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="11619-160">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) și [Furnizarea accesului la un mediu nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="11619-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



