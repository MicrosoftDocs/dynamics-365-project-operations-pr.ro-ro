---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 42, V3
description: Acest articol listează caracteristicile și remedierile disponibile în Microsoft Dynamics 365 Project Service Automation, versiunea de actualizare 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912730"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea de actualizare 42, V3. Această versiune are un număr de versiune V3.10.73.61 și este disponibil în general printr-o autoactualizare în aprilie 2022.

## <a name="update-release-42"></a>Lansarea de actualizări 42

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**

- Când o foaie de pontaj este respinsă, utilizatorul care a respins-o este identificat incorect ca **Sistem**.
- Când intrările de timp sunt importate, valoarea **Categorie de resurse** lipsește.
- Aprobatorii de proiecte pot aproba proiectele trimise atunci când permisiunile lor nu sunt setate în mod special **Poate aproba**.

**Vânzări**

- Când datele reale sunt înregistrate pe sarcini non-rădăcină, costurile reale sunt adunate incorect.
