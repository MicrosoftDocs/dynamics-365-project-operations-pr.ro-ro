---
title: Ce este nou în Project Service Automation versiunea actualizată 12, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754746"
---
# <a name="project-service-automation-v3-update-release-12"></a><span data-ttu-id="6999e-103">Project Service Automation V3, versiunea actualizată 12</span><span class="sxs-lookup"><span data-stu-id="6999e-103">Project Service Automation V3, Update Release 12</span></span>
<span data-ttu-id="6999e-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6999e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6999e-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="6999e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6999e-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6999e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6999e-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="6999e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6999e-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6999e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6999e-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 12.</span><span class="sxs-lookup"><span data-stu-id="6999e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="6999e-110">Această versiune are un număr de V3.10.2.34 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2019.</span><span class="sxs-lookup"><span data-stu-id="6999e-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="6999e-111">Lansarea de actualizări 12</span><span class="sxs-lookup"><span data-stu-id="6999e-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6999e-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="6999e-112">Bug fixes</span></span>

- <span data-ttu-id="6999e-113">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="6999e-113">Time and Expense</span></span>

    - <span data-ttu-id="6999e-114">Remediat: Mesajele de eroare la intrarea în timp au fost actualizate cu un context mai relevant.</span><span class="sxs-lookup"><span data-stu-id="6999e-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="6999e-115">Remediat: Grila de intrare a timpului și programul afișează corect bara de defilare verticală când este necesar.</span><span class="sxs-lookup"><span data-stu-id="6999e-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="6999e-116">Remediat: intrările de cost și timp remise pot fi aprobate.</span><span class="sxs-lookup"><span data-stu-id="6999e-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="6999e-117">Remediat: a fost corectat mesajul de dialog de confirmare a aprobării pentru a reflecta starea aprobării la schimbarea din **Aprobat** la **Înscris**.</span><span class="sxs-lookup"><span data-stu-id="6999e-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="6999e-118">Remediat: câmpurile **Preț**, **Unitate** și **Cantitate** sunt acum blocate în înregistrarea cheltuieli după ce a fost aprobată.</span><span class="sxs-lookup"><span data-stu-id="6999e-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="6999e-119">Gestionare de proiect</span><span class="sxs-lookup"><span data-stu-id="6999e-119">Project Management</span></span>

    - <span data-ttu-id="6999e-120">Remediat: formularul principal acțiune **Nou** pe **Membru al echipei** a fost eliminat.</span><span class="sxs-lookup"><span data-stu-id="6999e-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="6999e-121">Remediat: Alocările de resurse au fost actualizate pentru a contoriza erorile de rotunjire inexacte, care duc la o schimbare a datei de încheiere a unei activități.</span><span class="sxs-lookup"><span data-stu-id="6999e-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="6999e-122">Remediat: în grila de sarcini, pentru utilizator vor apărea erori relevante din partea serverului.</span><span class="sxs-lookup"><span data-stu-id="6999e-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="6999e-123">Remediat: Numele membrului echipei este acum redat în selecția persoanelor în sarcină în loc de numele poziției.</span><span class="sxs-lookup"><span data-stu-id="6999e-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="6999e-124">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="6999e-124">Resource Management</span></span>

    - <span data-ttu-id="6999e-125">Remediat: Detaliile privind cerințele de resurse pentru proiectele create dintr-un șablon folosesc acum calendarul de proiect.</span><span class="sxs-lookup"><span data-stu-id="6999e-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="6999e-126">Remediat: Abilitățile și competențele implicit acum de la datele de master de rol la cerința de resursă creată pentru acel rol.</span><span class="sxs-lookup"><span data-stu-id="6999e-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="6999e-127">Sales</span><span class="sxs-lookup"><span data-stu-id="6999e-127">Sales</span></span>

    - <span data-ttu-id="6999e-128">Remediat: ID-uri de duplicare ale obiectului găsite pe formularul **Contract principal**.</span><span class="sxs-lookup"><span data-stu-id="6999e-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="6999e-129">Remediat: Logica a fost actualizată pentru a face vizibilă fila **Analiza ofertelor**, astfel încât să afișeze configurația de metadate a filei.</span><span class="sxs-lookup"><span data-stu-id="6999e-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="6999e-130">Remediat: data contabilității înregistrării efective vine acum de la data intrării timpului/cheltuielilor și nu a datei aprobării.</span><span class="sxs-lookup"><span data-stu-id="6999e-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>
