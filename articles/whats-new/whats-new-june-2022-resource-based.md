---
title: Noutăți iunie 2022 - Project Operations pentru scenarii bazate pe stocuri/producție
description: Acest articol oferă informații despre actualizările de calitate care sunt disponibile în versiunea din iunie 2022 a Microsoft Dynamics 365 Project Operations pentru scenarii bazate pe resurse/neaprovizionate.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031346"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Noutăți iunie 2022 - Project Operations pentru scenarii bazate pe stocuri/producție

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol se aplică următoarelor componente și versiuni ale Microsoft Dynamics 365 Project Operations:

- Operațiuni de proiect în a Dataverse versiunea de mediu 4.43.0.77 sau 4.43.0.119
- Management de proiect și contabilitate într-un mediu Dynamics 365 Finance versiunea 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Actualizări de hărți Project Operations cu scriere duală

Următorul tabel arată hărțile cu dublă scriere care au fost modificate sau adăugate în versiunea Project Operations din iunie 2022.

| Maparea entității | Versiune actualizată | Comentarii |
| --- | --- | --- |
| Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Câmpul vechi a fost depreciat și mapat la noul câmp pentru urmărirea stării facturilor furnizorului. |

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. și activați toate hărțile de tabel asociate pe măsură ce actualizați operațiunile de proiect Dataverse soluție și versiunea soluției financiare. Este posibil ca unele funcții și capabilități să nu funcționeze corect dacă cea mai recentă versiune a hărții nu este activată. Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Pentru a activa o nouă versiune a hărții selectați **Versiuni ale hărții cu tabele**, selectați cea mai recentă versiune și apoi salvați versiunea selectată. Dacă ați personalizat o hartă a tabelului out-of-box, aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Dacă întâmpinați o problemă când porniți harta, urmați instrucțiunile din [Problemă cu coloanele din tabel lipsă pe hărți](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) secțiunea din ghidul de depanare cu scriere dublă.

## <a name="quality-updates"></a>Actualizări de calitate

### <a name="project-operations-on-dataverse"></a>Project Operations pe Dataverse

| Zonă de caracteristici | Număr de referință | Actualizare de calitate |
| --- | --- | --- |
| Subcontractare | 2708885 | S-a remediat mesajul de eroare care apare atunci când un utilizator creează o înregistrare antet de rezervare a resurselor rezervabile în care nu este completată nicio resursă rezervabilă. |
| Planificarea și urmărirea proiectului | 2629441 | S-a corectat logica de declanșare a fluxului de lucru pentru a ajuta la prevenirea unei bucle infinite atunci când sarcinile proiectului sunt actualizate. |
| Timp și cheltuieli | 2641209 | Importurile de intrări de timp din teme/rezervări trebuie să păstreze o referință de resurse care poate fi rezervată. |
| Planificarea și urmărirea proiectului | 2651148 | Antetul documentului de proiect trebuie protejat.|
| Planificarea și urmărirea proiectului | 2653145 | S-au adăugat validări pentru a se asigura că nu poate fi creată o înregistrare de proiect care are caractere nevalide în numele său. |
| Timp și cheltuieli | 2654710 | S-a corectat filtrarea pe **Aprobari** pagină. |
| Facturarea și stabilirea prețurilor | 2667805 | S-au adăugat validări pentru a preveni crearea de vânzări efective facturate dacă nu există susținerea vânzărilor reale nefacturate. |
| Facturarea și stabilirea prețurilor | 2668378 | Au fost adăugate validări pentru a împiedica adăugarea unei dimensiuni de preț personalizate, cu excepția cazului în care sunt completate un nume logic și un nume de câmp. |
| Subcontractare | 2677485 | S-a actualizat versiunea țintă a hărții cu scriere duală a liniilor de factură pentru furnizor. |
| Timp și cheltuieli | 2700428 | S-a îmbunătățit logica aprobărilor pentru a se asigura că alte seturi de aprobare pentru proiect pot fi procesate chiar dacă unul dintre seturile de aprobare este blocat în joburile de sistem. |

### <a name="project-management-and-accounting-in-finance"></a>Management de proiect si contabilitate in Finante

Pentru informații despre remedierea erorilor care sunt incluse în această actualizare, conectați-vă la Microsoft Dynamics Lifecycle Services (LCS) și vizualizați [articol KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).