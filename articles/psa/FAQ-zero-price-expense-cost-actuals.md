---
title: De ce prețul pentru cheltuielile reale revine la zero?
description: Depanarea motivului pentru care prețul pentru cheltuielile reale revine la zero.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082817"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>De ce prețul pentru cheltuielile reale revine la zero?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Acest FAQ se aplică cheltuielilor efective în cazul în care clasa de tranzacție este setată la Cheltuieli și tipul de tranzacție este Costul.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Depanarea ratelor de cost pe costurile reale pentru cheltuieli

Mergeți la intrarea pentru cheltuieli conexă și asigurați-vă că există o valoare în câmpul de intrare pentru cheltuieli. Dacă intrarea de cheltuieli inițială nu avea câmpul sumă completat, atunci ați izolat problema.
 
Pentru a rezolva această problemă, recreați intrarea cheltuieli cu o valoare validă și aprobați-o.
