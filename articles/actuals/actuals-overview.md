---
title: Date reale
description: Acest articol oferă informații despre cum să lucrați cu valorile reale în Microsoft Dynamics 365 Project Operations.
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

Valorile reale reprezintă progresul financiar revizuit și aprobat și evoluția planificată a unui proiect. Acestea sunt create atunci când timpul, cheltuielile și înregistrările de utilizare a materialelor, intrările din jurnal și facturile sunt aprobate.

> [!IMPORTANT]
> Valorile reale nu trebuie editate sau șterse din sistem. În caz contrar, integritatea financiară și orice integrare cu alte sisteme financiare și contabile ar putea fi afectate negativ. Microsoft Dynamics 365 Project Operations vă permite să utilizați inversarea și înlocuirea valorilor reale pentru a edita valorile reale în diferite puncte din ciclul de viață al procesului de afaceri al proiectelor dvs.

## <a name="recording-actuals-based-on-project-events"></a>Înregistrarea valorilor reale pe baza evenimentelor proiectului

Project Operations înregistrează tranzacțiile financiare care apar în timpul unui ciclu de viață al angajamentului de proiect ca valori reale. Crearea valorilor reale la diferite evenimente din ciclul de viață variază, în funcție de faptul dacă angajamentul proiectului folosește modelul de facturare pentru timp și materiale sau modelul de facturare pentru preț fix și dacă este în stadiul de pre-vânzare sau este un proiect intern.

Următoarele articole explică impactul asupra tabelului Valori reale la diferite evenimente pentru diferite variații:

- [Impactul datelor reale într-un angajament de timp și materiale](ActualsonTM.md)
- [Impactul datelor reale într-un angajament cu preț fix](ActualonFP.md)
- [Impactul datelor reale în timpul etapei de pre-vânzare a unui angajament](ActualonPreSales.md)
- [Impactul datelor reale pentru un proiect intern](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
