---
title: Prezentare generală Project Service Automation
description: Acest subiect oferă informații despre Dynamics 365 Project Service Automation la soluția de integrare Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754768"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="8cdff-103">Prezentare generală Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8cdff-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8cdff-104">Soluția de integrare Project Service Automation to Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțe de Dynamics 365 Finance și Dynamics 365 Project Service Automation prin intermediul Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8cdff-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="8cdff-105">Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de proiecte, contracte de proiect, linii de contracte de proiect, repere de linii de contracte de proiect, sarcini de proiect, categorii de tranzacții de cheltuieli, estimări de oră și estimări de cheltuieli de la Project Service Automation până la finanțe.</span><span class="sxs-lookup"><span data-stu-id="8cdff-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8cdff-106">Dacă utilizați versiunea 7.3.0, trebuie să instalați KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="8cdff-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8cdff-107">Veți putea apoi să integrați proiecte cu preț fix.</span><span class="sxs-lookup"><span data-stu-id="8cdff-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="8cdff-108">Dacă utilizați versiunea 7.3.0 și aduceți tranzacții cu taxe de la Project Service Automation, trebuie să instalați KB 4345320 pentru a include aceste taxe în factura proiectului.</span><span class="sxs-lookup"><span data-stu-id="8cdff-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="8cdff-109">Dacă utilizați versiunea 8.0, veți putea utiliza integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității.</span><span class="sxs-lookup"><span data-stu-id="8cdff-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="8cdff-110">Dacă utilizați versiunea 8.0.1 sau o versiune ulterioară, veți putea sincroniza datele reale.</span><span class="sxs-lookup"><span data-stu-id="8cdff-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="8cdff-111">Înainte de a putea integra Project Service Automation Finance, trebuie să configurați parametrii de integrare Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8cdff-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8cdff-112">Pentru informații suplimentare, consultați [Parametri de integrare Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8cdff-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="8cdff-113">Această soluție de integrare permite sincronizarea directă în următoarele scenarii:</span><span class="sxs-lookup"><span data-stu-id="8cdff-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8cdff-114">Mențineți contractele de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-115">Creați proiecte în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-116">Mențineți liniile de contract de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-117">Mențineți jaloanele de linii de contract de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-118">Mențineți sarcinile de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-119">Mențineți categoriile de tranzacții de cheltuieli în Finance și sincronizați-le direct din Finance la Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8cdff-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="8cdff-120">Creați estimări orare de proiect în Project Service Automation și sincronizați-le direct din Project Service Automation în Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-121">Creați estimări de cheltuieli de proiect în Project Service Automation și sincronizați-le direct din Project Service Automation în Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8cdff-122">Creați durata proiectului, cheltuielile și taxele reale în Project Service Automation și creați tranzacții de proiect în jurnalul de integrare Project Service Automation, astfel încât să poată fi postate în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="8cdff-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8cdff-123">Sincronizarea datelor</span><span class="sxs-lookup"><span data-stu-id="8cdff-123">Data synchronization</span></span>

<span data-ttu-id="8cdff-124">Următoarea ilustrație arată cum sunt sincronizate datele ca parte a integrării dintre Project Service Automation și Finance.</span><span class="sxs-lookup"><span data-stu-id="8cdff-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="8cdff-125">Nu toate șabloanele sunt disponibile în prezent.</span><span class="sxs-lookup"><span data-stu-id="8cdff-125">Not all templates are currently available.</span></span> <span data-ttu-id="8cdff-126">Șabloanele vor fi lansate pe măsură ce sunt completate.</span><span class="sxs-lookup"><span data-stu-id="8cdff-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8cdff-127">[![Integrarea Project Service Automation cu Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8cdff-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="8cdff-128">Cerințe de sistem pentru Finance</span><span class="sxs-lookup"><span data-stu-id="8cdff-128">System requirements for Finance</span></span>

<span data-ttu-id="8cdff-129">Pentru a utiliza soluția de integrare Project Service Automation to Finance, trebuie să instalați Enterprise edition 7.3 cu platforma de actualizare 12 sau mai recentă.</span><span class="sxs-lookup"><span data-stu-id="8cdff-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8cdff-130">Cerințe de sistem pentru Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8cdff-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8cdff-131">Pentru a utiliza soluția de integrare Project Service Automation to Finance, trebuie să instalați următoarele componente:</span><span class="sxs-lookup"><span data-stu-id="8cdff-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8cdff-132">Dynamics 365 Project Service Automation versiunea 9.0.0.0 sau ulterioară</span><span class="sxs-lookup"><span data-stu-id="8cdff-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="8cdff-133">Soluția de perspectivă către numerar pentru Dynamics 365 Sales, versiunea 1.14.0.0 (v14) sau o versiune ulterioară</span><span class="sxs-lookup"><span data-stu-id="8cdff-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="8cdff-134">Soluție Project Automation Service to Finance pentru Dynamics 365 Project Service Automation versiunea 1.0.0.0 sau o versiune ulterioară</span><span class="sxs-lookup"><span data-stu-id="8cdff-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8cdff-135">Instalați soluția de integrare Project Service Automation to Finance în instanța dvs. Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8cdff-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="8cdff-136">Descărcați soluția de integrare Project Service Automation to Finance [Centrul de descărcare Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) și urmați instrucțiunile incluse în soluție.</span><span class="sxs-lookup"><span data-stu-id="8cdff-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
