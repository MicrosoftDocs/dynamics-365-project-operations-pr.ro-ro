---
title: Stabilirea prețurilor de vânzare pentru estimări și valori reale bazate pe proiect
description: Acest articol oferă informații despre cum sunt stabilite prețurile de vânzare pentru estimările și valorile reale bazate pe proiect.
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
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Stabilirea prețurilor de vânzare pentru estimări și valori reale bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a stabili prețurile de vânzare pentru estimări și valori reale în Microsoft Dynamics 365 Project Operations, sistemul folosește mai întâi data și moneda în estimarea primită sau contextul real pentru a stabili lista de prețuri de vânzare. În contextul actual, în mod specific, sistemul utilizează câmpul **Dată tranzacție** pentru a determina care listă de prețuri este aplicabilă. Valoarea **Dată tranzacție** a estimării sau a valorii reale primite este comparată cu valorile **De la: (independent de fusul orar)** și **Până la: (independent de fusul orar)** de pe lista de preturi. După ce lista de prețuri de vânzare este stabilită, sistemul stabilește rata de vânzare sau de facturare.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Stabilirea ratelor de vânzare pe liniile de valori reale și estimate pentru Timp

Contextul estimat pentru **Timp** se referă la:

- Detalii pentru linia de ofertă pentru **Timp**.
- Detalii pentru linia de contract pentru **Timp**.
- Atribuirile de resurse într-un proiect.

Contextul real pentru **Timp** se referă la:

- Liniile de jurnalul de intrare și corecție pentru **Timp**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de timp.
- Detalii pentru linia de facturare pentru **Timp**. 

După ce o listă de prețuri pentru vânzare este stabilită, sistemul parcurge următorii pași pentru a introduce rata de facturare implicită.

1. Sistemul potrivește câmpurile **Rol**, **Companie de resurse** și **Unitate de resurse** în contextul estimat sau real pentru **Timp** cu liniile de prețuri de rol în lista de prețuri. Această potrivire presupune că utilizați dimensiunile de stabilire a prețurilor predefinite pentru ratele de facturare. Dacă ați configurat prețurile astfel încât să se bazeze pe oricare alte câmpuri decât sau în plus față de câmpurile **Rol**, **Companie de resurse** și **Unitate de resurse**, atunci această combinație de câmpuri va fi utilizată pentru a regăsi o linie de preț de rol potrivită.
1. Dacă sistemul găsește o linie de preț de rol care are o rată de facturare pentru combinația de câmpuri **Rol**, **Companie de resurse** și **Unitate de resurse**, atunci acea rată de facturare este utilizată ca rată de facturare implicită.

> [!NOTE]
> Dacă configurați o prioritate diferită pentru câmpurile **Rol**, **Companie de resurse** și **Unitate de resurse** sau dacă aveți alte dimensiuni care au prioritate mai mare, acest comportament precedent se va schimba în consecință. Sistemul preia înregistrările prețului de rolul care au valori care se potrivesc cu fiecare valoare a dimensiunii de preț în ordinea priorității. Rândurile care au valori nule pentru acele dimensiuni vin ultimele.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Stabilirea ratelor de vânzare pe liniile de valori reale și estimate pentru Cheltuieli

Contextul estimat pentru **Cheltuieli** se referă la:

- Detalii pentru linia de ofertă pentru **Cheltuieli**.
- Detalii pentru linia de contract pentru **Cheltuieli**.
- Linii de estimări de cheltuieli într-un proiect.

Contextul real pentru **Cheltuieli** se referă la:

- Liniile de jurnal de intrare și corecție pentru **Cheltuieli**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de cheltuieli.
- Detalii pentru linia de facturare pentru **Cheltuieli**. 

După o listă de prețuri pentru vânzări este stabilită, sistemul parcurge următorii pași pentru a introduce prețul de vânzare pe unitate implicit.

1. Sistemul potrivește combinația de câmpuri **Categorie** și **Unitate** pe linia de estimare pentru **Cheltuieli** cu liniile de preț de categorie pe lista de prețuri.
1. Dacă sistemul găsește o linie de preț de categorie care are o rată de vânzare pentru combinația de câmpuri **Categorie** și **Unitate**, acea rată de vânzare este utilizată ca rată de vânzare implicită.
1. Dacă sistemul găsește o linie de preț de categorie potrivită, metoda de stabilire a prețurilor poate fi utilizată pentru a introduce prețul de vânzare implicit. Următorul tabel prezintă comportamentul implicit pentru prețurile de cheltuieli în Project Operations.

    | Context | Metodă de stabilire a prețului | Preț implicit |
    | --- | --- | --- |
    | Estimată | Preț unitar | Pe baza liniei de preț a categoriei. |
    |        | La cost | 0.00 |
    |        | Adaos peste cost | 0.00 |
    | Real | Preț unitar | Pe baza liniei de preț a categoriei. |
    |        | La cost | Pe baza costului real aferent. |
    |        | Adaos peste cost | Un adaos este aplicat așa cum este definit de linia de preț a categoriei la rata de cost unitară a costului real aferent. |

1. Dacă sistemul nu poate să potrivească valorile de câmp **Categorie** și **Unitate**, rata de vânzare este setată la **0** (zero) în mod implicit.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Stabilirea ratelor de vânzări pe liniile de valori reale și estimate pentru Materiale

Contextul estimat pentru **Materiale** se referă la:

- Detalii pentru linia de ofertă pentru **Materiale**.
- Detalii pentru linia de contract pentru **Materiale**.
- Linii de estimări de materiale într-un proiect.

Contextul real pentru **Materiale** se referă la:

- Liniile de jurnal de intrare și corecție pentru **Materiale**.
- Liniile de jurnal care sunt create atunci când este trimisă o înregistrare de utilizare de Materiale.
- Detalii pentru linia de facturare pentru **Materiale**. 

După o listă de prețuri pentru vânzări este stabilită, sistemul parcurge următorii pași pentru a introduce prețul de vânzare pe unitate implicit.

1. Sistemul potrivește combinația de câmpuri **Produs** și **Unitate** pe linia de estimări pentru **Materiale** cu liniile de articole din lista de prețuri pe lista de prețuri.
1. Dacă sistemul găsește o listă de articole din lista de prețuri care are o rată de vânzare pentru combinația de câmp **Produs** și **Unitate** și dacă metoda de stabilire a prețurilor este **Sumă valută**, se folosește prețul de vânzare specificat pe linia listei de prețuri. 
1. Dacă valorile câmpurilor **Produs** și **Unitate** nu se potrivesc sau dacă metoda de stabilire a prețului este alta decât **Sumă valută**, rata de vânzare este setată la **0** (zero) implicit. Acest comportament apare deoarece Project Operations acceptă numai metoda de stabilire a prețurilor **Sumă valutară** pentru materialele care sunt utilizate într-un proiect.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
