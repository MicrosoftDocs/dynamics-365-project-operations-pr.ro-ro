---
title: Oferte și linii de ofertă
description: Acest subiect oferă informații despre oferte și linii de ofertă.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 024a7cdb81340a077e839d92c4321c8b0051404b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145148"
---
# <a name="quotes-and-quote-lines"></a>Oferte și linii de ofertă

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

În Dynamics 365 Project Service Automation, există două tipuri de oferte: oferte de proiect și oferte de vânzări. Cele două tipuri diferă în următoarele moduri:

- Într-o ofertă de vânzări, există o singură grilă pentru elementele de linie. Într-o ofertă de proiect, există două grile pentru elementele de linie: una pentru liniile de proiect și una pentru liniile de produse.
- O ofertă de vânzări acceptă activarea și revizuirile. O ofertă de proiect nu acceptă aceste procese.
- Aveți posibilitatea să atașați mai multe comenzi la o ofertă de vânzări. Aveți posibilitatea să atașați un singur contract de proiect la o ofertă de proiect.
- Aveți posibilitatea să câștigați o ofertă de vânzări și să mențineți deschisă oportunitatea corelată. După ce se câștigă o ofertă de proiect, oportunitatea corelată este închisă.
- O ofertă de vânzări nu include unele câmpuri și concepte care sunt incluse într-o ofertă de proiect. Câmpurile includ **Unitatea contractantă**, **Managerul de cont** și **Facturare către Nume persoană de contact**.  
- Ofertele de vânzări și ofertele de proiect sunt, de asemenea, identificate printr-un câmp bazat pe set de opțiuni care este denumit **Tip**. Pentru o ofertă de vânzări, acest câmp are valoarea **Pe bază de articol**. Pentru o ofertă de proiect, are valoarea **Pe bază de lucru**.

Acest subiect se va concentra pe detaliile ofertelor de proiect.

O ofertă de proiect în PSA poate avea mai multe elemente de linie sau linii de ofertă. De fapt, o ofertă de proiect are două grile pentru elemente de linie. O grilă este pentru liniile bazate pe proiect, care permit estimări detaliate. Cealaltă grilă este pentru liniile bazate pe produse, care utilizează un preț unitar simplu și o abordare bazată pe cantități.

- **Pe bază de proiect** – suma (valoarea ofertată) este determinată după ce estimați cât de multă muncă este necesară. Puteți estima lucrul la un nivel înalt sau îl puteți estima direct ca detalii de linie sub fiecare linie de ofertă. În cele din urmă, puteți estima munca pe baza estimărilor de la zero, utilizând un proiect și un plan de proiect. Liniile de ofertă bazate pe proiect se găsesc numai în ofertele bazate pe proiect care sunt create utilizând Project Service Automation. Acest tip de linie de ofertă este o formă particularizată a liniilor de ofertă din afara catalogului care sunt disponibile în Microsoft Dynamics 365 Sales.
- **Pe bază de produs** – suma (valoarea ofertată) este determinată în funcție de cantitatea de unități vândute și de prețul de vânzare unitar al produsului. Produsul dintr-o linie bazată pe produse poate proveni dintr-un catalog de produse din Vânzări sau poate fi un produs pe care îl definiți. Acest tip de linie de ofertă este disponibil și pe ofertele bazate pe proiect care sunt create utilizând PSA.

Suma dintr-o ofertă este totalul din liniile bazate pe produs și liniile bazate pe proiect.

> [!NOTE]
> Ofertele și liniile de ofertă nu sunt necesare în PSA. Puteți începe procesul de proiect cu un contract de proiect (proiect vândut). Cu toate acestea, o oportunitate este întotdeauna necesară, indiferent dacă începeți cu o ofertă sau un contract de proiect.

## <a name="project-based-quote-lines"></a>Linii de ofertă bazate pe proiect

O linie de ofertă bazată pe proiect în PSA are următoarele metode de facturare:

- Timp și materiale
- Preț fix

### <a name="time-and-material"></a>Timp și materiale

Metoda de facturare Timp și materiale se bazează pe consum. Când selectați această metodă de facturare, clientul este facturat pe măsură ce proiectul contractează costuri. Facturile sunt create cu o frecvență periodică bazată pe dată. În timpul procesului de vânzări, valoarea ofertată a unei componente de timp și materiale oferă doar o estimare a costului final pentru client. Vânzătorul nu se angajează să finalizeze proiectul exact la valoarea ofertată. Componentele de timp și materiale măresc riscul clientului. Clienții ar putea dori să negocieze clauze suplimentare de nedepășire pentru a-și minimiza riscul. PSA nu acceptă setarea de clauze de nedepășire.

### <a name="fixed-price"></a>Preț fix

În metoda de facturare Preț fix, un furnizor se angajează să livreze proiectul la un cost fix pentru client. Clientului i se facturează valoarea ofertată a liniei de ofertă cu preț fix, indiferent de costurile pe care furnizorul le suportă pentru a livra acea linie de ofertă. Valoarea liniei de ofertă cu preț fix este facturată într-unul din următoarele moduri: 

- Ca o sumă forfetară la începutul sau la sfârșitul proiectului, sau atunci când este atins un jalon de proiect. 
- Cu o frecvență bazată pe date a ratelor egale ale valorii fixe din linia de ofertă. Aceste rate sunt cunoscute ca jaloane periodice.
- În rate care au o valoare monetară aliniată cu progresul lucrului sau cu jaloane specifice care sunt atinse în cadrul proiectului. În acest caz, valoarea fiecărei rate poate diferi, dar toate însumate trebuie să atingă valoarea fixă din linia de ofertă.

PSA acceptă toate cele trei tipuri de planificări ale facturilor pentru liniile de ofertă cu preț fix.

## <a name="transaction-classification"></a>Clasificare tranzacții

Organizațiile profesionale de servicii de obicei își ofertează și facturează clienții prin clasificarea costurilor. În PSA, costurile sunt reprezentate de următoarele clasificări de tranzacții:

- **Timp** – această clasificare reprezintă costul muncii sau de timpul de resurse umane din cadrul unui proiect.
- **Cheltuieli**: – această clasificare reprezintă toate celelalte tipuri de cheltuieli pe un proiect. Deoarece cheltuielile pot fi clasificate în linii mari, cele mai multe organizații creează subcategorii, precum de deplasare, închirieri auto, cazare la hotel sau consumabile de birou.
- **Taxă** – această clasificare reprezintă diverse cheltuieli de regie, penalități și alte elemente care sunt percepute clientului. 
- **Impozit** – această clasificare reprezintă sumele fiscale pe care utilizatorii le adaugă în timp ce introduc cheltuieli.
- **Tranzacții materiale** – această clasificare reprezintă valorile reale din liniile de produse pe o factură de proiect confirmată.
- **Jalon** – această clasificare este utilizată de logica de facturare cu preț fix în PSA.

Una sau mai multe dintre aceste clasificări de tranzacții pot fi asociate cu fiecare linie de ofertă. După ce se câștigă o ofertă, maparea dintre clasificarea tranzacțiilor și linia de ofertă este transferată la linia de contract.
 
> ![Captură de ecran a mapării tipurilor de tranzacții la ofertă și linii de contract](media/basic-guide-5.png)
  
De exemplu, o ofertă poate conține următoarele două linii de ofertă: 
- Activitate de consultanță care utilizează o metodă de facturare Timp și materiale, în cadrul căreia se aplică clasificări de tranzacții timp și taxă. De exemplu, toate tranzacțiile de timp și taxă pentru proiectul de exemplificare **Implementare Dynamics AX** sunt facturate clientului pe baza orei și materialelor care sunt utilizate. 
- Cheltuieli corelate de deplasare care utilizează o metodă de facturare Preț fix. De exemplu, toate cheltuielile de deplasare pentru proiectul de exemplificare **Implementare Dynamics AX** sunt facturate la o valoare monetară fixă.

> [!NOTE]
> Combinația de clasificări de proiect și de tranzacții pentru **Timp**, **Cheltuieli** și **Taxă** care sunt asociate cu o linie de ofertă sau linie de contract trebuie să fie unică. Dacă aceeași combinație de clasă de proiect și de tranzacții este asociată cu mai mult de o linie de contract sau o linie de ofertă, PSA nu va funcționa corect.

## <a name="billing-types"></a>Tipuri de facturare

Câmpul **Tip de facturare** definește conceptul de exigibilitate în PSA. Este un set de opțiuni care are următoarele valori posibile:

- **Tarifabil** – costul care este acumulat de acest rol/categorie este un cost direct care determină executarea proiectului, iar clientul va plăti pentru această lucrare. Plata poate fi administrată ca un aranjament de timp și materiale sau cu preț fix. Cu toate acestea, angajatul care petrece acest timp va primi creditul corespunzător pentru utilizarea sa facturabilă.
- **Netarifabil** – costul care este acumulat de acest rol/categorie este considerat un cost direct care determină executarea proiectului, chiar dacă clientul nu recunoaște acest fapt și nu va plăti pentru această lucrare. Angajatul care petrece acest timp nu va fi creditat cu utilizare facturabilă pentru el.
- **Gratuit** – costul care este acumulat de acest rol/categorie este considerat un cost direct care determină executarea proiectului, iar clientul recunoaște acest fapt. Angajatul care petrece acest timp va fi creditat pentru utilizarea facturabilă pentru el. Cu toate acestea, acest cost nu este tarifat clientului.
- **Indisponibil** – costurile suportate pentru proiecte interne care nu necesită urmărirea veniturilor sunt urmărite utilizând această opțiune.

## <a name="invoice-schedule"></a>Planificare factură

O planificare a facturilor este o serie de date când se produce facturarea pentru un proiect. Opțional, puteți crea o planificare a facturilor pe o linie de ofertă în PSA. Fiecare linie de ofertă poate avea propria planificare a facturilor. Pentru a crea o planificare a facturilor, trebuie să furnizați următoarele valori de atribut:

- O dată de început facturare 
- O dată de livrare care reprezintă data de încheiere a facturării pe proiect
- O frecvență a facturilor

PSA utilizează aceste trei valori de atribut pentru a genera un set provizoriu de date pe baza căruia stabilește facturarea.

## <a name="invoice-frequency"></a>Frecvență facturi

Frecvența facturilor este o entitate care stochează valorile atributelor care ajută la exprimarea frecvenței creării de facturi. Următoarele atribute exprimă sau definesc entitatea Frecvență facturi:

- **Perioada** – sunt acceptate perioadele lunare, bisăptămânale și săptămânale. 
- **Rulări pe perioadă** – pentru perioade săptămânale și bisăptămânale, aveți posibilitatea să definiți doar o singură rulare pe perioadă. Pentru perioadele lunare, puteți defini între una și patru rulări pe perioadă. 
- **Zile de rulare** – zilele când facturarea trebuie executată. Puteți configura acest atribut în două moduri diferite:
  - **Zile lucrătoare** – de exemplu, aveți posibilitatea să specificați că facturarea se execută în fiecare luni sau în fiecare luni din două în două săptămâni. Clienții care trebuie să seteze facturarea să se execute într-o zi lucrătoare ar putea prefera acest tip de configurație. 
  - **Zile calendaristice** – de exemplu, aveți posibilitatea să specificați că facturarea se execută în a șaptea și a douăzeci și una zi a fiecărei luni. Unele organizații pot prefera acest tip de configurație, deoarece contribuie la garantarea faptului că facturarea se execută după un program fix în fiecare lună.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Planificarea facturii pentru o linie de ofertă cu preț fix

Pentru o linie de ofertă cu preț fix, aveți posibilitatea să utilizați grila **Planificare factură** pentru a crea jaloane de facturare care să fie egale cu valoarea liniei de ofertă.

- Pentru a crea jaloane de facturare care sunt împărțite în mod egal, selectați o frecvență a facturilor, introduceți data de începere a facturării pe linia de ofertă și selectați **Dată de finalizare solicitată** pentru ofertă în secțiunea **Rezumat** a antetului de ofertă. Apoi selectați **Generare jaloane periodice** pentru a crea jaloane divizate în mod egal pe baza frecvenței selectate a facturilor. 
- Pentru a crea un jalon de facturare cu sumă forfetară, creați un jalon, apoi introduceți valoarea liniei de ofertă ca sumă a jalonului.
- Pentru a crea jaloane de facturare care se bazează pe anumite activități din planul de proiect, creați un jalon și mapați-l la elementul de planificare al proiectului în IU pentru jaloanele de facturare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]