---
title: Configurarea listei de prețuri de vânzări
description: Acest subiect oferă informații despre listele de prețuri de vânzări pentru prețuri de proiect.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896476"
---
# <a name="sales-price-list-setup"></a>Configurarea listei de prețuri de vânzări

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
