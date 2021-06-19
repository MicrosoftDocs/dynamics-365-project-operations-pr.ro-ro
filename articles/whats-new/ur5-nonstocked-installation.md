---
title: Actualizați Project Operations în mediul dvs. de Finanțe
description: Acest subiect oferă informații despre cum să actualizați Project Operations în mediul Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011071"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="2e395-103">Actualizați Project Operations în mediul dvs. de Finanțe</span><span class="sxs-lookup"><span data-stu-id="2e395-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="2e395-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="2e395-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="2e395-105">Acest subiect oferă informații despre cum să actualizați Dynamics 365 Project Operations în mediul Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2e395-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="2e395-106">Există trei proceduri care sunt necesare pentru a actualiza Project Operations la Actualizarea 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="2e395-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="2e395-107">Importați pachetul în proiectul dvs. de previzualizare</span><span class="sxs-lookup"><span data-stu-id="2e395-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="2e395-108">Aplicați actualizarea</span><span class="sxs-lookup"><span data-stu-id="2e395-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="2e395-109">Actualizați mediul Dataverse</span><span class="sxs-lookup"><span data-stu-id="2e395-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="2e395-110">Importați pachetul în proiectul dvs. LCS</span><span class="sxs-lookup"><span data-stu-id="2e395-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="2e395-111">Conectați-vă la [Lifecycle Services (LCS)](https://lcs.dynamics.com/) ca proprietar de proiect sau manager de mediu.</span><span class="sxs-lookup"><span data-stu-id="2e395-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="2e395-112">Din lista de proiecte, selectați proiectul dvs. LCS.</span><span class="sxs-lookup"><span data-stu-id="2e395-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="2e395-113">Pe pagina **Proiect**, la grupul **Medii**, deschideți mediul pe care doriți să îl actualizați.</span><span class="sxs-lookup"><span data-stu-id="2e395-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="2e395-114">Verificați dacă mediul rulează.</span><span class="sxs-lookup"><span data-stu-id="2e395-114">Verify that the environment is running.</span></span> <span data-ttu-id="2e395-115">Dacă nu este pornit, porniți mediul.</span><span class="sxs-lookup"><span data-stu-id="2e395-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="2e395-116">În secțiunea **Noua versiune**, la **Actualizări disponibile**, selectați **Vizualizați actualizarea** pentru 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="2e395-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Vizualizați buton de actualizare](media/view-update.png)

6. <span data-ttu-id="2e395-118">Pe pagina **Actualizări binare**, selectați **Salvați pachetul**.</span><span class="sxs-lookup"><span data-stu-id="2e395-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="2e395-119">Pe pagina **Revizuiți și salvați actualizări**, selectați **Salvați pachetul**.</span><span class="sxs-lookup"><span data-stu-id="2e395-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="2e395-120">Pe panoul care se deschide **Salvați pachetul în biblioteca de active**, introduceți numele pachetului și apoi selectați **Salvați pachetul**.</span><span class="sxs-lookup"><span data-stu-id="2e395-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="2e395-121">Când LCS a terminat de salvat pachetul, se va activa butonul **Terminat**.</span><span class="sxs-lookup"><span data-stu-id="2e395-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="2e395-122">Selectați **Terminat**.</span><span class="sxs-lookup"><span data-stu-id="2e395-122">Select **Done**.</span></span> <span data-ttu-id="2e395-123">LCS va verifica pachetul.</span><span class="sxs-lookup"><span data-stu-id="2e395-123">LCS will verify the package.</span></span> <span data-ttu-id="2e395-124">Verificarea poate dura câteva minute sau până la o oră.</span><span class="sxs-lookup"><span data-stu-id="2e395-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="2e395-125">Aplicați actualizarea pachetului</span><span class="sxs-lookup"><span data-stu-id="2e395-125">Apply the package update</span></span>

1. <span data-ttu-id="2e395-126">În LCS, pe pagina **Detalii despre mediu**, selectați **Menţineți** > **Aplicați actualizări**.</span><span class="sxs-lookup"><span data-stu-id="2e395-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="2e395-127">Din listă, selectați pachetul pe care l-ați salvat mai devreme, apoi selectați **Aplicați**.</span><span class="sxs-lookup"><span data-stu-id="2e395-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="2e395-128">Selectați **Da** pentru a confirma că doriți să implementați pachetul.</span><span class="sxs-lookup"><span data-stu-id="2e395-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Casetă de dialog de confirmare a implementării pachetului](media/confirm-package-deployment.png)

4. <span data-ttu-id="2e395-130">Selectați **Da** pentru a confirma că doriți să actualizați aplicația.</span><span class="sxs-lookup"><span data-stu-id="2e395-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Casetă de dialog de confirmare a actualizării aplicației](media/confirm-application-update.png)

<span data-ttu-id="2e395-132">Implementarea și actualizarea aplicației vor începe.</span><span class="sxs-lookup"><span data-stu-id="2e395-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="2e395-133">Pe pagina **Detalii despre mediu**, în colțul din dreapta sus, starea mediului se va actualiza la **Service**.</span><span class="sxs-lookup"><span data-stu-id="2e395-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="2e395-134">În aproximativ două ore, actualizarea va fi completă.</span><span class="sxs-lookup"><span data-stu-id="2e395-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="2e395-135">Informațiile privind lansarea aplicației se vor actualiza la **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** iar starea mediului se va actualiza la **Implementat**.</span><span class="sxs-lookup"><span data-stu-id="2e395-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="2e395-136">Actualizați mediul Dataverse</span><span class="sxs-lookup"><span data-stu-id="2e395-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="2e395-137">Conectați-vă la [Centrul de administrare Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="2e395-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="2e395-138">În listă, găsiți și deschideți mediul pe care l-ați folosit pentru a instala Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2e395-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="2e395-139">Pe pagina **Medii**, selectați **Resursă** > **Aplicații Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="2e395-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="2e395-140">În listă, localizați **Microsoft Dynamics 365 Project Operations**, și în coloana **Stare**, selectați **Actualizare disponibilă**.</span><span class="sxs-lookup"><span data-stu-id="2e395-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="2e395-141">Bifați caseta de selectare **Sunt de acord cu termenele serviciului**, apoi selectați **Actualizați**.</span><span class="sxs-lookup"><span data-stu-id="2e395-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="2e395-142">Va fi instalată cea mai recentă versiune a soluției.</span><span class="sxs-lookup"><span data-stu-id="2e395-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="2e395-143">După finalizarea instalării, veți avea instalată versiunea 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="2e395-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="2e395-144">Configurați caracteristici noi</span><span class="sxs-lookup"><span data-stu-id="2e395-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="2e395-145">Activați maparea cu scriere duală</span><span class="sxs-lookup"><span data-stu-id="2e395-145">Enable dual-write mapping</span></span>

<span data-ttu-id="2e395-146">După ce finalizați actualizarea pentru mediile Finanțe și Dataverse, puteți activa mapările necesare cu scriere duală.</span><span class="sxs-lookup"><span data-stu-id="2e395-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="2e395-147">Realizați următoarele proceduri pentru a activa mapările cu scriere duală.</span><span class="sxs-lookup"><span data-stu-id="2e395-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="2e395-148">Actualizați setările de securitate din mediul Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="2e395-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="2e395-149">Reîmprospătarea entităților de date</span><span class="sxs-lookup"><span data-stu-id="2e395-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="2e395-150">Actualizați și rulați mapările cu scriere duală</span><span class="sxs-lookup"><span data-stu-id="2e395-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="2e395-151">Actualizați setările de securitate pe mediul Dataverse</span><span class="sxs-lookup"><span data-stu-id="2e395-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="2e395-152">Următoarele actualizări ale privilegiilor de securitate pentru entități sunt necesare ca parte a actualizării la UR5.</span><span class="sxs-lookup"><span data-stu-id="2e395-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="2e395-153">In mediul dvs. Dataverse, accesați **Setări**, iar în grupul **Sistem**, selectați **Securitate**.</span><span class="sxs-lookup"><span data-stu-id="2e395-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Setări ale mediului Dataverse](media/Picture21.png)

2. <span data-ttu-id="2e395-155">Selectare **roluri de securitate**.</span><span class="sxs-lookup"><span data-stu-id="2e395-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="2e395-156">Din lista de roluri, selectați **utilizator de aplicație cu scriere duală** și selectați fila **Entități personalizate**.</span><span class="sxs-lookup"><span data-stu-id="2e395-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="2e395-157">Verificați dacă rolul are permisiunile **Citit** și **Adăugați la** pentru:</span><span class="sxs-lookup"><span data-stu-id="2e395-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="2e395-158">**Tipul cursului de schimb valutar**</span><span class="sxs-lookup"><span data-stu-id="2e395-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="2e395-159">**Plan de conturi**</span><span class="sxs-lookup"><span data-stu-id="2e395-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="2e395-160">**Calendar fiscal**</span><span class="sxs-lookup"><span data-stu-id="2e395-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="2e395-161">**Registru**</span><span class="sxs-lookup"><span data-stu-id="2e395-161">**Ledger**</span></span>

5. <span data-ttu-id="2e395-162">După actualizarea rolului de securitate, accesați **Setări** > **Securitate** > **Echipe**.</span><span class="sxs-lookup"><span data-stu-id="2e395-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="2e395-163">Verificați dacă rolul de **utilizator de aplicație cu scriere duală** a fost aplicat echipei.</span><span class="sxs-lookup"><span data-stu-id="2e395-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="2e395-164">Reîmprospătați entitățile de date din actualizare</span><span class="sxs-lookup"><span data-stu-id="2e395-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="2e395-165">În mediul dvs. financiar, deschideți spațiul de lucru **Management de date**, apoi deschideți pagina **Parametrii cadru**.</span><span class="sxs-lookup"><span data-stu-id="2e395-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="2e395-166">Pe fila **Setări entitate**, selectați **Reîmprospătați lista entităților**.</span><span class="sxs-lookup"><span data-stu-id="2e395-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="2e395-167">Selectați **Închideți** pentru a confirma reîmprospătarea entității.</span><span class="sxs-lookup"><span data-stu-id="2e395-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2e395-168">Aceste proces va dura aproximativ 20 de minute până la finalizare.</span><span class="sxs-lookup"><span data-stu-id="2e395-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="2e395-169">Veți fi notificat când actualizarea este finalizată.</span><span class="sxs-lookup"><span data-stu-id="2e395-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="2e395-170">Actualizați mapările cu scriere duală</span><span class="sxs-lookup"><span data-stu-id="2e395-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="2e395-171">În spațiul de lucru **Management de date**, selectați **Scriere duală**.</span><span class="sxs-lookup"><span data-stu-id="2e395-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="2e395-172">Selectați **Aplicați soluții**, selectați ambele soluții din listă, apoi selectați **Aplicați**.</span><span class="sxs-lookup"><span data-stu-id="2e395-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="2e395-173">Pe pagina **Scriere duală**, selectați următoarele hărți de tabel, apoi selectați **Oprire**.</span><span class="sxs-lookup"><span data-stu-id="2e395-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="2e395-174">**Integrare valori reale Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="2e395-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="2e395-175">**Integrarea categoriilor de cheltuieli de proiect Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="2e395-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="2e395-176">**Integrarea entității de export a valorilor reale ale cheltuielilor pentru proiect în Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="2e395-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="2e395-177">Pe pagina **Versiunea hărții tabelului**, aplicați o nouă versiune a hărții fiecăreia dintre cele trei entități.</span><span class="sxs-lookup"><span data-stu-id="2e395-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="2e395-178">Pe pagina **Scriere duală**, selectați rulare pentru a reporni hărțile.</span><span class="sxs-lookup"><span data-stu-id="2e395-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="2e395-179">Din lista de hărți, selectați harta **Registru (msdyn_ledgers)** cu toate premisele si selectați caseta de bifare **Sincronizare inițială**.</span><span class="sxs-lookup"><span data-stu-id="2e395-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="2e395-180">În câmpul **Master pentru sincronizarea inițială**, selectați **aplicațiile Finance and Operations** și apoi selectați **Rulare**.</span><span class="sxs-lookup"><span data-stu-id="2e395-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronizarea hărții registrului](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]