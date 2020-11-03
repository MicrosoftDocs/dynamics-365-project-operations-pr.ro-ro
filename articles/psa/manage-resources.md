---
title: Gestionare resurse
description: Acest subiect oferă informații despre cum puteți gestiona resursele.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082997"
---
# <a name="manage-resources"></a><span data-ttu-id="002fe-103">Gestionare resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="002fe-104">Dynamics 365 Project Service Automation include un tablou de bord al managerului de resurse care oferă o prezentare vizuală a cererii și utilizării resurselor în întreaga organizație.</span><span class="sxs-lookup"><span data-stu-id="002fe-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="002fe-105">Puteți utiliza diagramele de pe acest tablou de bord pentru a vizualiza următoarele informații:</span><span class="sxs-lookup"><span data-stu-id="002fe-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="002fe-106">**Cerere resursă** – diagrama **Solicitare de resursă activă** afișează resursele care au fost remise.</span><span class="sxs-lookup"><span data-stu-id="002fe-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="002fe-107">Resursele sunt agregate după fiecare rol sau proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="002fe-108">**Cerere de resurse neremise** - diagrama **Cerere de resurse neremise** afișează toate cerințele de resurse care nu au fost remise.</span><span class="sxs-lookup"><span data-stu-id="002fe-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="002fe-109">Ajută managerii de resurse să vizualizeze cererea care nu este fermă și poate fi remisă printr-o solicitare de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="002fe-110">**Utilizarea facturabilă pentru săptămâna trecută** – diagrama **Utilizare în funcție de rol** arată procentul utilizării efective facturabile a organizației în funcție de rolul pe care l-a avut asupra utilizării sale facturabile în funcție de rol.</span><span class="sxs-lookup"><span data-stu-id="002fe-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="002fe-111">Pentru a face diagrama **Utilizare în funcție de rol** disponibilă, creați o operațiune care rulează fluxul de lucru UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="002fe-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="002fe-112">Această operațiune periodică se execută la fiecare șapte zile pentru a calcula utilizarea facturabilă pentru ultimele șapte zile.</span><span class="sxs-lookup"><span data-stu-id="002fe-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="002fe-113">Rezultatele sunt agregate în funcție de rol.</span><span class="sxs-lookup"><span data-stu-id="002fe-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="002fe-114">Gestionarea membrilor echipei de proiect</span><span class="sxs-lookup"><span data-stu-id="002fe-114">Manage project team members</span></span>

<span data-ttu-id="002fe-115">Managerii de proiect pot utiliza tabloul de bord al managerului de resurse pentru a gestiona resursele din proiecte.</span><span class="sxs-lookup"><span data-stu-id="002fe-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="002fe-116">De exemplu, ele pot adăuga un membru al echipei direct la un proiect și rezerva un membru al echipei pentru a îndeplini cerințele de resurse care au fost capturate de o resursă generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="002fe-117">Adăugarea unui membru al echipei direct la un proiect</span><span class="sxs-lookup"><span data-stu-id="002fe-117">Add a team member directly to a project</span></span>

<span data-ttu-id="002fe-118">Pentru a adăuga un membru al echipei direct la un proiect, pe pagina **Proiecte** , pe fila **Echipă** , selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="002fe-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="002fe-119">Apare caseta de dialog **Creare rapidă:membru al echipei de proiect**.</span><span class="sxs-lookup"><span data-stu-id="002fe-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="002fe-120">În această casetă de dialog, aveți posibilitatea să efectuați aceste activități:</span><span class="sxs-lookup"><span data-stu-id="002fe-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="002fe-121">**Rezervați o resursă denumită** - în câmpul **Resursă care se poate rezerva** , selectați numele resursei.</span><span class="sxs-lookup"><span data-stu-id="002fe-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="002fe-122">Apoi selectați rolul, setați perioada și selectați o metodă de alocare.</span><span class="sxs-lookup"><span data-stu-id="002fe-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="002fe-123">Resursa denumită pe care ați selectat-o este adăugată la proiect utilizând metoda de alocare selectată și calendarul de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="002fe-124">**Adăugați o resursă generică** - lăsați câmpul **Resurse care se pot rezerva** necompletat, apoi selectați rolul, setați perioada și selectați metoda de alocare preferată.</span><span class="sxs-lookup"><span data-stu-id="002fe-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="002fe-125">O resursă generică este adăugată la echipă ca un substituent pentru a ține modelul cererii care este utilizat pentru a rezerva resursele numite pe echipă.</span><span class="sxs-lookup"><span data-stu-id="002fe-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="002fe-126">Cerința se face în funcție de calendarul proiectului.</span><span class="sxs-lookup"><span data-stu-id="002fe-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="002fe-127">**Adăugați la echipă o resursă denumită fără a consuma capacitatea de resurse** - în câmpul **Resursă care se poate rezerva** , selectați o resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="002fe-128">Apoi selectați perioada și selectați **Niciuna** ca metodă de alocare.</span><span class="sxs-lookup"><span data-stu-id="002fe-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="002fe-129">Resursa este adăugată la echipă, dar capacitatea resursei nu este consumată printr-o rezervare.</span><span class="sxs-lookup"><span data-stu-id="002fe-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="002fe-130">Rezervați un membru al echipei pentru a îndeplini cerințele de resurse pentru o resursă generică</span><span class="sxs-lookup"><span data-stu-id="002fe-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="002fe-131">În PSA, aveți posibilitatea să rezervați o resursă generică într-o echipă de proiect și să specificați rolul, capacitatea necesară și modul în care este distribuită această capacitate.</span><span class="sxs-lookup"><span data-stu-id="002fe-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="002fe-132">Pe cerința de resurse, aveți posibilitatea să specificați atributele care sunt asociate cu resursa generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="002fe-133">Aceste atribute includ aptitudinile necesare, unitatea organizațională preferată și resursele preferate.</span><span class="sxs-lookup"><span data-stu-id="002fe-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="002fe-134">Urmați acești pași pentru a specifica abilitățile necesare pe o resursă generică pentru un dezvoltator.</span><span class="sxs-lookup"><span data-stu-id="002fe-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="002fe-135">Pe pagina **Proiecte** , pe fila **Echipă** , selectați **Nou** pentru a rezerva o resursă generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Resursă generică rezervată echipei](media/Resource-Management-image9.png)

2. <span data-ttu-id="002fe-137">În vizualizarea **Toți membrii echipei** , în coloana **Cerință de resursă** , selectați linkul pentru a adăuga abilitățile necesare pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Link cerință](media/Resource-Management-image10.png)

3. <span data-ttu-id="002fe-139">Pe pagina **Cerință de resurse** care apare, în grila **Abilități** , selectați punctele de suspensie ( **...** ) și apoi selectați **Adăugați noua caracteristică cerință** pentru a adăuga abilitățile necesare pentru dezvoltator.</span><span class="sxs-lookup"><span data-stu-id="002fe-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Adăugați comandă nouă Caracteristică cerință](media/Resource-Management-image11.png)

4. <span data-ttu-id="002fe-141">În caseta de dialog **Creare rapidă: caracteristică cerință** care apare, în câmpul **Caracteristică** , selectați abilitatea necesară.</span><span class="sxs-lookup"><span data-stu-id="002fe-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="002fe-142">Apoi, în câmpul **Valoare de evaluare** , selectați nivelul de competență pentru acea abilitate.</span><span class="sxs-lookup"><span data-stu-id="002fe-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="002fe-143">În cele din urmă în câmpul **Cerință de resursă** , setați cerința de resurse pentru a obține resurse din unități organizaționale sau chiar resurse numite.</span><span class="sxs-lookup"><span data-stu-id="002fe-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="002fe-144">Când ați terminat, selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="002fe-144">When you've finished, select **Save**.</span></span>

    ![Creare rapidă: caseta de dialog Caracteristică cerință](media/Resource-Management-image12.png)

5. <span data-ttu-id="002fe-146">Pe pagina **Cerință resursă** , selectați **Rezervare** pentru a îndeplini cerința de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Buton de rezervare pe pagina Cerință de resursă](media/Resource-Management-image13.png)

    <span data-ttu-id="002fe-148">De asemenea, puteți selecta resursa generică în grila **Toți membrii echipei** și apoi selectați **Rezervare**.</span><span class="sxs-lookup"><span data-stu-id="002fe-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Butonul rezervare de deasupra grilei Toți membrii echipei](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="002fe-150">În acest exemplu, există 40 ore necesare, dar nu ore rezervate reale, deoarece resursele generice nu au rezervări.</span><span class="sxs-lookup"><span data-stu-id="002fe-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="002fe-151">În plus, nu există ore atribuite, deoarece resursa generică a fost adăugată direct la echipă.</span><span class="sxs-lookup"><span data-stu-id="002fe-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="002fe-152">Nu s-a adăugat utilizând atribuirea sarcinilor.</span><span class="sxs-lookup"><span data-stu-id="002fe-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="002fe-153">În pagina **Asistent de planificare** , aveți posibilitatea să filtrați resursele disponibile după cerințele specificate în cerința de resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="002fe-154">Resursele sunt sortate în funcție de parametrii de sortare specificați în Tabloul de planificare.</span><span class="sxs-lookup"><span data-stu-id="002fe-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Pagina Asistent de planificare](media/Resource-Management-image15.png)

    <span data-ttu-id="002fe-156">Iată câteva filtre care sunt adesea utilizate:</span><span class="sxs-lookup"><span data-stu-id="002fe-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="002fe-157">**Caracteristici, împreună cu o evaluare** - filtrare după abilități, certificari, și alte calități de resurse, în plus față de evaluarea de competență.</span><span class="sxs-lookup"><span data-stu-id="002fe-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="002fe-158">**Roluri** – filtrați după rolurile implicite care sunt atribuite resurselor care se pot rezerva.</span><span class="sxs-lookup"><span data-stu-id="002fe-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="002fe-159">**Unități organizaționale** – filtrați resursele care pot fi rezervate de către unitățile organizaționale la care sunt atribuite.</span><span class="sxs-lookup"><span data-stu-id="002fe-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="002fe-160">Dacă nu sunteți mulțumit de rezultatele căutării inițiale de cerințe, aveți posibilitatea să modificați criteriile de filtrare.</span><span class="sxs-lookup"><span data-stu-id="002fe-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="002fe-161">Extindeți panoul **Vizualizare filtrare** din partea stângă, apoi selectați **Căutare** pentru a găsi resurse suplimentare.</span><span class="sxs-lookup"><span data-stu-id="002fe-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Panou vizualizare filtrare](media/Resource-Management-image16.png)

7. <span data-ttu-id="002fe-163">Pentru a modifica modul de sortare a rezultatelor, selectați **Sortare**.</span><span class="sxs-lookup"><span data-stu-id="002fe-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Comanda sortare](media/Resource-Management-image17.png)

8. <span data-ttu-id="002fe-165">Selectați resurse în funcție de cererea specificată pe cerință, așa cum este indicat în partea de sus a grilei.</span><span class="sxs-lookup"><span data-stu-id="002fe-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="002fe-166">Puteți goli selecția celulelor din grilă și lăsați acea capacitate de resurse deschisă.</span><span class="sxs-lookup"><span data-stu-id="002fe-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="002fe-167">Poate fi selectată drept rezervată o singură resursă pe rând.</span><span class="sxs-lookup"><span data-stu-id="002fe-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="002fe-168">Selectați **Rezervare** pentru a rezerva resursa selectată și lăsați tabloul de planificare deschis, astfel încât să puteți selecta resurse suplimentare.</span><span class="sxs-lookup"><span data-stu-id="002fe-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="002fe-169">Alternativ, selectați **Rezervați și ieșiți** pentru a rezerva resursa selectată și închideți tabloul de planificare.</span><span class="sxs-lookup"><span data-stu-id="002fe-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Resursă de rezervat](media/Resource-Management-image19.png)

    <span data-ttu-id="002fe-171">Primiți o notificare despre orele rezervate.</span><span class="sxs-lookup"><span data-stu-id="002fe-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="002fe-172">Indicatorii cererii arată cât de mult cerința de rezervare este îndeplinită și cât de mult rămâne.</span><span class="sxs-lookup"><span data-stu-id="002fe-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="002fe-173">De asemenea, puteți vedea cât de mult din capacitatea resursei selectate este consumată.</span><span class="sxs-lookup"><span data-stu-id="002fe-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="002fe-174">Selectați **Extindeți** pentru a vizualiza mai multe detalii despre rezervările de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="002fe-175">Reveniți la vizualizarea **Toți membrii echipei**.</span><span class="sxs-lookup"><span data-stu-id="002fe-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="002fe-176">În grilă, observați că resursa generic a fost înlocuită de resursa denumită și 40 ore sunt listate ca rezervate pentru acea resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Actualizat grila Toți membrii echipei](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="002fe-178">Nu sunt afișate ore alocate, deoarece acestea au fost rezervate direct în echipă.</span><span class="sxs-lookup"><span data-stu-id="002fe-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="002fe-179">Nu au fost rezervate prin atribuirea sarcinilor.</span><span class="sxs-lookup"><span data-stu-id="002fe-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="002fe-180">Atribuiți resurse generice la activități și generați cerințe de resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="002fe-181">În PSA, aveți posibilitatea să creați activități și apoi să le atribuiți resurse generice.</span><span class="sxs-lookup"><span data-stu-id="002fe-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="002fe-182">În acest fel, cererea de resurse poate fi reprezentată de substituenți în timp ce estimați planificarea și numerele financiare.</span><span class="sxs-lookup"><span data-stu-id="002fe-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="002fe-183">Puteți genera apoi cerințe de resurse pentru resursele generice și să le îndepliniți.</span><span class="sxs-lookup"><span data-stu-id="002fe-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="002fe-184">Pe pagina de **Proiecte** , în fila **Planificare** , selectați **Adăugare** pentru a crea o activitate.</span><span class="sxs-lookup"><span data-stu-id="002fe-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Activitate nouă creată](media/Resource-Management-image21.png)

2. <span data-ttu-id="002fe-186">În câmpul **Resurse** , selectați simbolul **Selectorul de resurse**.</span><span class="sxs-lookup"><span data-stu-id="002fe-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="002fe-187">Selectorul de resurse apare și afișează membrii echipei existente pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Selector resurse](media/Resource-Management-image22.png)

3. <span data-ttu-id="002fe-189">Introduceți numele resursei generice noi, apoi selectați **Creare**.</span><span class="sxs-lookup"><span data-stu-id="002fe-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Numele unei noi resurse generice introduse](media/Resource-Management-image23.png)

4. <span data-ttu-id="002fe-191">În caseta de dialog **Creare rapidă: membrul echipei de proiect** care apare, în câmpul **Rol** , selectați rolul pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="002fe-192">În câmpul **Unitate resursă** , selectați unitatea organizațională pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="002fe-193">Apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="002fe-193">Then select **Save**.</span></span>

    ![Creare rapidă: caseta de dialog Membrul echipei de proiect](media/Resource-Management-image24.png)

    <span data-ttu-id="002fe-195">Membrul generic al echipei este acum atribuit activității.</span><span class="sxs-lookup"><span data-stu-id="002fe-195">The generic team member is now assigned to the task.</span></span>

    ![Membrul generic al echipei atribuit activității](media/Resource-Management-image25.png)

    <span data-ttu-id="002fe-197">În fila **Echipă** , veți vedea noul membru generic al echipei.</span><span class="sxs-lookup"><span data-stu-id="002fe-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="002fe-198">Observați că are doar ore atribuite.</span><span class="sxs-lookup"><span data-stu-id="002fe-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="002fe-199">Aceste ore sunt suma tuturor activităților care sunt atribuite membrului generic de echipă.</span><span class="sxs-lookup"><span data-stu-id="002fe-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="002fe-200">Membrul generic al echipei nu are încă orele necesare sau o cerință de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Membru generic de echipă în fila Echipă](media/Resource-Management-image26.png)

5. <span data-ttu-id="002fe-202">Acum aveți posibilitatea să atribuiți membrul generic de echipă altor activități utilizând selectorul de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Membru generic de echipă în selectorul de resurse](media/Resource-Management-image27.png)

    <span data-ttu-id="002fe-204">După ce ați terminat asocierea resursei generice la activități, aveți posibilitatea să generați o cerință de resursă pentru resursa generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="002fe-205">În fila **Echipă** , selectați resursa generică, apoi selectați **Generare cerință**.</span><span class="sxs-lookup"><span data-stu-id="002fe-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Comanda Generați cerința](media/Resource-Management-image28.png)

    <span data-ttu-id="002fe-207">Când se generează cerința, membrul generic al echipei va avea ore necesare și un link pentru cerința de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Link cerință de resurse](media/Resource-Management-image29.png)

    <span data-ttu-id="002fe-209">După ce rezervați o resursă denumită, resursa generică este eliminată din echipă și înlocuită de resursa denumită.</span><span class="sxs-lookup"><span data-stu-id="002fe-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Resursă generică înlocuită de resursa denumită](media/Resource-Management-image30.png)

    <span data-ttu-id="002fe-211">În fila **Planificare** , atribuirile de resurse generice sunt eliminate și înlocuite de resursa denumită.</span><span class="sxs-lookup"><span data-stu-id="002fe-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Atribuiri ale resursei generice înlocuite de resursa denumită pe fila Planificare](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="002fe-213">Acest comportament are loc numai atunci când o resursă denumită este complet rezervată pentru cerința de resurse generice.</span><span class="sxs-lookup"><span data-stu-id="002fe-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="002fe-214">Când fie o resursă denumită înlocuiește parțial cerința de resurse generice sau mai multe resurse numite înlocuiesc cerința de resurse generice, resursa generică rămâne atribuită activității.</span><span class="sxs-lookup"><span data-stu-id="002fe-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="002fe-215">În ilustrația următoare, o activitate de 80 de ore a fost planificată pentru o durată de cinci zile (16 ore pe zi timp de cinci zile) și atribuită resursei generice care este numită **Funcțională**.</span><span class="sxs-lookup"><span data-stu-id="002fe-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Activitate de optzeci de ore, cinci zile, atribuită resursei generice funcționale](media/Resource-Management-image32.png)

    <span data-ttu-id="002fe-217">Când generați cerința, este de 80 de ore timp de cinci zile.</span><span class="sxs-lookup"><span data-stu-id="002fe-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Cerință generată pentru 80 ore tim de cinci zile](media/Resource-Management-image33.png)

    <span data-ttu-id="002fe-219">Deoarece resursele disponibile funcționează doar opt ore pe zi, sunt necesare două resurse pentru a îndeplini cerința.</span><span class="sxs-lookup"><span data-stu-id="002fe-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![A doua resursă](media/Resource-Management-image35.png)

    <span data-ttu-id="002fe-221">În fila **Echipă** , puteți vedea acum că resursa generică nu are ore necesare, dar orele atribuite apar în continuare împreună cu cele două resurse numite care alcătuiesc procesarea.</span><span class="sxs-lookup"><span data-stu-id="002fe-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Două resurse denumite în fila Echipă](media/Resource-Management-image36.png)

    <span data-ttu-id="002fe-223">Pe fila **Planificare** resursa generică rămâne atribuită activității.</span><span class="sxs-lookup"><span data-stu-id="002fe-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Resurse generice în fila planificare](media/Resource-Management-image37.png)

<span data-ttu-id="002fe-225">PSA nu atribuie ambele resurse activității, pentru că acel comportament ar produce o planificare mai puțin previzibilă.</span><span class="sxs-lookup"><span data-stu-id="002fe-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="002fe-226">În acest exemplu simplu, este ușor să împărțiți orele în mod egal între două resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="002fe-227">Cu toate acestea, în scenarii mai complexe care implică mai multe sarcini și mai multe resurse, PSA ar trebui să facă presupuneri despre ar trebui să aloce rezervările care sunt primite pentru mai multe resurse în mai multe activități.</span><span class="sxs-lookup"><span data-stu-id="002fe-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="002fe-228">Prin urmare, în aceste scenarii, managerul de proiect este responsabil pentru analizarea mai multor rezervări și atribuirea acestora după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="002fe-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="002fe-229">Pentru a aloca rezervările, managerul de proiect atribuie activitățile din resursele generice la resursele numite și apoi utilizează vizualizarea **Reconciliere** pentru a vă asigura că alocarea funcționează cu rezervările.</span><span class="sxs-lookup"><span data-stu-id="002fe-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="002fe-230">Editați o cerință de resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-230">Edit a resource requirement</span></span>

<span data-ttu-id="002fe-231">După ce s-a creat o cerință de resursă, un manager de proiect sau un manager de resurse poate dori să editeze detaliile pentru a rafina criteriile de căutare atunci când se utilizează tabloul de planificare.</span><span class="sxs-lookup"><span data-stu-id="002fe-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="002fe-232">Pentru a edita cerința de resurse, urmați acești pași.</span><span class="sxs-lookup"><span data-stu-id="002fe-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="002fe-233">Pe pagina **Proiecte** , pe fila **Echipă** , selectați linkul spre orice cerință pe o resursă generică.</span><span class="sxs-lookup"><span data-stu-id="002fe-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="002fe-234">Pe pagina **Cerință de resurse** care apare, aveți posibilitatea să actualizați mai multe atribute.</span><span class="sxs-lookup"><span data-stu-id="002fe-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="002fe-235">Iată câteva exemple:</span><span class="sxs-lookup"><span data-stu-id="002fe-235">Here are some examples:</span></span>

    - <span data-ttu-id="002fe-236">Nume</span><span class="sxs-lookup"><span data-stu-id="002fe-236">Name</span></span>
    - <span data-ttu-id="002fe-237">De la data</span><span class="sxs-lookup"><span data-stu-id="002fe-237">From Date</span></span>
    - <span data-ttu-id="002fe-238">Până în prezent</span><span class="sxs-lookup"><span data-stu-id="002fe-238">To Date</span></span>
    - <span data-ttu-id="002fe-239">Durată</span><span class="sxs-lookup"><span data-stu-id="002fe-239">Duration</span></span>
    - <span data-ttu-id="002fe-240">Tip de resursă</span><span class="sxs-lookup"><span data-stu-id="002fe-240">Resource Type</span></span>

<span data-ttu-id="002fe-241">Pe pagina **Cerință de resurse** , managerul de proiect sau managerul de resurse poate defini, de asemenea, următoarele informații:</span><span class="sxs-lookup"><span data-stu-id="002fe-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="002fe-242">Competențe</span><span class="sxs-lookup"><span data-stu-id="002fe-242">Skills</span></span>
- <span data-ttu-id="002fe-243">Roluri</span><span class="sxs-lookup"><span data-stu-id="002fe-243">Roles</span></span>
- <span data-ttu-id="002fe-244">Preferințe resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-244">Resource preferences</span></span>
- <span data-ttu-id="002fe-245">Unitate organizațională preferată</span><span class="sxs-lookup"><span data-stu-id="002fe-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="002fe-246">Actualizați rezervările de resurse după ce sunt rezervate pe un proiect</span><span class="sxs-lookup"><span data-stu-id="002fe-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="002fe-247">După ce ați adăugat o resursă generică sau denumită într-o echipă de proiect, aveți posibilitatea să modificați rezervările resursei.</span><span class="sxs-lookup"><span data-stu-id="002fe-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="002fe-248">Pe pagina **Proiecte** , pe fila **Echipă** , selectați un membru al echipei și apoi selectați **Mențineți rezervări**.</span><span class="sxs-lookup"><span data-stu-id="002fe-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Consiliul de planificare deschis pentru membrul de echipă selectat](media/Resource-Management-image40.png)

    <span data-ttu-id="002fe-250">Consiliul de planificare apare și afișează rezervările membrilor echipei de proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="002fe-251">Extindeți înregistrarea membrului echipei pentru a vizualiza orele care au fost rezervate împotriva acestui proiect și a altor proiecte care consumă capacitatea membrului echipei.</span><span class="sxs-lookup"><span data-stu-id="002fe-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="002fe-252">Selectați și glisați rezervarea pentru a o prelungi sau scurta.</span><span class="sxs-lookup"><span data-stu-id="002fe-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="002fe-253">Va apărea o casetă de dialog **Creare rezervare de resursă** care vă permite să ajustați rezervarea.</span><span class="sxs-lookup"><span data-stu-id="002fe-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Creați o casetă de dialog de Rezervare resursă](media/Resource-Management-image41.png)

3. <span data-ttu-id="002fe-255">Faceți clic dreapta pe rezervare.</span><span class="sxs-lookup"><span data-stu-id="002fe-255">Right-click the booking.</span></span> <span data-ttu-id="002fe-256">Apoi, puteți utiliza meniul de comenzi rapide pentru a finaliza următoarele acțiuni:</span><span class="sxs-lookup"><span data-stu-id="002fe-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="002fe-257">Modificați starea rezervării.</span><span class="sxs-lookup"><span data-stu-id="002fe-257">Change the booking status.</span></span>
    - <span data-ttu-id="002fe-258">Editați rezervarea.</span><span class="sxs-lookup"><span data-stu-id="002fe-258">Edit the booking.</span></span>
    - <span data-ttu-id="002fe-259">Înlocuiți o resursă în echipa de proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="002fe-260">Modificați starea rezervării</span><span class="sxs-lookup"><span data-stu-id="002fe-260">Change the booking status</span></span>

<span data-ttu-id="002fe-261">Aveți posibilitatea să modificați orice stare de rezervare implicită sau particularizată.</span><span class="sxs-lookup"><span data-stu-id="002fe-261">You can change any default or custom booking status.</span></span>

![Modificați starea comenzii](media/Resource-Management-image42.png)

<span data-ttu-id="002fe-263">Următoarele stări sunt incluse în PSA:</span><span class="sxs-lookup"><span data-stu-id="002fe-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="002fe-264">**Anulat** – această stare anulează rezervarea unei resurse și eliberează capacitatea resursei.</span><span class="sxs-lookup"><span data-stu-id="002fe-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="002fe-265">**Rezervare fermă** - această stare consumă capacitatea unei resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="002fe-266">O rezervare are de obicei această stare atunci când deschideți **Mențineți rezervările** din grila **Toți membrii echipei** pe pagina **Proiecte**.</span><span class="sxs-lookup"><span data-stu-id="002fe-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="002fe-267">**Rezervare permisivă** – această stare adaugă o resursă unei echipe, dar nu consumă capacitatea resursei.</span><span class="sxs-lookup"><span data-stu-id="002fe-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="002fe-268">Acesta indică faptul că resursa a fost rezervat pentru lucru potențial, dar are încă capacitate în cazul în care este nevoie de alte procese.</span><span class="sxs-lookup"><span data-stu-id="002fe-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="002fe-269">În vederea disponibilității globale a resurselor, rezervările provizorii au o stare diferită față de rezervările ferme.</span><span class="sxs-lookup"><span data-stu-id="002fe-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="002fe-270">**Propus** – acest statut reprezintă o propunere de manager de resurse sau de manager de proiect pentru o resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="002fe-271">Propunerile nu consumă capacitatea unei resurse, iar resursa nu este adăugată echipei de proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="002fe-272">Pentru a rezerva ferm resursa pe echipă, managerul de proiect trebuie să accepte propunerea.</span><span class="sxs-lookup"><span data-stu-id="002fe-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="002fe-273">Trimiterea solicitărilor de resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-273">Submit resource requests</span></span>

<span data-ttu-id="002fe-274">Solicitările de resurse sunt utilizate pentru a purta cererea (solicitarea de resursă) care trebuie procesată de un manager de resurse.</span><span class="sxs-lookup"><span data-stu-id="002fe-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="002fe-275">Pentru o resursă generică care este deja în echipă, aveți posibilitatea să remiteți direct o solicitare de resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="002fe-276">O solicitare de resurse poate fi procesată în două moduri:</span><span class="sxs-lookup"><span data-stu-id="002fe-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="002fe-277">Managerul de resurse procesează direct solicitarea.</span><span class="sxs-lookup"><span data-stu-id="002fe-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="002fe-278">În acest caz, resursa generică este înlocuită de o rezervare fermă care are o resursă denumită.</span><span class="sxs-lookup"><span data-stu-id="002fe-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="002fe-279">Managerul de resurse propune o resursă pentru managerul de proiect, iar managerul de proiect aprobă sau respinge resursa propusă.</span><span class="sxs-lookup"><span data-stu-id="002fe-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="002fe-280">Procesarea directă a cererilor de resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="002fe-281">Atunci când se generează o cerință de resurse, un manager de proiect poate remite o solicitare de resurse pentru o resursă generică selectând resursa și apoi selectând **Remitere solicitarea**.</span><span class="sxs-lookup"><span data-stu-id="002fe-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Buton Remiteți solicitarea](media/Resource-Management-image45.png)

<span data-ttu-id="002fe-283">Comentariile despre resursă pot fi furnizate managerului de resurse care procesează solicitarea.</span><span class="sxs-lookup"><span data-stu-id="002fe-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="002fe-284">După depunerea solicitării, câmpul **Stare** pentru membrul echipei este modificat la **Remis**.</span><span class="sxs-lookup"><span data-stu-id="002fe-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Introducerea comentariilor opționale](media/Resource-Management-image46.png)

<span data-ttu-id="002fe-286">Când managerul de resurse procesează solicitarea, membrul generic de echipă este înlocuit de resursa denumită în grila **Toți membrii echipei**.</span><span class="sxs-lookup"><span data-stu-id="002fe-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Membrul generic al echipei înlocuit de resursa denumită în grila Toți membrii echipei](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="002fe-288">Utilizarea unei propuneri de resurse pentru solicitări de resurse</span><span class="sxs-lookup"><span data-stu-id="002fe-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="002fe-289">În loc să rezerve direct o resursă pe o solicitare de resurse, un manager de resurse poate propune o resursă pentru managerul de proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="002fe-290">Un manager de resurse poate utiliza această opțiune atunci când nu este disponibilă o potrivire exactă pentru cerințe.</span><span class="sxs-lookup"><span data-stu-id="002fe-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="002fe-291">Atunci când un manager de resurse propune o resursă, managerul de proiect vede că câmpul **Stare** pentru membrul generic de echipă este modificat la **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="002fe-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Statutul de membru generic al echipei s-a schimbat la Necesită revizuire](media/Resource-Management-image48.png)

<span data-ttu-id="002fe-293">Pentru a vizualiza resursa propusă împreună cu o vizualizare a efectului rezervării propunerii, faceți dublu clic pe membrul echipei care are o stare de **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="002fe-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="002fe-294">Apoi selectați fila **Resurse propuse**.</span><span class="sxs-lookup"><span data-stu-id="002fe-294">Then select the **Proposed Resources** tab.</span></span>

![Fila Resurse propuse](media/Resource-Management-image49.png)

<span data-ttu-id="002fe-296">Selectați **Acceptați toate propunerile** pentru a accepta toate resursele propuse sau **Respingeți toate propunerile** pentru a le respinge.</span><span class="sxs-lookup"><span data-stu-id="002fe-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="002fe-297">Dacă acceptați resursele propuse, acestea sunt ferm rezervate pe proiect ca membri ai echipei și înlocuiesc resursele generice.</span><span class="sxs-lookup"><span data-stu-id="002fe-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="002fe-298">Trebuie fie să acceptați, fie să respingeți toate resursele propuse.</span><span class="sxs-lookup"><span data-stu-id="002fe-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="002fe-299">Nu le puteți accepta parțial sau respinge.</span><span class="sxs-lookup"><span data-stu-id="002fe-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="002fe-300">Înlocuiți o resursă în echipa de proiect</span><span class="sxs-lookup"><span data-stu-id="002fe-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="002fe-301">Uneori, un manager de proiect trebuie să înlocuiască un membru al echipei rezervat într-un proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="002fe-302">Pe pagina **Proiecte** , pe fila **Echipă** , selectați resursa care are nevoie de o înlocuire și apoi selectați **Mențineți rezervări**.</span><span class="sxs-lookup"><span data-stu-id="002fe-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="002fe-303">Extindeți resursa pentru a vizualiza proiectele la care este atribuită.</span><span class="sxs-lookup"><span data-stu-id="002fe-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Resursă extinsă pentru a afișa proiectele atribuite](media/Resource-Management-image50.png)

3. <span data-ttu-id="002fe-305">Faceți clic dreapta pe proiect și apoi selectați **Înlocuitor resursă**.</span><span class="sxs-lookup"><span data-stu-id="002fe-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="002fe-306">Dacă cunoașteți resursa pe care doriți să o înlocuiți pentru resursa curentă, selectați sau tastați numele, apoi selectați **Reatribuire**.</span><span class="sxs-lookup"><span data-stu-id="002fe-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Specificarea unui substituent de resursă](media/Resource-Management-image51.png)

    <span data-ttu-id="002fe-308">Alternativ, urmați acești pași pentru a căuta o resursă:</span><span class="sxs-lookup"><span data-stu-id="002fe-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="002fe-309">Selectați **Găsire substituire**.</span><span class="sxs-lookup"><span data-stu-id="002fe-309">Select **Find Substitution**.</span></span>

        ![Căutarea unei resurse substituent](media/Resource-Management-image52.png)

        <span data-ttu-id="002fe-311">Asistentul de planificare returnează o listă de înlocuitori disponibili.</span><span class="sxs-lookup"><span data-stu-id="002fe-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="002fe-312">În Asistentul de planificare, puteți filtra și mai mult resursele disponibile pentru a găsi un substitut adecvat.</span><span class="sxs-lookup"><span data-stu-id="002fe-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Listă de înlocuitori disponibili](media/Resource-Management-image53.png)

    2. <span data-ttu-id="002fe-314">Pentru a înlocui resursa, selectați resursa dorită, apoi selectați **Înlocuitor**.</span><span class="sxs-lookup"><span data-stu-id="002fe-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Resursă de înlocuit selectată](media/Resource-Management-image54.png)

    <span data-ttu-id="002fe-316">Rezervările și atribuirile sunt înlocuite cu noua resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervări și atribuiri înlocuite cu noua resursă.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="002fe-318">Reconciliați rezervările și atribuirile membrilor echipei</span><span class="sxs-lookup"><span data-stu-id="002fe-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="002fe-319">Pentru membrii echipei, rezervările și atribuirile sunt cuplate lejer.</span><span class="sxs-lookup"><span data-stu-id="002fe-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="002fe-320">Cu alte cuvinte, resursele pot avea misiuni, dar nu rezervări, sau pot avea rezervări, dar nu atribuiri.</span><span class="sxs-lookup"><span data-stu-id="002fe-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="002fe-321">În mod ideal, rezervările și atribuirile ar trebui aliniate, astfel încât resursele au o capacitate angajată de a realiza activitățile atribuite.</span><span class="sxs-lookup"><span data-stu-id="002fe-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="002fe-322">Cu toate acestea, rezervările s-ar putea să se bazeze pe disponibilitate, iar timpii de activitate s-ar putea modifica pe măsură ce proiectul continuă.</span><span class="sxs-lookup"><span data-stu-id="002fe-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="002fe-323">Prin urmare, cuplarea lejeră a rezervărilor și atribuirilor furnizează flexibilitate.</span><span class="sxs-lookup"><span data-stu-id="002fe-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="002fe-324">PSA are o filă de **Reconciliere** care permite managerilor de proiect să reconcilieze rezervările membrilor echipei și atribuirile lor pentru echipele de proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Fila Reconciliere](media/Resource-Management-image56.png)

<span data-ttu-id="002fe-326">Fila **Reconciliere** afișează rezervările și atribuirile până la nivelul atribuirii individuale a activității pentru fiecare membru al echipei.</span><span class="sxs-lookup"><span data-stu-id="002fe-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="002fe-327">Acesta arată ore în celule, care pot reprezenta perioade de timp de la luni până la zile.</span><span class="sxs-lookup"><span data-stu-id="002fe-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="002fe-328">Fila afișează, de asemenea, un total net global pentru proiect, împreună cu o coloană totală.</span><span class="sxs-lookup"><span data-stu-id="002fe-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="002fe-329">Pentru fiecare resursă, fila calculează diferența dintre rezervările membrului echipei pe proiect și un cumulul al atribuirilor de activități ale acelui membru al echipei.</span><span class="sxs-lookup"><span data-stu-id="002fe-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="002fe-330">În mod ideal, această diferență ar trebui să fie 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="002fe-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="002fe-331">Cu alte cuvinte, nu ar trebui să existe nicio diferență între rezervări și atribuiri.</span><span class="sxs-lookup"><span data-stu-id="002fe-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="002fe-332">Diferențele sunt colorate și umbrite pentru a atrage atenția asupra a două condiții:</span><span class="sxs-lookup"><span data-stu-id="002fe-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="002fe-333">**Deficit de rezervare** - un deficit de rezervare apare atunci când o resursă are mai multe atribuiri decât rezervări.</span><span class="sxs-lookup"><span data-stu-id="002fe-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="002fe-334">Deoarece această capacitate nu a fost rezervată, un manager de proiect ar putea vrea să corecteze această condiție extinzând rezervările resursei pentru a acoperi deficitul.</span><span class="sxs-lookup"><span data-stu-id="002fe-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="002fe-335">**Rezervări în exces** – rezervările în exces apar atunci când o resursă a fost rezervată proiectului, dar nu a fost atribuită activităților.</span><span class="sxs-lookup"><span data-stu-id="002fe-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="002fe-336">Această condiție ar putea fi acceptabilă în cazurile în care resursa a fost rezervată la proiect înainte să aibă loc atribuirea activității.</span><span class="sxs-lookup"><span data-stu-id="002fe-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="002fe-337">Cu toate acestea, în alte cazuri, resursa nu este planificată să fie atribuită activităților.</span><span class="sxs-lookup"><span data-stu-id="002fe-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="002fe-338">În aceste cazuri, managerul de proiect ar trebui să ia în considerare anularea rezervările resursei, astfel încât capacitatea să poată fi utilizată pentru un alt proiect.</span><span class="sxs-lookup"><span data-stu-id="002fe-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="002fe-339">În unele cazuri, când vizualizați timpul la un nivel mai înalt decât nivelul zilei (de exemplu, nivelul lunii), este posibil să vedeți o diferență netă de zero pentru o resursă (cu alte cuvinte, rezervări = misiuni).</span><span class="sxs-lookup"><span data-stu-id="002fe-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="002fe-340">Cu toate acestea, dacă vă uitați la nivel de săptămână, este posibil să vedeți că există atribuiri de zero ore și rezervări de 40 ore în prima săptămână, dar atribuiri de 40 ore și rezervări de zero ore în a doua săptămână.</span><span class="sxs-lookup"><span data-stu-id="002fe-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="002fe-341">În general, rezervările și atribuirile sunt reconciliate, dar acestea diferă de la o săptămână la alta.</span><span class="sxs-lookup"><span data-stu-id="002fe-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="002fe-342">Când vizualizați timpul la nivele mai înalte, celulele din fila **Reconciliere** au un indicator pentru a vă informa că sunt diferențe la niveluri mai joase.</span><span class="sxs-lookup"><span data-stu-id="002fe-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="002fe-343">Făcând dublu clic într-o celulă, aveți posibilitatea să măriți pentru a vizualiza diferența.</span><span class="sxs-lookup"><span data-stu-id="002fe-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="002fe-344">Apoi puteți face clic dreapta pentru a micșora. Selectând o resursă și apoi utilizând controlul **Următoarea diferență** pe grila barei de instrumente, puteți trece la următoarea diferență dintre rezervări și atribuiri pentru acea resursă.</span><span class="sxs-lookup"><span data-stu-id="002fe-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="002fe-345">Apoi puteți utiliza controlul **Diferenței anterioare** pentru a reveni.</span><span class="sxs-lookup"><span data-stu-id="002fe-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="002fe-346">De asemenea, puteți dezactiva indicatorul de diferență și comportamentul de navigare sub **Setări**.</span><span class="sxs-lookup"><span data-stu-id="002fe-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indicator diferență](media/Resource-Management-image57.png)

<span data-ttu-id="002fe-348">DAcă aveți atribuiri de activități pentru o resursă dar nu rezervări pe pagina **Proiecte** , pe fila **Reconciliere** , selectați deficitul de rezervare și apoi selectați **Extindeți rezervarea**.</span><span class="sxs-lookup"><span data-stu-id="002fe-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="002fe-349">Apare caseta de dialog **Extindere rezervare** și afișează rezervarea necesară pentru a aborda deficitul resursei.</span><span class="sxs-lookup"><span data-stu-id="002fe-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="002fe-350">De asemenea, arată rezervările existente ale resursei în toate proiectele sau alte entități care pot fi planificate.</span><span class="sxs-lookup"><span data-stu-id="002fe-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="002fe-351">Dacă selectați **OK** pentru a crea rezervarea pentru resursă, indiferent de disponibilitatea acelei resurse, este posibil să cauzați o suprarezervare.</span><span class="sxs-lookup"><span data-stu-id="002fe-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Caseta de dialog extindere rezervare](media/Resource-Management-image58.png)

<span data-ttu-id="002fe-353">Managerul de proiect sau managerul de resurse pot utiliza apoi Panoul de planificare pentru a gestiona orice situații în care o resursă este suprarezervată peste capacitate.</span><span class="sxs-lookup"><span data-stu-id="002fe-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
