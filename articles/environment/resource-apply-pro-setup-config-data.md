---
title: Instalați și aplicați datele de configurare în Common Data Service
description: Acest subiect furnizează informații despre configurare și aplicarea datelor de configurare în Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642243"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="0f711-103">Instalați și aplicați datele de configurare în Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0f711-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="0f711-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="0f711-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="0f711-105">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="0f711-105">Prerequisites</span></span>

<span data-ttu-id="0f711-106">Înainte de a începe să configurați datele în Common Data Service (CDS), trebuie îndeplinite următoarele condiții prealabile:</span><span class="sxs-lookup"><span data-stu-id="0f711-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="0f711-107">Furnizați un mediu CDS și un mediu Dynamics 365 Finance pentru Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0f711-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="0f711-108">Informații privind entitatea juridică de la Dynamics 365 Finance este partajat mediului CDS.</span><span class="sxs-lookup"><span data-stu-id="0f711-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="0f711-109">Aceasta înseamnă că entitatea **Companie** din CDS are următoarele înregistrări ale companiei:</span><span class="sxs-lookup"><span data-stu-id="0f711-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="0f711-110">THPM</span><span class="sxs-lookup"><span data-stu-id="0f711-110">THPM</span></span>
  - <span data-ttu-id="0f711-111">USPM</span><span class="sxs-lookup"><span data-stu-id="0f711-111">USPM</span></span>
  - <span data-ttu-id="0f711-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="0f711-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="0f711-113">Instalați datele de instalare și configurare</span><span class="sxs-lookup"><span data-stu-id="0f711-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="0f711-114">Descărcați, deblocați și dezarhivați fișierul [Setare și configurare pachet de date](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="0f711-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="0f711-115">Navigați la dosarul dezarhivat și rulați fișierul executabil, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="0f711-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="0f711-116">Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="0f711-118">Pe pagina 2 a expertului CMT, selectați **Microsoft 365** ca **Tip de implementare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="0f711-119">Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.</span><span class="sxs-lookup"><span data-stu-id="0f711-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="0f711-120">Selectați regiunea entității dvs. găzduite, introduceți acreditările, apoi selectați **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Conectare de configurare](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="0f711-122">Pe pagina 3, din lista de organizații de pe entitatea găzduită, selectați organizația în care doriți să importați datele demo și apoi selectați **Conectare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="0f711-123">La pagina 4, selectați fișierul arhivat, *SampleSetupAndConfigData* din dosarul arhivat.</span><span class="sxs-lookup"><span data-stu-id="0f711-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Selecție fișier arhivat](./media/3ZipFile.png)

![Selectați un fișier](./media/4SelectAFile.png)

9. <span data-ttu-id="0f711-126">După selectarea fișierului zip, selectați **Importați date**.</span><span class="sxs-lookup"><span data-stu-id="0f711-126">After the zip file is selected, select **Import Data**.</span></span>

![Import date](./media/5ImportData.png)

10. <span data-ttu-id="0f711-128">Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei.</span><span class="sxs-lookup"><span data-stu-id="0f711-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="0f711-129">După ce se termină importarea, ieșiți din expertul CMT.</span><span class="sxs-lookup"><span data-stu-id="0f711-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="0f711-130">Verificați organizația pentru date în următoarele 19 de entități:</span><span class="sxs-lookup"><span data-stu-id="0f711-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="0f711-131">Monedă</span><span class="sxs-lookup"><span data-stu-id="0f711-131">Currency</span></span>
  - <span data-ttu-id="0f711-132">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="0f711-132">Organizational Unit</span></span>
  - <span data-ttu-id="0f711-133">Contact</span><span class="sxs-lookup"><span data-stu-id="0f711-133">Contact</span></span>
  - <span data-ttu-id="0f711-134">Grup fiscal</span><span class="sxs-lookup"><span data-stu-id="0f711-134">Tax Group</span></span>
  - <span data-ttu-id="0f711-135">Grup de clienți</span><span class="sxs-lookup"><span data-stu-id="0f711-135">Customer Group</span></span>
  - <span data-ttu-id="0f711-136">Unitate</span><span class="sxs-lookup"><span data-stu-id="0f711-136">Unit</span></span>
  - <span data-ttu-id="0f711-137">Grup de unități</span><span class="sxs-lookup"><span data-stu-id="0f711-137">Unit Group</span></span>
  - <span data-ttu-id="0f711-138">Listă de prețuri</span><span class="sxs-lookup"><span data-stu-id="0f711-138">Price List</span></span>
  - <span data-ttu-id="0f711-139">Listă de prețuri parametru proiect</span><span class="sxs-lookup"><span data-stu-id="0f711-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="0f711-140">Frecvență factură</span><span class="sxs-lookup"><span data-stu-id="0f711-140">Invoice Frequency</span></span>
  - <span data-ttu-id="0f711-141">Categoria resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="0f711-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="0f711-142">Categorie tranzacție</span><span class="sxs-lookup"><span data-stu-id="0f711-142">Transaction Category</span></span>
  - <span data-ttu-id="0f711-143">Categorie de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="0f711-143">Expense Category</span></span>
  - <span data-ttu-id="0f711-144">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="0f711-144">Role Price</span></span>
  - <span data-ttu-id="0f711-145">Preț pentru categoria de tranzacție</span><span class="sxs-lookup"><span data-stu-id="0f711-145">Transaction Category Price</span></span>
  - <span data-ttu-id="0f711-146">Caracteristică</span><span class="sxs-lookup"><span data-stu-id="0f711-146">Characteristic</span></span>
  - <span data-ttu-id="0f711-147">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="0f711-147">Bookable Resource</span></span>
  - <span data-ttu-id="0f711-148">Asociere categorie resursă care se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="0f711-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="0f711-149">Caracteristică a resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="0f711-149">Bookable Resource Characteristic</span></span>

![Finalizați importul](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="0f711-151">Actualizați configurațiile Project Operations</span><span class="sxs-lookup"><span data-stu-id="0f711-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="0f711-152">Navigați la mediul CE.</span><span class="sxs-lookup"><span data-stu-id="0f711-152">Navigate to the CE environment.</span></span> <span data-ttu-id="0f711-153">O puteți găsi deschizând fișierul [Centrul de administrare Power Platform](https://admin.powerplatform.microsoft.com/environments), selectând mediul, apoi selectând **Mediu deschis**.</span><span class="sxs-lookup"><span data-stu-id="0f711-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Mediu deschis](./media/7OpenEnvironment.png)

2. <span data-ttu-id="0f711-155">Accesați **Proiecte** > **Resurse** și apoi selectați **Nou** pentru a crea o resursă care se poate rezerva pentru utilizatorul dvs.</span><span class="sxs-lookup"><span data-stu-id="0f711-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resurse ce se pot rezerva](./media/8BookableResources.png)

3. <span data-ttu-id="0f711-157">Pe fila **General**, selectați-vă utilizatorul de administrator.</span><span class="sxs-lookup"><span data-stu-id="0f711-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="0f711-158">Verificați dacă fusul orar se potrivește cu cel în care vă aflați.</span><span class="sxs-lookup"><span data-stu-id="0f711-158">Verify that the time zone matches the one you are in.</span></span> 

![Resursă nouă care se poate rezerva](./media/9NewBookableResource.png)

4. <span data-ttu-id="0f711-160">Pe fila **Planificare**, în câmpul **Companie**, alegeți compania **USPM**, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Filă de planificare](./media/10SchedulingTab.png)

5. <span data-ttu-id="0f711-162">Selectați fila **Ore de lucru**.</span><span class="sxs-lookup"><span data-stu-id="0f711-162">Select the **Work hours** tab.</span></span>  

![Ore de lucru](./media/11WorkHours.png)

6. <span data-ttu-id="0f711-164">Faceți dublu clic pe orice valoare din calendar și selectați **Editați** > **Toate evenimentele din serie**.</span><span class="sxs-lookup"><span data-stu-id="0f711-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendar de lucru](./media/12WorkCalendar.png)

7. <span data-ttu-id="0f711-166">Schimbați orele de lucru într-o zi de lucru de opt (8) ore, marcați weekendurile ca zile nelucrătoare și asigurați-vă că fusul orar se potrivește cu al dvs.</span><span class="sxs-lookup"><span data-stu-id="0f711-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="0f711-167">Selectați **Salvați și închideți**.</span><span class="sxs-lookup"><span data-stu-id="0f711-167">Select **Save and close**.</span></span>

![Actualizare calendar](./media/13UpdateCalendar.png)

9. <span data-ttu-id="0f711-169">Accesați **Setări** > **Șabloane de calendar** și selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="0f711-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Șabloane de calendar](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="0f711-171">Introduceți un nume, selectați resursa șablon pe care ați creat-o, apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Salvați șablonul de calendar](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="0f711-173">Accesați **Parametri** și faceți dublu clic pe înregistrare.</span><span class="sxs-lookup"><span data-stu-id="0f711-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri proiect](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="0f711-175">Actualizați următoarele câmpuri:</span><span class="sxs-lookup"><span data-stu-id="0f711-175">Update the following fields:</span></span>

 - <span data-ttu-id="0f711-176">**Companie implicită**: USPM</span><span class="sxs-lookup"><span data-stu-id="0f711-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="0f711-177">**Unitate organizațională implicită**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="0f711-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="0f711-178">**Frecvența facturii**: a șaptea și ultima zi</span><span class="sxs-lookup"><span data-stu-id="0f711-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="0f711-179">**Șablon de oră de lucru**: modificați șablonul pe care l-ați creat.</span><span class="sxs-lookup"><span data-stu-id="0f711-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="0f711-180">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="0f711-180">Select **Save**.</span></span> 

![Parametri de proiect actualizați](./media/17UpdatedProjectParameters.png)
