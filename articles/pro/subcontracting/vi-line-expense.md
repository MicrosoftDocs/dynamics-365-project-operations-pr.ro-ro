---
title: Liniile de factură furnizor pentru categoriile de cheltuieli
description: Acest articol explică cum să înregistrați liniile de factură pentru furnizori pentru categoriile de cheltuieli.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925912"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Liniile de factură furnizor pentru categoriile de cheltuieli

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru categoriile de cheltuieli. Managerii de proiect pot folosi liniile de factură ale furnizorului pentru categoriile de cheltuieli pentru a înregistra costurile serviciilor care sunt achiziționate ca categorii de cheltuieli.

Liniile de factură de furnizor pentru categoriile de cheltuieli ar putea sau nu să facă referire la o linie de subcontractare pentru categoriile de cheltuieli. Dacă o linie de factură a furnizorului pentru categoriile de cheltuieli face referire la un subcontract, managerii de proiect vor putea să coreleze și să verifice cheltuielile care sunt facturate de linia de factură ale furnizorului cu cheltuielile care sunt înregistrate pe aceste categorii de cheltuieli și aprobate de managerii de proiect în cadrul proiectului.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură de furnizor pentru categoriile de cheltuieli.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniei de factură a furnizorului, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană în toate căutările care se bazează pe liniile de factură pentru furnizor. |
| Descriere | O scurtă descriere a serviciilor care sunt facturate de către furnizor pe linia de facturare a furnizorului. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial serviciile. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor moșteni acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linia de subcontractare | Linia de subcontractare pe care au fost comandate serviciile. Lista liniilor de subcontract care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură de furnizor pentru categoriile de cheltuieli, valorile implicite pentru **Proiect**, **·**, și **Categoria tranzacției** câmpurile sunt introduse din câmpurile corespunzătoare de pe linia de subcontractare. Dacă linia de subcontractare selectată are valori în **Proiect**, **proiectului**, și **Categoria tranzacției** câmpuri, valorile câmpurilor corespunzătoare de pe linia facturii furnizorului nu pot diferi de acele valori. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. |Fără |
| Clasă de tranzacții | Selectați **Cheltuiala** pentru a înregistra o factură de furnizor pentru o categorie de cheltuieli. | Valoarea **Cheltuiala** indică faptul că linia de factură a furnizorului este utilizată pentru a înregistra suma facturii pentru serviciile care au fost achiziționate ca categorii de cheltuieli. |
| Project | Numele proiectului pentru care au fost utilizate serviciile care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate serviciile care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură a furnizorului cu cheltuielile care sunt înregistrate pentru orice sarcină a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, este posibil ca costurile să nu poată fi facturate clientului final. |
| Categorie tranzacție | Categoria tranzacției care este facturată. Trebuie creată o categorie de cheltuieli corespunzătoare pentru categoria de tranzacție selectată. | Combinația de **Categoria tranzacției** și **Unitate** valorile vor fi utilizate ca valoare implicită sau calculată pentru **Preț unitar** câmpul de pe linia facturii furnizorului. |
| Cantitate | Introduceți cantitatea care este facturată de furnizor pe linia de factură. |Fără|
| Grup de unități | O valoare implicită este introdusă pe baza grupului de unități din categoria de tranzacție selectată. | Fără |
| Unitate | Valoarea implicită este unitatea de bază a grupului de unități care este selectat. Puteți modifica această valoare pentru a cumpăra în orice unitate din grupul de unități. | Combinația de **Categoria tranzacției** și **Unitate** valorile vor fi utilizate ca valoare implicită sau calculată pentru **Preț unitar** câmpul de pe linia facturii furnizorului. |
| Preț unitar | Prețul unitar implicit folosește combinația de **Categoria tranzacției** și **Unitate** valorile din lista de prețuri a proiectului care este aplicabilă datei tranzacției din linia facturii furnizorului. | Dacă prețul pentru lista de prețuri de proiect aplicabilă este configurat într-o unitate care diferă de unitatea de pe linia de factură a furnizorului, sistemul utilizează conversia unității pentru a calcula prețul pe unitate. |
| Subtotal | Acest câmp numai pentru citire este calculat ca *Cantitate*&times;*Preț unitar*, dacă valorile sunt introduse în ambele **Cantitate** câmpul și **Preț unitar** camp. Dacă unul sau ambele câmpuri sunt goale, puteți introduce o valoare în acest câmp.| Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Suma totală a liniei de factură a furnizorului, inclusiv taxele. Acest câmp este calculat ca *Subtotal* + *Taxa de vanzari*. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
