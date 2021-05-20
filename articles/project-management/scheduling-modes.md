---
title: Moduri de planificare
description: Acest subiect oferă informații despre moduri de planificare.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981450"
---
# <a name="scheduling-modes"></a><span data-ttu-id="6bda0-103">Moduri de planificare</span><span class="sxs-lookup"><span data-stu-id="6bda0-103">Scheduling modes</span></span>

<span data-ttu-id="6bda0-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="6bda0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6bda0-105">Dynamics 365 Project Operations oferă capacitatea organizațiilor de a defini modul în care gestionează modificările variabilelor cheie în sarcinile din cadrul structurii detaliate a proiectului.</span><span class="sxs-lookup"><span data-stu-id="6bda0-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="6bda0-106">Pe baza nevoilor specifice de organizație, managerii de proiect pot aduce modificări modului de planificare atunci când este creat un proiect.</span><span class="sxs-lookup"><span data-stu-id="6bda0-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="6bda0-107">Există trei moduri de planificare disponibile în Project Operations:</span><span class="sxs-lookup"><span data-stu-id="6bda0-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="6bda0-108">Durată fixă (acesta este modul implicit)</span><span class="sxs-lookup"><span data-stu-id="6bda0-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="6bda0-109">Lucru fix</span><span class="sxs-lookup"><span data-stu-id="6bda0-109">Fixed work</span></span>
  - <span data-ttu-id="6bda0-110">Unități fixe</span><span class="sxs-lookup"><span data-stu-id="6bda0-110">Fixed units</span></span>

<span data-ttu-id="6bda0-111">Valorile afectate de definiția unui mod de planificare specific sunt determinate de următoarea formulă:</span><span class="sxs-lookup"><span data-stu-id="6bda0-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="6bda0-112">Efort (*Muncă*) = Durată x Unități</span><span class="sxs-lookup"><span data-stu-id="6bda0-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="6bda0-113">Când definiți modul de planificare al unui proiect, setați una dintre aceste valori, care apoi nu poate fi modificată.</span><span class="sxs-lookup"><span data-stu-id="6bda0-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="6bda0-114">Păstrarea acestei valori ca constantă acordă o prioritate acelei valori, care notifică sistemul astfel încât să nu o modifice atunci când se schimbă celelalte două valori.</span><span class="sxs-lookup"><span data-stu-id="6bda0-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="6bda0-115">Tabelul următor oferă informații despre impactul selectării unui mod specific.</span><span class="sxs-lookup"><span data-stu-id="6bda0-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="6bda0-116">**În această sarcină**</span><span class="sxs-lookup"><span data-stu-id="6bda0-116">**In this task**</span></span>             | <span data-ttu-id="6bda0-117">**Dacă revizuiți unitățile**</span><span class="sxs-lookup"><span data-stu-id="6bda0-117">**If you revise units**</span></span>   | <span data-ttu-id="6bda0-118">**Dacă revizuiți durata**</span><span class="sxs-lookup"><span data-stu-id="6bda0-118">**If you revise duration**</span></span> | <span data-ttu-id="6bda0-119">**Dacă revizuiți efortul**</span><span class="sxs-lookup"><span data-stu-id="6bda0-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="6bda0-120">Unități fixe de sarcină</span><span class="sxs-lookup"><span data-stu-id="6bda0-120">Fixed units task</span></span>     | <span data-ttu-id="6bda0-121">Durata este recalculată.</span><span class="sxs-lookup"><span data-stu-id="6bda0-121">Duration is recalculated.</span></span> | <span data-ttu-id="6bda0-122">Efortul este recalculat.</span><span class="sxs-lookup"><span data-stu-id="6bda0-122">Effort is recalculated.</span></span>    | <span data-ttu-id="6bda0-123">Durata este recalculată.</span><span class="sxs-lookup"><span data-stu-id="6bda0-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="6bda0-124">Efort fix de sarcină</span><span class="sxs-lookup"><span data-stu-id="6bda0-124">Fixed effort task</span></span>    | <span data-ttu-id="6bda0-125">Durata este recalculată.</span><span class="sxs-lookup"><span data-stu-id="6bda0-125">Duration is recalculated.</span></span> | <span data-ttu-id="6bda0-126">Unitățile sunt recalculate.</span><span class="sxs-lookup"><span data-stu-id="6bda0-126">Units are recalculated.</span></span>    | <span data-ttu-id="6bda0-127">Durata este recalculată.</span><span class="sxs-lookup"><span data-stu-id="6bda0-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="6bda0-128">Durată fixă de sarcină</span><span class="sxs-lookup"><span data-stu-id="6bda0-128">Fixed duration task</span></span>  | <span data-ttu-id="6bda0-129">Efortul este recalculat.</span><span class="sxs-lookup"><span data-stu-id="6bda0-129">Effort is recalculated.</span></span>   | <span data-ttu-id="6bda0-130">Efortul este recalculat.</span><span class="sxs-lookup"><span data-stu-id="6bda0-130">Effort is recalculated.</span></span>    | <span data-ttu-id="6bda0-131">Unitățile sunt recalculate.</span><span class="sxs-lookup"><span data-stu-id="6bda0-131">Units are recalculated.</span></span>   |

<span data-ttu-id="6bda0-132">Pentru mai multe informații privind implicațiile unui mod dat, consultați [Schimbați tipul de activitate pentru o planificare mai precisă](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="6bda0-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="6bda0-133">În subiect, termenul **Muncă** este folosit în loc de **Efort**.</span><span class="sxs-lookup"><span data-stu-id="6bda0-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="6bda0-134">Schimbați modul de planificare al organizației</span><span class="sxs-lookup"><span data-stu-id="6bda0-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="6bda0-135">Parcurgeți următorii pași pentru a defini modul de planificare al unei organizații.</span><span class="sxs-lookup"><span data-stu-id="6bda0-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="6bda0-136">Accesați **Setări** \> **General** \> **Parametrii**, apoi selectați parametrul proiectului.</span><span class="sxs-lookup"><span data-stu-id="6bda0-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="6bda0-137">Pe pagina **Parametrii proiectului**, selectați modul de planificare implicit pentru organizație, apoi definiți capacitatea managerului de proiect de a suprascrie setarea atunci când creați un proiect nou.</span><span class="sxs-lookup"><span data-stu-id="6bda0-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="6bda0-138">Modificați setarea modului de planificare pentru un proiect</span><span class="sxs-lookup"><span data-stu-id="6bda0-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="6bda0-139">Dacă o organizație permite managerului de proiect să suprascrie modul de planificare implicit, managerul de proiect poate face această modificare atunci când creează un proiect nou.</span><span class="sxs-lookup"><span data-stu-id="6bda0-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="6bda0-140">Cu toate acestea, după ce proiectul a fost salvat, modul de planificare nu poate fi schimbat.</span><span class="sxs-lookup"><span data-stu-id="6bda0-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="6bda0-141">Proiecte copiate</span><span class="sxs-lookup"><span data-stu-id="6bda0-141">Copied projects</span></span>

<span data-ttu-id="6bda0-142">Deoarece un proiect este creat atunci când se ia acțiunea de copiere a acelui proiect, managerul de proiect nu poate seta modul de planificare.</span><span class="sxs-lookup"><span data-stu-id="6bda0-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="6bda0-143">Proiectul de destinație va fi implicit întotdeauna la modul definit la nivel organizațional.</span><span class="sxs-lookup"><span data-stu-id="6bda0-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="6bda0-144">Sarcini copiate</span><span class="sxs-lookup"><span data-stu-id="6bda0-144">Copied tasks</span></span>

<span data-ttu-id="6bda0-145">Când este copiată o sarcină de la un proiect la altul, sarcina moștenește modul de planificare al proiectului de destinație.</span><span class="sxs-lookup"><span data-stu-id="6bda0-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
