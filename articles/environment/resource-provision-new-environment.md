---
title: Asigurarea accesului pentru un nou mediu
description: Acest subiect furnizează informații despre ucm să provizionați un nou mediu Project Operations.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 50e623d3716c9dd03ce34ec293ba57b5d966d39e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276903"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="abe40-103">Asigurarea accesului pentru un nou mediu</span><span class="sxs-lookup"><span data-stu-id="abe40-103">Provision a new environment</span></span>

<span data-ttu-id="abe40-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="abe40-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="abe40-105">Acest subiect furnizează informații despre cum să furnizați un mediu nou Dynamics 365 Project Operations pentru scenarii bazate pe resurse/fără stoc.</span><span class="sxs-lookup"><span data-stu-id="abe40-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="abe40-106">Activați pregătirea automată a Project Operations într-un proiect LCS</span><span class="sxs-lookup"><span data-stu-id="abe40-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="abe40-107">Utilizați pașii următori pentru a activa fluxul automatizat de pregătire pentru Project Operations pentru proiectul dvs. LCS.</span><span class="sxs-lookup"><span data-stu-id="abe40-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="abe40-108">Accesați [LCS](https://lcs.dynamics.com/v2) și selectați titlul **Previzualizarea gestionării caracteristicilor**.</span><span class="sxs-lookup"><span data-stu-id="abe40-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="abe40-109">În lista **Caracteristică de previzualizare**, selectați **Caracteristică Project Operations** și apoi selectați **Caracteristica de previzualizare activată** pentru a activa Project Operations.</span><span class="sxs-lookup"><span data-stu-id="abe40-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="abe40-110">Acest pas se efectuează o singură dată pentru fiecare proiect LCS.</span><span class="sxs-lookup"><span data-stu-id="abe40-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="abe40-111">Furnizarea unui mediu de Project Operations</span><span class="sxs-lookup"><span data-stu-id="abe40-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="abe40-112">Deschideți un nou Dynamics 365 Finance [mediul demonstrativ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) sau o implementare [sandbox/ mediu de producție](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="abe40-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="abe40-113">Vom arăta expertul **Pregătirea mediului**.</span><span class="sxs-lookup"><span data-stu-id="abe40-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="abe40-114">Asigurați-vă că versiunea aplicației selectate este 10.0.13 sau mai mare.</span><span class="sxs-lookup"><span data-stu-id="abe40-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="abe40-115">Pentru a pregări Project Operations, în secțiunea **Setări avansate**, selectați **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="abe40-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="abe40-116">Activați **Common Data Service Setarea** prin selectarea **Da** și apoi introduceți informații în câmpurile obligatorii:</span><span class="sxs-lookup"><span data-stu-id="abe40-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="abe40-117">Nume</span><span class="sxs-lookup"><span data-stu-id="abe40-117">Name</span></span>
  - <span data-ttu-id="abe40-118">Regiune</span><span class="sxs-lookup"><span data-stu-id="abe40-118">Region</span></span>
  - <span data-ttu-id="abe40-119">Limbă</span><span class="sxs-lookup"><span data-stu-id="abe40-119">Language</span></span>
  - <span data-ttu-id="abe40-120">Monedă</span><span class="sxs-lookup"><span data-stu-id="abe40-120">Currency</span></span>
 
5. <span data-ttu-id="abe40-121">În câmpul **Common Data Service Șablon**, selectați **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="abe40-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="abe40-122">Selectați tipul de mediu pentru implementarea dvs.</span><span class="sxs-lookup"><span data-stu-id="abe40-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="abe40-123">O versiune de probă bazată pe abonament vă va permite să implementați un mediu CDS timp de 30 de zile.</span><span class="sxs-lookup"><span data-stu-id="abe40-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Setări de implementare](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="abe40-125">Selectați **De acord** pentru a confirma condițiile de utilizare și apoi selectați **Terminat** pentru a reveni la setările de implementare.</span><span class="sxs-lookup"><span data-stu-id="abe40-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Acord de implementare](./media/2DeploymentConsent.png)

7. <span data-ttu-id="abe40-127">Opțional - Aplicați date demonstrative pentru mediu.</span><span class="sxs-lookup"><span data-stu-id="abe40-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="abe40-128">Mergi la **Setări avansate**, Selectați **Personalizați configurația bazei de date SQL**, și setați **Specificați un set de date pentru baza de date a aplicației** la **Demonstrativ**.</span><span class="sxs-lookup"><span data-stu-id="abe40-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="abe40-129">Completați câmpurile obligatorii rămase în expert și confirmați implementarea.</span><span class="sxs-lookup"><span data-stu-id="abe40-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="abe40-130">Timpul de aprovizionare a mediului variază în funcție de tipul de mediu.</span><span class="sxs-lookup"><span data-stu-id="abe40-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="abe40-131">Pregătirea poate dura până la șase ore.</span><span class="sxs-lookup"><span data-stu-id="abe40-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="abe40-132">După ce implementarea se finalizează cu succes, mediul se va afișa ca **Implementat**.</span><span class="sxs-lookup"><span data-stu-id="abe40-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="abe40-133">Pentru a confirma că mediul a fost implementat cu succes, selectați **Autentificare** și conectați-vă la mediu pentru a confirma.</span><span class="sxs-lookup"><span data-stu-id="abe40-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalii despre mediu](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="abe40-135">Aplicați actualizările la mediul de finanțe</span><span class="sxs-lookup"><span data-stu-id="abe40-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="abe40-136">Project Operations necesită un mediu financiar cu versiunea aplicației **10.0.13 (10.0.569.20009)** sau mai recentă.</span><span class="sxs-lookup"><span data-stu-id="abe40-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="abe40-137">Este posibil să trebuiască să aplicați actualizări de calitate mediului dvs. financiar pentru a primi această versiune.</span><span class="sxs-lookup"><span data-stu-id="abe40-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="abe40-138">În LCS, pe pagina **Detalii despre mediu**, în secțiunea **Actualizări disponibile**, selectați **Vizualizare actualizare**.</span><span class="sxs-lookup"><span data-stu-id="abe40-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Vizualizare actualizări](./media/5ViewUpdates.png)

2. <span data-ttu-id="abe40-140">Pe pagina **Actualizări binare**, selectați **Salvați pachetul.**</span><span class="sxs-lookup"><span data-stu-id="abe40-140">On the **Binary updates** page, select **Save package.**</span></span>

![Salvați pachetul](./media/6SavePackage.png)

3. <span data-ttu-id="abe40-142">Faceți clic pe **Selectați tot** și apoi selectați **Salvați pachetul**.</span><span class="sxs-lookup"><span data-stu-id="abe40-142">Click **Select all** and then select **Save package**.</span></span>

![Revizuiți și salvați actualizările](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="abe40-144">Introduceți un nume și o descriere a pachetului, apoi selectați **Salvați**.</span><span class="sxs-lookup"><span data-stu-id="abe40-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="abe40-145">În funcție de conexiunea la internet, acest proces poate dura ceva timp.</span><span class="sxs-lookup"><span data-stu-id="abe40-145">Depending on the internet connection, this process might take some time.</span></span>

![Încărcați pachetul în Biblioteca de active](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="abe40-147">După salvarea pachetului, selectați **Terminat** și salvați acest pachet în biblioteca Active din proiectul dvs. LCS.</span><span class="sxs-lookup"><span data-stu-id="abe40-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="abe40-148">Salvarea și validarea pachetului ar putea dura aproximativ 15 minute.</span><span class="sxs-lookup"><span data-stu-id="abe40-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="abe40-149">Pentru a aplica actualizarea, navigați la pagina **Detalii despre mediu** în LCS și selectați **Menţine** > **Aplicați actualizări**.</span><span class="sxs-lookup"><span data-stu-id="abe40-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Mențineți mediile](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="abe40-151">În lista de actualizări, selectați pachetul pe care l-ați creat și selectați **Aplicare**.</span><span class="sxs-lookup"><span data-stu-id="abe40-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicați actualizări](./media/10ApplyUpdates.png)

<span data-ttu-id="abe40-153">Întreținerea mediului va dura ceva timp.</span><span class="sxs-lookup"><span data-stu-id="abe40-153">Environment servicing will take some time.</span></span> <span data-ttu-id="abe40-154">După ce este complet, mediul va reveni la o stare implementată.</span><span class="sxs-lookup"><span data-stu-id="abe40-154">After it is complete, the environment will return to a deployed state.</span></span>

![Mediu implementat](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="abe40-156">Stabiliți o conexiune Dual Write</span><span class="sxs-lookup"><span data-stu-id="abe40-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="abe40-157">În proiectul dvs. LCS, accesați pagina **Detalii despre mediu**.</span><span class="sxs-lookup"><span data-stu-id="abe40-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="abe40-158">Sub **Common Data Service Informații despre mediu**, selectați **Link către CDS pentru aplicații**.</span><span class="sxs-lookup"><span data-stu-id="abe40-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="abe40-159">După ce linkul este complet, selectați din nou **Link către CDS pentru aplicații**.</span><span class="sxs-lookup"><span data-stu-id="abe40-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="abe40-160">Veți fi redirecționat către Dual Write în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="abe40-160">You will be redirected to Dual Write in Finance.</span></span>

![Link la CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="abe40-162">Selectați **Aplicați soluția** pentru a accesa entitățile care vor fi mapate în integrare.</span><span class="sxs-lookup"><span data-stu-id="abe40-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicați soluții](./media/13ApplySolutions.png)

5. <span data-ttu-id="abe40-164">Selectați ambele soluții, **Dynamics 365 Finance and Operations Harta entității cu scriere dublă** și **Dynamics 365 Project Operations Hărți cu entități de scriere duală**, apoi selectați **Aplicare**.</span><span class="sxs-lookup"><span data-stu-id="abe40-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Confirmați soluțiile](./media/14ConfirmSolutions.png)

<span data-ttu-id="abe40-166">După aplicarea soluțiilor, entitățile Dual Write sunt aplicate mediului.</span><span class="sxs-lookup"><span data-stu-id="abe40-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicarea soluțiilor](./media/15ApplyingSolutions.png)

<span data-ttu-id="abe40-168">După aplicarea entităților, toate mapările disponibile sunt listate în mediu.</span><span class="sxs-lookup"><span data-stu-id="abe40-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Hărți Dual Write](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="abe40-170">Reîmprospătați entitățile de date după actualizare</span><span class="sxs-lookup"><span data-stu-id="abe40-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="abe40-171">În Finanțe, accesați spațiul de lucru **Gestionarea datelor**..</span><span class="sxs-lookup"><span data-stu-id="abe40-171">In Finance, go to the **Data management** workspace.</span></span>

![Spațiul de lucru pentru gestionarea datelor](./media/16DataManagement.png)

2. <span data-ttu-id="abe40-173">Selectați dala **Parametrii cadru**.</span><span class="sxs-lookup"><span data-stu-id="abe40-173">Select the **Framework parameters** tile.</span></span>

![Parametrii de cadru](./media/17FrameworkParameters.png)

3. <span data-ttu-id="abe40-175">Pe pagina **Setări entitate**, selectați **Reîmprospătați lista entităților**.</span><span class="sxs-lookup"><span data-stu-id="abe40-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Reîmprospătare listă entitate](./media/18RefreshEntityList.png)

<span data-ttu-id="abe40-177">Reîmprospătarea va dura aproximativ 20 de minute.</span><span class="sxs-lookup"><span data-stu-id="abe40-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="abe40-178">Veți primi o alertă când aceasta este completă.</span><span class="sxs-lookup"><span data-stu-id="abe40-178">You will receive an alert when it is complete.</span></span>

![Reîmprospătare confirmare](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="abe40-180">Actualizați setările de securitate pentru Project Operations pe Dataverse</span><span class="sxs-lookup"><span data-stu-id="abe40-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="abe40-181">Mergeți la Project Operations pe mediul dvs. Dataverse.</span><span class="sxs-lookup"><span data-stu-id="abe40-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="abe40-182">Accesați **Setări** > **Securitate** > **Roluri de securitate**.</span><span class="sxs-lookup"><span data-stu-id="abe40-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="abe40-183">Pe pagina **Roluri de securitate**, în lista de roluri, selectați **utilizator de aplicație cu scriere duală** și selectați fila **Entități personalizate**.</span><span class="sxs-lookup"><span data-stu-id="abe40-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="abe40-184">Verificați dacă rolul are permisiunile **Citit** și **Adăuga la** pentru:</span><span class="sxs-lookup"><span data-stu-id="abe40-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="abe40-185">**Tipul cursului de schimb valutar**</span><span class="sxs-lookup"><span data-stu-id="abe40-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="abe40-186">**Plan de conturi**</span><span class="sxs-lookup"><span data-stu-id="abe40-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="abe40-187">**Calendar fiscal**</span><span class="sxs-lookup"><span data-stu-id="abe40-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="abe40-188">**Registru**</span><span class="sxs-lookup"><span data-stu-id="abe40-188">**Ledger**</span></span>

5. <span data-ttu-id="abe40-189">După actualizarea rolului de securitate, accesați **Setări** > **Securitate** > **Echipe** și selectați echipa implicită în vizualizarea de echipă **Proprietar de afaceri locale**.</span><span class="sxs-lookup"><span data-stu-id="abe40-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="abe40-190">Selectați **Gestionați rolurile** și verificați dacă privilegiul de securitate **utilizator de aplicație cu scriere duală** este aplicabil pentru această echipă.</span><span class="sxs-lookup"><span data-stu-id="abe40-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="abe40-191">Rulare hărți Project Operations Dual Write</span><span class="sxs-lookup"><span data-stu-id="abe40-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="abe40-192">În proiectul dvs. LCS, accesați pagina **Detalii despre mediu**.</span><span class="sxs-lookup"><span data-stu-id="abe40-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="abe40-193">Sub **Common Data Service Informații despre mediu**, selectați **Link către CDS pentru aplicații.**</span><span class="sxs-lookup"><span data-stu-id="abe40-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="abe40-194">După ce selectați linkul, veți fi redirecționat către lista entităților din mapări.</span><span class="sxs-lookup"><span data-stu-id="abe40-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="abe40-195">Porniți hărțile așa cum este descris în tabelul următor.</span><span class="sxs-lookup"><span data-stu-id="abe40-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="abe40-196">Asigurați-vă că urmați secvența așa cum este listată.</span><span class="sxs-lookup"><span data-stu-id="abe40-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="abe40-197">**Mapare entități**</span><span class="sxs-lookup"><span data-stu-id="abe40-197">**Entity Map**</span></span> | <span data-ttu-id="abe40-198">**Reîmprospătați entitatea**</span><span class="sxs-lookup"><span data-stu-id="abe40-198">**Refresh entity**</span></span> | <span data-ttu-id="abe40-199">**Sincronizare inițială**</span><span class="sxs-lookup"><span data-stu-id="abe40-199">**Initial sync**</span></span> | <span data-ttu-id="abe40-200">**Coordonator pentru sincronizarea inițială**</span><span class="sxs-lookup"><span data-stu-id="abe40-200">**Master for initial sync**</span></span> | <span data-ttu-id="abe40-201">**Rulați cerințe preliminare**</span><span class="sxs-lookup"><span data-stu-id="abe40-201">**Run prerequisites**</span></span> | <span data-ttu-id="abe40-202">**Cerințe preliminare sincronizare inițială**</span><span class="sxs-lookup"><span data-stu-id="abe40-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="abe40-203">**Roluri de resurse ale proiectului pentru toate companiile (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="abe40-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="abe40-204">No</span><span class="sxs-lookup"><span data-stu-id="abe40-204">No</span></span> | <span data-ttu-id="abe40-205">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-205">Yes</span></span> | <span data-ttu-id="abe40-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="abe40-206">Common Data Service</span></span> | <span data-ttu-id="abe40-207">No</span><span class="sxs-lookup"><span data-stu-id="abe40-207">No</span></span> | <span data-ttu-id="abe40-208">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-208">N\A</span></span> |
| <span data-ttu-id="abe40-209">**Entități legale (cdm\_companii)**</span><span class="sxs-lookup"><span data-stu-id="abe40-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="abe40-210">No</span><span class="sxs-lookup"><span data-stu-id="abe40-210">No</span></span> | <span data-ttu-id="abe40-211">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-211">Yes</span></span> | <span data-ttu-id="abe40-212">Aplicații Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="abe40-212">Finance and Operations apps</span></span> | <span data-ttu-id="abe40-213">No</span><span class="sxs-lookup"><span data-stu-id="abe40-213">No</span></span> | <span data-ttu-id="abe40-214">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-214">N\A</span></span> |
| <span data-ttu-id="abe40-215">**Registru (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="abe40-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="abe40-216">No</span><span class="sxs-lookup"><span data-stu-id="abe40-216">No</span></span> | <span data-ttu-id="abe40-217">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-217">Yes</span></span> | <span data-ttu-id="abe40-218">Aplicații Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="abe40-218">Finance and Operations apps</span></span> | <span data-ttu-id="abe40-219">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-219">Yes</span></span> | <span data-ttu-id="abe40-220">Da, aplicații Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="abe40-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="abe40-221">**Actualități de integrare a Project Operations (msdyn\_actuale)**</span><span class="sxs-lookup"><span data-stu-id="abe40-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="abe40-222">No</span><span class="sxs-lookup"><span data-stu-id="abe40-222">No</span></span> | <span data-ttu-id="abe40-223">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-223">No</span></span> | <span data-ttu-id="abe40-224">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-224">N\A</span></span> | <span data-ttu-id="abe40-225">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-225">Yes</span></span> | <span data-ttu-id="abe40-226">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-226">No</span></span> |
| <span data-ttu-id="abe40-227">**Linii de contract de proiect (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="abe40-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="abe40-228">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-228">No</span></span> | <span data-ttu-id="abe40-229">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-229">No</span></span> | <span data-ttu-id="abe40-230">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-230">N\A</span></span> | <span data-ttu-id="abe40-231">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-231">No</span></span> | <span data-ttu-id="abe40-232">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-232">No</span></span> |
| <span data-ttu-id="abe40-233">**Entitate de integrare pentru relațiile de tranzacție ale proiectului (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="abe40-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="abe40-234">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-234">No</span></span> | <span data-ttu-id="abe40-235">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-235">No</span></span> | <span data-ttu-id="abe40-236">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-236">N\A</span></span> | <span data-ttu-id="abe40-237">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-237">No</span></span> | <span data-ttu-id="abe40-238">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-238">N\A</span></span> |
| <span data-ttu-id="abe40-239">**Integrare Project Operations etape linie de contract (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="abe40-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="abe40-240">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-240">No</span></span> | <span data-ttu-id="abe40-241">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-241">No</span></span> | <span data-ttu-id="abe40-242">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-242">N\A</span></span> | <span data-ttu-id="abe40-243">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-243">No</span></span> | <span data-ttu-id="abe40-244">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-244">N\A</span></span> |
| <span data-ttu-id="abe40-245">**Entitate de integrare a Project Operations pentru estimări de cheltuieli (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="abe40-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="abe40-246">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-246">No</span></span> | <span data-ttu-id="abe40-247">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-247">No</span></span> | <span data-ttu-id="abe40-248">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-248">N\A</span></span> | <span data-ttu-id="abe40-249">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-249">No</span></span> | <span data-ttu-id="abe40-250">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-250">N\A</span></span> |
| <span data-ttu-id="abe40-251">**Entitate de integrare de export Project Operations pentru categorii de cheltuieli (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="abe40-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="abe40-252">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-252">No</span></span> | <span data-ttu-id="abe40-253">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-253">No</span></span> | <span data-ttu-id="abe40-254">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-254">N\A</span></span> | <span data-ttu-id="abe40-255">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-255">No</span></span> | <span data-ttu-id="abe40-256">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-256">N\A</span></span> |
| <span data-ttu-id="abe40-257">**Entitate de integrare a Project Operations pentru cheltuieli de export (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="abe40-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="abe40-258">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-258">Yes</span></span> | <span data-ttu-id="abe40-259">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-259">No</span></span> | <span data-ttu-id="abe40-260">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-260">N\A</span></span> | <span data-ttu-id="abe40-261">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-261">No</span></span> | <span data-ttu-id="abe40-262">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-262">N\A</span></span> |
| <span data-ttu-id="abe40-263">**Entitate de integrare a Project Operations pentru estimări orare (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="abe40-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="abe40-264">Da</span><span class="sxs-lookup"><span data-stu-id="abe40-264">Yes</span></span> | <span data-ttu-id="abe40-265">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-265">No</span></span> | <span data-ttu-id="abe40-266">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-266">N\A</span></span> | <span data-ttu-id="abe40-267">Nicio</span><span class="sxs-lookup"><span data-stu-id="abe40-267">No</span></span> | <span data-ttu-id="abe40-268">N\A</span><span class="sxs-lookup"><span data-stu-id="abe40-268">N\A</span></span> |


4. <span data-ttu-id="abe40-269">Pentru a reîmprospăta entitatea, selectați numele hărții, apoi selectați **Reîmprospătați entități**.</span><span class="sxs-lookup"><span data-stu-id="abe40-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Reîmprospătați harta](./media/20RefreshMapping.png)

5. <span data-ttu-id="abe40-271">După finalizarea reîmprospătării, rulați harta.</span><span class="sxs-lookup"><span data-stu-id="abe40-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="abe40-272">Înainte de a activa următoarea hartă, verificați dacă harta din tabel se află în starea **Rulării**.</span><span class="sxs-lookup"><span data-stu-id="abe40-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="abe40-273">Rularea hărților cu un număr mai mare de condiții prealabile ar putea dura ceva timp.</span><span class="sxs-lookup"><span data-stu-id="abe40-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="abe40-274">Pentru a rula o hartă cu condiții prealabile, activați comutarea **Afișați hărți de entități corelate**.</span><span class="sxs-lookup"><span data-stu-id="abe40-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="abe40-275">Dacă tabelul indică **Sincronizare inițială preliminară** este **Nu**, verificați dacă semnalizarea **Sincronizare inițială** este **Dezactivat** în toate hărțile premise înainte de a-l rula.</span><span class="sxs-lookup"><span data-stu-id="abe40-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Rulați Harta](./media/21RunMap.png)

6. <span data-ttu-id="abe40-277">Validați toate hărțile legate de proiect sunt în starea de rulare.</span><span class="sxs-lookup"><span data-stu-id="abe40-277">Validate all project related maps are in the running state.</span></span>

![Toate hărțile rulează](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="abe40-279">Aplicarea datelor de configurare în CDS pentru Project Operations (opțional)</span><span class="sxs-lookup"><span data-stu-id="abe40-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="abe40-280">Dacă ați aplicat date demonstrative mediului financiar, consultați [Configurați și aplicați datele de configurare în Common Data Service pentru Project Operations](resource-apply-pro-setup-config-data.md) pentru a aplica date demonstrative mediului CDS.</span><span class="sxs-lookup"><span data-stu-id="abe40-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="abe40-281">Mediul dvs. Project Operations are acum asigurat accesul și este configurat.</span><span class="sxs-lookup"><span data-stu-id="abe40-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]