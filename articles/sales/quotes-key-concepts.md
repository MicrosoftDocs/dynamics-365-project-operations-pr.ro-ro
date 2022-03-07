---
title: Oferte - Concepte cheie
description: Acest subiect oferă informații despre ofertele de proiect și ofertele de vânzare disponibile în Project Operations.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8a1b5152b76cbcdfb5160a0af78eceec2c42b9a13dfc76701b6ad935318c7ba8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997891"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Concepte unice pentru ofertele bazate pe proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În Dynamics 365 Project Operations, există două tipuri de oferte, de proiect și oferte de vânzări. Cele două tipuri de oferte diferă în următoarele moduri:

- **GGrile pentru elemente de linie**: într-o ofertă de vânzări, există o singură grilă pentru elementele de linie. Pe o ofertă de proiect sunt două grile pentru elemente de linie. O grilă este pentru liniile de proiect și cealaltă este pentru liniile de produse.
- **Activare și revizuiri**: cotațiile de vânzări acceptă activarea și revizuirea. Aceste procese nu sunt acceptate pe o ofertă de proiect.
- **Comenzi atașate**: puteți atașa mai multe comenzi la o ofertă de vânzări. Doar un contract de proiect poate fi atașat unei oferte de proiect.
- **Câștigarea unei oferte**: Când câștigați o ofertă de vânzare, oportunitatea aferentă poate rămâne deschisă. După ce se câștigă o ofertă de proiect, oportunitatea corelată este închisă.
- **Câmpuri și concepte**: o ofertă de vânzări nu include unele câmpuri și concepte care sunt incluse într-o ofertă de proiect. Câmpurile includ **Unitatea contractantă**, **Managerul de cont** și **Facturare către Nume persoană de contact**.  
- **Tip**: ofertele de vânzări și proiecte sunt identificate și de câmpul bazat pe setul de opțiuni, **Tip**. Pentru o ofertă de vânzări, acest câmp are valoarea **Pe bază de articol**. Pentru o ofertă de proiect, are valoarea **Pe bază de lucru**.

Acest subiect se concentrează pe detaliile ofertelor de proiect.

O ofertă de proiect în Project Operations poate avea mai multe elemente de linie sau linii de ofertă. De fapt, o ofertă de proiect are două grile pentru elemente de linie. O grilă este pentru liniile bazate pe proiect, care permit estimări detaliate. Cealaltă grilă este pentru liniile bazate pe produse, care utilizează un preț unitar simplu și o abordare bazată pe cantități.

- **Pe bază de proiect**: valoarea ofertată este determinată după ce estimați cât de multă muncă este necesară. Puteți estima munca la un nivel ridicat, direct ca detalii de linie sub fiecare linie de ofertă sau pe baza estimărilor de la sol, utilizând un proiect și un plan de proiect. Liniile de ofertă bazate pe proiect se găsesc numai în ofertele bazate pe proiect care sunt create utilizând Project Operations. Acest tip de linie de ofertă este o formă particularizată a liniilor de ofertă din afara catalogului care sunt disponibile în Microsoft Dynamics 365 Sales.

- **Pe bază de produs**: valoarea ofertată este determinată în funcție de cantitatea de unități vândute și de prețul de vânzare unitar. Produsul dintr-o linie bazată pe produse poate proveni dintr-un catalog de produse din Vânzări sau poate fi un produs pe care îl definiți. Acest tip de linie de ofertă este disponibil și pe ofertele bazate pe proiect care sunt create utilizând Project Operations.

Suma dintr-o ofertă este totalul din liniile bazate pe produs și liniile bazate pe proiect.

> [!NOTE]
> Ofertele și liniile de ofertă nu sunt necesare în Project Operations. Puteți începe procesul de proiect cu un contract de proiect (proiect vândut). Cu toate acestea, o oportunitate este întotdeauna necesară, indiferent dacă începeți cu o ofertă sau un contract de proiect.

## <a name="project-based-quote-lines"></a>Linii de oferte bazate pe proiect

O linie de ofertă bazată pe proiect în Project Operations are următoarele metode de facturare:

- Timp și material
- Preț fix

### <a name="time-and-material"></a>Timp și materiale

Metoda de facturare Timp și materiale se bazează pe consum. Când selectați această metodă de facturare, clientul este facturat pe măsură ce proiectul contractează costuri. Facturile sunt create cu o frecvență periodică bazată pe dată. În timpul procesului de vânzări, valoarea ofertată a unei componente de timp și materiale oferă doar o estimare a costului final pentru client. Vânzătorul nu se angajează să finalizeze proiectul exact la valoarea ofertată. Componentele de timp și materiale măresc riscul clientului. Clienții ar putea dori să negocieze clauze suplimentare de nedepășire pentru a-și minimiza riscul. Project Operations nu acceptă configurarea clauzelor care să nu exceadă.

### <a name="fixed-price"></a>Preț fix

În metoda de facturare Preț fix, un furnizor se angajează să livreze proiectul la un cost fix pentru client. Clientului i se facturează valoarea ofertată a liniei de ofertă cu preț fix, indiferent de costurile pe care furnizorul le suportă pentru a livra acea linie de ofertă. Valoarea liniei de ofertă cu preț fix este facturată într-unul din următoarele moduri: 

- Ca o sumă forfetară la începutul sau la sfârșitul proiectului, sau atunci când este atins un jalon de proiect. 
- Cu o frecvență bazată pe date a ratelor egale ale valorii fixe din linia de ofertă. Aceste rate sunt cunoscute ca jaloane periodice.
- În rate care au o valoare monetară aliniată cu progresul lucrului sau cu jaloane specifice care sunt atinse în cadrul proiectului. În acest caz, valoarea fiecărei rate poate diferi, dar toate însumate trebuie să atingă valoarea fixă din linia de ofertă.

Project Operations acceptă toate cele trei tipuri de planificări ale facturilor pentru liniile de ofertă cu preț fix.

## <a name="transaction-classification"></a>Clasificare tranzacții

Organizațiile profesionale de servicii de obicei își ofertează și facturează clienții prin clasificarea costurilor. Costurile sunt reprezentate de următoarele clasificări de tranzacții:

- **Timp**: această clasificare reprezintă costul muncii sau de timpul de resurse umane din cadrul unui proiect.
- **Cheltuieli**: această clasificare reprezintă toate celelalte tipuri de cheltuieli pe un proiect. Deoarece cheltuielile pot fi clasificate în linii mari, cele mai multe organizații creează subcategorii, precum de deplasare, închirieri auto, cazare la hotel sau consumabile de birou.
- **Taxă**: această clasificare reprezintă diverse cheltuieli de regie, penalități și alte elemente care sunt percepute clientului. 
- **Impozit**: această clasificare reprezintă sumele fiscale pe care utilizatorii le adaugă în timp ce introduc cheltuieli.
- **Tranzacții materiale**: această clasificare reprezintă valorile reale din liniile de produse pe o factură de proiect confirmată.
- **Jalon**: această clasificare este utilizată de logica facturării la preț fix.

Una sau mai multe dintre aceste clasificări de tranzacții pot fi asociate cu fiecare linie de ofertă. După ce se câștigă o ofertă, maparea dintre clasificarea tranzacțiilor și linia de ofertă este transferată la linia de contract.
  
De exemplu, o ofertă poate conține următoarele două linii de ofertă: 

- Activitate de consultanță care utilizează o metodă de facturare Timp și materiale, în cadrul căreia se aplică clasificări de tranzacții timp și taxă. De exemplu, toate tranzacțiile de timp și taxă pentru proiectul de exemplificare **Implementare Dynamics AX** sunt facturate clientului pe baza orei și materialelor care sunt utilizate. 
- Cheltuieli corelate de deplasare care utilizează o metodă de facturare Preț fix. De exemplu, toate cheltuielile de deplasare pentru proiectul de exemplificare **Implementare Dynamics AX** sunt facturate la o valoare monetară fixă.

> [!NOTE]
> Combinația de clasificări de proiect și de tranzacții pentru **Timp**, **Cheltuieli** și **Taxă** care sunt asociate cu o linie de ofertă sau linie de contract trebuie să fie unică. Dacă aceeași combinație de clasă de proiect și de tranzacții este asociată cu mai mult de o linie de contract sau o linie de ofertă, Project Operations nu vor funcționa corect.

## <a name="billing-types"></a>Tipuri de facturare

Câmpul **Tip de facturare** definește conceptul de tarifare. Este un set de opțiuni care are următoarele valori posibile:

- **Tarifabil**: costul care este acumulat de acest rol/categorie este un cost direct care determină executarea proiectului, iar clientul va plăti pentru această lucrare. Plata poate fi administrată ca un aranjament de timp și materiale sau cu preț fix. Cu toate acestea, angajatul care petrece acest timp va primi creditul corespunzător pentru utilizarea sa facturabilă.
- **Netarifabil**: costul care este acumulat de acest rol/categorie este considerat un cost direct care determină executarea proiectului, chiar dacă clientul nu recunoaște acest fapt și nu va plăti pentru această lucrare. Angajatul care petrece acest timp nu va fi creditat cu utilizare facturabilă pentru el.
- **Gratuit**: costul care este acumulat de acest rol/categorie este considerat un cost direct care determină executarea proiectului, iar clientul recunoaște acest fapt. Angajatul care petrece acest timp va fi creditat pentru utilizarea facturabilă pentru el. Cu toate acestea, acest cost nu este tarifat clientului.
- **Indisponibil**: costurile suportate pentru proiecte interne care nu necesită urmărirea veniturilor sunt urmărite utilizând această opțiune.

## <a name="invoice-schedule"></a>Planificare factură

O planificare a facturilor este o serie de date când se produce facturarea pentru un proiect. Opțional, puteți crea o planificare a facturilor pe o linie de ofertă: Fiecare linie de ofertă poate avea propria planificare a facturilor. Pentru a crea o planificare a facturilor, trebuie să furnizați următoarele valori de atribut:

- O dată de început facturare 
- O dată de livrare care reprezintă data de încheiere a facturării pe proiect
- O frecvență a facturilor

Aceste trei valori de atribut sunt utilizate pentru a genera un set provizoriu de date pe baza căruia stabilește facturarea.

## <a name="invoice-frequency"></a>Frecvență facturi

Frecvența facturilor este o entitate care stochează valorile atributelor care ajută la exprimarea frecvenței creării de facturi. Următoarele atribute exprimă sau definesc entitatea Frecvență facturi:

- **Perioada**: sunt acceptate perioadele lunare, bisăptămânale și săptămânale. 
- **Rulări pe perioadă**: pentru perioade săptămânale și bisăptămânale, aveți posibilitatea să definiți doar o singură rulare pe perioadă. Pentru perioadele lunare, puteți defini între una și patru rulări pe perioadă. 
- **Zile de rulare**: zilele când facturarea trebuie executată. Puteți configura acest atribut în două moduri diferite:
  - **Zile lucrătoare**: de exemplu, aveți posibilitatea să specificați că facturarea se execută în fiecare luni sau în fiecare luni din două în două săptămâni. Clienții care trebuie să seteze facturarea să se execute într-o zi lucrătoare ar putea prefera acest tip de configurație. 
  - **Zile calendaristice**: de exemplu, aveți posibilitatea să specificați că facturarea se execută în a șaptea și a douăzeci și una zi a fiecărei luni. Unele organizații pot prefera acest tip de configurație, deoarece contribuie la garantarea faptului că facturarea se execută după un program fix în fiecare lună.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Planificarea facturii pentru o linie de ofertă cu preț fix

Pentru o linie de ofertă cu preț fix, aveți posibilitatea să utilizați grila **Planificare factură** pentru a crea jaloane de facturare care să fie egale cu valoarea liniei de ofertă.

- Pentru a crea jaloane de facturare care sunt împărțite în mod egal, selectați o frecvență a facturilor, introduceți data de începere a facturării pe linia de ofertă și selectați **Dată de finalizare solicitată** pentru ofertă în secțiunea **Rezumat** a antetului de ofertă. Apoi selectați **Generare jaloane periodice** pentru a crea jaloane divizate în mod egal pe baza frecvenței selectate a facturilor. 
- Pentru a crea un jalon de facturare cu sumă forfetară, creați un jalon, apoi introduceți valoarea liniei de ofertă ca sumă a jalonului.
- Pentru a crea jaloane de facturare care se bazează pe anumite activități din planul de proiect, creați un jalon și mapați-l la elementul de planificare al proiectului în IU pentru jaloanele de facturare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
