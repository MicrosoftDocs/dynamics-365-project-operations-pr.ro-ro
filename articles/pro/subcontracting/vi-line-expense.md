---
title: Liniile de factură furnizor pentru categoriile de cheltuieli
description: Acest articol explică cum să înregistrați liniile de factură de furnizor pentru categoriile de cheltuieli.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261715"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Liniile de factură furnizor pentru categoriile de cheltuieli

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru categoriile de cheltuieli. Managerii de proiect pot folosi liniile de factură de furnizor pentru categoriile de cheltuieli pentru a înregistra costurile serviciilor care sunt achiziționate sub formă de categorii de cheltuieli.

Liniile de factură de furnizor pentru categoriile de cheltuieli pot sau nu să facă referire la o linie de subcontractare pentru categoriile de cheltuieli. Dacă o linie de factură de furnizor pentru categorii de cheltuieli face referire la un subcontract, managerii de proiect vor putea să potrivească și să verifice cheltuielile care sunt facturate de linia de factură de furnizor în raport cu cheltuielile care sunt înregistrate pe aceste categorii de cheltuieli și aprobate de managerii de proiect pe proiect.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură de furnizor pentru categoriile de cheltuieli.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniie de factură de furnizor, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană din toate căutările care sunt bazate pe liniile de factură de furnizor. |
| Descriere | O scurtă descriere a serviciilor și a produselor care sunt facturate de furnizor pe linia de factură de furnizor. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial serviciile. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor prelua acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linie de subcontractare | Linia de subcontractare pe care au fost comandate serviciile. Lista liniilor de subcontractare care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură de furnizor pentru categorii de cheltuieli, valorile implicite pentru câmpurile **Proiect**, **Sarcină** și **Categorie de tranzacție** sunt introduse din câmpurile corespunzătoare de pe linia de subcontractare. Dacă linia de subcontractare selectată are valori în câmpurile **Proiect**, **Sarcină de proiect** și **Categorie de tranzacție**, valorile câmpurilor corespunzătoare de pe linia de factură de furnizor nu pot diferi de acele valori. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. |Fără |
| Clasă de tranzacții | Selectați **Cheltuieli** pentru a înregistra o factură de furnizor pentru o categorie de cheltuieli. | Valoarea **Cheltuieli** indică faptul că linia de factură de furnizor este utilizată pentru a înregistra suma facturii pentru serviciile care au fost achiziționate sub formă de categorii de cheltuieli. |
| Project | Numele proiectului pentru care au fost utilizate serviciile care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate serviciile care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură a furnizorului cu cheltuielile care sunt înregistrate pe orice sarcină a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, este posibil ca costurile să nu poată fi facturate clientului final. |
| Categorie tranzacție | Categoria tranzacției care este facturată. Trebuie creată o categorie de cheltuieli corespunzătoare pentru categoria de tranzacție selectată. | Combinația dintre valorile **Categorie de tranzacție** și **Unitate** va fi folosită ca valoare implicită sau calculată pentru câmpul **Preț unitar** pe linia de factură de furnizor. |
| Cantitate | Introduceți cantitatea care este facturată de furnizor pe linia de factură. |Fără|
| Grup de unități | O valoare implicită este introdusă pe baza unui grup de unități din categoria de tranzacție selectată. | Fără |
| Unitate | Valoarea implicită este unitatea de bază din grupul de unități care este selectat. Puteți modifica această valoare pentru a cumpăra în orice unitate din grupul de unități. | Combinația dintre valorile **Categorie de tranzacție** și **Unitate** va fi folosită ca valoare implicită sau calculată pentru câmpul **Preț unitar** pe linia de factură de furnizor. |
| Preț unitar | Prețul unitar implicit utilizează combinația de valori **Categorie de tranzacție** și **Unitate** din lista de prețuri a proiectului care este aplicabilă la data tranzacției din linia de factură de furnizor. | Dacă prețul pentru lista de prețuri aplicabilă a proiectului este stabilit într-o unitate care diferă de unitatea de pe linia de factură de furnizor, sistemul folosește conversia de unități pentru a calcula prețul unitar. |
| Subtotal | Acest câmp numai în citire este calculat automat ca *Cantitate* &times; *Preț unitar*, dacă sunt introduse atât în câmpul **Cantitate**, cât și în câmpul **Preț unitar**. Dacă unul sau ambele dintre aceste câmpuri sunt necompletate, puteți introduce o valoare în acest câmp.| Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Valoarea totală a liniei de factură de furnizor, inclusiv impozitele. Acest câmp este calculat ca *Subtotal* + *Impozit pe vânzări*. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
