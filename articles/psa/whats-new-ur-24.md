---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 24, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 24, V3.
author: ruhercul
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
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000271"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="d6c93-103">Project Service Automation, versiunea actualizată 24, V3</span><span class="sxs-lookup"><span data-stu-id="d6c93-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d6c93-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d6c93-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d6c93-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="d6c93-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d6c93-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d6c93-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d6c93-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="d6c93-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d6c93-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d6c93-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d6c93-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 24.</span><span class="sxs-lookup"><span data-stu-id="d6c93-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="d6c93-110">Această versiune are un număr de versiune V 3.10.42.43 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2020.</span><span class="sxs-lookup"><span data-stu-id="d6c93-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="d6c93-111">Lansarea de actualizări 24</span><span class="sxs-lookup"><span data-stu-id="d6c93-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d6c93-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="d6c93-112">Bug fixes</span></span>

<span data-ttu-id="d6c93-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d6c93-113">**Sales**</span></span>

<span data-ttu-id="d6c93-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d6c93-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6c93-115">Problemă la stabilirea listei de prețuri implicite a produselor.</span><span class="sxs-lookup"><span data-stu-id="d6c93-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="d6c93-116">Performanța câștigului Ofertei este lentă din cauza listei de prețuri încorporate și a copiilor înregistrărilor de prețuri de roluri.</span><span class="sxs-lookup"><span data-stu-id="d6c93-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="d6c93-117">**Contract proiect/Hub de vânzări** > **Linie produs/Cantitate linie comandă** este rotunjit automat la cel mai apropiat număr întreg.</span><span class="sxs-lookup"><span data-stu-id="d6c93-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="d6c93-118">Creșteți la privilegiile de sistem atunci când citiți listele de prețuri.</span><span class="sxs-lookup"><span data-stu-id="d6c93-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="d6c93-119">Copiați câmpurile de adresă ale clientului **address1_freighttermscode** și **address1_shippingmethodcode** la Ofertă/Comandă.</span><span class="sxs-lookup"><span data-stu-id="d6c93-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="d6c93-120">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="d6c93-120">**Time and Expense**</span></span>

<span data-ttu-id="d6c93-121">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d6c93-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6c93-122">**Grila de introducere timp** nu acceptă comportamentul de timp **Numai dată**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="d6c93-123">**Intrare timp** nu se reîmprospătează automat.</span><span class="sxs-lookup"><span data-stu-id="d6c93-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="d6c93-124">Este necesară o reîmprospătare manuală.</span><span class="sxs-lookup"><span data-stu-id="d6c93-124">A manual refresh is required.</span></span>
- <span data-ttu-id="d6c93-125">Nu se pot importa intrările de timp dintr-o atribuire atunci când există o pauză (0 ore) în atribuirile unei resurse.</span><span class="sxs-lookup"><span data-stu-id="d6c93-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="d6c93-126">Când creați o intrare de timp, setați startul identic cu **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="d6c93-127">Reactivați editarea în bloc pentru introducerea timpului.</span><span class="sxs-lookup"><span data-stu-id="d6c93-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="d6c93-128">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="d6c93-128">**Resource Management**</span></span>

<span data-ttu-id="d6c93-129">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d6c93-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6c93-130">Încercarea de a actualiza starea unei rezervări inter-zile fără o cerință va genera o excepție de referință nulă.</span><span class="sxs-lookup"><span data-stu-id="d6c93-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="d6c93-131">Eroare la încărcarea **Vizualizare reconciliere**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="d6c93-132">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="d6c93-132">**Project Management**</span></span>

<span data-ttu-id="d6c93-133">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="d6c93-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="d6c93-134">În **Planificare proiect**, la schimbarea de la **Manual** la **Auto**, salvarea automată nu se finalizează.</span><span class="sxs-lookup"><span data-stu-id="d6c93-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="d6c93-135">Costurile cheltuielilor nu ar trebui să se calculeze în raport cu varianța pe **Grila de urmărire a proiectului**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="d6c93-136">Comportament neconstant pentru coloanele **Etichetă estimativă** în timpul încărcării versus schimbarea tipului **Fază de timp**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="d6c93-137">Este posibil ca costul real al unui proiect să nu reflecte totalurile din **Valori reale**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="d6c93-138">**Data estimată de finalizare** de pe fila **Rezumat** nu se potrivește cu **Planificare WBS**.</span><span class="sxs-lookup"><span data-stu-id="d6c93-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="d6c93-139">**Actualizați orele reale** pe outdent nu funcționează corect.</span><span class="sxs-lookup"><span data-stu-id="d6c93-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="d6c93-140">Un manager de proiect în afara rădăcinii **BU** nu poate crea un proiect.</span><span class="sxs-lookup"><span data-stu-id="d6c93-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="d6c93-141">Modificările activității sau categoriei pe **Estimări de cheltuieli** nu sunt persistente.</span><span class="sxs-lookup"><span data-stu-id="d6c93-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="d6c93-142">**Copie contract** copiază planificările facturilor și starea de rulare.</span><span class="sxs-lookup"><span data-stu-id="d6c93-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="d6c93-143">Butonul **Actualizați datele reale** calculează incorect activitățile de rezumat.</span><span class="sxs-lookup"><span data-stu-id="d6c93-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="d6c93-144">Program de completare Microsoft Project: Remediați eroarea de referință nulă dacă un membru al echipei are o unitate de resurse goală.</span><span class="sxs-lookup"><span data-stu-id="d6c93-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]