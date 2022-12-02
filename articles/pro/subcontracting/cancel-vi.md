---
title: Anularea unei facturi de furnizor pentru proiect
description: Acest articol explică cum să anulați o factură de furnizor de proiect în Microsoft Dynamics 365 Project Operations și impactul financiar al anulării unei facturi de furnizor de proiect.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261106"
---
# <a name="cancel-a-project-vendor-invoice"></a>Anularea unei facturi de furnizor pentru proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

După confirmarea unei facturi de furnizor, aceasta nu poate fi editată sau ștearsă. Dacă a existat o eroare pe o factură de furnizor care a fost confirmată, puteți utiliza acțiunea Anulare pentru a inversa impactul facturii de furnizor și pentru a crea o nouă factură de furnizor.

Când selectați **Anulare** pe o factură de furnizor, apare următorul comportament:

1. Starea facturii de furnizor este actualizată la **Anulat**.
2. Factura de furnizor anulată și înregistrările asociate acesteia devin numai pentru citire și nu pot fi editate sau șterse.
3. Orice costuri reale care au fost create pe baza liniilor de facturare a furnizorului ca parte a confirmării facturii furnizorului sunt inversate.
4. Dacă costurile reale au fost legate de liniile de facturare a furnizorului ca parte a procesului de potrivire, confirmarea inițială a facturii furnizorului le-a inversat. În timpul anulării facturii furnizorului, acele costuri reale sunt recreate. Originile indică intrările de timp, cheltuieli sau utilizare a materialelor.
5. După anularea facturii de furnizor, puteți crea din nou jurnale de corecție, puteți procesa retragerile de intrare de timp și puteți anula aprobarea valorilor reale inițiale pentru timp, cheltuieli sau materiale.

> [!NOTE]
> Numai facturile de furnizor de proiect confirmate pot fi anulate. Facturile de furnizor din alte state nu pot fi anulate.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
