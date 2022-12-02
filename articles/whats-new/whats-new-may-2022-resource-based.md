---
title: Ce este nou în mai 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea de Microsoft Dynamics 365 Project Operations din mai 2022 pentru scenarii bazate pe resurse/care nu există pe stoc.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921409"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în mai 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.42.0.70
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate
### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Gestionarea resurselor | 2634019 | Mesaje de eroare îmbunătățite pentru validările de afaceri atunci când adăugați membri generici ai echipei ca resurse. |
| Planificarea și urmărirea proiectului | 2648515 | Actualizări restricționate ale entității **proprietarid**, **stare** și **stare** în entităţile de planificare. |
| Facturarea și stabilirea prețurilor | 2653167 | Separatorul zecimal al grilei **Estimări** trebuie să urmeze setări de format din **Opțiuni personale**. |
| Facturarea și stabilirea prețurilor| 2662251 | Valori din câmpurile **Unitate corectată** și **Grup de unități** sunt implicite la crearea înregistrărilor în estimările de materiale. |
| Facturarea și stabilirea prețurilor| 2571408 | Valorile reale de vânzări nefacturate sunt ștampilate cu un ID de factură proformă atunci când se creează o schiță de factură. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

Pentru informații despre remedierile erorilor care sunt incluse în această actualizare, conectați-vă la Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [Articolul KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
