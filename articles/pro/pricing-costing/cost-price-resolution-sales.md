---
title: Rezolvarea prețurilor de cost pentru estimări de proiect și date reale
description: Acest subiect oferă informații despre cum sunt rezolvate prețurile de cost pe estimările și valorile reale ale proiectului.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9f20631f41c560f1a4047aaaa624fa4e8651c687
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877280"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Rezolvarea prețurilor de cost pentru estimări de proiect și date reale 

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Pentru a rezolva prețurile de cost și lista de prețuri de cost pentru estimări și date reale, sistemul folosește informațiile din câmpurile **Date**, **Monedă** și **Unitate Contractantă** ale proiectului aferent. După ce lista de prețuri a fost rezolvată, aplicația rezolvă rata de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rezolvarea ratelor de cost pe liniile reale și estimate pentru Timp

Liniile de estimare pentru Timp se referă la detaliile de ofertă și de linie de contract pentru atribuirea timpului și a resurselor unui proiect.

După rezolvarea unei liste de prețuri, câmpurile **Rol** și **Unitate de resurse** de pe linia de estimare pentru Timp sunt potrivite cu liniile de preț pe rol din lista de prețuri. Această potrivire presupune că utilizați dimensiunile standard de stabilire a prețurilor pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi câmpurilor în loc de sau în plus față de **Rol** și **Unitate de resurse**, atunci va fi utilizată o combinație diferită pentru a regăsi o linie de preț de rol potrivită. Dacă aplicația găsește o linie de preț de rol care are o rată de cost pentru combinația **Rol** și **Unitate de resurse**, aceasta este rata implicită a costurilor. Dacă aplicația nu se potrivește cu **Rol** și **Unitate de resurse**, atunci aceasta recuperează liniile de preț ale rolului cu un rol de potrivire, dar valori nule ale **Unitate de resurse**. După ce are o înregistrare de prețuri de rol potrivită, rata de cost este implicită din înregistrarea respectivă. 

> [!NOTE]
> Dacă configurați o prioritate diferită de **Rol** și **Unitate de resurse**, sau dacă aveți alte dimensiuni care au prioritate mai mare, acest comportament se va schimba în consecință. Sistemul preia înregistrările prețurilor rolurilor cu valori care se potrivesc fiecăreia dintre valorile parametrilor de stabilire a prețurilor în ordinea priorității, cu rânduri care au valori nule pentru dimensiunile din urmă.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rezolvarea ratelor de cost pe liniile reale și estimate pentru Cheltuială

Liniile de estimare pentru Cheltuială se referă la detaliile de ofertă și de linie de contract pentru cheltuieli și liniile de estimare a cheltuielilor unui proiect.

După rezolvarea unei liste de prețuri de cost, sistemul folosește o combinație a câmpurilor **Categorie** și **Unitate** de pe linia de estimare a cheltuielilor pentru a se potrivi cu liniile **Preț categorie** din lista de prețuri rezolvate. Dacă sistemul găsește o linie de preț de categorie care are o rată de cost pentru combinația de câmp **Categorie** și **Unitate**, rata de cost este implicită. Dacă sistemul nu poate realiza potrivirea dintre valorile **Categorie** și **Unitate** sau dacă poate găsi o linie de preț de categorie potrivită, dar metoda de stabilire a prețurilor nu este **Preț pe unitate**, rata de cost este setată implicit la zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rezolvarea ratelor de costuri pe liniile de valori reale și estimate pentru Materiale

Liniile de estimare pentru Materiale se referă la detaliile liniei de ofertă și a liniei de contract pentru materiale și la liniile de estimare pentru un proiect.

După rezolvarea unei liste de prețuri de cost, sistemul folosește o combinație a câmpurilor **Produs** și **Unitate** de pe linia de estimare pentru o estimare a materialelor, de potrivit cu liniile **Articole din lista de prețuri** din lista de prețuri rezolvate. Dacă sistemul găsește o linie de preț de produs care are o rată de cost pentru combinația de câmpuri **Produs** și **Unitate**, rata de cost revine la valoarea implicită. Dacă sistemul nu se potrivește cu valorile de **Produs** și **Unitate**, sau dacă poate să găsească o listă de articole corespunzătoare din lista de prețuri, dar metoda de stabilire a prețurilor se bazează pe Cost standard sau Cost curent și niciuna dintre acestea nu este definită pe produs, costul unitar primește valoarea implicită zero.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
