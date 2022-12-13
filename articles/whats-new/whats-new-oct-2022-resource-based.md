---
title: Ce este nou în Octombrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în ediția din octombrie 2022 a Microsoft Dynamics 365 Project Operations pentru scenarii bazate pe resurse/neaprovizionate.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806755"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în Octombrie 2022 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.57.0.176
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.30

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

| Zonă de caracteristici | Denumire funcție | Mai multe informații |
| --- | --- | --- |
| Planificare și urmărire de proiect | **Operațiuni de proiect Programare externă**<br>Modul de planificare externă permite clienților să creeze, să actualizeze și să ștergă în mod nativ entități care sunt legate de structurile de defalcare a lucrărilor (WBS) utilizând API-urile native Dataverse , fără limitele actuale impuse de Project for the Web. | [Programare externă](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementare și configurare | <p>**Permiteți clienților să aleagă tipul de implementare**<br>Actualizările bazate pe produs (PDU) ale Project Operations sunt folosite pentru a instala automat soluția Project Operations Dual-write atunci când soluțiile de bază și orchestrare Dual-write sunt instalate în mediu.</p><p>Această caracteristică introduce un nou parametru **Comportament de actualizare a soluției** în Parametrii proiectului. Când acest parametru este setat la **Numai Lite**, PUD-urile nu vor mai instala automat soluția de scriere dublă Project Operations, chiar dacă în mediu sunt instalate soluții de bază și de orchestrare dual-write. . Acest comportament va aduce beneficii clienților care intenționează să folosească soluții Dual-write pentru a integra comenzile de vânzări în aplicațiile de finanțare și operațiuni, dar doresc să folosească Operațiunile de proiect într-un mod simplificat (adică fără integrare în aplicațiile de finanțare și operațiuni).</p> | |
| Facturarea și stabilirea prețurilor | <p>**Conversie valutară pentru tranzacția de vânzare nefacturată pe cheltuieli în medii integrate**<br>Pentru clienții care utilizează Project Operations integrate cu aplicații de finanțare și operațiuni (adică în tipul de implementare cu resurse/ne-aprovizionate), ratele de schimb sunt de obicei stăpânite în aplicațiile de finanțare și operațiuni. Cu toate acestea, dacă o categorie de cheltuieli ar trebui să fie evaluată prin utilizarea metodei de calculare a prețului „la cost” sau „markup over cost” atunci când clientul este facturat, cursul de schimb care este utilizat pentru calcularea sumei vânzărilor folosește cursurile de schimb în Dataverse, nu cursurile de schimb din aplicațiile de finanțare și operațiuni.</p><p>Această funcție introduce un nou parametru **Comportamentul conversiei valutare** în Parametrii proiectului. Când acest parametru este setat la **Extins cu rezervă**, sumele vânzărilor nefacturate pentru tranzacțiile de cheltuieli sunt calculate utilizând cursurile de schimb din aplicațiile de finanțare și operațiuni.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual-write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2316317 | Sistemul permite crearea unei facturi care nu au tranzacții taxabile. |
| Facturarea și stabilirea prețurilor | 2737300 | Validați disponibilitatea câmpului **Client**  înainte de accesarea formularului. |
| Facturarea și stabilirea prețurilor | 2744948 | Adăugați o verificare nulă pentru Metoda de facturare. |
| Facturarea și stabilirea prețurilor | 2763515 | Gândirea erorii de referință nulă atunci când lipsește contractul de vânzare al facturii. |
| Facturarea și stabilirea prețurilor | 2844301 | Crearea facturii lot eșuează din cauza unei erori. |
| Facturarea și stabilirea prețurilor | 2845869 | Stocarea incorectă a serviciului de organizare. |
| Facturarea și stabilirea prețurilor | 2853729 | Detaliile despre rol și preț sunt actualizate atunci când se modifică Tipul de facturare. |
| Facturarea și stabilirea prețurilor | 2940350 | Când prețurile reale sunt stabilite, numai listele de prețuri active ar trebui introduse automat. |
| Implementare și configurare | 3001206 | Entitatea msdyn\_ replaylogheader împiedică actualizările organizațiilor clienților. |
| Managementul oportunităților | 2755582 | Gestionarea excepțiilor de referință nulă în Ajutorul regulilor de facturare împărțită. |
| Managementul oportunităților | 2761477 | Când se utilizează facturarea divizată, ștergerea unei etape (antet) lasă repere orfane. |
| Managementul oportunităților | 2767595 | Când o înregistrare de utilizare a materialului este deschisă în formularul principal, resursa rezervabilă pentru înregistrare este schimbată în utilizatorul conectat în prezent. |
| Planificare și urmărire de proiect | 2790384 | Timeout-ul Pending OperationSet este prea scurt. |
| Planificare și urmărire de proiect | 2957840 | Activitățile nu pot fi salvate, iar coloanele nu pot fi adăugate la pagina **Tasks**  din Integrated Project Operations. |
| Gestionarea de resurse | 2751560 | Unități de organizare preferate inconsecvente în necesarul de resurse. |
| Subcontractare | 2853245 | Potrivirea pentru valorile reale ale liniilor de factură pentru furnizor nu actualizează starea verificării dacă o linie de contract este deja conectată la linia de factură pentru furnizor. |
| Subcontractare | 2907231 | Etapa de procesare a facturilor furnizorilor nu poate avansa. |
| Timp și cheltuială | 2867363 | Înregistrările nu ies din vizualizarea Absențe/Vacanțe pentru aprobare atunci când sunt puse în coadă pentru aprobare. |
| Timp și cheltuială | 2894405 | TESA: Directorul POC neutilizat cauzează probleme de conformitate. |

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect și contabilitate în Finance

Pentru informații despre remedierile erorilor care sunt incluse în această actualizare, autentificați-vă în Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [Articolul KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
