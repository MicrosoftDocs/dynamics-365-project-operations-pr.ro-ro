---
title: Determinați prețurile de vânzare pentru estimările și realizările proiectului
description: Acest articol oferă informații despre modul în care sunt determinate prețurile de vânzare pentru estimările de proiect și efectivele.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410134"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Determinați prețurile de vânzare pentru estimările și realizările proiectului

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Pentru a determina prețurile de vânzare pe estimări și valori reale în Microsoft Dynamics 365 Project Operations, sistemul utilizează mai întâi data și moneda în estimarea primită sau contextul real pentru a determina lista de prețuri de vânzare. În contextul actual, în mod specific, sistemul utilizează **Data tranzacției** câmp pentru a determina care listă de prețuri este aplicabilă. După ce lista de prețuri de vânzare este determinată, sistemul determină rata de vânzare sau de facturare.

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

1. Sistemul se potrivește cu combinația dintre **Rol** și **Unitatea de Resurse** câmpuri în contextul estimativ sau real pentru **Timp** față de liniile de preț pentru rol de pe lista de prețuri. Această potrivire presupune că utilizați parametrii de preț out-of-box pentru tarifele facturilor. Dacă ați configurat prețul astfel încât să se bazeze pe alte câmpuri decât sau în plus față de **Rol** și **Unitatea de Resurse**, acea combinație de câmpuri este utilizată pentru a prelua o linie de preț pentru rol potrivită.
1. Dacă sistemul găsește o linie de preț pentru rol care are o rată de facturare pentru **Rol** și **Unitatea de Resurse** combinație, acea rată a facturii este utilizată ca rată implicită a facturii.
1. Dacă sistemul nu poate să se potrivească cu **Rol** și **Unitatea de Resurse** valori, preia liniile de preț de rol care au valori care se potrivesc pentru **Rol** câmp dar valori nule pentru **Unitatea de resurse** camp. După ce sistemul găsește o înregistrare a prețului rolului care se potrivește, rata de facturare din acea înregistrare va fi utilizată ca rată implicită de facturare. Această potrivire presupune o configurație out-of-box pentru prioritatea relativă a **Rol** impotriva **Unitatea de Resurse** ca dimensiune a prețului de vânzare.

> [!NOTE]
> Dacă configurați o altă prioritizare a **Rol** și **Unitatea de Resurse** câmpuri sau dacă aveți alte dimensiuni care au prioritate mai mare, comportamentul precedent se va modifica în consecință. Sistemul preia înregistrările prețului rolului care au valori care se potrivesc cu fiecare valoare a dimensiunii de preț în ordinea priorității. Rândurile care au valori nule pentru acele dimensiuni vin ultimele.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
