---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 13, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 7287054c470a44ed1fdc243018ec935fe21a6c4f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147263"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="6a12c-103">Project Service Automation, versiunea actualizată 13, V3</span><span class="sxs-lookup"><span data-stu-id="6a12c-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6a12c-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="6a12c-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="6a12c-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="6a12c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6a12c-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6a12c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6a12c-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="6a12c-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="6a12c-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6a12c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6a12c-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 13.</span><span class="sxs-lookup"><span data-stu-id="6a12c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="6a12c-110">Această versiune are un număr de V3.10.3.18 și este disponibilă în următoarea planificare:</span><span class="sxs-lookup"><span data-stu-id="6a12c-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="6a12c-111">**Disponibilitate generală (autoactualizare):** noiembrie 2019</span><span class="sxs-lookup"><span data-stu-id="6a12c-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="6a12c-112">**Auto-actualizare:** decembrie 2019</span><span class="sxs-lookup"><span data-stu-id="6a12c-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="6a12c-113">Lansarea de actualizări 13</span><span class="sxs-lookup"><span data-stu-id="6a12c-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="6a12c-114">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="6a12c-114">Bug fixes</span></span>

- <span data-ttu-id="6a12c-115">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="6a12c-115">Time and Expense</span></span>

     - <span data-ttu-id="6a12c-116">Remediat: funcționalitatea de căutare pe pagina **Aprobarea cheltuielilor** nu funcționează atunci când căutați după scopul cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="6a12c-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="6a12c-117">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="6a12c-117">Resource Management</span></span>

     - <span data-ttu-id="6a12c-118">Remediat: Numerele de reconciliere au fost actualizate pentru a fi justificate corect.</span><span class="sxs-lookup"><span data-stu-id="6a12c-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="6a12c-119">Remediat: Resurse denumite nu pot fi atribuite sarcinilor prin intermediul filei **Planificare**.</span><span class="sxs-lookup"><span data-stu-id="6a12c-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="6a12c-120">Gestionare de proiect</span><span class="sxs-lookup"><span data-stu-id="6a12c-120">Project Management</span></span>

     - <span data-ttu-id="6a12c-121">Remediat: excepție de referință nulă la atribuirea unui membru al echipei atunci când din **Tipul tranzacției** lipsesc informațiile de configurare pentru **Unitate** și **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="6a12c-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="6a12c-122">Sales</span><span class="sxs-lookup"><span data-stu-id="6a12c-122">Sales</span></span>

     - <span data-ttu-id="6a12c-123">Remediat: înregistrările de tipul de tranzacție duplicat returnează o eroare atunci când sunt create înregistrările de prețuri de rol.</span><span class="sxs-lookup"><span data-stu-id="6a12c-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="6a12c-124">Reparat: butoane suplimentare pentru **Oportunitate nouă**, **Ofertă**, **Linie de comandă** și **Adăugați produs** sunt vizibile în comenzile pentru Oportunități, Oferte, Produse de comandă și subgrila Linii bazate pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="6a12c-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


