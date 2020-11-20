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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122133"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="a775a-103">De ce prețul pentru cheltuielile reale revine la zero?</span><span class="sxs-lookup"><span data-stu-id="a775a-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a775a-104">Acest FAQ se aplică cheltuielilor efective în cazul în care clasa de tranzacție este setată la Cheltuieli și tipul de tranzacție este Costul.</span><span class="sxs-lookup"><span data-stu-id="a775a-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="a775a-105">Depanarea ratelor de cost pe costurile reale pentru cheltuieli</span><span class="sxs-lookup"><span data-stu-id="a775a-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="a775a-106">Mergeți la intrarea pentru cheltuieli conexă și asigurați-vă că există o valoare în câmpul de intrare pentru cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="a775a-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="a775a-107">Dacă intrarea de cheltuieli inițială nu avea câmpul sumă completat, atunci ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="a775a-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="a775a-108">Pentru a rezolva această problemă, recreați intrarea cheltuieli cu o valoare validă și aprobați-o.</span><span class="sxs-lookup"><span data-stu-id="a775a-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
