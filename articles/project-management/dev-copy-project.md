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
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131628"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="03969-103">Elaborarea șabloanelor de proiect cu Copiere proiect</span><span class="sxs-lookup"><span data-stu-id="03969-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="03969-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="03969-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03969-105">Dynamics 365 Project Operations acceptă capacitatea de a copia un proiect și de a reveni la orice resurse în resursele generice care reprezintă rolul.</span><span class="sxs-lookup"><span data-stu-id="03969-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="03969-106">Clienții pot utiliza această funcționalitate pentru a crea șabloane de bază de proiect.</span><span class="sxs-lookup"><span data-stu-id="03969-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="03969-107">Când selectați **Copie proiect**, starea proiectului țintă este actualizată.</span><span class="sxs-lookup"><span data-stu-id="03969-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="03969-108">Utilizați **Motiv stare** pentru a determina când este finalizată acțiunea de copiere.</span><span class="sxs-lookup"><span data-stu-id="03969-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="03969-109">Selectarea **Copie proiect** actualizează, de asemenea, și data de începere a proiectului la data de început curentă dacă nu este detectată nicio dată țintă în entitatea proiectului țintă.</span><span class="sxs-lookup"><span data-stu-id="03969-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="03969-110">Copiați acțiunea personalizată a proiectului</span><span class="sxs-lookup"><span data-stu-id="03969-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="03969-111">Nume</span><span class="sxs-lookup"><span data-stu-id="03969-111">Name</span></span> 

<span data-ttu-id="03969-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="03969-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="03969-113">Parametri de intrare</span><span class="sxs-lookup"><span data-stu-id="03969-113">Input parameters</span></span>
<span data-ttu-id="03969-114">Există trei parametri de intrare:</span><span class="sxs-lookup"><span data-stu-id="03969-114">There are three input parameters:</span></span>

| <span data-ttu-id="03969-115">Parametru</span><span class="sxs-lookup"><span data-stu-id="03969-115">Parameter</span></span>          | <span data-ttu-id="03969-116">Tip</span><span class="sxs-lookup"><span data-stu-id="03969-116">Type</span></span>   | <span data-ttu-id="03969-117">Valori</span><span class="sxs-lookup"><span data-stu-id="03969-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="03969-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="03969-118">ProjectCopyOption</span></span>  | <span data-ttu-id="03969-119">Șir</span><span class="sxs-lookup"><span data-stu-id="03969-119">String</span></span> | <span data-ttu-id="03969-120">**{"removeNamedResources":true}** sau **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="03969-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="03969-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="03969-121">SourceProject</span></span>      | <span data-ttu-id="03969-122">Referință de entitate</span><span class="sxs-lookup"><span data-stu-id="03969-122">Entity Reference</span></span> | <span data-ttu-id="03969-123">Proiectul sursă</span><span class="sxs-lookup"><span data-stu-id="03969-123">Source Project</span></span> |
| <span data-ttu-id="03969-124">Țintă</span><span class="sxs-lookup"><span data-stu-id="03969-124">Target</span></span>             | <span data-ttu-id="03969-125">Referință de entitate</span><span class="sxs-lookup"><span data-stu-id="03969-125">Entity Reference</span></span> | <span data-ttu-id="03969-126">Proiect țintă</span><span class="sxs-lookup"><span data-stu-id="03969-126">Target Project</span></span> |


- <span data-ttu-id="03969-127">**{"clearTeamsAndAssignments":true}**: Comportamentul implicit pentru proiectul pentru web și va elimina toate sarcinile și membrii echipei.</span><span class="sxs-lookup"><span data-stu-id="03969-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="03969-128">**{"removeNamedResources":true}** Comportamentul implicit pentru Project Operations și va reveni la atribuirea resurselor generice.</span><span class="sxs-lookup"><span data-stu-id="03969-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="03969-129">Pentru mai multe valori implicite privind acțiunile, consultați [Utilizați acțiuni Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="03969-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="03969-130">Specificați câmpurile de copiat</span><span class="sxs-lookup"><span data-stu-id="03969-130">Specify fields to copy</span></span> 
<span data-ttu-id="03969-131">Când este apelată acțiunea, **Copie proiect** va analiza vizualizarea proiectului **Copiere coloane de proiecte** pentru a determina ce câmpuri să fie copiate la copierea proiectului.</span><span class="sxs-lookup"><span data-stu-id="03969-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
