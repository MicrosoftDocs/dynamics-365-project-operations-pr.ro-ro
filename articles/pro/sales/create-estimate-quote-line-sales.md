---
title: Estimarea unei linii de ofertă pe bază de proiect
description: Acest subiect oferă informații despre cum să creați o estimare pe o linie de ofertă pe bază de proiect.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273567"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimarea unei linii de ofertă pe bază de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

O linie de ofertă bazată pe proiecte conține detalii care ajută la estimarea costului și a veniturilor potențiale ale lucrărilor implicate pentru livrarea liniei de ofertă.

Pentru a estima o linie de ofertă bazată pe proiect, pe linia de estimare bazată pe ofertă, selectați fila **Detalii linie ofertă**. Există două moduri de a crea o ofertă pe o linie de ofertă bazată pe proiect:

- Creați manual estimarea direct pe linia de ofertă folosind detaliile liniei de ofertă 
- Creați un proiect și un plan de proiect, apoi asociați proiectul și sarcinile proiectului la linia de ofertă. Va fi activat procesul de importare a estimărilor din planul de proiect în linia de ofertă pe baza informațiilor furnizate de dvs.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Creați estimările direct pe o linie de ofertă pe bază de proiect

Pentru a crea o ofertă pe o linie de ofertă bazată pe proiect, selectați fila **Detalii linie ofertă**. Elementul rând pe care îl creați în această filă va rezuma valoarea ofertată pentru acest rând de ofertă. 

Pentru a crea detalii despre linia de ofertă, selectați **+ Detaliu linie de ofertă nouă** pe subgrila **Detalii despre linia de ofertă**. Se va deschide un glisor de creare rapidă. Următoarele câmpuri de pe formularul **Linie ofertă**:

| **Câmp** | **Locaţie** | **Descriere** | **Impactul din aval** |
| --- | --- | --- | --- |
| Descriere | Creare rapidă | O descriere a estimării specifice. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Clasă de tranzacții | Creare rapidă | Această listă derulantă oferă clasele de tranzacții care sunt incluse în fila **General** a liniei de ofertă bazată pe proiect.  | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Rol | Creare rapidă | Persoana care va efectua această lucrare sau va suporta această cheltuială. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Categorie | Creare rapidă | Categoria lucrului sau cheltuielii. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Data de început | Creare rapidă | Data de început a lucrului. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Data de sfârșit | Creare rapidă | Data de încheiere a lucrului. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Unitate de finanțare | Creare rapidă | Unitate de resurse care va suporta acest cost și va oferi resursa pentru a lucra la acesta. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. Acest câmp este, de asemenea, utilizat în recuperarea prețurilor de cost. |
| Planificare unitate | Creare rapidă | Grup de unități al lucrului sau cheltuielii. Unitățile aparțin unei planificări de unitate sau unui grup de unități. De exemplu, mile și km sunt unități care aparțin unui grup de unități care descrie distanța. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Unitate | Creare rapidă | Unitatea lucrului sau cheltuielii. | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Cantitate | Creare rapidă | Cantitatea de lucru sau cheltuială | Acest câmp implicit se referă la detaliile referitoare la linia de ofertă pentru costul creat automat. |
| Preț unitar | Creare rapidă | Rata facturii pentru rolul care efectuează lucrarea sau Prețul de vânzare al categoriei de cheltuieli. Acest câmp implicit pentru Timp se bazează pe rolul și combinația de unități de resurse din lista de prețuri a proiectului care este efectivă pentru data de începere. Pentru cheltuieli, acest câmp este implicit din setarea prețului pentru categoria de tranzacții din lista de prețuri a proiectului, care este valabilă pentru data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul pe unitate, nu există nicio valoare implicită și acest câmp este lăsat necompletat. | Rata de cost pentru rolul care efectuează lucrarea sau costul per unitate al categoriei de cheltuieli. Acest câmp implicit pentru Timp se bazează pe rolul și combinația de preț a unității contractante a listei de prețuri de ofertă care începe de la data de începere. Pentru cheltuieli, acest câmp este implicit din setarea prețului pentru categoria de tranzacții din lista cu prețuri de cost a unității contractante care este valabilă pentru data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul pe unitate, nu există nicio valoare implicită și acest câmp este lăsat necompletat. |
| Impozit estimat | Creare rapidă | Puteți introduce manual taxa estimată pentru această lucrare sau cheltuială. | Nu există niciun impact din aval al acestui domeniu. |
| Sumă | Creare rapidă | Puteți introduce manual informații în acest câmp dacă câmpurile **Cantitate** și **Preț** sunt lăsate necompletate. Dacă aceste câmpuri nu sunt necompletate, acest câmp devine numai în citire și se calculează drept (Cantitate \* Preț unitar) + Taxă. | Nu există niciun impact din aval al acestui domeniu. |

## <a name="update-prices-on-quote-line-details"></a>Actualizați prețurile în detaliile liniei de ofertă

Dacă ați modificat prețurile în lista de prețuri a proiectului care este atașată la ofertă sau în lista de prețuri a costului unității contractante, puteți selecta pagina **Recalculează** pe pagina **Ofertă**, pentru a reîmprospăta prețurile din detaliile liniei de ofertă individuale pentru a reflecta această modificare. Când selectați **Recalculează**, apare un avertisment care vă informează că prețurile din detaliile liniei de ofertă pentru toate liniile de ofertă din această ofertă vor fi resetate. Selectați **Da**, pentru a reîmprospăta prețurile atât pentru vânzări, cât și pentru detaliile liniei de ofertă.

## <a name="access-quote-line-details-for-cost"></a>Accesați detaliile liniei de ofertă pentru cost

Pe fila **Detalii despre linia de ofertă**, selectați un rând din grilă pentru a activa unele acțiuni pe bara de instrumente a subgrilei. Prima acțiune pe bara de instrumente subgrilă atunci când este selectat un detaliu al liniei de ofertă este **Deschideți detaliile costurilor**. Selectați **Deschideți detaliile costurilor** pentru a vedea rata de cost aferentă și suma pentru această linie de ofertă.

> [!NOTE]
> Modificarea valorilor unității de resurse, cantității, datele, rolul sau categoriile din detaliile liniei de ofertă pentru costuri vor modifica valorile corespunzătoare din detaliile liniei de ofertă pentru vânzări.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moneda pe detaliile liniei de ofertă pentru cost și vânzări

Moneda din detaliul liniei de ofertă pentru valorile implicite din lista de prețuri a proiectului, care este valabilă pentru data de începere a detaliului liniei de ofertă.

Moneda din detaliul liniei de ofertă pentru valorile implicite de cost din lista de prețuri a unității de contractare a ofertei care este activă pentru data de început a detaliului liniei de ofertă pentru cost.

Calculele de rentabilitate convertesc suma din detaliile liniei de ofertă pentru costuri și vânzări în moneda de bază a mediului pentru a raporta marja generală estimată la ofertă.

Acest lucru ar putea duce la erori de rotunjire a valutei și la modificarea marjelor din cauza lipsei ratelor de schimb efective de dată. Utilizați aceste calcule în cotațiile proiectului doar ca aproximări și nu raportări statutare sau de altă natură care necesită o precizie mai mare a rotunjirii și conștientizarea efectivității datei pentru ratele de schimb.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]