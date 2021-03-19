---
title: De ce prețul pentru cheltuielile reale revine la zero?
description: Depanarea motivului pentru care prețul pentru cheltuielile reale revine la zero.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285865"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>De ce prețul pentru cheltuielile reale de costuri are valoarea implicită zero?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Acest FAQ se aplică cheltuielilor efective în cazul în care clasa de tranzacție este setată la Cheltuieli și tipul de tranzacție este Costul.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Depanarea ratelor de cost pe costurile reale pentru cheltuieli

Mergeți la intrarea pentru cheltuieli conexă și asigurați-vă că există o valoare în câmpul de intrare pentru cheltuieli. Dacă intrarea de cheltuieli inițială nu avea câmpul sumă completat, atunci ați izolat problema.
 
Pentru a rezolva această problemă, recreați intrarea cheltuieli cu o valoare validă și aprobați-o.


[!INCLUDE[footer-include](../includes/footer-banner.md)]