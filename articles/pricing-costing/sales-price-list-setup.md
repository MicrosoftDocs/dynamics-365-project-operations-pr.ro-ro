---
title: Configurarea unei liste de prețuri pentru vânzare
description: Acest subiect oferă informații despre listele de prețuri de vânzări pentru prețuri de proiect.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 952d518fb58b5be46c4b1cf4ed57b2494fdfdad85e7fe6fb0d622367bc071b5f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997621"
---
# <a name="set-up-a-sales-price-list"></a>Configurarea unei liste de prețuri pentru vânzare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pentru ofertele și contractele de proiect, o listă de prețuri de proiect are un alt model de suprascriere a prețului decât o listă de prețuri de produs. Pe o linie de ofertă bazată pe catalogul de produse, aveți posibilitatea să suprascrieți prețul la roluri și categorii direct pe linia de ofertă, deoarece fiecare linie de ofertă indică exact un element de catalog. Cu toate acestea, pe o linie de ofertă bazată pe proiect, nu puteți suprascrie prețul la roluri și categorii direct pe linia de ofertă. Puteți utiliza lista de prețuri a proiectului pentru a lucra cu cele două modele de suprascriere distincte.

> [!NOTE]
> Vă recomandăm să aveți o listă de prețuri separată pentru resursele proiectului și elementele de catalog, din cauza diferențelor de comportament între cele două atunci când suprascrieți tarifarea.

Fiecare dintre următoarele entități poate avea una sau mai multe liste de prețuri de vânzare asociate pentru tarifarea de proiect:

- (Cont) client 
- Oportunitate 
- Ofertă 
- Contract de proiect

Asocierea acestor entități cu o listă de prețuri este indicată de listele de prețuri ale proiectului. Aveți posibilitatea să asociați una sau mai multe liste de prețuri cu entitățile de vânzări Client, Oportunitate, Ofertă și Contract de proiect.

O listă de prețuri implicită a proiectului nu este introdusă automat într-o înregistrare de client. Cu toate acestea, aveți posibilitatea să atașați manual o listă de prețuri de proiect la înregistrarea clientului. Totuși, ar trebui să atașați manual o listă de prețuri de proiect numai atunci când aveți un acord de tarifare particularizat cu clientul. 

Atunci când o listă de prețuri de proiect este atașată la o entitate de vânzări, următoarele informații sunt validate:

- Lista de prețuri are un context de **Vânzări**. 
- Moneda listei de prețuri corespunde monedei clientului. 

Pe un contract de proiect, este utilizată următoarea ordine de prioritate pentru a seta automat liste de proiect corelate:

1. Ofertă
2. Oportunitate
3. Client 
4. Setări globale 

Atunci când o listă de prețuri de proiect este introdusă în mod implicit, sistemul validează că moneda se potrivește cu moneda clientului și că listele de prețuri implicite care au fost introduse au un context de **Vânzări**.

Aveți posibilitatea să asociați mai multe liste de prețuri cu entitățile Client, Oportunitate, Ofertă și Contract de proiect. Această capacitate acceptă prețuri implicite specifice datei pentru un contract de proiect de lungă durată, în cazul căruia este posibil să aveți nevoie de mai mult de o listă de prețuri pentru a ține cont de actualizările de preț care au loc din cauza inflației. Cu toate acestea, în cazul în care listele de prețuri pe care le asociați cu entitatea Client, Oportunitate, Ofertă sau Contract de proiect au o suprapunere a efectivității datelor, prețurile implicite ar putea fi incorecte. De aceea, ar trebui să vă asigurați că listele de prețuri de proiect care au o suprapunere a efectivității datelor nu sunt asociate cu aceste entități.


[!INCLUDE[footer-include](../includes/footer-banner.md)]