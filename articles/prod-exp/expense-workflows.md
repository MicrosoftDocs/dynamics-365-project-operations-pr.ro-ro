---
title: Configurați fluxuri de lucru de gestionare a cheltuielilor
description: Puteți configura un proces de flux de lucru pentru a revizui și aproba documentele de călătorie și cheltuieli.
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
ms.openlocfilehash: 36ab1edc4769013684fa9248e6c5eac025637bbd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271638"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="8e3f3-103">Configurați fluxuri de lucru de gestionare a cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="8e3f3-103">Set up Expense management workflows</span></span>

<span data-ttu-id="8e3f3-104">Puteți configura un proces de flux de lucru care este utilizat pentru a revizui și aproba documentele de călătorie și cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="8e3f3-105">Documentele pentru care pot fi definite fluxurile de lucru includ rapoarte de cheltuieli, cereri de călătorie și cereri de avans în numerar.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="8e3f3-106">Un flux de lucru reprezintă un proces de afaceri.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-106">A workflow represents a business process.</span></span> <span data-ttu-id="8e3f3-107">Acesta definește modul în care un document circulă prin sistem și indică cine trebuie să finalizeze o sarcină sau să aprobe un document.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8e3f3-108">Există mai multe avantaje ale utilizării sistemului de flux de lucru în organizația dvs.:</span><span class="sxs-lookup"><span data-stu-id="8e3f3-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="8e3f3-109">**Procese consistente** - Puteți defini procesul de aprobare pentru documente specifice, cum ar fi cereri de achiziții și rapoarte de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8e3f3-110">Utilizarea sistemului de flux de lucru vă asigură că documentele sunt procesate și aprobate într-un mod consecvent și eficient.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="8e3f3-111">Vizibilitatea procesului - Puteți urmări statutul, istoricul și valorile de performanță ale unei instanțe specifice de flux de lucru.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8e3f3-112">Acest lucru vă ajută să determinați dacă ar trebui făcute modificări ale fluxului de lucru pentru a îmbunătăți eficiența.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="8e3f3-113">Lista de lucru centralizată- Utilizatorii pot vizualiza o listă de lucru centralizată pentru a vizualiza sarcinile fluxului de lucru și aprobările atribuite acestora.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="8e3f3-114">**Tipurile de fluxuri de lucru pe care le puteți crea**</span><span class="sxs-lookup"><span data-stu-id="8e3f3-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="8e3f3-115">Următorul tabel listează tipurile de fluxuri de lucru în care puteți crea **Cheltuială**.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="8e3f3-116"><strong>Tip</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="8e3f3-117"><strong>Utilizați acest tip pentru</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="8e3f3-118"><strong>Raport de cheltuieli</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="8e3f3-119">Creați fluxuri de lucru de aprobare pentru rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="8e3f3-120"><strong>Publicarea automată a rapoartelor de cheltuieli</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="8e3f3-121">Creați fluxuri de lucru automate de publicare pentru rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="8e3f3-122"><strong>Element de linie de cheltuială</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="8e3f3-123">Creați fluxuri de lucru de aprobare pentru elemente de linie pe rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="8e3f3-124"><strong>Publicare automată de element de cheltuială de linie</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="8e3f3-125">Creați fluxuri de lucru de publicare automată pentru elemente de linie pe rapoartele de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="8e3f3-126"><strong>Cerere de călătorie</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="8e3f3-127">Creați fluxuri de lucru de aprobare pentru cererile de călătorie.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="8e3f3-128"><strong>Solicitare de avans în numerar</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="8e3f3-129">Creați fluxuri de lucru de aprobare pentru solicitări de avans în numerar.</span><span class="sxs-lookup"><span data-stu-id="8e3f3-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="8e3f3-130"><strong>Recuperarea impozitului TVA</strong></span><span class="sxs-lookup"><span data-stu-id="8e3f3-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="8e3f3-131">Creați fluxuri de lucru de aprobare pentru recuperarea taxei pe valoarea adăugată (TVA).</span><span class="sxs-lookup"><span data-stu-id="8e3f3-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]