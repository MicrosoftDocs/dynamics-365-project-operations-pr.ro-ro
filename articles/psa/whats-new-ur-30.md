---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 30, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010441"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="2c494-103">Ce este nou sau schimbat în Project Service Automation versiunea actualizată 30, V3</span><span class="sxs-lookup"><span data-stu-id="2c494-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2c494-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2c494-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2c494-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="2c494-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2c494-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2c494-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2c494-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="2c494-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2c494-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="2c494-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="2c494-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 30.</span><span class="sxs-lookup"><span data-stu-id="2c494-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="2c494-110">Această versiune are un număr de versiune V3.10.51.61 și este disponibil în general printr-o autoactualizare în aprilie 2021.</span><span class="sxs-lookup"><span data-stu-id="2c494-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="2c494-111">Lansarea de actualizări 30</span><span class="sxs-lookup"><span data-stu-id="2c494-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2c494-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="2c494-112">Bug fixes</span></span>

<span data-ttu-id="2c494-113">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="2c494-113">**Time and Expense**</span></span>

<span data-ttu-id="2c494-114">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2c494-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c494-115">O eroare apare atunci când creați și salvați o intrare de timp pe pagina **Creare rapidă** dacă câmpul **Rol** este eliminat.</span><span class="sxs-lookup"><span data-stu-id="2c494-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="2c494-116">Filtrul de introducere a timpului aplică un operator de filtrare greșit.</span><span class="sxs-lookup"><span data-stu-id="2c494-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="2c494-117">Fișele de timp copiate nu sunt afișate automat când selectați **Copiați săptămâna** pe controlul de intrare a timpului.</span><span class="sxs-lookup"><span data-stu-id="2c494-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="2c494-118">**Gestionarea resurselor**</span><span class="sxs-lookup"><span data-stu-id="2c494-118">**Resource Management**</span></span>

<span data-ttu-id="2c494-119">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2c494-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c494-120">Când extindeți o rezervare, starea rezervării atribuită rezervării hard este incorectă.</span><span class="sxs-lookup"><span data-stu-id="2c494-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="2c494-121">Extinderea unei rezervări respectă starea rezervării definită ca **Angajat** în metadatele de configurare a rezervării.</span><span class="sxs-lookup"><span data-stu-id="2c494-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="2c494-122">Când nu este specificată o stare de rezervare validă, mesajul de eroare nu este localizat corect.</span><span class="sxs-lookup"><span data-stu-id="2c494-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="2c494-123">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="2c494-123">**Project Management**</span></span>

<span data-ttu-id="2c494-124">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2c494-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c494-125">Proiectele nu pot fi create într-o monedă și includ sarcini conexe într-o altă monedă.</span><span class="sxs-lookup"><span data-stu-id="2c494-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="2c494-126">**Vânzări**</span><span class="sxs-lookup"><span data-stu-id="2c494-126">**Sales**</span></span>

<span data-ttu-id="2c494-127">S-au remediat următoarele probleme:</span><span class="sxs-lookup"><span data-stu-id="2c494-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="2c494-128">Când se copiază o listă de prețuri, prețurile nu sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="2c494-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="2c494-129">Închiderea unei cotații ca câștigat eșuează atunci când detaliile despre costuri au o valoare pentru origine.</span><span class="sxs-lookup"><span data-stu-id="2c494-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="2c494-130">Pe entitatea **Activitatea proiectului**, **Cost estimat** a fost redenumit în **Cost planificat (bază)**.</span><span class="sxs-lookup"><span data-stu-id="2c494-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="2c494-131">O excepție de referință nulă este generată atunci când facturile sunt create sau șterse.</span><span class="sxs-lookup"><span data-stu-id="2c494-131">A null reference exception is generated when invoices are created or deleted.</span></span>
