---
title: Determinarea tipului de implementare
description: Acest subiect oferă informații pentru a vă ajuta să determinați tipul corect de implementare a operațiunilor de proiect pentru compania dvs.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082800"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="cd1c2-103">Determinarea tipului de implementare</span><span class="sxs-lookup"><span data-stu-id="cd1c2-103">Determine your deployment type</span></span>

<span data-ttu-id="cd1c2-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="cd1c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd1c2-105">După ce ați achiziționat licența, începeți aici pentru a determina cel mai bun model de implementare a operațiunilor de proiect Dynamics 365 Project Operations folosind [Flux de instalare ghidat](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="cd1c2-106">După ce ați terminat fluxul de instalare ghidat, veți fi direcționat către portalul de management corect pentru a finaliza instalarea.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="cd1c2-107">Consultați detaliile de implementare pentru a finaliza instalarea.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="cd1c2-108">Clienții existenți ai Dynamics utilizând Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cd1c2-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="cd1c2-109">Project Operations include capabilitățile livrate împreună cu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="cd1c2-110">O cale de actualizare va fi lansată pentru acești clienți în viitor.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="cd1c2-111">Clienții existenți ai Dynamics 365 Finance care utilizează managementul proiectului și contabilitatea</span><span class="sxs-lookup"><span data-stu-id="cd1c2-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="cd1c2-112">Clienții existenți ai Finanțelor care utilizează funcționalitatea de gestionare a proiectelor și contabilitate pot utiliza în continuare acest lucru așa cum este.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="cd1c2-113">Consultați [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="cd1c2-114">Tip de implementare</span><span class="sxs-lookup"><span data-stu-id="cd1c2-114">Deployment types</span></span>
<span data-ttu-id="cd1c2-115">Project Operations acceptă mai multe opțiuni de implementare pentru a se potrivi cerințelor dvs.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="cd1c2-116">Indiferent dacă sunteți un client Dynamics 365 nou sau existent, Project Operations vă poate sprijini nevoile.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="cd1c2-117">[Chestionarul de implementare](https://aka.ms/provisionprojectoperations) de la noi vă va ajuta să determinați implementarea corectă.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="cd1c2-118">Rezultatele vă vor ghida către unul dintre următoarele tipuri de implementare:</span><span class="sxs-lookup"><span data-stu-id="cd1c2-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="cd1c2-119">Implementare simplificată - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="cd1c2-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="cd1c2-120">Project Operations pentru resurse/scenarii fără stoc</span><span class="sxs-lookup"><span data-stu-id="cd1c2-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="cd1c2-121">Project Operations pentru scenarii cu stocuri/comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="cd1c2-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="cd1c2-122">Project Operations acceptă scenarii de stocare/comandă de producție și scenarii ne-stocate/bazate pe resurse în același mediu prin configurații la nivel de entitate juridică.</span><span class="sxs-lookup"><span data-stu-id="cd1c2-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="cd1c2-123">De exemplu, Contoso poate utiliza capacitățile de stocare/comandă de producție în unitatea lor de producție din SUA (entitate juridică = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="cd1c2-124">Contoso poate utiliza capabilitățile non-stocate/bazate pe resurse în unitatea lor de service Contoso Robotics Arms din Regatul Unit (entitate juridică = Contoso Robotics Regatul Unit).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="cd1c2-125">Implementare simplificată - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="cd1c2-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="cd1c2-126">Implementarea simplă include următoarele funcții:</span><span class="sxs-lookup"><span data-stu-id="cd1c2-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="cd1c2-127">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="cd1c2-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="cd1c2-128">Prețuri multidimensionale</span><span class="sxs-lookup"><span data-stu-id="cd1c2-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="cd1c2-129">Gestionare unificată a resurselor</span><span class="sxs-lookup"><span data-stu-id="cd1c2-129">Unified Resource Management</span></span>
- <span data-ttu-id="cd1c2-130">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="cd1c2-130">Time Tracking</span></span>
- <span data-ttu-id="cd1c2-131">Cheltuieli de bază</span><span class="sxs-lookup"><span data-stu-id="cd1c2-131">Basic Expense</span></span>
- <span data-ttu-id="cd1c2-132">Propunere de factură</span><span class="sxs-lookup"><span data-stu-id="cd1c2-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="cd1c2-133">Pași de implementare</span><span class="sxs-lookup"><span data-stu-id="cd1c2-133">Deployment steps</span></span>
<span data-ttu-id="cd1c2-134">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="cd1c2-135">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](lite-preview-subscription-sign-up.md) și [Furnizarea accesului la un mediu nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="cd1c2-136">Project Operations pentru resurse/scenarii fără stoc</span><span class="sxs-lookup"><span data-stu-id="cd1c2-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="cd1c2-137">Project Operations pentru resurse/scenarii ne-stocate includ următoarele capacități:</span><span class="sxs-lookup"><span data-stu-id="cd1c2-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="cd1c2-138">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="cd1c2-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="cd1c2-139">Prețuri multidimensionale</span><span class="sxs-lookup"><span data-stu-id="cd1c2-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="cd1c2-140">Gestionare unificată a resurselor</span><span class="sxs-lookup"><span data-stu-id="cd1c2-140">Unified Resource Management</span></span>
- <span data-ttu-id="cd1c2-141">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="cd1c2-141">Time Tracking</span></span>
- <span data-ttu-id="cd1c2-142">Cheltuieli de bază</span><span class="sxs-lookup"><span data-stu-id="cd1c2-142">Basic Expense</span></span>
- <span data-ttu-id="cd1c2-143">Cheltuieli complete</span><span class="sxs-lookup"><span data-stu-id="cd1c2-143">Full Expense</span></span>
- <span data-ttu-id="cd1c2-144">Chitanță OCR</span><span class="sxs-lookup"><span data-stu-id="cd1c2-144">Receipt OCR</span></span>
- <span data-ttu-id="cd1c2-145">Facturare completă</span><span class="sxs-lookup"><span data-stu-id="cd1c2-145">Full Invoicing</span></span>
- <span data-ttu-id="cd1c2-146">Recunoașterea veniturilor</span><span class="sxs-lookup"><span data-stu-id="cd1c2-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="cd1c2-147">Pași de implementare</span><span class="sxs-lookup"><span data-stu-id="cd1c2-147">Deployment steps</span></span>
<span data-ttu-id="cd1c2-148">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="cd1c2-149">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](resource-sign-up-preview-subscription.md) și [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="cd1c2-150">Project Operations pentru scenarii cu stocuri/comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="cd1c2-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="cd1c2-151">Planificarea proiectelor utilizând WBS</span><span class="sxs-lookup"><span data-stu-id="cd1c2-151">Project planning using WBS</span></span>
- <span data-ttu-id="cd1c2-152">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="cd1c2-152">Resource Management</span></span>
- <span data-ttu-id="cd1c2-153">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="cd1c2-153">Time Tracking</span></span>
- <span data-ttu-id="cd1c2-154">Cheltuieli complete</span><span class="sxs-lookup"><span data-stu-id="cd1c2-154">Full Expense</span></span>
- <span data-ttu-id="cd1c2-155">Chitanță OCR</span><span class="sxs-lookup"><span data-stu-id="cd1c2-155">Receipt OCR</span></span>
- <span data-ttu-id="cd1c2-156">Facturare completă</span><span class="sxs-lookup"><span data-stu-id="cd1c2-156">Full Invoicing</span></span>
- <span data-ttu-id="cd1c2-157">Recunoașterea veniturilor</span><span class="sxs-lookup"><span data-stu-id="cd1c2-157">Revenue Recognition</span></span>
- <span data-ttu-id="cd1c2-158">Comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="cd1c2-158">Production Orders</span></span>
- <span data-ttu-id="cd1c2-159">Materiale de asistență</span><span class="sxs-lookup"><span data-stu-id="cd1c2-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="cd1c2-160">Pași de implementare</span><span class="sxs-lookup"><span data-stu-id="cd1c2-160">Deployment steps</span></span>
<span data-ttu-id="cd1c2-161">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="cd1c2-162">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) și [Furnizarea accesului la un mediu nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="cd1c2-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

