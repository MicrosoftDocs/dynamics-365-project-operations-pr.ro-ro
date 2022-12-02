---
title: Confirmarea unei facturi de furnizor pentru proiect
description: Acest articol explică cum să confirmați o factură de furnizor de proiect în Microsoft Dynamics 365 Project Operations și impactul financiar al confirmării unei facturi de furnizor de proiect.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261528"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmarea unei facturi de furnizor pentru proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

După ce ați verificat toate rândurile de pe o factură de furnizor în Microsoft Dynamics 365 Project Operations, puteți utiliza acțiunea Confirmare pentru a confirma factura furnizorului.

Când selectați **Confirmare** pe o factură de furnizor, apare următorul comportament:

1. Starea facturii de furnizor este actualizată la **Confirmat**.
2. Factura de furnizor confirmată și înregistrările asociate acesteia devin numai pentru citire și nu pot fi editate sau șterse.
3. Dacă orice costuri efective fac referire la linia de facturare a furnizorului ca parte a procesului de potrivire, toate costurile reale care sunt asociate cu linia de facturare a furnizorului la care se face referire sunt inversate.
4. Noile costuri reale sunt create prin utilizarea informațiilor de pe linia de facturare a furnizorului.
5. După confirmarea facturii de furnizor, nu mai puteți crea jurnale de corecție, procesa retrageri de intrare de timp sau anula aprobarea valorilor reale inițiale pentru timp, cheltuieli sau materiale care au fost inversate.

> [!NOTE]
> Dacă orice linie de pe o factură de furnizor are o altă stare de verificare decât **Finalizat**, factura furnizorului nu poate fi confirmată.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
