---
title: Anularea unei facturi de furnizor pentru proiect
description: Acest articol explică cum să anulați o factură de furnizor de proiect în Microsoft Dynamics 365 Project Operations și impactul financiar al anulării unei facturi de furnizor de proiect.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911565"
---
# <a name="cancel-a-project-vendor-invoice"></a>Anularea unei facturi de furnizor pentru proiect

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

După ce o factură de furnizor este confirmată, aceasta nu poate fi editată sau ștearsă. Dacă a existat o eroare pe o factură de furnizor care a fost confirmată, puteți utiliza acțiunea Anulare pentru a inversa impactul facturii de furnizor și pentru a crea o nouă factură de furnizor.

Când selectezi **Anulare** pe o factură de furnizor, apare următorul comportament:

1. Starea facturii furnizorului este actualizată la **Anulat**.
2. Factura de furnizor anulată și înregistrările asociate acesteia devin numai pentru citire și nu pot fi editate sau șterse.
3. Orice costuri reale care au fost create pe baza liniilor de factură a furnizorului ca parte a confirmării facturii furnizorului sunt inversate.
4. Dacă costurile reale au fost legate de liniile de factură a furnizorului ca parte a procesului de potrivire, confirmarea originală a facturii furnizorului le-a inversat. În timpul anulării facturii furnizorului, acele costuri reale sunt recreate. Originile indică intrările privind timpul, cheltuielile sau utilizarea materialului.
5. După ce factura furnizorului este anulată, puteți crea din nou jurnalele de corecție, puteți procesa retrageri de timp de intrare și puteți anula aprobarea timpului inițial, a cheltuielilor sau a materialelor reale.

> [!NOTE]
> Numai facturile de furnizor de proiect confirmate pot fi anulate. Facturile furnizorilor din alte state nu pot fi anulate.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
