---
title: Noutăți august 2022 - Project Operations pentru scenarii bazate pe resurse/fără stocuri
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea de Microsoft Dynamics 365 Project Operations din august 2022 pentru scenarii bazate pe resurse/care nu există pe stoc.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403872"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți august 2022 - Project Operations pentru scenarii bazate pe resurse/fără stocuri

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.45.0.53
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Managementul oportunităților | 2762089 | Gestionarea erorilor la închiderea contractului ca pierdut dacă salvarea automată este dezactivată în organizație.|
|Planificare și urmărire de proiect | 2767841 | Actualizări de telemetrie pentru Entitatea proiectului Creare sau Actualizare scenarii.|
|Facturarea și stabilirea prețurilor | 2771072 | Gestionarea excepțiilor referințelor nule în timpul câștigării ofertei.|
|Facturarea și stabilirea prețurilor | 2844181 |Eșecul în obținerea unui ID de corelare și blocarea creării unei facturi.|
|Facturarea și stabilirea prețurilor | 2852836 | Lipsesc date efective între companii pentru Cheltuielile între companii create și aprobate în CE.|


### <a name="project-management-and-accounting-in-finance"></a>Management de proiect și contabilitate în Finance

Pentru informații despre remedierile erorilor care sunt incluse în această actualizare, Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [Articolul KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
