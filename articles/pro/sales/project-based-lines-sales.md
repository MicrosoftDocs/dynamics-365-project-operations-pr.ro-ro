---
title: Linii de proiect bazate pe oportunitate - simplificat
description: Acest subiect oferă informații despre linii de oportunitate pe bază de proiect. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bba555003b76e3e87412679b274f74f68ac7203b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181029"
---
# <a name="project-based-opportunity-lines---lite"></a>Linii de proiect bazate pe oportunitate - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Liniile de oportunități bazate pe proiecte sunt disponibile numai în oportunitățile bazate pe proiecte. Înregistrările de oportunitate bazată pe proiect au valoarea câmpului **Tip** setată la **Bazat pe muncă**.

Liniile de oportunitate bazate pe proiect sunt elementele rând care vor fi livrate clientului folosind un proiect. Cu toate acestea, un proiect nu poate fi legat de o linie de oportunități bazată pe proiect. Proiectele pot fi legate de elemente rând din etapa **Ofertă** și înainte, deoarece de obicei oportunitatea se află într-un stadiu incipient al ciclului de viață al unei înțelegeri. Determinarea numărului de proiecte care vor fi utilizate pentru livrarea lucrărilor pentru client este o decizie care se ia mai târziu în faza de vânzări. Puteți utiliza faza de oportunitate pentru a identifica componentele de livrare discrete pentru client. Deciziile referitoare la numărul real de proiecte utilizate pentru livrarea acestor componente pot fi respinse până când se cunosc mai multe informații despre lucrarea în sine.

Mai jos sunt câmpurile de pe o linie de oportunități bazată pe proiecte:

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Tip produs | Fila General (ascuns) | Puteți selecta una dintre următoarele opţiuni:</br>- Serviciu bazat pe proiecte (disponibil numai atunci când este instalat Dynamics 365 Project Operations)</br>- Produs bazat pe proiecte (disponibil numai atunci când sunt instalate Project Operations și Dynamics 365 Sales) | Valoarea acestui câmp este setată la **Serviciu bazat pe proiect** atunci când creați o linie de oportunitate bazată pe proiect din grila de linii bazate pe proiect din Opportunity. <br> Dacă modificați sau înlocuiți această valoare, funcționalitatea proiectului nu va fi activată pentru elementele rând bazate pe proiect. |
| Oportunitate | Fila General | Acest câmp este doar în citire și face referire la înregistrarea de oportunitate părinte căreia îi aparține acest element rând. | Nu există niciun impact din aval din acest domeniu. |
| Nume | Fila General | Acest câmp text modificabil poate fi utilizat pentru a da o scurtă identitate elementului rând. | Această valoare este reportată la linia de cotație atunci când creați o cotație din această oportunitate. |
| Buget client | Fila General | Acest câmp valutar editabil poate fi utilizat pentru a urmări suma pe care clientul este dispus să o cheltuiască pentru acest element rând. | Această valoare este reportată la câmpul corespondent pe linia de ofertă atunci când creați o ofertă din această oportunitate. |
| Metodă de facturare | Fila General | Acest câmp editabil are următoarele valori:</br>- Timp și material</br>- Preț fix | Această valoare este reportată la câmpul corespondent pe linia de ofertă atunci când creați o ofertă din această oportunitate. După crearea liniei de ofertă, câmpul este blocat și nu poate fi schimbat. Atribuiți această valoare câmpului cât mai exact posibil. Dacă trebuie să modificați valoarea acestui câmp pe linia de ofertă, ștergeți și recreați linia de ofertă. |
