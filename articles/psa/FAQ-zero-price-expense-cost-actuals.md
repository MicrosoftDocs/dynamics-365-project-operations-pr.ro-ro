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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146363"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>De ce prețul pentru cheltuielile reale de costuri are valoarea implicită zero?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Acest FAQ se aplică cheltuielilor efective în cazul în care clasa de tranzacție este setată la Cheltuieli și tipul de tranzacție este Costul.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Depanarea ratelor de cost pe costurile reale pentru cheltuieli

Mergeți la intrarea pentru cheltuieli conexă și asigurați-vă că există o valoare în câmpul de intrare pentru cheltuieli. Dacă intrarea de cheltuieli inițială nu avea câmpul sumă completat, atunci ați izolat problema.
 
Pentru a rezolva această problemă, recreați intrarea cheltuieli cu o valoare validă și aprobați-o.
