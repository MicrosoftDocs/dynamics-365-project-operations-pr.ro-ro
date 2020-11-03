---
title: Prezentare generală a asistentului de planificare
description: Acest subiect furnizează informații despre lucrul cu asistentul de planificare pentru a rezerva resurse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082652"
---
# <a name="schedule-assistant-overview"></a>Prezentare generală a asistentului de planificare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Asistentul de planificare este utilizat pentru a rezerva resurse pe baza cerințelor definite de managerul de proiect. Asistentul de planificare se bazează pe parametrii furnizați în cerința resursei pentru a găsi resursa. Asistentul de planificare recomandă resurse care corespund cerințelor relevante, cum ar fi ferestrele de timp sau abilitățile necesare.

După identificarea resurselor adecvate, resursa sau managerul de proiect poate rezerva resursa la lucrare.

## <a name="prerequisites"></a>Cerințe preliminare

Asistentul de planificare face parte din soluția Universal Resource Scheduling. Această soluție este inclusă și instalată cu Dynamics 365 Project Operations, Dynamics 365 Field Service și Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Cerințe și resurse potrivite

O cerință de resursă generată se bazează pe detalii precum:

-   Caracteristici
-   Roluri
-   Unități de business
-   Preferințe resurse
-   Contururi de efort
-   Fus orar

Asistentul de planificare utilizează aceste detalii pentru a filtra resursele.

## <a name="launch-the-schedule-assistant"></a>Lansați Asistentul de planificare

Există două moduri în care este lansat asistentul de programare. Dacă utilizați modul hibrid, în grila membrilor echipei puteți selecta orice membru al echipei cu o cerință de resurse neîndeplinită, apoi selectați **Rezervare**. Dacă utilizați modul central, managerul de resurse găsește și selectează resursa.

## <a name="schedule-assistant-filters"></a>Filtre asistent de planificare

După executarea asistentului de planificare, detaliile din cerința de resurse sunt afișate ca valori filtrate în panoul din stânga. Managerul de resurse sau managerul de proiect pot ajusta rezultatele ajustând filtrele pentru a satisface nevoile de planificare.

Panoul de filtrare prezintă opțiuni legate de muncă, inclusiv:

-   Începutul și sfârșitul lucrului
-   Caracteristici
-   Roluri
-   Unități organizaționale
-   Firmă de resurse
-   Tipuri de resursă
-   Resurse preferate
