---
title: Determinați ratele de cost pentru estimările și valorile reale bazate pe proiecte
description: Acest articol oferă informații despre modul în care sunt determinate ratele de cost pentru estimările și valorile reale bazate pe proiecte.
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
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Determinați ratele de cost pentru estimările și valorile reale bazate pe proiecte

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a determina prețurile de cost pe estimări și valori reale în Microsoft Dynamics 365 Project Operations, sistemul utilizează mai întâi data și moneda în estimarea primită sau contextul real pentru a determina lista de prețuri de vânzare. În contextul actual, în mod specific, sistemul utilizează **Data tranzacției** câmp pentru a determina care listă de prețuri este aplicabilă. The **Data tranzacției** valoarea estimată sau reală primită este comparată cu **Pornire efectivă (independent de fus orar)** și **Sfârșit efectiv (independent de fusul orar)** valorile de pe lista de preturi. După ce lista de prețuri de cost este determinată, sistemul determină rata de cost.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinarea ratelor de cost în contexte estimative și reale pentru Timp

Estimați contextul pentru **Timp** se refera la:

- Cotați detaliile liniei pentru **Timp**.
- Detalii linie contract pentru **Timp**.
- Atribuții de resurse pentru un proiect.

Contextul real pentru **Timp** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Timp**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de timp.

După ce se stabilește o listă de prețuri de cost, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul se potrivește cu combinația dintre **Rol**, **de resurse**, și **Unitatea de Resurse** câmpuri în context estimativ sau real pentru **Timp** față de liniile de preț pentru rol de pe lista de prețuri. Această potrivire presupune că utilizați dimensiunile standard de preț pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi cu alte câmpuri decât sau în plus față de **Rol**, **de resurse** și **Unitatea de Resurse**, o combinație diferită este utilizată pentru a prelua o linie de preț cu rol potrivit.
1. Dacă sistemul găsește o linie de preț pentru rol care are o rată de cost pentru **Rol**, **de resurse**, și **Unitatea de Resurse** combinație, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate să se potrivească cu **Rol**, **de resurse**, și **Unitatea de Resurse** valori, renunță la dimensiunea care are cea mai scăzută prioritate, caută linii de preț pentru rol care au potriviri pentru celelalte două valori ale dimensiunii și continuă să renunțe treptat la dimensiuni până când este găsit un rând de preț pentru rol care se potrivește. Rata de cost din acea înregistrare va fi utilizată ca rată de cost implicită. Dacă sistemul nu găsește un rând de preț pentru rol potrivit, prețul va fi setat la **0** (zero) implicit.

> [!NOTE]
> Dacă configurați o altă prioritizare a **Rol** și **Unitatea de Resurse** câmpuri sau dacă aveți alte dimensiuni care au prioritate mai mare, comportamentul precedent se va modifica în consecință. Sistemul preia înregistrările prețului rolului care au valori care se potrivesc cu fiecare valoare a dimensiunii de preț în ordinea priorității. Rândurile care au valori nule pentru acele dimensiuni vin ultimele.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinarea ratelor de cost pe liniile reale și estimative pentru Cheltuieli

Estimați contextul pentru **Cheltuiala** se refera la:

- Cotați detaliile liniei pentru **Cheltuiala**.
- Detalii linie contract pentru **Cheltuiala**.
- Estimări de cheltuieli pentru un proiect.

Contextul real pentru **Cheltuiala** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Cheltuiala**.
- Liniile de jurnal care sunt create atunci când este trimisă o înregistrare de cheltuieli.

După ce se stabilește o listă de prețuri de cost, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul se potrivește cu combinația dintre **Categorie** și **Unitate** câmpuri în context estimativ sau real pentru **Cheltuiala** față de liniile de preț de categorie din lista de prețuri.
1. Dacă sistemul găsește o linie de preț de categorie care are o rată de cost pentru **Categorie** și **Unitate** combinație, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate să se potrivească cu **Categorie** și **Unitate** valori, prețul este setat la **0** (zero) implicit.
1. În contextul estimării, dacă sistemul poate găsi o linie de preț de categorie potrivită, dar metoda de stabilire a prețului este altceva decât **Preț pe unitate**, rata de cost este setată la **0** (zero) implicit.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinarea ratelor de cost pe liniile reale și estimative pentru Material

Estimați contextul pentru **Material** se refera la:

- Cotați detaliile liniei pentru **Material**.
- Detalii linie contract pentru **Material**.
- Estimări materiale pentru un proiect.

Contextul real pentru **Material** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Material**.
- Liniile de jurnal care sunt create atunci când este trimis un jurnal de utilizare a materialelor.

După ce se stabilește o listă de prețuri de cost, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul folosește combinația dintre **Produs** și **Unitate** câmpuri în context estimativ sau real pentru **Material** față de liniile de articole din lista de prețuri din lista de prețuri.
1. Dacă sistemul găsește o linie de articol din lista de prețuri care are o rată de cost pentru **Produs** și **Unitate** combinație, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate să se potrivească cu **Produs** și **Unitate** valori, costul unitar este setat la **0** (zero) implicit.
1. În contextul estimativ sau real, dacă sistemul poate găsi o linie de articole din lista de prețuri care se potrivește, dar metoda de stabilire a prețurilor este altceva decât **Suma valutară**, costul unitar este setat la **0** în mod implicit. Acest comportament apare deoarece Project Operations acceptă numai **Suma valutară** metoda de stabilire a prețurilor pentru materialele care sunt utilizate într-un proiect.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
