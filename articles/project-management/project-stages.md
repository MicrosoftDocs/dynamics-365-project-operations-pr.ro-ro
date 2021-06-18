---
title: Fazele unui proiect
description: Acest subiect oferă informații despre etapele proiectului care sunt disponibile în Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996941"
---
# <a name="project-stages"></a><span data-ttu-id="b6e2b-103">Fazele unui proiect</span><span class="sxs-lookup"><span data-stu-id="b6e2b-103">Project stages</span></span>

<span data-ttu-id="b6e2b-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="b6e2b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b6e2b-105">Fazele de proiect sunt proiectate să reflecte starea proiectului pe măsură ce progresează.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b6e2b-106">Particularizările pot fi utilizate pentru a actualiza automat etapele cu fluxuri de proces de afaceri, Power Automate sau extensii de inserturi.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="b6e2b-107">Următoarele etape sunt definite în fluxul de business implicit:</span><span class="sxs-lookup"><span data-stu-id="b6e2b-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="b6e2b-108">Noi</span><span class="sxs-lookup"><span data-stu-id="b6e2b-108">New</span></span>
- <span data-ttu-id="b6e2b-109">Ofertă</span><span class="sxs-lookup"><span data-stu-id="b6e2b-109">Quote</span></span>
- <span data-ttu-id="b6e2b-110">Plan</span><span class="sxs-lookup"><span data-stu-id="b6e2b-110">Plan</span></span>
- <span data-ttu-id="b6e2b-111">Livrare</span><span class="sxs-lookup"><span data-stu-id="b6e2b-111">Deliver</span></span>
- <span data-ttu-id="b6e2b-112">Terminată</span><span class="sxs-lookup"><span data-stu-id="b6e2b-112">Complete</span></span>
- <span data-ttu-id="b6e2b-113">Închideți</span><span class="sxs-lookup"><span data-stu-id="b6e2b-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b6e2b-114">Noi</span><span class="sxs-lookup"><span data-stu-id="b6e2b-114">New</span></span>

<span data-ttu-id="b6e2b-115">Când creați un proiect, etapa de proiect este setată la **Nou**.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b6e2b-116">Dacă proiectul a fost creat dintr-un șablon, este posibil să aibă date de planificare, estimare și echipă.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b6e2b-117">În caz contrar, este o schiță a proiectului, iar componentele rămase trebuie să fie introduse.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b6e2b-118">Ofertă</span><span class="sxs-lookup"><span data-stu-id="b6e2b-118">Quote</span></span>

<span data-ttu-id="b6e2b-119">Când asociați un proiect cu o ofertă sau când creați un proiect de la o ofertă, faza proiectului este setată la **Ofertă** și datele de început și de sfârșit estimate sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b6e2b-120">În timp ce proiectul este în etapa de **Ofertă**, fila **Vânzări** de pe pagina **Entitate de proiect** afișează detaliile ofertei.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b6e2b-121">Plan</span><span class="sxs-lookup"><span data-stu-id="b6e2b-121">Plan</span></span>

<span data-ttu-id="b6e2b-122">Atunci când câștigați o ofertă care este asociată cu un proiect și acesta este mutat la faza de **Contract**, etapa proiectului este actualizată la **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b6e2b-123">În timp ce proiectul este în etapa de **Plan**, pagina **Entitate de proiect** afișează detaliile contractului.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b6e2b-124">Livrare</span><span class="sxs-lookup"><span data-stu-id="b6e2b-124">Deliver</span></span>

<span data-ttu-id="b6e2b-125">Când planul de proiect este finalizat și sunteți gata să porniți proiectul, managerul de proiect ar trebui să actualizeze faza proiectului la **Livrare** pentru a arăta că proiectul a început.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b6e2b-126">Finalizare</span><span class="sxs-lookup"><span data-stu-id="b6e2b-126">Complete</span></span> 

<span data-ttu-id="b6e2b-127">Când lucrarea pentru proiect este finalizată, managerul de proiect poate actualiza etapa la **Finalizare**.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b6e2b-128">Prin actualizarea etapei de proiect la **Finalizare**, managerul de proiect indică faptul că lucrarea este 100% finalizată, dar că proiectul este ținut deschis, astfel încât orice timp în așteptare sau intrările de cheltuieli să poată fi înregistrate.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b6e2b-129">Închidere</span><span class="sxs-lookup"><span data-stu-id="b6e2b-129">Close</span></span>

<span data-ttu-id="b6e2b-130">Când toate tranzacțiile sunt înregistrate pentru proiect, managerul de proiect poate actualiza etapa la **Închidere**.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b6e2b-131">În acel moment, nu pot fi înregistrate tranzacții, iar proiectul este setat la doar în citire.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]