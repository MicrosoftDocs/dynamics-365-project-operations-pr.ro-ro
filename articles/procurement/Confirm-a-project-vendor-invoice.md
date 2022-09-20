---
title: Confirmați facturile furnizorilor de proiect
description: Acest articol explică cum să confirmați o factură de furnizor de proiect în Microsoft Dynamics 365 Project Operations și descrie impactul financiar al confirmării unei facturi de furnizor de proiect.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475474"
---
# <a name="confirm-project-vendor-invoices"></a>Confirmați facturile furnizorilor de proiect

_ **Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc

Cand **Este necesară confirmarea manuală de către PM** parametrul este activat, facturile furnizorilor care sunt create în Microsoft Dataverse avea **Proiect** stare. Facturile de furnizor care sunt create în acest fel trebuie revizuite și confirmate manual. Cand **Este necesară confirmarea manuală de către PM** parametrul este dezactivat, facturi de furnizor care sunt create în Dataverse sunt confirmate automat. Nu este necesară nicio acțiune suplimentară. 

După ce ați verificat toate rândurile de pe o factură de furnizor în Dynamics 365 Project Operations, Selectați **A confirma** pentru a confirma factura furnizorului.

Când selectați **A confirma** pe o factură de furnizor, apare următorul comportament:

1. Starea facturii furnizorului este actualizată la **Confirmat**.
1. Factura de furnizor confirmată și înregistrările asociate acesteia devin numai pentru citire și nu pot fi editate sau șterse.
1. Dacă costurile efective fac referire la linia de factură a furnizorului ca parte a procesului de potrivire, toate costurile reale care sunt asociate cu linia de factură a furnizorului la care se face referire sunt inversate.
1. Noile costuri reale sunt create prin utilizarea informațiilor de pe linia de factură a furnizorului.
1. Nu mai puteți crea jurnale de corecție, nu mai puteți procesa rechemarile de înregistrări de timp sau nu mai puteți anula aprobarea timpului inițial, a cheltuielilor sau a efectivelor materiale care au fost inversate.
1. În Dynamics 365 Finance, **Costul proiectului** valoarea este actualizată utilizând jurnalul de integrare a proiectului, iar contul de integrare Achiziții este *inversat* după ce jurnalul de integrare a proiectului este postat.

> [!NOTE]
> Dacă orice rând de pe o factură de furnizor are o stare de verificare diferită de **Complet**, factura furnizorului nu poate fi confirmată.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
