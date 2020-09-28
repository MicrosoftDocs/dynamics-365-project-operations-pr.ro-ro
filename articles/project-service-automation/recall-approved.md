---
title: Retragerea înregistrărilor aprobate de timp sau cheltuieli
description: Acest subiect oferă informații despre cum să retrageți o operațiune de timp sau cheltuieli aprobată anterior.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754828"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="45406-103">Retragerea înregistrărilor aprobate de timp sau cheltuieli</span><span class="sxs-lookup"><span data-stu-id="45406-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="45406-104">Un membru al echipei de proiect sau o altă persoană care depune o înregistrare de timp sau cheltuială poate retrage acea înregistrare de timp sau cheltuială după ce a fost aprobată.</span><span class="sxs-lookup"><span data-stu-id="45406-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="45406-105">Procesul de retragere a unei înregistrări de timp sau cheltuieli aprobate are două etape:</span><span class="sxs-lookup"><span data-stu-id="45406-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="45406-106">Un depunător cere o retragere.</span><span class="sxs-lookup"><span data-stu-id="45406-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="45406-107">Un aprobator aprobă retragerea.</span><span class="sxs-lookup"><span data-stu-id="45406-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="45406-108">Solicitați o retragere</span><span class="sxs-lookup"><span data-stu-id="45406-108">Request a recall</span></span>

<span data-ttu-id="45406-109">Urmați acești pași pentru a solicita o retragere a unei înregistrări de timp sau cheltuieli aprobate.</span><span class="sxs-lookup"><span data-stu-id="45406-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="45406-110">Pentru înregistrările de timp, accesați **Proiecte**\> **Munca mea** \> **Înregistrare timp**.</span><span class="sxs-lookup"><span data-stu-id="45406-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="45406-111">-sau-</span><span class="sxs-lookup"><span data-stu-id="45406-111">–or–</span></span>

    <span data-ttu-id="45406-112">Pentru înregistrările de cheltuieli, accesați **Proiecte**\> **Munca mea** \> **Cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="45406-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="45406-113">Pentru înregistrările de timp, selectați toate înregistrările de timp pentru o anumită combinație a unui proiect și a unei activități.</span><span class="sxs-lookup"><span data-stu-id="45406-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="45406-114">Alternativ, în grilă, selectați celulele individuale pentru timp la o anumită dată pentru un anumit proiect.</span><span class="sxs-lookup"><span data-stu-id="45406-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="45406-115">-sau-</span><span class="sxs-lookup"><span data-stu-id="45406-115">–or–</span></span>

    <span data-ttu-id="45406-116">Pentru înregistrările de cheltuieli, selectați rândul pentru înregistrarea de cheltuieli de retras.</span><span class="sxs-lookup"><span data-stu-id="45406-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="45406-117">Selectați **Retragere**.</span><span class="sxs-lookup"><span data-stu-id="45406-117">Select **Recall**.</span></span> <span data-ttu-id="45406-118">Apare o casetă de dialog de confirmare.</span><span class="sxs-lookup"><span data-stu-id="45406-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="45406-119">Dacă înregistrările de timp și cheltuieli selectate au fost deja aprobate, vi se solicită să introduceți un motiv pentru retragere.</span><span class="sxs-lookup"><span data-stu-id="45406-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="45406-120">Introduceți un motiv pentru retragere apoi selectați **OK** pentru a confirma operațiunea.</span><span class="sxs-lookup"><span data-stu-id="45406-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="45406-121">Sistemul trimite persoanei care a aprobat înregistrările o cerere de aprobare a retragerii.</span><span class="sxs-lookup"><span data-stu-id="45406-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="45406-122">Deși înregistrările aprobate de timp și cheltuieli pot fi retrase dacă un timp sau o cheltuială aprobată a fost deja facturată clientului, nu se poate crea o solicitare de retragere.</span><span class="sxs-lookup"><span data-stu-id="45406-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="45406-123">Un utilizator care încearcă să creeze o solicitare de retragere va primi un mesaj care afirmă că timpul sau cheltuiala nu poate fi retras/ă, deoarece a fost deja facturat/ă.</span><span class="sxs-lookup"><span data-stu-id="45406-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="45406-124">Aprobarea sau respingerea unei solicitări de retragere</span><span class="sxs-lookup"><span data-stu-id="45406-124">Approve or reject a recall request</span></span>

<span data-ttu-id="45406-125">Urmați acești pași pentru a aproba sau respinge o solicitare de retragere.</span><span class="sxs-lookup"><span data-stu-id="45406-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="45406-126">Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.</span><span class="sxs-lookup"><span data-stu-id="45406-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="45406-127">Pe pagina cu lista **Aprobări**, modificați vizualizarea la **Cereri de retragere de aprobat**.</span><span class="sxs-lookup"><span data-stu-id="45406-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="45406-128">Este afișată o listă de solicitări de retragere trimise.</span><span class="sxs-lookup"><span data-stu-id="45406-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="45406-129">Selectați una sau mai multe înregistrări, apoi selectați fie **Aprobare**, fie **Respingere**.</span><span class="sxs-lookup"><span data-stu-id="45406-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="45406-130">Dacă ați selectat **Aprobare**, primiți un mesaj de avertizare care explică impactul aprobării.</span><span class="sxs-lookup"><span data-stu-id="45406-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="45406-131">Selectați **OK** pentru a confirma operațiunea.</span><span class="sxs-lookup"><span data-stu-id="45406-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="45406-132">Solicitarea de retragere este aprobată</span><span class="sxs-lookup"><span data-stu-id="45406-132">The recall request is approved.</span></span>

    <span data-ttu-id="45406-133">-sau-</span><span class="sxs-lookup"><span data-stu-id="45406-133">–or–</span></span>

    <span data-ttu-id="45406-134">Dacă ați selectat **Respingere**, solicitarea de retragere este respinsă.</span><span class="sxs-lookup"><span data-stu-id="45406-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="45406-135">Ca atunci când se solicită o retragere, atunci când o retragere este aprobată, sistemul verifică orice activitate de facturare pe înregistrările de timp sau cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="45406-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="45406-136">Dacă o înregistrare a fost deja facturată sau dacă este pe un proiect de factură, aprobatorul va primi un mesaj de eroare care spune că timpul sau cheltuiala nu pot fi aprobate pentru retragere, deoarece au fost deja facturate.</span><span class="sxs-lookup"><span data-stu-id="45406-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="45406-137">Impactul unei solicitări de retragere</span><span class="sxs-lookup"><span data-stu-id="45406-137">Impact of a recall request</span></span>

<span data-ttu-id="45406-138">Atunci când se retrage o aprobare, există atât un impact operațional, cât și un impact financiar.</span><span class="sxs-lookup"><span data-stu-id="45406-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="45406-139">Impactul operațional</span><span class="sxs-lookup"><span data-stu-id="45406-139">Operational impact</span></span>

<span data-ttu-id="45406-140">Dacă se aprobă o solicitare de retragere, înregistrarea de aprobare este marcată **Respinsă**.</span><span class="sxs-lookup"><span data-stu-id="45406-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="45406-141">Starea înregistrării se modifică fie în **Returnată**, fie în **Respinsă**, în funcție de faptul dacă este o înregistrare de timp sau o înregistrare de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="45406-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="45406-142">Membrul echipei de proiect poate vizualiza înregistrările, poate, edita și apoi remite înregistrările sau poate șterge înregistrările în întregime.</span><span class="sxs-lookup"><span data-stu-id="45406-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="45406-143">Dacă o solicitare de retragere este respinsă, starea înregistrării rămâne **Aprobată**, iar înregistrarea nu poate fi editată de membrul echipei de proiect sau de aprobatorul proiectului.</span><span class="sxs-lookup"><span data-stu-id="45406-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="45406-144">Impactul financiar</span><span class="sxs-lookup"><span data-stu-id="45406-144">Financial impact</span></span>

<span data-ttu-id="45406-145">Dacă se aprobă o solicitare de retragere, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:</span><span class="sxs-lookup"><span data-stu-id="45406-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="45406-146">Câmpul **Stare Ajustare** este actualizat la **Ajustat**.</span><span class="sxs-lookup"><span data-stu-id="45406-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="45406-147">Câmpul **Stare Facturare** este actualizat la **Anulat**.</span><span class="sxs-lookup"><span data-stu-id="45406-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="45406-148">Apoi, intrările de inversare sunt create în tabelul Valori reale.</span><span class="sxs-lookup"><span data-stu-id="45406-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="45406-149">Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale.</span><span class="sxs-lookup"><span data-stu-id="45406-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="45406-150">Singurele valori peste care nu se copiază sunt valorile cantitative.</span><span class="sxs-lookup"><span data-stu-id="45406-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="45406-151">Aceste valori sunt inversate în schimb.</span><span class="sxs-lookup"><span data-stu-id="45406-151">These values are reversed instead.</span></span> <span data-ttu-id="45406-152">Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**.</span><span class="sxs-lookup"><span data-stu-id="45406-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="45406-153">Câmpul **Stare Ajustare** de pe valorile reale inversate este setat la **Neajustabil**, iar câmpul **Stare Facturare** este setat la **Anulat.**</span><span class="sxs-lookup"><span data-stu-id="45406-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="45406-154">Din cauza acestor modificări, restanțele înregistrare de cheltuieli și venituri de pe proiect nu vor mai duce la pentru sumele pe care le reprezintă aceste date reale.</span><span class="sxs-lookup"><span data-stu-id="45406-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="45406-155">Dacă o cerere de retragere este respinsă, nu există niciun impact financiar asupra proiectului.</span><span class="sxs-lookup"><span data-stu-id="45406-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="45406-156">Modificări la înregistrări de intrări de timp</span><span class="sxs-lookup"><span data-stu-id="45406-156">Changes to time entry records</span></span>

<span data-ttu-id="45406-157">Următoarea ilustrație arată modificările care apar pentru înregistrările de timp aprobate atunci când sunt retrase.</span><span class="sxs-lookup"><span data-stu-id="45406-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Tranziții de stare Înregistrare timp](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="45406-159">Modificări la înregistrări de înregistrări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="45406-159">Changes to expense entry records</span></span>

<span data-ttu-id="45406-160">Următoarea ilustrație arată modificările care apar pentru înregistrările de cheltuieli aprobate atunci când sunt retrase.</span><span class="sxs-lookup"><span data-stu-id="45406-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Tranziții de stare Înregistrare cheltuieli](media/ExpenseEntryStateTransitions.png)