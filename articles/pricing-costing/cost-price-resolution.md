---
title: Rezolvarea prețurilor de cost pentru estimări și date reale
description: Acest subiect oferă informații despre modul în care sunt rezolvate prețurile de cost pentru estimări și realități.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d3422ef2eacc1e0617e60d41b7ddbcefe44d5b90
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082658"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Rezolvarea prețurilor de cost pentru estimări și date reale

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a rezolva prețurile de cost și lista de prețuri de cost pentru estimări și date reale, sistemul folosește informațiile din câmpurile **Date** , **Monedă** și **Unitate Contractantă** ale proiectului aferent. După ce lista de prețuri a fost rezolvată, aplicația rezolvă rata de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rezolvarea ratelor de cost pe liniile reale și estimate pentru Timp

Liniile de estimare pentru Timp se referă la detaliile de ofertă și de linie de contract pentru atribuirea timpului și a resurselor unui proiect.

După rezolvarea unei liste de prețuri de cost, sistemul utilizează câmpurile **Rol** , **Firmă de resurse** și **Unitate de resurse** de pe linia estimativă pentru Timp pentru a se potrivi cu liniile de preț de rol din lista de prețuri. Această potrivire presupune că utilizați dimensiuni de stabilire a prețurilor predefinite pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi câmpurilor în loc de sau în plus față de **Rol** , **Firmă de resurse** și **Unitate de resurse** , atunci va fi utilizată o combinație diferită pentru a regăsi o linie de preț de rol potrivită. Dacă aplicația găsește o linie de preț de rol care are o rată de cost pentru combinația **Rol** , **Firmă de resurse** și **Unitate de resurse** , aceasta este rata implicită a costurilor. Dacă aplicația nu se potrivește cu **Rol** , **Firmă de resurse** și **Unitate de resurse** , atunci aceasta recuperează liniile de preț ale rolului cu un rol de potrivire, dar valori nule ale **Unitate de resurse**. După ce are o înregistrare de prețuri de rol potrivită, rata de cost este implicită din înregistrarea respectivă. 

> [!NOTE]
> Dacă configurați o prioritate diferită de **Rol** , **Firmă de resurse** și **Unitate de resurse** , sau dacă aveți alte dimensiuni care au prioritate mai mare, acest comportament se va schimba în consecință. Sistemul preia înregistrările prețurilor rolurilor cu valori care se potrivesc fiecăreia dintre valorile parametrilor de stabilire a prețurilor în ordinea priorității, cu rânduri care au valori nule pentru dimensiunile din urmă.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rezolvarea ratelor de cost pe liniile reale și estimate pentru Cheltuială

Liniile de estimare pentru Cheltuială se referă la detaliile de ofertă și de linie de contract pentru cheltuieli și liniile de estimare a cheltuielilor unui proiect.

După rezolvarea unei liste de prețuri de cost, sistemul utilizează o combinație de câmpuri **Categorie** și **Unitate** de pe linia de estimare pentru ca o cheltuială să se potrivească cu liniile **Preț de categorie** din lista de prețuri rezolvate. Dacă sistemul găsește o linie de preț de categorie care are o rată de cost pentru combinația de câmp **Categorie** și **Unitate** , rata de cost este implicită. Dacă sistemul nu se potrivește cu valorile **Categorie** și **Unitate** sau dacă este capabil să găsească o linie de preț de categorie potrivită, dar metoda de stabilire a prețurilor nu este **Preț pe unitate** , rata de cost trece implicit la zero (0).
