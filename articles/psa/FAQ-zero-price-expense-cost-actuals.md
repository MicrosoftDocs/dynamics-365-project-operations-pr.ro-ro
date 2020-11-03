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
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="b010b-103">De ce prețul pentru cheltuielile reale revine la zero?</span><span class="sxs-lookup"><span data-stu-id="b010b-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b010b-104">Acest FAQ se aplică cheltuielilor efective în cazul în care clasa de tranzacție este setată la Cheltuieli și tipul de tranzacție este Costul.</span><span class="sxs-lookup"><span data-stu-id="b010b-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="b010b-105">Depanarea ratelor de cost pe costurile reale pentru cheltuieli</span><span class="sxs-lookup"><span data-stu-id="b010b-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="b010b-106">Mergeți la intrarea pentru cheltuieli conexă și asigurați-vă că există o valoare în câmpul de intrare pentru cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="b010b-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="b010b-107">Dacă intrarea de cheltuieli inițială nu avea câmpul sumă completat, atunci ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="b010b-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="b010b-108">Pentru a rezolva această problemă, recreați intrarea cheltuieli cu o valoare validă și aprobați-o.</span><span class="sxs-lookup"><span data-stu-id="b010b-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
