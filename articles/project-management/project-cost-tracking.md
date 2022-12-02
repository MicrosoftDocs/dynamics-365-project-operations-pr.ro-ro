---
title: Urmărirea costului de proiect
description: Acest articol oferă informații despre modul în care Project Operations urmărește progresul în raport cu costul forței de muncă și cheltuielile pentru un proiect.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923755"
---
# <a name="labor-cost-tracking-on-projects"></a>Urmărirea costurilor cu forța de muncă în proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations urmărește estimările forței de muncă și cheltuie la cea mai mică granularitate necesară pentru planul de proiect. Estimarea financiară a costului forței de muncă se bazează pe efortul planificat și pe resursele generice sau denumite care sunt alocate fiecărei sarcini nod-frunză din planul de proiect. Când începe proiectul și oamenii încep să raporteze timpul asupra diferitelor sarcini ale proiectului, se rezumă cheltuiala reală cu forța de muncă care începe un calcul al proiecțiilor.

## <a name="labor-cost-tracking-view"></a>Vizualizare urmărire cost forță de muncă

Pe pagina **Proiecte**, pe fila **Urmărire**, puteți selecta **Urmărire** > **Cost** pentru a deschide vizualizarea **Urmărirea costurilor** și vedeți progresul cheltuielilor de muncă pentru fiecare sarcină din planul de proiect. Această viziune compară, de asemenea, costul real al forței de muncă cheltuit pentru o sarcină cu costul forței de muncă planificat al sarcinii. Project Operations utilizează următoarele formule pentru a calcula valorile costului forței de muncă:

- **Cost planificat**: Costul estimat al tuturor atribuirilor de resurse pentru fiecare sarcină de nod frunză
- **Costul actual**: Suma tuturor costurilor reale pentru timpul înregistrat în sarcină
- **Procentul de consum al costurilor**: Costul real ÷ Estimarea costului la final
- **Costul rămas**: estimarea de cost la final - costul real
- **Costul la final**: costul rămas + costul real
- **Varianța de cost**: cost planificat - estimarea de cost la final

Fiecare activitate afișează o proiecție a variației de cost la activitate. Dacă estimarea completă a costurilor este mai mare decât costul planificat, sarcina este proiectată să depășească bugetul. Dacă estimarea completă a costurilor este mai mică decât costul planificat, activitatea este proiectată pentru a se finaliza sub buget.

>[!NOTE]
> Project Operations arată doar costurile forței de muncă pe pagina **Proiect** pe fila **Urmărire**. În timp ce materialele și cheltuielile pot fi estimate și urmărite pentru consum, aceste costuri nu sunt incluse în costurile indicate pe fila **Urmărire**. Această filă este concepută să funcționeze numai pentru reproiectarea costurilor forței de muncă prin reproiectarea efortului.
Toate sumele de cost afișate sunt convertite în moneda de cost a proiectului din moneda de preț de cost a proiectului utilizată pentru a determina rata de cost. Moneda de cost a proiectului este moneda unității contractante din proiect. Valorile costurilor estimate pentru timp care sunt afișate pe fila **Estimări** de pe pagina **Proiect** s-ar putea să nu adauge costul planificat pe fila **Urmărire**. Motivul acestei discrepanțe se datorează diferențelor în modul în care costul estimat este rezumat pe grila **Estimări** și modul în care este calculat costul planificat pe grila **Urmărire**. 
>
> - Fila **Estimări** calculează costul estimat utilizând aceeași monedă a ratei de cost din lista de prețuri. Apoi, costul estimat în moneda listei de prețuri este convertit în costul estimat în moneda costului proiectului. Costul estimat în moneda proiectului este afișat rotunjit la 2 zecimale. În niciun moment al acestei conversii nu se aplică precizia monedei. 
> - Pe fila **Urmărire**, calculul costului planificat urmează un ordin de calcul ușor diferit care implică aplicarea preciziei valutare în două etape: 
   ><ol>
   ><li>Suma estimată a costului în moneda listei de prețuri este convertită în moneda de bază (conversia 1).</li>
   ><li>Suma estimată a costului în moneda de bază este convertită în moneda costului de proiect (conversia 2). </li>
   ></ol>
   >Precizia valutară se aplică în ambii pași pentru a obține un cost planificat (pe fila **Urmărire**) care se abate ușor de la costul estimat (pe vizualizarea **Timp - etapizat** pe fila **Estimări**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Reproiectarea costurilor asupra sarcinilor nodului frunză

Costurile forței de muncă pentru o sarcină de nod frunză nu pot fi reproiectate direct pe fila **Urmărire** de pe **Pagina proiectului**. Cu toate acestea, puteți utiliza vizualizarea **Urmărirea efortului** pentru a reproiecta efortul rămas pentru o sarcină. Acest lucru determină recalcularea costului rămas pentru activitate. Următoarea este o descriere a modului în care funcționează acest lucru.

1. Un manager de proiect poate reproiecta efortul asupra activităților actualizând valoarea implicită în câmpul **Efort rămas** cu o nouă estimare a efortului asupra activității. Reproiectarea actualizare cauzează o recalculare a estimării efortului activității (EAC) la finalizare, procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, estimarea de finalizare (ETC), și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.
2. Pe baza noii valori pentru efortul rămas pe sarcină, sistemul calculează costul rămas pe vizualizarea **Urmărirea costurilor**. Pentru a calcula costul rămas pe baza efortului rămas, sistemul calculează mai întâi costul mediu de o oră de efort pe sarcină ca cost planificat sau efort planificat. Costul planificat este suma costului tuturor alocărilor de resurse pentru activitate. Costul mediu pe oră este utilizat pentru a calcula costul rămas pentru efortul rămas nou proiectat pentru activitate.
3. Costul complet și procentul de consum al costurilor pentru sarcina nod-frunză sunt recalculate.
4. Sunt recalculate costurile la valoarea completă a activităților de rezumat până la nodul rădăcină.

## <a name="reprojecting-costs-on-summary-tasks"></a>Reproiectarea costurilor asupra activităților de rezumat

Puteți reproiecta costurile forței de muncă pentru sarcini sumare sau sarcini de container. Cu toate acestea, nu puteți reproiecta direct costurile cu forța de muncă pe activitatea de rezumat de proiect pe fila **Urmărire** pe pagina **Proiect**. Similar sarcinilor nodului frunze, rezumatul reproiectării și sarcinile containerului se pot face folosind vizualizarea **Urmărirea efortului**. În această vizualizare, puteți reproiecta efortul rămas pe o sarcină sumară provocând o recalculare a costului rămas pe activitatea de rezumat. Următoarea este o descriere a modului în care funcționează acest lucru.

1. Un manager de proiect poate reproiecta efortul asupra activităților prin actualizarea valorii implicite a efortului rămas cu o nouă estimare a activității. Această actualizare cauzează o recalculare a estimării activității (EAC) la finalizare, procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.
2. Pe baza noii valori pentru efortul rămas pe activitatea de rezumat, sistemul calculează costul rămas pe vizualizarea **Urmărirea costurilor**. Pentru a calcula costul rămas pe baza efortului rămas, sistemul calculează mai întâi costul mediu de o oră de efort pe activitatea de rezumat drept cost planificat sau efort planificat. Costul mediu pe oră este utilizat pentru a calcula costul rămas pentru efortul nou proiectat pentru activitatea de rezumat.
3. Costurile complete și procentul de consum al costurilor pentru activitatea de rezumat sunt recalculate.
4. Costul nou la final este distribuit către activitățile secundare în aceeași proporție cum a fost costul original planificat pe activitate.
5. Este calculat costul nou la valoare finală pe fiecare dintre activitățile individuale până la activitățile de nod frunză. Pe baza acestei valori, sarcinile copilului afectat până la nodurile frunze vor avea costul rămas și procentul de consum de cost recalculat pe baza costului la valoarea completă. Această valoare duce la o nouă proiecție pentru varianța de cost a activității. 


Câmpul **Performanța costurilor** poate fi setat din datele de urmărire. Când variația costurilor pentru nodul rădăcină în vizualizarea **Urmărirea costurilor** este negativă, puteți seta acest câmp la **Sub buget**. Când variația costurilor pentru nodul rădăcină este pozitivă, puteți seta valoarea la **Peste buget**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
