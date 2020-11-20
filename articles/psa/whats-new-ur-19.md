---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 19, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126857"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="857ec-103">Project Service Automation, versiunea actualizată 19, V3</span><span class="sxs-lookup"><span data-stu-id="857ec-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="857ec-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="857ec-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="857ec-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="857ec-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="857ec-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="857ec-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="857ec-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="857ec-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="857ec-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="857ec-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="857ec-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 19.</span><span class="sxs-lookup"><span data-stu-id="857ec-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="857ec-110">Această versiune are un număr de versiune V3.10.30.41 și este disponibil în general printr-o autoactualizare în mai 2020.</span><span class="sxs-lookup"><span data-stu-id="857ec-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="857ec-111">Lansarea de actualizări 19</span><span class="sxs-lookup"><span data-stu-id="857ec-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="857ec-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="857ec-112">Bug fixes</span></span>

<span data-ttu-id="857ec-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="857ec-113">**Time and Expense**</span></span>

<span data-ttu-id="857ec-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="857ec-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="857ec-115">Erorile derivate din importurile de intrare temporale nu sunt descoperite corect.</span><span class="sxs-lookup"><span data-stu-id="857ec-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="857ec-116">Grila de intrare în timp nu acceptă formatul câmpului **Numai dată**.</span><span class="sxs-lookup"><span data-stu-id="857ec-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="857ec-117">Resursele proiectului nu pot crea o cheltuială cu un proiect.</span><span class="sxs-lookup"><span data-stu-id="857ec-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="857ec-118">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="857ec-118">**Project Management**</span></span>

<span data-ttu-id="857ec-119">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="857ec-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="857ec-120">Sarcina secundară de nivelul II determină o estimare incorectă a efortului în timpul calculului finalizării (EAC).</span><span class="sxs-lookup"><span data-stu-id="857ec-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="857ec-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="857ec-121">**Sales**</span></span>

<span data-ttu-id="857ec-122">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="857ec-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="857ec-123">Acțiunea **Recalculare** nu funcționează cu detaliile liniei contractului de cheltuieli sau cu detaliile liniei de ofertă.</span><span class="sxs-lookup"><span data-stu-id="857ec-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="857ec-124">La **Actualizați prețurile** lipsesc estimările cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="857ec-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="857ec-125">Clienții nu sunt în măsură să selecteze motivele statutului personalizat ale contractului din pagina **Contract de proiect**.</span><span class="sxs-lookup"><span data-stu-id="857ec-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="857ec-126">Clienții experimentează performanțe degradate atunci când creează o listă de prețuri personalizate dintr-o ofertă.</span><span class="sxs-lookup"><span data-stu-id="857ec-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="857ec-127">Clienții se confruntă cu inconsistența valorii **unitate** implicte pe **Detalii despre linie de ofertă** și pagini **Detalii linie contract**.</span><span class="sxs-lookup"><span data-stu-id="857ec-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="857ec-128">Adăugarea de articole din categoria de tranzacții care nu sunt exigibile la o linie de contract exigibilă nu va respecta tipul de facturare **Neaplicabil** al categoriei tranzacției.</span><span class="sxs-lookup"><span data-stu-id="857ec-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="857ec-129">Clienții nu pot utiliza rolurile și categoria nou adăugate la contractele create anterior.</span><span class="sxs-lookup"><span data-stu-id="857ec-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="857ec-130">Clienții experimentează performanțe degradate Necesarul de regăsire în PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="857ec-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="857ec-131">Rolurile sunt stabilite ca neimpozabile în lista **Categorii de resurse** ar trebui adăugată la fila **Roluri tarifabile** ca **Neaplicabil** pe linia contractului pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="857ec-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="857ec-132">Clienții pot experimenta performanțe degradate atunci când creează un proiect deoarece **GetBookableResourceIdFromUser** preia toate coloanele de resurse rezervabile în loc de doar ID-ul primar.</span><span class="sxs-lookup"><span data-stu-id="857ec-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="857ec-133">Entitatea **TransactionType** de unde lipsește insertul de actualizare a pre-validării pentru a împiedica accesul utilizatorilor **Unități** și **UnitGroups** care nu sunt valabile pentru tipurile de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="857ec-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="857ec-134">Pasul **Elimină** nu funcționează pentru importul de intrare în timp.</span><span class="sxs-lookup"><span data-stu-id="857ec-134">The **Remove** step does not work for time entry import.</span></span>
