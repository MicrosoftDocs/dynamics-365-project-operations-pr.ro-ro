---
title: Stabilirea ratelor de cost pentru estimări și valori reale de proiect
description: Acest articol oferă informații despre cum sunt stabilite ratele de cost pentru estimările și valorile reale pe proiect.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475251"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Stabilirea ratelor de cost pentru estimări și valori reale de proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Pentru a stabili ratele de cost pentru estimări și valori reale în Microsoft Dynamics 365 Project Operations, sistemul folosește mai întâi data și moneda în estimarea primită sau contextul real pentru a stabili lista de prețuri de cost. În contextul actual, în mod specific, sistemul utilizează câmpul **Dată tranzacție** pentru a determina care listă de prețuri este aplicabilă. Valoarea **Dată tranzacție** a estimării sau a valorii reale primite este comparată cu valorile **De la: (independent de fusul orar)** și **Până la: (independent de fusul orar)** de pe lista de preturi. După ce lista de prețuri de cost a fost stabilită, sistemul stabilește rata de cost. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Stabilirea ratelor de cost în contextele estimate și reale pentru Timp

Contextul estimat pentru **Timp** se referă la:

- Detalii pentru linia de ofertă pentru **Timp**.
- Detalii pentru linia de contract pentru **Timp**.
- Atribuirile de resurse într-un proiect.

Contextul real pentru **Timp** se referă la:

- Liniile de jurnalul de intrare și corecție pentru **Timp**.
- Liniile de jurnal care sunt create atunci când este trimisă o intrare de timp.

După ce o listă de prețuri de cost este stabilită, sistemul parcurge următorii pași pentru a introduce rata de cost implicită.

1. Sistemul potrivește combinația de câmpuri **Rol** și **Unitate de resurse** în contextul estimat sau real pentru **Timp** cu liniile de prețuri de rol în lista de prețuri. Această potrivire presupune că utilizați dimensiunile standard de stabilire a prețurilor pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi altor câmpuri decât sau în plus față de câmpurile **Rol** și **Unitate de resurse**, o combinație diferită este utilizată pentru a regăsi o linie de preț de rol potrivită.
1. Dacă sistemul găsește o linie de preț de rol care are o rată de cost pentru combinația **Rol** și **Unitate de resurse**, acea rată de cost este utilizată ca rată de cost implicită.
1. Dacă sistemul nu poate să potrivească valorile de câmp **Rol** și **Unitate de resurse**, acesta regăsește linii de preț de rol care au valori care se potrivesc câmpului **Rol** însă care sunt nule pentru câmpul **Unitate de resurse**. După ce sistemul are o înregistrare de preț de rol potrivită, rata de cost din acea înregistrare va fi utilizată ca rată de cost implicită.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
