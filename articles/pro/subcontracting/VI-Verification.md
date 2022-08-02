---
title: Verificarea facturilor de furnizori cu datele reale aprobate
description: Acest articol explică cum Microsoft Dynamics 365 Project Operations Haideți managerii de proiect să verifice facturile furnizorilor cu datele reale care au fost aprobate pe măsură ce antreprenorii au efectuat lucrări și au înregistrat timpul, precum și cheltuielile și materialele care au fost folosite de membrii echipei de proiect.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204190"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verificarea facturilor de furnizori cu datele reale aprobate

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Microsoft Dynamics 365 Project Operations să verificăm managerii de proiect liniile de facturi ale furnizorului în următoarele moduri:

- Folosește **Starea de verificare** câmpul de pe liniile facturii furnizorului.
- Dacă liniile de factură ale furnizorului fac referire la o linie de subcontractare, legați costurile reale din activitatea subcontractantului la acele linii de factură ale furnizorului. Legătura este creată prin potrivirea costurilor reale cu liniile de factură pentru furnizor.

    > [!NOTE]
    > Deși starea de verificare poate fi urmărită pentru liniile de factură de furnizor care nu fac referire la un subcontract, costurile reale nu pot fi legate de acele linii de factură de furnizor.

## <a name="verification-status"></a>Starea de verificare

The **Starea de verificare** câmpul de pe o linie de factură de furnizor indică starea verificării. Sunt acceptate următoarele stări:

1. Neînceput
2. În desfășurare
3. Finalizați

Linii de factură de furnizor care au o stare de verificare de **Nu a început** poate fi editat.

Linii de factură de furnizor care au o stare de verificare de **În curs** nu mai poate fi editat. Pentru o linie de factură de furnizor care face referire la un subcontract, starea de verificare este setată automat la **În curs** de îndată ce primul cost real este corelat cu linia de factură a furnizorului.

Linii de factură de furnizor care au o stare de verificare de **Complet** nu mai poate fi editat. Când toate liniile de pe o factură de furnizor au această stare de verificare, factura de furnizor poate fi confirmată.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Potriviți costurile reale cu liniile de factură ale furnizorului

Potrivirea costurilor reale ajută la procesul de verificare pe o linie de factură a furnizorului. Pentru a potrivi costurile reale cu o linie de factură a furnizorului, urmați acești pași.

1. Deschideți linia de factură a furnizorului și selectați **Costuri reale de neegalat** fila. O grilă arată o listă de costuri reale care fac referire la aceeași linie de subcontractare ca și linia de factură a furnizorului.
2. Selectați unul sau mai multe dintre costurile reale, apoi selectați **Meci** pe bara de instrumente de deasupra grilei. Sistemul validează faptul că costurile reale selectate pot fi corelate. După ce validarea este trecută, costurile reale sunt legate de linia de factură a furnizorului.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Criterii de validare care sunt utilizate pentru a lega costurile reale la liniile de factură ale furnizorului

În timpul procesului de potrivire, o legătură între un cost real și o linie de factură a furnizorului poate fi stabilită numai dacă sunt îndeplinite ambele condiții următoare:

- The **Starea de ajustare** câmpul pentru fiecare cost real selectat trebuie să fie necompletat. Cu alte cuvinte, costurile reale nu trebuie să fi fost înlocuite cu alte costuri reale în timpul unui proces de rechemare, anulare a aprobării sau jurnal de corecție.
- Valorile următoarelor câmpuri sunt corelate între linia de factură a furnizorului și costul real selectat. Dacă niciun câmp nu este setat pe linia facturii furnizorului, nu este luat în considerare pentru potrivire.

    - Contract pentru proiect
    - Linie contract proiect
    - Clasă de tranzacții
    - Project
    - Activitate
    - Categoria de resurse
    - Categorie tranzacție
    - Produs
    - Linia de subcontractare
    - Resursă ce se poate rezerva

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Nepotriviți costurile reale dintr-o linie de factură a furnizorului

Nepotrivirea costurilor reale poate ajuta, de asemenea, la procesul de verificare pe o factură de furnizor, permițând eliminarea linkurilor stabilite anterior. Costurile reale pot fi nepotrivite numai din liniile de factură ale furnizorului care au o stare de verificare de **În curs**. Pentru a nu compara costurile reale dintr-o linie de factură de furnizor, urmați acești pași.

1. Deschideți linia de factură a furnizorului și selectați **Costuri reale potrivite** fila. O grilă arată o listă de costuri reale care fac referire la linia de factură a furnizorului.
2. Selectați unul sau mai multe dintre costurile reale, apoi selectați **Nepotrivire** pe bara de instrumente de deasupra grilei.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
