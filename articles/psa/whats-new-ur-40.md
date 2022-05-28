---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 40, V3
description: Acest subiect listează caracteristicile și remedierile disponibile în Actualizarea Microsoft Dynamics 365 Project Service Automation, versiunea 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588659"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 40, V3. Această versiune are numărul de versiune V3.10.61.61 și este în general disponibilă printr-o actualizare automată în februarie 2022.

## <a name="update-release-40"></a>Lansarea de actualizări 40

### <a name="features"></a>Caracteristici
Faza 1 a upgrade-ului de la Project Service Automation la Project Operations - Lite va fi lansată în februarie 2022 pentru toți clienții. Pentru a verifica eligibilitatea, consultați [Upgrade de la Project Service Automation la Project Operations](upgrade-project-operations-non-stocked.md). Dacă aplicația nu apare în instanța dvs. în Power Platform Centrul de administrare, contactați asistența și solicitați ca zborul să fie activat pentru mediile dvs. Solicitarea dvs. trebuie să includă o listă de ID-uri de mediu în care zborul trebuie să fie activat.

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**
- O intrare de notă lipsește atunci când o intrare de oră este respinsă sau anulată. 

**Vânzări**

- Când actualizați estimările de cost sau de vânzări utilizând plug-in-uri disponibile, vi se permite în mod incorect să trimiteți încărcături utile JSON care nu sunt valide în afara interfeței cu utilizatorul.
- Când actualizați liniile de cotație folosind vizualizarea rapidă, aveți permisiunea să activați cotațiile.
