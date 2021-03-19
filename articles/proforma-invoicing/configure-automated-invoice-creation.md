---
title: Configurarea creării automate a facturilor
description: Acest subiect oferă informații despre cum să configurați sistemul pentru a genera facturi automat.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0dddd963e79f8ecd91a96a6e684ab79e1b95bd6d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287928"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="8f91d-103">Configurarea creării automate a facturilor</span><span class="sxs-lookup"><span data-stu-id="8f91d-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="8f91d-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="8f91d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="8f91d-105">Finalizați pașii următori pentru a configura o rulare automată a facturilor în operațiunile proiectului Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8f91d-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="8f91d-106">Accesați **Setări** > **Operațiuni de lot**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="8f91d-107">Creați o operațiune de lot și denumiți-o **Project Operations creați facturi**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="8f91d-108">Numele operațiunii de lot trebuie să includă cuvintele „creare facturi”.</span><span class="sxs-lookup"><span data-stu-id="8f91d-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="8f91d-109">În câmpul **Tip lucrare**, selectați **Fără**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="8f91d-110">În mod implicit, opțiunile **Frecvența zilnică** și **Este activ** sunt setate la **Da**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="8f91d-111">Selectați **Rulați fluxul de lucru**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-111">Select **Run Workflow**.</span></span> <span data-ttu-id="8f91d-112">În caseta de dialog **Căutare înregistrare**, veți vedea trei fluxuri de lucru:</span><span class="sxs-lookup"><span data-stu-id="8f91d-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="8f91d-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="8f91d-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="8f91d-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="8f91d-114">ProcessRunner</span></span>
    - <span data-ttu-id="8f91d-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="8f91d-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="8f91d-116">Selectați **ProcessRunCaller**, apoi selectați **Adăugare**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="8f91d-117">În următoarea casetă de dialog, selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="8f91d-118">Un flux de lucru **Stare de repaus** este urmat de un fux de lucru **Proces**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="8f91d-119">De asemenea, puteți selecta **ProcessRunner** în pasul 5.</span><span class="sxs-lookup"><span data-stu-id="8f91d-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="8f91d-120">Apoi, când selectați **OK**, un flux de lucru **Proces** este urmat de un flux de lucru **Stare de repaus**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="8f91d-121">Fluxurile de lucru **ProcessRunCaller** și **ProcessRunner** creează facturi.</span><span class="sxs-lookup"><span data-stu-id="8f91d-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="8f91d-122">**ProcessRunCaller** apelează **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="8f91d-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="8f91d-123">**ProcessRunner** este fluxul de lucru care creează de fapt facturile.</span><span class="sxs-lookup"><span data-stu-id="8f91d-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="8f91d-124">Trece prin toate liniile de contract pentru care trebuie create facturile și creează facturi pentru acele linii.</span><span class="sxs-lookup"><span data-stu-id="8f91d-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="8f91d-125">Pentru a determina liniile de contract pentru care trebuie create facturile, lucrarea analizează datele de rulare a facturii pentru liniile de contract.</span><span class="sxs-lookup"><span data-stu-id="8f91d-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="8f91d-126">Dacă liniile de contract care aparțin unui contract au aceeași dată de rulare a facturii, tranzacțiile sunt combinate într-o singură factură care are două linii de factură.</span><span class="sxs-lookup"><span data-stu-id="8f91d-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="8f91d-127">Dacă nu există tranzacții pentru care să fie create facturi, lucrarea ignoră crearea facturii.</span><span class="sxs-lookup"><span data-stu-id="8f91d-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="8f91d-128">După ce **ProcessRunner** a terminat să ruleze, apelează **ProcessRunCaller**, oferă ora de sfârșit și este închis.</span><span class="sxs-lookup"><span data-stu-id="8f91d-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="8f91d-129">**ProcessRunCaller** pornește apoi un cronometru care rulează timp de 24 de ore de la ora de sfârșit specificată.</span><span class="sxs-lookup"><span data-stu-id="8f91d-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="8f91d-130">La sfârșitul cronometru, **ProcessRunCaller** este închis.</span><span class="sxs-lookup"><span data-stu-id="8f91d-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="8f91d-131">Lucrarea proces de lot pentru crearea facturilor este o lucrare recurentă.</span><span class="sxs-lookup"><span data-stu-id="8f91d-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="8f91d-132">Dacă acest proces de lot rulează de mai multe ori, sunt create mai multe instanțe ale lucrării și cauzează erori.</span><span class="sxs-lookup"><span data-stu-id="8f91d-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="8f91d-133">De aceea, ar trebui să porniți procesul de lot doar o singură dată și ar trebui să îl reporniți numai dacă se oprește rularea.</span><span class="sxs-lookup"><span data-stu-id="8f91d-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="8f91d-134">Facturarea în serie se execută numai pentru liniile de contract ale proiectului care sunt configurate de planurile de facturare.</span><span class="sxs-lookup"><span data-stu-id="8f91d-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="8f91d-135">O linie de contract cu o metodă de facturare a prețurilor fixe trebuie să aibă configurate repere.</span><span class="sxs-lookup"><span data-stu-id="8f91d-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="8f91d-136">O linie de contract de proiect cu o metodă de facturare a timpului și a materialului va avea nevoie de o planificare a facturilor pe bază de date.</span><span class="sxs-lookup"><span data-stu-id="8f91d-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="8f91d-137">Același lucru este valabil și pentru o linie de contract bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="8f91d-137">The same applies to a project-based contract line.</span></span>     


[!INCLUDE[footer-include](../includes/footer-banner.md)]