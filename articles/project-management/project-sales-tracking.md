---
title: Urmărire vânzări pe proiect
description: Acest subiect oferă informații despre modul în care Project Operations urmărește progresul în raport cu venitul forței de muncă pentru un proiect.
author: rumant
manager: AnnBe
ms.date: 03/24/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 438c44dcfaf9677075eb07688c1e65c6e7053755
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711079"
---
# <a name="project-sales-tracking"></a>Urmărire vânzări pe proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations urmărește estimările forței de muncă și veniturile la cea mai mică granularitate necesară pentru un plan de proiect. Estimarea venitului forței de muncă se bazează pe efortul planificat și pe resursele generice sau denumite care sunt alocate fiecărei sarcini nod frunză din planul de proiect. Când începe proiectul și oamenii încep să raporteze timpul asupra diferitelor sarcini ale proiectului, se rezumă venitul real cu forța de muncă care începe un calcul al proiecțiilor.

## <a name="labor-revenue-tracking-view"></a>Vizualizare urmărire venit forță de muncă

Pe pagina **Proiecte**, pe fila **Urmărire**, puteți selecta **Urmărire** > **Cost** pentru a deschide vizualizarea **Urmărirea costurilor**. Sau, puteți selecta **Utilizare** > **Rata facturii** pentru a deschide vizualizarea **Urmărirea veniturilor**, care arată progresul veniturilor din muncă pe fiecare sarcină din planul de proiect. Această viziualizare compară, de asemenea, venitul real al forței de muncă cheltuit pentru o sarcină cu venitul forței de muncă planificat al activității. Project Operations utilizează următoarele formule pentru a calcula valorile venitului forței de muncă:

- **Venit planificat**: valorile de vânzare estimat al tuturor atribuirilor de resurse pentru fiecare activitate de nod frunză
- **Venitul actual**: Suma tuturor vânzărilor netarifate reale pentru timpul înregistrat în sarcină
- **Procent venituri facturabile**: Venit real ÷ Estimarea veniturilor la final
- **Venit rămas**: venit estimat la final - venit real
- **Venit estimat la final**: venit rămas + venit real
- **Varianță de venit**: venit planificat – venit estimat la final


> [!NOTE]
> Project Operations arată doar veniturile forței de muncă pe pagina **Proiect** pe fila **Urmărire**. În timp ce materialele și cheltuielile pot fi estimate și urmărite pentru consum, aceste venituri nu sunt incluse în venituri indicate pe fila **Urmărire**. Această filă este concepută să funcționeze numai pentru reproiectarea veniturilor forței de muncă prin reproiectarea efortului.  
> Toate veniturile afișate sunt convertite în moneda de cost a proiectului. Moneda de cost a proiectului este moneda unității contractante din proiect. Pentru proiectele cu preț fix, numerele de venituri pe vizualizarea **Urmărirea veniturilor din muncă** nu este relevantă, deoarece efectele vânzărilor nefacturate nu sunt înregistrate la aprobarea timpului.
> Valorile estimate ale vânzărilor pentru timp care sunt afișate pe fila **Estimare** a proiectului nu se poate adăuga la valoarea veniturilor planificate pe fila **Urmărire**. Sursa acestei discrepanțe se datorează a două motive posibile:
><ol>
   ><li> Fila <b>Estimări</b> arată veniturile estimate în moneda de vânzări, în timp ce fila <b>Urmărire</b> arată veniturile planificate convertite în moneda de cost. </li>
   ><li> Atunci când vânzările estimate sunt convertite în moneda contractului, după cum se arată în fila <b>Estimări</b>, în moneda proiectului, conversia implică pași care ar putea duce la o anumită pierdere de precizie: </li>
><ol>
><li> Suma estimată a vânzărilor în moneda contractului este mai întâi convertită în moneda de bază (conversia 1).</li>
><li> Suma estimată a vânzărilor în moneda de bază este convertită în moneda costului de proiect (conversia 2). </li>
></ol>
></ol>
> Precizia monedei se aplică în ambii pași, ceea ce duce la o deviere a veniturilor planificate în moneda proiectului față de vânzările planificate în moneda contractului.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Reproiectarea veniturilor asupra activităților nodului frunze

Veniturile forței de muncă pentru o sarcină de nod frunză nu pot fi reproiectate direct pe fila **Urmărire** de pe pagina **Proiect**. Cu toate acestea, puteți utiliza vizualizarea **Urmărirea efortului** pentru a reproiecta efortul rămas pentru o sarcină. Acest lucru determină recalcularea venitului rămas pentru activitate. Următoarea este o descriere a modului în care funcționează acest lucru.

1. Un manager de proiect poate reproiecta efortul asupra activităților actualizând valoarea implicită în câmpul **Efort rămas** cu o nouă estimare a efortului asupra activității. Reproiectarea actualizare cauzează o recalculare a estimării efortului activității (EAC) la finalizare, procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, estimarea de finalizare (ETC), și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.
2. Pe baza noii valori pentru efortul rămas pe sarcină, sistemul calculează venitul rămas pe vizualizarea **Urmărirea costurilor**. Pentru a calcula venitul rămas pe baza efortului rămas, sistemul calculează mai întâi venitul mediu de o oră de efort pe activitatea de rezumat drept venit planificat sau efort planificat. Venitul planificat este suma venitului tuturor alocărilor de resurse pentru activitate. Venitul mediu pe oră este utilizat pentru a calcula venitul rămas pentru efortul rămas nou proiectat pentru activitate.
3. Venitul estimat la final și procentul de consum al venitului pentru sarcina nod-frunză sunt recalculate.
4. Sunt recalculate veniturile la valoarea completă a activităților de rezumat până la nodul rădăcină.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Reproiectarea veniturilor asupra activităților de rezumat

Puteți reproiecta veniturile forței de muncă pentru sarcini sumare sau sarcini de container. Cu toate acestea, nu puteți reproiecta direct veniturile cu forța de muncă pe activitatea de rezumat de proiect pe fila **Urmărire** pe pagina **Proiect**. Similar sarcinilor nodului frunze, rezumatul reproiectării și sarcinile containerului se pot face folosind vizualizarea **Urmărirea efortului**. În această vizualizare, puteți reproiecta efortul rămas pe o sarcină sumară provocând o recalculare a venitului rămas pe activitatea de rezumat. Următoarea este o descriere a modului în care funcționează acest lucru.

1. Un manager de proiect poate reproiecta efortul asupra activităților actualizând valoarea implicită în câmpul **Efort rămas** cu o nouă estimare a **Efortului rămas** pe activitate. Reproiectarea actualizare cauzează o recalculare a estimării activității (EAC) la finalizare, procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.
2. Pe baza noii valori în câmpul **Efort rămas** pe activitate, sistemul calculează venitul rămas în vizualizarea **Urmărirea venitului**. Pentru a calcula venitul rămas pe baza efortului rămas, sistemul calculează mai întâi venitul mediu de o oră de efort pe activitate drept venit planificat sau efort planificat. Venitul planificat este suma venitului tuturor alocărilor de resurse pentru activitate. Acest venit mediu pe oră este apoi utilizat pentru a calcula venitul efortului nou proiectat rămas asupra activității.
3. Venitul estimat la final și procentul de consum al venitului pentru procentele de consum asupra activității de rezumat și sunt recalculate.
4. Valoarea nouă pentru venitul estimat la final este distribuită până la activitățile secundare în aceeași proporție cum a fost venitul original planificat pe activitate.
5. Este calculat venitul nou la valoare finală pe fiecare dintre activitățile individuale până la activitățile de nod frunză. Pe baza acestei valori, sarcinile copilului afectat până la nodurile frunze vor avea venitul rămas și procentul de consum de venit recalculat pe baza venitului la valoarea completă. Acest lucru duce la o nouă proiecție pentru varianța venitului activității. 
6. Sunt recalculate veniturile la valoarea completă a activităților de rezumat până la nodul rădăcină.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

