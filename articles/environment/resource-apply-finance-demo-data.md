---
title: Aplicarea datelor demonstrative Project Operations la un mediu Finance găzduit în cloud
description: Acest subiect explică modul de aplicare a datelor demo din Project Operations la un mediu Dynamics 365 Finance găzduit în cloud.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949035"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="980a6-103">Aplicarea datelor demonstrative Project Operations la un mediu Finance găzduit în cloud</span><span class="sxs-lookup"><span data-stu-id="980a6-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="980a6-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="980a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="980a6-105">[Important] Acest subiect se aplică numai Microsoft Dynamics 365 Finance versiunea 10.0.13 și poate fi efectuată numai pe un mediu găzduit în cloud.</span><span class="sxs-lookup"><span data-stu-id="980a6-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="980a6-106">Finalizați pașii din acest subiect **ÎNAINTE DE** aplicați actualizări de calitate mediului.</span><span class="sxs-lookup"><span data-stu-id="980a6-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="980a6-107">În proiectul dvs. LCS, deschideți pagina **Detalii despre mediu**.</span><span class="sxs-lookup"><span data-stu-id="980a6-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="980a6-108">Observați că include detaliile necesare pentru a vă conecta la mediu utilizând Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="980a6-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalii despre mediul ](./media/1EnvironmentDetails.png)

<span data-ttu-id="980a6-110">Primul set de acreditări evidențiate sunt acreditările contului local și conțin un hyperlink către conexiunea desktop la distanță.</span><span class="sxs-lookup"><span data-stu-id="980a6-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="980a6-111">Acreditările includ numele de utilizator și parola administratorului mediului.</span><span class="sxs-lookup"><span data-stu-id="980a6-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="980a6-112">Al doilea set de acreditări este utilizat pentru a vă conecta la SQL Server în acest mediu.</span><span class="sxs-lookup"><span data-stu-id="980a6-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="980a6-113">conectați-vă la mediu prin hyperlink în **Conturi locale**, și utilizați **Acreditări de cont local** pentru a autentifica.</span><span class="sxs-lookup"><span data-stu-id="980a6-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="980a6-114">Accesați **Servicii de informare pe internet** > **Grupuri de aplicații** > **Serviciul AOSS** și opriți serviciul.</span><span class="sxs-lookup"><span data-stu-id="980a6-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="980a6-115">Opriți serviciul în acest moment, astfel încât să puteți continua să înlocuiți baza de date SQL.</span><span class="sxs-lookup"><span data-stu-id="980a6-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Stop AOS](./media/2StopAOS.png)

4. <span data-ttu-id="980a6-117">Accesați **Servicii** și opriți următoarele două elemente:</span><span class="sxs-lookup"><span data-stu-id="980a6-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="980a6-118">Microsoft Dynamics 365 Unified Operations: Serviciul de gestionare a loturilor</span><span class="sxs-lookup"><span data-stu-id="980a6-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="980a6-119">Microsoft Dynamics 365 Unified Operations: Cadrul de export al importului de date</span><span class="sxs-lookup"><span data-stu-id="980a6-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Opriți serviciile](./media/3StopServices.png)

5. <span data-ttu-id="980a6-121">Deschideți Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="980a6-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="980a6-122">Conectați-vă cu acreditările serverului SQL și utilizați utilizatorul și parola axdbadmin din pagina LCS **Detalii despre medii**.</span><span class="sxs-lookup"><span data-stu-id="980a6-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="980a6-124">În Object Explorer, **Baze de date** și localizați **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="980a6-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="980a6-125">Veți înlocui baza de date cu o nouă bază de date care se află în [Centrul de descărcare](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="980a6-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="980a6-126">Copiați fișierul zip în VM-ul în care sunteți îndepărtat și extrageți conținutul zip.</span><span class="sxs-lookup"><span data-stu-id="980a6-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="980a6-127">În SQL Server Management Studio, faceți clic dreapta **AxDB**, apoi selectați **Sarcini** > **Restabili** > **Bază de date**.</span><span class="sxs-lookup"><span data-stu-id="980a6-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Restaurați baza de date](./media/5RestoreDatabase.png)

9. <span data-ttu-id="980a6-129">Selectați **Dispozitiv sursă** și navigați la fișierul extras din zip pe care l-ați copiat.</span><span class="sxs-lookup"><span data-stu-id="980a6-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispozitive sursă](./media/6SourceDevice.png)

10. <span data-ttu-id="980a6-131">Selectați **Opțiuni**, apoi selectați **Suprascrieți baza de date existentă** și **Închideți conexiunile existente la baza de date destinație**.</span><span class="sxs-lookup"><span data-stu-id="980a6-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="980a6-132">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="980a6-132">Select **OK**.</span></span>

![Restaurați setări](./media/7RestoreSetting.png)

<span data-ttu-id="980a6-134">Veți primi confirmarea că restaurarea AXDB a avut succes.</span><span class="sxs-lookup"><span data-stu-id="980a6-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="980a6-135">După ce primiți această confirmare, puteți închide SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="980a6-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="980a6-136">Reveniți la **Servicii de informare pe internet** > **Grupuri de aplicații** > **Serviciul AOSS** și porniți serviciul AOSS.</span><span class="sxs-lookup"><span data-stu-id="980a6-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="980a6-137">Accesați **Servicii** și porniți cele două servicii pe care le-ați oprit mai devreme.</span><span class="sxs-lookup"><span data-stu-id="980a6-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="980a6-138">Găsiți instrumentul AdminUserProvisioning pe această mașină virtuală.</span><span class="sxs-lookup"><span data-stu-id="980a6-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="980a6-139">Căutați sub, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="980a6-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="980a6-140">Rulați fișierul .ext folosind adresa de utilizator din câmpul **Adresa de email**.</span><span class="sxs-lookup"><span data-stu-id="980a6-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="980a6-141">Selectați **Remitere**.</span><span class="sxs-lookup"><span data-stu-id="980a6-141">Select **Submit**.</span></span>

![Furnizare acces utilizator administrator](./media/8AdminUserProvisioning.png)

<span data-ttu-id="980a6-143">Finalizarea acestui proces durează câteva minute.</span><span class="sxs-lookup"><span data-stu-id="980a6-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="980a6-144">Ar trebui să primiți un mesaj de confirmare a faptului că utilizatorul administratorului a fost actualizat cu succes.</span><span class="sxs-lookup"><span data-stu-id="980a6-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="980a6-145">În cele din urmă, executați Command Prompt ca administrator și efectuați iisreset</span><span class="sxs-lookup"><span data-stu-id="980a6-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Reiniţializare IIS](./media/9IISReset.png)

18. <span data-ttu-id="980a6-147">Închideți sesiunea desktop la distanță și utilizați pagina LCS **Detalii despre mediu** pentru a vă conecta la mediu pentru a confirma că funcționează conform așteptărilor.</span><span class="sxs-lookup"><span data-stu-id="980a6-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
