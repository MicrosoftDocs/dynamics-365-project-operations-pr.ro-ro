---
title: Aplicarea datelor de instalare și configurare demonstrative - simplificat
description: Acest subiect oferă informații despre cum se aplică datele de configurare și configurare demo pentru Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401278"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="a05eb-103">Aplicați date de configurare și instalare pentru Project Operations - simplificat</span><span class="sxs-lookup"><span data-stu-id="a05eb-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="a05eb-104">_\*\*Implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="a05eb-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a05eb-105">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="a05eb-105">Prerequisites</span></span>

<span data-ttu-id="a05eb-106">Înainte de a începe configurarea, trebuie să aveți un mediu Common Data Service (CDS) asigurat pentru operațiunile din Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a05eb-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="a05eb-107">Instrucțiuni</span><span class="sxs-lookup"><span data-stu-id="a05eb-107">Instructions</span></span>

1. <span data-ttu-id="a05eb-108">Descărcați [Pachetul de date master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="a05eb-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="a05eb-109">Navigați la dosarul *ProjOpsDemoDataSetupAndMaster - CMT integrat* și rulați fișierul executabil, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="a05eb-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="a05eb-110">Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.</span><span class="sxs-lookup"><span data-stu-id="a05eb-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="a05eb-112">Pe pagina 2 a expertului CMT, selectați **Microsoft 365** ca **Tip de implementare**.</span><span class="sxs-lookup"><span data-stu-id="a05eb-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="a05eb-113">Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.</span><span class="sxs-lookup"><span data-stu-id="a05eb-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="a05eb-114">Selectați regiunea chiriașului, introduceți acreditările, apoi selectați **Autentificare**.</span><span class="sxs-lookup"><span data-stu-id="a05eb-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Conectare de configurare](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="a05eb-116">Pe pagina 3, din lista Organizațiilor de pe entitatea găzduită, selectați în ce organizație doriți să importați datele demo și apoi selectați **Autentificare**.</span><span class="sxs-lookup"><span data-stu-id="a05eb-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="a05eb-117">La pagina 4, selectați fișierul zip, *MasterAndSetupData* din folderul despachetat, *ProjOpsDemoDataSetupAndMaster - CMT integrat*.</span><span class="sxs-lookup"><span data-stu-id="a05eb-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Fișier zip](./media/3ZipFile.png)

![Selectați un fișier](./media/4SelectAFile.png)

9. <span data-ttu-id="a05eb-120">După selectarea fișierului zip, selectați **Importați date**.</span><span class="sxs-lookup"><span data-stu-id="a05eb-120">After the zip file is selected, select **Import Data**.</span></span>

![Importați date](./media/5ImportData.png)

10. <span data-ttu-id="a05eb-122">Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei.</span><span class="sxs-lookup"><span data-stu-id="a05eb-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="a05eb-123">După finalizare, ieșiți din CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="a05eb-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="a05eb-124">Verificați organizația pentru date în următoarele 20 de entități:</span><span class="sxs-lookup"><span data-stu-id="a05eb-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="a05eb-125">Monedă</span><span class="sxs-lookup"><span data-stu-id="a05eb-125">Currency</span></span>
-   <span data-ttu-id="a05eb-126">Cont</span><span class="sxs-lookup"><span data-stu-id="a05eb-126">Account</span></span>
-   <span data-ttu-id="a05eb-127">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="a05eb-127">Organizational Unit</span></span>
-   <span data-ttu-id="a05eb-128">Contact</span><span class="sxs-lookup"><span data-stu-id="a05eb-128">Contact</span></span>
-   <span data-ttu-id="a05eb-129">Grup fiscal</span><span class="sxs-lookup"><span data-stu-id="a05eb-129">Tax Group</span></span>
-   <span data-ttu-id="a05eb-130">Grup de clienți</span><span class="sxs-lookup"><span data-stu-id="a05eb-130">Customer Group</span></span>
-   <span data-ttu-id="a05eb-131">Unitate</span><span class="sxs-lookup"><span data-stu-id="a05eb-131">Unit</span></span>
-   <span data-ttu-id="a05eb-132">Grup de unități</span><span class="sxs-lookup"><span data-stu-id="a05eb-132">Unit Group</span></span>
-   <span data-ttu-id="a05eb-133">Listă de prețuri</span><span class="sxs-lookup"><span data-stu-id="a05eb-133">Price List</span></span>
-   <span data-ttu-id="a05eb-134">Listă de prețuri parametru proiect</span><span class="sxs-lookup"><span data-stu-id="a05eb-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="a05eb-135">Frecvență factură</span><span class="sxs-lookup"><span data-stu-id="a05eb-135">Invoice Frequency</span></span>
-   <span data-ttu-id="a05eb-136">Categoria resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="a05eb-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="a05eb-137">Categorie tranzacție</span><span class="sxs-lookup"><span data-stu-id="a05eb-137">Transaction Category</span></span>
-   <span data-ttu-id="a05eb-138">Categorie de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="a05eb-138">Expense Category</span></span>
-   <span data-ttu-id="a05eb-139">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="a05eb-139">Role Price</span></span>
-   <span data-ttu-id="a05eb-140">Preț pentru categoria de tranzacție</span><span class="sxs-lookup"><span data-stu-id="a05eb-140">Transaction Category Price</span></span>
-   <span data-ttu-id="a05eb-141">Caracteristică</span><span class="sxs-lookup"><span data-stu-id="a05eb-141">Characteristic</span></span>
-   <span data-ttu-id="a05eb-142">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="a05eb-142">Bookable Resource</span></span>
-   <span data-ttu-id="a05eb-143">Asociere categorie resursă care se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="a05eb-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="a05eb-144">Caracteristică a resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="a05eb-144">Bookable Resource Characteristic</span></span>

![Finalizați importul](./media/6CompleteImport.png)
