---
title: De ce prețul pentru cheltuielile reale de vânzare revine la zero?
description: Următoarele trei verificări vă vor ajuta să detectați motivul pentru care prețul este setat implicit pe 0 pe cheltuieli reale de vânzare.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 85a177ec-ad61-450d-bfe6-cdea7a415566
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ccbad4ac969ffe4f09744557e2a9be68aa93e8c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754809"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>De ce prețul pentru cheltuielile reale de vânzare revine la zero?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Acest FAQ se aplică cheltuielilor reale în cazul în care clasa de tranzacție este setată la Cheltuieli și tipul de tranzacție este Vânzări nefacturate. Următoarele trei verificări vă vor ajuta să detectați motivul pentru care prețul (rata de facturare) este setat implicit pe 0 pe cheltuieli reale de vânzare.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Verificarea 1: Identificarea listei de prețuri de vânzare pentru proiect

Găsiți proiectul din domeniul proiectului efectiv și mergeți la pagina proiectului. Apoi, mergeți la fila Vânzări. Pe grila de linii de contract proiect, faceți clic pe legătură în câmpul Contractul proiectului. Pagina Contractul proiectului se va deschide. Pe pagina Contractul proiectului, mergeți la fila Liste de prețuri proiect. Verificați dacă există cel puțin o listă de prețuri atașată aici.

În cazul în care nu este atașată nicio listă de prețuri în grila de liste de prețuri proiect a contractului proiectului, procedați după cum urmează:

- Atașați o listă de prețuri la grila de liste de prețuri a proiectului. Listele de prețuri care sunt autorizate să fie atașate aici ar trebui să aibă câmpul context setat pe Vânzări și câmpul monedă din lista de prețuri trebuie să corespundă cu câmpul monedă din contractul de proiect. Odată ce ați făcut remedierile necesare, recreați o intrare de cheltuieli, aprobați-o și verificați dacă vânzările nefacturate afișează efectiv un preț valid.
- Dacă aveți una sau mai multe liste de prețuri atașate în grila listei de prețuri a proiectului din contractul proiectului, mergeți la Verificarea 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Verificarea 2: Listele de prețuri identificate mai sus sunt valabile pentru data specifică a cheltuielii reale?

Pentru ca Project Service să ia în considerare o listă de prețuri pentru prețul implicit, lista de prețuri respectivă trebuie să se aplice pentru data de vânzări cheltuieli efective. Verificați următoarele pentru a vedea dacă lista (listele) de prețuri identificate mai sus sunt aplicabile:

- Începeți prin a verifica dacă datele de început și de sfârșit din fila generală pentru listele de prețuri atașate nu sunt necompletate. În cazul în care datele de început și de sfârșit de pe listele de prețuri identificate anterior sunt necompletate, ați izolat problema. 
- Faceți o notă în câmpul dată de început pe cheltuielile reale de vânzare și verificați dacă oricare dintre listele de prețuri identificate se aplică pentru această dată. De exemplu, data de cheltuieli reale ar trebui să se încadrează între data de început și data de sfârșit pe lista de prețuri. 
    - În cazul în care nu există nicio listă de prețuri care să acopere data pe cheltuielile reale de vânzare, ați izolat problema. Modificați datele de început și de sfârșit din lista de prețuri pentru a vă asigura că lista de prețuri cuprinde data cheltuielii efective. 
    - În cazul în care există mai mult de o listă de prețuri care să acopere data pe cheltuielile reale de vânzare, ați izolat problema. Puteți remedia acest lucru prin editarea datelor de început și sfârșit din listele de prețuri, astfel încât să existe doar o listă de prețuri, care să acopere data de cheltuieli reale. 
    - În cazul în care există doar o listă de prețuri, care să acopere data cheltuielilor reale, treceți la Verificarea 3.
Odată ce ați făcut remedierile necesare, recreați o intrare de cheltuieli, aprobați-o și verificați dacă vânzările nefacturate afișează efectiv un preț valid.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Verificarea 3: Există un preț valid pentru categoria de cheltuieli în lista de prețuri aplicabile proiectului? 

În cazul în care ați finalizat cu succes a Verificările 1 și 2, ar trebui să aveți acum doar o singură listă de prețuri proiect, care se aplică pentru data cheltuielilor reale de vânzare. Deschideți lista de prețuri proiect și mergeți la fila Prețuri categorie. Asigurați-vă că există un rând în grilă pentru categoria de cheltuieli specifice pe Cheltuiala efectivă.
 
- În cazul în care nu există niciun rând, ați izolat problema. Creați un rând în grila de preț categorie pentru categoria din cheltuiala dvs. reală. Odată ce ați făcut remedierile necesare, recreați o intrare de cheltuieli, aprobați-o și verificați dacă vânzările nefacturate afișează efectiv un preț valid. 
- În cazul în care există un rând pentru categoria de cheltuieli în grila de prețuri categorie, verificați dacă acesta are un preț valid.

Pentru a înțelege ce este un preț valid, utilizați aceste metode:

- În cazul în care câmpul Metodă de stabilire a prețurilor de pe linia Preț categorie este setat pe La cost, atunci rata de unitate pe Cheltuielile reale de vânzare va fi implicit valoarea din intrarea Cheltuieli.
- În cazul în care câmpul Metodă de stabilire a prețurilor de pe linia Preț categorie este setat la Adaos procentaj, atunci verificați dacă câmpul Procentaj este setat la o valoare validă. Rata de unitate pe cheltuielile reale de vânzare este setată implicit prin aplicarea acestui adaos de procent la prețul din intrarea Cheltuieli.
- În cazul în care câmpul Metodă de stabilire a prețurilor de pe linia Preț categorie este setat la Preț per unitate, atunci verificați dacă prețul este setat la o valoare validă. Rata de unitate pe cheltuielile reale de vânzare va fi implicit suma în valută specificată în câmpul preț.

Dacă setarea de preț pentru categoria de cheltuieli nu este validă, atunci ați izolat problema. Soluția este de a edita linia de preț categorie cu un preț valid pentru categoria de cheltuieli în conformitate cu regulile de mai sus. Odată ce ați făcut remedierile necesare, recreați o intrare de cheltuieli, aprobați-o și apoi verificați dacă vânzările nefacturate obțin efectiv un preț valid.

Dacă nu vedeți în continuare un preț valid pe cheltuielile reale de vânzare după ce ați efectuat cele trei verificări de mai sus, vă rugăm să solicitați un tichet de asistență.


