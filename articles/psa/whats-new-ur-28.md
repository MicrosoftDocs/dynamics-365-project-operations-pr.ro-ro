---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 28, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280233"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="f8282-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 28, V3</span><span class="sxs-lookup"><span data-stu-id="f8282-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f8282-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f8282-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f8282-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="f8282-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f8282-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f8282-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f8282-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="f8282-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f8282-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f8282-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f8282-109">Acest subiect listează caracteristicile și corecțiile noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 28 Această versiune are un număr de compilare de V3.10.46.32 și este, în general, disponibilă prin auto-actualizare în ianuarie 2021.</span><span class="sxs-lookup"><span data-stu-id="f8282-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="f8282-110">Lansarea de actualizări 28</span><span class="sxs-lookup"><span data-stu-id="f8282-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f8282-111">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="f8282-111">Bug fixes</span></span>

<span data-ttu-id="f8282-112">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="f8282-112">**Time and Expense**</span></span>

<span data-ttu-id="f8282-113">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="f8282-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="f8282-114">Utilizatorii pot folosi funcția **Editare în bloc** pentru a actualiza intrările de timp care au fost aprobate și trimise.</span><span class="sxs-lookup"><span data-stu-id="f8282-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="f8282-115">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="f8282-115">**Project Management**</span></span>

<span data-ttu-id="f8282-116">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="f8282-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="f8282-117">În cazurile în care sarcina GUID este interpretat ca un număr, sarcinile nu pot fi deschise pentru editare folosind comanda **Editați sarcina** de pe panglica de la pagina **Structura defalcării lucrului**.</span><span class="sxs-lookup"><span data-stu-id="f8282-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="f8282-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f8282-118">**Sales**</span></span>

<span data-ttu-id="f8282-119">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="f8282-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="f8282-120">O excepție de referință nulă este generată atunci când insertul **ObținețiEstimăriPentruProiect** este invocat.</span><span class="sxs-lookup"><span data-stu-id="f8282-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="f8282-121">Comanda **Marcați gata de facturare** pe grila de repere actualizează doar parțial atributele, cu excepția atributului **Stare factură**, care este actualizat.</span><span class="sxs-lookup"><span data-stu-id="f8282-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]