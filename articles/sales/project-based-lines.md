---
title: Linii de proiect bazate pe oportunitate
description: Acest subiect oferă informații despre lucrul cu linii de oportunitate pe bază de proiect.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04e091a58f72a99fb17f37b95f9cac2b4476757b79965177854423361f416d51
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996361"
---
# <a name="project-based-opportunity-lines"></a>Linii de proiect bazate pe oportunitate

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Liniile de oportunități bazate pe proiecte sunt disponibile numai în oportunitățile bazate pe proiecte. Înregistrările de oportunitate bazată pe proiect au valoarea câmpului **Tip** setată la **Bazat pe muncă**.

Liniile de oportunitate bazate pe proiect sunt elementele rând care vor fi livrate clientului folosind un proiect. Cu toate acestea, un proiect nu poate fi legat de o linie de oportunități bazată pe proiect. Proiectele pot fi legate de elemente rând din etapa **Ofertă** și ulterior, deoarece de obicei oportunitatea apare într-un stadiu incipient al unei tranzacții. Determinarea numărului de proiecte care vor fi utilizate pentru livrarea lucrărilor pentru client este o decizie care se ia mai târziu în faza de vânzări. Utilizați faza de oportunitate pentru a identifica componentele de livrare discrete pentru client. Deciziile referitoare la numărul real de proiecte utilizate pentru livrarea acestor componente pot fi respinse până când se cunosc mai multe informații despre lucrarea în sine.

Mai jos sunt câmpurile de pe o linie de oportunități bazată pe proiecte:

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Tip produs | Fila General (ascuns) | Acesta este un câmp set de opțiuni. Dacă aveți Dynamics 365 Operations instalat, una dintre opțiunile disponibile este, **Serviciu bazat pe proiect**.  | Valoarea acestui câmp este setată la **Serviciu bazat pe proiect** atunci când creați linia de oportunitate bazată pe proiect din grila de linii bazate pe proiect din oportunitate. <br> Dacă modificați sau înlocuiți această valoare, funcționalitatea proiectului nu va fi activată pentru elementele rând bazate pe proiect. |
| Oportunitate | Fila General | Acest câmp este doar în citire și face referire la înregistrarea de oportunitate principală căreia îi aparține acest element de linie. | Nu există niciun impact din aval al acestui domeniu. |
| Nume | Fila General | Acesta este un câmp de text editabil care poate fi utilizat pentru a da o identitate scurtă a acestui element de linie | Această valoare este reportată la linia de ofertă atunci când creați o ofertă din această oportunitate |
| Buget client | Fila General | Acest câmp valutar editabil poate fi utilizat pentru a urmări suma pe care clientul este dispus să o cheltuiască pentru acest element rând. | Această valoare este reportată la câmpul corespondent pe linia de ofertă atunci când creați o ofertă din această oportunitate |
| Metodă de facturare | Fila General | Acest câmp editabil are următoarele valori:</br>- Timp și material</br>- Preț fix | Această valoare este reportată la câmpul corespondent pe linia de ofertă atunci când creați o ofertă din această oportunitate. După crearea liniei de ofertă, câmpul este blocat și nu poate fi schimbat. Atribuiți această valoare câmpului cât mai exact posibil. Dacă trebuie să modificați valoarea acestui câmp pe linia de ofertă, ștergeți și recreați linia de ofertă. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]