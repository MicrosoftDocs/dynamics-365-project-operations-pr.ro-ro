---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 31, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945550"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="1a7d5-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 31, V3</span><span class="sxs-lookup"><span data-stu-id="1a7d5-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1a7d5-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1a7d5-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1a7d5-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1a7d5-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1a7d5-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1a7d5-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1a7d5-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 31.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="1a7d5-110">Această versiune are un număr de versiune V3.10.52.77 și este disponibil în general printr-o autoactualizare în mai 2021.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="1a7d5-111">Lansarea de actualizări 31</span><span class="sxs-lookup"><span data-stu-id="1a7d5-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1a7d5-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="1a7d5-112">Bug fixes</span></span>

<span data-ttu-id="1a7d5-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="1a7d5-113">**Time and Expense**</span></span>

<span data-ttu-id="1a7d5-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="1a7d5-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a7d5-115">Butoanele de comandă pentru introducerea timpului de pe pagina **Resursă ce se poate rezerva** erau confuze.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="1a7d5-116">O excepție de referință nulă a fost generată în **Project.SetTrackingFields** la aprobarea unei intrări de timp.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="1a7d5-117">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="1a7d5-117">**Resource Management**</span></span>

<span data-ttu-id="1a7d5-118">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="1a7d5-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a7d5-119">**Creare membru echipă** nu afișează corect setarea metadatelor de configurare a rezervării pentru **Stare rezervare comisă implicită**.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="1a7d5-120">La actualizarea de la PSA 1.X la 3.X, procesul de actualizare eșuează la **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="1a7d5-121">**Vânzări**</span><span class="sxs-lookup"><span data-stu-id="1a7d5-121">**Sales**</span></span>

<span data-ttu-id="1a7d5-122">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="1a7d5-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="1a7d5-123">Venitul real convertește sumele în moneda proiectului din grila de urmărire.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="1a7d5-124">Valoarea implicită a monedei nu este clară la crearea liniilor jurnal, a liniilor de ofertă și a liniilor de contract în scenarii în care moneda de bază a unei organizații diferă de moneda proiectului.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="1a7d5-125">Interogarea **Validarea de jurnal de corecții în așteptare** nu se filtrează după proiect.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="1a7d5-126">Vânzările rămase sunt calculate incorect pe un proiect.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="1a7d5-127">Ofertele pe bază de contact eșuează atunci când sunt create fără o listă de prețuri.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="1a7d5-128">Când selectați **Confirmați factura** nu este afișat niciun spinner de procesare.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="1a7d5-129">Când selectați **Creați factura** nu este afișat niciun spinner de procesare.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="1a7d5-130">Închiderea unei oferte ca pierdută nu anulează rezervările.</span><span class="sxs-lookup"><span data-stu-id="1a7d5-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







