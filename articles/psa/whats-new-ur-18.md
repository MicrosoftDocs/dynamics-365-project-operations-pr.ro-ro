---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 18, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 18, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: f7def50e77a83fd790b81b1b4fd36008ce293b0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006661"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="9ba8a-103">Project Service Automation, versiunea actualizată 18, V3</span><span class="sxs-lookup"><span data-stu-id="9ba8a-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9ba8a-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9ba8a-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9ba8a-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9ba8a-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="9ba8a-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9ba8a-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9ba8a-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 18.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="9ba8a-110">Această versiune are un număr de versiune V3.10.8.12 și este disponibil în general printr-o autoactualizare în aprilie 2020.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="9ba8a-111">Lansarea de actualizări 18</span><span class="sxs-lookup"><span data-stu-id="9ba8a-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9ba8a-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="9ba8a-112">Bug fixes</span></span>

<span data-ttu-id="9ba8a-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="9ba8a-113">**Time and Expense**</span></span>

- <span data-ttu-id="9ba8a-114">Remediat: fluxurile **Retragere** . **Cerere** și **Anulare aprobare** declanșează excepții cu mesaje de eroare neclare.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="9ba8a-115">Remediat: când **Anulare aprobare** eșuează pentru o cheltuială, nu este declanșată o eroare de excepție relevantă.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="9ba8a-116">Remediat: grila de introducere a timpului gestionează în mod incorect zilele nelucrătoare în Australia, după trecerea la ora de vară (DST) în octombrie.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="9ba8a-117">Remediat: o logică implicită incorectă împiedică remiterea cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="9ba8a-118">Remediat: când aprobarea intrării de timp nu reușește, aprobarea rămâne într-o stare de **Asteptare**.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="9ba8a-119">Remediat: erori SQL la aprobările în bloc (blocare deadlock/expirare).</span><span class="sxs-lookup"><span data-stu-id="9ba8a-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="9ba8a-120">Remediat: probleme semnificative de performanță în experiența utilizatorului, cauzate de actualizarea membrilor echipei în timp ce aprobă înregistrările de timp.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="9ba8a-121">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="9ba8a-121">**Project Management**</span></span>

- <span data-ttu-id="9ba8a-122">Remediat: notificarea pentru fusul orar a fost mutată din vizualizarea **Reconciliere** la formularul principal **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="9ba8a-123">Remediat: șablonul Calendar nu este ales implicit corect atunci când se deschide un nou formular de proiect.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="9ba8a-124">Remediat: pentru browserele bazate pe Chromium, utilizatorii nu pot selecta cu ușurință sarcinile predecesoare pentru a le șterge.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="9ba8a-125">Remediat: crearea sau copierea **Proiect din șablon gol** preia atribuiri fără legătură.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="9ba8a-126">Remediat: în cazuri specifice Microsoft Edge, crearea unei noi atribuiri din grila de sarcini duce la crearea de înregistrări duplicate.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="9ba8a-127">Remediat: în modul manual, utilizatorii nu pot actualiza datele de începere a activității pentru a fi mai târzii decât data salvată curentă.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="9ba8a-128">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="9ba8a-128">**Resource Management**</span></span>

- <span data-ttu-id="9ba8a-129">Remediat: vizualizarea **Reconciliere** rândul subtotal calculează incorect variația rezervărilor după extinderea rezervărilor.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="9ba8a-130">Remediat: vizualizarea **Reconciliere** afișează incorect atribuirile resurselor atunci când resursa rezervabilă are un calendar care nu se potrivește cu calendarul proiectului.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="9ba8a-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9ba8a-131">**Sales**</span></span>

- <span data-ttu-id="9ba8a-132">Remediat: când intrările de timp sunt reaprobate (**Aprobare > Anulare >** aprobați din nou), este creat un duplicat real netarifabil.</span><span class="sxs-lookup"><span data-stu-id="9ba8a-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]