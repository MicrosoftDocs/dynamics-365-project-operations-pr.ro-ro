---
title: Șabloane de proiect
description: Acest subiect furnizează informații despre modul de utilizare a șabloanelor de proiect pentru configurarea rapidă a proiectului.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d9d208ebcef127062428afdadde2c54eb07ea505
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283608"
---
# <a name="project-templates"></a><span data-ttu-id="0c367-103">Șabloane de proiect</span><span class="sxs-lookup"><span data-stu-id="0c367-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0c367-104">Un șablon de proiect este un cadru predefinit care vă ajută să începeți rapid și ușor un proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="0c367-105">Aveți posibilitatea să utilizați un șablon predefinit pentru a crea un proiect nou cu un singur clic.</span><span class="sxs-lookup"><span data-stu-id="0c367-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="0c367-106">În ceea ce privește proiectele, trebuie să definiți cerințele preliminare pentru șabloanele de proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="0c367-107">Trebuie să definiți un calendar de proiect pentru fiecare șablon de proiect, iar rolurile și listele de prețuri trebuie să fie predefinite în organizație, astfel încât componentele șablonului să aibă date utile.</span><span class="sxs-lookup"><span data-stu-id="0c367-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="0c367-108">Un șablon de proiect constă din trei componente: o planificare, estimări de proiect și membri ai echipei de proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="0c367-109">Planificare</span><span class="sxs-lookup"><span data-stu-id="0c367-109">Schedule</span></span>

<span data-ttu-id="0c367-110">O planificare dintr-un șablon de proiect are același set de elemente ca o planificare într-un proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="0c367-111">Puteți să creați o ierarhie de activități, să asociați roluri cu activități, să definiți atribute de program și să configurați dependențe.</span><span class="sxs-lookup"><span data-stu-id="0c367-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="0c367-112">O planificare dintr-un șablon de proiect acceptă, de asemenea, modurile de activitate pentru fiecare activitate.</span><span class="sxs-lookup"><span data-stu-id="0c367-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="0c367-113">Prin urmare, acesta acceptă motorul de planificare.</span><span class="sxs-lookup"><span data-stu-id="0c367-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="0c367-114">Trebuie să asociați un calendar de proiect cu proiectul.</span><span class="sxs-lookup"><span data-stu-id="0c367-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="0c367-115">Când creați o planificare de lucru, nu există nici o diferență între un șablon de proiect și un proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="0c367-116">Estimări de proiect</span><span class="sxs-lookup"><span data-stu-id="0c367-116">Project estimates</span></span>

<span data-ttu-id="0c367-117">Estimările proiectului într-un șablon de proiect funcționează în același mod ca și estimările de proiect într-un proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="0c367-118">Cu toate acestea, costul și prețurile de vânzare sunt extrase din costul implicit și listele de preț de vânzare care sunt definite în parametrii.</span><span class="sxs-lookup"><span data-stu-id="0c367-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="0c367-119">Crearea unui proiect dintr-un șablon</span><span class="sxs-lookup"><span data-stu-id="0c367-119">Creating a project from a template</span></span>
 
<span data-ttu-id="0c367-120">Există mai multe modalități de a crea un proiect dintr-un șablon de proiect:</span><span class="sxs-lookup"><span data-stu-id="0c367-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="0c367-121">Când creați un proiect dintr-o ofertă, puteți selecta un șablon de proiect în caseta de dialog **Creare rapidă: proiect**.</span><span class="sxs-lookup"><span data-stu-id="0c367-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Creare rapidă: casetă de dialog proiect](media/project-11.png)

- <span data-ttu-id="0c367-123">Când creați un proiect selectând **Proiect nou**, pagina **Proiect** apare înainte ca înregistrarea să fie salvată.</span><span class="sxs-lookup"><span data-stu-id="0c367-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="0c367-124">În câmpul **Alegeți un șablon**, selectați unul dintre șabloanele de proiect predefinite din organizație.</span><span class="sxs-lookup"><span data-stu-id="0c367-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="0c367-125">Utilizați **Creare proiect dintr-un șablon** de pe pagina **Entitate șablon**.</span><span class="sxs-lookup"><span data-stu-id="0c367-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="0c367-126">Copierea componentelor unui șablon în proiect</span><span class="sxs-lookup"><span data-stu-id="0c367-126">Copying components of template to project</span></span>

<span data-ttu-id="0c367-127">Când copiați componentele unui șablon de proiect la un proiect, câteva suprascrieri pot apărea, în funcție de setările din proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="0c367-128">Copierea planificării</span><span class="sxs-lookup"><span data-stu-id="0c367-128">Copying the schedule</span></span>

<span data-ttu-id="0c367-129">Când copiați planificarea dintr-un șablon de proiect, dacă proiectul are un alt calendar de proiect decât șablonul, orele de lucru din calendarul proiectului se aplică la planificarea activităților.</span><span class="sxs-lookup"><span data-stu-id="0c367-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="0c367-130">Astfel, planificarea este ajustată ca să se potrivească cu calendarul proiectului de rezervă.</span><span class="sxs-lookup"><span data-stu-id="0c367-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="0c367-131">În mod similar, prima activitate din planificare ia data de începere a proiectului, iar restul planificării ierarhice a activităților se actualizează pe baza duratei și a dependențelor care sunt specificate în șablon.</span><span class="sxs-lookup"><span data-stu-id="0c367-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="0c367-132">Copierea estimărilor de proiect</span><span class="sxs-lookup"><span data-stu-id="0c367-132">Copying project estimates</span></span> 

<span data-ttu-id="0c367-133">Când copiați pe linii de estimare proiect, listele de prețuri sunt actualizate.</span><span class="sxs-lookup"><span data-stu-id="0c367-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="0c367-134">Pentru lista de prețuri de cost, aceste actualizări se bazează pe unitatea deținătoare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="0c367-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="0c367-135">Pentru lista de prețuri de vânzări, acestea se bazează pe client.</span><span class="sxs-lookup"><span data-stu-id="0c367-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="0c367-136">Pentru proiecte asociate cu o unitate de vânzări, costul unitar și prețurile de vânzare sunt determinate pe baza acestor liste de prețuri.</span><span class="sxs-lookup"><span data-stu-id="0c367-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="0c367-137">Copierea unei echipe de proiect</span><span class="sxs-lookup"><span data-stu-id="0c367-137">Copying a project team</span></span>

<span data-ttu-id="0c367-138">Când o echipă de proiect este copiată dintr-un șablon într-un proiect, resursele generice sunt copiate, împreună cu abilitățile și nivelurile de competență definite în șablon.</span><span class="sxs-lookup"><span data-stu-id="0c367-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="0c367-139">Atribuirile de resurse generice sunt păstrate cum erau în șablonul de proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="0c367-140">Resursele denumite nu sunt acceptate în șabloanele de proiect.</span><span class="sxs-lookup"><span data-stu-id="0c367-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]