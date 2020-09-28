---
title: Revizuiți jurnalul de așteptare de facturare pe proiecte și contracte de proiect
description: Acest subiect oferă informații despre cum se revizuiesc jurnalele de așteptare de timp, cheltuieli și produs și cum se marchează ca fiind pregătite pentru facturare.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754795"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="b501a-103">Revizuiți jurnalul de așteptare de facturare pe proiecte și contracte de proiect</span><span class="sxs-lookup"><span data-stu-id="b501a-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b501a-104">Când o tranzacție este gata pentru a avea o factură creată și procesată, tranzacția ar trebui să fie marcată ca **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="b501a-105">Acest subiect descrie tipurile de tranzacții care pot fi create.</span><span class="sxs-lookup"><span data-stu-id="b501a-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="b501a-106">Revizuiți jurnalele de așteptare de facturare timp și materiale</span><span class="sxs-lookup"><span data-stu-id="b501a-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="b501a-107">Atunci când o intrare de timp sau cheltuieli este remisă și aprobată pentru un proiect, PSA creează un proiect real.</span><span class="sxs-lookup"><span data-stu-id="b501a-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="b501a-108">În cazul în care combinația de proiect și clasa de tranzacții sunt mapate la o linie de contract pentru un proiect de timp și materiale, două date reale sunt create atunci când intrarea este aprobată:</span><span class="sxs-lookup"><span data-stu-id="b501a-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="b501a-109">Cost real</span><span class="sxs-lookup"><span data-stu-id="b501a-109">Cost actual</span></span> 
- <span data-ttu-id="b501a-110">Vânzări reale nefacturate</span><span class="sxs-lookup"><span data-stu-id="b501a-110">Unbilled sales actual</span></span>

<span data-ttu-id="b501a-111">Vânzările reale nefacturate reprezintă jurnalul de așteptare de facturare, iar starea lor de facturare trebuie setată la **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="b501a-112">Când se creează o factură proiect, vânzările reale nefacturate care sunt marcate **Gata de facturare** sunt copiate ca detalii de linie de facturare.</span><span class="sxs-lookup"><span data-stu-id="b501a-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="b501a-113">Pentru a revizui jurnalele de așteptare de facturare pentru timp și materiale, accesați **Vânzări** \> **Facturare** \> **Jurnale de așteptare de facturare timp și materiale**.</span><span class="sxs-lookup"><span data-stu-id="b501a-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="b501a-114">Selectați toate vânzările reale nefacturate care sunt pregătite pentru a fi facturate, apoi selectați **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="b501a-115">Starea de facturare a acestor date reale este modificată la **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Jurnale de așteptare de facturare timp și materiale](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="b501a-117">Vizualizați jurnalul de așteptare pentru facturarea produselor</span><span class="sxs-lookup"><span data-stu-id="b501a-117">Review the product billing backlog</span></span>

<span data-ttu-id="b501a-118">În PSA, atunci când un contract de proiect are linii de contract bazate pe produse, aceste linii sunt luate în calcul pentru facturare ori de câte ori se creează o factură pentru contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="b501a-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="b501a-119">Orice produs care are linii de contract marcate **gata de facturare** este copiat la factura de proiect ca linii de factură proiect.</span><span class="sxs-lookup"><span data-stu-id="b501a-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="b501a-120">Pentru a revizui jurnalele de așteptare facturare pentru produse, accesați **Vânzări** \> **Facturare** \> **Jurnal de așteptare facturare produs**.</span><span class="sxs-lookup"><span data-stu-id="b501a-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="b501a-121">Selectați toate liniile de contract pe bază de produs care sunt pregătite pentru a fi facturate, apoi selectați **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="b501a-122">Starea de facturare a acestor linii este modificată la **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Jurnal de așteptare pentru facturarea produselor](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="b501a-124">Revizuiți etapele de facturare pentru contractele cu preț fix</span><span class="sxs-lookup"><span data-stu-id="b501a-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="b501a-125">Fiecare linie de contract de proiect care are o metodă de facturare cu preț fix trebuie să definească etapele contractului.</span><span class="sxs-lookup"><span data-stu-id="b501a-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="b501a-126">Aceste repere ale contractului pot fi facturate numai dacă sunt marcate **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="b501a-127">Pentru a revizui etapele de facturare, accesați **Vânzări** \> **Facturare** \> **Repere preț fix**.</span><span class="sxs-lookup"><span data-stu-id="b501a-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="b501a-128">Selectați toate reperele care sunt pregătite pentru a fi facturate, apoi selectați **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="b501a-129">Starea de facturare a acestor repere este modificată la **Gata de facturare**.</span><span class="sxs-lookup"><span data-stu-id="b501a-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Repere cu preț fix](media/FPBacklog.png)