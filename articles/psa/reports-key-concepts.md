---
title: Concepte-cheie
description: Acest subiect oferă informații despre conceptele-cheie pentru gestionarea resurselor în Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8e56523a9a2fbe8bc07e6d46062f4e1c20e6d2fa2244b32ff53e96d898b0086c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995101"
---
# <a name="key-concepts"></a>Concepte-cheie

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Următorul tabel definește conceptele cheie care sunt utilizate în aplicația Dynamics 365 Project Service Automation.

| Concept                    | Definire |
|----------------------------|------------|
| Membru echipă de proiect        | Ca parte a echipei de proiect, un membru al echipei de proiect poate fi o resursă denumită care are rezervări, o resursă denumită care nu are rezervări sau o resursă generică. Resursele generice nu au rezervări, sunt locale pentru proiect și nu au constrângeri de capacitate în cadrul proiectelor. |
| Resursă generică proiect   | Un substituent de resurse care vă permite să formați o echipă și un personal pentru un plan de proiect fără a fi nevoie să cunoașteți resursa denumită. Calendarul proiectului este utilizat drept calendarul resursei generice. Resursele generice pot fi adăugate la o echipă de proiect și atribuite la activități. |
| Ore rezervate               | Orele resursei sunt rezervate ferm pe un proiect pentru a ajuta la garantarea finalizării lucrului la proiect. Orele rezervate sunt consumate din capacitatea globală a resursei. Rezervările se fac numai pentru resursele denumite, nu pentru resursele generice. |
| Ore atribuite             | Orele resurselor sunt atribuite activităților din planificarea proiectului. Atribuirile pot fi făcute fie pentru resurse numite sau pentru resurse generice. Atribuirile pot fi independente de rezervări. |
| Ore obligatorii             | Capacitatea necesară, dar care nu este încă îndeplinită de o resursă denumită. Orele necesare sunt relevante numai pentru membrii generici ai echipei care au generat cerințe de resurse. |
| Cerere                     | Volumul de muncă curent și viitor. În Project Service Automation, cererea este afișată ca cerințe de resurse sau solicitări de resurse. |
| Cerință resursă       | O entitate care este utilizată pentru a capta orele necesare, datele de început și de sfârșit, competențele, geografia și alte dimensiuni de preț pentru resursele necesare. Cerințele de resurse sunt fie generate de membrii echipei de proiect, fie create individual. |
| Solicitare de resurse           | O entitate care este utilizată ca un „plic" pentru a transporta cerința de resurse care trebuie să îndeplinită de către un manager de resurse. |
| Rolul implicit al resursei      | Rolul sub care este grupată o resursă pentru calculul de utilizare. Se presupune că resursa are competențele necesare pentru rolul și îndeplinirea obiectivului de utilizare a acestui rol. |
| Unitatea organizațională a resursei | Unitatea organizațională la care este atribuită o resursă. |
| Contur                    | Activitate, cerință sau ore de atribuire conform defalcării într-o distribuție zilnică. De exemplu, o activitate de cinci zile, 40 de ore poate fi conturată în opt ore pe zi, timp de cinci zile. |
| Vizualizare reconciliere        | O vizualizare care afișează rezervările și atribuirile pentru fiecare membru al echipei de proiect. Această vizualizare îi permite managerului de proiect să caute orice nepotrivire între rezervări și atribuiri și să ia măsuri corective dacă are loc o nepotrivire. |
| Ore de lucru                 | O entitate care este utilizată pentru a identifica capacitatea de resurse și orele de lucru și non-lucru. Această entitate este denumită și calendarul resursei. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]