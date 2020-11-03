---
title: Crearea unui șablon de proiect
description: Cum să creați un șablon de proiect în Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082809"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="da997-103">Crearea unui șablon de proiect (Project Service)</span><span class="sxs-lookup"><span data-stu-id="da997-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="da997-104">Șabloanele de proiect vă economisesc timp în cazul în care compania dvs. licitează regulat pentru tipuri similare de proiecte.</span><span class="sxs-lookup"><span data-stu-id="da997-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="da997-105">Acestea oferă un set standard de roluri și ore estimate pentru un tip de proiect.</span><span class="sxs-lookup"><span data-stu-id="da997-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="da997-106">Managerii de cont și managerii de proiect pot crea proiecte bazate pe un șablon de proiect sau pot să copieze șablonul și să creeze unul propriu.</span><span class="sxs-lookup"><span data-stu-id="da997-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="da997-107">Componentele șablonului de proiect</span><span class="sxs-lookup"><span data-stu-id="da997-107">Components of project template</span></span>
 <span data-ttu-id="da997-108">Un șablon de proiect constă în trei componente:</span><span class="sxs-lookup"><span data-stu-id="da997-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="da997-109">**Structura detaliată a proiectului** : O structură de defalcare a proiectului dintr-un șablon de proiect are același set de elemente ca în proiect.</span><span class="sxs-lookup"><span data-stu-id="da997-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="da997-110">Puteți să creați o ierarhie de activități, să asociați roluri la activitate, să definiți atribute de program, să stabiliți dependențe și să vedeți toate datele în Gantt.</span><span class="sxs-lookup"><span data-stu-id="da997-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="da997-111">Structura detaliată a proiectului din șabloanele de proiect acceptă și modurile pentru fiecare activitate.</span><span class="sxs-lookup"><span data-stu-id="da997-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="da997-112">Nu există nici o diferență între un șablon de proiect și un proiect de la crearea programului de lucru.</span><span class="sxs-lookup"><span data-stu-id="da997-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="da997-113">**Estimările de proiect** : estimările de proiect din șabloane funcționează la fel ca în proiecte, cu excepția faptului că listele de prețuri pentru costurile și prețurile de vânzare implicite sunt întotdeauna costurile implicit și listele de prețuri de vânzare definite în parametrii [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="da997-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="da997-114">Restul funcționalității este la fel ca într-un proiect.</span><span class="sxs-lookup"><span data-stu-id="da997-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="da997-115">**Formarea echipei de proiect** : atunci când se formează o echipă de proiect pentru un șablon de proiect, nu se poate rezerva o resursă denumită într-un șablon.</span><span class="sxs-lookup"><span data-stu-id="da997-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="da997-116">Puteți utiliza opțiunea **Generați echipa de proiect** în structura detaliată a proiectului pentru a genera un set de resurse generice.</span><span class="sxs-lookup"><span data-stu-id="da997-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="da997-117">De asemenea, puteți specifica abilitățile și expertizele necesare pentru resursele generice.</span><span class="sxs-lookup"><span data-stu-id="da997-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="da997-118">Nu puteți substitui o resursă generică cu o resursă ce se poate rezerva din șabloanele de proiect.</span><span class="sxs-lookup"><span data-stu-id="da997-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="da997-119">Creați un proiect dintr-un șablon</span><span class="sxs-lookup"><span data-stu-id="da997-119">Create a project from a template</span></span>  
 <span data-ttu-id="da997-120">Puteți crea un proiect dintr-un șablon în următoarele moduri:</span><span class="sxs-lookup"><span data-stu-id="da997-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="da997-121">La crearea unui proiect din ofertă, puteți alege un șablon de proiect în formularul de creare rapidă proiect.</span><span class="sxs-lookup"><span data-stu-id="da997-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="da997-122">Atunci când creați un proiect făcând clic pe **Proiect nou** , formularul de proiect se afișează înainte de a salva înregistrarea.</span><span class="sxs-lookup"><span data-stu-id="da997-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="da997-123">De aici, puteți face clic pe câmpul **Alegeți un șablon** pentru a alege din lista de șabloane de proiect predefinite din organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="da997-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="da997-124">Faceți clic pe **Creați proiectul dintr-un șablon** pe pagina **Șablon de proiect** pentru a crea un proiect din șablon.</span><span class="sxs-lookup"><span data-stu-id="da997-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="da997-125">Copierea componentelor unui șablon într-un proiect</span><span class="sxs-lookup"><span data-stu-id="da997-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="da997-126">Când copiați componentele unui șablon într-un proiect, există câteva lucruri pe care trebuie să le știți.</span><span class="sxs-lookup"><span data-stu-id="da997-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="da997-127">**Copierea unei structuri detaliate a proiectului** : Când copiați structura detaliată a proiectului dintr-un șablon de proiect, dacă proiectul are un alt calendar de proiect decât șablonul, orele de lucru din calendarul proiectului se vor aplica la programul activităților.</span><span class="sxs-lookup"><span data-stu-id="da997-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="da997-128">Acest lucru ajustează planificarea la calendarul proiectului.</span><span class="sxs-lookup"><span data-stu-id="da997-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="da997-129">În mod similar, prima activitate din structura detaliată a proiectului ia data de începere a proiectului, astfel încât restul planificării ierarhice a activităților se actualizează pe baza duratei și a dependențelor specificate în structura de detaliere a proiectului.</span><span class="sxs-lookup"><span data-stu-id="da997-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="da997-130">**Copierea estimărilor de proiect** : Când copiați peste liniile de estimare a proiectului, listele de prețuri sunt actualizate pe baza unității deținătoare a proiectului pentru lista de prețuri de cost și lista de clienți pentru prețul de vânzare.</span><span class="sxs-lookup"><span data-stu-id="da997-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="da997-131">Costul unitar și prețurile de vânzare sunt determinate din aceste liste de prețuri pentru proiectele asociate cu o entitate de vânzări.</span><span class="sxs-lookup"><span data-stu-id="da997-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="da997-132">**Copierea unei echipe de proiect** : Când copiați echipa proiectului din șablon într-un proiect, resursele generice sunt copiate, împreună cu abilitățile și expertizele definite în șablon.</span><span class="sxs-lookup"><span data-stu-id="da997-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="da997-133">Atribuirile de resurse generice sunt păstrate ca în șablonul de proiect.</span><span class="sxs-lookup"><span data-stu-id="da997-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="da997-134">Consultați și</span><span class="sxs-lookup"><span data-stu-id="da997-134">See Also</span></span>  
 [<span data-ttu-id="da997-135">Ghidul Managerului de proiect</span><span class="sxs-lookup"><span data-stu-id="da997-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
