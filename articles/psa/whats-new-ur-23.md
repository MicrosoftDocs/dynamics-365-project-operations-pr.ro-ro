---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 23, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: f90c0d2168b261cf1b6ef10374f282274ea61af5
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948974"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="42816-103">Project Service Automation, versiunea actualizată 23, V3</span><span class="sxs-lookup"><span data-stu-id="42816-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="42816-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="42816-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="42816-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="42816-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="42816-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="42816-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="42816-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="42816-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="42816-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="42816-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="42816-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 23.</span><span class="sxs-lookup"><span data-stu-id="42816-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="42816-110">Această versiune are un număr de versiune V 3.10.34.30 și este, în general, disponibilă printr-o auto-actualizare în august 2020.</span><span class="sxs-lookup"><span data-stu-id="42816-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="42816-111">Lansarea de actualizări 23</span><span class="sxs-lookup"><span data-stu-id="42816-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="42816-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="42816-112">Bug fixes</span></span>

<span data-ttu-id="42816-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="42816-113">**Time and Expense**</span></span>

<span data-ttu-id="42816-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="42816-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="42816-115">Gestionați cazul marginal în **Ștergere membru echipă proiect** pentru a oferi o excepție semnificativă.</span><span class="sxs-lookup"><span data-stu-id="42816-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="42816-116">Importul de activități are ca rezultat un ecran gol de eliminare.</span><span class="sxs-lookup"><span data-stu-id="42816-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="42816-117">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="42816-117">**Resource Management**</span></span>

<span data-ttu-id="42816-118">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="42816-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="42816-119">**Cardul de resurse al grilei de utilizare a resurselor** afișează date incorecte atunci când scala de timp este mai mare de cinci zile.</span><span class="sxs-lookup"><span data-stu-id="42816-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="42816-120">Când clienții creează o resursă rezervabilă, insertul nu reușește să adauge automat resursa la un grup Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="42816-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="42816-121">Vizualizarea **Reconciliere** afișează incorect contururile manuale în vizualizarea **Săptămână** sau **Lună**.</span><span class="sxs-lookup"><span data-stu-id="42816-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="42816-122">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="42816-122">**Project Management**</span></span>

<span data-ttu-id="42816-123">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="42816-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="42816-124">Un număr excesiv de entități **RetrieveMultiple pentru usersettings** cauzează performanțe degradate pentru aprobările de proiect și alte operațiuni.</span><span class="sxs-lookup"><span data-stu-id="42816-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="42816-125">Căutarea resurselor grilă **Planificarea activităților** este limitată pentru a afișa doar până la cinci membri ai echipei din echipa proiectului.</span><span class="sxs-lookup"><span data-stu-id="42816-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="42816-126">Căutarea resurselor grilă **Planificarea activităților** nu filtrează resursele inactive.</span><span class="sxs-lookup"><span data-stu-id="42816-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="42816-127">Modul manual nu funcționează așa cum era de așteptat în structura de repartizare a lucrărilor de planificare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="42816-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="42816-128">Grila **Planificarea activităților** arată **Categorii de tranzacții inactive**.</span><span class="sxs-lookup"><span data-stu-id="42816-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="42816-129">Grila **Alocarea resurselor** rotunjește incorect atunci când o activitate are mai multe atribuții.</span><span class="sxs-lookup"><span data-stu-id="42816-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="42816-130">Valorile de rotunjire sunt diferite între costul planificat și costul real pentru o singură activitate.</span><span class="sxs-lookup"><span data-stu-id="42816-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="42816-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="42816-131">**Sales**</span></span>

<span data-ttu-id="42816-132">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="42816-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="42816-133">**Preluați toate categoriile de tranzacții** la dublu clic creează mai multe linii.</span><span class="sxs-lookup"><span data-stu-id="42816-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]