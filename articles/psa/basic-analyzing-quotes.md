---
title: Analiza ofertelor de proiect
description: Acest subiect oferă informații despre analiza ofertelor de proiect.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145238"
---
# <a name="analysis-of-project-quotes"></a>Analiza ofertelor de proiect

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analizează ofertele de proiect pentru estimarea profitabilității. De asemenea, analizează cât de bine este aliniată oferta la așteptările clienților despre data de livrare sau data finalizării și despre buget.

## <a name="profitability-analysis"></a>Analiza de profitabilitate

Project Service Automation analizează profitabilitatea prin utilizarea marjei brute și a marjei brute ajustate.

- Marjele brute se calculează utilizând următoarea formulă:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Marja brută ajustată se calculează utilizând următoarea formulă:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

În cazul în care valorile pentru marja brută și marja brută ajustată diferă cu o marjă largă, o mare parte din activitatea din ofertă este clasificată ca netarifabilă.

## <a name="analysis-of-customer-expectations"></a>Analiza așteptărilor clientului

Aveți posibilitatea să analizați ofertele și să generați diagrame pentru așteptările clienților despre planificare și buget dacă introduceți valori pentru următoarele câmpuri:

- Câmpul **Dată solicitată pentru livrare** din antetul ofertei.
- Câmpul **Buget client** pentru fiecare linie de ofertă (pentru linii bazate pe proiect și linii bazate pe produse).

Analiza așteptărilor clienților cu privire la planificare se face comparând cea mai recentă dată de încheiere a detaliilor liniei de ofertă cu data de livrare solicitată în toate liniile de ofertă din ofertă.

Analiza așteptărilor clienților cu privire la buget se face prin compararea sumei bugetului total al clienților cu valoarea ofertată în toate liniile de ofertă.
