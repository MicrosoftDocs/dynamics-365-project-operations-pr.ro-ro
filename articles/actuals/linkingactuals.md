---
title: Originile tranzacțiilor - Conectarea valorilor reale la sursa acestora
description: Acest articol explică modul în care conceptul de origini de tranzacție este utilizat pentru a conecta valorile reale la înregistrările inițiale, cum ar fi introducerea timpului, introducerea cheltuielilor sau jurnalele de utilizare a materialelor.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921317"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Originile tranzacțiilor - Conectarea valorilor reale la sursa acestora

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Înregistrările despre originea tranzacției sunt create pentru a conecta datele reale la sursa lor, cum ar fi intrări de timp, înregistrări de cheltuieli, jurnalele de utilizare a materialelor și facturile de proiect.

Următorul exemplu arată procesarea tipică a intrărilor de timp într-un ciclu de viață al proiectului în Project Operations.

> ![Procesarea intrărilor de timp în Project Operations.](media/basic-guide-17.png)
 
1. Remiterea unei intrări de timp determină crearea a două linii de jurnal: una pentru cost și una pentru vânzările nefacturate.
2. Aprobarea eventuală a intrării de timp determină crearea a două valori reale: una pentru cost și una pentru vânzările nefacturate.
3. Atunci când utilizatorul creează o factură de proiect, tranzacția linie factură este creată utilizând date din valorile reale pentru vânzările nefacturate.
4. Când este confirmată factura, sunt create două valori reale: o inversare a vânzărilor nefacturate și o valoare reală pentru vânzări facturate.

Fiecare eveniment din acest flux de procesare declanșează crearea de înregistrări în entitatea Originea tranzacției, pentru a ajuta la construirea unei urmăriri a relațiilor dintre aceste înregistrări care sunt create pe detaliile pentru intrarea de timp, linia de jurnal, valoarea reală și linia de facturare.

Următorul tabel afișează înregistrările din entitatea Origine tranzacție pentru fluxul de lucru precedent.

| Eveniment                        | Origine                   | Tip de origine                       | Tranzacție                       | Tipul tranzacției         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Remitere intrare de timp        | GUID înregistrare intrare de timp   | Intrare de timp                        | GUID înregistrare linie de jurnal (cost)   | Linie de jurnal             |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID înregistrare linie de jurnal (vânzări)  | Linie de jurnal                      |                          |
| Aprobare timp                | GUID înregistrare linie de jurnal | Linie de jurnal                      | GUID înregistrare vânzări nefacturate        | Real                   |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID înregistrare vânzări nefacturate        | Real                            |                          |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | GUID înregistrare valori reale cost           | Real                            |                          |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID înregistrare valori reale cost           | Real                            |                          |
| Creare factură             | GUID înregistrare intrare de timp   | Intrare de timp                        | GUID tranzacție linie factură     | Tranzacție linie factură |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | GUID tranzacție linie factură     | Tranzacție linie factură          |                          |
| Confirmare factură         | GUID linie factură        | Linie factură                      | GUID înregistrare vânzări facturate          | Real                   |
| GUID factură                 | Factură                  | GUID înregistrare vânzări facturate          | Real                            |                          |
| GUID detaliu linie factură     | Detaliu linie factură      | GUID înregistrare vânzări facturate          | Real                            |                          |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID înregistrare vânzări facturate          | Real                            |                          |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | GUID înregistrare vânzări facturate          | Real                            |                          |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID inversare vânzări nefacturate      | Real                            |                          |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | GUID inversare vânzări nefacturate      | Real                            |                          |
| Corecție factură schiță     | Vechiul GUID DLF             | Tranzacție linie factură          | Corecție GUID DLF               | Tranzacție linie factură |
| Vechiul GUID DL                  | Linie factură             | Corecție GUID DLF               | Tranzacție linie factură          |                          |
| Vechiul GUID factură             | Factură                  | Corecție GUID DLF               | Tranzacție linie factură          |                          |
| GUID înregistrare intrare de timp       | Intrare de timp               | Corecție GUID DLF               | Tranzacție linie factură          |                          |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | Corecție GUID DLF               | Tranzacție linie factură          |                          |
| Corecție factură confirmată | Vechiul GUID DLF             | Tranzacție linie factură          | GUID valoare reală vânzări facturate inversate | Real                   |
| Vechiul GUID DL                  | Linie factură             | GUID valoare reală vânzări facturate inversate | Real                            |                          |
| Vechiul GUID factură             | Factură                  | GUID valoare reală vânzări facturate inversate | Real                            |                          |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID valoare reală vânzări facturate inversate | Real                            |                          |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | GUID valoare reală vânzări facturate inversate | Real                            |                          |
| Vechiul GUID DLF                 | Tranzacție linie factură | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| Vechiul GUID DL                  | Linie factură             | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| Vechiul GUID factură             | Factură                  | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| GUID înregistrare intrare de timp       | Intrare de timp               | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| GUID înregistrare linie de jurnal     | Linie de jurnal             | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| Corecție GUID DLF          | Tranzacție linie factură | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| Corecție GUID DL           | Linie factură             | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |
| Corecție GUID factură      | Factură                  | GUID nou valoare reală vânzări nefacturate    | Real                            |                          |


Următoarea ilustrație arată legăturile care sunt create între diferite tipuri de valori reale și sursele acestora la diferite evenimente folosind exemplul de intrări de timp în Project Operations.

> ![Modul în care valorile reale sunt legate la înregistrările sursă în Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
