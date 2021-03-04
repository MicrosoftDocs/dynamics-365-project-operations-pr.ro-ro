---
title: Tipuri de etape de proiect
description: Acest subiect oferă informații despre etapele de proiect.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148118"
---
# <a name="project-stage-types"></a><span data-ttu-id="9678d-103">Tipuri de etape de proiect</span><span class="sxs-lookup"><span data-stu-id="9678d-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9678d-104">Fazele de proiect sunt proiectate să reflecte starea proiectului pe măsură ce progresează.</span><span class="sxs-lookup"><span data-stu-id="9678d-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="9678d-105">Particularizările pot fi utilizate pentru a actualiza automat etapele cu fluxuri de proces de afaceri, Power Automate sau extensii de inserturi.</span><span class="sxs-lookup"><span data-stu-id="9678d-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="9678d-106">Următoarele etape sunt definite în BPF implicit:</span><span class="sxs-lookup"><span data-stu-id="9678d-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="9678d-107">Noi</span><span class="sxs-lookup"><span data-stu-id="9678d-107">New</span></span>
- <span data-ttu-id="9678d-108">Ofertă</span><span class="sxs-lookup"><span data-stu-id="9678d-108">Quote</span></span>
- <span data-ttu-id="9678d-109">Plan</span><span class="sxs-lookup"><span data-stu-id="9678d-109">Plan</span></span>
- <span data-ttu-id="9678d-110">Livrare</span><span class="sxs-lookup"><span data-stu-id="9678d-110">Deliver</span></span>
- <span data-ttu-id="9678d-111">Finalizare</span><span class="sxs-lookup"><span data-stu-id="9678d-111">Complete</span></span>
- <span data-ttu-id="9678d-112">Închidere</span><span class="sxs-lookup"><span data-stu-id="9678d-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="9678d-113">Nou</span><span class="sxs-lookup"><span data-stu-id="9678d-113">New</span></span>

<span data-ttu-id="9678d-114">Când creați un proiect, etapa de proiect este setată la **Nou**.</span><span class="sxs-lookup"><span data-stu-id="9678d-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="9678d-115">Dacă proiectul a fost creat dintr-un șablon, este posibil să aibă date de planificare, estimare și echipă.</span><span class="sxs-lookup"><span data-stu-id="9678d-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="9678d-116">În caz contrar, este doar o schiță a proiectului, iar componentele rămase trebuie să fie introduse.</span><span class="sxs-lookup"><span data-stu-id="9678d-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="9678d-117">Ofertă</span><span class="sxs-lookup"><span data-stu-id="9678d-117">Quote</span></span>

<span data-ttu-id="9678d-118">Când asociați un proiect cu o ofertă sau când creați un proiect de la o ofertă, faza proiectului este setată la **Ofertă** și datele de început și de sfârșit estimate sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="9678d-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="9678d-119">În timp ce proiectul este în etapa de **Ofertă**, fila **Vânzări** de pe pagina **Entitate de proiect** afișează detaliile ofertei.</span><span class="sxs-lookup"><span data-stu-id="9678d-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="9678d-120">Plan</span><span class="sxs-lookup"><span data-stu-id="9678d-120">Plan</span></span>

<span data-ttu-id="9678d-121">Atunci când câștigați o ofertă care este asociată cu un proiect și acesta este mutat la faza de **Contract**, etapa proiectului este actualizată la **Plan**.</span><span class="sxs-lookup"><span data-stu-id="9678d-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="9678d-122">În timp ce proiectul este în etapa de **Plan**, pagina **Entitate de proiect** afișează detaliile contractului.</span><span class="sxs-lookup"><span data-stu-id="9678d-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="9678d-123">Livrare</span><span class="sxs-lookup"><span data-stu-id="9678d-123">Deliver</span></span>

<span data-ttu-id="9678d-124">Când planul de proiect este finalizat și sunteți gata să porniți proiectul, managerul de proiect ar trebui să actualizeze faza proiectului la **Livrare** pentru a arăta că proiectul a început.</span><span class="sxs-lookup"><span data-stu-id="9678d-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="9678d-125">Finalizare</span><span class="sxs-lookup"><span data-stu-id="9678d-125">Complete</span></span> 

<span data-ttu-id="9678d-126">Când lucrarea pentru proiect este finalizată, managerul de proiect poate actualiza etapa la **Finalizare**.</span><span class="sxs-lookup"><span data-stu-id="9678d-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="9678d-127">Prin actualizarea etapei de proiect la **Finalizare**, managerul de proiect indică faptul că lucrarea este 100% finalizată, dar că proiectul este ținut deschis, astfel încât orice timp în așteptare sau intrările de cheltuieli să poată fi înregistrate.</span><span class="sxs-lookup"><span data-stu-id="9678d-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="9678d-128">Închidere</span><span class="sxs-lookup"><span data-stu-id="9678d-128">Close</span></span>

<span data-ttu-id="9678d-129">Când toate tranzacțiile sunt înregistrate pentru proiect, managerul de proiect poate actualiza etapa la **Închidere**.</span><span class="sxs-lookup"><span data-stu-id="9678d-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="9678d-130">În acel moment, nu pot fi înregistrate tranzacții, iar proiectul este setat la doar în citire.</span><span class="sxs-lookup"><span data-stu-id="9678d-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
