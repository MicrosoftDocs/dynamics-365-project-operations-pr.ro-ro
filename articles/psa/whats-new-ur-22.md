---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 22, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 22, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082744"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="0e51f-103">Project Service Automation, versiunea actualizată 22, V3</span><span class="sxs-lookup"><span data-stu-id="0e51f-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="0e51f-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0e51f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0e51f-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="0e51f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0e51f-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0e51f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0e51f-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="0e51f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0e51f-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0e51f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0e51f-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 22.</span><span class="sxs-lookup"><span data-stu-id="0e51f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="0e51f-110">Această versiune are un număr de versiune V 3.10.33.48 și este disponibil în general printr-o autoactualizare în iunie 2020.</span><span class="sxs-lookup"><span data-stu-id="0e51f-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="0e51f-111">Lansarea de actualizări 22</span><span class="sxs-lookup"><span data-stu-id="0e51f-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0e51f-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="0e51f-112">Bug fixes</span></span>



<span data-ttu-id="0e51f-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="0e51f-113">**Time and Expense**</span></span>

<span data-ttu-id="0e51f-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="0e51f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="0e51f-115">**Intrările de timp** nu sunt adăugate automat în planificarea de intrări de timp după import.</span><span class="sxs-lookup"><span data-stu-id="0e51f-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="0e51f-116">Selectorul de date grilă **Intrare de timp** nu recunoaște setările regionale ale unui utilizator.</span><span class="sxs-lookup"><span data-stu-id="0e51f-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="0e51f-117">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="0e51f-117">**Resource Management**</span></span>

<span data-ttu-id="0e51f-118">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="0e51f-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="0e51f-119">În modul manual, modificările la contururile **Alocarea resurselor** nu sunt recunoscute când se generează **Cerințe de resurse**.</span><span class="sxs-lookup"><span data-stu-id="0e51f-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="0e51f-120">**Solicitări de resurse** nu acceptă stări de solicitare personalizate.</span><span class="sxs-lookup"><span data-stu-id="0e51f-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="0e51f-121">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="0e51f-121">**Project Management**</span></span>

<span data-ttu-id="0e51f-122">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="0e51f-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="0e51f-123">Utilizând dublu clic pe EstimateGridControl nu va analiza corect numerele formatului olandez.</span><span class="sxs-lookup"><span data-stu-id="0e51f-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="0e51f-124">Orele alocate nu se actualizează corect atunci când alocările sunt schimbate folosind suplimentul client de desktop Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="0e51f-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="0e51f-125">Rețelele de urmărire și estimare a proiectului afișează cod de monedă de vânzare incorect atunci când moneda contractului este diferită de moneda clientului și organizația este configurată pentru a afișa coduri valutare în loc de simboluri valutare.</span><span class="sxs-lookup"><span data-stu-id="0e51f-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="0e51f-126">Data de încheiere a unui membru al echipei va adăuga o zi dacă programul orelor de lucru este de 24 de ore pe zi.</span><span class="sxs-lookup"><span data-stu-id="0e51f-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="0e51f-127">Pe Planificarea de proiect, adăugarea unei categorii de tranzacții la o sarcină nu declanșează salvarea automată.</span><span class="sxs-lookup"><span data-stu-id="0e51f-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="0e51f-128">Următoarea eroare este afișată la adăugarea unui membru al echipei la șablonul de proiect: „Cerințele de resurse nu pot fi asociate cu șabloanele de proiect”.</span><span class="sxs-lookup"><span data-stu-id="0e51f-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="0e51f-129">Scriptul de regulă al panglicii „msdyn.Approval.CanApproveOrReject” afișează o eroare de expirare.</span><span class="sxs-lookup"><span data-stu-id="0e51f-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="0e51f-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0e51f-130">**Sales**</span></span>

<span data-ttu-id="0e51f-131">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="0e51f-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="0e51f-132">Mesaj de eroare de validare care nu este afișat atunci când este selectată o listă de prețuri de costuri în căutarea Listă de prețuri în formularul/entitatea „Ofertă nouă de preț de proiect”.</span><span class="sxs-lookup"><span data-stu-id="0e51f-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="0e51f-133">Închiderea ofertei ca câștigată nu navighează la contractul creat dacă un BPF atașat la ofertă se află în etapa finală.</span><span class="sxs-lookup"><span data-stu-id="0e51f-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="0e51f-134">Reversul **Vânzări fără factură** este legat de costul inițial atunci când este înregistrată o intrare în timp.</span><span class="sxs-lookup"><span data-stu-id="0e51f-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="0e51f-135">După selectarea butonului **Confirmare** , starea facturii nu se modifică la **Confirmat** cu excepția cazului în care factura este actualizată.</span><span class="sxs-lookup"><span data-stu-id="0e51f-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
