---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 40, V3
description: Acest articol enumeră caracteristicile și remedierile disponibile în Microsoft Dynamics 365 Project Service Automation Actualizați versiunea 40, V3.
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912807"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și remedierile care sunt noi sau modificate pentru Actualizarea Project Service Automation Versiunea 40, V3. Această versiune are numărul de versiune V3.10.61.61 și este în general disponibilă printr-o actualizare automată în februarie 2022.

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
