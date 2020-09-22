---
title: Anularea intrărilor de timp și cheltuieli aprobate anterior
description: Acest subiect oferă informații despre cum să anulați o tranzacție de timp și cheltuieli de proiect aprobată anterior.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754660"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="ced28-103">Anularea intrărilor de timp sau cheltuieli aprobate anterior</span><span class="sxs-lookup"><span data-stu-id="ced28-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ced28-104">În cea mai recentă versiune de Dynamics 365 Project Service Automation, aprobatorii pot anula intrările de timp sau cheltuieli pe care le-au aprobat anterior.</span><span class="sxs-lookup"><span data-stu-id="ced28-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="ced28-105">Anularea unei intrări de timp sau cheltuieli aprobată anterior</span><span class="sxs-lookup"><span data-stu-id="ced28-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="ced28-106">Urmați acești pași pentru a anula o intrare de timp sau cheltuieli aprobată anterior de dvs.</span><span class="sxs-lookup"><span data-stu-id="ced28-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="ced28-107">Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.</span><span class="sxs-lookup"><span data-stu-id="ced28-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="ced28-108">Pe pagina cu lista **Aprobări**, modificați vizualizarea la **Aprobările mele anterioare**.</span><span class="sxs-lookup"><span data-stu-id="ced28-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="ced28-109">Este afișată o listă a intrărilor de timp și cheltuieli pe care le-ați aprobat anterior.</span><span class="sxs-lookup"><span data-stu-id="ced28-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="ced28-110">Selectați una sau mai multe intrări, apoi selectați **Anulați aprobarea**.</span><span class="sxs-lookup"><span data-stu-id="ced28-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="ced28-111">Primiți un mesaj de avertizare.</span><span class="sxs-lookup"><span data-stu-id="ced28-111">You receive a warning message.</span></span>
4. <span data-ttu-id="ced28-112">Selectați **OK** pentru a anula aprobarea.</span><span class="sxs-lookup"><span data-stu-id="ced28-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="ced28-113">Înțelegeți impactul anularii unei aprobări de intrare de timp sau cheltuieli</span><span class="sxs-lookup"><span data-stu-id="ced28-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="ced28-114">Atunci când o aprobare este anulată, există atât un impact operațional, cât și un impact financiar.</span><span class="sxs-lookup"><span data-stu-id="ced28-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="ced28-115">Impactul operațional</span><span class="sxs-lookup"><span data-stu-id="ced28-115">Operational impact</span></span>

<span data-ttu-id="ced28-116">Pe partea de operațiuni, atunci când o aprobare este anulată, starea înregistrării este resetată **Schiță** și aprobarea nu mai apare în vizualizarea **Aprobările mele anterioare**.</span><span class="sxs-lookup"><span data-stu-id="ced28-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="ced28-117">În schimb, aprobarea anulată apare fie în vizualizarea **Intrări de timp pentru aprobare**, fie în vizualizarea **Intrări de cheltuieli pentru aprobare**, în funcție de dacă a fost o intrare de timp sau o intrare de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="ced28-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="ced28-118">În plus, starea intrării de timp sau de cheltuieli corelată este modificată la **Remisă**, astfel încât intrarea corelată este în concordanță cu aprobările care au o stare de **Schiță**.</span><span class="sxs-lookup"><span data-stu-id="ced28-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="ced28-119">Ca aprobator, aveți posibilitatea să editați unele dintre câmpurile unei aprobări care are starea **Schiță**.</span><span class="sxs-lookup"><span data-stu-id="ced28-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="ced28-120">Aceste câmpuri includ **Tip de facturare** și **Ore facturabile pentru intrările de timp**.</span><span class="sxs-lookup"><span data-stu-id="ced28-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="ced28-121">După ce efectuați modificări, aveți posibilitatea să aprobați din nou înregistrarea.</span><span class="sxs-lookup"><span data-stu-id="ced28-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="ced28-122">Alternativ, puteți respinge intrarea.</span><span class="sxs-lookup"><span data-stu-id="ced28-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="ced28-123">Dacă respingeți aprobarea unei intrări de timp, starea intrării se modifică la **Returnat**.</span><span class="sxs-lookup"><span data-stu-id="ced28-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="ced28-124">Dacă respingeți aprobarea unei intrări de cheltuieli, starea se modifică la **Returnat**.</span><span class="sxs-lookup"><span data-stu-id="ced28-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="ced28-125">Din punct de vedere funcțional, intrările returnate și respinse se comportă la fel ca o intrare care are starea **Schiță**.</span><span class="sxs-lookup"><span data-stu-id="ced28-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="ced28-126">Un membru al echipei de proiect poate face orice modificări necesare intrării și apoi remite intrarea pentru aprobare, sau poate șterge intrarea în întregime.</span><span class="sxs-lookup"><span data-stu-id="ced28-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="ced28-127">Impactul financiar</span><span class="sxs-lookup"><span data-stu-id="ced28-127">Financial impact</span></span>

<span data-ttu-id="ced28-128">Un proiect este, de asemenea, afectat financiar atunci când o aprobare este anulată.</span><span class="sxs-lookup"><span data-stu-id="ced28-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="ced28-129">Mai întâi, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:</span><span class="sxs-lookup"><span data-stu-id="ced28-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="ced28-130">Starea de ajustare este setată la **Ajustat**.</span><span class="sxs-lookup"><span data-stu-id="ced28-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="ced28-131">Starea de facturare este setată la **Anulat**.</span><span class="sxs-lookup"><span data-stu-id="ced28-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="ced28-132">Apoi, intrările de inversare sunt create în tabelul Valori reale.</span><span class="sxs-lookup"><span data-stu-id="ced28-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="ced28-133">Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale.</span><span class="sxs-lookup"><span data-stu-id="ced28-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="ced28-134">Singurele valori peste care nu se copiază sunt valorile cantitative.</span><span class="sxs-lookup"><span data-stu-id="ced28-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="ced28-135">Aceste valori sunt inversate în schimb.</span><span class="sxs-lookup"><span data-stu-id="ced28-135">These values are reversed instead.</span></span> <span data-ttu-id="ced28-136">Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**.</span><span class="sxs-lookup"><span data-stu-id="ced28-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="ced28-137">Câmpul **Stare ajustare** din valorile reale inversate este setat la **Neajustabil**, iar starea de facturare este setată la **Anulat**.</span><span class="sxs-lookup"><span data-stu-id="ced28-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="ced28-138">După efectuarea acestor modificări, suma înregistrată ca fiind cheltuită pe proiect și restanțele de venituri de pe proiect nu vor mai totaliza sumele pe care le reprezintă aceste date reale.</span><span class="sxs-lookup"><span data-stu-id="ced28-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
