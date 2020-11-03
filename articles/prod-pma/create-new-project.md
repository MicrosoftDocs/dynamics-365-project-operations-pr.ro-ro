---
title: Creați un nou proiect
description: Acest subiect oferă informații despre cum să creați un proiect nou.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082931"
---
# <a name="create-a-new-project"></a><span data-ttu-id="35ddf-103">Creați un nou proiect</span><span class="sxs-lookup"><span data-stu-id="35ddf-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35ddf-104">Parcurgeți pașii următori pentru a crea un nou proiect.</span><span class="sxs-lookup"><span data-stu-id="35ddf-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="35ddf-105">În pagina **Management de proiect** , selectați **Proiect nou** , și introduceți următoarele valori:</span><span class="sxs-lookup"><span data-stu-id="35ddf-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="35ddf-106">**Tipul proiectului:** Timp și material</span><span class="sxs-lookup"><span data-stu-id="35ddf-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="35ddf-107">**Denumirea proiectului:** Faza 2 de upgrade XYZ</span><span class="sxs-lookup"><span data-stu-id="35ddf-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="35ddf-108">**Grup de proiect:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="35ddf-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="35ddf-109">**ID contract proiect:** 00000002</span><span class="sxs-lookup"><span data-stu-id="35ddf-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="35ddf-110">Selectați **Creați un proiect**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="35ddf-111">Atribuirea unei resurse unui proiect</span><span class="sxs-lookup"><span data-stu-id="35ddf-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="35ddf-112">Din pagina **Angajați** , în lista **Angajați** , selectați înregistrarea pentru angajatul pentru care ați configurat anterior competențele, și deschideți înregistrarea angajatului.</span><span class="sxs-lookup"><span data-stu-id="35ddf-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="35ddf-113">În panoul de acțiuni, în fila **Proiect** , în grupul **Configurare** , selectați **Atribuire proiecte**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="35ddf-114">Din pagina **Validarea resurselor pentru atribuiri în proiect** , din fila **Proiecte** , în câmpul **Adăugați proiectul la proiectele selectate** , filtrați pentru proiectul **Faza 2 de upgrade XYZ**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="35ddf-115">În panoul **Proiecte rămase** , selectați un proiect, apoi selectați butonul săgeată pentru a-l adăuga la panoul **Proiecte selectate**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="35ddf-116">De asemenea, puteți atribui categorii pentru o resursă după cum doriți.</span><span class="sxs-lookup"><span data-stu-id="35ddf-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="35ddf-117">Tipul categoriei este fie **Cost** fie **Venit**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="35ddf-118">Tipul categoriei este determinat de organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="35ddf-118">The category type is determined by your organization.</span></span> <span data-ttu-id="35ddf-119">Dacă nu sunt alocate categorii pentru o resursă, Finanțele caută categoria implicită a prețurilor orare pentru costuri și venituri.</span><span class="sxs-lookup"><span data-stu-id="35ddf-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="35ddf-120">Configurați resursele proiectului și caracteristicile rolului</span><span class="sxs-lookup"><span data-stu-id="35ddf-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="35ddf-121">Un manager de proiect poate utiliza funcționalitatea de alocare de resurse proiectului pentru a crea rolurile necesare pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="35ddf-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="35ddf-122">Rolurile pot fi utilizate dacă resursele confirmate sunt încă necunoscute atunci când resursele sunt rezervate.</span><span class="sxs-lookup"><span data-stu-id="35ddf-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="35ddf-123">Rolurile pot fi rezervate temporar ca resurse planificate, astfel încât să puteți continua etapele de planificare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="35ddf-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="35ddf-124">[![Exemplu de rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="35ddf-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="35ddf-125">**Scenariu:** Contoso a fost angajat pentru a finaliza un proiect de timp și materiale care are o cartă de proiect aprobată.</span><span class="sxs-lookup"><span data-stu-id="35ddf-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="35ddf-126">Managerul de proiect junior continuă să finalizeze domeniul de aplicare al proiectului.</span><span class="sxs-lookup"><span data-stu-id="35ddf-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="35ddf-127">Managerul de resurse identifică în prezent resursele specifice care vor fi rezervate pentru a lucra la noul proiect.</span><span class="sxs-lookup"><span data-stu-id="35ddf-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="35ddf-128">Datorită naturii critice a proiectului, sponsorul proiectului a solicitat managerul de proiect senior ca unul dintre roluri.</span><span class="sxs-lookup"><span data-stu-id="35ddf-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="35ddf-129">Managerul de resurse trebuie să dobândească noua resursă și să definească rolul în sistem în cazul în care managerul de proiect junior are nevoie de informații despre resurse în timpul planificării proiectului.</span><span class="sxs-lookup"><span data-stu-id="35ddf-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="35ddf-130">Următorii pași arată modul în care managerul de resurse poate configura rolul de manager de proiect senior și poate asocia caracteristicile resursei acestuia.</span><span class="sxs-lookup"><span data-stu-id="35ddf-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="35ddf-131">Ulterior, rolul poate fi folosit pentru a căuta resursele disponibile care corespund competențelor necesare pentru resursă.</span><span class="sxs-lookup"><span data-stu-id="35ddf-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="35ddf-132">În pagina **Configurare roluri** , selectați **Nou** , și introduceți următoarele valori:</span><span class="sxs-lookup"><span data-stu-id="35ddf-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="35ddf-133">**ID rol:** Manager de proiect senior</span><span class="sxs-lookup"><span data-stu-id="35ddf-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="35ddf-134">**Descriere:** Manager de proiect senior</span><span class="sxs-lookup"><span data-stu-id="35ddf-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="35ddf-135">Selectați **Creare**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-135">Select **Create**.</span></span>
3. <span data-ttu-id="35ddf-136">Selectați rolul **Manager de proiect senior** , apoi selectați **Configurare caracteristici**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="35ddf-137">În câmpul **Tip caracteristici** , selectați **Abilitate**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="35ddf-138">În câmpul **Caracteristici disponibile** , introduceți abilitatea de căutat.</span><span class="sxs-lookup"><span data-stu-id="35ddf-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="35ddf-139">În câmpul **Tip caracteristică** , selectați **Certificat**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="35ddf-140">În câmpul **Caracteristici disponibile** , introduceți tipul de certificat de căutat.</span><span class="sxs-lookup"><span data-stu-id="35ddf-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="35ddf-141">Atribuirea unei resurse de proiect unui proiect</span><span class="sxs-lookup"><span data-stu-id="35ddf-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="35ddf-142">Din pagina **Toate proiectele** , selectați proiectul **Faza 2 de upgrade XYZ**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="35ddf-143">Din fila **Echipa proiectului și planificarea** , selectați **Adăugare**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="35ddf-144">În câmpul **Rol** , selectați **Membru al echipei**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="35ddf-145">Selectați **Rezervare din calendar**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="35ddf-146">Din pagina **Disponibilitate resurse** , selectați **Vizualizare setări**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="35ddf-147">În pagina **Reglați setările de vizualizare** , introduceți următoarele valori:</span><span class="sxs-lookup"><span data-stu-id="35ddf-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="35ddf-148">**Format pentru vizualizarea intervalului de dată:** Zi</span><span class="sxs-lookup"><span data-stu-id="35ddf-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="35ddf-149">**Afișați descrierile disponibilității:** Da</span><span class="sxs-lookup"><span data-stu-id="35ddf-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="35ddf-150">**Afișați capacitatea rămasă:** Da</span><span class="sxs-lookup"><span data-stu-id="35ddf-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="35ddf-151">În lista de resurse, selectați o resursă.</span><span class="sxs-lookup"><span data-stu-id="35ddf-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="35ddf-152">Selectați **Rezervare fermă** și **Capacitate completă**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="35ddf-153">Atribuirea unei resurse unui rol implicit</span><span class="sxs-lookup"><span data-stu-id="35ddf-153">Assign a resource to a default role</span></span>

<span data-ttu-id="35ddf-154">Pentru a ajuta managerii de proiect sau de resurse pentru drill down mai mult pentru resursele care pot fi rezervate pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="35ddf-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="35ddf-155">Puteți asocia un rol implicit cu o resursă existentă sau cu o resursă nou achiziționată.</span><span class="sxs-lookup"><span data-stu-id="35ddf-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="35ddf-156">De exemplu, când Daniel a fost angajat, avea experiența și abilitățile pentru a ocupa rolul de analist de afaceri.</span><span class="sxs-lookup"><span data-stu-id="35ddf-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="35ddf-157">Managerul de resurse a atribuit acest rol ca rolul implicit al lui Daniel.</span><span class="sxs-lookup"><span data-stu-id="35ddf-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="35ddf-158">Prin urmare, managerul de resurse l-a adăugat pe Daniel la un grup de analiști de afaceri care sunt disponibili să lucreze la proiecte.</span><span class="sxs-lookup"><span data-stu-id="35ddf-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="35ddf-159">În timpul rezervării resurselor, managerii de proiect pot filtra resursele de rol disponibile pentru a lucra la proiecte.</span><span class="sxs-lookup"><span data-stu-id="35ddf-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="35ddf-160">Aceștia pot utiliza aceste informații ca un criteriu atunci când efectuează o analiză a deciziilor pe mai multe criterii în timpul îndeplinirii resurselor.</span><span class="sxs-lookup"><span data-stu-id="35ddf-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="35ddf-161">De asemenea, pot adăuga alte caracteristici ale resurselor la filtru pentru a căuta resurse care au abilități, educație și experiență specifice pentru un anumit proiect.</span><span class="sxs-lookup"><span data-stu-id="35ddf-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="35ddf-162">**Scenariu:** A început un proiect aprobat, iar rolul Manager de proiect senior a fost rezervat ca resursă planificată în etapa de planificare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="35ddf-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="35ddf-163">Managerul de resurse a achiziționat acum o resursă pentru a îndeplini rolul de manager de proiect senior.</span><span class="sxs-lookup"><span data-stu-id="35ddf-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="35ddf-164">Din pagina **Lista resurselor** , selectați **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="35ddf-165">În pagina **Rol resursă** , selectați **Nou** , și introduceți următoarele valori:</span><span class="sxs-lookup"><span data-stu-id="35ddf-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="35ddf-166">**În vigoare:** Introduceți data curentă.</span><span class="sxs-lookup"><span data-stu-id="35ddf-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="35ddf-167">**Expirare:** introduceți **Niciodată**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="35ddf-168">**Rol:** introduceți **Manager de proiect senior**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="35ddf-169">Selectați **Salvare** , apoi închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="35ddf-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="35ddf-170">Din fila **Competențe** , adăugați abilitatea **ProjectMgmt** și certificatul **PMP**.</span><span class="sxs-lookup"><span data-stu-id="35ddf-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
