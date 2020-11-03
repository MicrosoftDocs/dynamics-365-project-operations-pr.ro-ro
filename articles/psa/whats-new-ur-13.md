---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 13, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 13, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082756"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="b3893-103">Project Service Automation, versiunea actualizată 13, V3</span><span class="sxs-lookup"><span data-stu-id="b3893-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="b3893-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b3893-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b3893-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="b3893-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b3893-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b3893-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b3893-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="b3893-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b3893-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b3893-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b3893-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 13.</span><span class="sxs-lookup"><span data-stu-id="b3893-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="b3893-110">Această versiune are un număr de V3.10.3.18 și este disponibilă în următoarea planificare:</span><span class="sxs-lookup"><span data-stu-id="b3893-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="b3893-111">**Disponibilitate generală (autoactualizare):** noiembrie 2019</span><span class="sxs-lookup"><span data-stu-id="b3893-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="b3893-112">**Auto-actualizare:** decembrie 2019</span><span class="sxs-lookup"><span data-stu-id="b3893-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="b3893-113">Lansarea de actualizări 13</span><span class="sxs-lookup"><span data-stu-id="b3893-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="b3893-114">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="b3893-114">Bug fixes</span></span>

- <span data-ttu-id="b3893-115">Timp și cheltuială</span><span class="sxs-lookup"><span data-stu-id="b3893-115">Time and Expense</span></span>

     - <span data-ttu-id="b3893-116">Remediat: funcționalitatea de căutare pe pagina **Aprobarea cheltuielilor** nu funcționează atunci când căutați după scopul cheltuielii.</span><span class="sxs-lookup"><span data-stu-id="b3893-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="b3893-117">Gestionarea de resurse</span><span class="sxs-lookup"><span data-stu-id="b3893-117">Resource Management</span></span>

     - <span data-ttu-id="b3893-118">Remediat: Numerele de reconciliere au fost actualizate pentru a fi justificate corect.</span><span class="sxs-lookup"><span data-stu-id="b3893-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="b3893-119">Remediat: Resurse denumite nu pot fi atribuite sarcinilor prin intermediul filei **Planificare**.</span><span class="sxs-lookup"><span data-stu-id="b3893-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="b3893-120">Gestionare de proiect</span><span class="sxs-lookup"><span data-stu-id="b3893-120">Project Management</span></span>

     - <span data-ttu-id="b3893-121">Remediat: excepție de referință nulă la atribuirea unui membru al echipei atunci când din **Tipul tranzacției** lipsesc informațiile de configurare pentru **Unitate** și **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="b3893-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="b3893-122">Sales</span><span class="sxs-lookup"><span data-stu-id="b3893-122">Sales</span></span>

     - <span data-ttu-id="b3893-123">Remediat: înregistrările de tipul de tranzacție duplicat returnează o eroare atunci când sunt create înregistrările de prețuri de rol.</span><span class="sxs-lookup"><span data-stu-id="b3893-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="b3893-124">Remediat: Butoane suplimentare pentru **Oportunitate nouă** , **Ofertă** , **Linie de comandă** și **Adaugă produs** sunt vizibile în comenzile pentru Oportunități, Oferte, Produse pentru Comandă și sub-rețeaua Linii bazate pe proiect.</span><span class="sxs-lookup"><span data-stu-id="b3893-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


