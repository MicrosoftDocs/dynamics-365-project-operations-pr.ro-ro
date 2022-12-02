---
title: Ce este nou în septembrie 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate disponibile în lansarea din septembrie 2021 a Project Operations pentru scenarii de resurse/care nu există pe stoc.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923387"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în septembrie 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest articol se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

   - Project Operations în mediul Microsoft Dataverse versiunea 4.14.0.99.
   - Management de proiect și contabilitate în mediul Dynamics 365 Finance, versiunea 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Dataverse în Project Operations și versiunea de soluție financiară. Este posibil ca anumite caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vedea versiunea activă a hărții pe pagina **Scriere duală** în coloana **Versiune**. Pentru a activa o nouă versiune a hărții selectați  **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului predefinită, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă la pornirea hărții, urmați instrucțiunile din secțiunea [Coloanele tabelului lipsă apar pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) ghidului de depanare a scrierii duale.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Timp și cheltuieli | 1811407 | A fost modificat rolul de securitate pentru Aprobatorul de proiect pentru aprobările de intrare a cheltuielilor. |
| Timp și cheltuieli | 1811438 | A fost modificat rolul de securitate al Aprobatorului de proiect pentru anularea aprobărilor intrărilor de timp. |
| Timp și cheltuieli | 2370126 | S-au actualizat pictogramele **Sarcina proiectului** și **Rol** în entitatea **Intrare de timp**. |
| Timp și cheltuieli | 2379879 | Am corectat funcția **Copiați săptămâna** în introducerea timpului atunci când utilizați Dynamics 365 pentru telefon. |
| Facturarea și stabilirea prețurilor | 2371906 | Suma totală a facturii Proforma nu trebuie să fie ajustabilă în Project Operations pentru implementări bazate pe resurse. |
| Facturarea și stabilirea prețurilor | 2385802 | S-a remediat eroarea care apare cu ore reale negative atunci când totalurile proiectului sunt actualizate. |
| Facturarea și stabilirea prețurilor | 2389675 | Îmbunătățirea comportamentului de confirmare a facturii proforma. Entitatea de locuri de muncă de lungă durată trebuie să ia în considerare activitatea necesară pentru a scrie rezultatele confirmării pentru contabilitate. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Deplasări și cheltuieli | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Sumele aferente tranzacțiilor privind vânzătorul și impozitul pe vânzări înregistrate dintr-o cheltuială care a fost creată dintr-o tranzacție cu cardul de credit sunt incorecte. |
| Deplasări și cheltuieli | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Liniile greșite de decontare sunt create atunci când este generat jurnalul de plăți. |
| Deplasări și cheltuieli | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Sumele aferente tranzacțiilor privind impozitul pe vânzări înregistrate dintr-o cheltuială care a fost creată dintr-o tranzacție cu cardul de credit sunt incorecte. |
| Deplasări și cheltuieli | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Ștergerea unei linii de cheltuieli ar putea dura mult. |
| Contabilitatea proiectelor | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | După ce aplicați KB 4619395, schimbând secvența numerică în **Continuu** nu este acceptat și atunci când postați o estimare, apare următoarea eroare: „Sistemul nu acceptă configurarea„ continuă ”a secvenței numerice Proj_X.” |
| Contabilitatea proiectelor | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Publicarea unei facturi de furnizor ar putea eșua cu următorul mesaj de eroare, „Tranzacțiile pe cupon nu se echilibrează conform 17/05/2021. (monedă contabilă: 0,00 - monedă de raportare: 0,01).” |
