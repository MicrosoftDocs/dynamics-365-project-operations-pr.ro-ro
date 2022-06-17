---
title: Tranzacții comerciale
description: Acest articol oferă informații despre tranzacțiile comerciale.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 07002890e0474dbdaf979d9dcdf064e9c382a0f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927021"
---
# <a name="business-transactions"></a>Tranzacții comerciale

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

În Dynamics 365 Project Service Automation, *Tranzacție comercială* este un concept abstract care nu este reprezentat de nicio entitate. Cu toate acestea, unele câmpuri și procese comune pe entități sunt concepute pentru a utiliza conceptul de tranzacții comerciale. Următoarele entități utilizează această abstracțiune:

- Detalii linie de ofertă
- Detalii linie de contract
- Linii de estimare
- Linii de jurnal
- Reale

Dintre aceste entități, Detaliile liniei de ofertă, Detaliile liniei de contract și Liniile de estimare sunt mapate la faza de estimare din ciclul de viață al proiectului. Entitățile Linii de jurnal și Valori reale sunt mapate la faza de execuție în ciclul de viață al proiectului.

PSA tratează înregistrările din aceste cinci entități ca tranzacții comerciale. Singura distincție este că înregistrările din entități care sunt mapate la faza de estimare sunt considerate previziuni financiare, în timp ce înregistrările din entități care sunt mapate la faza de execuție sunt considerate fapte financiare care au avut deja loc.

Pentru mai multe informații, consultați [Estimări](estimates.md) și [Valori reale](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concepte care sunt unice pentru tranzacțiile comerciale
Conceptele următoare sunt unice pentru conceptul de tranzacții comerciale:

- Tipul tranzacției
- Clasă de tranzacții
- Origine tranzacție
- Conexiune de tranzacție

### <a name="transaction-type"></a>Tipul tranzacției

Tipul tranzacției reprezintă temporizarea și contextul impactului financiar asupra unui proiect. Acesta este reprezentat de un set de opțiuni care are următoarele valori acceptate în PSA:
- Cost
- Contract pentru proiect
- Vânzări nefacturate
- Vânzări facturate
- Vânzări inter-organizaționale
- Cost de unitate resursă

### <a name="transaction-class"></a>Clasă de tranzacții

Clasa de tranzacții reprezintă diferitele tipuri de costuri suportate pentru proiecte. Acesta este reprezentat de un set de opțiuni care are următoarele valori acceptate în PSA:

- Time
- Cheltuială
- Materiale
- Taxă
- Jalon
- Impozit

Valoarea **Jalon** este utilizată de obicei de logica de afaceri pentru facturarea cu preț fix în PSA.

### <a name="transaction-origin"></a>Origine tranzacție

Originea tranzacției este o entitate care stochează originea fiecărei tranzacții comerciale. Pe măsură ce execuția proiectului începe, fiecare tranzacție comercială va da naștere unei alte tranzacții comerciale, care la rândul său va crea o alta și așa mai departe. Entitatea de origine a tranzacției a fost proiectată pentru a stoca date despre originea fiecărei tranzacții pentru a asista raportarea și trasabilitatea. 

### <a name="transaction-connection"></a>Conexiune de tranzacție

Conexiunea de tranzacție este o entitate care stochează relația dintre două tranzacții comerciale similare, precum cost și valorile reale corelate cu vânzările, sau inversările tranzacțiilor care sunt declanșate de activități de facturare, cum ar fi confirmarea facturii sau corecțiile facturilor.

Împreună, entitățile Origine tranzacție și Conexiune de tranzacție vă ajută să monitorizați relațiile dintre tranzacțiile comerciale și acțiuni care au dus la crearea unei tranzacții comerciale specifice.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplu: cum funcționează Origine tranzacție cu Conexiune de tranzacție

Următorul exemplu arată procesarea tipică a intrărilor de timp într-un ciclu de viață al proiectului în PSA.

> ![Procesarea intrărilor de timp dintr-un ciclu de viață Project Service.](media/basic-guide-17.png)
 
1. Remiterea unei intrări de timp determină crearea a două linii de jurnal: una pentru cost și una pentru vânzările nefacturate.
2. Aprobarea eventuală a intrării de timp determină crearea a două valori reale: una pentru cost și una pentru vânzările nefacturate.
3. Atunci când utilizatorul creează o factură de proiect, tranzacția linie factură este creată utilizând date din valorile reale pentru vânzările nefacturate. 
4. Când este confirmată factura, sunt create două valori reale: o inversare a vânzărilor nefacturate și o valoare reală pentru vânzări facturate.

Fiecare dintre aceste evenimente declanșează crearea de înregistrări în entitățile Origine tranzacție și Conexiune de tranzacție, pentru a ajuta la construirea unei urmăriri a relațiilor dintre aceste înregistrări care sunt create pe baza detaliilor pentru intrarea de timp, linia de jurnal, valorile reale și linia factură.

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

Următorul tabel afișează înregistrările din entitatea Conexiune de tranzacție pentru fluxul de lucru precedent.

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
