---
title: Ce este nou în Project Service Automation versiunea actualizată 16, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 16, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754742"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="2ab77-103">Project Service Automation V3, versiunea actualizată 16</span><span class="sxs-lookup"><span data-stu-id="2ab77-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="2ab77-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2ab77-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2ab77-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="2ab77-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="2ab77-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2ab77-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2ab77-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="2ab77-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="2ab77-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea unei soluții preferate](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="2ab77-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="2ab77-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 16.</span><span class="sxs-lookup"><span data-stu-id="2ab77-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="2ab77-110">Această versiune are un număr de V3.10.6.34 și este, în general, disponibilă printr-o auto-actualizare în ianuarie 2020</span><span class="sxs-lookup"><span data-stu-id="2ab77-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="2ab77-111">Lansarea de actualizări 16</span><span class="sxs-lookup"><span data-stu-id="2ab77-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2ab77-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="2ab77-112">Bug fixes</span></span>

-   <span data-ttu-id="2ab77-113">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="2ab77-113">Time and Expense</span></span>

    -   <span data-ttu-id="2ab77-114">Soluționat: Utilizatorii care încearcă să trimită intrări de timp și cheltuieli șterse pentru aprobări vor primi acum mesaje de eroare relevante.</span><span class="sxs-lookup"><span data-stu-id="2ab77-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="2ab77-115">Gestionare de proiect</span><span class="sxs-lookup"><span data-stu-id="2ab77-115">Project Management</span></span>

    -   <span data-ttu-id="2ab77-116">Soluționat: Unitățile de resurse definite pentru membrii echipei din șabloane sunt respectate cu șabloanele care se aplică unui nou proiect.</span><span class="sxs-lookup"><span data-stu-id="2ab77-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="2ab77-117">Soluționat: o gestionare îmbunătățită a realocării proprietății înregistrărilor.</span><span class="sxs-lookup"><span data-stu-id="2ab77-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="2ab77-118">Soluționat: proiectele care sunt în proces de copiere nu vor putea fi copiate până la finalizarea tuturor operațiunilor de copiere.</span><span class="sxs-lookup"><span data-stu-id="2ab77-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="2ab77-119">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="2ab77-119">Resource Management</span></span>

    -   <span data-ttu-id="2ab77-120">Soluționat: Extinderea rezervărilor gestionează acum duratele scurte corect și nu mai creează zero ore pentru rezervările extinse.</span><span class="sxs-lookup"><span data-stu-id="2ab77-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="2ab77-121">Soluționat: Vizualizarea de reconciliere se face acum când fusul orar al proiectului este +5:30 GMT și timpul de utilizare al utilizatorului este diferit.</span><span class="sxs-lookup"><span data-stu-id="2ab77-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="2ab77-122">Sales</span><span class="sxs-lookup"><span data-stu-id="2ab77-122">Sales</span></span>

    -   <span data-ttu-id="2ab77-123">Soluționat: Când un proiect mapat la o linie de contract este eliminat și un nou proiect este mapat, înregistrările efective ale noului proiect nu erau reevaluate pe baza regulilor de facturare și prețuri definite pe linia contractului.</span><span class="sxs-lookup"><span data-stu-id="2ab77-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="2ab77-124">Acest lucru a fost soluționat în această versiune.</span><span class="sxs-lookup"><span data-stu-id="2ab77-124">This has been fixed in this release.</span></span> <span data-ttu-id="2ab77-125">Prețurile și înregistrările efective ale proiectului nou mapat vor fi inversate și re-create în mod corect pe baza regulilor de stabilire a prețurilor și de facturare a liniei de contract.</span><span class="sxs-lookup"><span data-stu-id="2ab77-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="2ab77-126">Ca urmare, înregistrările reale ale proiectului care nu a fost mapat vor fi reevaluate și re-create.</span><span class="sxs-lookup"><span data-stu-id="2ab77-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="2ab77-127">Soluționat: validarea suplimentară a fost adăugată la linia estimativă în câmpul **Cantitate** pentru a se asigura că valorile nule nu persistă.</span><span class="sxs-lookup"><span data-stu-id="2ab77-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="2ab77-128">Soluționat: Când datele reale au fost actualizate pe un proiect, a fost adăugat un buton de actualizare în formularul principal al proiectului, pentru a permite utilizatorilor să resincronizeze datele reale.</span><span class="sxs-lookup"><span data-stu-id="2ab77-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="2ab77-129">Soluționat: Când utilizatorii trec de la 2.X la 3.X, proiectele cu o valoare NULL pentru numele proiectului vor fi permise.</span><span class="sxs-lookup"><span data-stu-id="2ab77-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

