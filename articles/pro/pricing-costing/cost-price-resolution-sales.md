---
title: Determinați ratele de cost pentru estimările și efectivele de proiect
description: Acest articol oferă informații despre modul în care sunt determinate ratele de cost pentru estimările și efectivele de proiect.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410174"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Determinați ratele de cost pentru estimările și efectivele de proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Pentru a determina lista de prețuri de cost și ratele de cost în contexte estimative și reale, sistemul utilizează informațiile din **Data**, **·**, și **Unitatea de Contractare** domeniile proiectului aferent.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinarea ratelor de cost în contexte estimative și reale pentru Timp

Estimați contextul pentru **Timp** se refera la:

- Cotați detaliile liniei pentru **Timp**.
- Detalii linie contract pentru **Timp**.
- Atribuții de resurse pentru un proiect.

Contextul real pentru **Timp** se refera la:

- Liniile jurnalului de intrare și corecție pentru **Timp**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de timp.

După ce se stabilește o listă de prețuri de cost, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul se potrivește cu combinația dintre **Rol** și **Unitatea de Resurse** câmpuri în contextul estimativ sau real pentru **Timp** față de liniile de preț pentru rol de pe lista de prețuri. Această potrivire presupune că utilizați dimensiunile standard de preț pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi cu alte câmpuri decât sau în plus față de **Rol** și **Unitatea de Resurse**, o combinație diferită este utilizată pentru a prelua o linie de preț cu rol potrivit.
1. Dacă sistemul găsește o linie de preț pentru rol care are o rată de cost pentru **Rol** și **Unitatea de Resurse** combinație, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate să se potrivească cu **Rol** și **Unitatea de Resurse** valori, preia liniile de preț de rol care au valori care se potrivesc pentru **Rol** câmp dar valori nule pentru **Unitatea de Resurse** camp. După ce sistemul are o înregistrare de preț de rol care se potrivește, rata de cost din acea înregistrare va fi utilizată ca rată de cost implicită.

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

1. Sistemul se potrivește cu combinația dintre **Categorie** și **Unitate** câmpuri în contextul estimativ sau real pentru **Cheltuiala** față de liniile de preț de categorie din lista de prețuri.
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
1. În context estimativ sau real, dacă sistemul poate găsi o linie de articole din lista de prețuri care se potrivește, dar metoda de stabilire a prețurilor este altceva decât **Suma valutară**, costul unitar este setat la **0** în mod implicit. Acest comportament apare deoarece Project Operations acceptă numai **Suma valutară** metoda de stabilire a prețurilor pentru materialele care sunt utilizate într-un proiect.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
