---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 45, V3
description: Acest articol listează caracteristicile și remedierile disponibile în Microsoft Dynamics 365 Project Service Automation, versiunea de actualizare 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169185"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea de actualizare 45, V3. Această versiune are un număr de compilări V3.10.76.168 și este, în general, disponibilă prin auto-actualizare în iulie 2022.

## <a name="update-release-45"></a>Lansarea de actualizări 45

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Vânzări**

- Utilizatorii nu pot crea cu succes facturi după ce încearcă să creeze o factură fără vânzări nefacturate, dacă vizualizează și aceeași instanță a paginii și nu o reîmprospătează.

**Timp și cheltuială**

- Când Aprobări moderne este activat și se aprobă o aprobare de proiect rechemată, etapa de înregistrare este actualizată incorect la **Cerere de retragere aprobată**.
- Când Aprobări moderne este activat și Fluxuri Cloud este inactiv, procesul de aprobare nu are succes, iar utilizatorii care trimit sau aprobă nu sunt notificați.
