---
title: Noutăți august 2022 - Project Operations pentru scenarii bazate pe resurse/fără stocuri
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din august 2022 a Microsoft Dynamics 365 Project Operations pentru scenarii bazate pe resurse/neaprovizionate.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348108"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți august 2022 - Project Operations pentru scenarii bazate pe resurse/fără stocuri

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.45.0.53
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel asociate pe măsură ce actualizați operațiunile de proiect Dataverse soluție și versiunea soluției financiare. Este posibil ca unele funcții și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului out-of-box, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din [Problemă cu coloanele din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) secțiunea din ghidul de depanare cu scriere dublă.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Managementul oportunităților | 2762089 | Gestionarea erorilor la închiderea contractului ca pierdută dacă salvarea automată este dezactivată în organizație.|

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect si contabilitate in Finante

Pentru informații despre remedierea erorilor care sunt incluse în această actualizare, conectați-vă la Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [articol KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).