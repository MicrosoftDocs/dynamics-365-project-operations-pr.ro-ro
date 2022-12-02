---
title: Caracteristici eliminate sau perimate în Dynamics 365 Project Operations
description: Acest articol descrie caracteristici care au fost eliminate sau care sunt planificate pentru eliminare din Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028344"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Caracteristici eliminate sau perimate în Dynamics 365 Project Operations

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/non-stoc, implementare simplificată - facturare de la ofertă la proforma și Project Operations pentru scenarii stocate/bazate pe producție_

Acest articol descrie caracteristici care au fost eliminate sau care sunt planificate pentru eliminare din Dynamics 365 Project Operations.

- O caracteristică *eliminat* nu mai este disponibilă în produs.
- O caracteristică *perimat* nu este în dezvoltare activă și poate fi eliminată într-o actualizare viitoare.

Această listă este menită să vă ajute să luați în considerare aceste eliminări și perimări pentru propria dvs. planificare.

> [!NOTE]
> Informații detaliate despre obiectele din aplicațiile pentru finanșe și operațiuni pot fi găsite în [**Rapoarte tehnice de referință**](/dynamics/s-e/global/axtechrefrep_61). Puteți compara diferitele versiuni ale acestor rapoarte pentru a afla despre obiectele care s-au schimbat sau au fost eliminate din fiecare versiune a aplicațiilor de finanțe și operațiuni.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Caracteristici eliminate sau perimate în versiunea Project Operations din martie 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametrul de management de proiect și contabilitate „Creați întotdeauna tranzacția de ajustare”

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivul deprecierii / eliminării** | Tranzacțiile de ajustare sunt necesare în scopuri de audit. După perimare, acest parametru va fi ascuns. Sistemul va crea întotdeauna tranzacții de ajustare, așa cum face în prezent când parametrul este setat la **Da**. |
| **Înlocuit de altă caracteristică?** | No |
| **Zonele de produse afectate** | Aplicație |
| **Opțiune de implementare** | Project Operations pentru scenarii de producție/care există pe stoc |
| **Stare** | Perimat: până la 1 martie 2023, vom ascunde parametrul și vom schimba comportamentul sistemului, astfel încât tranzacțiile de ajustare să fie întotdeauna create. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametrul de management de proiect și contabilitate „Utilizarea datei de ajustare ca dată nouă a proiectului”

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivul deprecierii / eliminării** | Acest parametru a fost utilizat inițial pentru a permite ajustări atunci când un perioadă fiscală a fost închisă. Cu toate acestea, nu mai este necesar, deoarece data contabilă a tranzacției poate fi modificată la prima dată a perioadei deschise, dacă este configurată. Data proiectului nu trebuie modificată, deoarece reprezintă data la care a avut loc tranzacția. |
| **Înlocuit de altă caracteristică?** | No |
| **Zonele de produse afectate** | Aplicație |
| **Opțiune de implementare** | Project Operations pentru scenarii de producție/care există pe stoc |
| **Stare** | Perimat: până la 1 martie 2023, vom ascunde parametrul și vom schimba comportamentul sistemului astfel încât data proiectului să nu se modifice niciodată la ajustări. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Flux de lucru de solicitare de resurse în Project Operations pentru scenarii care există pe stoc/bazate pe producție

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivul deprecierii / eliminării** | Perimat din cauza limitărilor reduse de utilizare și volum de tranzacții. |
| **Înlocuit de altă caracteristică?** | No |
| **Zonele de produse afectate** | Aplicație |
| **Opțiune de implementare** | Project Operations pentru scenarii de producție/care există pe stoc |
| **Stare** | Perimat: până la 1 martie 2023, vom dezactiva opțiunea de a solicita resurse pentru proiect utilizând fluxul de lucru. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Pagina de propunere de factură de proiect fără vizualizări pentru Antet și Linii

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivul deprecierii / eliminării** | Perimat din cauza îmbunătățirilor aduse paginii care a fost introdusă împreună cu caracteristica cheie **Utilizarea formularelor de propunere de factură de proiect și jurnal de factură cu vizualizare pentru Antet și linii**. |
| **Înlocuit de altă caracteristică?** | Da |
| **Zonele de produse afectate** | Aplicație |
| **Opțiune de implementare** | Project Operations pentru scenarii de producție/care există pe stoc; Project Operations pentru scenarii de resurse/care nu există pe stoc |
| **Stare** | Perimat: până la 1 martie 2023, vom dezactiva pagina anterioară (tradițională) și vom activa caracteristica cheie **Utilizarea formularelor de propunere de factură de proiect și jurnal de factură cu vizualizare pentru Antet și linii** în mod implicit. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Caracteristici eliminate sau perimate în versiunea Project Operations din decembrie 2021

### <a name="collaboration-workspaces"></a>Spații de lucru de colaborare

[Creați sau conectați la un spațiu de lucru de colaborare (Proiect)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motivul deprecierii / eliminării** | Perimat din cauza utilizării reduse. Clienții care folosesc Project Operations pentru scenarii de resurse/care nu există pe stoc pot utiliza [Colaborare cu grupuri Office](../project-management/collaboration-groups.md). |
| **Înlocuit de altă caracteristică?** | No |
| **Zonele de produse afectate** | Aplicație  |
| **Opțiune de implementare** | Project Operations pentru scenarii de producție/care există pe stoc |
| **Stare** | Perimat: până la 1 decembrie 2022, intenționăm să nu mai acceptăm Spațiile de lucru de colaborare. |
