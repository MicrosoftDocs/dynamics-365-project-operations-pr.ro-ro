---
title: Utilizarea programului de completare Project Service pentru a vă planifica munca în Microsoft Project | MicrosoftDocs
description: Acest subiect furnizează informații despre cum se adaugă, se configurează și se utilizează programul de completare Microsoft Project pentru Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129693"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="ca5e7-103">Utilizarea programului de completare Project Service Automation pentru a vă planifica munca în Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="ca5e7-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="ca5e7-104">vă ajută să vă planificați proiectele, inclusiv să realizați estimări.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="ca5e7-105">Puteți defini lucrarea astfel încât costurile, efortul și valoarea vânzărilor să fie clare la momentul când se trimite propunerea finală.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="ca5e7-106">Acum puteți instala [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] și puteți planifica în mediul familiar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="ca5e7-107">Utilizați capacitățile robuste de planificare și management din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], apoi actualizați-vă planul de proiect în Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="ca5e7-108">Pentru a utiliza gestionarea documentelor SharePoint pentru a vă stoca filierele [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pentru proiectele [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], administratorul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] va trebui să pornească gestionare documente.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="ca5e7-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] este compatibil numai cu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="ca5e7-110">Descărcați și instalați programul de completare</span><span class="sxs-lookup"><span data-stu-id="ca5e7-110">Download and install the add-in</span></span>  
 <span data-ttu-id="ca5e7-111">Țineți informațiile de conectare [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la îndemână.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="ca5e7-112">Veți avea nevoie de aceste informații pentru a vă conecta de la [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="ca5e7-113">De la Centrul de descărcare puteți descărca programul de completare pentru versiunea acceptată de Project Service, fie [v2. X](https://go.microsoft.com/fwlink/?linkid=828268), fie [v 3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="ca5e7-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="ca5e7-114">Faceți clic pe linkul de descărcare.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-114">Click the download link.</span></span>  

3.  <span data-ttu-id="ca5e7-115">Odată ce descărcarea s-a finalizat, faceți clic pe **Da** pentru a instala programul de completare.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="ca5e7-116">Configurați programul de completare</span><span class="sxs-lookup"><span data-stu-id="ca5e7-116">Configure the add-in</span></span>  

1. <span data-ttu-id="ca5e7-117">Deschideți [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și faceți clic pe fila **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="ca5e7-118">Faceți clic pe **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="ca5e7-119">Introduceți informațiile de conectare și faceți clic pe **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="ca5e7-120">Acum puteți începe să folosiți programul de completare.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="ca5e7-121">Citirea de pe un șablon</span><span class="sxs-lookup"><span data-stu-id="ca5e7-121">Read from a template</span></span>  
 <span data-ttu-id="ca5e7-122">Citiți dintr-un șablon creat în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] și copiat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pentru a începe să vă planificați proiectul.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ca5e7-123">[Crearea unui șablon de proiect (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="ca5e7-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="ca5e7-124">De pe fila **Project Service**, faceți clic pe **Citire** > **Șablon de proiect Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="ca5e7-125">Alegeți un șablon de proiect din listă și faceți clic pe **Deschidere**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="ca5e7-126">În mod implicit, activitățile copiate din șablon în Project sunt setate drept planificate manual.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="ca5e7-127">Atribuiți roluri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] resurselor proiectului</span><span class="sxs-lookup"><span data-stu-id="ca5e7-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="ca5e7-128">Deschideți un proiect și faceți clic pe panglica **Activitate**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="ca5e7-129">Faceți clic pe meniul **Diagramă Gantt** și alegeți **Foaie de resurse**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="ca5e7-130">Pe foaia de resurse, faceți clic pe meniul vertical **Rol de resursă Project Service** și alegeți un rol Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="ca5e7-131">Găsiți resurse pentru proiectul dvs.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="ca5e7-132">Din fila Project Service, selectați un rând și faceți clic pe **Găsiți resurse**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="ca5e7-133">Pe ecranul **Rezervați resursa**, selectați resursa pe care doriți s-o utilizați pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="ca5e7-134">Faceți clic pe **Rezervare**, apoi pe **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="ca5e7-135">Publicarea proiectului</span><span class="sxs-lookup"><span data-stu-id="ca5e7-135">Publish your project</span></span>  
<span data-ttu-id="ca5e7-136">Atunci când terminați de planificat proiectul, următorul pas este să importați și să publicați proiectul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="ca5e7-137">Proiectul se va importa în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="ca5e7-138">Se aplică procesul de generare a echipelor și a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="ca5e7-139">Deschideți proiectul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pentru a vedea că echipa, estimările de proiect și structura detaliată a proiectului au fost generate.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="ca5e7-140">Următorul tabel arată unde să găsiți rezultatele:</span><span class="sxs-lookup"><span data-stu-id="ca5e7-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="ca5e7-141">**Diagramă Gantt**</span><span class="sxs-lookup"><span data-stu-id="ca5e7-141">**Gantt Chart**</span></span>   | <span data-ttu-id="ca5e7-142">Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Structura detaliată a proiectului**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="ca5e7-143">**Foaie de resurse**</span><span class="sxs-lookup"><span data-stu-id="ca5e7-143">**Resource Sheet**</span></span> |   <span data-ttu-id="ca5e7-144">Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membrii echipei de proiect**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="ca5e7-145">**Folosirea utilizării**</span><span class="sxs-lookup"><span data-stu-id="ca5e7-145">**Use Usage**</span></span>    |    <span data-ttu-id="ca5e7-146">Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimări de proiect**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="ca5e7-147">**Pentru a vă importa și a vă publica proiectul**</span><span class="sxs-lookup"><span data-stu-id="ca5e7-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="ca5e7-148">De pe fila **Project Service**, faceți clic pe **Publicare** > **Proiect nou Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="ca5e7-149">În caseta de dialog **Publicați într-un nou proiect din Project Service**, introduceți **Numele proiectului** și selectați **Clientul**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="ca5e7-150">Opțional, bifați **Legați planul de proiect la Project Service Automation** pentru a lega planul fișierului Project la Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="ca5e7-151">Faceți clic pe **Publicare**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-151">Click **Publish**.</span></span>  

   <span data-ttu-id="ca5e7-152">Legarea fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] face fișierul Project coordonator și stabilește structura detaliată a proiectului din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] drept doar în citire.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="ca5e7-153">Pentru a face modificări în planul de proiect, trebuie să le efectuați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să le publicați ca actualizări la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="ca5e7-154">Editarea unui proiect care a fost importat</span><span class="sxs-lookup"><span data-stu-id="ca5e7-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="ca5e7-155">Pentru a modifica un plan de proiect care a fost importat în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aveți două opțiuni:</span><span class="sxs-lookup"><span data-stu-id="ca5e7-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="ca5e7-156">Deschideți fișierul principal și editați-l în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="ca5e7-157">Anulați legarea fișierului și editați-l direct în Project Service.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="ca5e7-158">În mod implicit, un proiect care a fost încărcat din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] este blocat și poate fi editat numai în Project.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="ca5e7-159">Pentru a edita fișierul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], legarea fișierului trebuie anulată.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="ca5e7-160">Editarea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="ca5e7-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="ca5e7-161">Din meniul principal, faceți clic pe **Project Service** > **Proiecte**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="ca5e7-162">Din lista de proiecte, deschideți-l pe cel creat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="ca5e7-163">Faceți clic pe **Deschideți în MS Project** din panglică.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="ca5e7-164">Acest lucru va deschide fișierul coordonator legat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="ca5e7-165">Anulați legarea unui fișier și editați-l în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="ca5e7-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="ca5e7-166">Din meniul principal, faceți clic pe **Project Service** > **Proiecte**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="ca5e7-167">Din lista de proiecte, deschideți-l pe cel creat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="ca5e7-168">Faceți clic pe **Anulați legarea în MS Project** din panglică.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="ca5e7-169">Încărcarea unui fișier Project în SharePoint sau în Grupurile Office</span><span class="sxs-lookup"><span data-stu-id="ca5e7-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="ca5e7-170">Puteți încărca fișierul Project în SharePoint și îl puteți găsi sub Documentele asociate pentru proiectul dvs. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="ca5e7-171">Trebuie ca administratorul dvs. să configureze gestionarea de documente SharePoint și să o activeze pentru entitatea Project.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="ca5e7-172">De asemenea, puteți încărca fișierul Project în [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] dacă aveți grupurile Office configurate.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="ca5e7-173">Încărcarea unui fișier pentru SharePoint</span><span class="sxs-lookup"><span data-stu-id="ca5e7-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="ca5e7-174">Din meniul principal, faceți clic pe **Project Service** > **Încărcare**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="ca5e7-175">Selectați **În documentele Project din Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="ca5e7-176">În caseta de dialog **Activați deschiderea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selectați **Da** sau **Nu**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="ca5e7-177">Dacă faceți clic pe **Da**, veți putea selecta butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** din Project Service Automation, veți putea lansa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și încărca fișierul Project din biblioteca de documente SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="ca5e7-178">Dacă faceți clic pe **Nu**, linkul pentru butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nu va funcționa.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="ca5e7-179">Fișierul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] poate fi găsit în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sub **Documente** pentru respectivul proiect [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="ca5e7-180">Încărcarea unui fișier pentru grupurile Office</span><span class="sxs-lookup"><span data-stu-id="ca5e7-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="ca5e7-181">Din meniul principal, faceți clic pe **Project Service** > **Încărcare**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="ca5e7-182">Selectați **În documentele Project din Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="ca5e7-183">În caseta de dialog **Activați deschiderea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selectați **Da** sau **Nu**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="ca5e7-184">Dacă faceți clic pe **Da**, veți putea selecta butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** în Project Service Automation, veți putea lansa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și încărca fișierul Project din biblioteca de documente SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="ca5e7-185">Dacă faceți clic pe **Nu**, linkul pentru butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nu va funcționa.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="ca5e7-186">Fișierul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] poate fi găsit în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sub **Documente** pentru respectivul proiect [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="ca5e7-187">Publicarea proiectului ca șablon</span><span class="sxs-lookup"><span data-stu-id="ca5e7-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="ca5e7-188">Puteți să vă salvați proiectul și să-l refolosiți dacă îl salvați ca șablon de proiect în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="ca5e7-189">Șabloanele de proiect sunt planuri de proiect reutilizabile din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ca5e7-190">[Crearea unui șablon de proiect (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="ca5e7-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="ca5e7-191">De pe fila **Project Service**, faceți clic pe **Publicare** > **Șablon proiect nou Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="ca5e7-192">În caseta de dialog **Publicați într-un nou proiect din șablonul Project Service**, introduceți **Numele șablonului de proiect**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="ca5e7-193">Opțional, bifați **Legați planul de proiect la Project Service Automation** pentru a lega fișierul Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="ca5e7-194">Faceți clic pe **Publicare**.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-194">Click **Publish**.</span></span>  

<span data-ttu-id="ca5e7-195">Legarea fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] face fișierul Project coordonator și stabilește structura detaliată a proiectului din șablonul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] drept doar în citire.</span><span class="sxs-lookup"><span data-stu-id="ca5e7-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="ca5e7-196">Pentru a face modificări în planul de proiect, trebuie să le efectuați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să le publicați ca actualizări la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca5e7-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="ca5e7-197">Consultați și</span><span class="sxs-lookup"><span data-stu-id="ca5e7-197">See Also</span></span>  
 [<span data-ttu-id="ca5e7-198">Ghidul Managerului de proiect</span><span class="sxs-lookup"><span data-stu-id="ca5e7-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
