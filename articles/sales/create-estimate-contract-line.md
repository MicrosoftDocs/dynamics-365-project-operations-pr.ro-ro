---
title: Estimarea unei linii de contract bazate pe proiect
description: Acest subiect oferă informații despre estimări pe o linie de contract bazate pe proiect.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180477"
---
# <a name="estimate-a-projectbased-contract-line"></a>Estimarea unei linii de contract bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_ 

În Dynamics 365 Project Operations, o linie de contract pe bază de proiect conține detalii care ajută la estimarea costului și a veniturilor potențiale ale lucrărilor implicate pentru livrarea liniei de contract.

Pentru a estima o linie de contract bazată pe proiect, accesați fila **Detaliu linie contract** de pe **Linie de contract** bazată pe proiect.  Există două moduri de a crea o estimare pe o linie de contract bazată pe proiect:

   - Creați o estimare direct pe linia contractului adăugând manual detaliile liniei contractului.
   - Creați un proiect și un plan de proiect, apoi asociați proiectul și sarcinile la linia contractuală a proiectului. Aceasta permite procesul prin care puteți importa estimarea planului de proiect în linia contractului pe baza componentelor incluse pe linia contractului.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Creați o estimare direct pe o linie de contract bazată pe proiect

1. Accesați linia de și selectați fila **Detaliu linie contract**. Liniile pe care le creați în această filă sunt rezumate și afișate ca **Valoarea contractată** pentru această **Linie de contract**. 
2. În subgrila **Detalii linie contract**, selectați **+ Detaliu linie contract nouă**. Se deschide un glisor de creare rapidă. Următoarele câmpuri sunt disponibile pe formularul **Detalii linie contract**:

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| **Descriere** | **Creare rapidă** | O descriere a estimării specifice. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Clasă de tranzacții** | **Creare rapidă** | Această listă derulantă este o listă a claselor de tranzacții incluse în fila **General** a liniei de contract bazate pe proiect. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Rol** | **Creare rapidă** | Rolul persoanei care efectuează această lucrare sau suportă această cheltuială. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Categorie** | **Creare rapidă** | Categoria de lucru sau cheltuială. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Dată de început** | **Creare rapidă** | Data de început a lucrului. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Dată de sfârşit** | **Creare rapidă** | Data de final a lucrului. | Acest câmp implicit este detaliul liniei contractului aferent pentru costul creat automat. |
| **Firmă de resurse** | **Creare rapidă** | Compania resurse sau entitatea juridică care suportă acest cost și furnizează resursa pentru a lucra la acesta. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. Acest câmp este, de asemenea, utilizat în recuperarea prețurilor de cost. |
| **Unitate de finanțare** | **Creare rapidă** | Unitatea de resurse care suportă acest cost și furnizează resursa pentru a lucra la acesta. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. Acest câmp este, de asemenea, utilizat în recuperarea prețurilor de cost. |
| **Planificare unitate** | **Creare rapidă** | Grupul unitar al lucrului sau cheltuielilor. Unitățile aparțin unei planificări de unitate sau unui grup de unități. De exemplu, *mile* și *kilometri (Kms)* sunt unități care aparțin unui grup de unități care descriu distanța. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Unitate** | **Creare rapidă** | Unitatea de lucru sau cheltuială. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Cantitate** | **Creare rapidă** | Cantitatea de lucru sau cheltuială. | Acest câmp implicit este detaliul liniei contractului aferent pentru costurile care sunt create automat. |
| **Preț unitar** | **Creare rapidă** | Rata facturii rolului care efectuează lucrarea sau prețul de vânzare al categoriei de cheltuieli. Acest câmp implicit pentru **Timp** se bazează pe rolul și combinația de unități de resurse din lista de prețuri a proiectului care este efectivă pentru data de începere. Pentru cheltuieli, valoarea implicită a acestui câmp este de la setarea prețului pentru categoria de tranzacții din lista de prețuri a proiectului, care este valabilă pentru data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este **prețul pe unitate**, nu există nicio valoare implicită și acest câmp este lăsat necompletat. | Rata costului rolului care efectuează lucrarea sau costul pe unitate al categoriei de cheltuieli. Acest câmp implicit pentru **Timp bazat pe rol** și combinația de unități de resurse pe linia de preț de rol din lista de prețuri de cost atașată unității contractante în vigoare pentru data de începere. Pentru cheltuieli, valoarea implicită a acestui câmp pe categoria de linie de preț a listei de prețuri de cost atașată la unitatea contractoare care este valabilă pentru data de începere. Dacă metoda de stabilire a prețurilor pentru categoria tranzacției nu este prețul pe unitate, nu există nicio valoare implicită și acest câmp este lăsat necompletat. |
| **Impozit estimat** | **Creare rapidă** | Impozitul estimat pentru această lucrare sau cheltuială ca intrare de către utilizator. | Impozitul estimat pentru această lucrare sau cheltuială ca intrare de către utilizator. |
| **Valoare** | **Creare rapidă** | Această valoare din acest câmp poate fi adăugată de utilizator dacă câmpurile **Cantitate** și **Preț** sunt lăsate necompletate. Dacă **Cantitate** și **Preț** sunt completate, câmpul **Cantitate** este numai în citire și este calculat ca **(Cantitate \* Preț unitar) + Taxe**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Actualizați prețurile în detaliile liniei contractului

Dacă modificați prețurile din lista de prețuri a proiectului care este atașată contractului sau lista de prețuri a costului unității contractante, puteți actualiza prețurile din detaliile liniei contractuale individuale pentru a reflecta modificarea. Pe pagina **Contract**, selecta'i **Recalculare**. Se deschide un avertisment pentru a vă informa că prețurile pentru toate liniile contractuale din acest contract sunt resetate. Selectați **Da** pentru a reîmprospăta prețurile atât pentru detaliile liniei contractului de vânzare, cât și pentru cele de cost.

## <a name="access-contract-line-details-for-cost"></a>Accesați detaliile liniei contractului pentru cost

Pe fila **Detalii despre linia de contracct**, selectați un rând din grilă pentru a afișa acțiuni pe bara de instrumente a subgrilei. Prima acțiune pe bara de instrumente subgrilă este **Deschideți detaliile costurilor**. Pentru a vedea rata de cost aferentă și suma pentru această linie de contract, selectați **Deschideți detaliile costurilor**. 

> [!NOTE]
> Schimbarea valorii companiei de resurse, a unității de resurse, a cantității, a datelor, a rolului sau a valorilor categoriei pe detaliile liniei contractului pentru **Cost** modifică, de asemenea, valorile corespunzătoare pe detaliul liniei de contract pentru **Vânzări**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moneda pe detaliile liniei contractului pentru cost și vânzări

Detaliile liniei contractului pentru **Vânzări** setează moneda implicită din lista de prețuri a proiectului care este efectivă pentru data de începere a detaliilor liniei contractului.

Detaliul liniei de contract pentru **Cost** seetează moneda implicită din lista de prețuri a unității contractante care este efectivă pentru data de începere a detaliului de linie de contract pentru **Cost**.

Calculele de rentabilitate convertesc sumele pentru detaliile liniei contractului pentru **Cost** și **Vânzări** în moneda de bază a mediului pentru a raporta marjele reale reale și estimate pe contract.

> [!NOTE]
> Erorile de rotunjire a valutei și modificarea marjelor ar putea apărea din cauza lipsei ratelor de schimb efective la dată. Utilizați aceste calcule pentru contractele de proiect doar ca aproximări și nu pentru raportarea legală sau de altă natură care necesită o precizie mai mare a rotunjirii și conștientizarea efectivității datei pentru ratele de schimb.


[!INCLUDE[footer-include](../includes/footer-banner.md)]