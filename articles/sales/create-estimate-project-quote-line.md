---
title: Estimarea unei linii de ofertă de proiect
description: Acest subiect oferă informații despre cum să creați o estimare a unei linii de ofertă de proiect.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 96a83bb51864297098db28588e22197d78462fa2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580011"
---
# <a name="estimate-a-project-quote-line"></a>Estimarea unei linii de ofertă de proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

O linie de ofertă bazată pe proiecte conține detalii care ajută la estimarea costului și a veniturilor potențiale ale lucrărilor implicate pentru livrarea liniei de ofertă.

Pentru a estima o linie de ofertă de proiect, pe linia ofertei selectați fila **Detalii linie ofertă**. Există două moduri de a crea o estimare pe o linie de ofertă bazată pe proiect:

   - Creați manual estimarea direct pe linia de ofertă folosind detaliile liniei de ofertă. 
   - Creați un proiect și un plan de proiect, apoi asociați proiectul și sarcinile proiectului la linia de ofertă. Va fi activat procesul de importare a estimărilor din planul de proiect în linia de ofertă pe baza informațiilor furnizate de dvs.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Creați estimările direct pe o linie de ofertă pe bază de proiect

Pentru a crea estimări direct pe o linie de ofertă bazată pe proiect, urmați acești pași:

1. Pentru a crea o ofertă pe o linie de ofertă bazată pe proiect, selectați fila **Detalii linie ofertă**. Elementul rând pe care îl creați în această filă va rezuma valoarea ofertată pentru acest rând de ofertă. 
2. Pentru a crea detalii despre linia de ofertă, selectați **Detaliu linie de ofertă nou** pe subgrila **Detalii despre linia de ofertă**. Se va deschide un glisor de creare rapidă. Următoarele câmpuri de pe pagina **Linie de ofertă**.

| **Câmp** | **Locație** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Descriere | Creare rapidă | O descriere a estimării specifice. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Clasă de tranzacții | Creare rapidă | Această listă derulantă oferă clasele de tranzacții care sunt incluse în fila **General** a liniei de ofertă bazată pe proiect.  | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Selectare produs | Creare rapidă | Se aplică atunci când clasa tranzacției este **Material**. Puteți selecta să specificați că această linie estimativă este pentru un produs (de catalog) **Existent** sau un produs **Din afara catalogului**. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Produs | Creare rapidă | ID-ul produsului din catalogul de produse. Acest câmp este activat numai atunci când selectați **Existent** în câmpul **Selectare Produs**. ID-ul este utilizat pentru a prelua prețul de vânzare din lista de prețuri a proiectului de pe ofertă. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Produs din afara catalogului | Creare rapidă | O casetă de text pentru a scrie în numele produsului. Acest câmp este activat numai atunci când selectați **Din afara catalogului** în câmpul **Selectare Produs**.| Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Rol | Creare rapidă | Rolul persoanei care va efectua această lucrare sau care va suporta această cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Categorie | Creare rapidă | Categoria de lucru sau cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Data de început | Creare rapidă | Data de început a lucrului. | Acest câmp este setat implicit la detaliul liniei de ofertă pentru costul creat automat. |
| Data de sfârșit | Creare rapidă | Data de final a lucrului. | Acest câmp este setat implicit la detaliul liniei de ofertă pentru costul creat automat. |
| Firmă de resurse | Creați rapid | Compania de resurse sau entitatea juridică care suportă acest cost și care oferă resursa pentru a se lucra pe ea. | Valoarea este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat și este utilizată în preluarea prețului de cost. |
| Unitate de resurse | Creare rapidă | Unitatea de resurse care suportă acest cost și care oferă resursa pentru a se lucra pe ea. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat și este utilizată în preluarea prețului de cost. |
| Planificare unitate | Creare rapidă | Grupul de unitate pentru activitate, produs sau cheltuială. Unitățile aparțin unei planificări de unitate sau unui grup de unități. De exemplu, mile și kilometri sunt unități care aparțin unui grup de unități care descrie distanța. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Unitate | Creare rapidă | Unitatea de activitate, produs sau cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Cantitate | Creare rapidă | Cantitatea de activitate, produs sau cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Preț unitar | Creați rapid |Rata de facturare a rolului care efectuează lucrarea, prețul pe unitate al produsului sau prețul de vânzare al produsului sau categoriei de cheltuieli. Valoarea implicită pentru **Timp** se bazează pe combinația valorilor de dimensiune de stabilire a prețurilor de pe linia de preț a rolului din lista de prețuri a proiectului, care este în vigoare la data de începere. Pentru **Cheltuieli**, valoarea implicită este din setarea prețului pentru categoria de tranzacții din lista de prețuri a proiectului, în vigoare la data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul pe unitate, nu există nicio valoare implicită și acest câmp este lăsat necompletat. Pentru produse, valoarea implicită a acestui câmp se bazează pe linia **Articol din lista de prețuri** din lista de prețuri a proiectului care este în vigoare la data de începere.| Rata de cost a rolului care efectuează lucrarea, costul pe unitate din categoria de cheltuieli sau costul unitar al produsului. Valoarea implicită pentru **Timp** se bazează pe combinația valorilor de dimensiune de stabilire a prețurilor de pe linia de preț a rolului din lista de prețuri de cost atașată unității contractante, în vigoare la data de începere. Pentru cheltuieli, valoarea implicită se bazează pe linia de preț a categoriei din lista de prețuri de cost atașată unității contractante, în vigoare la data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul unitar, nu există nicio valoare implicită și acest câmp este lăsat necompletat. Pentru produse, valoarea implicită a acestui câmp se bazează pe linia **Element listă de preț** din lista de prețuri de cost atașată unității contractante, în vigoare la data de începere.|
| Impozit estimat | Creare rapidă | Puteți introduce manual taxa estimată pentru această lucrare sau cheltuială. | Nu există niciun impact în aval pentru acest câmp. |
| Sumă | Creare rapidă | Puteți introduce manual informații în acest câmp dacă câmpurile **Cantitate** și **Preț** sunt lăsate necompletate. Dacă aceste câmpuri nu sunt goale, acest câmp devine numai în citire și se calculează drept (Cantitate \* Preț unitar) + Taxă. | Nu există niciun impact în aval pentru acest câmp. |

## <a name="update-prices-on-quote-line-details"></a>Actualizați prețurile în detaliile liniei de ofertă

Dacă ați modificat prețurile în lista de prețuri a proiectului care este atașată la ofertă sau în lista de prețuri a costului unității contractante, puteți selecta pagina **Recalculează** pe pagina **Ofertă**, pentru a reîmprospăta prețurile din detaliile liniei de ofertă individuale pentru a reflecta această modificare. Când selectați **Recalculare**, apare un avertisment care vă informează că vor fi resetate prețurile din detaliile liniei de ofertă pentru toate liniile de ofertă din această ofertă. Selectați **Da** pentru a reîmprospăta prețurile atât pentru vânzări, cât și pentru detaliile liniei de ofertă.

## <a name="access-quote-line-details-for-cost"></a>Accesați detaliile liniei de ofertă pentru cost

Pentru a accesa detaliile liniei de ofertă pentru cost, urmați acești pași:

1. Pe fila **Detalii despre linia de ofertă**, selectați un rând din grilă pentru a activa acțiuni pe bara de instrumente a subgrilei. 
2. Selectați **Deschideți detaliile costurilor** pentru a vedea rata de cost aferentă și suma pentru această linie de ofertă.

> [!NOTE]
> Modificarea valorilor unității de resurse, cantității, datele, rolul sau categoriile din detaliile liniei de ofertă pentru costuri vor modifica valorile corespunzătoare din detaliile liniei de ofertă pentru vânzări.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moneda pe detaliile liniei de ofertă pentru cost și vânzări

Moneda din detaliul liniei de ofertă pentru valorile implicite din lista de prețuri a proiectului, care este valabilă la data de începere a detaliului liniei de ofertă.

Moneda din detaliul liniei de ofertă pentru valorile implicite ale costului pentru unitatea contractantă a ofertei, care este valabilă la data de începere a detaliului liniei de ofertă pentru cost.

> [!NOTE]
> Calculele de rentabilitate convertesc suma din detaliile liniei de ofertă pentru costuri și vânzări în moneda de bază a mediului pentru a raporta marja generală estimată la ofertă. Erorile de rotunjire a valutei și modificarea marjelor ar putea apărea din cauza lipsei ratelor de schimb efective la dată. Utilizați aceste calcule numai la ofertele proiectului, deoarece acestea sunt aproximări și nu sunt raportări legale sau de altă natură care necesită o precizie mai mare a rotunjirii și conștientizarea aplicabilității datei pentru ratele de schimb.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
