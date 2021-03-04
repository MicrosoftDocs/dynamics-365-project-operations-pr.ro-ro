---
title: Configurați o planificare pentru onorariu
description: Acest subiect oferă informații despre cum să configurați o planificare de onorariu în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596387"
---
# <a name="set-up-a-retainer-schedule"></a>Configurați o planificare pentru onorariu

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Planificările de onorariu sunt configurate pe pagina **Contract de proiect** în Dynamics 365 Project Operations.

1. Pe pagina **Contract de proiect**, pe fila **Avansuri și onorarii**, selectați **Configurați planificare de onorariu**.
2. În pagina de dialog care se deschide, sunt afișate câmpurile listate în tabelul următor. Tabelul oferă o idee despre modul în care valorile introduse influențează sau influențează planificarea de onorariu care va fi creată.

| Câmp | Descriere | Impactul din aval |
| --- | --- | --- |
| Client pentru contractul de proiect | Clientul de pe contract care va fi facturat pentru acest onorariu sau avans. | Dacă aveți mai mulți clienți în contract și aveți nevoie să îi facturați pe fiecare dintre aceștia pentru un anumit punct de reținere sau o sumă în avans, creați manual o factură pentru fiecare client. |
| Început planificare onorariu | Introduceți data de începere a planificării de onorariu. | Este posibil ca această dată să nu fie data la care este creat primul onorariu sau avans. Data la care se creează primul onorariu sau avans este, de asemenea, influențată de frecvența facturii. |
| Sfârșit planificare onorariu | Introduceți data de final a planificării de onorariu. | Este posibil ca această dată să nu fie data la care este creat ultimul onorariu sau avans. Data la care se creează ultimul onorariu sau avans este, de asemenea, influențată de frecvența facturii. |
| Număr de onorarii de creat | Când introduceți numărul de rețele de creat, sistemul folosește data și frecvența de începere pentru a crea numărul în acest câmp. | Când acest câmp este actualizat manual, sistemul ignoră valoarea din câmpul **Sfârșitul planificării de onorariu** și creează în schimb numărul specific de onorarii sau avansuri. |
| Frecvență factură | Cât de des aplicația va crea elemente de onorarii și avansuri. | Această valoare influențează în mod direct numărul de elemente de onorarii și avansuri și datele create. |
| Sumă totală | Suma totală este suma care este împărțită în onorariu individual sau plățile în avans care vor fi create. | Nu există niciun impact din aval pentru acest domeniu. |