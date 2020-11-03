---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 14, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 14 V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082754"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="e5b03-103">Project Service Automation, versiunea actualizată 14, V3</span><span class="sxs-lookup"><span data-stu-id="e5b03-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="e5b03-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e5b03-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e5b03-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="e5b03-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e5b03-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e5b03-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e5b03-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="e5b03-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e5b03-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e5b03-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e5b03-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 14.</span><span class="sxs-lookup"><span data-stu-id="e5b03-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="e5b03-110">Această versiune are un număr de V3.10.4.21 și este disponibilă în următoarea planificare:</span><span class="sxs-lookup"><span data-stu-id="e5b03-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="e5b03-111">**Disponibilitate generală (autoactualizare):** ianuarie 2020</span><span class="sxs-lookup"><span data-stu-id="e5b03-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="e5b03-112">**Actualizare automată:** februarie 2020</span><span class="sxs-lookup"><span data-stu-id="e5b03-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="e5b03-113">Lansarea de actualizări 14</span><span class="sxs-lookup"><span data-stu-id="e5b03-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="e5b03-114">Îmbunătățiri</span><span class="sxs-lookup"><span data-stu-id="e5b03-114">Enhancements</span></span>

- <span data-ttu-id="e5b03-115">Sales</span><span class="sxs-lookup"><span data-stu-id="e5b03-115">Sales</span></span>

     - <span data-ttu-id="e5b03-116">Valorile câmpului personalizate din **Detalii despre linie de ofertă** sunt copiate în **Detalii linie contract contract** când o ofertă este actualizată la **Închisă drept câștigată**.</span><span class="sxs-lookup"><span data-stu-id="e5b03-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="e5b03-117">Proiectele confirmate pot fi **Închise ca pierdute**.</span><span class="sxs-lookup"><span data-stu-id="e5b03-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="e5b03-118">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="e5b03-118">Resource Management</span></span>

     - <span data-ttu-id="e5b03-119">Când extindeți rezervările, utilizatorii vor primi o casetă de dialog de confirmare pentru a rezuma rezultatele rezervării și pentru a oferi un link către Menținerea rezervărilor.</span><span class="sxs-lookup"><span data-stu-id="e5b03-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="e5b03-120">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="e5b03-120">Bug fixes</span></span>

- <span data-ttu-id="e5b03-121">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="e5b03-121">Time and Expense</span></span>

     - <span data-ttu-id="e5b03-122">Remediat: experiența îmbunătățită a utilizatorului atunci când acesta nu a selectat nicio înregistrare care trebuie corectată.</span><span class="sxs-lookup"><span data-stu-id="e5b03-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="e5b03-123">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="e5b03-123">Resource Management</span></span>

     - <span data-ttu-id="e5b03-124">Remediat: Rezervarea unei resurse de mai multe ori revărsă numele resursei rezervabile.</span><span class="sxs-lookup"><span data-stu-id="e5b03-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="e5b03-125">Sales</span><span class="sxs-lookup"><span data-stu-id="e5b03-125">Sales</span></span>

     - <span data-ttu-id="e5b03-126">Remediat: prețul total de vânzare nu este calculat până când utilizatorul introduce și un preț de cost pentru estimările cheltuielilor la un proiect.</span><span class="sxs-lookup"><span data-stu-id="e5b03-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="e5b03-127">Remediat: Închiderea unei oferte ca **Câștigată** eșuează dacă contractul de proiect asociat nu se află într-o stare de **Schiță**.</span><span class="sxs-lookup"><span data-stu-id="e5b03-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

