---
title: Ce este nou în februarie 2022 - Project Operations pentru scenarii bazate pe resurse/ne-stocate
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din februarie 2022 a Operațiunilor de proiect pentru scenarii bazate pe resurse/neaprovizionate.
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

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.28.0.120
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.24

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

- Începând cu această versiune, puteți adăuga până la 300 de membri ai echipei la un singur proiect. Anterior, limita numărului de membri ai echipei era de 150. Pentru mai multe informații, vezi [Limitele proiectului](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Actualizări ale hărților cu scriere duală pentru Operațiunile de proiect

Următoarea listă arată hărțile cu dublă scriere care au fost modificate sau adăugate în versiunea Project Operations din februarie 2022.

| Maparea entității | Versiune actualizată | Comentarii |
| --- | --- | --- |
| Entitatea de export pentru cheltuielile proiectului de integrare a operațiunilor de proiect (msdyn\_ cheltuieli) | 1.0.0.3 | Extins pentru sincronizarea activității proiectului la Dataverse. |

Pentru lista curentă și versiunile de hărți cu scriere duală Project Operations, consultați [Versiuni de hărți cu scriere duală pentru Operațiuni de proiect](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel asociate pe măsură ce actualizați operațiunile de proiect Dataverse soluție și versiunea soluției financiare. Este posibil ca unele funcții și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului out-of-box, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din [Problemă cu coloanele din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) secțiunea din ghidul de depanare Dual Write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2415109 | Valoarea implicită în **Condiții de plată pentru operațiuni** câmpul trebuie să fie înregistrarea clientului contractului de proiect și înregistrarea facturii proforma. |
| Facturarea și stabilirea prețurilor | 2497369 | Corecția materială trebuie să urmeze valoarea datei din **Corecţie** parametrii. |
| Facturarea și stabilirea prețurilor | 2498697 | S-a îmbunătățit configurația de securitate pentru **Rechemarea timpului de intrare**. |
| Facturarea și stabilirea prețurilor | 2513824 | Pentru scenariile bazate pe resurse, ID-ul categoriei de tranzacție nu trebuie să depășească 28 de caractere în Operațiuni de proiect. |
| Facturarea și stabilirea prețurilor | 2517455 | The **Actualizează tranzacțiile pe linia de factură** acțiunea nu trebuie să fie declanșată de mai multe ori simultan pentru aceeași factură. |
| Facturarea și stabilirea prețurilor | 2517465 | The **Dezactivați detaliile liniei de factură** acțiunea este blocată deoarece nu este acceptată. |
| Facturarea și stabilirea prețurilor | 2556660 | S-a remediat verificarea datei de efectivitate care se face pe lista de prețuri care este atașată la o înregistrare a parametrilor proiectului. |
| Managementul oportunităților | 2369202 | S-a corectat logica de afaceri care verifică că listele de prețuri care au date de intrare în vigoare suprapuse pot fi atașate aceluiași contract de proiect. |
| Managementul oportunităților | 2385965 | S-a corectat comportamentul pe **Clienți** fila din **Contract de proiect** pagina când selectați **Salveaza si inchide**. |
| Timp și cheltuieli | 2538503 | O sarcină de proiect trebuie să fie disponibilă în **Realitatea proiectului** entitate după înregistrarea unui raport de cheltuieli. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Management de proiect și contabilitate pe Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | În timpul importului notelor de credit ale furnizorului, apare o eroare. Mesajul de eroare afirmă: „Suma reținută nu poate fi mai mare decât suma netă rămasă”. |
| Management de proiect și contabilitate | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Dacă o propunere de factură include orice tranzacții cu taxe cu sumă zero care sunt vânzări reale nefacturate, facturarea nu poate avea loc. |
| Management de proiect și contabilitate | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Costul postat nu este corect după actualizarea prețului de achiziție și **Activați gestionarea modificărilor** este activat.|
| Management de proiect și contabilitate | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Devizul de înregistrare pentru un proiect cu preț fix utilizează moneda și suma incorecte din bonul de estimare, chiar și atunci când **Activați moneda contractului de proiect pentru calcularea estimării** caracteristica este activată. |
| Management de proiect și contabilitate | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Extensie** nu ar trebui să efectueze un apel pentru a activa urmărirea modificărilor fără a detecta excepții pentru entitățile care au chei de configurare care nu sunt activate. |
| Management de proiect și contabilitate | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Lucrarea în lot este remediată atunci când sunt postate mai multe jurnale avansate și apare o eroare. |
| Deplasări și cheltuieli | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Din cauza unei probleme de decontare care este legată de avansurile în numerar în rapoartele de cheltuieli, suma impozitului nu este acoperită ca parte a avansului în numerar. |
| Deplasări și cheltuieli | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informațiile privind impozitul pe vânzări nu sunt incluse în **Cheltuieli - Tranzacții înregistrate** raport. |
| Deplasări și cheltuieli | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | The **Chitanțe necesare** încălcarea politicii de cheltuieli afișează incorect un avertisment pe rapoartele de cheltuieli. |
| Deplasări și cheltuieli | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | O tranzacție de proiect nu include impozitul pe vânzări nerecuperabil în valoarea totală a vânzărilor atunci când tranzacția este rezultatul unei cheltuieli de kilometraj. |
| Deplasări și cheltuieli | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Când un rând detaliat are taxe, nu puteți modifica data rândului de detaliere și apare o eroare de stare a documentului sursă. |

## <a name="removed-and-deprecated-features"></a>Funcții eliminate și depreciate

The [Caracteristici eliminate sau depreciate în Operațiuni de proiect](removed-depreciated-features-project.md) articolul descrie funcțiile pentru care au fost eliminate sau depreciate Dynamics 365 Project Operations.

- O caracteristică eliminat nu mai este disponibilă în produs.
- O funcție învechită nu este în dezvoltare activă și ar putea fi eliminată într-o actualizare viitoare.

Un anunț de depreciere va apărea în [Caracteristici eliminate sau depreciate în Operațiuni de proiect](removed-depreciated-features-project.md) articol cu 12 luni înainte ca orice caracteristică să fie eliminată din produs.

Pentru modificările nerespective care afectează doar timpul de compilare, dar sunt compatibile binar cu mediile sandbox și de producție, timpul de depreciere va fi mai mic de 12 luni. De obicei, aceste modificări sunt actualizări funcționale care trebuie făcute compilatorului.
