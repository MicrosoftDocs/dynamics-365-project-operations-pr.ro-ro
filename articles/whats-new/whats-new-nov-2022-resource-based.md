---
title: Ce este nou în noiembrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din noiembrie 2022 a Microsoft Dynamics 365 Project Operations pentru scenarii bazate pe resurse/nestoc.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831138"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în noiembrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.58.0.119
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Dataverse în Project Operations și versiunea de soluție financiară. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2781818 | Eroare cheie nu a fost găsită la stabilirea prețului implicit pentru jurnalul de utilizare a materialelor. |
| Facturarea și stabilirea prețurilor | 2922373 | Nu se poate conecta linia de ofertă la proiectul care s-a închis ca ofertă pierdută. |
| Facturarea și stabilirea prețurilor | 2943206 | **Câmpul Contract Line** din Entitatea de proiect ar trebui să fie opțional. |
| Facturarea și stabilirea prețurilor | 2953182 | Îmbunătățiți mesajul de eroare pentru facturile de corectare.|
| Facturarea și stabilirea prețurilor | 2959500 | Nu se poate conecta linia de ofertă la o sarcină de proiect care este deja asociată cu o ofertă pierdută.|
| Facturarea și stabilirea prețurilor | 2959560 | Mesajul „Acest client este deja în contractul de proiect” a primit în timp ce închidea oferta ca câștigată în anumite locații. |
| Facturarea și stabilirea prețurilor | 3031727 | Atribuțiile de resurse eșuează cu eroare lipsă în câmpul obligatoriu „msdyn_Company”. |
| Facturarea și stabilirea prețurilor | 3036905 | Compania proprietară nu este niciodată inițializată pe ProjectTeamMember. |
| Managementul oportunităților | 2763519 | Eroare de referință nulă în EnsureProjectContractAllowsUpdates. |
| Managementul oportunităților | 2783798 | La importarea estimărilor de proiect pe linia de cotație, lipsesc descrierile sarcinilor pentru estimările de cheltuieli și materiale.|
| Managementul oportunităților | 2988635 | Îmbunătățiți descrierea mesajului de eroare la ștergerea clientului din cotație. |
| Managementul oportunităților | 3001191 | Nu se poate crea o ofertă din Opportunity unde metoda de facturare este specificată ca nulă. |
| Upgrade | 3012324 | Conversia proiectului a eșuat pentru un proiect cu caractere de control precum Tab în numele său. || Planificare și urmărire de proiect | 2790384 | Timeout-ul Pending OperationSet este prea scurt. |
| Planificare și urmărire de proiect | 3044275 | Lipsește localizarea pentru: missingProjectSchedulerErrorMessage. |
| Planificare și urmărire de proiect | 3044277 | Grila Project Recon nu se încarcă când planificatorul este dezactivat.|
| Gestionarea de resurse | 2943153 | Actualizați fila Urmărire pentru a afișa două zecimale pentru Durată.|
| Subcontractare | 2932774 | Linia de factură a furnizorului, eroare de aruncare numai în citire incorect. |
| Subcontractare | 2939556 | Starea antetului facturii furnizorului nu ar trebui să fie setată la Ștergerea online a schiței dacă nu este activă. |
| Timp și cheltuială | 2939998 | Utilizați noua versiune TESA în ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Management de proiect și contabilitate în Finance

Pentru informații despre remedierile erorilor care sunt incluse în această actualizare, autentificați-vă în Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [Articolul KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
