---
title: Aplicarea datelor de instalare și configurare demonstrative - simplificat
description: Acest subiect oferă informații despre cum se aplică datele de configurare și configurare demo pentru Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 694dbc74591de74895095a9da6e590069711fc83
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290149"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="3cdac-103">Aplicați date de configurare și instalare pentru Project Operations - simplificat</span><span class="sxs-lookup"><span data-stu-id="3cdac-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="3cdac-104">_\*\*Implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="3cdac-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="3cdac-105">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="3cdac-105">Prerequisites</span></span>

<span data-ttu-id="3cdac-106">Înainte să începeți configurarea, trebuie să aveți un mediu Common Data Service (CDS) furnizat pentru Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3cdac-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="3cdac-107">Instrucțiuni</span><span class="sxs-lookup"><span data-stu-id="3cdac-107">Instructions</span></span>

1. <span data-ttu-id="3cdac-108">Descărcați [Pachetul de date master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="3cdac-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="3cdac-109">Navigați la dosarul *ProjOpsDemoDataSetupAndMaster - CMT integrat* și rulați fișierul executabil, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="3cdac-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="3cdac-110">Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.</span><span class="sxs-lookup"><span data-stu-id="3cdac-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrarea configurării](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="3cdac-112">Pe pagina 2 a expertului CMT, selectați **Microsoft 365** ca **Tip de implementare**.</span><span class="sxs-lookup"><span data-stu-id="3cdac-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="3cdac-113">Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.</span><span class="sxs-lookup"><span data-stu-id="3cdac-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="3cdac-114">Selectați regiunea chiriașului, introduceți acreditările, apoi selectați **Autentificare**.</span><span class="sxs-lookup"><span data-stu-id="3cdac-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Conectare de configurare](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="3cdac-116">Pe pagina 3, din lista Organizațiilor de pe entitatea găzduită, selectați în ce organizație doriți să importați datele demo și apoi selectați **Autentificare**.</span><span class="sxs-lookup"><span data-stu-id="3cdac-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="3cdac-117">La pagina 4, selectați fișierul zip, *MasterAndSetupData* din folderul despachetat, *ProjOpsDemoDataSetupAndMaster - CMT integrat*.</span><span class="sxs-lookup"><span data-stu-id="3cdac-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Fișier zip](./media/3ZipFile.png)

   ![Selectați un fișier](./media/4SelectAFile.png)

9. <span data-ttu-id="3cdac-120">După selectarea fișierului zip, selectați **Importați date**.</span><span class="sxs-lookup"><span data-stu-id="3cdac-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importați date](./media/5ImportData.png)

10. <span data-ttu-id="3cdac-122">Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei.</span><span class="sxs-lookup"><span data-stu-id="3cdac-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="3cdac-123">După finalizare, ieșiți din CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="3cdac-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="3cdac-124">Verificați organizația pentru date în următoarele 20 de entități:</span><span class="sxs-lookup"><span data-stu-id="3cdac-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="3cdac-125">Monedă</span><span class="sxs-lookup"><span data-stu-id="3cdac-125">Currency</span></span>
    -   <span data-ttu-id="3cdac-126">Cont</span><span class="sxs-lookup"><span data-stu-id="3cdac-126">Account</span></span>
    -   <span data-ttu-id="3cdac-127">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="3cdac-127">Organizational Unit</span></span>
    -   <span data-ttu-id="3cdac-128">Contact</span><span class="sxs-lookup"><span data-stu-id="3cdac-128">Contact</span></span>
    -   <span data-ttu-id="3cdac-129">Unitate</span><span class="sxs-lookup"><span data-stu-id="3cdac-129">Unit</span></span>
    -   <span data-ttu-id="3cdac-130">Grup de unități</span><span class="sxs-lookup"><span data-stu-id="3cdac-130">Unit Group</span></span>
    -   <span data-ttu-id="3cdac-131">Listă de prețuri</span><span class="sxs-lookup"><span data-stu-id="3cdac-131">Price List</span></span>
    -   <span data-ttu-id="3cdac-132">Listă de prețuri parametru proiect</span><span class="sxs-lookup"><span data-stu-id="3cdac-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="3cdac-133">Frecvență factură</span><span class="sxs-lookup"><span data-stu-id="3cdac-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="3cdac-134">Categoria resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3cdac-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="3cdac-135">Categorie tranzacție</span><span class="sxs-lookup"><span data-stu-id="3cdac-135">Transaction Category</span></span>
    -   <span data-ttu-id="3cdac-136">Categorie de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="3cdac-136">Expense Category</span></span>
    -   <span data-ttu-id="3cdac-137">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="3cdac-137">Role Price</span></span>
    -   <span data-ttu-id="3cdac-138">Preț pentru categoria de tranzacție</span><span class="sxs-lookup"><span data-stu-id="3cdac-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="3cdac-139">Caracteristică</span><span class="sxs-lookup"><span data-stu-id="3cdac-139">Characteristic</span></span>
    -   <span data-ttu-id="3cdac-140">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3cdac-140">Bookable Resource</span></span>
    -   <span data-ttu-id="3cdac-141">Asociere categorie resursă care se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3cdac-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="3cdac-142">Caracteristică a resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3cdac-142">Bookable Resource Characteristic</span></span>

    ![Finalizați importul](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]