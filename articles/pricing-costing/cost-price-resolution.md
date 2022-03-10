---
title: Rezolvarea prețurilor de cost pentru estimări și date reale
description: Acest subiect oferă informații despre modul în care sunt rezolvate prețurile de cost pentru estimări și realități.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003696"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Rezolvarea prețurilor de cost pentru estimări și date reale

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Pentru a rezolva prețurile de cost și lista de prețuri de cost pentru estimări și date reale, sistemul folosește informațiile din câmpurile **Date**, **Monedă** și **Unitate Contractantă** ale proiectului aferent. După ce lista de prețuri a fost rezolvată, aplicația rezolvă rata de cost.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rezolvarea ratelor de cost pe liniile reale și estimate pentru Timp

Liniile de estimare pentru Timp se referă la detaliile de ofertă și de linie de contract pentru atribuirea timpului și a resurselor unui proiect.

După rezolvarea unei liste de prețuri de cost, sistemul utilizează câmpurile **Rol**, **Firmă de resurse** și **Unitate de resurse** de pe linia estimativă pentru Timp pentru a se potrivi cu liniile de preț de rol din lista de prețuri. Această potrivire presupune că utilizați dimensiuni de stabilire a prețurilor predefinite pentru costul forței de muncă. Dacă ați configurat sistemul pentru a se potrivi câmpurilor în loc de sau în plus față de **Rol**, **Firmă de resurse** și **Unitate de resurse**, atunci va fi utilizată o combinație diferită pentru a regăsi o linie de preț de rol potrivită. Dacă aplicația găsește o linie de preț de rol care are o rată de cost pentru combinația **Rol**, **Firmă de resurse** și **Unitate de resurse**, aceasta este rata implicită a costurilor. Dacă aplicația nu se potrivește exact cu combinația de **Rol**, **Companie de resurse** și **Unitate de resurse**, va prelua liniile de preț ale rolului cu o valoare de rol potrivită, dar are valori nule pentru **Unitate de resurse** și **Companie de resurse**. După potrivirea unei înregistrări a prețului de rol cu valoarea prețului de rol aferent, rata de cost primește valoarea implicită din înregistrarea respectivă. 

> [!NOTE]
> Dacă configurați o prioritate diferită de **Rol**, **Firmă de resurse** și **Unitate de resurse**, sau dacă aveți alte dimensiuni care au prioritate mai mare, acest comportament se va schimba în consecință. Sistemul preia înregistrările prețurilor de rol cu valori care se potrivesc fiecăreia dintre valorile dimensiunilor de stabilire a prețurilor în ordine de prioritate cu rânduri care au valori nule pentru dimensiunile care sunt ultimele în ordinea priorității.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rezolvarea ratelor de cost pe liniile reale și estimate pentru Cheltuială

Liniile de estimare pentru Cheltuială se referă la detaliile de ofertă și de linie de contract pentru cheltuieli și liniile de estimare a cheltuielilor unui proiect.

După rezolvarea unei liste de prețuri de cost, sistemul utilizează o combinație de câmpuri **Categorie** și **Unitate** de pe linia de estimare pentru ca o cheltuială să se potrivească cu liniile **Preț de categorie** din lista de prețuri rezolvate. Dacă sistemul găsește o linie de preț de categorie care are o rată de cost pentru combinația de câmp **Categorie** și **Unitate**, rata de cost este implicită. Dacă sistemul nu se potrivește cu valorile **Categorie** și **Unitate** sau dacă este capabil să găsească o linie de preț de categorie potrivită, dar metoda de stabilire a prețurilor nu este **Preț pe unitate**, rata de cost trece implicit la zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rezolvarea ratelor de costuri pe liniile reale și estimate pentru material

Liniile de estimare pentru materiale se referă la detaliile liniei de ofertă și a liniei de contract pentru materiale și la liniile de estimare pentru un proiect.

După rezolvarea unei liste de prețuri de cost, sistemul folosește o combinație a câmpurilor **Produs** și **Unitate** de pe linia de estimare pentru o estimare a materialelor, de potrivit cu liniile **Articole din lista de prețuri** din lista de prețuri rezolvate. Dacă sistemul găsește o linie de preț de produs care are o rată de cost pentru combinația de câmpuri **Produs** și **Unitate**, rata de cost revine la valoarea implicită. Dacă sistemul nu poate asocia valorile **Produs** și **Unitate**, costum unitar capătă valoarea implicită zero. Această valoare implicită se va întâmpla și dacă există o linie aferentă de articole din lista de prețuri, dar metoda de stabilire a prețurilor se bazează pe un cost standard sau cost curent care nu este definit în produs.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
