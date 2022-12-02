---
title: Tranzacții de business în Project Operations
description: Acest articol oferă o prezentare generală a conceptului de tranzacții comerciale în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923295"
---
# <a name="business-transactions-in-project-operations"></a>Tranzacții de business în Project Operations

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În Microsoft Dynamics 365 Project Operations, *tranzacția comercială* este un concept abstract care nu este reprezentat de nicio entitate. Cu toate acestea, unele câmpuri și procese comune pe entități sunt concepute pentru a utiliza conceptul de tranzacții comerciale. Următoarele entități utilizează această abstracțiune:

- Detalii linie de ofertă
- Detalii linie de contract
- Linii de estimare
- Linii de jurnal
- Reale

Dintre aceste entități, Detaliile liniei de ofertă, Detaliile liniei de contract și Liniile de estimare sunt mapate la *faza de estimare* din ciclul de viață al proiectului. Entitățile Linii de jurnal și Entitățile Valori reale sunt mapate la faza de *execuție* în ciclul de viață al proiectului.

Project Operations tratează înregistrările din toate aceste cinci entități ca tranzacții comerciale. Singura diferență constă în faptul că înregistrările din entități care sunt mapate la faza de estimare (Detaliile liniei de ofertă, Detaliile liniei de contract și Liniile de estimare) sunt considerate *previziuni financiare*, în timp ce înregistrările din entitățile care sunt mapate la faza de execuție (Linii de jurnal și Valori reale) sunt considerate *fapte financiare* care au avut deja loc.

Pentru mai multe informații, consultați [Estimări](../project-management/estimating-projects-overview.md) și [Valori reale](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concepte care sunt unice pentru tranzacțiile comerciale

Conceptele următoare sunt unice pentru conceptul de tranzacții comerciale:

- Tipul tranzacției
- Clasă de tranzacții
- Origine tranzacție
- Conexiune de tranzacție

### <a name="transaction-type"></a>Tipul tranzacției

Tipul tranzacției reprezintă temporizarea și contextul impactului financiar asupra unui proiect. Este reprezentat de un set de opțiuni care are următoarele valori acceptate în Project Operations:

- Cost
- Contract pentru proiect
- Vânzări nefacturate
- Vânzări facturate
- Vânzări inter-organizaționale
- Cost de unitate resursă

### <a name="transaction-class"></a>Clasă de tranzacții

Clasa de tranzacții reprezintă diferitele tipuri de costuri suportate pentru proiecte. Este reprezentat de un set de opțiuni care are următoarele valori acceptate în Project Operations:

- Timp
- Cheltuială
- Material
- Taxă
- Jalon
- Taxe

> [!NOTE]
> Valoarea **Jalon** este utilizată, de obicei, de logica de afaceri pentru facturarea cu preț fix în Project Operations.

### <a name="transaction-origin"></a>Origine tranzacție

Originea tranzacției este o entitate care stochează originea fiecărei tranzacții comerciale pentru a ajuta la raportare și trasabilitate. Pe măsură ce execuția proiectului începe, fiecare tranzacție comercială creează o altă tranzacție comercială care, la rândul său, va crea o altă tranzacție comercială și așa mai departe.

### <a name="transaction-connection"></a>Conexiune de tranzacție

Conexiunea de tranzacție este o entitate care stochează relația dintre două tranzacții comerciale similare, precum cost și valorile reale corelate cu vânzările sau inversările tranzacțiilor care sunt declanșate de activități de facturare, cum ar fi confirmarea facturii sau corecții ale facturii.

Împreună, entitățile Origine tranzacție și Conexiune de tranzacție vă ajută să urmăriți relațiile dintre tranzacțiile comerciale și acțiuni care au cauzat crearea unei tranzacții comerciale specifice.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
