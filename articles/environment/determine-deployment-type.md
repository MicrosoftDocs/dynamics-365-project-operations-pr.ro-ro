---
title: Determinarea tipului de implementare
description: Acest subiect oferă informații pentru a vă ajuta să determinați tipul corect de implementare a operațiunilor de proiect pentru compania dvs.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401233"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="f2621-103">Determinarea tipului de implementare</span><span class="sxs-lookup"><span data-stu-id="f2621-103">Determine your deployment type</span></span>

<span data-ttu-id="f2621-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="f2621-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f2621-105">După ce ați achiziționat licența, începeți aici pentru a determina cel mai bun model de implementare a operațiunilor de proiect Dynamics 365 Project Operations folosind [Flux de instalare ghidat](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f2621-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="f2621-106">După ce ați terminat fluxul de instalare ghidat, veți fi direcționat către portalul de management corect pentru a finaliza instalarea.</span><span class="sxs-lookup"><span data-stu-id="f2621-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="f2621-107">Consultați detaliile de implementare pentru a finaliza instalarea.</span><span class="sxs-lookup"><span data-stu-id="f2621-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="f2621-108">Clienții existenți ai Dynamics utilizând Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f2621-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="f2621-109">Project Operations include capabilitățile livrate împreună cu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f2621-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="f2621-110">O cale de actualizare va fi lansată pentru acești clienți în versiunea 1 de lansare 2021.</span><span class="sxs-lookup"><span data-stu-id="f2621-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="f2621-111">Clienții existenți ai Dynamics 365 Finance care utilizează managementul proiectului și contabilitatea</span><span class="sxs-lookup"><span data-stu-id="f2621-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="f2621-112">Clienții existenți ai Finanțelor care utilizează funcționalitatea de gestionare a proiectelor și contabilitate pot continua să o utilizeze așa cum este.</span><span class="sxs-lookup"><span data-stu-id="f2621-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="f2621-113">Consultați [Project Operations pentru scenarii cu stocuri/comenzi de producție](#pma).</span><span class="sxs-lookup"><span data-stu-id="f2621-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="f2621-114">Tip de implementare</span><span class="sxs-lookup"><span data-stu-id="f2621-114">Deployment types</span></span>
<span data-ttu-id="f2621-115">Project Operations acceptă mai multe opțiuni de implementare pentru a se potrivi cerințelor dvs.</span><span class="sxs-lookup"><span data-stu-id="f2621-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="f2621-116">Indiferent dacă sunteți un client Dynamics 365 nou sau existent, Project Operations vă poate sprijini nevoile.</span><span class="sxs-lookup"><span data-stu-id="f2621-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="f2621-117">[Chestionarul de implementare](https://aka.ms/provisionprojectoperations) de la noi vă va ajuta să determinați implementarea corectă.</span><span class="sxs-lookup"><span data-stu-id="f2621-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="f2621-118">Rezultatele vă vor ghida către unul dintre următoarele tipuri de implementare:</span><span class="sxs-lookup"><span data-stu-id="f2621-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="f2621-119">Implementare simplificată - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="f2621-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="f2621-120">Project Operations pentru resurse/scenarii fără stoc</span><span class="sxs-lookup"><span data-stu-id="f2621-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="f2621-121">Project Operations pentru scenarii cu stocuri/comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="f2621-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="f2621-122">Project Operations acceptă scenarii de stocare/comandă de producție și scenarii ne-stocate/bazate pe resurse în același mediu prin configurații la nivel de entitate juridică.</span><span class="sxs-lookup"><span data-stu-id="f2621-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="f2621-123">De exemplu, Contoso poate utiliza capacitățile de stocare/comandă de producție în unitatea lor de producție din SUA (entitate juridică = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="f2621-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="f2621-124">Contoso poate utiliza capabilitățile non-stocate/bazate pe resurse în unitatea lor de service Contoso Robotics Arms din Regatul Unit (entitate juridică = Contoso Robotics Regatul Unit).</span><span class="sxs-lookup"><span data-stu-id="f2621-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="f2621-125">Implementare simplificată - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="f2621-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="f2621-126">Implementarea simplă include următoarele funcții:</span><span class="sxs-lookup"><span data-stu-id="f2621-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="f2621-127">Proces de vânzări pentru proiecte care extinde experiențele aplicației Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f2621-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="f2621-128">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="f2621-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f2621-129">Prețuri multidimensionale</span><span class="sxs-lookup"><span data-stu-id="f2621-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f2621-130">Gestionare unificată a resurselor</span><span class="sxs-lookup"><span data-stu-id="f2621-130">Unified resource management</span></span>
- <span data-ttu-id="f2621-131">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="f2621-131">Time tracking</span></span>
- <span data-ttu-id="f2621-132">Cheltuieli de bază</span><span class="sxs-lookup"><span data-stu-id="f2621-132">Basic expense</span></span>
- <span data-ttu-id="f2621-133">Facturare Proforma și orientată către clienți</span><span class="sxs-lookup"><span data-stu-id="f2621-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="f2621-134">Pași de implementare</span><span class="sxs-lookup"><span data-stu-id="f2621-134">Deployment steps</span></span>
<span data-ttu-id="f2621-135">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f2621-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f2621-136">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](lite-preview-subscription-sign-up.md) și [Furnizarea accesului la un mediu nou](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="f2621-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="f2621-137">Project Operations pentru resurse/scenarii fără stoc</span><span class="sxs-lookup"><span data-stu-id="f2621-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="f2621-138">Project Operations pentru resurse/scenarii ne-stocate includ următoarele capacități:</span><span class="sxs-lookup"><span data-stu-id="f2621-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="f2621-139">Proces de vânzări pentru proiecte care extinde aplicația Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f2621-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="f2621-140">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="f2621-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f2621-141">Prețuri multidimensionale</span><span class="sxs-lookup"><span data-stu-id="f2621-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f2621-142">Gestionare unificată a resurselor</span><span class="sxs-lookup"><span data-stu-id="f2621-142">Unified resource management</span></span>
- <span data-ttu-id="f2621-143">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="f2621-143">Time tracking</span></span>
- <span data-ttu-id="f2621-144">Cheltuieli de bază</span><span class="sxs-lookup"><span data-stu-id="f2621-144">Basic expense</span></span>
- <span data-ttu-id="f2621-145">Cheltuieli complete</span><span class="sxs-lookup"><span data-stu-id="f2621-145">Full expense</span></span>
- <span data-ttu-id="f2621-146">Chitanță OCR</span><span class="sxs-lookup"><span data-stu-id="f2621-146">Receipt OCR</span></span>
- <span data-ttu-id="f2621-147">Facturare Proforma și orientată către clienți</span><span class="sxs-lookup"><span data-stu-id="f2621-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="f2621-148">Recunoașterea veniturilor pentru proiecte</span><span class="sxs-lookup"><span data-stu-id="f2621-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f2621-149">Pași de implementare</span><span class="sxs-lookup"><span data-stu-id="f2621-149">Deployment steps</span></span>
<span data-ttu-id="f2621-150">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f2621-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f2621-151">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](resource-sign-up-preview-subscription.md) și [Furnizarea accesului la un mediu nou](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f2621-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="f2621-152">Project Operations pentru scenarii cu stocuri/comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="f2621-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="f2621-153">Planificarea proiectelor utilizând WBS</span><span class="sxs-lookup"><span data-stu-id="f2621-153">Project planning using WBS</span></span>
- <span data-ttu-id="f2621-154">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="f2621-154">Resource Management</span></span>
- <span data-ttu-id="f2621-155">Urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="f2621-155">Time Tracking</span></span>
- <span data-ttu-id="f2621-156">Cheltuieli complete</span><span class="sxs-lookup"><span data-stu-id="f2621-156">Full Expense</span></span>
- <span data-ttu-id="f2621-157">Chitanță OCR</span><span class="sxs-lookup"><span data-stu-id="f2621-157">Receipt OCR</span></span>
- <span data-ttu-id="f2621-158">Facturare completă</span><span class="sxs-lookup"><span data-stu-id="f2621-158">Full Invoicing</span></span>
- <span data-ttu-id="f2621-159">Recunoașterea veniturilor</span><span class="sxs-lookup"><span data-stu-id="f2621-159">Revenue Recognition</span></span>
- <span data-ttu-id="f2621-160">Comenzi de producție</span><span class="sxs-lookup"><span data-stu-id="f2621-160">Production Orders</span></span>
- <span data-ttu-id="f2621-161">Materiale de asistență</span><span class="sxs-lookup"><span data-stu-id="f2621-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f2621-162">Pași de implementare</span><span class="sxs-lookup"><span data-stu-id="f2621-162">Deployment steps</span></span>
<span data-ttu-id="f2621-163">Determinați cel mai bun model de implementare a Project Operations utilizând [Chestionar de implementare](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f2621-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f2621-164">Pentru această desfășurare, consultați [Înscrieți-vă pentru abonamente de previzualizare](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) și [Furnizarea accesului la un mediu nou](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f2621-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

