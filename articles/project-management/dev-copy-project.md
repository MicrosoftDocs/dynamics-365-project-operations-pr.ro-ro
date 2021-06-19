---
title: Elaborarea șabloanelor de proiect cu Copiere proiect
description: Acest subiect oferă informații despre cum să creați șabloane de proiect utilizând acțiunea personalizată Copiere proiect.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 7a1f602e789e07014fd6c742940f52341ce6c672
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005671"
---
# <a name="develop-project-templates-with-copy-project"></a>Elaborarea șabloanelor de proiect cu Copiere proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations acceptă capacitatea de a copia un proiect și de a reveni la orice resurse în resursele generice care reprezintă rolul. Clienții pot utiliza această funcționalitate pentru a crea șabloane de bază de proiect.

Când selectați **Copie proiect**, starea proiectului țintă este actualizată. Utilizați **Motiv stare** pentru a determina când este finalizată acțiunea de copiere. Selectarea **Copie proiect** actualizează, de asemenea, și data de începere a proiectului la data de început curentă dacă nu este detectată nicio dată țintă în entitatea proiectului țintă.

## <a name="copy-project-custom-action"></a>Copiați acțiunea personalizată a proiectului 

### <a name="name"></a>Nume 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parametri de intrare
Există trei parametri de intrare:

| Parametru          | Tip   | Valori                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | Șir | **{"removeNamedResources":true}** sau **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referință de entitate | Proiectul sursă |
| Țintă             | Referință de entitate | Proiect țintă |


- **{"clearTeamsAndAssignments":true}**: Comportamentul implicit pentru proiectul pentru web și va elimina toate sarcinile și membrii echipei.
- **{"removeNamedResources":true}** Comportamentul implicit pentru Project Operations și va reveni la atribuirea resurselor generice.

Pentru mai multe valori implicite privind acțiunile, consultați [Utilizați acțiuni Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Specificați câmpurile de copiat 
Când este apelată acțiunea, **Copie proiect** va analiza vizualizarea proiectului **Copiere coloane de proiecte** pentru a determina ce câmpuri să fie copiate la copierea proiectului.


### <a name="example"></a>Exemplu
Următorul exemplu arată cum să apelați acțiunea personalizată **CopiațiProiect** cu setul de parametri **EliminațiResurseNumite**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]