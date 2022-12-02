---
title: Liniile de factură furnizor pentru timp
description: Acest articol explică cum să înregistrați liniile de factură ale furnizorului pentru costurile de timp pe care subcontractanții le introduc.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262028"
---
# <a name="vendor-invoice-lines-for-time"></a>Liniile de factură furnizor pentru timp

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O factură de furnizor în Microsoft Dynamics 365 Project Operations poate avea linii de factură de furnizor pentru timp. Managerii de proiect pot utiliza liniile de factură de furnizor pentru a înregistra costurile de timp ale subcontractantului pe proiecte.

Liniile de factură ale furnizorului pentru timp pot sau nu să facă referire la o linie de subcontractare pentru timp. Dacă o linie de factură a furnizorului pentru timp face referire la un subcontract, managerii de proiect vor putea să potrivească și să verifice timpul care este facturat de linia de factură a furnizorului în raport cu timpul înregistrat de subcontractanți și aprobat de managerii de proiect pe proiect.

Următorul tabel oferă informații despre câmpurile de pe liniile de factură de furnizor pentru timp.

| Câmp | Descriere | Impact funcțional |
| --- | --- | --- |
| Nume | Numele liniie de factură de furnizor, pentru a ajuta la identificare. | Acest nume va fi afișat ca prima coloană din toate căutările care sunt bazate pe liniile de factură de furnizor. |
| Descriere | O scurtă descriere a serviciilor și a produselor care sunt facturate de furnizor pe linia de factură de furnizor. | Fără |
| Subcontract | Subcontractul pe care au fost comandate inițial serviciile. | Când este selectat un subcontract pentru factura de furnizor, toate liniile de pe factura de furnizor vor prelua acea selecție. O factură de furnizor nu poate avea linii de factură de furnizor care să facă referire la diferite subcontracte. |
| Linie de subcontractare | Linia de subcontractare pe care au fost comandate serviciile. Lista liniilor de subcontractare care pot fi selectate este limitată la liniile din subcontractul selectat. | Când o linie de subcontractare este selectată pe o linie de factură a furnizorului pentru timp, valorile implicite pentru câmpurile **Proiect**, **Rol** și **Resurse rezervabile** sunt introduse din câmpurile corespunzătoare de pe linia de subcontractare. Dacă linia de subcontractare selectată are valori în câmpurile **Proiect**, **Rol** și **Rezervabil**, valorile câmpurilor corespunzătoare de pe linia de factură de furnizor nu pot diferi de acele valori. |
| Data tranzacției | Data la care costul real al liniei de factură a furnizorului va fi înregistrat în proiect. | Fără |
| Clasă de tranzacții | Valoarea implicită este **Timp**. | Valoarea **Timp** indică faptul că linia de factură a furnizorului este utilizată pentru a înregistra valoarea facturii din timpul subcontractantului. |
| Project | Numele proiectului pentru care au fost utilizate serviciile care sunt facturate. | Acest câmp este obligatoriu și nu poate fi lăsat necompletat. |
| Activitate | Numele sarcinii de proiect pentru care au fost utilizate serviciile care sunt facturate. Acest câmp este disponibil numai dacă este selectat un proiect. Selectarea unei sarcini de proiect este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură a furnizorului cu timpul înregistrat de resursele subcontractantului pentru orice sarcină a proiectului. Dacă linia de factură a furnizorului nu face referire la o linie de subcontractare și acest câmp este lăsat necompletat, costul real creat de linia de factură a furnizorului nu va fi legat de nicio valoare reală a vânzărilor nefacturate. În acest caz, dacă este configurată facturarea bazată pe sarcini, este posibil ca costurile să nu poată fi facturate clientului final. |
| Rol | Rolul resurselor din subcontract al căror timp este facturat. | Acest câmp specifică rolul pe care îl au resursele de subcontractare al căror timp este facturat pe factura furnizorului. |
| Resursă ce se poate rezerva | Numele subcontractantului al cărui timp este facturat. Selectarea unei resurse rezervabile este opțională. | Dacă acest câmp este lăsat necompletat, managerul de proiect poate potrivi linia de factură a furnizorului cu timpul înregistrat de orice resursă care aparține furnizorului pe linia de factură a furnizorului. |
| Cantitate | Introduceți numărul de ore de timp care sunt facturate de furnizor pe linia de factură de furnizor. |Fără |
| Grup de unități | Valoarea implicită este **Grup de unități de timp** și nu poate fi modificat. | Fără |
| Unitate | Valoarea implicită este unitatea de bază de ore din grupul de unități de timp. Puteți modifica această valoare în orice unitate unitate din grupul de unități de timp, cum ar fi ziua sau săptămâna. | Combinația dintre valorile **Rol** și **Unitate** va fi folosită ca valoare implicită sau calculată pentru câmpul **Preț unitar** pe linia de factură de furnizor. |
| Preț unitar | Prețul unitar implicit utilizează combinația de **Rol** și **Unitate** din lista de prețuri a proiectului care este aplicabilă la data tranzacției din linia de factură de furnizor. | Dacă prețul pentru lista de prețuri aplicabilă a proiectului este stabilit într-o unitate care diferă de unitatea de pe linia de factură de furnizor, sistemul folosește conversia de unități pentru a calcula prețul unitar. |
| Subtotal | Acest câmp numai în citire este calculat automat ca *Cantitate* &times; *Preț unitar*, dacă sunt introduse atât în câmpul **Cantitate**, cât și în câmpul **Preț unitar**. Dacă unul sau ambele dintre aceste câmpuri sunt necompletate, puteți introduce o valoare în acest câmp. | Fără |
| Impozit pe vânzări | Introduceți valoarea impozitului pe vânzări. | Fără |
| Valoare totală | Valoarea totală a liniei de factură de furnizor, inclusiv impozitele. Acest câmp este calculat ca *Subtotal* + *Impozit pe vânzări*. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
