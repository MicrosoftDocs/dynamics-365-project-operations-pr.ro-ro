---
title: Elaborarea șabloanelor de proiect cu Copiere proiect
description: Acest subiect oferă informații despre cum să creați șabloane de proiect utilizând acțiunea personalizată Copiere proiect.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045024"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="00f23-103">Elaborarea șabloanelor de proiect cu Copiere proiect</span><span class="sxs-lookup"><span data-stu-id="00f23-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="00f23-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="00f23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="00f23-105">Dynamics 365 Project Operations acceptă capacitatea de a copia un proiect și de a reveni la orice resurse în resursele generice care reprezintă rolul.</span><span class="sxs-lookup"><span data-stu-id="00f23-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="00f23-106">Clienții pot utiliza această funcționalitate pentru a crea șabloane de bază de proiect.</span><span class="sxs-lookup"><span data-stu-id="00f23-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="00f23-107">Când selectați **Copie proiect**, starea proiectului țintă este actualizată.</span><span class="sxs-lookup"><span data-stu-id="00f23-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="00f23-108">Utilizați **Motiv stare** pentru a determina când este finalizată acțiunea de copiere.</span><span class="sxs-lookup"><span data-stu-id="00f23-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="00f23-109">Selectarea **Copie proiect** actualizează, de asemenea, și data de începere a proiectului la data de început curentă dacă nu este detectată nicio dată țintă în entitatea proiectului țintă.</span><span class="sxs-lookup"><span data-stu-id="00f23-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="00f23-110">Copiați acțiunea personalizată a proiectului</span><span class="sxs-lookup"><span data-stu-id="00f23-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="00f23-111">Nume</span><span class="sxs-lookup"><span data-stu-id="00f23-111">Name</span></span> 

<span data-ttu-id="00f23-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="00f23-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="00f23-113">Parametri de intrare</span><span class="sxs-lookup"><span data-stu-id="00f23-113">Input parameters</span></span>
<span data-ttu-id="00f23-114">Există trei parametri de intrare:</span><span class="sxs-lookup"><span data-stu-id="00f23-114">There are three input parameters:</span></span>

| <span data-ttu-id="00f23-115">Parametru</span><span class="sxs-lookup"><span data-stu-id="00f23-115">Parameter</span></span>          | <span data-ttu-id="00f23-116">Tip</span><span class="sxs-lookup"><span data-stu-id="00f23-116">Type</span></span>   | <span data-ttu-id="00f23-117">Valori</span><span class="sxs-lookup"><span data-stu-id="00f23-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="00f23-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="00f23-118">ProjectCopyOption</span></span>  | <span data-ttu-id="00f23-119">Șir</span><span class="sxs-lookup"><span data-stu-id="00f23-119">String</span></span> | <span data-ttu-id="00f23-120">**{"removeNamedResources":true}** sau **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="00f23-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="00f23-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="00f23-121">SourceProject</span></span>      | <span data-ttu-id="00f23-122">Referință de entitate</span><span class="sxs-lookup"><span data-stu-id="00f23-122">Entity Reference</span></span> | <span data-ttu-id="00f23-123">Proiectul sursă</span><span class="sxs-lookup"><span data-stu-id="00f23-123">Source Project</span></span> |
| <span data-ttu-id="00f23-124">Țintă</span><span class="sxs-lookup"><span data-stu-id="00f23-124">Target</span></span>             | <span data-ttu-id="00f23-125">Referință de entitate</span><span class="sxs-lookup"><span data-stu-id="00f23-125">Entity Reference</span></span> | <span data-ttu-id="00f23-126">Proiect țintă</span><span class="sxs-lookup"><span data-stu-id="00f23-126">Target Project</span></span> |


- <span data-ttu-id="00f23-127">**{"clearTeamsAndAssignments":true}**: Comportamentul implicit pentru proiectul pentru web și va elimina toate sarcinile și membrii echipei.</span><span class="sxs-lookup"><span data-stu-id="00f23-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="00f23-128">**{"removeNamedResources":true}** Comportamentul implicit pentru Project Operations și va reveni la atribuirea resurselor generice.</span><span class="sxs-lookup"><span data-stu-id="00f23-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="00f23-129">Pentru mai multe valori implicite privind acțiunile, consultați [Utilizați acțiuni Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="00f23-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="00f23-130">Specificați câmpurile de copiat</span><span class="sxs-lookup"><span data-stu-id="00f23-130">Specify fields to copy</span></span> 
<span data-ttu-id="00f23-131">Când este apelată acțiunea, **Copie proiect** va analiza vizualizarea proiectului **Copiere coloane de proiecte** pentru a determina ce câmpuri să fie copiate la copierea proiectului.</span><span class="sxs-lookup"><span data-stu-id="00f23-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="00f23-132">Exemplu</span><span class="sxs-lookup"><span data-stu-id="00f23-132">Example</span></span>
<span data-ttu-id="00f23-133">Următorul exemplu arată cum să apelați acțiunea personalizată **CopiațiProiect** cu setul de parametri **EliminațiResurseNumite**.</span><span class="sxs-lookup"><span data-stu-id="00f23-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
