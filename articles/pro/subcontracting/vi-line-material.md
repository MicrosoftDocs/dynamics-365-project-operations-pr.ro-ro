---
title: Liniile de factură furnizor pentru produse
description: Acest articol explică cum să înregistrați liniile de factură de la furnizori pentru produse și să utilizați diferitele câmpuri pentru a înregistra achizițiile de produse de la furnizori.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931391"
---
# <a name="vendor-invoice-lines-for-products"></a>Liniile de factură furnizor pentru produse

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru produse (numite și materiale). Managerii de proiect pot folosi liniile de factură ale furnizorilor pentru produse pentru a înregistra costurile produselor care au fost achiziționate în cadrul proiectelor.

Liniile de factură de furnizor pentru produse pot face sau nu referire la o linie de subcontractare pentru materiale. Dacă o linie de factură a furnizorului pentru produse face referire la un subcontract, managerii de proiect vor putea să coreleze și să verifice produsele care sunt facturate de linia de facturi ale furnizorului cu utilizarea produselor achiziționate care sunt înregistrate și aprobate de managerii de proiect.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură de furnizor pentru produse.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniei de factură a furnizorului, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană în toate căutările care se bazează pe liniile de factură pentru furnizor. |
| Descriere | O scurtă descriere a produselor care sunt facturate de vânzător pe linia de factură pentru furnizor. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial produsele. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor moșteni acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linia de subcontractare | Linia de subcontractare pe care au fost comandate produsele. Lista liniilor de subcontract care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură de furnizor pentru produse, valorile implicite pentru **Proiect**, **·**, și **Produs** câmpurile sunt introduse din câmpurile corespunzătoare de pe linia de subcontractare. Dacă linia de subcontractare selectată are valori în **Proiect**, **·**, și **Produs** câmpuri, valorile câmpurilor corespunzătoare de pe linia facturii furnizorului nu pot diferi de acele valori. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. | Fără|
| Clasă de tranzacții | Când produsele sunt facturate, acest câmp trebuie setat la **Material**. | Valoarea **Material** indică faptul că linia de factură a furnizorului este utilizată pentru a înregistra suma facturii pentru materialele care au fost achiziționate. |
| Project | Numele proiectului pe care au fost utilizate produsele care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate produsele care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură a furnizorului cu produsul achiziționat care este utilizat pentru orice activitate a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, costurile nu vor putea fi facturate clientului final. |
| Selectare produs | Selectați dacă produsul care este facturat este un produs existent din catalog sau un produs înscris. | Valoarea implicită este introdusă din linia de subcontract atunci când este selectată o linie de subcontract. |
| Produs | Selectați produsul din catalog. Dacă produsul este un produs înscris, introduceți numele produsului. | Acest câmp este folosit pentru a introduce prețurile implicite de achiziție pentru produsele existente. |
| Cantitate | Introduceți cantitatea de material care este facturată de furnizor pe această linie de factură. | Fără |
| Grup de unități | Selectați grupul de unități al unității în care este exprimată cantitatea care este facturată. | Fără |
| Unitate | Valoarea implicită este unitatea de bază a grupului de unități care este selectat. Puteți modifica această valoare pentru a plăti în orice unitate din grupul de unități selectat. | Combinația de **Produs** și **Unitate** valorile vor fi utilizate ca valoare implicită sau calculată pentru **Preț unitar** câmpul de pe linia facturii furnizorului. |
| Preț unitar | Prețul unitar implicit folosește combinația de **Produs** și **Unitate** valorile din lista de prețuri a proiectului care este aplicabilă datei tranzacției din linia facturii furnizorului. | Fără |
| Subtotal | Acest câmp numai pentru citire este calculat ca *Cantitate*&times;*Preț unitar*, dacă valorile sunt introduse în ambele **Cantitate** câmpul și **Preț unitar** camp. Dacă unul sau ambele câmpuri sunt goale, puteți introduce o valoare în acest câmp. | Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Suma totală a liniei de factură a furnizorului, inclusiv taxele. Acest câmp este calculat ca *Subtotal* + *Taxa de vanzari*. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
