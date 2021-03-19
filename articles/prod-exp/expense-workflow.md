---
title: Flux de lucru pentru gestionarea cheltuielilor
description: Acest subiect explică modul în care puteți utiliza sistemul fluxului de lucru în Microsoft Dynamics 365 Finance, pentru a stabili un proces de revizuire a rapoartelor de cheltuieli în gestionarea cheltuielilor.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271683"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="059f5-103">Flux de lucru pentru gestionarea cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="059f5-103">Expense management workflow</span></span>

<span data-ttu-id="059f5-104">Puteți utiliza sistemul fluxului de lucru pentru a stabili un proces de revizuire a rapoartelor de cheltuieli în gestionarea cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="059f5-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="059f5-105">Puteți configura un flux de lucru care utilizează următoarele criterii pentru a determina cine aprobă rapoartele de cheltuieli:</span><span class="sxs-lookup"><span data-stu-id="059f5-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="059f5-106">Ierarhia raportării angajaților și limitele de aprobare predefinite</span><span class="sxs-lookup"><span data-stu-id="059f5-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="059f5-107">Aprobare pe mai multe niveluri care acceptă aprobatorii intermediari și un aprobator final</span><span class="sxs-lookup"><span data-stu-id="059f5-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="059f5-108">Dimensiunile financiare și responsabilitatea proiectului</span><span class="sxs-lookup"><span data-stu-id="059f5-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="059f5-109">Atribuirea pentru anumiți utilizatori sau grupuri de utilizatori</span><span class="sxs-lookup"><span data-stu-id="059f5-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="059f5-110">Aprobările fluxului de lucru pot fi create pentru rapoarte de cheltuieli, cereri de călătorie, avansuri de numerar și recuperarea taxei pe valoarea adăugată (TVA).</span><span class="sxs-lookup"><span data-stu-id="059f5-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="059f5-111">**Exemplu**</span><span class="sxs-lookup"><span data-stu-id="059f5-111">**Example**</span></span>

<span data-ttu-id="059f5-112">Următorul proces este un exemplu al fluxului de lucru de gestionare a cheltuielilor pentru un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="059f5-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="059f5-113">Un angajat creează și salvează un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="059f5-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="059f5-114">Angajatul transmite raportul de cheltuieli pentru aprobare.</span><span class="sxs-lookup"><span data-stu-id="059f5-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="059f5-115">Aprobatorul este identificat pe baza regulilor care au fost definite atunci când a fost configurat fluxul de lucru.</span><span class="sxs-lookup"><span data-stu-id="059f5-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="059f5-116">Aprobatorul primește o notificare că un raport de cheltuieli este pregătit pentru aprobare.</span><span class="sxs-lookup"><span data-stu-id="059f5-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="059f5-117">Aprobatorul examinează raportul de cheltuieli și verifică dacă sunt îndeplinite următoarele condiții:</span><span class="sxs-lookup"><span data-stu-id="059f5-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="059f5-118">Cheltuielile nu încalcă nicio politică de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="059f5-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="059f5-119">Dacă o cheltuială încalcă o politică, aprobatorul verifică dacă raportul de cheltuieli include o justificare validă pentru afaceri.</span><span class="sxs-lookup"><span data-stu-id="059f5-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="059f5-120">Chitanțele electronice sunt atașate la raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="059f5-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="059f5-121">Aprobatorul aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="059f5-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="059f5-122">Raportul de cheltuieli este atribuit coordonatorului de conturi de furnizori pentru postare.</span><span class="sxs-lookup"><span data-stu-id="059f5-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="059f5-123">Unul dintre pașii următori are loc, în funcție de configurarea de postare automată:</span><span class="sxs-lookup"><span data-stu-id="059f5-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="059f5-124">Dacă este configurată postarea automată, raportul de cheltuieli este procesat pentru plată, iar starea raportului de cheltuieli este actualizată.</span><span class="sxs-lookup"><span data-stu-id="059f5-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="059f5-125">Dacă postarea automată nu este configurată, coordonatorul conturilor de furnizori verifică dacă toate chitanțele originale au fost depuse și că chitanțele sunt aliniate cu cheltuielile din raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="059f5-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="059f5-126">Toate codurile fiscale care sunt introduse în raportul de cheltuieli trebuie, de asemenea, verificate pentru corectitudine.</span><span class="sxs-lookup"><span data-stu-id="059f5-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="059f5-127">După verificarea acestor cerințe, raportul de cheltuieli este postat.</span><span class="sxs-lookup"><span data-stu-id="059f5-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="059f5-128">După postarea raportului de cheltuieli, plata este autorizată pentru raportul de cheltuieli, iar angajatul este rambursat.</span><span class="sxs-lookup"><span data-stu-id="059f5-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]