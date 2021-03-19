---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 21, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 21, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 69b592db7456bf11c2e933256569d726056d1a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280638"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="2d682-103">Project Service Automation, versiunea actualizată 21, V3</span><span class="sxs-lookup"><span data-stu-id="2d682-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2d682-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2d682-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2d682-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="2d682-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2d682-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2d682-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2d682-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="2d682-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2d682-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2d682-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2d682-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 21.</span><span class="sxs-lookup"><span data-stu-id="2d682-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="2d682-110">Această versiune are un număr de versiune V 3.10.32.50 și este disponibil în general printr-o autoactualizare în iunie 2020.</span><span class="sxs-lookup"><span data-stu-id="2d682-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="2d682-111">Lansarea de actualizări 21</span><span class="sxs-lookup"><span data-stu-id="2d682-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2d682-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="2d682-112">Bug fixes</span></span>

<span data-ttu-id="2d682-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="2d682-113">**Time and Expense**</span></span>

<span data-ttu-id="2d682-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2d682-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d682-115">La găzduirea **Control grilă introducere timp** în tablouri de bord, grila nu utilizează lățimea completă a containerului grilei tabloului de bord.</span><span class="sxs-lookup"><span data-stu-id="2d682-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="2d682-116">Pentru anumite zone orare, controlul grilei **Intrare de timp** nu afișează înregistrări.</span><span class="sxs-lookup"><span data-stu-id="2d682-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="2d682-117">Înregistrările orare care sunt după ora 21:00 apar în ziua greșită.</span><span class="sxs-lookup"><span data-stu-id="2d682-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="2d682-118">Utilizatorii nu pot depune cheltuieli dacă categoria de cheltuieli, **Chitanța de cheltuială necesară** nu are nicio valoare.</span><span class="sxs-lookup"><span data-stu-id="2d682-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="2d682-119">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="2d682-119">**Resource Management**</span></span>

<span data-ttu-id="2d682-120">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2d682-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d682-121">Rezervările inactive sunt afișate în vizualizarea **Reconciliere**.</span><span class="sxs-lookup"><span data-stu-id="2d682-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="2d682-122">Lipsa de validare a resurselor generice a lipsit pentru a se asigura că există o stare de rezervare valabilă.</span><span class="sxs-lookup"><span data-stu-id="2d682-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="2d682-123">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="2d682-123">**Project Management**</span></span>

<span data-ttu-id="2d682-124">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2d682-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d682-125">Grilele formularului **Proiect** (**Atribuirea resurselor**, **Activitate**, vizualizarea **Reconciliere**, **Estimarea cheltuielilor**) rămân editabile chiar și atunci când un proiect nu este activ.</span><span class="sxs-lookup"><span data-stu-id="2d682-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="2d682-126">Clienții duplicat nu pot fi îmbinați cu clienții care sunt legați de contractele de proiect confirmate.</span><span class="sxs-lookup"><span data-stu-id="2d682-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="2d682-127">Când se adaugă o resursă care nu are un calendar valid, sistemul nu returnează un mesaj de eroare de utilizator.</span><span class="sxs-lookup"><span data-stu-id="2d682-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="2d682-128">Butonul **Adăugați activitate** de pe grila de activități este activat atunci când proiectul este conectat **Program de completare Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="2d682-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="2d682-129">Efortul crește incontrolabil atunci când o sarcină cu o categorie este atribuită unei resurse cu un rol pentru care este definit un preț de cost.</span><span class="sxs-lookup"><span data-stu-id="2d682-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="2d682-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2d682-130">**Sales**</span></span>

<span data-ttu-id="2d682-131">Au fost realizate următoarele îmbunătățiri:</span><span class="sxs-lookup"><span data-stu-id="2d682-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="2d682-132">**Frecvența facturilor** și **Startul facturării** au fost mutați în fila **Planificarea facturilor**.</span><span class="sxs-lookup"><span data-stu-id="2d682-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="2d682-133">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2d682-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="2d682-134">**Preț total de vânzare** este zero (0) pentru **Categorie** chiar dacă **Rol** are un preț total de vânzare care nu este zero.</span><span class="sxs-lookup"><span data-stu-id="2d682-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="2d682-135">Clienții nu pot modifica valoarea câmpului **Starea facturii** la **Gata pentru facturare** când un alt proces personalizat actualizează un câmp suplimentar.</span><span class="sxs-lookup"><span data-stu-id="2d682-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="2d682-136">Butonul **Actualizați liniile de factură** poate crea mai multe linii duplicate dacă este selectat în mod repetat.</span><span class="sxs-lookup"><span data-stu-id="2d682-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="2d682-137">Butonul **Actualizați prețurile** nu funcționează pe subgrila **Prețurile rolului** în formularul **Vizualizare rapidă**.</span><span class="sxs-lookup"><span data-stu-id="2d682-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="2d682-138">Logica **Rezolvare listă prețuri de vânzare** gestionează în mod necorespunzător zonele orare, rezultând în selecția incorectă a listelor de prețuri.</span><span class="sxs-lookup"><span data-stu-id="2d682-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="2d682-139">**Costul real total** al unui proiect poate fi decalat cu o sumă fracționată după aprobarea unei singure intrări.</span><span class="sxs-lookup"><span data-stu-id="2d682-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="2d682-140">Logica **Rezoluția prețurilor** nu oferă un mesaj de eroare ușor de utilizat dacă **Preluare RolePrice** nu are valori în câmpurile **„Unitate primară”** și **„Preț în unitatea primară”**.</span><span class="sxs-lookup"><span data-stu-id="2d682-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]