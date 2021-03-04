---
title: Configurarea categoriilor de cheltuieli
description: Acest subiect oferă informații despre cum să configurați categoriile de cheltuieli și categoriile partajate pentru rapoartele de cheltuieli.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123798"
---
# <a name="set-up-expense-categories"></a>Configurarea categoriilor de cheltuieli

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Când angajații creează rapoarte de cheltuieli, fiecare cheltuială pe care o înregistrează trebuie să fie asociată unei categorii de cheltuieli. Categoriile de cheltuieli sunt derivate din categorii comune care pot fi partajate între entitățile juridice din organizația dvs. În funcție de modul în care este definită organizația dvs., aceste categorii de cheltuieli pot fi distribuite și în alte domenii. Pe baza definiției organizației dvs. și a îndrumărilor din partea echipei de implementare, trebuie să determinați dacă categoriile care sunt utilizate în gestionarea cheltuielilor vor fi utilizate numai în gestionarea cheltuielilor sau ar trebui să fie partajate în alte domenii.

> [!NOTE]
> Aceste categorii pot fi împărțite între managementul de proiect și contabilitate și managementul cheltuielilor, sau între managementul de proiect și contabilitate și producție. Cu toate acestea, acestea nu pot fi împărțite între managementul cheltuielilor și producție.

Înainte de a putea începe procesul de configurare, trebuie luate următoarele decizii pentru fiecare categorie de cheltuieli:

- Care este categoria de cheltuieli? Exemplele includ categorii pentru zboruri, hotel sau kilometraj.
- Categoria de cheltuieli poate fi utilizată și în managementul proiectelor și contabilitate? Dacă poate, trebuie să luați și următoarele decizii:

    - Ce conturi de costuri vor fi utilizate pentru următoarele cheltuieli?

        - Cost
        - Alocare stat de plată
        - WIP-valoare de cost
        - Cost-element
        - WIP-valoare de cost-element
        - Pierderi acumulate
        - WIP-pierderi acumulate

    - Ce conturi de venituri vor fi utilizate pentru următoarele surse de venit?

        - Venituri facturate
        - Venit acumulat-valoarea vânzărilor
        - WIP-valoarea vânzărilor
        - Producție de venituri acumulate
        - WIP-producție
        - Venituri acumulate-profit
        - WIP-profit
        - Venituri acumulate-abonament
        - WIP-abonament

- Care este tipul de cheltuieli?
- Care este metoda de plată implicită pentru categoria de cheltuieli?
- Cheltuielile din categoria cheltuielilor trebuie să fie detaliate?
- Care este contul principal implicit pentru categoria de cheltuieli?
- Care este grupul implicit de impozitare pe vânzări pentru categoria de cheltuieli?
- Sunt permise metode de plată suplimentare pentru categoria de cheltuieli? Dacă da, care sunt acestea?
- Există subcategorii în această categorie de cheltuieli? Dacă sunt subcategorii, trebuie să luați și următoarele decizii:

    - Există vreuna dintre subcategoriile excluse din recuperarea impozitelor?
    - Care este grupul de taxe pe vânzări de articole din subcategorii?


[!INCLUDE[footer-include](../includes/footer-banner.md)]