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
# <a name="develop-project-templates-with-copy-project"></a>Elaborarea șabloanelor de proiect cu Copiere proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

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

Pentru mai multe valori implicite privind acțiunile, consultați [Utilizați acțiuni Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Specificați câmpurile de copiat 
Când este apelată acțiunea, **Copie proiect** va analiza vizualizarea proiectului **Copiere coloane de proiecte** pentru a determina ce câmpuri să fie copiate la copierea proiectului.
