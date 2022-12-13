---
title: Configurați conversia valutară pentru a calcula prețurile de vânzare din ratele de cost
description: Acest articol explică cum să configurați comportamentul de conversie valutară care va fi utilizat în Microsoft Dynamics 365 Project Operations atunci când tranzacțiile de vânzare sunt generate din tranzacțiile de cost.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816697"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configurați conversia valutară pentru a calcula prețurile de vânzare din ratele de cost

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

În Microsoft Dynamics 365 Project Operations, prețurile de vânzare pentru categoriile de cheltuieli pot fi setate ca valori numerice sau pot fi configurate astfel încât să fie calculate pe baza costului suportat.

Când sunt configurate pentru a fi calculate pe baza costului suportat, sunt disponibile următoarele opțiuni:

- La cost
- Marcați procentul peste cost

În scenariile în care costul cheltuielilor este suportat într-o monedă care diferă de moneda de vânzare pentru contractul de proiect, conversia valutară este necesară pentru a calcula prețul de vânzare pe baza costului.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportament de conversie valutară care utilizează rate de schimb Dataverse native

În mod implicit, Operațiunile de proiect utilizează ratele de schimb valutare care sunt stocate în tabelul Monede în Dataverse. Pentru a configura Operațiunile de proiect pentru a utiliza cursurile de schimb native pentru a calcula prețurile de vânzare din cost, urmați acești pași.

1. Accesați **Operațiuni de proiect \> Setări \> Parametri**.
1. Deschideți pagina de detalii **Parametrul proiectului** .
1. Setați câmpul **Logica de conversie valutară** la o valoare goală.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportament de conversie valutară care utilizează ratele de schimb din aplicațiile financiare și operaționale

Cursurile de schimb din tabelul Monede care este disponibil nativ în Dataverse nu sunt valabile pentru data. Prin urmare, este posibil ca acestea să nu fie întotdeauna scalate la cerințele pe care le aveți pentru calcularea prețurilor de vânzare din ratele de cost.

Puteți utiliza cursurile de schimb din mediul financiar și operațional pentru a calcula prețul de vânzare în moneda de vânzare dintr-o rată de cost în moneda de cost. Pentru a configura acest comportament de conversie valutară, urmați acești pași.

1. Pe pagina **Parametrii proiectului**, adăugați câmpul **Logica de conversie valutară** . Apoi salvați și publicați personalizarea.
1. Accesați **Operațiuni de proiect \> Setări \> Parametri**.
1. Deschideți pagina de detalii **Parametrul proiectului** . 
1. Setați câmpul **Comportament de conversie valutară** la **Extins cu revenire la implicit**.
1. Acordați **utilizatorul aplicației cu dublă scriere** rol de securitate **Permisiunea de citire globală** la următoarele tabele:

    - msdyn\_ valută de schimb
    - msdyn\_ currencyexchangeratepairs
    - msdyn\_ exchangeratetypes

1. În mediul dumneavoastră financiar și operațional, rulați următoarele hărți cu scriere duală cu sincronizare inițială:

    - Tipul cursului de schimb (msdyn\_ exchangeratetypes)
    - Perechea valutară a cursului de schimb (msdyn\_ currencyexchangeratepairs)
    - Rate de schimb CDS (msdyn\_ currencyexchangerates)

După finalizarea acestor modificări, dual-write va face ca ratele de schimb din mediul financiar și operațional să fie disponibile în Dataverse. Operațiunile de proiect vor folosi apoi acele rate de schimb pentru a converti ratele de cost în moneda de vânzare a contractului.

> [!NOTE]
> Acest comportament de conversie valutară se aplică numai pentru calcularea prețurilor de vânzare din ratele de cost. Nu va fi folosit pentru a calcula în mod generic valorile monedei de bază. Valorile monedei de bază vor folosi întotdeauna cursurile de schimb Dataverse native, indiferent dacă finalizați această procedură.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
