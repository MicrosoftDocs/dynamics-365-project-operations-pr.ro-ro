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
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082669"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="cf6c3-103">Configurați și aplicați datele de configurare în Common Data Service pentru Project Operations</span><span class="sxs-lookup"><span data-stu-id="cf6c3-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="cf6c3-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="cf6c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="cf6c3-105">Instalați datele de instalare și configurare</span><span class="sxs-lookup"><span data-stu-id="cf6c3-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="cf6c3-106">Descărcați, deblocați și dezarhivați fișierul [Setare și configurare pachet de date](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="cf6c3-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="cf6c3-107">Navigați la dosarul dezarhivat și rulați fișierul executabil, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="cf6c3-108">Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="cf6c3-110">Pe pagina 2 a expertului CMT, selectați **Microsoft 365** ca **Tip de implementare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="cf6c3-111">Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="cf6c3-112">Selectați regiunea entității dvs. găzduite, introduceți acreditările, apoi selectați **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Conectare de configurare](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="cf6c3-114">Pe pagina 3, din lista de organizații de pe entitatea găzduită, selectați organizația în care doriți să importați datele demo și apoi selectați **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="cf6c3-115">La pagina 4, selectați fișierul arhivat, *SampleSetupAndConfigData* din dosarul arhivat.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selecție fișier arhivat](./media/3ZipFile.png)

![Selectați un fișier](./media/4SelectAFile.png)

9. <span data-ttu-id="cf6c3-118">După selectarea fișierului zip, selectați **Importați date**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-118">After the zip file is selected, select **Import Data**.</span></span>

![Import date](./media/5ImportData.png)

10. <span data-ttu-id="cf6c3-120">Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="cf6c3-121">După ce se termină importarea, ieșiți din expertul CMT.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="cf6c3-122">Verificați organizația pentru date în următoarele 19 de entități:</span><span class="sxs-lookup"><span data-stu-id="cf6c3-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="cf6c3-123">Monedă</span><span class="sxs-lookup"><span data-stu-id="cf6c3-123">Currency</span></span>
  - <span data-ttu-id="cf6c3-124">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="cf6c3-124">Organizational Unit</span></span>
  - <span data-ttu-id="cf6c3-125">Contact</span><span class="sxs-lookup"><span data-stu-id="cf6c3-125">Contact</span></span>
  - <span data-ttu-id="cf6c3-126">Grup fiscal</span><span class="sxs-lookup"><span data-stu-id="cf6c3-126">Tax Group</span></span>
  - <span data-ttu-id="cf6c3-127">Grup de clienți</span><span class="sxs-lookup"><span data-stu-id="cf6c3-127">Customer Group</span></span>
  - <span data-ttu-id="cf6c3-128">Unitate</span><span class="sxs-lookup"><span data-stu-id="cf6c3-128">Unit</span></span>
  - <span data-ttu-id="cf6c3-129">Grup de unități</span><span class="sxs-lookup"><span data-stu-id="cf6c3-129">Unit Group</span></span>
  - <span data-ttu-id="cf6c3-130">Listă de prețuri</span><span class="sxs-lookup"><span data-stu-id="cf6c3-130">Price List</span></span>
  - <span data-ttu-id="cf6c3-131">Listă de prețuri parametru proiect</span><span class="sxs-lookup"><span data-stu-id="cf6c3-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="cf6c3-132">Frecvență factură</span><span class="sxs-lookup"><span data-stu-id="cf6c3-132">Invoice Frequency</span></span>
  - <span data-ttu-id="cf6c3-133">Categoria resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="cf6c3-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="cf6c3-134">Categorie tranzacție</span><span class="sxs-lookup"><span data-stu-id="cf6c3-134">Transaction Category</span></span>
  - <span data-ttu-id="cf6c3-135">Categorie de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="cf6c3-135">Expense Category</span></span>
  - <span data-ttu-id="cf6c3-136">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="cf6c3-136">Role Price</span></span>
  - <span data-ttu-id="cf6c3-137">Preț pentru categoria de tranzacție</span><span class="sxs-lookup"><span data-stu-id="cf6c3-137">Transaction Category Price</span></span>
  - <span data-ttu-id="cf6c3-138">Caracteristică</span><span class="sxs-lookup"><span data-stu-id="cf6c3-138">Characteristic</span></span>
  - <span data-ttu-id="cf6c3-139">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="cf6c3-139">Bookable Resource</span></span>
  - <span data-ttu-id="cf6c3-140">Asociere categorie resursă care se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="cf6c3-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="cf6c3-141">Caracteristică a resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="cf6c3-141">Bookable Resource Characteristic</span></span>

![Finalizați importul](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="cf6c3-143">Actualizați configurațiile Project Operations</span><span class="sxs-lookup"><span data-stu-id="cf6c3-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="cf6c3-144">Navigați la mediul CE.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-144">Navigate to the CE environment.</span></span> <span data-ttu-id="cf6c3-145">O puteți găsi deschizând fișierul [Centrul de administrare Power Platform](https://admin.powerplatform.microsoft.com/environments), selectând mediul, apoi selectând **Mediu deschis**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Mediu deschis](./media/7OpenEnvironment.png)

2. <span data-ttu-id="cf6c3-147">Accesați **Proiecte** > **Resurse** și apoi selectați **Nou** pentru a crea o resursă care se poate rezerva pentru utilizatorul dvs.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resurse ce se pot rezerva](./media/8BookableResources.png)

3. <span data-ttu-id="cf6c3-149">Pe fila **General** , selectați-vă utilizatorul de administrator.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="cf6c3-150">Verificați dacă fusul orar se potrivește cu cel în care vă aflați.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-150">Verify that the time zone matches the one you are in.</span></span> 

![Resursă nouă care se poate rezerva](./media/9NewBookableResource.png)

4. <span data-ttu-id="cf6c3-152">Pe fila **Planificare** , în câmpul **Companie** , alegeți compania **USPM** , apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Filă de planificare](./media/10SchedulingTab.png)

5. <span data-ttu-id="cf6c3-154">Selectați fila **Ore de lucru**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-154">Select the **Work hours** tab.</span></span>  

![Ore de lucru](./media/11WorkHours.png)

6. <span data-ttu-id="cf6c3-156">Faceți dublu clic pe orice valoare din calendar și selectați **Editați** > **Toate evenimentele din serie**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendar de lucru](./media/12WorkCalendar.png)

7. <span data-ttu-id="cf6c3-158">Schimbați orele de lucru într-o zi de lucru de opt (8) ore, marcați weekendurile ca zile nelucrătoare și asigurați-vă că fusul orar se potrivește cu al dvs.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="cf6c3-159">Selectați **Salvați și închideți**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-159">Select **Save and close**.</span></span>

![Actualizare calendar](./media/13UpdateCalendar.png)

9. <span data-ttu-id="cf6c3-161">Accesați **Setări** > **Șabloane de calendar** și selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Șabloane de calendar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="cf6c3-163">Introduceți un nume, selectați resursa șablon pe care ați creat-o, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvați șablonul de calendar](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="cf6c3-165">Accesați **Parametri** și faceți dublu clic pe înregistrare.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri proiect](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="cf6c3-167">Actualizați următoarele câmpuri:</span><span class="sxs-lookup"><span data-stu-id="cf6c3-167">Update the following fields:</span></span>

 - <span data-ttu-id="cf6c3-168">**Companie implicită** : USPM</span><span class="sxs-lookup"><span data-stu-id="cf6c3-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="cf6c3-169">**Unitate organizațională implicită** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="cf6c3-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="cf6c3-170">**Frecvența facturii** : a șaptea și ultima zi</span><span class="sxs-lookup"><span data-stu-id="cf6c3-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="cf6c3-171">**Șablon de oră de lucru** : modificați șablonul pe care l-ați creat.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="cf6c3-172">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="cf6c3-172">Select **Save**.</span></span> 

![Parametri de proiect actualizați](./media/17UpdatedProjectParameters.png)
