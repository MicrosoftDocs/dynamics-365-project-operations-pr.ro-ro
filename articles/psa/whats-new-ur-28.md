---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 28, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 28, V3.
author: ruhercul
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010531"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="ef7a9-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 28, V3</span><span class="sxs-lookup"><span data-stu-id="ef7a9-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ef7a9-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ef7a9-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ef7a9-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ef7a9-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ef7a9-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ef7a9-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ef7a9-109">Acest subiect listează caracteristicile și corecțiile noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 28 Această versiune are un număr de compilare de V3.10.46.32 și este, în general, disponibilă prin auto-actualizare în ianuarie 2021.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="ef7a9-110">Lansarea de actualizări 28</span><span class="sxs-lookup"><span data-stu-id="ef7a9-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ef7a9-111">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="ef7a9-111">Bug fixes</span></span>

<span data-ttu-id="ef7a9-112">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="ef7a9-112">**Time and Expense**</span></span>

<span data-ttu-id="ef7a9-113">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="ef7a9-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="ef7a9-114">Utilizatorii pot folosi funcția **Editare în bloc** pentru a actualiza intrările de timp care au fost aprobate și trimise.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="ef7a9-115">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="ef7a9-115">**Project Management**</span></span>

<span data-ttu-id="ef7a9-116">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="ef7a9-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="ef7a9-117">În cazurile în care sarcina GUID este interpretat ca un număr, sarcinile nu pot fi deschise pentru editare folosind comanda **Editați sarcina** de pe panglica de la pagina **Structura defalcării lucrului**.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="ef7a9-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ef7a9-118">**Sales**</span></span>

<span data-ttu-id="ef7a9-119">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="ef7a9-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="ef7a9-120">O excepție de referință nulă este generată atunci când insertul **ObținețiEstimăriPentruProiect** este invocat.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="ef7a9-121">Comanda **Marcați gata de facturare** pe grila de repere actualizează doar parțial atributele, cu excepția atributului **Stare factură**, care este actualizat.</span><span class="sxs-lookup"><span data-stu-id="ef7a9-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]