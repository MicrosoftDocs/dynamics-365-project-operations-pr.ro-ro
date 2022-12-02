---
title: Ce este nou în noiembrie 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în lansarea din noiembrie 2021 a Project Operations pentru scenarii bazate pe resurse/care nu există pe stoc.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932909"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în noiembrie 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunilre 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.22

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- Interfețele de Tablou de planificare a aplicațiilor (API) pentru planificarea proiectelor acceptă acum capacitatea de a crea și de a șterge bucketurile pentru proiect.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-in-dataverse"></a>Project Operations în Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2240080 | Câmpul **Termeni de plată** nu trebuie să fie duplicat pe factura proformă. |
| Facturarea și stabilirea prețurilor | 2358236 | Corectarea facturii trebuie să permită corecții care au linii de preț zero. |
| Gestionarea de resurse | 2410072 | Permite configurarea unei resurse care este atribuită sarcinii ca manager de proiect. |
| Facturarea și stabilirea prețurilor | 2430234 | Remediați o problemă de calcul al performanței costurilor. |
| Timp și cheltuială | 2436978 | Permiteți introducerea timpului în format hh:mm. |
| Facturarea și stabilirea prețurilor | 2448623 | Permiteți actualizarea listelor de prețuri după ce sunt asociate cu o unitate organizațională. |
| Timp și cheltuială | 2460396 | Permiteți ștergerea unei intrări de timp prin ștergerea celulei. |
| Facturarea și stabilirea prețurilor | 2467386 | Permiteți ștergerea unui proiect care are o sarcină, chiar și atunci când sarcina este asociată cu o ofertă câștigată. |
| Timp și cheltuială | 2461744 | Vizualizarea **Aprobarea mea eșuată** conține numai aprobări de proiecte în starea de **Trimis**. |
| Timp și cheltuială | 2464082 | Eliminați legătura de la aprobările de proiect la setul de aprobare atunci când se potrivește o stare țintă. |
| Timp și cheltuială | 2468108 | Lucrarea de programare nu trebuie să seteze o stare **Prelucrare** pentru setul de aprobare. |
| Timp și cheltuială | 2471503 | Ștergeți seturile de aprobare vechi de șapte zile. |
| Facturarea și stabilirea prețurilor | 2480687 | Referința liniei de ofertă nu trebuie eliminată atunci când este creat un jalon al liniei de ofetă. |

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect și contabilitate în Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Sumele reținute ale furnizorului în tranzacțiile de cheltuieli ale proiectului nu sunt afișate în lista de tranzacții. |
| Management de proiect și contabilitate | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Factura furnizorului intercompanii este întreruptă atunci când integrarea facturii furnizorului este activată. |
| Management de proiect și contabilitate | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Condițiile de plată de pe facturile de proiect nu funcționează conform așteptărilor. |
| Management de proiect și contabilitate | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Când reținerea pentru furnizor este eliberată, publicarea voucherului are rânduri suplimentare care sunt incorecte. |
| Management de proiect și contabilitate | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Când este publicat jurnalul de integrare Project Operations, acesta eșuează din cauza dimensiunilor lipsă pentru un cont în care nu este publicat. |
| Management de proiect și contabilitate | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Fila **Project** nu poate fi editată pe o factură de furnizor în așteptare atunci când categoria de achiziție este atribuită articolului. |
| Management de proiect și contabilitate | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panoul de navigare lipsește dacă nu sunteți conectat la Project Operations Dataverse. |
| Management de proiect și contabilitate | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Când publicați venituri dintr-o factură de proiect într-un caz de reținere aplicat, apare o problemă deoarece tranzacțiile de pe voucher nu se echilibrează. |
| Management de proiect și contabilitate | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Crearea unei estimări după ce publicați o propunere de factură blochează liniile de corecție de la import. |
| Management de proiect și contabilitate | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Nu ar trebui să fie posibilă modificarea unei înregistrări facturate integral. |
| Deplasări și cheltuieli | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Toate rapoartele de cheltuieli sunt vizibile atunci când căutați o categorie în aplicația mobilă Cheltuieli. |
| Deplasări și cheltuieli | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Sumele incorecte pentru tranzacțiile furnizorilor și tranzacțiile cu impozitul pe vânzări sunt publicate dintr-o cheltuială care a fost creată dintr-o tranzacție cu cardul de credit. |
| Deplasări și cheltuieli | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Se afișează un avertisment irelevant atunci când actualizați pagina **Raport cheltuieli**. |
| Deplasări și cheltuieli | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Aprobatorul interimar greșit este utilizat când ștergeți un aprobator interimar și apoi retrimiteți un raport de cheltuieli prin fluxul de lucru. |
| Deplasări și cheltuieli | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | O eroare de postare legată de configurarea kilometrajului apare. |
