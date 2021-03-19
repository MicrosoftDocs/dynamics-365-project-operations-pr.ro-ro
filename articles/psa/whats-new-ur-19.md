---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 19, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280728"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, versiunea actualizată 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 19. Această versiune are un număr de versiune V3.10.30.41 și este disponibil în general printr-o autoactualizare în mai 2020.

## <a name="update-release-19"></a>Lansarea de actualizări 19

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme: 

- Erorile derivate din importurile de intrare temporale nu sunt descoperite corect.
- Grila de intrare în timp nu acceptă formatul câmpului **Numai dată**.
- Resursele proiectului nu pot crea o cheltuială cu un proiect.

**Gestionare de proiect**

S-au remediat următoarele probleme: 

-  Sarcina secundară de nivelul II determină o estimare incorectă a efortului în timpul calculului finalizării (EAC).

**Sales**

S-au remediat următoarele probleme: 

- Acțiunea **Recalculare** nu funcționează cu detaliile liniei contractului de cheltuieli sau cu detaliile liniei de ofertă.
- La **Actualizați prețurile** lipsesc estimările cheltuielilor.
-  Clienții nu sunt în măsură să selecteze motivele statutului personalizat ale contractului din pagina **Contract de proiect**.
- Clienții experimentează performanțe degradate atunci când creează o listă de prețuri personalizate dintr-o ofertă.
- Clienții se confruntă cu inconsistența valorii **unitate** implicte pe **Detalii despre linie de ofertă** și pagini **Detalii linie contract**.
- Adăugarea de articole din categoria de tranzacții care nu sunt exigibile la o linie de contract exigibilă nu va respecta tipul de facturare **Neaplicabil** al categoriei tranzacției.
- Clienții nu pot utiliza rolurile și categoria nou adăugate la contractele create anterior.
- Clienții experimentează performanțe degradate Necesarul de regăsire în PreValidateProjectTeamMemberUpdate.cs
- Rolurile sunt stabilite ca neimpozabile în lista **Categorii de resurse** ar trebui adăugată la fila **Roluri tarifabile** ca **Neaplicabil** pe linia contractului pentru un proiect.
- Clienții pot experimenta performanțe degradate atunci când creează un proiect deoarece **GetBookableResourceIdFromUser** preia toate coloanele de resurse rezervabile în loc de doar ID-ul primar.
- Entitatea **TransactionType** de unde lipsește insertul de actualizare a pre-validării pentru a împiedica accesul utilizatorilor **Unități** și **UnitGroups** care nu sunt valabile pentru tipurile de tranzacții.
- Pasul **Elimină** nu funcționează pentru importul de intrare în timp.


[!INCLUDE[footer-include](../includes/footer-banner.md)]