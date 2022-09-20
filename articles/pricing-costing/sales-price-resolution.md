---
title: Determinați prețurile de vânzare pentru estimări și valori reale bazate pe proiecte
description: Acest articol oferă informații despre modul în care sunt determinate prețurile de vânzare pentru estimările și valorile reale bazate pe proiecte.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475385"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Determinați prețurile de vânzare pentru estimări și valori reale bazate pe proiecte

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a determina prețurile de vânzare pe estimări și valori reale în Microsoft Dynamics 365 Project Operations, sistemul utilizează mai întâi data și moneda în estimarea primită sau contextul real pentru a determina lista de prețuri de vânzare. În contextul actual, în mod specific, sistemul utilizează **Data tranzacției** câmp pentru a determina care listă de prețuri este aplicabilă. The **Data tranzacției** valoarea estimată sau reală primită este comparată cu **Pornire efectivă (independent de fus orar)** și **Sfârșit efectiv (independent de fusul orar)** valorile de pe lista de preturi. După ce lista de prețuri de vânzare este determinată, sistemul determină rata de vânzare sau de facturare.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinarea ratelor de vânzare pe liniile reale și estimative pentru Time

Estimați contextul pentru **Timp** se refera la:

- Cotați detaliile liniei pentru **Timp**.
- Detalii linie contract pentru **Timp**.
- Atribuții de resurse pentru un proiect.

Contextul real pentru **Timp** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Timp**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de timp.
- Detaliile liniei de factură pentru **Timp**. 

După ce se stabilește o listă de prețuri pentru vânzări, sistemul parcurge următorii pași pentru a introduce rata de facturare implicită.

1. Sistemul se potrivește cu combinația dintre **Rol**, **de resurse**, și **Unitatea de Resurse** câmpuri în context estimativ sau real pentru **Timp** față de liniile de preț pentru rol de pe lista de prețuri. Această potrivire presupune că utilizați parametrii de preț out-of-box pentru tarifele facturilor. Dacă ați configurat prețul astfel încât să se bazeze pe alte câmpuri decât sau în plus față de **Rol**, **de resurse**, și **Unitatea de Resurse**, acea combinație de câmpuri este utilizată pentru a prelua o linie de preț pentru rol potrivită.
1. Dacă sistemul găsește o linie de preț pentru rol care are o rată de facturare pentru **Rol**, **de resurse**, și **Unitatea de Resurse** combinație, acea rată a facturii este utilizată ca rată implicită a facturii.

> [!NOTE]
> Dacă configurați o altă prioritizare a **Rol**, **de resurse**, și **Unitatea de Resurse** câmpuri sau dacă aveți alte dimensiuni care au prioritate mai mare, comportamentul precedent se va modifica în consecință. Sistemul preia înregistrările prețului rolului care au valori care se potrivesc cu fiecare valoare a dimensiunii de preț în ordinea priorității. Rândurile care au valori nule pentru acele dimensiuni vin ultimele.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinarea ratelor de vânzare pe liniile reale și estimative pentru Cheltuieli

Estimați contextul pentru **Cheltuiala** se refera la:

- Cotați detaliile liniei pentru **Cheltuiala**.
- Detalii linie contract pentru **Cheltuiala**.
- Linii de estimare a cheltuielilor pe un proiect.

Contextul real pentru **Cheltuiala** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Cheltuiala**.
- Liniile de jurnal care sunt create atunci când este trimisă o înregistrare de cheltuieli.
- Detaliile liniei de factură pentru **Cheltuiala**. 

După ce se stabilește o listă de prețuri pentru vânzări, sistemul parcurge următorii pași pentru a introduce prețul unitar de vânzare implicit.

1. Sistemul se potrivește cu combinația dintre **Categorie** și **Unitate** câmpurile de pe linia de estimare pentru **Cheltuiala** față de liniile de preț de categorie din lista de prețuri.
1. Dacă sistemul găsește o linie de preț de categorie care are o rată de vânzare pentru **Categorie** și **Unitate** combinație, acea rată de vânzări este utilizată ca rată implicită de vânzări.
1. Dacă sistemul găsește o linie de preț de categorie potrivită, metoda de stabilire a prețului poate fi utilizată pentru a introduce prețul de vânzare implicit. Următorul tabel arată comportamentul implicit pentru prețurile de cheltuieli în Operațiuni de proiect.

    | Context | Metodă de stabilire a prețului | Preț implicit |
    | --- | --- | --- |
    | Estimată | Preț unitar | Pe baza liniei de preț de categorie. |
    |        | La cost | 0.00 |
    |        | Adaos peste cost | 0.00 |
    | Real | Preț unitar | Pe baza liniei de preț de categorie. |
    |        | La cost | Pe baza costului real aferent. |
    |        | Adaos peste cost | Se aplică o majorare, așa cum este definită de linia prețului categoriei, ratei de cost unitar a costului real aferent. |

1. Dacă sistemul nu poate să se potrivească cu **Categorie** și **Unitate** valori, rata de vânzări este setată la **0** (zero) implicit.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinarea ratelor de vânzare pe liniile reale și estimative pentru Material

Estimați contextul pentru **Material** se refera la:

- Cotați detaliile liniei pentru **Material**.
- Detalii linie contract pentru **Material**.
- Linii de estimare a materialului pe un proiect.

Contextul real pentru **Material** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Material**.
- Liniile de jurnal care sunt create atunci când este trimis un jurnal de utilizare a materialelor.
- Detaliile liniei de factură pentru **Material**. 

După ce se stabilește o listă de prețuri pentru vânzări, sistemul parcurge următorii pași pentru a introduce prețul unitar de vânzare implicit.

1. Sistemul se potrivește cu combinația dintre **Produs** și **Unitate** câmpurile de pe linia de estimare pentru **Material** față de liniile de articole din lista de prețuri din lista de prețuri.
1. Dacă sistemul găsește o linie de articol din lista de prețuri care are o rată de vânzare pentru **Produs** și **Unitate** combinație și dacă metoda de stabilire a prețului este **Suma valutară**, se folosește prețul de vânzare care este specificat pe rândul listei de prețuri. 
1. Dacă **Produs** și **Unitate** valorile câmpurilor nu se potrivesc sau dacă metoda de stabilire a prețului este altceva decât **Suma valutară**, rata de vânzări este setată la **0** (zero) implicit. Acest comportament apare deoarece Project Operations acceptă numai **Suma valutară** metoda de stabilire a prețurilor pentru materialele care sunt utilizate într-un proiect.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
