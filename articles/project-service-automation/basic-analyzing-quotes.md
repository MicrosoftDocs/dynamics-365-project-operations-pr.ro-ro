---
title: Analiza ofertelor de proiect
description: Acest subiect oferă informații despre analiza ofertelor de proiect.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754687"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="0c979-103">Analiza ofertelor de proiect</span><span class="sxs-lookup"><span data-stu-id="0c979-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0c979-104">Dynamics 365 Project Service Automation analizează ofertele de proiect pentru estimarea profitabilității.</span><span class="sxs-lookup"><span data-stu-id="0c979-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="0c979-105">De asemenea, analizează cât de bine este aliniată oferta la așteptările clienților despre data de livrare sau data finalizării și despre buget.</span><span class="sxs-lookup"><span data-stu-id="0c979-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="0c979-106">Analiza de profitabilitate</span><span class="sxs-lookup"><span data-stu-id="0c979-106">Profitability analysis</span></span>

<span data-ttu-id="0c979-107">Project Service Automation analizează profitabilitatea prin utilizarea marjei brute și a marjei brute ajustate.</span><span class="sxs-lookup"><span data-stu-id="0c979-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="0c979-108">Marjele brute se calculează utilizând următoarea formulă:</span><span class="sxs-lookup"><span data-stu-id="0c979-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="0c979-109">Marja brută ajustată se calculează utilizând următoarea formulă:</span><span class="sxs-lookup"><span data-stu-id="0c979-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="0c979-110">În cazul în care valorile pentru marja brută și marja brută ajustată diferă cu o marjă largă, o mare parte din activitatea din ofertă este clasificată ca netarifabilă.</span><span class="sxs-lookup"><span data-stu-id="0c979-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="0c979-111">Analiza așteptărilor clientului</span><span class="sxs-lookup"><span data-stu-id="0c979-111">Analysis of customer expectations</span></span>

<span data-ttu-id="0c979-112">Aveți posibilitatea să analizați ofertele și să generați diagrame pentru așteptările clienților despre planificare și buget dacă introduceți valori pentru următoarele câmpuri:</span><span class="sxs-lookup"><span data-stu-id="0c979-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="0c979-113">Câmpul **Dată solicitată pentru livrare** din antetul ofertei.</span><span class="sxs-lookup"><span data-stu-id="0c979-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="0c979-114">Câmpul **Buget client** pentru fiecare linie de ofertă (pentru linii bazate pe proiect și linii bazate pe produse).</span><span class="sxs-lookup"><span data-stu-id="0c979-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="0c979-115">Analiza așteptărilor clienților cu privire la planificare se face comparând cea mai recentă dată de încheiere a detaliilor liniei de ofertă cu data de livrare solicitată în toate liniile de ofertă din ofertă.</span><span class="sxs-lookup"><span data-stu-id="0c979-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="0c979-116">Analiza așteptărilor clienților cu privire la buget se face prin compararea sumei bugetului total al clienților cu valoarea ofertată în toate liniile de ofertă.</span><span class="sxs-lookup"><span data-stu-id="0c979-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
