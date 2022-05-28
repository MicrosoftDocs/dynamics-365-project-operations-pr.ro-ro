---
title: Prezentare generală a modurilor de gestionare a resurselor
description: Acest subiect furnizează informații despre funcționalitatea de management al resurselor Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: f30bac95b2beb92345cbe25332963c58d2bde4bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585071"
---
# <a name="resource-management-modes-overview"></a>Prezentare generală a modurilor de gestionare a resurselor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Dynamics 365 Project Operations acceptă două moduri pentru ca dvs. să puteți executa fluxul general de rezervare. Modul de gestionare este definit ca un parametru de proiect și poate fi modificat dacă afacerea dvs. are nevoie de schimbări.    

## <a name="central-mode"></a>Mod central
Pentru organizațiile care centralizează alocarea resurselor pentru proiecte, modul Central oferă o modalitate de a se asigura că managerii de proiect pot defini cerințele de resurse la nivelul proiectului. Îndeplinirea cerințelor de resurse este delegată unui manager de resurse. Managerii de proiect pot accepta sau respinge resursele propuse de managerul de resurse.

![Mod central.](./media/resource-management-central.png)

Pentru a gestiona resursele cu modul Central, consultați:

- [Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervarea anumitor resurse din cerințele de resurse](/dynamics365/project-service/book-named-resource)
- [Remiterea unei solicitări de resursă](/dynamics365/project-service/submit-resource-request)
- [Îndepliniți o solicitare de resurse](/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptați sau respingeți o resursă de proiect propusă dintr-o solicitare de resursă](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mod hibrid
Pentru organizațiile care necesită flexibilitate în alocarea resurselor, modul hibrid permite atât managerilor de proiect, cât și managerilor de resurse capacitatea de a rezerva resurse.

![Mod hibrid.](./media/resource-management-hybrid.png)

În plus față de procesul de modul central acceptat, consultați următoarele subiecte pentru a gestiona toate celelalte fluxuri de rezervare acceptate în modul hibrid:

Rezervați o resursă direct unui proiect:
- [Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini](/dynamics365/project-service/assign-named-bookable-resource)

Rezervați o resursă dintr-o cerință de resurse:
- [Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervarea anumitor resurse din cerințele de resurse](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]