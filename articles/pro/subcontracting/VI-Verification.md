---
title: Verificarea facturilor de furnizori cu datele reale aprobate
description: Acest articol explică cum Microsoft Dynamics 365 Project Operations permite managerilor de proiect să verifice facturile furnizorilor cu valorile reale care au fost aprobate pe măsură ce contractanții au efectuat lucrări și au înregistrat timpul, precum și cheltuielile și materialele care au fost folosite de membrii echipei de proiect.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522944"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificarea facturilor de furnizori cu datele reale aprobate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Microsoft Dynamics 365 Project Operations permite managerilor de proiect să verifice liniile de factură de furnizor în următoarele moduri:

- Utilizați câmpul **Stare de verificare** de pe liniile de factură de furnizor.
- Dacă liniile de factură de furnizor fac referire la o linie de subcontractare, legați costurile reale din activitatea subcontractantului la acele linii de factură ale furnizorului. Legătura este creată prin potrivirea costurilor reale cu liniile de factură de furnizor.

    > [!NOTE]
    > Deși starea de verificare poate fi urmărită pentru liniile de factură de furnizor care nu fac referire la un subcontract, costurile reale nu pot fi legate de acele linii de factură de furnizor.

## <a name="verification-status"></a>Stare verificare

Câmpul **Stare de verificare** de pe o linie de factură de furnizor indică starea verificării. Sunt acceptate următoarele stări:

1. Neînceput
2. În desfășurare
3. Finalizați

Liniile de factură de furnizor care au o stare de verificare de **Neînceput** pot fi editate.

Liniile de factură de furnizor care au o stare de verificare de **În curs** nu mai pot fi editate. Pentru o linie de factură de furnizor care face referire la un subcontract, starea de verificare este setată automat la **În curs** de îndată ce primul cost real este corelat cu linia de factură a furnizorului.

Liniile de factură de furnizor care au o stare de verificare de **Finalizat** nu mai pot fi editate. Când toate liniile de pe o factură de furnizor au această stare de verificare, factura de furnizor poate fi confirmată.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Potriviți costurile reale la linii de factură de furnizor

Potrivirea costurilor reale ajută la procesul de verificare pe o linie de factură de furnizor. Pentru a potrivi costurile reale cu o linie de factură de furnizor, urmați acești pași.

1. Deschideți linia de factură de furnizor și selectați fila **Costuri reale nepotrivite**. O grilă arată o listă de costuri reale care fac referire la aceeași linie de subcontractare ca și linia de factură de furnizor.
2. Selectați unul sau mai multe dintre costurile reale, apoi selectați **Potrivire** pe bara de instrumente de deasupra grilei. Sistemul validează faptul că costurile reale selectate pot fi potrivite. După aprobarea validării, costurile reale sunt legate de linia de factură de furnizor.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criterii de validare care sunt utilizate pentru a lega costurile reale la liniile de factură de furnizor

În timpul procesului de potrivire, o legătură dintre un cost real și o linie de factură de furnizor poate fi stabilită numai dacă sunt îndeplinite ambele condiții următoare:

- Câmpul **Stare de ajustare** pentru fiecare cost real selectat trebuie să fie necompletat. Cu alte cuvinte, costurile reale nu trebuie să fi fost înlocuite cu alte costuri reale în timpul unui proces de retragere, anulare a aprobării sau proces de corecție a jurnalului.
- Valorile următoarelor câmpuri sunt potrivite între linia de factură de furnizor și costul real selectat. Dacă niciun câmp nu este setat pe linia de factură de furnizor, nu este luat în considerare pentru potrivire.

    - Contract pentru proiect
    - Linie contract proiect
    - Clasă de tranzacții
    - Project
    - Activitate
    - Categorie de resursă
    - Categorie tranzacție
    - Produs
    - Linie de subcontractare
    - Resursă ce se poate rezerva

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Anulați potrivirea costurilor reale dintr-o linie de factură de furnizor

Anularea potrivirii costurilor reale poate ajuta, de asemenea, la procesul de verificare pe o factură de furnizor, permițând eliminarea linkurilor stabilite anterior. Se poate anula potrivirea costurilor reale numai din liniile de factură de furnizor care au o stare de verificare de **În curs**. Pentru a anula potrivirea costurilor reale de pe o linie de factură de furnizor, urmați acești pași.

1. Deschideți linia de factură de furnizor și selectați fila **Costuri reale potrivite**. O grilă arată o listă de costuri reale care fac referire la aceeași linie de subcontractare ca și linia de factură de furnizor.
2. Selectați unul sau mai multe dintre costurile reale, apoi selectați **Anulare potrivire** pe bara de instrumente de deasupra grilei.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
