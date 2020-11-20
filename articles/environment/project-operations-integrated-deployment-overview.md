---
title: Prezentare generală a implementării Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc
description: Acest subiect oferă informații despre tipul de implementare, Project Operations pentru scenarii bazate pe resursă/nestocate.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365587"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="2db2c-103">Prezentare generală a implementării Project Operations pentru scenarii de resurse/care nu sunt bazate pe stoc</span><span class="sxs-lookup"><span data-stu-id="2db2c-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="2db2c-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="2db2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2db2c-105">Tipul de implementare, Dynamics 365 Project Operations pentru scenarii bazate pe resurse/scenarii nebazate pe stoc, are următoarele capacități pentru companiile bazate pe proiecte:</span><span class="sxs-lookup"><span data-stu-id="2db2c-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="2db2c-106">Planificarea proiectului utilizând Microsoft Project pentru web</span><span class="sxs-lookup"><span data-stu-id="2db2c-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="2db2c-107">Prețuri și costuri multidimensionale pentru resursele de muncă</span><span class="sxs-lookup"><span data-stu-id="2db2c-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="2db2c-108">Prețuri bazate pe categorii pentru categoriile de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="2db2c-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="2db2c-109">Gestionarea vânzărilor bazate pe proiecte utilizând capabilitățile Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="2db2c-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="2db2c-110">Universal resource scheduling care se integrează cu alte aplicații precum Dynamics 365 Field Service și Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="2db2c-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="2db2c-111">Progresul proiectului și urmărirea timpului</span><span class="sxs-lookup"><span data-stu-id="2db2c-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="2db2c-112">Experiențe de gestionare a cheltuielilor de bază și complete pentru cheltuieli de proiect și non-proiect inclusiv cu captarea de chitanțe utilizând capacitățile OCR</span><span class="sxs-lookup"><span data-stu-id="2db2c-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="2db2c-113">Facturarea care se extinde de la proforma la orientarea către clienți și este susținută de un sistem de impozitare pe vânzări la nivel de întreprindere și un sistem de curs de schimb efectiv la dată.</span><span class="sxs-lookup"><span data-stu-id="2db2c-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="2db2c-114">Costuri proiectabile configurabile, profiluri de venituri și reguli pentru contabilitate și acumulări de lucrări în curs (WIP)</span><span class="sxs-lookup"><span data-stu-id="2db2c-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="2db2c-115">Recunoașterea veniturilor din proiecte</span><span class="sxs-lookup"><span data-stu-id="2db2c-115">Project revenue recognition</span></span>
- <span data-ttu-id="2db2c-116">Extensibilitatea prin Power Platform</span><span class="sxs-lookup"><span data-stu-id="2db2c-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="2db2c-117">Acest tip de implementare oferă o extensie la funcționalitatea oferită de aplicațiile Dynamics 365 Finance și Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2db2c-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="2db2c-118">Această implementare ar trebui să fie aleasă dacă așteptările dvs. de la Project Operations este să utilizați ciclul de viață complet al proiectului care include următoarele cerințe:</span><span class="sxs-lookup"><span data-stu-id="2db2c-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="2db2c-119">Abilitatea de a gestiona vânzările bazate pe proiecte cu alte tipuri de vânzări utilizând funcțiile din aplicația Vânzări.</span><span class="sxs-lookup"><span data-stu-id="2db2c-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="2db2c-120">Un sistem integrat de gestionare a proiectelor care gestionează proiecte interne și facturabile pentru programe și situații financiare, de la vânzările de proiecte până la contabilitate.</span><span class="sxs-lookup"><span data-stu-id="2db2c-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="2db2c-121">Un sistem de gestionare a cheltuielilor care include aplicarea politicilor și rambursările pentru urmărirea cheltuielilor de proiect și non-proiect.</span><span class="sxs-lookup"><span data-stu-id="2db2c-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="2db2c-122">Necesită un motor de impozitare pe vânzări și un curs de schimb pentru a genera facturi orientate către clienți pentru proiecte.</span><span class="sxs-lookup"><span data-stu-id="2db2c-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="2db2c-123">Un sistem de contabilitate a proiectelor și de recunoaștere a veniturilor conform standardelor internaționale de raportare financiară (IFRS).</span><span class="sxs-lookup"><span data-stu-id="2db2c-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="2db2c-124">Aplicații de finanțare sau de Supply Chain Management și integrarea tranzacțiilor bazate pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="2db2c-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
