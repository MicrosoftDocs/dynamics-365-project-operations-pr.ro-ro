---
title: Confirmarea facturilor de la furnizorii din proiect
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
# <a name="confirm-project-vendor-invoices"></a>Confirmarea facturilor de la furnizorii din proiect

_ **Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc

Cand parametrul **Este necesară confirmarea manuală de către MP** este activat, facturile de furnizori care sunt create în Microsoft Dataverse au starea **Schiță**. Facturile de furnizor care sunt create în acest fel trebuie revizuite și confirmate manual. Cand parametrul **Este necesară confirmarea manuală de către MP** este dezactivat, facturile de furnizor care sunt create în Dataverse sunt confirmate automat. Nu este necesară nicio acțiune suplimentară. 

După ce ați verificat toate rândurile de pe o factură de furnizor în Dynamics 365 Project Operations, selectați **Confirmare** pentru a confirma factura de furnizor.

Când selectați **Confirmare** pe o factură de furnizor, apare următorul comportament:

1. Starea facturii de furnizor este actualizată la **Confirmat**.
1. Factura de furnizor confirmată și înregistrările asociate acesteia devin numai pentru citire și nu pot fi editate sau șterse.
1. Dacă orice costuri efective fac referire la linia de facturare a furnizorului ca parte a procesului de potrivire, toate costurile reale care sunt asociate cu linia de facturare a furnizorului la care se face referire sunt inversate.
1. Noile costuri reale sunt create prin utilizarea informațiilor de pe linia de facturare a furnizorului.
1. Nu mai puteți crea jurnale de corecție, procesa retrageri de intrări de timp sau anula aprobarea valorilor reale inițiale pentru timp, cheltuieli sau materiale care au fost inversate.
1. În Dynamics 365 Finance, valoarea **Cost proiect** este actualizată utilizând Jurnalul de integrare a proiectului, iar Contul de integrare Achiziții este *Inversat* după ce jurnalul de integrare a proiectului este publlicat.

> [!NOTE]
> Dacă orice linie de pe o factură de furnizor are o altă stare de verificare decât **Finalizat**, factura furnizorului nu poate fi confirmată.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
