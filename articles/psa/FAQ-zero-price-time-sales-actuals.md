---
title: De ce prețul pentru timpul de vânzare real revine la zero?
description: Detectarea motivului pentru care prețul pentru timpul de vânzare real revine la zero.
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
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146228"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>De ce prețul pentru timpul de vânzare real revine la zero?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Acest FAQ se aplică valorilor reale în cazul în care clasa de tranzacție este setată pe Timp și tipul de tranzacție este Vânzări nefacturate. Următoarele trei verificări vă vor ajuta să detectați motivul pentru care prețul (rata de facturare) este setat implicit pe 0 pe timpul de vânzare real.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Verificarea 1: Identificarea listei de prețuri de vânzare pentru proiect

Găsiți proiectul din domeniul proiectului efectiv și mergeți la pagina proiectului. Apoi, mergeți la fila Vânzări și pe grila de linii de contract proiect, faceți clic pe legătură în câmpul Contractul proiectului. Pagina Contractul proiectului se va deschide. Pe pagina Contractul proiectului, mergeți la fila Liste de prețuri proiect. Verificați dacă există cel puțin o listă de prețuri atașată aici. În cazul în care nu este atașată nicio listă de prețuri în grila de liste de prețuri proiect a contractului proiectului, ați izolat problema. Atașați o listă de prețuri la grila de liste de prețuri a proiectului. Listele de prețuri care sunt autorizate să fie atașate aici ar trebui să aibă câmpul context setat pe Vânzări și câmpul monedă din lista de prețuri trebuie să corespundă cu câmpul monedă din contractul de proiect. Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă vânzările nefacturate afișează efectiv un preț valid. 

Dacă aveți una sau mai multe liste de prețuri atașate în grila listei de prețuri a proiectului din contractul proiectului, mergeți la următoarea verificare a documentului.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Verificarea 2: Listele de prețuri identificate mai sus sunt valabile pentru data specifică a timpului de vânzare real?

Pentru ca Project Service să ia în considerare o listă de prețuri pentru prețul implicit, lista de prețuri respectivă trebuie să se aplice pentru data timpului de vânzare real. Verificați următoarele pentru a vedea dacă lista (listele) de prețuri identificate mai sus sunt aplicabile:
- Verificați dacă datele de început și de sfârșit din fila generală pentru listele de prețuri atașate nu sunt necompletate. În cazul în care datele de început și de sfârșit de pe listele de prețuri identificate anterior sunt necompletate, ați izolat problema. 
- Faceți o notă în câmpul dată de început pe timpul de vânzare real și verificați dacă oricare dintre listele de prețuri identificate se aplică pentru această dată. De exemplu, data timpului de vânzare real ar trebui să se încadreze între data de început și data de sfârșit pe lista de prețuri. 
    - În cazul în care nu există nicio listă de prețuri care să acopere data pe timpul de vânzare real, ați izolat problema. Modificați datele de început și de sfârșit din lista de prețuri pentru a vă asigura că lista de prețuri cuprinde data timpului de vânzare real. 
    - În cazul în care există mai mult de o listă de prețuri care să acopere data pe timpul de vânzare real, ați izolat problema. Puteți remedia acest lucru prin editarea datelor de început și sfârșit din listele de prețuri, astfel încât să existe doar o listă de prețuri, care să acopere data timpului de vânzare real. 
    - În cazul în care există doar o listă de prețuri, care să acopere data timpului de vânzare real, treceți la Verificarea 3.
Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă timpul de vânzare real afișează un preț valid.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Verificarea 3: Există un preț în lista de prețuri pentru dimensiunile tarifare pe timpul de vânzare real?

În cazul în care ați finalizat cu succes Verificările 1 și 2, ar trebui să aveți acum doar o singură listă de prețuri, care se aplică pentru data timpului de vânzare real. Deschideți această listă de prețuri și navigați la fila Prețuri rol. Asigurați-vă că există un rând în grilă pentru dimensiunile de stabilire a prețului pe timpul de vânzare real.

Dacă nu există niciun rând în grila de preț rol pentru dimensiunile de stabilire a prețului pe timpul de vânzare real, atunci ați izolat problema. Creați un rând în grila de Prețuri rol pentru dimensiunile tarifare pe timpul de vânzare real. Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă timpul de vânzare real afișează un preț valid.

Dacă nu vedeți în continuare un preț valid pe timpul de vânzare real după ce ați efectuat cele trei verificări de mai sus, vă rugăm să solicitați un tichet de asistență. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]