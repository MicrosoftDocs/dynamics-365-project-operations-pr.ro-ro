---
title: Actualizarea unui proiect
description: Acest subiect furnizează informații despre actualizarea proiectelor în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286398"
---
# <a name="update-a-project"></a><span data-ttu-id="1a51b-103">Actualizarea unui proiect</span><span class="sxs-lookup"><span data-stu-id="1a51b-103">Update a project</span></span>

<span data-ttu-id="1a51b-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="1a51b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1a51b-105">Mai jos este un rezumat al câmpurilor care pot fi actualizate pe un proiect după ce a fost creat și orice implicații aplicabile ale actualizărilor.</span><span class="sxs-lookup"><span data-stu-id="1a51b-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="1a51b-106">Câmpuri de detaliu ale proiectului</span><span class="sxs-lookup"><span data-stu-id="1a51b-106">Project detail fields</span></span>

- <span data-ttu-id="1a51b-107">**Nume**: titlul proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a51b-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="1a51b-108">**Descriere**: o prezentare generală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a51b-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="1a51b-109">**Client**: Compania căreia îi va fi livrat proiectul.</span><span class="sxs-lookup"><span data-stu-id="1a51b-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="1a51b-110">**Șablon de calendar**: orele de lucru ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a51b-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="1a51b-111">Când câmpul este schimbat, întreaga planificare este recalculată.</span><span class="sxs-lookup"><span data-stu-id="1a51b-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="1a51b-112">**Monedă**: moneda pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="1a51b-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="1a51b-113">Acest câmp implicit se bazează pe moneda definită în unitatea contractantă.</span><span class="sxs-lookup"><span data-stu-id="1a51b-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="1a51b-114">Când unitatea contractantă este actualizată, câmpul este, de asemenea, actualizat.</span><span class="sxs-lookup"><span data-stu-id="1a51b-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="1a51b-115">**Unitate contractantă**: unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client.</span><span class="sxs-lookup"><span data-stu-id="1a51b-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="1a51b-116">**Manager de proiect**: membru al echipei de proiect care are autoritatea de a revizui și aproba intrările și cheltuielile de timp.</span><span class="sxs-lookup"><span data-stu-id="1a51b-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="1a51b-117">Câmpuri de estimare</span><span class="sxs-lookup"><span data-stu-id="1a51b-117">Estimate fields</span></span>

- <span data-ttu-id="1a51b-118">**Data estimată de începere**: data la care va începe proiectul.</span><span class="sxs-lookup"><span data-stu-id="1a51b-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="1a51b-119">Când acest câmp este actualizat, orice sarcini din proiect se vor muta proporțional cu data de începere nouă.</span><span class="sxs-lookup"><span data-stu-id="1a51b-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="1a51b-120">**Data de finalizare**: data la care proiectul este programat să se încheie.</span><span class="sxs-lookup"><span data-stu-id="1a51b-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="1a51b-121">**Efort**: efortul estimat al proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a51b-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="1a51b-122">Când sarcinile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.</span><span class="sxs-lookup"><span data-stu-id="1a51b-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="1a51b-123">**Costul estimat al forței de muncă**: costul estimat al forței de muncă al proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a51b-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="1a51b-124">Când costurile cu forța de muncă sunt adăugate la proiect, acest câmp nu mai poate fi modificat.</span><span class="sxs-lookup"><span data-stu-id="1a51b-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="1a51b-125">**Cheltuieli estimate**: cheltuielile estimate ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a51b-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="1a51b-126">Când cheltuielile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.</span><span class="sxs-lookup"><span data-stu-id="1a51b-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="1a51b-127">Proiectați câmpurile reale</span><span class="sxs-lookup"><span data-stu-id="1a51b-127">Project actual fields</span></span>
- <span data-ttu-id="1a51b-128">**Start efectiv**: data la care a început proiectul.</span><span class="sxs-lookup"><span data-stu-id="1a51b-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="1a51b-129">**Finalizare efectivă**: pentru a fi actualizat la finalizarea unui proiect.</span><span class="sxs-lookup"><span data-stu-id="1a51b-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="1a51b-130">Câmpuri de stare proiect</span><span class="sxs-lookup"><span data-stu-id="1a51b-130">Project status fields</span></span>

- <span data-ttu-id="1a51b-131">**Starea generală a proiectului**: starea generală a proiectului oferită de managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="1a51b-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="1a51b-132">**Comentarii**: o narațiune privind starea actuală a proiectului oferită de managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="1a51b-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]