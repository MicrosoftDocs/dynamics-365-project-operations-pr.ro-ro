---
title: Elaborarea șabloanelor de proiect cu Copiere proiect
description: Acest subiect oferă informații despre cum să creați șabloane de proiect utilizând acțiunea personalizată Copiere proiect.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642423"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="fe7ad-103">Elaborarea șabloanelor de proiect cu Copiere proiect</span><span class="sxs-lookup"><span data-stu-id="fe7ad-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="fe7ad-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="fe7ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="fe7ad-105">Dynamics 365 Project Operations acceptă capacitatea de a copia un proiect și de a reveni la orice resurse în resursele generice care reprezintă rolul.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="fe7ad-106">Clienții pot utiliza această funcționalitate pentru a crea șabloane de bază de proiect.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="fe7ad-107">Când selectați **Copie proiect**, starea proiectului țintă este actualizată.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="fe7ad-108">Utilizați **Motiv stare** pentru a determina când este finalizată acțiunea de copiere.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="fe7ad-109">Selectarea **Copie proiect** actualizează, de asemenea, și data de începere a proiectului la data de început curentă dacă nu este detectată nicio dată țintă în entitatea proiectului țintă.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="fe7ad-110">Copiați acțiunea personalizată a proiectului</span><span class="sxs-lookup"><span data-stu-id="fe7ad-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="fe7ad-111">Nume</span><span class="sxs-lookup"><span data-stu-id="fe7ad-111">Name</span></span> 

<span data-ttu-id="fe7ad-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="fe7ad-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="fe7ad-113">Parametri de intrare</span><span class="sxs-lookup"><span data-stu-id="fe7ad-113">Input parameters</span></span>
<span data-ttu-id="fe7ad-114">Există trei parametri de intrare:</span><span class="sxs-lookup"><span data-stu-id="fe7ad-114">There are three input parameters:</span></span>

| <span data-ttu-id="fe7ad-115">Parametru</span><span class="sxs-lookup"><span data-stu-id="fe7ad-115">Parameter</span></span>          | <span data-ttu-id="fe7ad-116">Tip</span><span class="sxs-lookup"><span data-stu-id="fe7ad-116">Type</span></span>   | <span data-ttu-id="fe7ad-117">Valori</span><span class="sxs-lookup"><span data-stu-id="fe7ad-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="fe7ad-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="fe7ad-118">ProjectCopyOption</span></span>  | <span data-ttu-id="fe7ad-119">Șir</span><span class="sxs-lookup"><span data-stu-id="fe7ad-119">String</span></span> | <span data-ttu-id="fe7ad-120">**{"removeNamedResources":true}** sau **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="fe7ad-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="fe7ad-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="fe7ad-121">SourceProject</span></span>      | <span data-ttu-id="fe7ad-122">Referință de entitate</span><span class="sxs-lookup"><span data-stu-id="fe7ad-122">Entity Reference</span></span> | <span data-ttu-id="fe7ad-123">Proiectul sursă</span><span class="sxs-lookup"><span data-stu-id="fe7ad-123">Source Project</span></span> |
| <span data-ttu-id="fe7ad-124">Țintă</span><span class="sxs-lookup"><span data-stu-id="fe7ad-124">Target</span></span>             | <span data-ttu-id="fe7ad-125">Referință de entitate</span><span class="sxs-lookup"><span data-stu-id="fe7ad-125">Entity Reference</span></span> | <span data-ttu-id="fe7ad-126">Proiect țintă</span><span class="sxs-lookup"><span data-stu-id="fe7ad-126">Target Project</span></span> |


- <span data-ttu-id="fe7ad-127">**{"clearTeamsAndAssignments":true}**: Comportamentul implicit pentru proiectul pentru web și va elimina toate sarcinile și membrii echipei.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="fe7ad-128">**{"removeNamedResources":true}** Comportamentul implicit pentru Project Operations și va reveni la atribuirea resurselor generice.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="fe7ad-129">Pentru mai multe valori implicite privind acțiunile, consultați [Utilizați acțiuni Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="fe7ad-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="fe7ad-130">Specificați câmpurile de copiat</span><span class="sxs-lookup"><span data-stu-id="fe7ad-130">Specify fields to copy</span></span> 
<span data-ttu-id="fe7ad-131">Când este apelată acțiunea, **Copie proiect** va analiza vizualizarea proiectului **Copiere coloane de proiecte** pentru a determina ce câmpuri să fie copiate la copierea proiectului.</span><span class="sxs-lookup"><span data-stu-id="fe7ad-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
