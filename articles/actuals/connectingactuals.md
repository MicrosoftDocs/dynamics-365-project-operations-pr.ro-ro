---
title: Conexiunile tranzacțiilor - Conectarea datelor reale ale diferitelor tipuri de tranzacții
description: Acest articol explică modul în care o conexiune de tranzacție este utilizată pentru a lega datele reale de diferite tipuri pentru a ajuta la urmărirea profitabilității, a întârzierilor de facturare și a calculelor veniturilor facturate versus nefacturate.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926101"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Conexiunile tranzacțiilor - Conectarea datelor reale ale diferitelor tipuri de tranzacții

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Înregistrările de conexiuni ale tranzacțiilor sunt create pentru a lega reale de diferite tipuri, pe măsură ce timpul, cheltuielile sau utilizarea materialelor se deplasează în ciclul său de viață de la etapa de cotație sau de pre-vânzare la etapa de contract, aprobări și/sau retrageri, facturare și, eventual, facturare de credit sau corecție. .

Următorul exemplu arată procesarea tipică a intrărilor de timp într-un ciclu de viață al proiectului în Project Operations.

> ![Procesarea intrărilor de timp în Operațiuni de proiect.](media/basic-guide-17.png)

Procesarea intrărilor de timp într-un ciclu de viață al unui proiect Project Operations urmează acești pași: 

1. Trimiterea unei intrări de timp determină crearea a două linii de jurnal: unul pentru cost și unul pentru vânzări nefacturate. 
2. Aprobarea eventuală a introducerii timpului face ca două valori reale să fie create: unul pentru cost și unul pentru vânzări nefacturate. Aceste 2 date reale sunt legate folosind conexiuni de tranzacție.
3. Atunci când utilizatorul creează o factură de proiect, tranzacția linie factură este creată utilizând date din valorile reale pentru vânzările nefacturate.
4. Când factura este confirmată, se creează două noi date reale: o anulare a vânzărilor nefacturate și o vânzări efective facturate. Anularea vânzărilor nefacturate și vânzările reale nefacturate inițiale sunt conectate folosind conexiuni de tranzacție inversă. Vânzările facturate și datele reale ale vânzărilor inițiale nefacturate sunt, de asemenea, conectate pentru a arăta legăturile dintre ceea ce a fost cândva venitul întârziat sau în curs (WIP) și ceea ce este acum venit facturat.   

Fiecare eveniment din fluxul de lucru de procesare declanșează crearea de înregistrări în **Conexiunea tranzacției** masa. Acest lucru ajută la construirea unei urme a relațiilor dintre înregistrările care sunt create prin introducerea de timp, linia jurnalului, detaliile reale și linia de factură.

Următorul tabel arată înregistrările din **Conexiunea tranzacției** entitate pentru fluxul de lucru anterior.

|Eveniment                   |Tranzacție 1                 |Rol tranzacție 1 |Tip tranzacție 1       |Tranzacție 2          |Rol tranzacție 2 |Tip tranzacție 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Remitere intrare de timp   |GUID linie de jurnal (vânzări)     |Vânzări nefacturate |msdyn_journalline            |GUID linie de jurnal (cost)     |Cost            |msdyn_journalline  |
|Aprobare timp           |GUID valori reale nefacturate (vânzări)  |Vânzări nefacturate |msdyn_actual                 |GUID valoare reală cost (cost)       |Cost            |msdyn_actual       |
|Creare factură        |GUID detaliu linie factură      |Vânzări facturate   |msdyn_invoicelinetransaction |GUID valori reale vânzări nefacturate   |Vânzări nefacturate  |msdyn_actual       |
|Confirmare factură    |Inversarea GUID-ului real         |Inversare      |msdyn_actual                 |GUID vânzări inițiale nefacturate |Inițiale        |msdyn_actual       |
|                        |GUID vânzări facturate             |Vânzări facturate   |msdyn_actual                 |GUID valori reale vânzări nefacturate   |Vânzări nefacturate  |msdyn_actual       |
|Corecție factură schiță |GUID tranzacție linie factură|Înlocuire      |msdyn_invoicelinetransaction |GUID vânzări facturate            |Inițiale        |msdyn_actual       |
|Confirmare corecție factură|GUID inversare vânzări facturate  |Inversare      |msdyn_actual                 |GUID vânzări facturate            |Inițiale        |msdyn_actual       |
|                        |Noul GUID pentru vânzări nefacturate |Înlocuire            |msdyn_actual                 |GUID vânzări facturate            |Inițiale        |msdyn_actual       |


Următoarea ilustrație arată legăturile care sunt create între diferite tipuri de realizări la diferite evenimente folosind exemplul de intrări de timp în Operațiuni de proiect.

> ![Cum sunt legate între ele elementele reale de diferite tipuri în Operațiunile de proiect.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
