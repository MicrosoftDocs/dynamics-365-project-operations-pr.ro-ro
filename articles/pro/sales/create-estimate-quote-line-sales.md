---
title: Estimarea unei linii de ofertă de proiect
description: Acest articol oferă informații despre cum să creați o estimare pe o linie de ofertă de proiect.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bac3a3fa2d14c857edfb469a005406c346c8dbf6
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826003"
---
# <a name="estimate-a-project-quote-line"></a>Estimarea unei linii de ofertă de proiect

_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_

O linie de ofertă bazată pe proiecte conține detalii care ajută la estimarea costului și a veniturilor potențiale ale lucrărilor implicate pentru livrarea liniei de ofertă.

Pentru a estima o linie de ofertă bazată pe proiect, pe linia de estimare bazată pe ofertă, selectați fila **Detalii linie ofertă**. Există două moduri de a crea o ofertă pe o linie de ofertă bazată pe proiect:

- Creați manual estimarea direct pe linia de ofertă folosind detaliile liniei de ofertă. 
- Creați un proiect și un plan de proiect, apoi asociați proiectul și sarcinile proiectului la linia de ofertă. Va fi activat procesul de importare a estimărilor din planul de proiect în linia de ofertă pe baza informațiilor furnizate de dvs.

## <a name="create-estimates-directly-on-a-project-quote-line"></a>Creați estimări direct pe o linie de ofertă de proiect

Pentru a crea o ofertă pe o linie de ofertă bazată pe proiect, selectați fila **Detalii linie ofertă**. Elementul rând pe care îl creați în această filă va rezuma valoarea ofertată pentru acest rând de ofertă. 

Pentru a crea detalii despre linia de ofertă, selectați **Detaliu linie de ofertă nou** pe subgrila **Detalii despre linia de ofertă**. Se va deschide un glisor de creare rapidă. Următorul tabel oferă detalii despre câmpurile de pe pagina **Detalii linie ofertă** și modul în care valorile au impact asupra funcționalității.

| **Câmp** | **Locație** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Descriere | Creare rapidă | O descriere a estimării specifice. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Clasă de tranzacții | Creare rapidă | Această listă derulantă oferă clasele de tranzacții care sunt incluse în fila **General** a liniei de ofertă bazată pe proiect.  | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Selectare produs | Creare rapidă | Se aplică atunci când clasa tranzacției este **Material**. Puteți selecta să specificați că această linie estimativă este pentru un produs (de catalog) **Existent** sau un produs **Din afara catalogului**. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Produs | Creare rapidă | ID-ul produsului din catalogul de produse. Acest câmp este activat numai dacă selectați **Existent** în câmpul **Selectare Produs**. ID-ul este utilizat pentru a prelua prețul de vânzare din lista de prețuri a proiectului de pe ofertă. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Produs din afara catalogului | Creare rapidă | O casetă text pentru a introduce numele produsului. Acest câmp este activat numai dacă selectați **Din afara catalogului** în câmpul **Selectare Produs**.| Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Rol | Creare rapidă | Rolul persoanei care va efectua această lucrare sau care va suporta această cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Categorie | Creare rapidă | Categoria de lucru sau cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Data de început | Creare rapidă | Data de început a lucrului. | Acest câmp este setat implicit la detaliul liniei de ofertă pentru costul creat automat. |
| Data de sfârșit | Creare rapidă | Data de final a lucrului. | Acest câmp este setat implicit la detaliul liniei de ofertă pentru costul creat automat. |
| Unitate de resurse | Creare rapidă | Unitatea de resurse care va suporta acest cost și care oferă resursa pentru a se lucra pe ea. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat și este utilizată în preluarea prețului de cost. |
| Planificare unitate | Creare rapidă | Grupul de unitate pentru activitate, produs sau cheltuială. Unitățile aparțin unei planificări de unitate sau unui grup de unități. De exemplu, mile și kilometri sunt unități care aparțin unui grup de unități care descrie distanța. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Unitate | Creare rapidă | Unitatea de activitate, produs sau cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Cantitate | Creare rapidă | Cantitatea de activitate, produs sau cheltuială. | Această valoare este setată implicit la detaliul liniei de ofertă aferente pentru costul creat automat. |
| Preț unitar | Creați rapid |Rata de facturare a rolului care efectuează lucrarea, prețul pe unitate al produsului sau prețul de vânzare al produsului sau categoriei de cheltuieli. Valoarea implicită pentru acest câmp este **Timp** pe baza combinației valorilor de dimensiune de stabilire a prețurilor de pe linia de preț a rolului din lista de prețuri a proiectului, care este în vigoare la data de începere. Pentru **Cheltuieli**, valoarea implicită este din setarea prețului pentru categoria de tranzacții din lista de prețuri a proiectului, în vigoare la data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul unitar, nu există nicio valoare implicită și acest câmp este lăsat necompletat. Pentru produse, valoarea implicită a acestui câmp se bazează pe linia **Articol din lista de prețuri** din lista de prețuri a proiectului care este în vigoare la data de începere.| Rata de cost a rolului care efectuează lucrarea, costul pe unitate din categoria de cheltuieli sau costul unitar al produsului. Valoarea implicită pentru acest câmp este **Timp** pe baza combinației valorilor de dimensiune de stabilire a prețurilor de pe linia de preț a rolului din lista de prețuri a proiectului, care este în vigoare la data de începere. Pentru **Cheltuieli**, valoarea implicită este din setarea prețului pentru categoria de tranzacții din lista de prețuri a proiectului, în vigoare la data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul unitar, nu există nicio valoare implicită și acest câmp este lăsat necompletat. Pentru produse, valoarea implicită a acestui câmp se bazează pe linia **Articol din lista de prețuri** din lista de prețuri a proiectului care este în vigoare la data de începere.|
| Impozit estimat | Creare rapidă | Puteți introduce manual taxa estimată pentru această lucrare sau cheltuială. | Nu există niciun impact în aval pentru acest câmp. |
| Sumă | Creare rapidă | Puteți introduce manual informații în acest câmp dacă câmpurile **Cantitate** și **Preț** sunt lăsate necompletate. Dacă aceste câmpuri nu sunt goale, acest câmp devine numai în citire și se calculează drept (Cantitate \* Preț unitar) + Taxă. | Nu există niciun impact în aval pentru acest câmp. |


## <a name="update-prices-on-quote-line-details"></a>Actualizați prețurile în detaliile liniei de ofertă

Dacă ați modificat prețurile în lista de prețuri a proiectului care este atașată la ofertă sau în lista de prețuri a unității contractante, puteți selecta **Recalculare** pe pagina **Ofertă** pentru a reîmprospăta prețurile din detaliile liniei de ofertă individuale pentru a reflecta această modificare. Când selectați **Recalculare**, apare un avertisment care vă informează că vor fi resetate prețurile din detaliile liniei de ofertă pentru toate liniile de ofertă din această ofertă. Selectați **Da** pentru a reîmprospăta prețurile atât pentru vânzări, cât și pentru detaliile liniei de ofertă.

## <a name="access-quote-line-details-for-cost"></a>Accesați detaliile liniei de ofertă pentru cost

Pe fila **Detalii despre linia de ofertă**, selectați un rând din grilă pentru a activa unele acțiuni pe bara de instrumente a subgrilei. Prima acțiune pe bara de instrumente subgrilă atunci când este selectat un detaliu al liniei de ofertă este **Deschideți detaliile costurilor**. Selectați **Deschideți detaliile costurilor** pentru a vedea rata de cost aferentă și suma pentru această linie de ofertă.

> [!NOTE]
> Modificarea valorilor unității de resurse, cantității, datele, rolul sau categoriile din detaliile liniei de ofertă pentru costuri vor modifica valorile corespunzătoare din detaliile liniei de ofertă pentru vânzări.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moneda pe detaliile liniei de ofertă pentru cost și vânzări

Moneda din detaliul liniei de ofertă pentru valorile implicite din lista de prețuri a proiectului, care este valabilă pentru data de începere a detaliului liniei de ofertă.

Moneda din detaliul liniei de ofertă pentru valorile implicite de cost din lista de prețuri a unității de contractare a ofertei care este activă pentru data de început a detaliului liniei de ofertă pentru cost.

Calculele de rentabilitate convertesc suma din detaliile liniei de ofertă pentru costuri și vânzări în moneda de bază a mediului pentru a raporta marja generală estimată la ofertă.

> [!NOTĂ Erorile de rotunjire a monedei și marjele modificate pot apărea din cauza lipsei cursurilor de schimb efective ale datei. Utilizați aceste calcule numai la contractele proiectului, deoarece acestea sunt aproximări și nu sunt pentru raportări legale sau de altă natură care necesită o precizie mai mare a rotunjirii și conștientizarea aplicabilității datei pentru ratele de schimb.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
