---
title: Fazele unui proiect
description: Acest subiect oferă informații despre etapele proiectului care sunt disponibile în Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897961"
---
# <a name="project-stages"></a><span data-ttu-id="e92ca-103">Fazele unui proiect</span><span class="sxs-lookup"><span data-stu-id="e92ca-103">Project stages</span></span>

<span data-ttu-id="e92ca-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="e92ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e92ca-105">Fazele de proiect sunt proiectate să reflecte starea proiectului pe măsură ce progresează.</span><span class="sxs-lookup"><span data-stu-id="e92ca-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="e92ca-106">Particularizările pot fi utilizate pentru a actualiza automat etapele cu fluxuri de proces de afaceri, Power Automate sau extensii de inserturi.</span><span class="sxs-lookup"><span data-stu-id="e92ca-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="e92ca-107">Următoarele etape sunt definite în fluxul de business implicit:</span><span class="sxs-lookup"><span data-stu-id="e92ca-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="e92ca-108">Noi</span><span class="sxs-lookup"><span data-stu-id="e92ca-108">New</span></span>
- <span data-ttu-id="e92ca-109">Ofertă</span><span class="sxs-lookup"><span data-stu-id="e92ca-109">Quote</span></span>
- <span data-ttu-id="e92ca-110">Plan</span><span class="sxs-lookup"><span data-stu-id="e92ca-110">Plan</span></span>
- <span data-ttu-id="e92ca-111">Livrare</span><span class="sxs-lookup"><span data-stu-id="e92ca-111">Deliver</span></span>
- <span data-ttu-id="e92ca-112">Terminată</span><span class="sxs-lookup"><span data-stu-id="e92ca-112">Complete</span></span>
- <span data-ttu-id="e92ca-113">Închideți</span><span class="sxs-lookup"><span data-stu-id="e92ca-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="e92ca-114">Noi</span><span class="sxs-lookup"><span data-stu-id="e92ca-114">New</span></span>

<span data-ttu-id="e92ca-115">Când creați un proiect, etapa de proiect este setată la **Nou**.</span><span class="sxs-lookup"><span data-stu-id="e92ca-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="e92ca-116">Dacă proiectul a fost creat dintr-un șablon, este posibil să aibă date de planificare, estimare și echipă.</span><span class="sxs-lookup"><span data-stu-id="e92ca-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="e92ca-117">În caz contrar, este o schiță a proiectului, iar componentele rămase trebuie să fie introduse.</span><span class="sxs-lookup"><span data-stu-id="e92ca-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="e92ca-118">Ofertă</span><span class="sxs-lookup"><span data-stu-id="e92ca-118">Quote</span></span>

<span data-ttu-id="e92ca-119">Când asociați un proiect cu o ofertă sau când creați un proiect de la o ofertă, faza proiectului este setată la **Ofertă** și datele de început și de sfârșit estimate sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="e92ca-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="e92ca-120">În timp ce proiectul este în etapa de **Ofertă**, fila **Vânzări** de pe pagina **Entitate de proiect** afișează detaliile ofertei.</span><span class="sxs-lookup"><span data-stu-id="e92ca-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="e92ca-121">Plan</span><span class="sxs-lookup"><span data-stu-id="e92ca-121">Plan</span></span>

<span data-ttu-id="e92ca-122">Atunci când câștigați o ofertă care este asociată cu un proiect și acesta este mutat la faza de **Contract**, etapa proiectului este actualizată la **Plan**.</span><span class="sxs-lookup"><span data-stu-id="e92ca-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="e92ca-123">În timp ce proiectul este în etapa de **Plan**, pagina **Entitate de proiect** afișează detaliile contractului.</span><span class="sxs-lookup"><span data-stu-id="e92ca-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="e92ca-124">Livrare</span><span class="sxs-lookup"><span data-stu-id="e92ca-124">Deliver</span></span>

<span data-ttu-id="e92ca-125">Când planul de proiect este finalizat și sunteți gata să porniți proiectul, managerul de proiect ar trebui să actualizeze faza proiectului la **Livrare** pentru a arăta că proiectul a început.</span><span class="sxs-lookup"><span data-stu-id="e92ca-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="e92ca-126">Finalizare</span><span class="sxs-lookup"><span data-stu-id="e92ca-126">Complete</span></span> 

<span data-ttu-id="e92ca-127">Când lucrarea pentru proiect este finalizată, managerul de proiect poate actualiza etapa la **Finalizare**.</span><span class="sxs-lookup"><span data-stu-id="e92ca-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="e92ca-128">Prin actualizarea etapei de proiect la **Finalizare**, managerul de proiect indică faptul că lucrarea este 100% finalizată, dar că proiectul este ținut deschis, astfel încât orice timp în așteptare sau intrările de cheltuieli să poată fi înregistrate.</span><span class="sxs-lookup"><span data-stu-id="e92ca-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="e92ca-129">Închidere</span><span class="sxs-lookup"><span data-stu-id="e92ca-129">Close</span></span>

<span data-ttu-id="e92ca-130">Când toate tranzacțiile sunt înregistrate pentru proiect, managerul de proiect poate actualiza etapa la **Închidere**.</span><span class="sxs-lookup"><span data-stu-id="e92ca-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="e92ca-131">În acel moment, nu pot fi înregistrate tranzacții, iar proiectul este setat la doar în citire.</span><span class="sxs-lookup"><span data-stu-id="e92ca-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

