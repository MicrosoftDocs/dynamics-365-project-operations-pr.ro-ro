---
title: Prezentare generală a reținerii furnizorilor
description: Acest articol oferă o prezentare generală a capabilităților de păstrare a furnizorilor.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916855"
---
# <a name="vendor-retention-overview"></a>Prezentare generală a reținerii furnizorilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Este posibil ca organizația dvs. să dorească să rețină o parte din plăți către furnizorii care lucrează la proiecte pentru organizația dvs. De exemplu, înainte de a plăti furnizorul dvs., vă recomandăm să vă asigurați că articolele și serviciile pe care le-au furnizat corespund așteptărilor dvs.

Când negociați achiziții pentru proiecte cu furnizori, puteți specifica termenii de păstrare a furnizorilor care includ procentul sau suma de reținut. Pe măsură ce furnizorul livrează articole și servicii, deduceți procentul sau suma de păstrare specificată din plata dvs. către furnizor. Când proiectul este finalizat sau atinge un stadiu intermediar, după cum se specifică în contractul furnizorului, eliberați suma reținută și creați o plată către furnizor.

## <a name="vendor-retention-example"></a>Exemplu de păstrare a furnizorilor

Următorul exemplu arată cum este reținut un procent din suma facturii furnizorului pe baza procentului complet pentru un proiect.

Contoso Robotics USA a contractat cu furnizorul Fabrikam pentru a oferi 100 de ore de instruire pentru proiectul de reînnoire a echipamentelor. Valoarea totală a contractului este 30.000 USD cu un preț de achiziție convenit de USD 300 pe oră.

Instruirea va fi livrată în trei etape cu următorul program:

- Faza 1: 50 de ore sau 50% din proiect
- Faza 2: 30 de ore sau 80% din proiect în total
- Faza 3: 20 de ore sau 100% din proiect

Următorul tabel listează termenii de păstrare.

| **Procentul de unități livrate** | **Procent de păstrat** | **Procent de eliberat** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Tranzacțiile au ca rezultat următoarele sume:

- Faza 1:
  - Suma de plătit este de 50 x 300 sau 15.000.
  - 20 la sută din sumă, sau 3.000, sunt reținute și vor fi eliberate într-o fază ulterioară.
  - Suma plătită furnizorului este de 12.000.
- Faza 2:
  - Suma de plătit este de 30 x 300 sau 9.000.
  - 10 la sută din sumă, sau 900, sunt reținute.
  - 10% din cei 3.000 care au fost reținuți în faza 1, sau 300, sunt eliberate.
  - Suma plătită furnizorului este de 8.400. Această sumă este cu 9.000 mai puțin de reținerea de 900 plus cele 300 care au fost eliberate din reținerea de fază 1.
- Faza 3:
  - Suma de plătit este de 20 x 300 sau 6.000.
  - Nu se reține nicio sumă.
  - Suma eliberată este de 3.600. Această sumă este formată din cele 3.000 care au fost reținute în faza 1, mai puțin cele 300 din faza 1 care au fost eliberate în faza 2, plus cele 900 care au fost reținute în faza 2.
  - Suma plătită furnizorului este de 9.600. Această sumă constă din suma reținută de 3.600 plus 6.000 pentru finalizarea fazei 3.

Suma totală plătită furnizorului după finalizarea celor trei faze este de 30.000, care este suma totală a comenzii de cumpărare (15.000 + 9.000 + 6.000).
