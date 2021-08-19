---
title: Estimarea unei linii de contract pentru proiect
description: Acest subiect oferă informații despre cum estimările unei linii de contract de proiect.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ae2d96170348a00b58f1571b6c9b31af894c281bdfdfcb00f4e348b2705186c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986911"
---
# <a name="estimate-a-project-contract-line"></a>Estimarea unei linii de contract pentru proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_ 

În Dynamics 365 Project Operations, o linie de contract pe bază de proiect conține detalii care ajută la estimarea costului și a veniturilor potențiale ale lucrărilor implicate pentru livrarea liniei de contract.

Pentru a estima o linie de contract bazată pe proiect, accesați fila **Detaliu linie contract** de pe **Linie de contract** bazată pe proiect.  Există două moduri de a crea o estimare pe o linie de contract bazată pe proiect:

   - Creați o estimare direct pe linia contractului adăugând manual detaliile liniei contractului.
   - Creați un proiect și un plan de proiect, apoi asociați proiectul și sarcinile la linia contractuală a proiectului. Aceasta permite procesul prin care puteți importa estimarea planului de proiect în linia contractului pe baza componentelor incluse pe linia contractului.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Crearea unei estimări direct într-o linie de contract a unui proiect

Pentru a crea o estimare direct pe o linie de contract bazată pe proiect, urmați acești pași:

1. Accesați linia de și selectați fila **Detaliu linie contract**. Liniile pe care le creați în această filă sunt rezumate și afișate ca **Valoarea contractată** pentru această **Linie de contract**. 
2. În subgrila **Detalii linie contract**, selectați **Detaliu linie contract nouă**. Se deschide un glisor de creare rapidă. Următoarele câmpuri sunt disponibile pe pagina **Detalii linie contract**.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| **Descriere** | **Creați rapid** | O descriere a estimării specifice. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Clasă de tranzacții** | **Creați rapid** | Această listă a claselor de tranzacții este inclusă în fila **General** a liniei de contract bazate pe proiect. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Selectare produs** | **Creare rapidă** | Se aplică atunci când clasa tranzacției este **Material**. Puteți selecta să specificați că această linie estimativă este pentru un produs **Existent** (de catalog) sau un produs **Din afara catalogului**. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Produs** | **Creare rapidă** | ID-ul produsului din catalogul de produse. Acest câmp este activat numai atunci când selectați **Produs existent** în câmpul **Selectare Produs**. ID-ul este utilizat pentru a prelua prețul de vânzare din lista de prețuri a proiectului de pe contract. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Produs din afara catalogului** | **Creare rapidă** | Un câmp text pentru a introduce numele produsului. Acest câmp este activat numai atunci când selectați **Din afara catalogului** în câmpul **Selectare Produs**.| Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Rol** | **Creați rapid** | Rolul persoanei care efectuează această lucrare sau suportă această cheltuială. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat.|
| **Categorie** | **Creați rapid** | Categoria de lucru sau cheltuială. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat.|
| **Data de început** | **Creați rapid** | Data de început a lucrului. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Dată de sfârşit** | **Creați rapid** | Data de final a lucrului. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Firmă de resurse** | **Creați rapid** | Compania de resurse sau entitatea juridică care suportă acest cost și care oferă resursa pentru a se lucra pe ea. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat și este utilizată în preluarea prețului de cost. |
| **Unitate de resurse** | **Creați rapid** | Unitatea de resurse care suportă acest cost și care oferă resursa pentru a se lucra pe ea. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat și este utilizată în preluarea prețului de cost. |
| **Planificare unitate** | **Creare rapidă** | Grupul de unitate pentru activitate, produs sau cheltuială. Unitățile aparțin unei planificări de unitate sau unui grup de unități. De exemplu, *mile* și *kilometri (km)* sunt unități care aparțin unui grup de unități care descriu distanța. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Unitate** | **Creați rapid** | Unitatea de activitate, produs sau cheltuială. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Cantitate** | **Creați rapid** | Cantitatea de activitate, produs sau cheltuială. | Această valoare este setată implicit la detaliul liniei de contract aferente pentru costul creat automat. |
| **Preț unitar** | **Creați rapid** | Rata de facturare a rolului care efectuează lucrarea, prețul pe unitate al produsului sau prețul de vânzare al produsului sau categoriei de cheltuieli. Valoarea implicită pentru **Timp** se bazează pe combinația valorilor de dimensiune de stabilire a prețurilor de pe linia de preț a rolului din lista de prețuri a proiectului, care este în vigoare la data de începere. Pentru **Cheltuieli**, valoarea implicită a acestui câmp este de la setarea prețului pentru categoria de tranzacții din lista de prețuri a proiectului, care este valabilă pentru data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este **prețul pe unitate**, nu există nicio valoare implicită și acest câmp este lăsat necompletat. Pentru produse, valoarea implicită a acestui câmp se bazează pe linia **Articol din lista de prețuri** din lista de prețuri a proiectului care este în vigoare la data de începere.| Rata de cost a rolului care efectuează lucrarea sau costul pe unitate din categoria de cheltuieli sau costul unitar al produsului. Valoarea implicită pentru **Timp** se bazează pe combinația valorilor de dimensiune de stabilire a prețurilor de pe linia de preț a rolului din lista de prețuri de cost atașată unității contractante, în vigoare la data de începere. Pentru **Cheltuieli**, valoarea implicită pentru cest câmp se bazează pe linia de preț a categoriei din lista de prețuri de cost atașată unității contractante, în vigoare la data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul pe unitate, nu există nicio valoare implicită și acest câmp este lăsat necompletat. Pentru produse, valoarea implicită a acestui câmp se bazează pe linia **Element listă de preț** din lista de prețuri de cost atașată unității contractante, în vigoare la data de începere.|
| **Impozit estimat** | **Creați rapid** | Impozitul estimat pentru această lucrare sau cheltuială ca intrare de către utilizator. | &nbsp; |
| **Sumă** | **Creați rapid** | Valoarea din acest câmp se poate adăuga în cazul în care câmpurile **Cantitate** și **Preț** sunt lăsate necompletate. Dacă sunt completate câmpurile **Cantitate** și **Preț**, câmpul **Valoare** este numai în citire și este calculat ca **(Cantitate \* Preț unitar) + Taxe**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualizați prețurile în detaliile liniei contractului

Dacă modificați prețurile din lista de prețuri a proiectului care este atașată contractului sau lista de prețuri a costului unității contractante, puteți actualiza prețurile din detaliile liniei contractuale individuale pentru a reflecta modificarea. Pe pagina **Contract**, selecta'i **Recalculare**. Apare un avertisment pentru a vă informa că prețurile pentru toate liniile contractuale din acest contract sunt resetate. Selectați **Da** pentru a reîmprospăta prețurile atât pentru detaliile liniei contractului de vânzare, cât și pentru cele de cost.

## <a name="access-contract-line-details-for-cost"></a>Accesați detaliile liniei contractului pentru cost

Pe fila **Detalii despre linia de contracct**, selectați un rând din grilă pentru a afișa acțiuni pe bara de instrumente a subgrilei. Prima acțiune pe bara de instrumente subgrilă este **Deschideți detaliile costurilor**. Pentru a vedea rata de cost aferentă și suma pentru această linie de contract, selectați **Deschideți detaliile costurilor**. 

> [!NOTE]
> Schimbarea valorii companiei de resurse, a unității de resurse, a cantității, a datelor, a rolului sau a valorilor categoriei pe detaliile liniei contractului pentru **Cost** modifică, de asemenea, valorile corespunzătoare pe detaliul liniei de contract pentru **Vânzări**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moneda pe detaliile liniei contractului pentru cost și vânzări

Detaliile liniei contractului pentru **Vânzări** setează moneda implicită din lista de prețuri a proiectului care este efectivă pentru data de începere a detaliilor liniei contractului.

Detaliul liniei de contract pentru **Cost** seetează moneda implicită din lista de prețuri a unității contractante care este efectivă pentru data de începere a detaliului de linie de contract pentru **Cost**.

Calculele de rentabilitate convertesc sumele pentru detaliile liniei contractului pentru **Cost** și **Vânzări** în moneda de bază a mediului pentru a raporta marjele reale reale și estimate pe contract.

> [!NOTE]
> Erorile de rotunjire a valutei și modificarea marjelor ar putea apărea din cauza lipsei ratelor de schimb efective la dată. Utilizați aceste calcule numai la contractele proiectului, deoarece acestea sunt aproximări și nu sunt pentru raportări legale sau de altă natură care necesită o precizie mai mare a rotunjirii și conștientizarea aplicabilității datei pentru ratele de schimb.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
