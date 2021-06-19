---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 32, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129681"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="17bbd-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 32, V3</span><span class="sxs-lookup"><span data-stu-id="17bbd-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="17bbd-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="17bbd-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="17bbd-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="17bbd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="17bbd-106">Este compatibil cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="17bbd-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="17bbd-107">Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea.</span><span class="sxs-lookup"><span data-stu-id="17bbd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="17bbd-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="17bbd-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="17bbd-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 32.</span><span class="sxs-lookup"><span data-stu-id="17bbd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="17bbd-110">Această versiune are un număr de versiune V3.10.53.108 și este, în general, disponibilă prin auto-actualizare în iunie 2021.</span><span class="sxs-lookup"><span data-stu-id="17bbd-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="17bbd-111">Lansarea de actualizări 32</span><span class="sxs-lookup"><span data-stu-id="17bbd-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="17bbd-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="17bbd-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="17bbd-113">General</span><span class="sxs-lookup"><span data-stu-id="17bbd-113">General</span></span>

- <span data-ttu-id="17bbd-114">Atunci când o actualizare majoră eșuează, numai punctele principale de intrare ale aplicației ar trebui blocate, pentru a se asigura că entitățile partajate sunt încă accesibile.</span><span class="sxs-lookup"><span data-stu-id="17bbd-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="17bbd-115">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="17bbd-115">Time and Expense</span></span>

<span data-ttu-id="17bbd-116">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="17bbd-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="17bbd-117">**TimeEntriesImportFromResourceAssignment** nu menține timpii de început și de sfârșit ai porțiunii de sector a alocării resurselor.</span><span class="sxs-lookup"><span data-stu-id="17bbd-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="17bbd-118">Când selectați **Deschideți intrarea** pe grila **Intrare în timp**, este posibil să vi se împiedice selectarea altor formulare.</span><span class="sxs-lookup"><span data-stu-id="17bbd-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="17bbd-119">În timp ce importați alocări la intrări de timp, interogarea codului clientului poate genera o adresă URL lungă care nu reușește interogarea.</span><span class="sxs-lookup"><span data-stu-id="17bbd-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="17bbd-120">În grila **Intrare de timp**, după ce o valoare este ștearsă dintr-o celulă, focalizarea nu rămâne în grilă.</span><span class="sxs-lookup"><span data-stu-id="17bbd-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="17bbd-121">Butonul **Respinge** a fost eliminat din vizualizarea **Aprobări de procesare** pentru aprobări moderne.</span><span class="sxs-lookup"><span data-stu-id="17bbd-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="17bbd-122">Stabilitatea și performanța aprobării în bloc a timpului sunt afectate de blocaje și de eșecul de a gestiona în mod adecvat personalizările care sunt legate de entitatea **Intrare de timp**.</span><span class="sxs-lookup"><span data-stu-id="17bbd-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="17bbd-123">Planificare de proiect</span><span class="sxs-lookup"><span data-stu-id="17bbd-123">Project Planning</span></span>

- <span data-ttu-id="17bbd-124">O excepție de referință nulă este generată atunci când actualizați un proiect care are o valoare nulă în câmpul **Unitatea Contractantă**.</span><span class="sxs-lookup"><span data-stu-id="17bbd-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="17bbd-125">**Reîmprospătați totalul proiectului** calculează incorect costul rămas și vânzările rămase pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="17bbd-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="17bbd-126">Calculele de tarifare redundante afectează performanțele legate de actualizările contururilor de alocare a resurselor.</span><span class="sxs-lookup"><span data-stu-id="17bbd-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="17bbd-127">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="17bbd-127">Resource Management</span></span>

<span data-ttu-id="17bbd-128">A fost rezolvată următoarea problemă:</span><span class="sxs-lookup"><span data-stu-id="17bbd-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="17bbd-129">Când capacitatea calendaristică a unei resurse rezervabile este mai mare de 1, Project Service Automation recunoaște incorect capacitatea ca 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="17bbd-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="17bbd-130">Prin urmare, apare o buclă infinită în vizualizarea planificării.</span><span class="sxs-lookup"><span data-stu-id="17bbd-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="17bbd-131">Vânzări</span><span class="sxs-lookup"><span data-stu-id="17bbd-131">Sales</span></span>

<span data-ttu-id="17bbd-132">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="17bbd-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="17bbd-133">Când se creează o linie de jurnal care are un tip de tranzacție particularizat, apare următoarea excepție de referință nulă: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="17bbd-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="17bbd-134">Rolurile și categoriile care sunt inactivate înainte ca o ofertă să fie copiată nu ar trebui adăugate la rolurile și categoriile cu taxă ale ofertelor nou copiate.</span><span class="sxs-lookup"><span data-stu-id="17bbd-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="17bbd-135">Data documentului și data contabilă nu sunt aliniate cu data de început care este furnizată pe un detaliu al liniei de factură care este creat direct pe o schiță de factură.</span><span class="sxs-lookup"><span data-stu-id="17bbd-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="17bbd-136">Excepțiile de referință nulă sunt generate în scenarii care sunt legate de inactivarea rolurilor și categoriilor înainte de copierea unei cotații.</span><span class="sxs-lookup"><span data-stu-id="17bbd-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="17bbd-137">Acțiunea **Actualizați prețurile** asupra **Proiecte** nu actualizează estimările cheltuielilor și estimările de materiale.</span><span class="sxs-lookup"><span data-stu-id="17bbd-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
