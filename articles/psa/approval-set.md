---
title: Seturi de aprobări
description: Acest subiect oferă informații despre setul de aprobări, cereri și subseturile acelor operațiuni.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116886"
---
# <a name="approval-sets"></a><span data-ttu-id="670d4-103">Seturi de aprobări</span><span class="sxs-lookup"><span data-stu-id="670d4-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="670d4-104">Aprobarea stabilește cererile de aprobare de grup împreună în subseturi mai mici de operațiuni.</span><span class="sxs-lookup"><span data-stu-id="670d4-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="670d4-105">Această grupare permite procesarea aprobărilor în ordine de către proiect și permite reîncercarea și secvențierea.</span><span class="sxs-lookup"><span data-stu-id="670d4-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="670d4-106">Gruparea îmbunătățește fiabilitatea și trasabilitatea procesării aprobărilor pentru volume mari de aprobări.</span><span class="sxs-lookup"><span data-stu-id="670d4-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="670d4-107">Seturile de aprobare indică starea generală de procesare a înregistrărilor lor conexe.</span><span class="sxs-lookup"><span data-stu-id="670d4-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="670d4-108">Când o înregistrare de aprobare este procesată utilizând un set de aprobare, înregistrarea se mută de la **Trimis** la **Aprobat** și este deconectat de la setul de aprobare.</span><span class="sxs-lookup"><span data-stu-id="670d4-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="670d4-109">Dacă o înregistrare eșuează atunci când este trimisă spre aprobare, înregistrarea rămâne în starea de **Trimis** iar setul de aprobare este marcat ca eșuat.</span><span class="sxs-lookup"><span data-stu-id="670d4-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="670d4-110">Setul de aprobare înregistrează mesajul de eroare al eșecului.</span><span class="sxs-lookup"><span data-stu-id="670d4-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="670d4-111">Procesarea aprobărilor și seturilor de aprobare</span><span class="sxs-lookup"><span data-stu-id="670d4-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="670d4-112">Aprobările aflate în coadă pentru procesare sunt vizibile în vizualizarea **Procesarea aprobărilor**.</span><span class="sxs-lookup"><span data-stu-id="670d4-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="670d4-113">Sistemul încearcă să proceseze toate intrările de mai multe ori asincron, inclusiv reîncercarea unei aprobări dacă încercările anterioare au eșuat.</span><span class="sxs-lookup"><span data-stu-id="670d4-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="670d4-114">Câmpul **Durata de viață a setului de aprobare** înregistrează numărul de încercări rămase de procesare a setului înainte ca acesta să fie marcat ca eșuat.</span><span class="sxs-lookup"><span data-stu-id="670d4-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="670d4-115">Aprobări eșuate și seturi de aprobare</span><span class="sxs-lookup"><span data-stu-id="670d4-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="670d4-116">Vizualizarea **Aprobări eșuate** listează toate aprobările care necesită intervenția utilizatorului.</span><span class="sxs-lookup"><span data-stu-id="670d4-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="670d4-117">Deschideți jurnalele de seturi de aprobare asociate pentru a identifica cauza eșecului.</span><span class="sxs-lookup"><span data-stu-id="670d4-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="670d4-118">Selectarea **Reîncercați** adaugă la numărul de durată de viață al setului de aprobare, mută setul de aprobare înapoi la o stare de **Procesare**, și încearcă să proceseze înregistrările rămase.</span><span class="sxs-lookup"><span data-stu-id="670d4-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="670d4-119">Configurați seturi de aprobare</span><span class="sxs-lookup"><span data-stu-id="670d4-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="670d4-120">Activați caracteristica Seturi de aprobare</span><span class="sxs-lookup"><span data-stu-id="670d4-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="670d4-121">Înainte de a activa funcția Seturi de aprobări, verificați dacă nu există aprobări în curs de procesare.</span><span class="sxs-lookup"><span data-stu-id="670d4-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="670d4-122">Accesați pagina **Parametrii proiectului** și selectați **Controlul caracteristicilor** > **Activați aprobările moderne**.</span><span class="sxs-lookup"><span data-stu-id="670d4-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="670d4-123">Dezactivați caracteristica Seturi de aprobare</span><span class="sxs-lookup"><span data-stu-id="670d4-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="670d4-124">Înainte de a dezactiva funcția Seturi de aprobări, verificați dacă nu există aprobări în curs de procesare.</span><span class="sxs-lookup"><span data-stu-id="670d4-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="670d4-125">Accesați pagina **Parametrii proiectului** și selectați **Controlul caracteristicilor** > **Dezactivați aprobările moderne**.</span><span class="sxs-lookup"><span data-stu-id="670d4-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="670d4-126">Configurarea pragului asincron</span><span class="sxs-lookup"><span data-stu-id="670d4-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="670d4-127">Când sunt create seturi de aprobare, procesarea se mută în fundal atunci când numărul selectat de înregistrări pentru aprobare depășește pragul indicat.</span><span class="sxs-lookup"><span data-stu-id="670d4-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="670d4-128">Utilizați câmpul **Prag asincron** pentru a configura când procesarea aprobării ar trebui să fie executată sincron sau asincron.</span><span class="sxs-lookup"><span data-stu-id="670d4-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="670d4-129">Valorile valide sunt:</span><span class="sxs-lookup"><span data-stu-id="670d4-129">Valid values are:</span></span>

  - <span data-ttu-id="670d4-130">Zero: toate solicitările ar trebui procesate asincron.</span><span class="sxs-lookup"><span data-stu-id="670d4-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="670d4-131">Numere mai mari decât zero: aprobările sunt procesate asincron numai atunci când numărul de aprobări trimise depășește această valoare.</span><span class="sxs-lookup"><span data-stu-id="670d4-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
