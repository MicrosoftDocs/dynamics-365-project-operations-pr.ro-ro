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
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="49bb6-103">Analiza ofertelor de proiect</span><span class="sxs-lookup"><span data-stu-id="49bb6-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="49bb6-104">Dynamics 365 Project Service Automation analizează ofertele de proiect pentru estimarea profitabilității.</span><span class="sxs-lookup"><span data-stu-id="49bb6-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="49bb6-105">De asemenea, analizează cât de bine este aliniată oferta la așteptările clienților despre data de livrare sau data finalizării și despre buget.</span><span class="sxs-lookup"><span data-stu-id="49bb6-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="49bb6-106">Analiza de profitabilitate</span><span class="sxs-lookup"><span data-stu-id="49bb6-106">Profitability analysis</span></span>

<span data-ttu-id="49bb6-107">Project Service Automation analizează profitabilitatea prin utilizarea marjei brute și a marjei brute ajustate.</span><span class="sxs-lookup"><span data-stu-id="49bb6-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="49bb6-108">Marjele brute se calculează utilizând următoarea formulă:</span><span class="sxs-lookup"><span data-stu-id="49bb6-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="49bb6-109">Marja brută ajustată se calculează utilizând următoarea formulă:</span><span class="sxs-lookup"><span data-stu-id="49bb6-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="49bb6-110">În cazul în care valorile pentru marja brută și marja brută ajustată diferă cu o marjă largă, o mare parte din activitatea din ofertă este clasificată ca netarifabilă.</span><span class="sxs-lookup"><span data-stu-id="49bb6-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="49bb6-111">Analiza așteptărilor clientului</span><span class="sxs-lookup"><span data-stu-id="49bb6-111">Analysis of customer expectations</span></span>

<span data-ttu-id="49bb6-112">Aveți posibilitatea să analizați ofertele și să generați diagrame pentru așteptările clienților despre planificare și buget dacă introduceți valori pentru următoarele câmpuri:</span><span class="sxs-lookup"><span data-stu-id="49bb6-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="49bb6-113">Câmpul **Dată solicitată pentru livrare** din antetul ofertei.</span><span class="sxs-lookup"><span data-stu-id="49bb6-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="49bb6-114">Câmpul **Buget client** pentru fiecare linie de ofertă (pentru linii bazate pe proiect și linii bazate pe produse).</span><span class="sxs-lookup"><span data-stu-id="49bb6-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="49bb6-115">Analiza așteptărilor clienților cu privire la planificare se face comparând cea mai recentă dată de încheiere a detaliilor liniei de ofertă cu data de livrare solicitată în toate liniile de ofertă din ofertă.</span><span class="sxs-lookup"><span data-stu-id="49bb6-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="49bb6-116">Analiza așteptărilor clienților cu privire la buget se face prin compararea sumei bugetului total al clienților cu valoarea ofertată în toate liniile de ofertă.</span><span class="sxs-lookup"><span data-stu-id="49bb6-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
