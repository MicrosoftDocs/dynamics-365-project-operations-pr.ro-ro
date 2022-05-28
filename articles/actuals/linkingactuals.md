---
title: Originile tranzacției - Conectați datele reale la sursa lor
description: Acest subiect explică modul în care conceptul originii tranzacției este utilizat pentru a lega datele reale la înregistrările sursă originale, cum ar fi înregistrarea timpului, înregistrarea cheltuielilor sau jurnalele de utilizare a materialelor.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584841"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Originile tranzacției - Conectați datele reale la sursa lor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Înregistrările despre originea tranzacției sunt create pentru a lega datele reale la sursa lor, astfel de intrări de timp, înregistrări de cheltuieli, jurnalele de utilizare a materialelor și facturile de proiect.

Următorul exemplu arată procesarea tipică a intrărilor de timp într-un ciclu de viață al proiectului în Project Operations.

> ![Timp de procesare întregi în Operațiuni de proiect.](media/basic-guide-17.png)
 
1. Trimiterea unei intrări de timp determină crearea a două linii de jurnal: unul pentru cost și unul pentru vânzări nefacturate.
2. Aprobarea eventuală a introducerii timpului face ca două valori reale să fie create: unul pentru cost și unul pentru vânzări nefacturate.
3. Atunci când utilizatorul creează o factură de proiect, tranzacția linie factură este creată utilizând date din valorile reale pentru vânzările nefacturate.
4. Când este confirmată factura, sunt create două valori reale: o inversare a vânzărilor nefacturate și o valoare reală pentru vânzări facturate.

Fiecare eveniment din acest flux de lucru de procesare declanșează crearea de înregistrări în entitatea de origine a tranzacției pentru a ajuta la construirea unei urme a relațiilor dintre aceste înregistrări care sunt create prin introducerea de timp, rândul jurnalului, detaliile reale și linia de factură.

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


Următoarea ilustrație arată legăturile care sunt create între efective și sursele lor la diferite evenimente folosind exemplul de intrări de timp în Operațiuni de proiect.

> ![Modul în care datele reale sunt legate de înregistrările sursă în Operațiuni de proiect.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
