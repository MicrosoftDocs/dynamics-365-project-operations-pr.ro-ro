---
title: Prezentare generală a recunoașterii veniturilor
description: Acest subiect furnizează informații despre recunoașterea veniturilor în Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013771"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="69009-103">Prezentare generală a recunoașterii veniturilor</span><span class="sxs-lookup"><span data-stu-id="69009-103">Revenue recognition overview</span></span>

<span data-ttu-id="69009-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="69009-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="69009-105">În Dynamics 365 Project Operations, principiile de recunoaștere a veniturilor variază în funcție de metoda de facturare selectată pentru un proiect sau porțiune din proiect.</span><span class="sxs-lookup"><span data-stu-id="69009-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="69009-106">Acest subiect furnizează informații despre recunoașterea veniturilor în Project Operations.</span><span class="sxs-lookup"><span data-stu-id="69009-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="69009-107">Tranzacțiile contabilizate utilizând metoda de facturare de materiale și timp</span><span class="sxs-lookup"><span data-stu-id="69009-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="69009-108">Recunoașterea costurilor și a veniturilor sunt conectate.</span><span class="sxs-lookup"><span data-stu-id="69009-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="69009-109">Costul tranzacției și vânzările nefacturate sunt înregistrate utilizând [Jurnal de integrare a Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="69009-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="69009-110">Costul proiectului și profilul de venituri determină dacă tranzacțiile de vânzare nefacturate sunt înregistrate în registrul general.</span><span class="sxs-lookup"><span data-stu-id="69009-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="69009-111">Dacă este selectat **Acumulați venituri**, sistemul utilizează **Valoarea vânzărilor WIP** și conturi **Valoarea vânzărilor din venituri acumulate** în timpul postării.</span><span class="sxs-lookup"><span data-stu-id="69009-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="69009-112">În continuare este prezentat un exemplu al acestei metode.</span><span class="sxs-lookup"><span data-stu-id="69009-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="69009-113">Tip de tranzacție</span><span class="sxs-lookup"><span data-stu-id="69009-113">Transaction type</span></span> | <span data-ttu-id="69009-114">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="69009-114">Debit/Credit</span></span> | <span data-ttu-id="69009-115">Sumă</span><span class="sxs-lookup"><span data-stu-id="69009-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="69009-116">WIP valoarea Vânzărilor</span><span class="sxs-lookup"><span data-stu-id="69009-116">WIP Sales value</span></span> | <span data-ttu-id="69009-117">Debit</span><span class="sxs-lookup"><span data-stu-id="69009-117">Debit</span></span> | <span data-ttu-id="69009-118">100</span><span class="sxs-lookup"><span data-stu-id="69009-118">100</span></span> |
  | <span data-ttu-id="69009-119">Venit acumulat valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="69009-119">Accrued revenue sales value</span></span> | <span data-ttu-id="69009-120">Credit</span><span class="sxs-lookup"><span data-stu-id="69009-120">Credit</span></span> | <span data-ttu-id="69009-121">100</span><span class="sxs-lookup"><span data-stu-id="69009-121">100</span></span> |

- <span data-ttu-id="69009-122">Veniturile sunt recunoscute în timpul facturării.</span><span class="sxs-lookup"><span data-stu-id="69009-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="69009-123">Sistemul utilizează contul **Venituri facturate** în timpul publicării.</span><span class="sxs-lookup"><span data-stu-id="69009-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="69009-124">În continuare este prezentat un exemplu al acestei metode.</span><span class="sxs-lookup"><span data-stu-id="69009-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="69009-125">Tip de tranzacție</span><span class="sxs-lookup"><span data-stu-id="69009-125">Transaction type</span></span> | <span data-ttu-id="69009-126">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="69009-126">Debit/Credit</span></span> | <span data-ttu-id="69009-127">Sumă</span><span class="sxs-lookup"><span data-stu-id="69009-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="69009-128">Soldul clienților</span><span class="sxs-lookup"><span data-stu-id="69009-128">Customer balance</span></span> | <span data-ttu-id="69009-129">Debit</span><span class="sxs-lookup"><span data-stu-id="69009-129">Debit</span></span> | <span data-ttu-id="69009-130">120</span><span class="sxs-lookup"><span data-stu-id="69009-130">120</span></span> |
  | <span data-ttu-id="69009-131">Conturi impozit pe vânzări</span><span class="sxs-lookup"><span data-stu-id="69009-131">Sales tax payable</span></span> | <span data-ttu-id="69009-132">Credit</span><span class="sxs-lookup"><span data-stu-id="69009-132">Credit</span></span> | <span data-ttu-id="69009-133">20</span><span class="sxs-lookup"><span data-stu-id="69009-133">20</span></span> |
  | <span data-ttu-id="69009-134">Venit facturat</span><span class="sxs-lookup"><span data-stu-id="69009-134">Invoiced Revenue</span></span> | <span data-ttu-id="69009-135">Credit</span><span class="sxs-lookup"><span data-stu-id="69009-135">Credit</span></span> | <span data-ttu-id="69009-136">100</span><span class="sxs-lookup"><span data-stu-id="69009-136">100</span></span> |

- <span data-ttu-id="69009-137">În cazul în care veniturile au fost acumulate atunci când sunt înregistrate vânzările nefacturate, sistemul va inversa veniturile acumulate la facturare.</span><span class="sxs-lookup"><span data-stu-id="69009-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="69009-138">Tip de tranzacție</span><span class="sxs-lookup"><span data-stu-id="69009-138">Transaction type</span></span> | <span data-ttu-id="69009-139">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="69009-139">Debit/Credit</span></span> | <span data-ttu-id="69009-140">Sumă</span><span class="sxs-lookup"><span data-stu-id="69009-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="69009-141">WIP valoarea Vânzărilor</span><span class="sxs-lookup"><span data-stu-id="69009-141">WIP Sales value</span></span> | <span data-ttu-id="69009-142">Credit</span><span class="sxs-lookup"><span data-stu-id="69009-142">Credit</span></span> | <span data-ttu-id="69009-143">100</span><span class="sxs-lookup"><span data-stu-id="69009-143">100</span></span> |
  | <span data-ttu-id="69009-144">Venit acumulat valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="69009-144">Accrued revenue sales value</span></span> | <span data-ttu-id="69009-145">Debit</span><span class="sxs-lookup"><span data-stu-id="69009-145">Debit</span></span> | <span data-ttu-id="69009-146">100</span><span class="sxs-lookup"><span data-stu-id="69009-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="69009-147">Tranzacțiile contabilizate utilizând metoda de facturare de preț fix</span><span class="sxs-lookup"><span data-stu-id="69009-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="69009-148">Recunoașterea costurilor și a veniturilor sunt separate.</span><span class="sxs-lookup"><span data-stu-id="69009-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="69009-149">Costul tranzacției nefacturate este înregistrat utilizând [Jurnal de integrare a Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="69009-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="69009-150">Tranzacțiile de vânzare necotificate nu sunt create.</span><span class="sxs-lookup"><span data-stu-id="69009-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="69009-151">Veniturile pot fi recunoscute în timpul facturării dacă costul proiectului și profilul de venituri au **Principiul utilizat pentru calculele de finalizare a proiectului** setat la **Fără WIP**.</span><span class="sxs-lookup"><span data-stu-id="69009-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="69009-152">Folosiți această metodă doar pentru proiecte simple pe termen scurt.</span><span class="sxs-lookup"><span data-stu-id="69009-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="69009-153">Veniturile pot fi recunoscute utilizând estimări ale veniturilor la preț fix, fie cu **Contract finalizat** sau metoda **Recunoașterea veniturilor realizate în procente**.</span><span class="sxs-lookup"><span data-stu-id="69009-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69009-154">Resurse suplimentare</span><span class="sxs-lookup"><span data-stu-id="69009-154">Additional resources</span></span>
[<span data-ttu-id="69009-155">Configurarea contabilității pentru articolul de proiecte facturabile</span><span class="sxs-lookup"><span data-stu-id="69009-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="69009-156">Proiecte cu estimarea veniturilor cu preț fix</span><span class="sxs-lookup"><span data-stu-id="69009-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="69009-157">Gestionarea estimărilor de venituri</span><span class="sxs-lookup"><span data-stu-id="69009-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="69009-158">Metode pentru costul de finalizare</span><span class="sxs-lookup"><span data-stu-id="69009-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]