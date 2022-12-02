---
title: Ce este nou în februarie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în lansarea din februarie 2022 a Project Operations pentru scenarii bazate pe resurse/care nu există pe stoc.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933001"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în februarie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate

*Se aplică la: Project Operations pentru scenarii bazate pe resurse/fără stoc*

Acest articol se aplică următoarelor componente și versiuni de Microsoft Dynamics 365 Project Operations:

- Project Operations într-un mediu Dataverse versiunea 4.28.0.120
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance, versiunea 10.0.24

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

- Începând cu această versiune, puteți adăuga până la 300 de membri ai echipei la un singur proiect. Anterior, limita numărului de membri ai echipei era de 150. Pentru informaţii suplimentare, consultaţi [Limite de proiect](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualizări de hartă Project Operations cu scriere duală

Următoarea listă prezintă hărțile cu scriere duală care au fost modificate sau adăugate în Project Operations, versiunea februarie 2022.

| Maparea entității | Versiune actualizată | Comentarii |
| --- | --- | --- |
| Entitate de integrare a Project Operations pentru cheltuieli de export (msdyn\_expenses) | 1.0.0.3 | Extins pentru sincronizarea activității proiectului la Dataverse. |

Pentru lista actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția Project Operations Dataverse și versiunea de soluție Finance. Este posibil ca unele caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă predefinită a tabelului, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din secțiunea [Problema coloanelor din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) a ghidului de depanare Dual Write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2415109 | Valoarea implicită în câmpul **Condiții de plată pentru operațiuni** trebuie să fie înregistrarea clientului contractului de proiect și înregistrarea facturii proformă. |
| Facturarea și stabilirea prețurilor | 2497369 | Corecția pentru materiale trebuie să urmeze valoarea datei din parametrii **Corecţie**. |
| Facturarea și stabilirea prețurilor | 2498697 | S-a îmbunătățit configurația de securitate pentru **Retragerea intrării de timp**. |
| Facturarea și stabilirea prețurilor | 2513824 | Pentru scenariile bazate pe resurse, ID-ul categoriei de tranzacție nu trebuie să depășească 28 de caractere în Project Operations. |
| Facturarea și stabilirea prețurilor | 2517455 | Acțiunea **Actualizare tranzacții pe linia de factură** nu trebuie să fie declanșată de mai multe ori simultan pentru aceeași factură. |
| Facturarea și stabilirea prețurilor | 2517465 | Acțiunea **Dezactivare detalii linie de factură** este blocată deoarece nu este acceptată. |
| Facturarea și stabilirea prețurilor | 2556660 | S-a remediat verificarea datei de intrare în vigoare care se face pe lista de prețuri care este atașată la o înregistrare a parametrilor proiectului. |
| Managementul oportunităților | 2369202 | S-a corectat logica de afaceri care verifică dacă listele de prețuri care au date de intrare în vigoare suprapuse pot fi atașate aceluiași contract de proiect. |
| Managementul oportunităților | 2385965 | S-a corectat comportamentul pe fila **Clienți** de pe pagina **Contract de proiect** când selectați **Salvare și închidere**. |
| Timp și cheltuieli | 2538503 | O sarcină de proiect trebuie să fie disponibilă în entitatea **Valori reale ale proiectului** după ce un raport de cheltuieli este publicat. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | În timpul importului de note de credit de la furnizor, apare o eroare. Mesajul de eroare afirmă: „Suma reținută nu poate fi mai mare decât suma netă rămasă”. |
| Management de proiect și contabilitate | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Dacă o propunere de factură include tranzacții cu taxe cu sumă zero care sunt vânzări reale nefacturate, facturarea nu poate avea loc. |
| Management de proiect și contabilitate | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Costul publicat nu este corect după actualizarea prețului de achiziție și **Activare gestionare modificări** este activat.|
| Management de proiect și contabilitate | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Devizul de înregistrare pentru un proiect cu preț fix utilizează moneda și suma incorecte din bonul de estimare, chiar și atunci când caracteristica **Activare a monedei contractului de proiect pentru calcularea estimării** este activată. |
| Management de proiect și contabilitate | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** nu ar trebui să efectueze un apel pentru a activa urmărirea modificărilor fără a detecta excepții pentru entitățile care au chei de configurare care nu sunt activate. |
| Management de proiect și contabilitate | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Lucrarea lot este remediată atunci când sunt postate mai multe jurnale avansate și apare o eroare. |
| Deplasări și cheltuieli | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Din cauza unei probleme de decontare care este legată de avansurile în numerar în rapoartele de cheltuieli, suma impozitului nu este acoperită ca parte a avansului în numerar. |
| Deplasări și cheltuieli | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informațiile privind taxele pe vânzări nu sunt incluse în raportul **Cheltuieli - Tranzacții publicate**. |
| Deplasări și cheltuieli | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Încălcarea politicii de cheltuieli **Chitanțe necesare** afișează incorect un avertisment pe rapoartele de cheltuieli. |
| Deplasări și cheltuieli | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | O tranzacție de proiect nu include impozitul pe vânzări nerecuperabil în valoarea totală a vânzărilor atunci când tranzacția este rezultatul unei cheltuieli de kilometraj. |
| Deplasări și cheltuieli | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Când un rând detaliat are taxe, nu puteți modifica data rândului de detaliere și apare o eroare de stare a documentului sursă. |

## <a name="removed-and-deprecated-features"></a>Caracteristici eliminate și perimate

Articolul [Caracteristici eliminate sau perimate în Project Operations](removed-depreciated-features-project.md) descrie funcțiile care au fost eliminate sau perimate pentru Dynamics 365 Project Operations.

- O caracteristică eliminat nu mai este disponibilă în produs.
- O caracteristică perimată nu este în dezvoltare activă și ar putea fi eliminată într-o actualizare viitoare.

Un anunț de perimare va apărea în articolul [Caracteristici eliminate sau perimate în Project Operations](removed-depreciated-features-project.md) cu 12 luni înainte ca orice caracteristică să fie eliminată din produs.

Pentru modificările nerespective care afectează doar timpul de compilare, dar sunt compatibile binar cu mediile sandbox și de producție, timpul de perimare va fi mai mic de 12 luni. De obicei, aceste modificări sunt actualizări funcționale care trebuie făcute compilatorului.
