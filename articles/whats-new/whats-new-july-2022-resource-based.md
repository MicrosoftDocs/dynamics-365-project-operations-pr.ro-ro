---
title: Noutăți iulie 2022 - Project Operations pentru scenarii bazate pe stocuri/producție
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din iulie 2022 a Microsoft Dynamics 365 Project Operations pentru scenarii bazate pe resurse/neaprovizionate.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403967"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți iulie 2022 - Project Operations pentru scenarii bazate pe stocuri/producție

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.44.0.22
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Nu există actualizări pentru hărțile cu dublă scriere Project Operations în această versiune. Pentru o listă actuală și versiuni ale hărților cu scriere duală Project Operations, consultați [Versiuni de hartă cu scriere duală Project Operations](../environment/resource-dual-write-maps.md).

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel asociate pe măsură ce actualizați operațiunile de proiect Dataverse soluție și versiunea soluției financiare. Este posibil ca unele funcții și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului out-of-box, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din [Problemă cu coloanele din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) secțiunea din ghidul de depanare cu scriere dublă.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Implementare și configurare | 2761472 | Este tratată o eroare de instalare Project Operations. |
| Facturarea și stabilirea prețurilor | 2746940 | Numele liniei de subcontractare trebuie să aibă o lungime maximă de 100 de caractere. |
| Facturarea și stabilirea prețurilor | 2739162 | Clienții trebuie să poată vedea butoanele de tip panglică în vizualizarea actuală a grilei. |
| Planificare și urmărire de proiect | 2730318 | Validare actualizată pentru caracterele neacceptate din subiectul proiectului. |
| Facturarea și stabilirea prețurilor | 2705361 | Datele efective de vânzări facturate de reper trebuie incluse în câmpurile de urmărire a proiectului. |
| Facturarea și stabilirea prețurilor | 2675880 | Preveniți conectarea unui proiect la o linie de contract care nu este bazată pe muncă. |
| Facturarea și stabilirea prețurilor | 2664396 | Dacă o listă de prețuri de cotație este salvată fără o cotație, trebuie să existe o eroare care afirmă că oferta nu poate fi goală. |
| Facturarea și stabilirea prețurilor | 2184019 | The **Facturare bazată pe sarcini** fila nu ar trebui să fie afișată pentru proiectele care nu au contract de sprijin sau ofertă. |
| Timp și cheltuială | 2754459 | Când fluxul cloud de programare recurentă este inactiv, afișați bannerul și ocoliți procesarea asincronă. |
| Facturarea și stabilirea prețurilor | 2724391 | Se face o excepție greșită atunci când regula de facturare împărțită în contractul de proiect lipsește o valoare pentru client. |
| Facturarea și stabilirea prețurilor | 2708638 | Înregistrarea nu a fost găsită în timpul căutării utilizând căutarea pe grilă în Utilizări materiale și aprobări pentru utilizări materiale.|
| Facturarea și stabilirea prețurilor | 2686977 | Preveniți validarea liniei de factură în timpul creării facturii. |
| Facturarea și stabilirea prețurilor | 2683032 | Copierea rolurilor și categoriilor taxabile nu depășește 5000 de înregistrări.|
| Facturarea și stabilirea prețurilor | 2673363 | Procentul consumului de cost pe proiect este corupt atunci când există atât estimări de efort, cât și cheltuieli și valori reale pentru un proiect. |

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect si contabilitate in Finante

Pentru informații despre remedierea erorilor care sunt incluse în această actualizare, conectați-vă la Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [articol KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcțiile sunt activate în mod prestabilit în versiunea viitoare

Următorul tabel listează caracteristicile care sunt activate implicit în versiunea 10.0.29. Majoritatea funcțiilor care au fost activate automat pot fi dezactivate în [Managementul caracteristicilor](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). În viitor, unele funcții care au fost activate automat ar putea fi eliminate din Gestionarea caracteristicilor și devin obligatorii. Această modificare asigură că clienții folosesc funcționalitatea actuală, astfel încât îmbunătățirile se pot construi pe funcționalitatea curentă pe măsură ce sunt adăugate. Funcțiile nu vor fi niciodată activate automat în mai puțin de un an, cu excepția cazului în care se consideră că sunt esențiale.

| Numele caracteristicii | Activați data | Funcție adăugată | Stare caracteristică | Modul |
| --- | --- | --- |--- |--- |
| Activați ajustarea orelor de tranzacție în funcție de modificarea regulilor de finanțare | 16 septembrie 2022 | 7 Octombrie 2020 | Activat implicit | Management de proiect și contabilitate |
| Funcția de anulare a facturii de plată anticipată a comenzii de achiziție de proiect | 16 septembrie 2022 | 6 Octombrie 2021 | Activat implicit | Management de proiect și contabilitate |
| Ștergeți liniile de propunere de factură atunci când utilizați Operațiuni de proiect pentru scenarii bazate pe resurse/nestoc | 16 septembrie 2022 | 6 Octombrie 2021 | Activat implicit | Management de proiect și contabilitate |
| Ajustați contabilitatea pentru o tranzacție de proiect înregistrată | 16 septembrie 2022 | 10 mai 2020 | Activat implicit | Management de proiect și contabilitate |
| Activați configurarea contabilă implicită pentru proiect | 16 septembrie 2022 | 19 februarie 2020 | Activat implicit | Management de proiect și contabilitate |
| Activați mai multe linii contractuale pentru un proiect | 16 septembrie 2022 | 29 iunie 2020 | Activat implicit | Management de proiect și contabilitate |
| Faceți jurnalele Ora de proiect doar în citire dacă starea actuală de aprobare nu permite editarea | 16 septembrie 2022 | 6 Octombrie 2021 | Activat implicit | Management de proiect și contabilitate |
| Activați sincronizarea liniilor de vânzări din liniile de achiziție atunci când liniile de achiziție sunt actualizate și parametrul de gestionare a modificării comenzii de achiziție este activat | 16 septembrie 2022 | 7 Octombrie 2020 | Activat implicit | Management de proiect și contabilitate |
| Activați operațiunile de proiect pe Dynamics 365 Customer Engagement | 16 septembrie 2022 | 29 iunie 2020 | Activat implicit | Management de proiect și contabilitate |
| Caracteristica de corectare a inversării tranzacției de proiect | 16 septembrie 2022 | 13 iulie 2020 | Activat implicit | Management de proiect și contabilitate |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funcții care devin obligatorii în următoarea lansare

Următorul tabel listează caracteristicile care sunt obligatorii începând cu versiunea 10.0.29.

| Numele caracteristicii | Activați data | Funcție adăugată | Stare caracteristică | Modul |
| --- | --- | --- | --- | --- |
| Calculați valoarea angajată pe sursa de finanțare fără a rotunji cursul de schimb | 16 septembrie 2022 | 14 iunie 2020 | Obligatoriu | Management de proiect și contabilitate |
| Activați înregistrarea ajustărilor de proiect cu același cont contabil ca tranzacția inițială | 16 septembrie 2022 | 14 iunie 2020 | Obligatoriu | Management de proiect și contabilitate |
| Detaliu suma angajată prin contract de proiect | 16 septembrie 2022 | 31 august, 2019 | Obligatoriu | Management de proiect și contabilitate |
| Activați sortarea după resursă în timpul creării propunerii de factură de proiect | 16 septembrie 2022 | 31 august, 2019 | Obligatoriu | Management de proiect și contabilitate |
