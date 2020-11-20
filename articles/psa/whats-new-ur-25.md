---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 25, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183558"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="45158-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 25, V3</span><span class="sxs-lookup"><span data-stu-id="45158-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="45158-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="45158-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="45158-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="45158-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="45158-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="45158-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="45158-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="45158-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="45158-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="45158-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="45158-109">Acest subiect listează caracteristicile și remedierile noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 25 Această versiune are un număr de compilare de V 3.10.43.76 și este, în general, disponibilă prin auto-actualizare în octombrie 2020.</span><span class="sxs-lookup"><span data-stu-id="45158-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="45158-110">Lansarea de actualizări 25</span><span class="sxs-lookup"><span data-stu-id="45158-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="45158-111">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="45158-111">Bug fixes</span></span>

<span data-ttu-id="45158-112">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="45158-112">**Time and Expense**</span></span>

<span data-ttu-id="45158-113">A fost rezolvată următoarea problemă:</span><span class="sxs-lookup"><span data-stu-id="45158-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="45158-114">Diagrama de introducere a timpului care arată date suplimentare pe baza unui interval prea mare de recuperare.</span><span class="sxs-lookup"><span data-stu-id="45158-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="45158-115">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="45158-115">**Resource Management**</span></span>

<span data-ttu-id="45158-116">A fost rezolvată următoarea problemă:</span><span class="sxs-lookup"><span data-stu-id="45158-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="45158-117">A fost adăugat codul de implementare a pachetului Package Deployer pentru a omite importarea patch-urilor Universal Resource Scheduling dacă există deja o versiune superioară de patch-uri.</span><span class="sxs-lookup"><span data-stu-id="45158-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="45158-118">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="45158-118">**Project Management**</span></span>

<span data-ttu-id="45158-119">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="45158-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="45158-120">Corecții de rotunjire și discrepanțe de curs valutar care rezultă în costuri planificate incorecte în grila de urmărire a proiectului.</span><span class="sxs-lookup"><span data-stu-id="45158-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="45158-121">Sprijiniți capacitatea de a afișa două sau mai multe grile de reacție pe formularul **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="45158-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="45158-122">Validare oferită pentru a aborda capacitatea de a atribui o sarcină după data de încheiere a calendarului, ceea ce duce la o alocare a resurselor eșuată.</span><span class="sxs-lookup"><span data-stu-id="45158-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="45158-123">Îmbunătățirea gestionării erorilor pentru a aborda excepția de referință nulă generată din următoarele:</span><span class="sxs-lookup"><span data-stu-id="45158-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="45158-124">**PreValidateProjectTeamMemberCreate** insert</span><span class="sxs-lookup"><span data-stu-id="45158-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="45158-125">**PreValidateProjectTaskCreate** când se creează o sarcină de proiect fără un proiect asociat</span><span class="sxs-lookup"><span data-stu-id="45158-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="45158-126">**PreProjectTeamMemberCreate** insert</span><span class="sxs-lookup"><span data-stu-id="45158-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="45158-127">**PostProjectTeamMemberDelete** insert</span><span class="sxs-lookup"><span data-stu-id="45158-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="45158-128">**PreValidateProjectTaskDelete** insert</span><span class="sxs-lookup"><span data-stu-id="45158-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="45158-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="45158-129">**Sales**</span></span>

<span data-ttu-id="45158-130">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="45158-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="45158-131">Îmbunătățirea gestionării erorilor pentru a aborda excepțiile de referință nule generate de **Copiați proiectul: estimări HelperResource Management**.</span><span class="sxs-lookup"><span data-stu-id="45158-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="45158-132">**Nu este pregătit pentru facturare** pe o **Restanță de facturare de timp și materiale** nu șterge starea de facturare.</span><span class="sxs-lookup"><span data-stu-id="45158-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="45158-133">S-au corectat butoanele **Prețuri** etichetate greșit pe filele **Prețul rolului** și **Articole din catalog**.</span><span class="sxs-lookup"><span data-stu-id="45158-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
