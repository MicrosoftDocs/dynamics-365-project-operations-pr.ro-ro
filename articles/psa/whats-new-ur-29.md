---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 29, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664658"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="30c81-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 29, V3</span><span class="sxs-lookup"><span data-stu-id="30c81-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="30c81-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="30c81-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="30c81-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="30c81-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="30c81-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="30c81-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="30c81-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="30c81-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="30c81-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="30c81-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="30c81-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 29.</span><span class="sxs-lookup"><span data-stu-id="30c81-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="30c81-110">Această versiune are numărul de versiune V3.10.47.7 și este în general disponibilă printr-o actualizare automată în februarie 2021.</span><span class="sxs-lookup"><span data-stu-id="30c81-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="30c81-111">Lansarea de actualizări 29</span><span class="sxs-lookup"><span data-stu-id="30c81-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="30c81-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="30c81-112">Bug fixes</span></span>

<span data-ttu-id="30c81-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="30c81-113">**Time and Expense**</span></span>

<span data-ttu-id="30c81-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="30c81-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="30c81-115">Utilizatorii nu pot vizualiza orele de lucru înregistrate în zilele nelucrătoare în grila de introducere a timpului.</span><span class="sxs-lookup"><span data-stu-id="30c81-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="30c81-116">Intrările de cheltuieli aprobate pot fi editate în grilă.</span><span class="sxs-lookup"><span data-stu-id="30c81-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="30c81-117">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="30c81-117">**Project Management**</span></span>

<span data-ttu-id="30c81-118">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="30c81-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="30c81-119">Lipsa logicii de validare pentru a asigura orele de efort de atribuire a resurselor nu poate fi negativă.</span><span class="sxs-lookup"><span data-stu-id="30c81-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="30c81-120">Acțiunea personalizată, **AtribuireResursePentruSarcină** actualizează toate câmpurile în loc să actualizeze doar câmpurile modificate.</span><span class="sxs-lookup"><span data-stu-id="30c81-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="30c81-121">Când copiați un proiect într-un mediu cu inserturi sau fluxuri de lucru înregistrate pe evenimentul **CreațiProiect**, atributul **msdyn_bulkgenerationstatus** nu este actualizat dacă **CopiațiWBSLaProiect** eșuează.</span><span class="sxs-lookup"><span data-stu-id="30c81-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="30c81-122">Când extindeți calendarul proiectului, zilele lucrătoare nu sunt sortate în ordine crescătoare, cauzând eșecul unor actualizări ale sarcinilor proiectului.</span><span class="sxs-lookup"><span data-stu-id="30c81-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="30c81-123">Schimbarea managerului de proiect pe un proiect existent declanșează logica implicită a unității organizaționale.</span><span class="sxs-lookup"><span data-stu-id="30c81-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="30c81-124">**Vânzări**</span><span class="sxs-lookup"><span data-stu-id="30c81-124">**Sales**</span></span>

<span data-ttu-id="30c81-125">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="30c81-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="30c81-126">Fila **Executarea contractului** de pe pagina **Contract** eșuează în mod silențios în timpul inițializării când nu există linii de contract.</span><span class="sxs-lookup"><span data-stu-id="30c81-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
