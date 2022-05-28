---
title: Date reale
description: Acest subiect oferă informații despre cum să lucrați cu cifrele reale în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581299"
---
# <a name="actuals"></a>Date reale

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Valorile reale reprezintă progresul financiar revizuit și aprobat și evoluția planificată a unui proiect. Acestea sunt create atunci când sunt aprobate înregistrările de timp, cheltuieli și utilizarea materialelor, înregistrările de jurnal și facturile.

> [!IMPORTANT]
> Datele reale nu trebuie editate sau șterse din sistem. În caz contrar, integritatea financiară și orice integrare cu alte sisteme financiare și contabile ar putea fi afectate negativ. Microsoft Dynamics 365 Project Operations vă permite să utilizați inversarea și înlocuirea datelor reale pentru a edita valorile reale în diferite puncte din ciclul de viață al procesului de afaceri al proiectelor dvs.

## <a name="recording-actuals-based-on-project-events"></a>Înregistrarea valorilor reale pe baza evenimentelor proiectului

Operațiunile de proiect înregistrează tranzacțiile financiare care au loc în timpul ciclului de viață al angajamentului de proiect ca date reale. Crearea efectivelor la diferite evenimente din ciclul de viață variază, în funcție de faptul dacă angajamentul proiectului folosește modelul de facturare cu timp și materiale sau modelul de facturare cu preț fix și dacă este în stadiul de pre-vânzare sau este un proiect intern.

Următoarele subiecte explică impactul asupra tabelului Realități la diferite evenimente pentru diferite variații:

- [Impactul real într-un timp și implicarea materialelor](ActualsonTM.md)
- [Impactul real într-un angajament cu preț fix](ActualonFP.md)
- [Impactul real în timpul etapei de pre-vânzare a unui angajament](ActualonPreSales.md)
- [Impactul real pentru un proiect intern](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
