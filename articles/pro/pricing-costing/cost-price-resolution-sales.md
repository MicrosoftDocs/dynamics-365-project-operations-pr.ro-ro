---
title: Rezolvarea prețurilor de cost pentru estimări și date reale - simplificat
description: Acest subiect oferă informații despre modul în care sunt rezolvate prețurile de cost pe estimări și realități.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764609"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Rezolvarea prețurilor de cost pentru estimări și date reale - simplificat

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
