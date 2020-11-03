---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 17, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082752"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="e43ff-103">Project Service Automation, versiunea actualizată 17, V3</span><span class="sxs-lookup"><span data-stu-id="e43ff-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="e43ff-104">Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e43ff-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e43ff-105">Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.</span><span class="sxs-lookup"><span data-stu-id="e43ff-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="e43ff-106">Această versiune este compatibilă cu Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e43ff-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e43ff-107">Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea.</span><span class="sxs-lookup"><span data-stu-id="e43ff-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e43ff-108">Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e43ff-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e43ff-109">Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 17.</span><span class="sxs-lookup"><span data-stu-id="e43ff-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="e43ff-110">Această versiune are un număr de V3.10.6.34 și este, în general, disponibilă printr-o auto-actualizare în martie 2020.</span><span class="sxs-lookup"><span data-stu-id="e43ff-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="e43ff-111">Lansarea de actualizări 17</span><span class="sxs-lookup"><span data-stu-id="e43ff-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e43ff-112">Remedieri de erori</span><span class="sxs-lookup"><span data-stu-id="e43ff-112">Bug fixes</span></span>

<span data-ttu-id="e43ff-113">**General**</span><span class="sxs-lookup"><span data-stu-id="e43ff-113">**General**</span></span>

- <span data-ttu-id="e43ff-114">Soluționat: Actualizați Project Service Automation pentru a implementa licențele pentru membrii echipei (Hub-ul de resurse al proiectului va include metadatele planului de servicii pentru membrii echipei 3.x)</span><span class="sxs-lookup"><span data-stu-id="e43ff-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="e43ff-115">**Timp și cheltuială**</span><span class="sxs-lookup"><span data-stu-id="e43ff-115">**Time and Expense**</span></span>

- <span data-ttu-id="e43ff-116">Soluționat: nu este posibilă modificarea unei estimări a cheltuielilor de la un preț diferit de zero la zero (0).</span><span class="sxs-lookup"><span data-stu-id="e43ff-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="e43ff-117">Modificarea este ignorată.</span><span class="sxs-lookup"><span data-stu-id="e43ff-117">The change is ignored.</span></span>

<span data-ttu-id="e43ff-118">**Gestionare de proiect**</span><span class="sxs-lookup"><span data-stu-id="e43ff-118">**Project Management**</span></span>

- <span data-ttu-id="e43ff-119">Soluționat: S-a adăugat o verificare a valorilor nule pe numele poziției unui membru al echipei.</span><span class="sxs-lookup"><span data-stu-id="e43ff-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="e43ff-120">Soluționat: câmpul **msdyn_userresourceid** din entitatea **msdyn_resourceassignment** a fost perimat.</span><span class="sxs-lookup"><span data-stu-id="e43ff-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="e43ff-121">Soluționat: Upgrade-ul de la 2.x la 3.x gestionează acum contururile de efort goale în atribuirile de activități.</span><span class="sxs-lookup"><span data-stu-id="e43ff-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="e43ff-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e43ff-122">**Sales**</span></span>

- <span data-ttu-id="e43ff-123">Soluționat: **Invoice.PreValidateInvoiceUpdate** gestionează acum scenariul realocării proprietarilor de înregistrări în mod corespunzător.</span><span class="sxs-lookup"><span data-stu-id="e43ff-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="e43ff-124">Soluționat: Când clasa de tranzacție este **Timp** , **UnitGroup** este needitabil pentru toate entitățile inclusiv, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , și **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e43ff-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="e43ff-125">În orice caz, **Unitate** este needitabil doar pentru **JournalLine** și **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e43ff-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


