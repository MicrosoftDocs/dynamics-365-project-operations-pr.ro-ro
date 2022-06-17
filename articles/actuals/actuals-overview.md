---
title: Date reale
description: Acest articol oferă informații despre cum să lucrați cu datele reale în Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924813"
---
# <a name="actuals"></a>Date reale

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Valorile reale reprezintă progresul financiar revizuit și aprobat și evoluția planificată a unui proiect. Acestea sunt create atunci când sunt aprobate înregistrările de timp, cheltuieli și utilizarea materialelor, înregistrările de jurnal și facturile.

> [!IMPORTANT]
> Datele reale nu trebuie editate sau șterse din sistem. În caz contrar, integritatea financiară și orice integrare cu alte sisteme financiare și contabile ar putea fi afectate negativ. Microsoft Dynamics 365 Project Operations vă permite să utilizați inversarea și înlocuirea datelor reale pentru a edita valorile reale în diferite puncte din ciclul de viață al procesului de afaceri al proiectelor dvs.

## <a name="recording-actuals-based-on-project-events"></a>Înregistrarea valorilor reale pe baza evenimentelor proiectului

Operațiunile de proiect înregistrează tranzacțiile financiare care au loc în timpul ciclului de viață al angajamentului de proiect ca date reale. Crearea efectivelor la diferite evenimente din ciclul de viață variază, în funcție de faptul dacă angajamentul proiectului folosește modelul de facturare cu timp și materiale sau modelul de facturare cu preț fix și dacă este în stadiul de pre-vânzare sau este un proiect intern.

Următoarele articole explică impactul asupra tabelului Realități la diferite evenimente pentru diferite variații:

- [Impactul real într-o angajare în timp și materiale](ActualsonTM.md)
- [Impactul real într-un angajament cu preț fix](ActualonFP.md)
- [Impactul real în timpul etapei de pre-vânzare a unui angajament](ActualonPreSales.md)
- [Impactul real pentru un proiect intern](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
