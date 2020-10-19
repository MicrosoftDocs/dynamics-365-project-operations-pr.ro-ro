---
title: Configurați și aplicați datele de configurare în Common Data Service pentru Project Operations
description: Acest subiect furnizează informații despre configurare și aplicarea datelor de configurare în Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949030"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="f7701-103">Configurați și aplicați datele de configurare în Common Data Service pentru Project Operations</span><span class="sxs-lookup"><span data-stu-id="f7701-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="f7701-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="f7701-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="f7701-105">Instalați datele de instalare și configurare</span><span class="sxs-lookup"><span data-stu-id="f7701-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="f7701-106">Descărcați, deblocați și dezarhivați fișierul [Setare și configurare pachet de date](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="f7701-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="f7701-107">Navigați la dosarul dezarhivat și rulați fișierul executabil, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f7701-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f7701-108">Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f7701-110">Pe pagina 2 a Expertului CMT, selectați **Office 365** după **Tipul de implementare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f7701-111">Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.</span><span class="sxs-lookup"><span data-stu-id="f7701-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f7701-112">Selectați regiunea entității dvs. găzduite, introduceți acreditările, apoi selectați **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Conectare de configurare](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f7701-114">Pe pagina 3, din lista de organizații de pe entitatea găzduită, selectați organizația în care doriți să importați datele demo și apoi selectați **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="f7701-115">La pagina 4, selectați fișierul arhivat, *SampleSetupAndConfigData* din dosarul arhivat.</span><span class="sxs-lookup"><span data-stu-id="f7701-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selecție fișier arhivat](./media/3ZipFile.png)

![Selectați un fișier](./media/4SelectAFile.png)

9. <span data-ttu-id="f7701-118">După selectarea fișierului zip, selectați **Importați date**.</span><span class="sxs-lookup"><span data-stu-id="f7701-118">After the zip file is selected, select **Import Data**.</span></span>

![Import date](./media/5ImportData.png)

10. <span data-ttu-id="f7701-120">Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei.</span><span class="sxs-lookup"><span data-stu-id="f7701-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f7701-121">După ce se termină importarea, ieșiți din expertul CMT.</span><span class="sxs-lookup"><span data-stu-id="f7701-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f7701-122">Verificați organizația pentru date în următoarele 19 de entități:</span><span class="sxs-lookup"><span data-stu-id="f7701-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="f7701-123">Monedă</span><span class="sxs-lookup"><span data-stu-id="f7701-123">Currency</span></span>
  - <span data-ttu-id="f7701-124">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="f7701-124">Organizational Unit</span></span>
  - <span data-ttu-id="f7701-125">Contact</span><span class="sxs-lookup"><span data-stu-id="f7701-125">Contact</span></span>
  - <span data-ttu-id="f7701-126">Grup fiscal</span><span class="sxs-lookup"><span data-stu-id="f7701-126">Tax Group</span></span>
  - <span data-ttu-id="f7701-127">Grup de clienți</span><span class="sxs-lookup"><span data-stu-id="f7701-127">Customer Group</span></span>
  - <span data-ttu-id="f7701-128">Unitate</span><span class="sxs-lookup"><span data-stu-id="f7701-128">Unit</span></span>
  - <span data-ttu-id="f7701-129">Grup de unități</span><span class="sxs-lookup"><span data-stu-id="f7701-129">Unit Group</span></span>
  - <span data-ttu-id="f7701-130">Listă de prețuri</span><span class="sxs-lookup"><span data-stu-id="f7701-130">Price List</span></span>
  - <span data-ttu-id="f7701-131">Listă de prețuri parametru proiect</span><span class="sxs-lookup"><span data-stu-id="f7701-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="f7701-132">Frecvență factură</span><span class="sxs-lookup"><span data-stu-id="f7701-132">Invoice Frequency</span></span>
  - <span data-ttu-id="f7701-133">Categoria resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="f7701-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="f7701-134">Categorie tranzacție</span><span class="sxs-lookup"><span data-stu-id="f7701-134">Transaction Category</span></span>
  - <span data-ttu-id="f7701-135">Categorie de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="f7701-135">Expense Category</span></span>
  - <span data-ttu-id="f7701-136">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="f7701-136">Role Price</span></span>
  - <span data-ttu-id="f7701-137">Preț pentru categoria de tranzacție</span><span class="sxs-lookup"><span data-stu-id="f7701-137">Transaction Category Price</span></span>
  - <span data-ttu-id="f7701-138">Caracteristică</span><span class="sxs-lookup"><span data-stu-id="f7701-138">Characteristic</span></span>
  - <span data-ttu-id="f7701-139">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="f7701-139">Bookable Resource</span></span>
  - <span data-ttu-id="f7701-140">Asociere categorie resursă care se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="f7701-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="f7701-141">Caracteristică a resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="f7701-141">Bookable Resource Characteristic</span></span>

![Finalizați importul](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="f7701-143">Actualizați configurațiile Project Operations</span><span class="sxs-lookup"><span data-stu-id="f7701-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="f7701-144">Navigați la mediul CE.</span><span class="sxs-lookup"><span data-stu-id="f7701-144">Navigate to the CE environment.</span></span> <span data-ttu-id="f7701-145">O puteți găsi deschizând fișierul [Centrul de administrare Power Platform](https://admin.powerplatform.microsoft.com/environments), selectând mediul, apoi selectând **Mediu deschis**.</span><span class="sxs-lookup"><span data-stu-id="f7701-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Mediu deschis](./media/7OpenEnvironment.png)

2. <span data-ttu-id="f7701-147">Accesați **Proiecte** > **Resurse** și apoi selectați **Nou** pentru a crea o resursă care se poate rezerva pentru utilizatorul dvs.</span><span class="sxs-lookup"><span data-stu-id="f7701-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resurse ce se pot rezerva](./media/8BookableResources.png)

3. <span data-ttu-id="f7701-149">Pe fila **General**, selectați-vă utilizatorul de administrator.</span><span class="sxs-lookup"><span data-stu-id="f7701-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="f7701-150">Verificați dacă fusul orar se potrivește cu cel în care vă aflați.</span><span class="sxs-lookup"><span data-stu-id="f7701-150">Verify that the time zone matches the one you are in.</span></span> 

![Resursă nouă care se poate rezerva](./media/9NewBookableResource.png)

4. <span data-ttu-id="f7701-152">Pe fila **Planificare**, în câmpul **Companie**, alegeți compania **USPM**, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Filă de planificare](./media/10SchedulingTab.png)

5. <span data-ttu-id="f7701-154">Selectați fila **Ore de lucru**.</span><span class="sxs-lookup"><span data-stu-id="f7701-154">Select the **Work hours** tab.</span></span>  

![Ore de lucru](./media/11WorkHours.png)

6. <span data-ttu-id="f7701-156">Faceți dublu clic pe orice valoare din calendar și selectați **Editați** > **Toate evenimentele din serie**.</span><span class="sxs-lookup"><span data-stu-id="f7701-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendar de lucru](./media/12WorkCalendar.png)

7. <span data-ttu-id="f7701-158">Schimbați orele de lucru într-o zi de lucru de opt (8) ore, marcați weekendurile ca zile nelucrătoare și asigurați-vă că fusul orar se potrivește cu al dvs.</span><span class="sxs-lookup"><span data-stu-id="f7701-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="f7701-159">Selectați **Salvați și închideți**.</span><span class="sxs-lookup"><span data-stu-id="f7701-159">Select **Save and close**.</span></span>

![Actualizare calendar](./media/13UpdateCalendar.png)

9. <span data-ttu-id="f7701-161">Accesați **Setări** > **Șabloane de calendar** și selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="f7701-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Șabloane de calendar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="f7701-163">Introduceți un nume, selectați resursa șablon pe care ați creat-o, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvați șablonul de calendar](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="f7701-165">Accesați **Parametri** și faceți dublu clic pe înregistrare.</span><span class="sxs-lookup"><span data-stu-id="f7701-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri proiect](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="f7701-167">Actualizați următoarele câmpuri:</span><span class="sxs-lookup"><span data-stu-id="f7701-167">Update the following fields:</span></span>

 - <span data-ttu-id="f7701-168">**Companie implicită**: USPM</span><span class="sxs-lookup"><span data-stu-id="f7701-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="f7701-169">**Unitate organizațională implicită**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="f7701-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="f7701-170">**Frecvența facturii**: a șaptea și ultima zi</span><span class="sxs-lookup"><span data-stu-id="f7701-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="f7701-171">**Șablon de oră de lucru**: modificați șablonul pe care l-ați creat.</span><span class="sxs-lookup"><span data-stu-id="f7701-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="f7701-172">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="f7701-172">Select **Save**.</span></span> 

![Parametri de proiect actualizați](./media/17UpdatedProjectParameters.png)
