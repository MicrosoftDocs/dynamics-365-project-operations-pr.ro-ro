---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 41, V3
description: Acest articol enumeră caracteristicile și remediile disponibile în Microsoft Dynamics 365 Project Service Automation Actualizați versiunea 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930563"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și corecțiile care sunt noi sau modificate pentru Actualizarea Project Service Automation Versiunea 41, V3. Această versiune are un număr de V3.10.62.162 și este, în general, disponibilă printr-o auto-actualizare în martie 2022.

## <a name="update-release-41"></a>Lansarea de actualizări 41

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Gestionare de proiect**
- Când încercați să creați un proiect dintr-un șablon care se bazează pe un proiect creat din programul de completare desktop, se afișează următoarea eroare, „Validarea câmpului de lucru planificat pentru alocarea resurselor: data de sfârșit a fiecărei secțiuni de timp alocarii resurselor nu trebuie să fie anterioară începerii acesteia. Data".

**Timp și cheltuială**
- Când încercați să ștergeți o intrare de timp, se afișează următorul mesaj de eroare, „Apare o eroare neașteptată din codul ISV”.

**Vânzări**
- Când creați o factură pentru o etapă de preț fix, **Descriere** și **Descriere externă** câmpurile nu sunt populate. 
