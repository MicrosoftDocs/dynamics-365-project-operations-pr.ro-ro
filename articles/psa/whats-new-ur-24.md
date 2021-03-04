---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 24, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146723"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="d123a-103">Project Service Automation, versiunea actualizată 24, V3</span><span class="sxs-lookup"><span data-stu-id="d123a-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d123a-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d123a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d123a-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="d123a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d123a-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d123a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d123a-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="d123a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d123a-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d123a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d123a-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 24.</span><span class="sxs-lookup"><span data-stu-id="d123a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="d123a-110">Această versiune are un număr de versiune V 3.10.42.43 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2020.</span><span class="sxs-lookup"><span data-stu-id="d123a-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="d123a-111">Lansarea de actualizări 24</span><span class="sxs-lookup"><span data-stu-id="d123a-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d123a-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="d123a-112">Bug fixes</span></span>

<span data-ttu-id="d123a-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d123a-113">**Sales**</span></span>

<span data-ttu-id="d123a-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d123a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d123a-115">Problemă la stabilirea listei de prețuri implicite a produselor.</span><span class="sxs-lookup"><span data-stu-id="d123a-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="d123a-116">Performanța câștigului Ofertei este lentă din cauza listei de prețuri încorporate și a copiilor înregistrărilor de prețuri de roluri.</span><span class="sxs-lookup"><span data-stu-id="d123a-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="d123a-117">**Contract proiect/Hub de vânzări** > **Linie produs/Cantitate linie comandă** este rotunjit automat la cel mai apropiat număr întreg.</span><span class="sxs-lookup"><span data-stu-id="d123a-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="d123a-118">Creșteți la privilegiile de sistem atunci când citiți listele de prețuri.</span><span class="sxs-lookup"><span data-stu-id="d123a-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="d123a-119">Copiați câmpurile de adresă ale clientului **address1_freighttermscode** și **address1_shippingmethodcode** la Ofertă/Comandă.</span><span class="sxs-lookup"><span data-stu-id="d123a-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="d123a-120">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="d123a-120">**Time and Expense**</span></span>

<span data-ttu-id="d123a-121">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d123a-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="d123a-122">**Grila de introducere timp** nu acceptă comportamentul de timp **Numai dată**.</span><span class="sxs-lookup"><span data-stu-id="d123a-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="d123a-123">**Intrare timp** nu se reîmprospătează automat.</span><span class="sxs-lookup"><span data-stu-id="d123a-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="d123a-124">Este necesară o reîmprospătare manuală.</span><span class="sxs-lookup"><span data-stu-id="d123a-124">A manual refresh is required.</span></span>
- <span data-ttu-id="d123a-125">Nu se pot importa intrările de timp dintr-o atribuire atunci când există o pauză (0 ore) în atribuirile unei resurse.</span><span class="sxs-lookup"><span data-stu-id="d123a-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="d123a-126">Când creați o intrare de timp, setați startul identic cu **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="d123a-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="d123a-127">Reactivați editarea în bloc pentru introducerea timpului.</span><span class="sxs-lookup"><span data-stu-id="d123a-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="d123a-128">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="d123a-128">**Resource Management**</span></span>

<span data-ttu-id="d123a-129">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d123a-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="d123a-130">Încercarea de a actualiza starea unei rezervări inter-zile fără o cerință va genera o excepție de referință nulă.</span><span class="sxs-lookup"><span data-stu-id="d123a-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="d123a-131">Eroare la încărcarea **Vizualizare reconciliere**.</span><span class="sxs-lookup"><span data-stu-id="d123a-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="d123a-132">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="d123a-132">**Project Management**</span></span>

<span data-ttu-id="d123a-133">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d123a-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="d123a-134">În **Planificare proiect**, la schimbarea de la **Manual** la **Auto**, salvarea automată nu se finalizează.</span><span class="sxs-lookup"><span data-stu-id="d123a-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="d123a-135">Costurile cheltuielilor nu ar trebui să se calculeze în raport cu varianța pe **Grila de urmărire a proiectului**.</span><span class="sxs-lookup"><span data-stu-id="d123a-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="d123a-136">Comportament neconstant pentru coloanele **Etichetă estimativă** în timpul încărcării versus schimbarea tipului **Fază de timp**.</span><span class="sxs-lookup"><span data-stu-id="d123a-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="d123a-137">Este posibil ca costul real al unui proiect să nu reflecte totalurile din **Valori reale**.</span><span class="sxs-lookup"><span data-stu-id="d123a-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="d123a-138">**Data estimată de finalizare** de pe fila **Rezumat** nu se potrivește cu **Planificare WBS**.</span><span class="sxs-lookup"><span data-stu-id="d123a-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="d123a-139">**Actualizați orele reale** pe outdent nu funcționează corect.</span><span class="sxs-lookup"><span data-stu-id="d123a-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="d123a-140">Un manager de proiect în afara rădăcinii **BU** nu poate crea un proiect.</span><span class="sxs-lookup"><span data-stu-id="d123a-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="d123a-141">Modificările activității sau categoriei pe **Estimări de cheltuieli** nu sunt persistente.</span><span class="sxs-lookup"><span data-stu-id="d123a-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="d123a-142">**Copie contract** copiază planificările facturilor și starea de rulare.</span><span class="sxs-lookup"><span data-stu-id="d123a-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="d123a-143">Butonul **Actualizați datele reale** calculează incorect activitățile de rezumat.</span><span class="sxs-lookup"><span data-stu-id="d123a-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="d123a-144">Program de completare Microsoft Project: Remediați eroarea de referință nulă dacă un membru al echipei are o unitate de resurse goală.</span><span class="sxs-lookup"><span data-stu-id="d123a-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

