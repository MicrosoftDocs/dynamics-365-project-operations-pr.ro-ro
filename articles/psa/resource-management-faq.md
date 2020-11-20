---
title: Întrebări frecvente de gestionarea resurselor
description: Acest subiect oferă răspunsuri la întrebările frecvente despre gestionarea resurselor.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120153"
---
# <a name="resource-management-faq"></a><span data-ttu-id="876b9-103">Întrebări frecvente de gestionarea resurselor</span><span class="sxs-lookup"><span data-stu-id="876b9-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="876b9-104">Care este diferența dintre un membru al echipei și o cerință de resurse?</span><span class="sxs-lookup"><span data-stu-id="876b9-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="876b9-105">Un membru al echipei de proiect poate fi atribuit la activități, rezervat sau supra-rezervat și poate fi setat ca aprobator.</span><span class="sxs-lookup"><span data-stu-id="876b9-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="876b9-106">O cerință de resurse poate exista fără un membru al echipei de proiect, ca o notă de proiect de cerere.</span><span class="sxs-lookup"><span data-stu-id="876b9-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="876b9-107">Care este diferența dintre orele propuse și cele cu rezervare provizorie?</span><span class="sxs-lookup"><span data-stu-id="876b9-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="876b9-108">Orele propuse și orele de rezervate provizoriu diferă ca vizibilitate.</span><span class="sxs-lookup"><span data-stu-id="876b9-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="876b9-109">Orele propuse sunt vizibile numai pentru managerii de resurse și managerul de proiect care a inițiat cererea utilizând o solicitare de resurse.</span><span class="sxs-lookup"><span data-stu-id="876b9-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="876b9-110">Orele rezervate provizoriu sunt vizibile pentru oricine are acces la panoul de planificare.</span><span class="sxs-lookup"><span data-stu-id="876b9-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="876b9-111">Pot vedea orele de rezervate provizoriu pentru resurse într-o echipă?</span><span class="sxs-lookup"><span data-stu-id="876b9-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="876b9-112">Rezervările provizorii pot fi făcute când vă rezervați o cerere de resurse.</span><span class="sxs-lookup"><span data-stu-id="876b9-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="876b9-113">Resursele care sunt rezervate provizoriu într-o echipă de proiect apar ca membri ai echipei care au ore cu rezervare provizorie.</span><span class="sxs-lookup"><span data-stu-id="876b9-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="876b9-114">Acestea apar, de asemenea, pe tabloul de planificare.</span><span class="sxs-lookup"><span data-stu-id="876b9-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="876b9-115">Cum modific orele necesare și datele de început și de sfârșit pentru o resursă (generică sau denumită) pe care am rezervat-o?</span><span class="sxs-lookup"><span data-stu-id="876b9-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="876b9-116">După ce resursele sunt rezervate, selectați **Menținere rezervări** pentru a face orice modificări necesare.</span><span class="sxs-lookup"><span data-stu-id="876b9-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="876b9-117">Ce tipuri de resurse suportă Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="876b9-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="876b9-118">**Utilizator** și **Persoană de contact** sunt singurele tipuri de resurse care sunt acceptate în Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="876b9-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="876b9-119">Deși puteți crea alte tipuri de resurse (de exemplu, **Echipamente** și **Grupuri**), nu este acceptat niciun caz de utilizare completă pentru ele.</span><span class="sxs-lookup"><span data-stu-id="876b9-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="876b9-120">Care este diferența dintre o atribuire și o rezervare?</span><span class="sxs-lookup"><span data-stu-id="876b9-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="876b9-121">Atribuirile sunt alocarea de resurse pentru activitățile de proiect în planificarea proiectului.</span><span class="sxs-lookup"><span data-stu-id="876b9-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="876b9-122">Resursele pot fi reale sau generice.</span><span class="sxs-lookup"><span data-stu-id="876b9-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="876b9-123">Rezervările sunt alocarea fermă sau provizorie de resurse pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="876b9-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="876b9-124">Rezervările ferme consumă capacitatea unei resurse.</span><span class="sxs-lookup"><span data-stu-id="876b9-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="876b9-125">În mod ideal, pentru resurse reale, rezervările și atribuirile ar trebui să fie în acord, deoarece acestea nu diferă.</span><span class="sxs-lookup"><span data-stu-id="876b9-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="876b9-126">Cu toate acestea, PSA nu pune în aplicare acest acord.</span><span class="sxs-lookup"><span data-stu-id="876b9-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="876b9-127">Vizualizarea Reconciliere arată unui manager de proiect locurile în care rezervările și atribuirile unei resurse nu sunt de acord.</span><span class="sxs-lookup"><span data-stu-id="876b9-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
