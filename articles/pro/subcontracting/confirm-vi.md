---
title: Confirmați o factură de furnizor de proiect
description: Acest subiect explică cum să confirmați o factură de furnizor de proiect în Microsoft Dynamics 365 Project Operations și impactul financiar al confirmării unei facturi de furnizor de proiect.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595743"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmați o factură de furnizor de proiect

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

După ce ați verificat toate rândurile de pe o factură de furnizor în Microsoft Dynamics 365 Project Operations, puteți utiliza acțiunea Confirmare pentru a confirma factura furnizorului.

Când selectezi **A confirma** pe o factură de furnizor, apare următorul comportament:

1. Starea facturii furnizorului este actualizată la **Confirmat**.
2. Factura confirmată a furnizorului și înregistrările asociate acesteia devin numai pentru citire și nu pot fi editate sau șterse.
3. Dacă costurile efective fac referire la linia de factură a furnizorului ca parte a procesului de potrivire, toate costurile reale care sunt asociate cu linia de factură a furnizorului la care se face referire sunt inversate.
4. Noile costuri reale sunt create prin utilizarea informațiilor de pe linia de factură a furnizorului.
5. După confirmarea facturii furnizorului, nu mai puteți crea jurnale de corecție, nu mai puteți procesa retrageri de timp de intrare sau nu mai puteți anula aprobarea timpului inițial, a cheltuielilor sau a materialelor reale care au fost inversate.

> [!NOTE]
> Dacă orice rând de pe o factură de furnizor are o stare de verificare diferită de **Complet**, factura furnizorului nu poate fi confirmată.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]