---
title: Configurați fluxuri de lucru pentru gestionarea cheltuielilor
description: Puteți configura un proces de flux de lucru care este utilizat pentru a revizui și aproba documentele de călătorie și cheltuieli.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896566"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="96d00-103">Configurați fluxuri de lucru pentru gestionarea cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="96d00-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="96d00-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="96d00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="96d00-105">Puteți configura un proces de flux de lucru pentru a revizui și aproba documentele de călătorie și cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="96d00-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="96d00-106">Puteți defini fluxuri de lucru pentru rapoarte de cheltuieli, cereri de călătorie și cereri de avans în numerar.</span><span class="sxs-lookup"><span data-stu-id="96d00-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="96d00-107">Un flux de lucru reprezintă un proces de afaceri și definește modul în care un document circulă prin sistem.</span><span class="sxs-lookup"><span data-stu-id="96d00-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="96d00-108">Fluxul de lucru indică, de asemenea, cine trebuie să finalizeze o sarcină sau să aprobe un document.</span><span class="sxs-lookup"><span data-stu-id="96d00-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="96d00-109">Există mai multe avantaje ale utilizării sistemului de flux de lucru în organizația dvs.:</span><span class="sxs-lookup"><span data-stu-id="96d00-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="96d00-110">**Procese consistente**: Puteți defini procesul de aprobare pentru documente specifice, cum ar fi cereri de achiziții și rapoarte de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="96d00-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="96d00-111">Utilizarea sistemului de flux de lucru vă asigură că documentele sunt procesate și aprobate într-un mod consecvent și eficient.</span><span class="sxs-lookup"><span data-stu-id="96d00-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="96d00-112">**Vizibilitatea procesului**: Puteți urmări statutul, istoricul și valorile de performanță ale unei instanțe specifice de flux de lucru.</span><span class="sxs-lookup"><span data-stu-id="96d00-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="96d00-113">Acest lucru vă ajută să determinați dacă ar trebui făcute modificări ale fluxului de lucru pentru a îmbunătăți eficiența.</span><span class="sxs-lookup"><span data-stu-id="96d00-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="96d00-114">**Lista de lucru centralizată**: utilizatorii pot vizualiza o listă de lucru centralizată pentru a vizualiza sarcinile fluxului de lucru și aprobările atribuite acestora.</span><span class="sxs-lookup"><span data-stu-id="96d00-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="96d00-115">Tipuri de flux de lucru</span><span class="sxs-lookup"><span data-stu-id="96d00-115">Workflow types</span></span>

<span data-ttu-id="96d00-116">Următorul tabel listează tipurile de fluxuri de lucru în care puteți crea **Managementul cheltuielilor**.</span><span class="sxs-lookup"><span data-stu-id="96d00-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="96d00-117"><strong>Tip</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="96d00-118"><strong>Utilizați acest tip pentru</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="96d00-119"><strong>Auto aprobarea raportului de cheltuieli</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="96d00-120">Creați fluxuri de lucru de aprobare pentru rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="96d00-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="96d00-121"><strong>Publicarea automată a rapoartelor de cheltuieli</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="96d00-122">Creați fluxuri de lucru automate de publicare pentru rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="96d00-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="96d00-123"><strong>Element de linie de cheltuială</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="96d00-124">Creați fluxuri de lucru de aprobare pentru elemente de linie pe rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="96d00-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="96d00-125"><strong>Publicare automată de element de cheltuială de linie</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="96d00-126">Creați fluxuri de lucru de publicare automată pentru elemente de linie pe rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="96d00-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="96d00-127"><strong>Cerere de călătorie</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="96d00-128">Creați fluxuri de lucru de aprobare pentru cererile de călătorie.</span><span class="sxs-lookup"><span data-stu-id="96d00-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="96d00-129"><strong>Solicitare de avans în numerar</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="96d00-130">Creați fluxuri de lucru de aprobare pentru solicitări de avans în numerar.</span><span class="sxs-lookup"><span data-stu-id="96d00-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="96d00-131"><strong>Recuperarea impozitului TVA</strong></span><span class="sxs-lookup"><span data-stu-id="96d00-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="96d00-132">Creați fluxuri de lucru de aprobare pentru recuperarea taxei pe valoarea adăugată (TVA).</span><span class="sxs-lookup"><span data-stu-id="96d00-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
