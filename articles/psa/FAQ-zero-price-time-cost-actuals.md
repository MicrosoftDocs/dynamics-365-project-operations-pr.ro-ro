---
title: De ce prețul pentru costurile de timp reale revine la zero?
description: Detectarea motivului pentru care prețul pentru costurile de timp reale revine la zero.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146273"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>De ce prețul pentru costurile de timp reale revine la zero?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Acest FAQ se aplică cheltuielilor efective în cazul în care clasa de tranzacție este setată la Timp și tipul de tranzacție este la Cost. Următoarele trei verificări vă vor ajuta să detectați motivul pentru care prețul este setat implicit pe 0 pe costurile de timp reale.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Verificarea 1: Identificarea listei de prețuri de cost pentru proiect

Găsiți proiectul din domeniul proiectului efectiv și apoi mergeți la pagina proiectului. Faceți clic pe linkul unității contractante în câmp. Pe pagina unității contractante, verificați dacă unitatea contractantă are o listă de prețuri în grila de liste de prețuri de cost.

În cazul în care există mai mult de o listă de prețuri, ați izolat problema. Project Service acceptă numai o listă de prețuri per unitate organizațională. Eliminați toate listele de prețuri din această entitate, până când rămâne doar o listă de prețuri atașată în grila de Liste de prețuri de cost a unității organizaționale.

Dacă nu există nicio listă de prețuri atașată la unitatea organizațională, faceți o notă referitoare la moneda unității organizaționale. Mergeți la Project Service și apoi la Parametri și deschideți fila Liste de prețuri. Verificați dacă există liste de prețuri cu contextul setat la Cost și monedă care se potrivește cu moneda Unității organizaționale.
 
În cazul în care nu există nicio listă de prețuri care să îndeplinească aceste criterii, ați izolat problema. Asigurați-vă că aveți cel puțin o listă de prețuri a cărei context este setat pe Cost și a cărei monedă se potrivește cu moneda unității organizaționale.

În cazul în care există mai mult de o listă de prețuri care îndeplinește aceste criterii, continuați lectura acestui document pentru a face mai multe verificări.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Verificarea 2: Listele de prețuri identificate mai sus sunt valabile pentru data specifică a costurilor de timp reale?

Pentru ca Project Service să ia în considerare o listă de prețuri pentru prețul implicit, lista de prețuri respectivă trebuie să se aplice pentru data costurilor de timp reale. Verificați următoarele pentru a vedea dacă lista (listele) de prețuri identificate mai sus sunt aplicabile:

- Verificați dacă datele de început și de sfârșit din fila generală pentru listele de prețuri atașate nu sunt necompletate. În cazul în care datele de început și de sfârșit de pe listele de prețuri identificate anterior sunt necompletate, ați izolat problema. 
- Faceți o notă în câmpul dată de început pe costurile de timp reale și verificați dacă oricare dintre listele de prețuri identificate se aplică pentru această dată. De exemplu, data costurilor de timp reale ar trebui să se încadrează între data de început și data de sfârșit pe lista de prețuri. 
    - În cazul în care nu există nicio listă de prețuri care să acopere data pe costurile de timp reale, ați izolat problema. Modificați datele de început și de sfârșit din lista de prețuri pentru a vă asigura că lista de prețuri cuprinde data costurilor de timp reale. 
    - În cazul în care există mai mult de o listă de prețuri care să acopere data pe costurile de timp reale, ați izolat problema. Puteți remedia acest lucru prin editarea datelor de început și sfârșit din listele de prețuri, astfel încât să existe doar o listă de prețuri, care să acopere data costurilor de timp reale. 
    - Dacă există doar o listă de prețuri care acoperă data costurilor de timp reale, treceți la următoarea verificare în document.
Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă costurile de timp reale afișează un preț valid.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Verificarea 3: Există un preț în lista de prețuri pentru dimensiunile tarifare pe costurile de timp reale?

În cazul în care ați finalizat cu succes Verificările 1 și 2, ar trebui să aveți acum doar o singură listă de prețuri, care se aplică pentru data costurilor de timp reale. Deschideți această listă de prețuri și mergeți la fila Prețuri rol. Asigurați-vă că există un rând în grilă pentru dimensiunile de stabilire a prețului pe costurile de timp reale.

Dacă nu există niciun rând în grila de preț rol pentru dimensiunile de stabilire a prețului pe costurile de timp reale, atunci ați izolat problema. Creați un rând în grila de Prețuri rol pentru dimensiunile tarifare pe costurile de timp reale. Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă costurile de timp reale afișează un preț valid.
 
Dacă nu vedeți în continuare un preț valid pe costurile de timp reale după ce ați efectuat cele trei verificări de mai sus, vă rugăm să solicitați un tichet de asistență.





[!INCLUDE[footer-include](../includes/footer-banner.md)]