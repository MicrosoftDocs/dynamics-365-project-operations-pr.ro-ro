---
title: Actualizarea unui proiect
description: Acest subiect furnizează informații despre actualizarea proiectelor în Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993386"
---
# <a name="update-a-project"></a><span data-ttu-id="ee3d8-103">Actualizarea unui proiect</span><span class="sxs-lookup"><span data-stu-id="ee3d8-103">Update a project</span></span>

<span data-ttu-id="ee3d8-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="ee3d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee3d8-105">Mai jos este un rezumat al câmpurilor care pot fi actualizate pe un proiect după ce a fost creat și orice implicații aplicabile ale actualizărilor.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="ee3d8-106">Câmpuri de detaliu ale proiectului</span><span class="sxs-lookup"><span data-stu-id="ee3d8-106">Project detail fields</span></span>

- <span data-ttu-id="ee3d8-107">**Nume**: titlul proiectului.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="ee3d8-108">**Descriere**: o prezentare generală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="ee3d8-109">**Client**: Compania căreia îi va fi livrat proiectul.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="ee3d8-110">**Șablon de calendar**: orele de lucru ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="ee3d8-111">Când câmpul este schimbat, întreaga planificare este recalculată.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="ee3d8-112">**Monedă**: moneda pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="ee3d8-113">Acest câmp implicit se bazează pe moneda definită în unitatea contractantă.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="ee3d8-114">Când unitatea contractantă este actualizată, câmpul este, de asemenea, actualizat.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="ee3d8-115">**Unitate contractantă**: unitatea organizațională care reprezintă grupul de firme sau divizia care este principalul responsabil cu câștigarea vânzării și cu gestionarea livrării de lucrări și servicii către client.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="ee3d8-116">**Manager de proiect**: membru al echipei de proiect care are autoritatea de a revizui și aproba intrările și cheltuielile de timp.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="ee3d8-117">Câmpuri de estimare</span><span class="sxs-lookup"><span data-stu-id="ee3d8-117">Estimate fields</span></span>

- <span data-ttu-id="ee3d8-118">**Data estimată de începere**: data la care va începe proiectul.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="ee3d8-119">Când acest câmp este actualizat, orice sarcini din proiect se vor muta proporțional cu data de începere nouă.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="ee3d8-120">**Data de finalizare**: data la care proiectul este programat să se încheie.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="ee3d8-121">**Efort**: efortul estimat al proiectului.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="ee3d8-122">Când sarcinile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="ee3d8-123">**Costul estimat al forței de muncă**: costul estimat al forței de muncă al proiectului.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="ee3d8-124">Când costurile cu forța de muncă sunt adăugate la proiect, acest câmp nu mai poate fi modificat.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="ee3d8-125">**Cheltuieli estimate**: cheltuielile estimate ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="ee3d8-126">Când cheltuielile sunt adăugate la proiect, acest câmp nu mai poate fi modificat.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="ee3d8-127">Proiectați câmpurile reale</span><span class="sxs-lookup"><span data-stu-id="ee3d8-127">Project actual fields</span></span>
- <span data-ttu-id="ee3d8-128">**Start efectiv**: data la care a început proiectul.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="ee3d8-129">**Finalizare efectivă**: pentru a fi actualizat la finalizarea unui proiect.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="ee3d8-130">Câmpuri de stare proiect</span><span class="sxs-lookup"><span data-stu-id="ee3d8-130">Project status fields</span></span>

- <span data-ttu-id="ee3d8-131">**Starea generală a proiectului**: starea generală a proiectului oferită de managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="ee3d8-132">**Comentarii**: o narațiune privind starea actuală a proiectului oferită de managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="ee3d8-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]