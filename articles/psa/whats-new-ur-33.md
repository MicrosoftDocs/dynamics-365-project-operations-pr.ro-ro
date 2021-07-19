---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 33, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334587"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="4156f-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 33, V3</span><span class="sxs-lookup"><span data-stu-id="4156f-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4156f-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4156f-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="4156f-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="4156f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4156f-106">Este compatibil cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4156f-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4156f-107">Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea.</span><span class="sxs-lookup"><span data-stu-id="4156f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="4156f-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4156f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4156f-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 33.</span><span class="sxs-lookup"><span data-stu-id="4156f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="4156f-110">Această versiune are un număr de compilări V3.10.54.98 și este, în general, disponibilă prin auto-actualizare în iulie 2021.</span><span class="sxs-lookup"><span data-stu-id="4156f-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="4156f-111">Lansarea de actualizări 33</span><span class="sxs-lookup"><span data-stu-id="4156f-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4156f-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="4156f-112">Bug fixes</span></span>

<span data-ttu-id="4156f-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="4156f-113">**Time and Expense**</span></span>

<span data-ttu-id="4156f-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="4156f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4156f-115">Două câmpuri blocate, **msdyn_description** și **msdyn_externaldescription**, sunt editabile după trimitere.</span><span class="sxs-lookup"><span data-stu-id="4156f-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="4156f-116">Apare un mesaj de eroare dacă se creează o cheltuială care nu este legată de un proiect.</span><span class="sxs-lookup"><span data-stu-id="4156f-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="4156f-117">Atunci când se creează o intrare de timp, rolul resursei este implicit un rol inactiv.</span><span class="sxs-lookup"><span data-stu-id="4156f-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="4156f-118">Liniile din jurnal asociate cu o cheltuială retrasă și ștearsă nu sunt șterse.</span><span class="sxs-lookup"><span data-stu-id="4156f-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="4156f-119">Pe **Intrare de timp Formular de creare rapidă**, actualizați vizualizarea **Lista sarcinilor proiectului** pentru a schimba data afișată implicit la data de începere a sarcinii.</span><span class="sxs-lookup"><span data-stu-id="4156f-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="4156f-120">Când creați o intrare de timp din fila **Corelate** a resursei rezervabile, intrarea de timp este creată incorect pentru utilizatorul conectat în locul resursei principale rezervabile.</span><span class="sxs-lookup"><span data-stu-id="4156f-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="4156f-121">Se adaugă câmpuri noi la căsuța de dialog **Aprobare în bloc MDD**.</span><span class="sxs-lookup"><span data-stu-id="4156f-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="4156f-122">**Planificarea unui proiect**</span><span class="sxs-lookup"><span data-stu-id="4156f-122">**Project planning**</span></span>

<span data-ttu-id="4156f-123">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="4156f-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="4156f-124">Performanță lentă la crearea proiectului atunci când șabloanele pentru orele de lucru la proiect sunt aplicate cu calendare complexe.</span><span class="sxs-lookup"><span data-stu-id="4156f-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="4156f-125">Când data de începere este ulterioară față de data de încheiere, se afișează o eroare pe șablonul de copiere a proiectului din cauza diferențelor în componenta de timp a fiecărui câmp.</span><span class="sxs-lookup"><span data-stu-id="4156f-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="4156f-126">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="4156f-126">**Resource management**</span></span>

<span data-ttu-id="4156f-127">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="4156f-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="4156f-128">Un parametru incorect este utilizat în interogarea utilizării resurselor și XML duce la rezultate incorecte ale filtrului pe grila **Utilizarea resurselor**.</span><span class="sxs-lookup"><span data-stu-id="4156f-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="4156f-129">Confirmarea **Extindere rezervări** afișează data incorectă de încheiere a rezervărilor.</span><span class="sxs-lookup"><span data-stu-id="4156f-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="4156f-130">**Vânzări**</span><span class="sxs-lookup"><span data-stu-id="4156f-130">**Sales**</span></span>

<span data-ttu-id="4156f-131">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="4156f-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="4156f-132">Apare un mesaj de eroare dacă se creează un preț de categorie cu valori lipsă.</span><span class="sxs-lookup"><span data-stu-id="4156f-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="4156f-133">Apare un mesaj de eroare dacă se creează o etapă a liniei de contract fără o linie de comandă.</span><span class="sxs-lookup"><span data-stu-id="4156f-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
