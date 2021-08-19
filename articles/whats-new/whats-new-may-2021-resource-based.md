---
title: Ce este nou în mai 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest subiect oferă informații despre actualizările de calitate disponibile în versiunea din mai 2021 a Project Operations pentru scenarii bazate pe resurse/fără stoc.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26d4d9feb386075fec2b5c0854e0762604a74d36c90068e35d351e52d95165d4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994696"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Ce este nou în mai 2021 - Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect se aplică următoarelor componente și versiuni Dynamics 365 Project Operations:

- Project Operations pe versiunea de mediu Dynamics 365 Dataverse 4.10.0.186
- Management de proiect și contabilitate în medii de aplicații Finance and Operations versiunea 10.0.18

## <a name="features-included-in-this-release"></a>Caracteristicile incluse în această versiune

Următoarele caracteristici sunt incluse în această versiune:

- [Moduri de planificare](../project-management/scheduling-modes.md): Managerii de proiect pot defini dacă un proiect ar trebui să fie gestionat utilizând durata fixă, munca fixă sau modul de planificare a unităților fixe.
- [Configurați kilometrajul utilizând nivelurile de rată a kilometrajului](../expense/set-up-mileage.md): Actualizați nivelurile de rată a kilometrajului pentru rapoartele de cheltuieli ale angajaților.

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următoarea listă prezintă hărțile cu scriere duală care au fost modificate sau adăugate în Project Operations, versiunea mai 2021.

| Maparea entității | Versiune actualizată | Comentarii |
| --- | --- | --- |
| Sursă de finanțare a proiectului (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronizarea contractului de proiect condițiile de plată ale clienților. |
| Propunere de facturi de proiect V2 (facturi) | 1.0.0.3 | Sincronizarea termenilor de plată a facturii proforma. |
| Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Actualizări de calitate |
| Proiecte V2 (msdyn\_projects) | 1.0.0.2 | Actualizări de calitate |

Rulați întotdeauna cea mai recentă versiune a hărții din mediul dvs. și să activați toate hărțile de tabel aferente pe măsură ce vă actualizați soluția dvs. Project Operations Dataverse și versiunea soluției Finance and Operations. Este posibil ca anumite caracteristici și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vedea versiunea activă a hărții în coloana  **Versiune**  de pe pagina  **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului predefinită, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management.md).

Dacă întâmpinați o problemă la pornirea hărții, urmați instrucțiunile din secțiunea [Problema coloanelor lipsă din tabel, pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) a ghidului de depanare Dual Write.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| **Zonă de caracteristici** | **Număr de referință** | **Actualizare de calitate** |
| --- | --- | --- |
| Facturarea și stabilirea prețurilor | 2227635 | Valorile din câmpurile implicite **Grup de unități** și **Unitate** din produsul din grila **Estimări materiale**. |
| Facturarea și stabilirea prețurilor | 2234127 | Câmpul **ID sarcina** se integrează acum corect în datele actuale ale proiectului Dataverse atunci când este postată o factură de furnizor. |
| Facturarea și stabilirea prețurilor | 2235564 | Salvarea liniei de jurnal asigură faptul că moneda afișată în intrarea liniei de jurnal corespunde monedei implicite cu linia după salvare. |
| Facturarea și stabilirea prețurilor | 2246671 | Efectuarea unei tranzacții neimpozabile în timpul facturării inversează înregistrarea inițială de vânzări nefacturate și creează un nou record de vânzări nefacturate ca neimpozabil. |
| Facturarea și stabilirea prețurilor | 2264042 | Corecția validă a facturii nu trebuie blocată dacă există un detaliu de corectare a facturii care nu este valid în mediu. |
| Facturarea și stabilirea prețurilor | 2146367 | Cartografierea cu scriere duală a antetului facturii proiectului este extinsă pentru a include condițiile de plată. |
| Managementul oportunităților | 2086888 | Nu adăugați roluri și categorii care sunt dezactivate înainte să copiați o ofertă la roluri tarifabile și categoriile unei oferte nou copiate. |
| Managementul oportunităților | 2234376 | Câmpurile numai în citire sunt în gri în grila **Estimări materiale**. |
| Managementul oportunităților | 2238337 | O ofertă bazată pe un contact poate fi salvată chiar dacă nu este asociată cu o listă de prețuri a proiectului. |
| Managementul oportunităților | 2239810 | Închiderea unei oferte pierdute închide, de asemenea, proiectul asociat și anulează orice rezervare. |
| Planificare și urmărire de proiect | 2099559 | S-au adăugat validări suplimentare pentru sănătatea sistemului înainte ca grila **Sarcini de proiect** să se deschidă. |
| Planificare și urmărire de proiect | 2178987 | S-a remediat o eroare tranzitorie care apare când selectați **Etapa următoare** pe pagina **Proiect**. |
| Gestionarea de resurse | 2224817 | Funcționalitatea pentru extinderea rezervărilor implicit la starea corectă a rezervării. |
| Intrare de timp | 2202476 | Pagina **Intrare de timp** folosește acum controlul rețelei de reacție și remediază probleme precum nealinierea grilei. |
| Intrare de timp | 2223377 | Intrarea de timp este ascunsă de secțiunea **Asociate cu** de pe pagina **Resursă care se poate rezerva** pentru a evita confuzia cu utilizabilitatea. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Management de proiect și contabilitate în Dynamics 365 Finance

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Management de proiect și contabilitate | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | În Project Operations pentru scenarii pe bază de resurse, nu puteți converti o ofertă în câștigată din cauza unei erori de integrare. |
| Management de proiect și contabilitate | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: apare un mesaj de eroare atunci când încercați să asociați o linie de contract la un ID de proiect din cauza verificării suprapunerii liniilor de contract și a tipurilor de tranzacții. |
| Management de proiect și contabilitate | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** setează adresa facturii sursă de finanțare de la un alt client. |
| Deplasări și cheltuieli | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Poate apărea o eroare de postare legată de configurarea kilometrajului. |
| Deplasări și cheltuieli | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funcționalitatea **Divizare la personal** nu funcționează pentru tranzacțiile cu cheltuieli în valută străină. |
| Deplasări și cheltuieli | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Valorile categoriei de cheltuieli din lista verticală afișează categorii incorecte pentru delegați, indiferent dacă sunt o resursă. |
| Deplasări și cheltuieli | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Nu puteți salva un raport de cheltuieli între companii din cauza unei erori la **Validarea resursei/categoriei**. |
| Deplasări și cheltuieli | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Calculul greșit al ratei de kilometraj în înregistrarea de raport de cheltuieli are linii separate. |
| Deplasări și cheltuieli | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Nu puteți publica un raport de cheltuieli între companii atunci când este inclusă taxa pe vânzări și tipul de cont compensat pe metoda de plată este **Lucrător**. |
| Deplasări și cheltuieli | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Entitata de date **TrvRequisitionLine** de derulare înapoi și indexul unic sunt asociate. |
| Deplasări și cheltuieli | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Raportul de cheltuieli acceptă crearea și actualizarea liniei de documente sursă. |
| Deplasări și cheltuieli | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un jurnal subregistru greșit este arătat într-un scenariu între companii dacă taxa de vânzări este înregistrată entității juridice de destinație. |
| Deplasări și cheltuieli | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: estimarea cheltuielii nu este ștearsă din Finanțe atunci când este ștearsă din Dataverse. |
| Deplasări și cheltuieli | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Când categoria de cheltuieli este o categorie care nu face parte din proiect, dimensiunile financiare care sunt selectate pe pagina **Cheltuieli** nu sunt copiate în raportul de cheltuieli. |
