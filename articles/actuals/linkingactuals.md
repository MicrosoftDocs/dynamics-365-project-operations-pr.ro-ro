---
title: Conectarea datelor reale la înregistrările originale
description: Acest subiect explică cum să legați datele reale la înregistrările originale, cum ar fi introducerea timpului, introducerea cheltuielilor sau jurnalele de utilizare a materialelor.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991771"
---
# <a name="link-actuals-to-original-records"></a>Conectarea datelor reale la înregistrările originale

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


În Dynamics 365 Project Operations, *Tranzacție comercială* este un concept abstract care nu este reprezentat de o entitate. Cu toate acestea, unele câmpuri și procese comune pe entități sunt concepute pentru a utiliza conceptul de tranzacții comerciale. Următoarele entități utilizează acest concept:

- Detalii linie de ofertă
- Detalii linie de contract
- Linii de estimare
- Linii de jurnal
- Reale

Dintre aceste entități, **Detaliile liniei de ofertă**, **Detaliile liniei de contract** și **Liniile de estimare** sunt mapate la faza de estimare din ciclul de viață al proiectului. Entitățile **Linii de jurnal** și **Entități reale** sunt mapate la faza de execuție în ciclul de viață al proiectului.

Project Operations recunoaște înregistrările din aceste cinci entități ca tranzacții comerciale. Singura distincție este că înregistrările din entități care sunt mapate la faza de estimare sunt considerate previziuni financiare, în timp ce înregistrările din entități care sunt mapate la faza de execuție sunt considerate fapte financiare care au avut deja loc.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concepte care sunt unice pentru tranzacțiile comerciale
Conceptele următoare sunt unice pentru conceptul de tranzacții comerciale:

- Tipul tranzacției
- Clasă de tranzacții
- Origine tranzacție
- Conexiune de tranzacție

### <a name="transaction-type"></a>Tipul tranzacției

Tipul tranzacției reprezintă temporizarea și contextul impactului financiar asupra unui proiect. Acesta este reprezentat de un set de opțiuni care are următoarele valori acceptate în Project Operations:

  - Cost
  - Contract pentru proiect
  - Vânzări nefacturate
  - Vânzări facturate
  - Vânzări inter-organizaționale
  - Cost de unitate resursă

### <a name="transaction-class"></a>Clasă de tranzacții

Clasa de tranzacții reprezintă diferitele tipuri de costuri suportate pentru proiecte. Acesta este reprezentat de un set de opțiuni care are următoarele valori acceptate în Project Operations:

  - Timp
  - Cheltuială
  - Material
  - Taxă
  - Jalon
  - Taxe

**Jalon** este utilizată de obicei de logica de afaceri pentru facturarea cu preț fix în Project Operations.

### <a name="transaction-origin"></a>Origine tranzacție

**Originea tranzacției** este o entitate care stochează originea fiecărei tranzacții comerciale. Odată cu începerea unui proiect, fiecare tranzacție comercială va da naștere unei alte tranzacții comerciale care, la rândul său, va crea alta și așa mai departe. Entitatea de origine a tranzacției este concepută pentru a stoca date despre originea fiecărei tranzacții pentru a ajuta la raportare și trasabilitate. 

### <a name="transaction-connection"></a>Conexiune de tranzacție

**Conexiunea de tranzacție** este o entitate care stochează relația dintre două tranzacții comerciale similare, precum cost și valorile reale corelate cu vânzările, sau inversările tranzacțiilor care sunt declanșate de activități de facturare, cum ar fi confirmarea facturii sau corecțiile facturilor.

Împreună, entitățile **Origine tranzacție** și **Conexiune de tranzacție** vă ajută să monitorizați relațiile dintre tranzacțiile comerciale și acțiuni care au dus la o tranzacție comercială specifică.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplu: cum funcționează Origine tranzacție cu Conexiune de tranzacție

Următorul exemplu arată procesarea tipică a intrărilor de timp într-un ciclu de viață al proiectului în Project Operations.

> ![Procesarea intrărilor de timp dintr-un ciclu de viață Project Service.](media/basic-guide-17.png)
 
1. O remitere de intrare de timp creează două linii de jurnal: o linie pentru cost și o linie pentru vânzările nefacturate.
2. Aprobarea finală a intrării de timp creează a două valori reale: una pentru cost și una pentru vânzările nefacturate.
3. Atunci când se creează o nouă factură de proiect, tranzacția linie factură este creată utilizând date din valorile reale pentru vânzările nefacturate. 
4. Când este confirmată factura, sunt create două valori reale: o inversare a vânzărilor nefacturate reale și o valoare reală pentru vânzări facturate.

Fiecare dintre aceste evenimente creează o înregistrare în entitățile **Originea tranzacției** și **Conexiune de tranzacție**. Aceste noi înregistrări vă ajută să construiți un istoric al relațiilor dintre înregistrările care sunt create pe intrarea în timp, linia de jurnal, datele reale și detaliile liniei de facturare.

Următorul tabel afișează înregistrările din entitatea **Origine tranzacție** pentru fluxul de lucru.

| Eveniment                        | Origine                   | Tip de origine                       | Tranzacție                       | Tip tranzacție         |
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

Următorul tabel afișează înregistrările din entitatea **Conexiune de tranzacție** pentru fluxul de lucru.

| Eveniment                          | Tranzacție 1                 | Rol tranzacție 1 | Tip tranzacție 1           | Tranzacție 2                | Rol tranzacție 2 | Tip tranzacție 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Remitere intrare de timp          | GUID linie de jurnal (vânzări)     | Vânzări nefacturate     | msdyn_journalline            | GUID linie de jurnal (cost)     | Cost               | msdyn_journalline  |
| Aprobare timp                  | GUID valori reale nefacturate (vânzări)  | Vânzări nefacturate     | msdyn_actual                 | GUID valoare reală cost (cost)       | Cost               | msdyn_actual       |
| Creare factură               | GUID detaliu linie factură      | Vânzări facturate       | msdyn_invoicelinetransaction | GUID valori reale vânzări nefacturate   | Vânzări nefacturate     | msdyn_actual       |
| Confirmare factură           | Inversarea GUID-ului real         | Inversare          | msdyn_actual                 | GUID vânzări inițiale nefacturate | Inițiale           | msdyn_actual       |
| GUID vânzări facturate              | Vânzări facturate                  | msdyn_actual       | GUID valori reale vânzări nefacturate   | Vânzări nefacturate               | msdyn_actual       |                    |
| Corecție factură schiță       | GUID tranzacție linie factură | Înlocuire          | msdyn_invoicelinetransaction | GUID vânzări facturate            | Inițiale           | msdyn_actual       |
| Confirmare corecție factură     | GUID inversare vânzări facturate    | Inversare          | msdyn_actual                 | GUID vânzări facturate            | Inițiale           | msdyn_actual       |
| GUID nou valoare reală vânzări nefacturate | Înlocuire                     | msdyn_actual       | GUID vânzări facturate            | Inițiale                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
