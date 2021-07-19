---
title: Prezentare generală a implementării Project Operations pentru scenarii bazate pe stoc/producție
description: Acest subiect oferă informații despre tipul de implementare, Project Operations pentru scenarii stocate/bazate pe producție.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 71fd9d3ae30147c3c03202a54f74477a95838eb9
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369526"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="be417-103">Prezentare generală a implementării Project Operations pentru scenarii bazate pe stoc/producție</span><span class="sxs-lookup"><span data-stu-id="be417-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="be417-104">_**Se aplică la:** Project Operations pentru scenariile bazate pe stocuri/producție_</span><span class="sxs-lookup"><span data-stu-id="be417-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="be417-105">Acest tip de implementare are următoarele funcții pentru companiile bazate pe proiecte:</span><span class="sxs-lookup"><span data-stu-id="be417-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="be417-106">Planificarea proiectului folosind [Structuri de defalcare a proiectului](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="be417-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="be417-107">Achiziționați și consumați inventar stocat pentru proiecte</span><span class="sxs-lookup"><span data-stu-id="be417-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="be417-108">Gestionarea vânzărilor bazate pe proiecte folosind modulul **Vânzări și marketing** în aplicații Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="be417-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="be417-109">Prețuri și costuri ale proiectului utilizând configurația ratei costurilor și a ratei facturilor din aplicații Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="be417-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="be417-110">Gestionarea resurselor pentru proiecte în aplicații Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="be417-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="be417-111">Progresul proiectului și urmărirea timpului în aplicații Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="be417-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="be417-112">Experiențe de gestionare a cheltuielilor pentru cheltuieli de proiect și non-proiect cu captarea de chitanțe utilizând capacitățile OCR</span><span class="sxs-lookup"><span data-stu-id="be417-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="be417-113">Facturarea utilizând un sistem de impozite pe vânzări la nivel de întreprindere și un sistem de rate de schimb eficiente în funcție de dată</span><span class="sxs-lookup"><span data-stu-id="be417-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="be417-114">Grupuri de proiecte configurabile pentru contabilitate și acumulări WIP</span><span class="sxs-lookup"><span data-stu-id="be417-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="be417-115">Recunoașterea veniturilor din proiecte</span><span class="sxs-lookup"><span data-stu-id="be417-115">Project revenue recognition</span></span>

<span data-ttu-id="be417-116">Acest tip de implementare oferă, de asemenea, o extensie la funcționalitatea oferită de aplicațiile Dynamics 365 Finance și Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="be417-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="be417-117">Selectați acest tip de implementare pentru a utiliza Dynamics 365 Project Operations pentru ciclul de viață complet al proiectului, inclusiv următoarele cerințe cheie:</span><span class="sxs-lookup"><span data-stu-id="be417-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="be417-118">Un sistem extins de gestionare a proiectelor care gestionează articole inventariate și costuri de comandă/producție pentru proiecte interne și facturabile pentru programe și situații financiare.</span><span class="sxs-lookup"><span data-stu-id="be417-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="be417-119">Organizația are deja Dynamics 365 Finance sau aplicațiile Dynamics 365 Supply Chain și Manufacturing și integrarea tranzacțiilor bazate pe proiecte vor simplifica accesul la date și nevoile de raportare.</span><span class="sxs-lookup"><span data-stu-id="be417-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="be417-120">Un sistem de gestionare a cheltuielilor complet funcțional care include aplicarea politicilor și rambursările pentru urmărirea cheltuielilor de proiect și non-proiect.</span><span class="sxs-lookup"><span data-stu-id="be417-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="be417-121">Un motor de impozitare pe vânzări și un curs de schimb pentru a genera facturi orientate către clienți pentru proiecte.</span><span class="sxs-lookup"><span data-stu-id="be417-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="be417-122">Un sistem de contabilitate a proiectelor și de recunoaștere a veniturilor conform standardelor internaționale de raportare financiară (IFRS).</span><span class="sxs-lookup"><span data-stu-id="be417-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]