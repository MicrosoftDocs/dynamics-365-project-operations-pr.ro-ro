---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 26, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280413"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="cd72a-103">Project Service Automation, versiunea actualizată 26, V3</span><span class="sxs-lookup"><span data-stu-id="cd72a-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cd72a-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cd72a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cd72a-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="cd72a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cd72a-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cd72a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cd72a-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="cd72a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cd72a-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cd72a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cd72a-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 26, V3.</span><span class="sxs-lookup"><span data-stu-id="cd72a-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="cd72a-110">Această versiune are un număr de versiune V3.10.44.59 și este în general disponibilă printr-o actualizare automată în decembrie 2020.</span><span class="sxs-lookup"><span data-stu-id="cd72a-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="cd72a-111">Lansarea de actualizări 26</span><span class="sxs-lookup"><span data-stu-id="cd72a-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cd72a-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="cd72a-112">Bug fixes</span></span>

<span data-ttu-id="cd72a-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="cd72a-113">**Time and Expense**</span></span>

<span data-ttu-id="cd72a-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="cd72a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd72a-115">Utilizatorii pot modifica sarcina la o intrare de timp care a fost aprobată/trimisă.</span><span class="sxs-lookup"><span data-stu-id="cd72a-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="cd72a-116">Eroare „Referință obiect neconfigurat” la salvarea timpului de intrare.</span><span class="sxs-lookup"><span data-stu-id="cd72a-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="cd72a-117">Importarea intrării de timp din alocările de resurse creează intrări de timp cu valorile incorecte DateTime.</span><span class="sxs-lookup"><span data-stu-id="cd72a-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="cd72a-118">Când Project Service Automation și aplicația Field Service sunt ambele instalate, butonul **Nou** se afișează de două ori pe bara de comandă pentru intrările de timp în aplicația Field Service.</span><span class="sxs-lookup"><span data-stu-id="cd72a-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="cd72a-119">Actualizările de celule **Permiteți unitate** și **Grup de unități** funcționează acum pe grila **Estimări de cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="cd72a-120">Formularul **Actualizare editare intrare timp** include **Cronologie**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="cd72a-121">Aprobarea timpului pentru intrările de timp care nu fac parte din proiect blochează sistemul atunci când caută un rol de aprobator de proiect.</span><span class="sxs-lookup"><span data-stu-id="cd72a-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="cd72a-122">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="cd72a-122">**Resource Management**</span></span>

<span data-ttu-id="cd72a-123">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="cd72a-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd72a-124">S-a adăugat validarea în insertul **PostProjectCreate** pentru a verifica o cerință principală înainte de a crea una.</span><span class="sxs-lookup"><span data-stu-id="cd72a-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="cd72a-125">Formularul de creare rapidă **Membru al echipei de proiect** aruncă o excepție de referință nulă dacă câmpurile sunt eliminate din formular.</span><span class="sxs-lookup"><span data-stu-id="cd72a-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="cd72a-126">Generarea cerințelor pentru 12 ore peste 1 an va eșua.</span><span class="sxs-lookup"><span data-stu-id="cd72a-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="cd72a-127">S-a îmbunătățit excepția de referință nulă a mesajului de eroare în timpul creării cerințelor de resurse.</span><span class="sxs-lookup"><span data-stu-id="cd72a-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="cd72a-128">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="cd72a-128">**Project Management**</span></span>

<span data-ttu-id="cd72a-129">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="cd72a-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd72a-130">Validare îmbunătățită pentru a aborda excepția de referință nulă generată în insertul **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="cd72a-131">Proiectele publicate de programul de completare desktop Microsoft Project șterg atribuțiile neatribuite.</span><span class="sxs-lookup"><span data-stu-id="cd72a-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="cd72a-132">S-a adăugat o nouă validare atunci când referința proiectului unei sarcini este invalidă din cauza excepției de referință nulă din insertul **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="cd72a-133">Grila membrilor echipei nu afișează sarcini distincte în înregistrarea membrilor echipei.</span><span class="sxs-lookup"><span data-stu-id="cd72a-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="cd72a-134">S-au adăugat noi mesaje de validare și eroare din cauza excepției de referință nulă în insertul **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="cd72a-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cd72a-135">**Sales**</span></span>

<span data-ttu-id="cd72a-136">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="cd72a-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd72a-137">Atunci când selectați o linie bazată pe proiect în ofertă sau contract, butonul **Sugestie** ar trebui să fie vizibil numai atunci când selectați o linie bazată pe produs asociată unui produs existent.</span><span class="sxs-lookup"><span data-stu-id="cd72a-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="cd72a-138">Scindează privilegiul **Create_Product** din privilegiul **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="cd72a-139">Ștergerea unei linii de facturare provoacă eșecul referinței nule pe **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="cd72a-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]