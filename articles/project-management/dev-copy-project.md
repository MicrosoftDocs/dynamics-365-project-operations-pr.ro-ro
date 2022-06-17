---
title: Elaborarea șabloanelor de proiect cu Copiere proiect
description: Acest articol oferă informații despre cum să creați șabloane de proiect folosind acțiunea personalizată Copiere proiect.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923847"
---
# <a name="develop-project-templates-with-copy-project"></a>Elaborarea șabloanelor de proiect cu Copiere proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations acceptă capacitatea de a copia un proiect și de a reveni la orice resurse în resursele generice care reprezintă rolul. Clienții pot utiliza această funcționalitate pentru a crea șabloane de bază de proiect.

Când selectați **Copie proiect**, starea proiectului țintă este actualizată. Utilizați **Motiv stare** pentru a determina când este finalizată acțiunea de copiere. Selectarea **Copie proiect** actualizează, de asemenea, și data de începere a proiectului la data de început curentă dacă nu este detectată nicio dată țintă în entitatea proiectului țintă.

## <a name="copy-project-custom-action"></a>Copiați acțiunea personalizată a proiectului

### <a name="name"></a>Nume 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Parametri de intrare

Există trei parametri de intrare:

- **ÎnlocuieșteNamedResources** sau **ClearTeamsAndAssignments** – Setați doar una dintre opțiuni. Nu le seta pe amândouă.

    - **\{„ReplaceNamedResources”:true\}** – Comportamentul implicit pentru Operațiuni de proiect. Orice resurse numite sunt înlocuite cu resurse generice.
    - **\{„ClearTeamsAndAssignments”:adevărat\}** – Comportamentul implicit pentru Proiect pentru Web. Toate misiunile și membrii echipei sunt eliminați.

- **SourceProject** – Referința entității a proiectului sursă din care să se copieze. Acest parametru nu poate fi nul.
- **Ţintă** – Referința entității a proiectului țintă în care să se copieze. Acest parametru nu poate fi nul.

Următorul tabel oferă un rezumat al celor trei parametri.

| Parametru                | Tipul             | Valoare                 |
|--------------------------|------------------|-----------------------|
| ÎnlocuieșteNamedResources    | Boolean          | **Adevărat** sau **Fals** |
| ClearTeamsAndAssignments | Boolean          | **Adevărat** sau **Fals** |
| SourceProject            | Referință de entitate | Proiectul sursă    |
| Țintă                   | Referință de entitate | Proiectul țintă    |

Pentru mai multe valori implicite ale acțiunilor, consultați [Utilizați acțiunile API-ului web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validari

Se fac următoarele validări.

1. Null verifică și preia proiectele sursă și țintă pentru a confirma existența ambelor proiecte în organizație.
2. Sistemul validează că proiectul țintă este valabil pentru copiere prin verificarea următoarelor condiții:

    - Nu există nicio activitate anterioară în cadrul proiectului (inclusiv selecția **Sarcini** fila), iar proiectul este nou creat.
    - Nu există o copie anterioară, nu a fost solicitat niciun import pentru acest proiect și proiectul nu are un **A eșuat** stare.

3. Operația nu este apelată folosind HTTP.

## <a name="specify-fields-to-copy"></a>Specificați câmpurile de copiat

Când este apelată acțiunea, **Copie proiect** va analiza vizualizarea proiectului **Copiere coloane de proiecte** pentru a determina ce câmpuri să fie copiate la copierea proiectului.

### <a name="example"></a>Exemplu

Următorul exemplu arată cum să apelați **CopyProjectV3** acțiune personalizată cu **removeNamedResources** set de parametri.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
