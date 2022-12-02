---
title: Liniile de factură furnizor pentru produse
description: Acest articol explică modul de înregistrare a liniilor de factură de furnizor pentru produse și utilizarea diferitelor câmpuri pentru înregistrarea achizițiilor de produse de la furnizori.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261574"
---
# <a name="vendor-invoice-lines-for-products"></a>Liniile de factură furnizor pentru produse

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru produse (numite și materiale). Managerii de proiect pot utiliza liniile de factură de furnizor pentru produse, pentru a înregistra costurile pentru produsele care au fost achiziționate pe proiecte.

Liniile de factură ale furnizorului pentru produse pot sau nu să facă referire la o linie de subcontractare pentru materiale. Dacă o linie de factură a furnizorului pentru produse face referire la un subcontract, managerii de proiect vor putea să potrivească și să verifice produsele care sunt facturate de linia de factură a furnizorului în raport cu produsele care sunt înregistrate de subcontractanți și aprobate de managerii de proiect pe proiect.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură de furnizor pentru produse.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniie de factură de furnizor, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană din toate căutările care sunt bazate pe liniile de factură de furnizor. |
| Descriere | O scurtă descriere a produselor care sunt facturate de furnizor pe linia de factură de furnizor. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial produsele. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor prelua acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linie de subcontractare | Linia de subcontractare pe care au fost comandate produsele. Lista liniilor de subcontractare care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură de furnizor pentru produse, valorile implicite pentru câmpurile **Proiect**, **Sarcină** și **Produs** sunt introduse din câmpurile corespunzătoare de pe linia de subcontractare. Dacă linia de subcontractare selectată are valori în câmpurile **Proiect**, **Sarcină** și **Produs**, valorile câmpurilor corespunzătoare de pe linia de factură de furnizor nu pot diferi de acele valori. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. | Fără|
| Clasă de tranzacții | Când produsele sunt facturate, acest câmp trebuie setat la **Materiale**. | Valoarea **Materiale** indică faptul că linia de factură de furnizor este utilizată pentru a înregistra suma facturii pentru materialele care au fost achiziționate. |
| Project | Numele proiectului pentru care au fost utilizate produsele care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate produsele care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură de furnizor cu produsele achiziționate care sunt utilizate pe orice sarcină a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, costurile nu vor putea fi facturate clientului final. |
| Selectați produs | Selectați dacă produsul care este facturat este un produs existent din catalog sau este un produs din afara catalogului. | Valoarea implicită este introdusă din linia de subcontract atunci când este selectată o linie de subcontract. |
| Produs | Selectați produsul din catalog. Dacă produsul este unul din afara catalogului, introduceți numele produsului. | Acest câmp este utilizat pentru a introduce prețurile implicite de achiziție pentru produsele existente. |
| Cantitate | Introduceți cantitatea de material care este facturată de furnizor această linie de facturare. | Fără |
| Grup de unități | Selectați grupul de unități al unității în care este exprimată cantitatea care este facturată. | Fără |
| Unitate | Valoarea implicită este unitatea de bază din grupul de unități care este selectat. Puteți modifica această valoare pentru a plăti în orice unitate din grupul de unități selectat. | Combinația dintre valorile **Produs** și **Unitate** va fi folosită ca valoare implicită sau calculată pentru câmpul **Preț unitar** pe linia de factură de furnizor. |
| Preț unitar | Prețul unitar implicit utilizează combinația de valori **Produs** și **Unitate** din lista de prețuri a proiectului care este aplicabilă la data tranzacției din linia de factură de furnizor. | Fără |
| Subtotal | Acest câmp numai în citire este calculat automat ca *Cantitate* &times; *Preț unitar*, dacă sunt introduse atât în câmpul **Cantitate**, cât și în câmpul **Preț unitar**. Dacă unul sau ambele dintre aceste câmpuri sunt necompletate, puteți introduce o valoare în acest câmp. | Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Valoarea totală a liniei de factură de furnizor, inclusiv impozitele. Acest câmp este calculat ca *Subtotal* + *Impozit pe vânzări*. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
