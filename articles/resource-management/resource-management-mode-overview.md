---
title: Prezentare generală a modurilor de gestionare a resurselor
description: Acest subiect oferă informații despre funcționalitatea gestionării resurselor în Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118533"
---
# <a name="resource-management-modes-overview"></a>Prezentare generală a modurilor de gestionare a resurselor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Dynamics 365 Project Operations acceptă două moduri pentru a putea executa fluxul general de rezervare. Modul de gestionare este definit ca un parametru de proiect și poate fi modificat dacă afacerea dvs. are nevoie de schimbări.    

## <a name="central-mode"></a>Mod central
Pentru organizațiile care centralizează alocarea resurselor pentru proiecte, modul Central oferă o modalitate de a se asigura că managerii de proiect pot defini cerințele de resurse la nivelul proiectului. Îndeplinirea cerințelor de resurse este delegată unui manager de resurse. Managerii de proiect pot accepta sau respinge resursele propuse de managerul de resurse.

![Mod central](./media/resource-management-central.png)

Pentru a gestiona resursele cu modul Central, consultați:

- [Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervarea anumitor resurse din cerințele de resurse](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Remiterea unei solicitări de resursă](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Îndepliniți o solicitare de resurse](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptați sau respingeți o resursă de proiect propusă dintr-o solicitare de resursă](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mod hibrid
Pentru organizațiile care necesită flexibilitate în alocarea resurselor, modul hibrid permite atât managerilor de proiect, cât și managerilor de resurse capacitatea de a rezerva resurse.

![Mod hibrid](./media/resource-management-hybrid.png)

În plus față de procesul de modul central acceptat, consultați următoarele subiecte pentru a gestiona toate celelalte fluxuri de rezervare acceptate în modul hibrid:

Rezervați o resursă direct unui proiect:
- [Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezervați o resursă dintr-o cerință de resurse:
- [Atribuirea de resurse generice care se pot rezerva unei activități și generarea cerințelor de resurse](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervarea anumitor resurse din cerințele de resurse](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]