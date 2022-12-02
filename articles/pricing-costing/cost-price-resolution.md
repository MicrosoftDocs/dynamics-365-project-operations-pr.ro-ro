---
title: Stabilirea ratelor de cost pentru estimările și valorile reale bazate pe proiect
description: Acest articol oferă informații despre cum sunt stabilite ratele de cost pentru estimările și valorile reale bazate pe proiect.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475294"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Stabilirea ratelor de cost pentru estimările și valorile reale bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a stabili prețurile de cost pentru estimări și valori reale în Microsoft Dynamics 365 Project Operations, sistemul folosește mai întâi data și moneda în estimarea primită sau contextul real pentru a stabili lista de prețuri de vânzare. În contextul actual, în mod specific, sistemul utilizează câmpul **Dată tranzacție** pentru a determina care listă de prețuri este aplicabilă. Valoarea **Dată tranzacție** a estimării sau a valorii reale primite este comparată cu valorile **De la: (independent de fusul orar)** și **Până la: (independent de fusul orar)** de pe lista de preturi. După ce lista de prețuri a fost stabilită, sistemul stabilește rata de cost.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Stabilirea ratelor de cost în contextele estimate și reale pentru Timp

Contextul estimat pentru **Timp** se referă la:

- Detalii pentru linia de ofertă pentru **Timp**.
- Detalii pentru linia de contract pentru **Timp**.
- Atribuirile de resurse într-un proiect.

Contextul real pentru **Timp** se referă la:

- Liniile de jurnalul de intrare și corecție pentru **Timp**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de timp.

După ce o listă de prețuri de cost este stabilită, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul potrivește câmpurile **Rol**, **Companie de resurse** și **Unitate de resurse** în contextul estimat sau real pentru **Timp** cu liniile de prețuri de rol în lista de prețuri. Această potrivire presupune că utilizați dimensiunile standard de stabilire a prețurilor pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi unor câmpuri, altele sau în plus față de cele pentru **Rol**, **Companie de resurse** și **Unitate de resurse**, atunci se utilizează o combinație diferită pentru a regăsi o linie de preț de rol potrivită.
1. Dacă sistemul găsește o linie de preț de rol care are o rată de cost pentru combinația **Rol**, **Companie de resurse** și **Unitate de resurse**, rata de cost este utilizată ca rată implicită a costurilor.
1. Dacă sistemul nu poate să potrivească valorile **Rol**, **Companie de resurse** și **Unitate de Resurse**, renunță la dimensiunea care are cea mai scăzută prioritate, caută linii de preț de rol care au potriviri pentru celelalte două valori ale dimensiunii și continuă să renunțe treptat la dimensiuni până când este găsită o linie de preț de rol care se potrivește. Rata de cost din acea înregistrare va fi utilizată ca rată de cost implicită. Dacă sistemul nu găsește o linie de preț de rol potrivită, prețul va fi setat la **0** (zero) implicit.

> [!NOTE]
> Dacă configurați o prioritizare diferită de câmpurile **Rol** și **Unitate de resurse** sau dacă aveți alte dimensiuni care au prioritate mai mare, comportamentul precedent se va schimba ca atare. Sistemul preia înregistrările prețului de rolul care au valori care se potrivesc cu fiecare valoare a dimensiunii de preț în ordinea priorității. Rândurile care au valori nule pentru acele dimensiuni vin ultimele.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Stabilirea ratelor de cost pe liniile de valori reale și estimate pentru Cheltuieli

Contextul estimat pentru **Cheltuieli** se referă la:

- Detalii pentru linia de ofertă pentru **Cheltuieli**.
- Detalii pentru linia de contract pentru **Cheltuieli**.
- Estimări de cheltuieli într-un proiect

Contextul real pentru **Cheltuieli** se referă la:

- Liniile de jurnal de intrare și corecție pentru **Cheltuieli**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de cheltuieli.

După ce o listă de prețuri de cost este stabilită, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul potrivește combinația de câmpuri **Categorie** și **Unitate** în contextul estimat sau real pentru **Cheltuieli** cu liniile de prețuri de categorie în lista de prețuri.
1. Dacă sistemul găsește o linie de preț de categorie care are o rată de cost pentru combinația de câmp **Categorie** și **Unitate**, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate să potrivească valorile de câmp **Categorie** și **Unitate**, prețul este setat la **0** (zero) în mod implicit.
1. În contextul de estimare, dacă sistemul nu poate găsi o linie de preț de categorie potrivită, dar metoda de stabilire a prețurilor este alta decât **Preț pe unitate**, rata de cost este setată la **0** (zero) în mod implicit.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Stabilirea ratelor de cost pe liniile de valori reale și estimate pentru Materiale

Contextul estimat pentru **Materiale** se referă la:

- Detalii pentru linia de ofertă pentru **Materiale**.
- Detalii pentru linia de contract pentru **Materiale**.
- Estimări de materiale într-un proiect.

Contextul real pentru **Materiale** se referă la:

- Liniile de jurnal de intrare și corecție pentru **Materiale**.
- Liniile de jurnal care sunt create atunci când este trimisă o înregistrare de utilizare de Materiale.

După ce o listă de prețuri de cost este stabilită, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul utilizează combinația de câmpuri **Produs** și **Unitate** în contextul estimat sau real pentru **Materiale** cu liniile de articole din lista de prețuri în lista de prețuri
1. Dacă sistemul găsește o linie de articole din lista de prețuri care are o rată de cost pentru combinația de câmp **Produs** și **Unitate**, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate potrivi valorile **Produs** și **Unitate**, costul unitar este setat la **0** (zero) în mod implicit.
1. În contextul estimat sau real, dacă sistemul nu poate găsi o linie de articole din lista de prețuri potrivită, dar metoda de stabilire a prețurilor este alta decât **Sumă valutară**, costul unitar este setat la **0** în mod implicit. Acest comportament apare deoarece Project Operations acceptă numai metoda de stabilire a prețurilor **Sumă valutară** pentru materialele care sunt utilizate într-un proiect.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
