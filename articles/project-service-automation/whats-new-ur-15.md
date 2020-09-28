---
title: Ce este nou în Project Service Automation versiunea actualizată 15, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 15, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754743"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="807ce-103">Project Service Automation V3, versiunea actualizată 15</span><span class="sxs-lookup"><span data-stu-id="807ce-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="807ce-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="807ce-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="807ce-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="807ce-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="807ce-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="807ce-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="807ce-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="807ce-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="807ce-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="807ce-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="807ce-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 15.</span><span class="sxs-lookup"><span data-stu-id="807ce-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="807ce-110">Această versiune are un număr de V3.10.5.28 și este, în general, disponibilă printr-o auto-actualizare în ianuarie 2020.</span><span class="sxs-lookup"><span data-stu-id="807ce-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="807ce-111">Lansarea de actualizări 15</span><span class="sxs-lookup"><span data-stu-id="807ce-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="807ce-112">Îmbunătățiri</span><span class="sxs-lookup"><span data-stu-id="807ce-112">Enhancements</span></span>

- <span data-ttu-id="807ce-113">Gestionare de proiect</span><span class="sxs-lookup"><span data-stu-id="807ce-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="807ce-114">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="807ce-114">Bug fixes</span></span>

- <span data-ttu-id="807ce-115">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="807ce-115">Time and Expense</span></span>

  - <span data-ttu-id="807ce-116">Soluție: Adăugați gestionarea erorilor la încărcare în vizualizarea de reconciliere.</span><span class="sxs-lookup"><span data-stu-id="807ce-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="807ce-117">Soluție: Hub Resource Project: Redenumește **Cantitate** pentru a reduce ambiguitatea.</span><span class="sxs-lookup"><span data-stu-id="807ce-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="807ce-118">Remediat: Reglați vizualizarea **Copiere Coloane intrare de timp** pentru a include tipul.</span><span class="sxs-lookup"><span data-stu-id="807ce-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="807ce-119">Remediat: editarea duratei de intrare a timpului în vizualizarea grilei folosind numere zecimale are ca rezultat o eroare necunoscută pentru unele numere.</span><span class="sxs-lookup"><span data-stu-id="807ce-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="807ce-120">Gestionare de proiect</span><span class="sxs-lookup"><span data-stu-id="807ce-120">Project Management</span></span>

  - <span data-ttu-id="807ce-121">Remediat: Meniul derulant pentru **Folosiți în Urmărirea vizualizării** acum se extinde pe baza lățimii opțiunilor.</span><span class="sxs-lookup"><span data-stu-id="807ce-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="807ce-122">Remediat: Când gestionați proiecte în fusul orar +13, calculele sarcinilor pot afișa rezultate inexacte.</span><span class="sxs-lookup"><span data-stu-id="807ce-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="807ce-123">Remediat: **Ora de terminare a membrilor echipei** a fost corectat la utilizarea unui calendar de 24 de ore.</span><span class="sxs-lookup"><span data-stu-id="807ce-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="807ce-124">Remediat: a fost reactivat **FTB** în formularul principal **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="807ce-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="807ce-125">Remediat: calculul misiunilor nu mai ignoră într-o zi.</span><span class="sxs-lookup"><span data-stu-id="807ce-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="807ce-126">Remediat: Un nou banner de notificări a fost adăugat la formularul de proiect atunci când fusul orar diferă între utilizator și proiect.</span><span class="sxs-lookup"><span data-stu-id="807ce-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="807ce-127">Sales</span><span class="sxs-lookup"><span data-stu-id="807ce-127">Sales</span></span>

  - <span data-ttu-id="807ce-128">Remediat: căutarea categoriei estimării cheltuielilor poate fi utilizată pentru a filtra duplicatele.</span><span class="sxs-lookup"><span data-stu-id="807ce-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="807ce-129">Remediat: Cod **PluginDomain.ExecuteInTryCatchBlock (..)** nu mai ascunde originea excepției.</span><span class="sxs-lookup"><span data-stu-id="807ce-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="807ce-130">Remediat: Nu mai primiți un mesaj de eroare **Cercetare proiect** în formularul **Linie de ofertă** când există mai mult de 1000 de proiecte.</span><span class="sxs-lookup"><span data-stu-id="807ce-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="807ce-131">Remediat: gria **Estimări** pentru estimările forței de muncă și estimările cheltuielilor afișează acum simbolul corect al monedei.</span><span class="sxs-lookup"><span data-stu-id="807ce-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="807ce-132">Remediat: După ce o organizație actualizează PSA de la Update Release 14 la Update Release 15, fila **Planificare** nu mai apare la fel de goală pe formularul **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="807ce-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>