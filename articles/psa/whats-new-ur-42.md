---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 42, V3
description: Acest subiect listează caracteristicile și remedierile disponibile în Actualizarea Microsoft Dynamics 365 Project Service Automation, versiunea 42, V3.
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589211"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 42, V3. Această versiune are un număr de versiune V3.10.73.61 și este disponibil în general printr-o autoactualizare în aprilie 2022.

## <a name="update-release-42"></a>Lansarea de actualizări 42

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**

- Când o foaie de pontaj este respinsă, utilizatorul care a respins-o este identificat incorect ca **Sistem**.
- Când intrările de timp sunt importate, **Categoria de resurse** valoarea lipsește.
- Aprobatorii de proiecte pot aproba proiectele trimise atunci când permisiunile lor nu sunt setate în mod special **Poate aproba**.

**Vânzări**

- Când datele reale sunt înregistrate pe sarcini non-root, costurile reale sunt agregate incorect.
