---
title: Prezentare generală a utilizării resurselor
description: Acest subiect furnizează informații despre vizualizarea utilizării resurselor în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279333"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="45b74-103">Prezentare generală a utilizării resurselor</span><span class="sxs-lookup"><span data-stu-id="45b74-103">Resource utilization overview</span></span>

<span data-ttu-id="45b74-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="45b74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45b74-105">Resursele pot avea o utilizare facturabilă țintă.</span><span class="sxs-lookup"><span data-stu-id="45b74-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="45b74-106">Această utilizare țintă este definită ca un atribut al rolului implicit al unei resurse, fie setat pe înregistrarea resursei individuale care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="45b74-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="45b74-107">Calculele de utilizare se bazează pe orele efective pe care le-au raportat resursele utilizând intrările de timp aprobate.</span><span class="sxs-lookup"><span data-stu-id="45b74-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="45b74-108">Următoarele formule sunt utilizate pentru a calcula utilizarea:</span><span class="sxs-lookup"><span data-stu-id="45b74-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="45b74-109">Utilizare facturabilă = Ore efective taxabile ÷ Capacitate resursă.</span><span class="sxs-lookup"><span data-stu-id="45b74-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="45b74-110">Utilizare non-facturabilă = Timp real cu ID-ul de facturare = non-exigibil, Complementar sau Indisponibil ÷ capacitate resursă</span><span class="sxs-lookup"><span data-stu-id="45b74-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="45b74-111">Intern = Timp real fără contract de vânzare ÷ Capacitate resursă</span><span class="sxs-lookup"><span data-stu-id="45b74-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="45b74-112">Capacitate resursă = Ore de lucru resursă – Absent de la birou – zile nelucrătoare</span><span class="sxs-lookup"><span data-stu-id="45b74-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="45b74-113">Puteți găsi vizualizarea de **Utilizare resurse** în panoul **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="45b74-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="45b74-114">Fiecare celulă din grilă reprezintă procentul de utilizare facturabil al resursei într-o perioadă, cum ar fi o zi, o săptămână sau o lună.</span><span class="sxs-lookup"><span data-stu-id="45b74-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="45b74-115">Următoarele formule sunt utilizate pentru a colora celulele:</span><span class="sxs-lookup"><span data-stu-id="45b74-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="45b74-116">**Verde**: utilizare facturabilă >= utilizarea țintă a resursei</span><span class="sxs-lookup"><span data-stu-id="45b74-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="45b74-117">**Galben**: utilizare țintă – 20 <= utilizare facturabilă < utilizare țintă</span><span class="sxs-lookup"><span data-stu-id="45b74-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="45b74-118">**Roșu**: utilizare facturabilă < utilizare țintă – 20</span><span class="sxs-lookup"><span data-stu-id="45b74-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="45b74-119">Deoarece vizualizarea **Utilizare resurse** se bazează pe tabloul de planificare, aveți posibilitatea să utilizați capacitățile de filtrare ale tabloului de planificare pentru a filtra rezultatele.</span><span class="sxs-lookup"><span data-stu-id="45b74-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="45b74-120">Grila necesită să setați o utilizare țintă fie pe rol, fie pe resursa individuală.</span><span class="sxs-lookup"><span data-stu-id="45b74-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="45b74-121">Pentru a face această configurare, accesați **Resurse** > **Roluri resurse**.</span><span class="sxs-lookup"><span data-stu-id="45b74-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="45b74-122">În plus, un rol implicit trebuie să fie atribuit fiecărei resurse care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="45b74-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="45b74-123">Accesați **Resurse** > **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="45b74-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="45b74-124">În fila **Project Service**, verificați că este definit un rol de resursă și că câmpul **Este implicit** este setat la **Da**.</span><span class="sxs-lookup"><span data-stu-id="45b74-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="45b74-125">Aveți posibilitatea să adăugați roluri suplimentare acolo unde **Este implicit** = **Nu**.</span><span class="sxs-lookup"><span data-stu-id="45b74-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="45b74-126">Rolul unde **Este implicit** = **Da** este utilizat pentru a evalua utilizarea resursei față de obiectivul pentru rolul respectiv.</span><span class="sxs-lookup"><span data-stu-id="45b74-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="45b74-127">În fila **Project Service**, puteți seta, de asemenea, o utilizare țintă individuală pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="45b74-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="45b74-128">Calculul utilizării folosește apoi acea utilizare țintă pentru a evalua ținta resursei în locul țintei rolului implicit al resursei.</span><span class="sxs-lookup"><span data-stu-id="45b74-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="45b74-129">Utilizarea este afișată numai pentru o resursă numai în cazul în care resursa are aprobat timp facturabil în perioada afișată în grilă.</span><span class="sxs-lookup"><span data-stu-id="45b74-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]