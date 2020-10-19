---
title: Aplicarea datelor de instalare și configurare demonstrative
description: Acest subiect oferă informații despre cum se aplică datele de configurare și configurare demo pentru Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949027"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="3177c-103">Aplicați datele de configurare și configurare a demonstrației pentru implementarea Project Operations simplificat - de la tranzacție la factura proforma</span><span class="sxs-lookup"><span data-stu-id="3177c-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="3177c-104">_\*\*Implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="3177c-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="3177c-105">Descărcați [Pachetul de date master](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="3177c-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="3177c-106">Navigați la dosarul *ProjOpsDemoDataSetupAndMaster - CMT integrat* și rulați fișierul executabil, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="3177c-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="3177c-107">Pe pagina 1 din Common Data Service Expertul Migrare configurare (CMT), selectați **Importați date** și apoi selectați **Continuare**.</span><span class="sxs-lookup"><span data-stu-id="3177c-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrarea configurării](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="3177c-109">Pe pagina 2 a Expertului CMT, selectați **Office 365** după **Tipul de implementare**.</span><span class="sxs-lookup"><span data-stu-id="3177c-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="3177c-110">Selectați **Afișați o listă a organizațiilor disponibile** și casetele de selectare **Afișați avansat**.</span><span class="sxs-lookup"><span data-stu-id="3177c-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="3177c-111">Selectați regiunea chiriașului, introduceți acreditările, apoi selectați **Autentificare**.</span><span class="sxs-lookup"><span data-stu-id="3177c-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Conectare de configurare](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="3177c-113">Pe pagina 3, din lista Organizațiilor de pe entitatea găzduită, selectați în ce organizație doriți să importați datele demo și apoi selectați **Autentificare**.</span><span class="sxs-lookup"><span data-stu-id="3177c-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="3177c-114">La pagina 4, selectați fișierul zip, *MasterAndSetupData* din folderul despachetat, *ProjOpsDemoDataSetupAndMaster - CMT integrat*.</span><span class="sxs-lookup"><span data-stu-id="3177c-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Fișier zip](./media/3ZipFile.png)

![Selectați un fișier](./media/4SelectAFile.png)

9. <span data-ttu-id="3177c-117">După selectarea fișierului zip, selectați **Importați date**.</span><span class="sxs-lookup"><span data-stu-id="3177c-117">After the zip file is selected, select **Import Data**.</span></span>

![Importați date](./media/5ImportData.png)

10. <span data-ttu-id="3177c-119">Importul va rula aproximativ două-zece minute, în funcție de viteza rețelei.</span><span class="sxs-lookup"><span data-stu-id="3177c-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="3177c-120">După finalizare, ieșiți din CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="3177c-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="3177c-121">Verificați organizația pentru date în următoarele 20 de entități:</span><span class="sxs-lookup"><span data-stu-id="3177c-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="3177c-122">Monedă</span><span class="sxs-lookup"><span data-stu-id="3177c-122">Currency</span></span>
- <span data-ttu-id="3177c-123">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="3177c-123">Organizational Unit</span></span>
- <span data-ttu-id="3177c-124">Contact</span><span class="sxs-lookup"><span data-stu-id="3177c-124">Contact</span></span>
- <span data-ttu-id="3177c-125">Grup fiscal</span><span class="sxs-lookup"><span data-stu-id="3177c-125">Tax Group</span></span>
- <span data-ttu-id="3177c-126">Grup de clienți</span><span class="sxs-lookup"><span data-stu-id="3177c-126">Customer Group</span></span>
- <span data-ttu-id="3177c-127">Unitate</span><span class="sxs-lookup"><span data-stu-id="3177c-127">Unit</span></span>
- <span data-ttu-id="3177c-128">Grup de unități</span><span class="sxs-lookup"><span data-stu-id="3177c-128">Unit Group</span></span>
- <span data-ttu-id="3177c-129">Listă de prețuri</span><span class="sxs-lookup"><span data-stu-id="3177c-129">Price List</span></span>
- <span data-ttu-id="3177c-130">Listă de prețuri parametru proiect</span><span class="sxs-lookup"><span data-stu-id="3177c-130">Project Parameter Price List</span></span>
- <span data-ttu-id="3177c-131">Frecvență factură</span><span class="sxs-lookup"><span data-stu-id="3177c-131">Invoice Frequency</span></span>
- <span data-ttu-id="3177c-132">Detaliu frecvență factură</span><span class="sxs-lookup"><span data-stu-id="3177c-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="3177c-133">Categoria resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3177c-133">Bookable Resource Category</span></span>
- <span data-ttu-id="3177c-134">Categorie tranzacție</span><span class="sxs-lookup"><span data-stu-id="3177c-134">Transaction Category</span></span>
- <span data-ttu-id="3177c-135">Categorie de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="3177c-135">Expense Category</span></span>
- <span data-ttu-id="3177c-136">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="3177c-136">Role Price</span></span>
- <span data-ttu-id="3177c-137">Preț pentru categoria de tranzacție</span><span class="sxs-lookup"><span data-stu-id="3177c-137">Transaction Category Price</span></span>
- <span data-ttu-id="3177c-138">Caracteristică</span><span class="sxs-lookup"><span data-stu-id="3177c-138">Characteristic</span></span>
- <span data-ttu-id="3177c-139">Resursă ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3177c-139">Bookable Resource</span></span>
- <span data-ttu-id="3177c-140">Asociere categorie resursă care se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3177c-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="3177c-141">Caracteristică a resursei ce se poate rezerva</span><span class="sxs-lookup"><span data-stu-id="3177c-141">Bookable Resource Characteristic</span></span>

![Finalizați importul](./media/6CompleteImport.png)
