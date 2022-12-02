---
title: Configurați tarifelor de cost și de vânzare pentru cheltuieli
description: Acest articol oferă informații despre modul de configurare al costului și a ratelor de vânzăare pentru categorii de tranzacție și de cheltuieli.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911887"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configurați tarifelor de cost și de vânzare pentru cheltuieli

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Puteți configura costuri și prețuri de vânzare pentru categoriile de tranzacții în Dynamics 365 Project Operations. Deoarece costul și prețurile de vânzare sunt concepute pentru Cheltuieli, fiecare categorie de tranzacții care le include, trebuie să fie, de asemenea, configurată ca o categorie de cheltuieli. Această configurație asigură precizia funcționalității din aval. Costurile și prețurile de vânzare pentru categoriile de tranzacții pot fi listate numai într-o singură monedă, care trebuie să fie moneda din antetul listei de prețuri.

Pentru a configura costurile și ratele de vânzare pentru categoriile de tranzacții, parcurgeți pașii următori. 

1. Accesați **Vânzări** > **Clienți** > **Liste de prețuri**.
2. Selectați **Nou** pentru a crea o nouă listă de prețuri. 
3. Pe **Prețuri categorii**, din meniul subgrilă, selectați **Preț categorie nouă**. 
4. Pe pagina **Creare rapidă**, introduceți categoria tranzacției și unitatea pentru care creați noul preț.

Următorul tabel listează câmpurile pe fila **General** și pagina **Creare rapidă** a unei linii de preț de categorie pe care ar trebui să-l aveți în vedere atunci când creați prețuri de categorie pe o listă de vânzări sau de prețuri de cost.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Categorie tranzacție | Fila **General** și pagini **Creare rapidă** | Selectați categoria de tranzacții pentru care creați un preț de vânzare sau de cost. | Categoria de tranzacții de pe estimarea de intrare sau date reale pentru Cheltuieli va fi asortată cu această linie pentru a stabili implicit costul sau rata vânzărilor a categoriei de tranzacții. |
| Planificare unitate | Fila **General** și pagini **Creare rapidă** | Programul de unitate este implicit din programul de unitate al categoriei de tranzacții. | Nu există niciun impact din aval din acest domeniu. |
| Unitate | Fila **General** și pagini **Creare rapidă** | Selectați unitatea pentru care sunt stabilite tarifele. | Unitatea din estimarea de intrare sau reală este comparată cu unitatea de pe această linie pentru a respecta rata implicită a estimării cheltuielilor sau reală. |
| Metodă de stabilire a prețului | Fila **General** și pagini **Creare rapidă** | Valorile posibile ale câmpului **Metoda de stabilire a prețurilor** sunt, **Preț pe unitate**, **La cost** și **Adaos peste cost**. | În timpul configurării prețului, selectarea **Preț pe unitate** blochează câmpul **La sută** pe linia de preț categorie. Dacă **Cu cost** este selectat, câmpurile **Preț** și **La sută** sunt blocate în lista de prețuri de vânzare. Selectarea **Adaos peste cost** blochează câmpul **Preț** pe lista de prețuri de vânzare. Pe o linie reală de intrare pentru cheltuială, metoda de stabilire a prețurilor **Cu cost** sau **Adaos peste cost** are ca rezultat atribuirea liniei de vânzări nefacturate corespunzătoare unui preț care este egal cu prețul din costul real sau calculat ca o majorare a prețului. |
| Preț | Fila **General** și pagini **Creare rapidă** | Configurați o rată pe unitate pentru categoria tranzacției și combinația de unități. De exemplu, rata pentru kilometraj este 10 USD pe milă și 8 USD pe kilometru. | Rata kilometrajului va fi rata implicită pe prețul sau costul pe unitate a estimării primite sau linia reală pentru o clasă de tranzacție de cheltuială.|
| Procentaj | Fila **General** și pagini **Creare rapidă** | Configurați procentul de cost pentru categoria tranzacției și combinația de unități. De exemplu, rata de vânzare a biletului de avion ar trebui să fie mărită cu 10% peste costul cheltuielilor suportate pentru biletele de avion. | Acest procent peste cost este aplicabil numai pe o listă de prețuri de vânzare când metoda de prețuri selectată este **Adaos peste cost**. |
| Monedă | Fila **General** și pagini **Creare rapidă** | În mod implicit, această valoare provine din moneda din antetul listei de prețuri. Pentru tarifarea categoriilor de tranzacții, moneda nu poate fi înlocuită. | Această monedă implicită pentru prețul pe unitate al liniei reale de vânzări pentru clasa tranzacției de cheltuială pentru cost și vânzări. |

## <a name="pricing-methods-for-expenses"></a>Metode de stabilire a prețurilor pentru cheltuieli

Când setați prețuri de categorie care sunt relevante numai în contextul stabilirii prețurilor pentru cheltuieli, puteți utiliza una dintre următoarele trei metode de stabilire a prețurilor:

- **Preț unitar**
- **La cost**
- **Adaos peste cost**

### <a name="price-per-unit"></a>Preț unitar
Atunci când această metodă de stabilire a prețurilor este selectată pe o linie de preț de categorie care este legată de o listă de prețuri de vânzare, prețurile implicite pentru combinația de categorii și unități, atât în estimare, cât și în cea reală. Estimările se referă la liniile de estimare de proiect pentru cheltuieli, detaliul liniei de ofertă și detaliul liniei de contract pentru cheltuieli.

### <a name="at-cost"></a>La cost
Atunci când această metodă de stabilire a prețurilor este selectată pe o linie de preț a categoriei care este legată de o listă de prețuri de vânzare, prețurile implicite pentru combinația de categorii și unități, numai pentru datele reale de cheltuieli. De exemplu, cifrele reale de vânzare facturate pentru clasa tranzacției de cheltuieli. Prețul unitar este stabilit pe vânzările nefacturate efective din prețul unitar pe costul efectiv pentru acea cheltuială. Prețul implicit pe baza costului nu se face pe estimările proiectului pentru cheltuieli sau pe linia de ofertă și detaliile liniei contractului pentru cheltuieli.

### <a name="markup-over-cost"></a>Adaos peste cost
Atunci când această metodă de stabilire a prețurilor este selectată pe o linie de preț a categoriei care este legată de o listă de prețuri de vânzare, prețurile implicite pentru combinația de categorii și unități, numai pentru o dată reală de cheltuială. De exemplu, cifrele reale de vânzare facturate pentru clasa tranzacției de cheltuieli. Acest preț unitar este stabilit pe vânzările nefacturate efective la o valoare calculată din prețul unitar pe costul efectiv pentru acea cheltuială după aplicarea procentului de majorare definit. Prețul implicit pe baza costului nu se face în estimările proiectului pentru cheltuieli sau pe linia de ofertă și detaliile liniei contractului pentru cheltuieli.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
