---
title: Gestionarea listelor de prețuri ale proiectelor dintr-o ofertă
description: Acest subiect oferă informații despre entitatea proiect listă de prețuri.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 4bd4e9cb22bfd6a86fd86e5fc403cb185aab140a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277758"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Gestionarea listelor de prețuri ale proiectelor dintr-o ofertă

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations extinde entitatea Listă de prețuri în Dynamics 365 Sales. 

## <a name="key-entities"></a>Entități-cheie

O listă de prețuri include informații furnizate de patru entități diferite:

- **Listă de prețuri**: această entitate stochează informații despre context, monedă, efectivitatea datelor și unitatea de timp pentru timpul de tarifare. Contextul arată dacă lista de prețuri exprimă ratele de cost sau ratele de vânzări. 
- **Monedă**: această entitate stochează moneda prețurilor de pe lista de prețuri. 
- **Dată**: această entitate este utilizată atunci când sistemul încearcă să introducă un preț implicit pe o tranzacție. Este selectată o listă de prețuri care are o efectivitate a datelor care include data tranzacției. Dacă este găsită mai mult de o listă de prețuri care este eficientă pentru data tranzacției și este atașată la oferta corelată, contract sau unitate organizațională, atunci niciun preț nu este implicit. 
- **Timp**: această entitate stochează unitatea de timp pentru care sunt exprimate prețurile, cum ar fi tarifele zilnice sau orare. 

Entitatea Listă de prețuri are trei tabele corelate care stochează prețurile:

  - **Preț pentru rol**: acest tabel stochează o rată pentru o combinație de valori ale rolului și ale unităților organizaționale și este utilizat pentru a configura prețuri bazate pe roluri pentru resursele umane.
  - **Preț pentru categoria de tranzacție**: acest tabel stochează prețurile după categoria de tranzacții și este utilizat pentru a configura prețurile categoriilor de cheltuieli.
  - **Elemente de listă de prețuri**: acest tabel stochează prețurile pentru produsele din catalog.
 
Lista de prețuri este o grilă tarifară. O grilă tarifară este o combinație a entității Listă de prețuri și a rândurilor corelate din tabelele Preț de rol, Preț categorie tranzacție și Elemente de listă de prețuri.

## <a name="resource-roles"></a>Roluri de resursă

Termenul *rol de resursă* se referă la un set de aptitudini, competențe și certificări pe care o persoană trebuie să le aibă pentru a efectua un anumit set de activități într-un proiect.

Timpul de resurse umane este ofertat pe baza rolului pe care o resursă îl îndeplinește pe un anumit proiect. Pentru timpul de resurse umane, costurile și facturarea se bazează pe rolul de resursă. Timpul poate fi tarifat în orice unitate din grupul de unități **Timp**.

Grupul de unități **Timp** este creat atunci când instalați Project Operations. Acesta are o unitate implicită de **Oră.** Nu aveți posibilitatea să ștergeți, să redenumiți sau să editați atributele pentru grupul de unități **Timp** sau pentru unitatea **Oră**. Cu toate acestea, puteți adăuga alte unități la grupul de unități **Timp**. Dacă încercați să ștergeți fie grupul de unități **Timp**, fie unitatea **Oră**, s-ar putea să provocați erori în logica de afaceri.
 
## <a name="transaction-categories-and-expense-categories"></a>Categoriile de tranzacții și categoriile de cheltuieli

Cheltuielile de deplasare și alte cheltuieli pe care consultanții de proiect le suportă sunt facturate clientului. Tarifarea categoriilor de cheltuieli este completată utilizând listele de prețuri. Biletele de avion, cazarea la hotel și închirierile auto sunt exemple de categorii de cheltuieli. Fiecare linie de listă de prețuri pentru cheltuieli specifică tarifarea pentru o anumită categorie de cheltuieli. Următoarele trei metode sunt utilizate pentru prețul categoriilor de cheltuieli:

- **La cost**: costul cheltuielilor este facturat clientului și nu se aplică niciun adaos.
- **Procent adaos**: procentul din costul real este facturat clientului. 
- **Preț unitar**: un preț de facturare este setat pentru fiecare unitate din categoria de cheltuieli. Suma facturată clientului se calculează pe baza numărului de unități de cheltuieli pe care le raportează consultantul. Kilometraj utilizează metoda de tarifare preț pe unitate. De exemplu, categoria de cheltuieli kilometraj poate fi configurată pentru 30 de dolari SUA (USD) pe zi sau 2 USD pe kilometru. Atunci când un consultant raportează kilometrajul pe un proiect, suma de facturat se calculează în funcție de numărul de kilometri raportat de consultant.
 
## <a name="project-sales-pricing-and-overrides"></a>Tarifarea vânzărilor de proiect și suprascrieri

Pentru ofertele și contractele de proiect, o listă de prețuri de proiect are un alt model de suprascriere a prețului decât o listă de prețuri de produs. Pe o linie de ofertă bazată pe catalogul de produse, aveți posibilitatea să suprascrieți prețul la roluri și categorii direct pe linia de ofertă, deoarece fiecare linie de ofertă indică exact un element de catalog. Cu toate acestea, pe o linie de ofertă bazată pe proiect, nu puteți suprascrie prețul la roluri și categorii direct pe linia de ofertă. Utilizați proiectul de listă de prețuri pentru a accepta cele două șabloane distincte de suprascriere.

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

Pe un contract de proiect, următoarea ordine de prioritate pentru a seta automat liste de prețuri de proiect corelate:

1. Ofertă
2. Oportunitate
3. Client 
4. Setări globale 

Atunci când o listă de prețuri de proiect este introdusă în mod implicit, sistemul validează că moneda se potrivește cu moneda clientului și că listele de prețuri implicite care au fost introduse au un context de **Vânzări**.

Aveți posibilitatea să asociați mai multe liste de prețuri cu entitățile Client, Oportunitate, Ofertă și Contract de proiect. Această capacitate acceptă prețuri implicite specifice datei pentru un contract de proiect de lungă durată, în cazul căruia este posibil să aveți nevoie de mai mult de o listă de prețuri pentru a ține cont de actualizările de preț care au loc din cauza inflației. Cu toate acestea, în cazul în care listele de prețuri pe care le asociați cu entitatea Client, Oportunitate, Ofertă sau Contract de proiect au o suprapunere a efectivității datelor, prețurile implicite ar putea fi incorecte. De aceea, ar trebui să vă asigurați că listele de prețuri de proiect care au o suprapunere a efectivității datelor nu sunt asociate cu aceste entități.

### <a name="deal-specific-price-overrides"></a>Suprascrieri ale prețurilor specifice unei tranzacții

Aveți posibilitatea să creați suprascrieri specifice unei tranzacții pentru prețurile selectate pe listele de prețuri de proiect care sunt introduse în mod implicit pe o ofertă sau un contract de proiect.

În mod implicit, un contract de proiect primește întotdeauna o copie a listei de prețuri de vânzare principală în loc de o legătură directă la aceasta. Acest comportament ajută la garantarea faptului că acordurile de preț care sunt făcute cu un client pentru o specificație de lucru (SL) nu se modifică dacă se modifică lista de prețuri principală.

Cu toate acestea, pe o ofertă, aveți posibilitatea să utilizați o listă de prețuri principală. Alternativ, aveți posibilitatea să copiați o listă de prețuri principală și să o editați pentru a crea o listă de prețuri particularizată care se aplică numai la acea ofertă. Pentru a crea o listă de prețuri nouă care este specifică unei oferte, pe pagina **Ofertă** selectați **Creați prețuri particularizate**. Aveți posibilitatea să accesați lista de prețuri de proiect specifică unei tranzacții numai din ofertă. 

Atunci când creați o listă de prețuri de proiect particularizată, numai componentele proiectului din lista de prețuri sunt copiate. Cu alte cuvinte, o nouă listă de prețuri este creată ca o copie a listei de prețuri existente a proiectului care este atașată la ofertă și această nouă listă de prețuri are numai prețuri de rol corelate și prețuri pentru categoriile de tranzacții.
  
## <a name="tracking-costs"></a>Costuri urmărire

Project Operations urmăresc costurile pentru utilizarea timpului de resurse umane pe proiecte. De asemenea, urmărește costurile pentru alte cheltuieli care sunt achitate în timpul proiectului, cum ar fi cheltuielile de deplasare.

Ca și ratele de facturare, ratele de cost pentru resurse umane sunt, de asemenea, configurate folosind listele de prețuri. Aici sunt principalele diferențe de comportament între lista de prețuri de cost și lista de prețuri de vânzare:

- Rata de cost a unei resurse nu poate fi suprascrisă pe un anumit proiect, contract sau ofertă. Cu toate acestea, ratele de facturare pot fi suprascrise per tranzacție dacă se fac modificări care sunt specifice pentru natura tranzacției. 

- Următoarea ordine este utilizată pentru a rezolva o listă de prețuri de cost:

    1. Lista de prețuri de cost care este atașată la unitatea organizațională.
    2. Lista de prețuri de cost care este atașată la parametrii Project Operations. Deoarece listele de prețuri de cost în mai multe monede diferite pot fi atașate la parametrii, o potrivire de monedă este finalizată între moneda unității organizaționale contractante a proiectului, contractului sau ofertei și moneda din lista de prețuri de cost.
    3. Pentru cheltuieli, metodele de tarifare la cost și de tarifare cu adaos peste cost nu se aplică listelor de prețuri de cost. Chiar dacă aceste metode de tarifare sunt utilizate pe linii de listă de prețuri de cost pentru a configura costurile categoriei de tranzacții, sistemul le ignoră și nu este introdus niciun preț de cost implicit.


[!INCLUDE[footer-include](../includes/footer-banner.md)]