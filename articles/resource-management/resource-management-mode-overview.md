---
title: Prezentare generală a modurilor de gestionare a resurselor
description: Acest articol oferă informații despre funcționalitatea de gestionare a resurselor în Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928447"
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

În plus față de procesul de mod central acceptat, consultați următoarele articole pentru a gestiona toate celelalte fluxuri de rezervare acceptate în modul hibrid:

Rezervați o resursă direct unui proiect:
- [Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini](/dynamics365/project-service/assign-named-bookable-resource)

Rezervați o resursă dintr-o cerință de resurse:
- [Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervarea anumitor resurse din cerințele de resurse](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]