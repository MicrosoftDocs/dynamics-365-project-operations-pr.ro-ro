---
title: Furnizați estimări de lucru pentru un proiect în timpul procesului de vânzare
description: Cum să furnizați estimări de lucru pentru un proiect în timpul procesului de vânzări în Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120603"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="65c7b-103">Furnizați estimări de lucru pentru un proiect în timpul procesului de vânzare (Project Service)</span><span class="sxs-lookup"><span data-stu-id="65c7b-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="65c7b-104">În timpul procesului de vânzare, puteți efectua estimări de vânzări de la zero cu linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="65c7b-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="65c7b-105">Capacitățile de servicii de proiecte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] din [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] oferă o modalitate mai științifică și mai deterministă de a realiza estimări de vânzare prin defalcarea elementelor de lucru și asocierea de atribute relevante care contribuie la estimările privind proiectul în structura detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="65c7b-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="65c7b-106">Odată ce ați câștigat vânzarea, puteți utiliza structura detaliată a proiectului în planul de proiect, rafinând-o după cum este necesar pentru o finalizare cu succes a proiectului.</span><span class="sxs-lookup"><span data-stu-id="65c7b-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="65c7b-107">Legați un proiect la o linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="65c7b-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="65c7b-108">Atunci când creați o linie de ofertă pe baza proiectului, puteți să creați un proiect nou din linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="65c7b-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="65c7b-109">Puteți utiliza apoi șabloane de proiect, care sunt fie planuri de proiect standard preconfigurate și estimări financiare comune organizației dumneavoastră, fie o copie a unui plan de proiect și estimări de la un proiect de trecut.</span><span class="sxs-lookup"><span data-stu-id="65c7b-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="65c7b-110">Atunci când creați un proiect, alegerea unui șablon de proiect oferă o bază pentru a rafina planul de proiect, estimări și cerințe de rol.</span><span class="sxs-lookup"><span data-stu-id="65c7b-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="65c7b-111">Prin crearea proiectului din ofertă, proiectul este asociat automat cu linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="65c7b-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="65c7b-112">Componente estimării de proiect</span><span class="sxs-lookup"><span data-stu-id="65c7b-112">Project estimate components</span></span>  
 <span data-ttu-id="65c7b-113">Structură detaliată a proiectului dintr-un proiect oferă o modalitate de a împărți proiectul în activități, de a menține o ierarhie de activități și de a atribui o estimare a efortului necesar pentru a finaliza fiecare activitate.</span><span class="sxs-lookup"><span data-stu-id="65c7b-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="65c7b-114">De asemenea, puteți asocia roluri la o activitate, pentru a indica o estimare a tipului de resursă necesar pentru a finaliza o activitate și un program.</span><span class="sxs-lookup"><span data-stu-id="65c7b-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="65c7b-115">Structură detaliată a proiectului vă ajută să determinați efortul de lucru și estimările de planificare.</span><span class="sxs-lookup"><span data-stu-id="65c7b-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="65c7b-116">În mod implicit, proiectul utilizează liste de prețuri implicite pe care le-ați definit anterior.</span><span class="sxs-lookup"><span data-stu-id="65c7b-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="65c7b-117">Costurile și prețurile de vânzări definite în listele de prețuri vă ajută să determinați estimările financiare pentru componentele de lucru ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="65c7b-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="65c7b-118">Dacă proiectul dumneavoastră este asociat cu o ofertă, iar oferta are o altă listă de prețuri decât cea implicită, lista de prețuri a ofertei este folosită pentru estimări financiare.</span><span class="sxs-lookup"><span data-stu-id="65c7b-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="65c7b-119">Importați estimările dintr-un proiect într-o ofertă</span><span class="sxs-lookup"><span data-stu-id="65c7b-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="65c7b-120">După ce aveți estimările de proiect în proiect, aveți posibilitatea să importați aceste estimări în linia de ofertă:</span><span class="sxs-lookup"><span data-stu-id="65c7b-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="65c7b-121">În **Detalii linie de ofertă**, faceți clic pe **Import de la estimări**.</span><span class="sxs-lookup"><span data-stu-id="65c7b-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="65c7b-122">Selectați dacă să importați estimările proiectului rezumate după tipul tranzacției, rol sau nivel de nod de structură detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="65c7b-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="65c7b-123">Consultați și</span><span class="sxs-lookup"><span data-stu-id="65c7b-123">See Also</span></span>  
 [<span data-ttu-id="65c7b-124">Ghidul Managerului de proiect</span><span class="sxs-lookup"><span data-stu-id="65c7b-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
