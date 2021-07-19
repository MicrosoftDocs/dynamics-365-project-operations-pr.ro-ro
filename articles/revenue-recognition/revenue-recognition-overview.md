---
title: Prezentare generală a recunoașterii veniturilor
description: Acest subiect furnizează informații despre recunoașterea veniturilor în Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368041"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="3656d-103">Prezentare generală a recunoașterii veniturilor</span><span class="sxs-lookup"><span data-stu-id="3656d-103">Revenue recognition overview</span></span>

<span data-ttu-id="3656d-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="3656d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3656d-105">În Dynamics 365 Project Operations, principiile de recunoaștere a veniturilor variază în funcție de metoda de facturare selectată pentru un proiect sau porțiune din proiect.</span><span class="sxs-lookup"><span data-stu-id="3656d-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="3656d-106">Acest subiect furnizează informații despre recunoașterea veniturilor în Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3656d-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="3656d-107">Tranzacțiile contabilizate utilizând metoda de facturare de materiale și timp</span><span class="sxs-lookup"><span data-stu-id="3656d-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="3656d-108">Recunoașterea costurilor și a veniturilor sunt conectate.</span><span class="sxs-lookup"><span data-stu-id="3656d-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="3656d-109">Costul tranzacției și vânzările nefacturate sunt înregistrate utilizând [Jurnal de integrare a Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="3656d-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="3656d-110">Costul proiectului și profilul de venituri determină dacă tranzacțiile de vânzare nefacturate sunt înregistrate în registrul general.</span><span class="sxs-lookup"><span data-stu-id="3656d-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="3656d-111">Dacă este selectat **Acumulați venituri**, sistemul utilizează **Valoarea vânzărilor WIP** și conturi **Valoarea vânzărilor din venituri acumulate** în timpul postării.</span><span class="sxs-lookup"><span data-stu-id="3656d-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="3656d-112">În continuare este prezentat un exemplu al acestei metode.</span><span class="sxs-lookup"><span data-stu-id="3656d-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="3656d-113">Tip de tranzacție</span><span class="sxs-lookup"><span data-stu-id="3656d-113">Transaction type</span></span> | <span data-ttu-id="3656d-114">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-114">Debit/Credit</span></span> | <span data-ttu-id="3656d-115">Sumă</span><span class="sxs-lookup"><span data-stu-id="3656d-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="3656d-116">WIP valoarea Vânzărilor</span><span class="sxs-lookup"><span data-stu-id="3656d-116">WIP Sales value</span></span> | <span data-ttu-id="3656d-117">Debit</span><span class="sxs-lookup"><span data-stu-id="3656d-117">Debit</span></span> | <span data-ttu-id="3656d-118">100</span><span class="sxs-lookup"><span data-stu-id="3656d-118">100</span></span> |
  | <span data-ttu-id="3656d-119">Venit acumulat valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="3656d-119">Accrued revenue sales value</span></span> | <span data-ttu-id="3656d-120">Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-120">Credit</span></span> | <span data-ttu-id="3656d-121">100</span><span class="sxs-lookup"><span data-stu-id="3656d-121">100</span></span> |

- <span data-ttu-id="3656d-122">Veniturile sunt recunoscute în timpul facturării.</span><span class="sxs-lookup"><span data-stu-id="3656d-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="3656d-123">Sistemul utilizează contul **Venituri facturate** în timpul publicării.</span><span class="sxs-lookup"><span data-stu-id="3656d-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="3656d-124">În continuare este prezentat un exemplu al acestei metode.</span><span class="sxs-lookup"><span data-stu-id="3656d-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="3656d-125">Tip de tranzacție</span><span class="sxs-lookup"><span data-stu-id="3656d-125">Transaction type</span></span> | <span data-ttu-id="3656d-126">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-126">Debit/Credit</span></span> | <span data-ttu-id="3656d-127">Sumă</span><span class="sxs-lookup"><span data-stu-id="3656d-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="3656d-128">Soldul clienților</span><span class="sxs-lookup"><span data-stu-id="3656d-128">Customer balance</span></span> | <span data-ttu-id="3656d-129">Debit</span><span class="sxs-lookup"><span data-stu-id="3656d-129">Debit</span></span> | <span data-ttu-id="3656d-130">120</span><span class="sxs-lookup"><span data-stu-id="3656d-130">120</span></span> |
  | <span data-ttu-id="3656d-131">Conturi impozit pe vânzări</span><span class="sxs-lookup"><span data-stu-id="3656d-131">Sales tax payable</span></span> | <span data-ttu-id="3656d-132">Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-132">Credit</span></span> | <span data-ttu-id="3656d-133">20</span><span class="sxs-lookup"><span data-stu-id="3656d-133">20</span></span> |
  | <span data-ttu-id="3656d-134">Venit facturat</span><span class="sxs-lookup"><span data-stu-id="3656d-134">Invoiced Revenue</span></span> | <span data-ttu-id="3656d-135">Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-135">Credit</span></span> | <span data-ttu-id="3656d-136">100</span><span class="sxs-lookup"><span data-stu-id="3656d-136">100</span></span> |

- <span data-ttu-id="3656d-137">În cazul în care veniturile au fost acumulate atunci când sunt înregistrate vânzările nefacturate, sistemul va inversa veniturile acumulate la facturare.</span><span class="sxs-lookup"><span data-stu-id="3656d-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="3656d-138">Tip de tranzacție</span><span class="sxs-lookup"><span data-stu-id="3656d-138">Transaction type</span></span> | <span data-ttu-id="3656d-139">Debit/Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-139">Debit/Credit</span></span> | <span data-ttu-id="3656d-140">Sumă</span><span class="sxs-lookup"><span data-stu-id="3656d-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="3656d-141">WIP valoarea Vânzărilor</span><span class="sxs-lookup"><span data-stu-id="3656d-141">WIP Sales value</span></span> | <span data-ttu-id="3656d-142">Credit</span><span class="sxs-lookup"><span data-stu-id="3656d-142">Credit</span></span> | <span data-ttu-id="3656d-143">100</span><span class="sxs-lookup"><span data-stu-id="3656d-143">100</span></span> |
  | <span data-ttu-id="3656d-144">Venit acumulat valoarea vânzărilor</span><span class="sxs-lookup"><span data-stu-id="3656d-144">Accrued revenue sales value</span></span> | <span data-ttu-id="3656d-145">Debit</span><span class="sxs-lookup"><span data-stu-id="3656d-145">Debit</span></span> | <span data-ttu-id="3656d-146">100</span><span class="sxs-lookup"><span data-stu-id="3656d-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="3656d-147">Tranzacțiile contabilizate utilizând metoda de facturare de preț fix</span><span class="sxs-lookup"><span data-stu-id="3656d-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="3656d-148">Recunoașterea costurilor și a veniturilor sunt separate.</span><span class="sxs-lookup"><span data-stu-id="3656d-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="3656d-149">Costul tranzacției nefacturate este înregistrat utilizând [Jurnal de integrare a Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="3656d-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="3656d-150">Tranzacțiile de vânzare necotificate nu sunt create.</span><span class="sxs-lookup"><span data-stu-id="3656d-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="3656d-151">Veniturile pot fi recunoscute în timpul facturării dacă costul proiectului și profilul de venituri au **Principiul utilizat pentru calculele de finalizare a proiectului** setat la **Fără WIP**.</span><span class="sxs-lookup"><span data-stu-id="3656d-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="3656d-152">Folosiți această metodă doar pentru proiecte simple pe termen scurt.</span><span class="sxs-lookup"><span data-stu-id="3656d-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="3656d-153">Veniturile pot fi recunoscute utilizând estimări ale veniturilor la preț fix, fie cu **Contract finalizat** sau metoda **Recunoașterea veniturilor realizate în procente**.</span><span class="sxs-lookup"><span data-stu-id="3656d-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3656d-154">Resurse suplimentare</span><span class="sxs-lookup"><span data-stu-id="3656d-154">Additional resources</span></span>
[<span data-ttu-id="3656d-155">Configurarea contabilității pentru articolul de proiecte facturabile</span><span class="sxs-lookup"><span data-stu-id="3656d-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="3656d-156">Proiecte cu estimarea veniturilor cu preț fix</span><span class="sxs-lookup"><span data-stu-id="3656d-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="3656d-157">Gestionarea estimărilor de venituri</span><span class="sxs-lookup"><span data-stu-id="3656d-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="3656d-158">Metode pentru costul de finalizare</span><span class="sxs-lookup"><span data-stu-id="3656d-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]