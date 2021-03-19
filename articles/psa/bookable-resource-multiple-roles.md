---
title: Estimează vânzările și costurile proiectului atunci când o resursă care poate fi rezervată îndeplinește mai multe roluri pentru un proiect
description: Acest subiect oferă informații referitoare la modul în care pot fi utilizate dimensiunile de stabilire a prețurilor pentru a sprijini estimarea prețurilor și a costurilor pentru o resursă care îndeplinește mai multe roluri în cadrul unui proiect.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291004"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="4a030-103">Estimează vânzările și costurile proiectului atunci când o resursă care poate fi rezervată îndeplinește mai multe roluri pentru un proiect</span><span class="sxs-lookup"><span data-stu-id="4a030-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4a030-104">Companiile bazate pe proiecte au deseori nevoia unei resurse pentru a realiza mai multe roluri în cadrul unui proiect.</span><span class="sxs-lookup"><span data-stu-id="4a030-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="4a030-105">Pentru fiecare dintre aceste roluri ar putea fi prețurile și costurile ar putea fi calculate diferit, ceea ce înseamnă că timpul aceleiași resurse pentru proiect ar putea obține o estimare financiară diferită în funcție de factură și de ratele de cost pentru fiecare dintre roluri.</span><span class="sxs-lookup"><span data-stu-id="4a030-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="4a030-106">Project Service Automation permite setarea valorilor din înregistrarea membrilor echipei pentru resursa numită și permite diferențieri diferite pentru fiecare dintre activitățile la care este atribuit membrul echipei.</span><span class="sxs-lookup"><span data-stu-id="4a030-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="4a030-107">Următorul exemplu explică modul în care simpla înlocuire a acestei valori permite unei resurse să aibă mai multe roluri într-un proiect cu costuri și rate de facturare diferite.</span><span class="sxs-lookup"><span data-stu-id="4a030-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="4a030-108">Crearea de activități</span><span class="sxs-lookup"><span data-stu-id="4a030-108">Create tasks</span></span>
<span data-ttu-id="4a030-109">Creați două activități de proiect pentru 40 de ore fiecare, activitatea A și activitatea B. Selectați activitatea A ca predecesor pentru activitatea B.</span><span class="sxs-lookup"><span data-stu-id="4a030-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="4a030-110">Configurați rolul și unitatea organizațională pentru un membru generic al echipei de proiect</span><span class="sxs-lookup"><span data-stu-id="4a030-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="4a030-111">Pe pagina **Planificare**, selectați rândul **Activitate** pentru Activitatea A.</span><span class="sxs-lookup"><span data-stu-id="4a030-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="4a030-112">În câmpul **Resurse**, selectați **Creare** în lista verticală.</span><span class="sxs-lookup"><span data-stu-id="4a030-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="4a030-113">Pe pagina **Creare rapidă a membrilor echipei**, specificați atributele membrilor echipei generice care pot îndeplini această activitate.</span><span class="sxs-lookup"><span data-stu-id="4a030-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="4a030-114">Selectați rolul și unitatea organizațională corespunzătoare, apoi selectați **Salvați și închideți**.</span><span class="sxs-lookup"><span data-stu-id="4a030-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="4a030-115">Un membru generic al echipei este creat și atribuit acestei activități.</span><span class="sxs-lookup"><span data-stu-id="4a030-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="4a030-116">Repetați acești pași pentru Activitatea B și asigurați-vă că rolul și unitatea organizațională a membrilor echipei generice create pentru Activitatea B sunt diferite de Activitatea A.</span><span class="sxs-lookup"><span data-stu-id="4a030-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="4a030-117">Configurați rolul și unitatea organizațională pentru o activitate de proiect</span><span class="sxs-lookup"><span data-stu-id="4a030-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="4a030-118">După ce creați Activitatea A, selectați activitatea, apoi selectați **Editați activitatea**.</span><span class="sxs-lookup"><span data-stu-id="4a030-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="4a030-119">Pe pagina **Detalii despre activitate** pagina, găsiți câmpurile **Rol** și **Unitate organizațională**, adăugați valorile necesare unei resurse care ar efectua această activitate.</span><span class="sxs-lookup"><span data-stu-id="4a030-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="4a030-120">Dacă completați aceste scenarii utilizând datele demo ale Project Service Automation, selectați **Lider consultant** pentru rol și **Fabrikam SUA** ca unitate organizațională.</span><span class="sxs-lookup"><span data-stu-id="4a030-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="4a030-121">Selectați Activitatea B, apoi selectați **Editare activitate**.</span><span class="sxs-lookup"><span data-stu-id="4a030-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="4a030-122">Pe pagina **Detalii despre activitate** pagina, găsiți câmpurile **Rol** și **Unitate organizațională**, adăugați valorile necesare unei resurse care ar efectua această activitate.</span><span class="sxs-lookup"><span data-stu-id="4a030-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="4a030-123">Asigurați-vă că valorile din câmpurile **Rol** și **Unitate organizațională** sunt diferite pentru sarcina B de valorile pentru sarcina A.</span><span class="sxs-lookup"><span data-stu-id="4a030-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="4a030-124">Dacă completați aceste scenarii utilizând datele demo ale Project Service Automation, selectați **Tehnician rețea** pentru rol și **Fabrikam SUA** ca unitate organizațională.</span><span class="sxs-lookup"><span data-stu-id="4a030-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="4a030-125">Salvați și închideți pagina **Detalii activitate**.</span><span class="sxs-lookup"><span data-stu-id="4a030-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="4a030-126">Membru al echipei și estimează comportamentul</span><span class="sxs-lookup"><span data-stu-id="4a030-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="4a030-127">Pe pagina **Detalii despre activitate**, pe **Membru al echipei**, selectați cei doi membri generici ai echipei și apoi selectați **Generați cerințe**.</span><span class="sxs-lookup"><span data-stu-id="4a030-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="4a030-128">Selectați rândul membrului echipei pentru **Lider consultant** și apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="4a030-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="4a030-129">Tabloul de programare se deschide și rezervă o resursă pentru acea cerință.</span><span class="sxs-lookup"><span data-stu-id="4a030-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="4a030-130">Selectați rândul membrului echipei pentru **Tehnician rețea** și apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="4a030-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="4a030-131">Tabloul de programare se deschide și rezervă aceeași resursă pentru acea cerință.</span><span class="sxs-lookup"><span data-stu-id="4a030-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="4a030-132">Grila membrilor echipei</span><span class="sxs-lookup"><span data-stu-id="4a030-132">Team Member grid</span></span> 
<span data-ttu-id="4a030-133">Pe grila **Membru al echipei**, observați că cele două înregistrări generice ale membrilor echipei sunt șterse și au fost înlocuite cu o singură resursă.</span><span class="sxs-lookup"><span data-stu-id="4a030-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="4a030-134">Există un set de valori pentru resursa respectivă care arată un set implicit de valori pentru **Rol** și **Unitate organizațională**.</span><span class="sxs-lookup"><span data-stu-id="4a030-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="4a030-135">Când extindeți rândul înregistrării acelui membru al echipei, puteți vedea atribuiri distincte în înregistrarea membrilor echipei pentru ambele activități.</span><span class="sxs-lookup"><span data-stu-id="4a030-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="4a030-136">Fiecare rând de atribuire are valori specifice activității pentru **Rol** și **Unitate organizațională**.</span><span class="sxs-lookup"><span data-stu-id="4a030-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="4a030-137">Grilă estimări</span><span class="sxs-lookup"><span data-stu-id="4a030-137">Estimates grid</span></span> 
<span data-ttu-id="4a030-138">Când navigați la grila **Estimări**, veți observa că ambele activități pentru aceeași resursă au un preț diferit.</span><span class="sxs-lookup"><span data-stu-id="4a030-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="4a030-139">Atribuirea pentru resursa din Activitatea A este evaluată cu ajutorul valorii atributului **Rol** al **Lider consultant**.</span><span class="sxs-lookup"><span data-stu-id="4a030-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="4a030-140">Atribuirea pentru aceeași resursă din Activitatea A este evaluată cu ajutorul valorii atributului **Rol** pentru **Tehnician rețea**.</span><span class="sxs-lookup"><span data-stu-id="4a030-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]