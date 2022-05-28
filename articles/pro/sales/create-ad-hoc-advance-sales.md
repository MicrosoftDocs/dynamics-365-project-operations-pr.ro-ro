---
title: Crearea unui avans ad-hoc pe un contract
description: Acest subiect oferă informații despre crearea unui avans pe un contract, după cum este necesar.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ee97710a9f0229cef3ff9dbfda6a2f108726df20
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594041"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Crearea unui avans ad-hoc pe un contract

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Microsoft Dynamics 365 Project Operations acceptă scenarii de facturare care implică plăți în avans și avansuri. Procesul pentru utilizarea **Avansuri** în **Project Operations** este asemănător contractelor de **Onorariu**. 

Parcurgeți pașii următori pentru a factura clientului un avans.

1. Accesați pagina **Contract proiect** și apoi selectați fila **Avansuri și onorarii**.
2. În subgrila care listează toate avansurile și plățile anticipate înregistrate anterior, selectați **+ Onorariu de contract de proiect nou**. 

    Formularul **Creare rapidă** se deschide pentru înregistrarea unei plăți în avans sau a unui avans.
    
3. Tabelul de mai jos enumeră câmpurile pentru înregistrarea unui avans și considerațiile de care trebuie să țineți cont atunci când creați altele noi:

    | Câmp | Descriere | Impactul din aval |
    | --- | --- | --- |
    | **Client pentru contractul de proiect** | Acest câmp indică ce client din contract va fi facturat pentru acest avans. | Dacă aveți mai mulți clienți în contract și doriți să facturați fiecare dintre aceștia pentru un anumit punct de reținere sau o sumă în avans, creați un avans pentru fiecare client individual. |
    | **Descriere** | Descrierea scopului sau a calendarului avansului pentru a ajuta la identificarea acestui avans. | Această descriere este afișată pe linia de facturare pentru acest avans. |
    | **Valoare** | Suma pentru plata în avans sau avans. | Această sumă este afișată pe linia de facturare pentru acest avans. |
    | **Data facturii** | Data la care acest avans este facturat clientului. | Aceasta este data pentru procesul automat de creare a facturilor pentru a crea o linie de facturare pentru acest avans. |
    | **Stare factură** | Aceasta este o opțiune care indică dacă acest avans este adăugat la o schiță de factură pentru acest client. Valorile posibile sunt:</br>- **Nu este gata de facturat**</br>- **Gata de facturat** | Când un avans sau plata în avans este marcat ca **Gata de facturare**, este adăugat ca timp de linie pe un proiect de factură. Doar un avans complet facturat poate fi utilizat pentru a se concilia cu costurile proiectului pentru următoarea perioadă de facturare. |

4. Selectați **Salvați și închideți** pe dialogul de creare rapidă pentru a înregistra avansul sau plata în avans.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]