---
title: Procesarea chitanțelor de cheltuieli
description: Acest subiect oferă informații despre procesarea recunoașterii optice a caracterelor (OCR) pentru chitanțe. Această caracteristică este concepută pentru a îmbunătăți experiența utilizatorului când sunt create rapoarte de cheltuieli în Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082954"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="8ca98-104">Procesarea chitanțelor de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="8ca98-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ca98-105">Introducerea cheltuielilor a fost îmbunătățită prin introducerea procesării de recunoaștere optică a caracterelor (OCR) pentru chitanțe.</span><span class="sxs-lookup"><span data-stu-id="8ca98-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8ca98-106">Această caracteristică este concepută pentru a îmbunătăți experiența utilizatorului când sunt create rapoarte de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8ca98-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="8ca98-107">Caracteristici cheie</span><span class="sxs-lookup"><span data-stu-id="8ca98-107">Key features</span></span>

- <span data-ttu-id="8ca98-108">Numele comerciantului, data și suma totală sunt extrase din chitanțe.</span><span class="sxs-lookup"><span data-stu-id="8ca98-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="8ca98-109">Caracteristica încercă să potrivească chitanțele neatașate cu tranzacțiile de cheltuieli neatașate.</span><span class="sxs-lookup"><span data-stu-id="8ca98-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8ca98-110">Utilizatorii pot crea tranzacții de cheltuieli introduse manual din chitanțe.</span><span class="sxs-lookup"><span data-stu-id="8ca98-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="8ca98-111">Exemple de utilizare</span><span class="sxs-lookup"><span data-stu-id="8ca98-111">Usage examples</span></span>

<span data-ttu-id="8ca98-112">Pentru a atașa automat chitanțe care includ tranzacții cu cardul de credit atunci când este creat un raport de cheltuieli, parcurgeți pașii următori:</span><span class="sxs-lookup"><span data-stu-id="8ca98-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="8ca98-113">Deschideți spațiul de lucru **Gestionarea cheltuielilor**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8ca98-114">Pe fila **Chitanțe** , verificați dacă există chitanțe neatașate.</span><span class="sxs-lookup"><span data-stu-id="8ca98-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8ca98-115">De asemenea, puteți încărca chitanțe pe fila **Chitanțe**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8ca98-116">Pe fila **Cheltuieli** , verificați dacă există cheltuieli neatașate.</span><span class="sxs-lookup"><span data-stu-id="8ca98-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8ca98-117">De obicei, administratorul cheltuielilor importă aceste cheltuieli de la furnizorul cardului de credit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8ca98-118">Selectați **Nou raport de cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-118">Select **New expense report**.</span></span> <span data-ttu-id="8ca98-119">Observați că puteți include cheltuieli și chitanțe și acum, atunci când creați un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8ca98-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8ca98-120">Dacă adăugați atât cheltuieli, cât și chitanțe, se declanșează corelarea automată a chitanțelor cu cheltuielile.</span><span class="sxs-lookup"><span data-stu-id="8ca98-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="8ca98-121">Pentru a crea o cheltuială sau pentru a potrivi o cheltuială dintr-o chitanță, parcurgeți pașii următori:</span><span class="sxs-lookup"><span data-stu-id="8ca98-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="8ca98-122">Pe un raport de cheltuieli, pe fila **Chitanțe** , atașați o chitanță selectând **Adăugați chitanțe**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8ca98-123">Sub imaginea încărcată a chitanței, observați opțiunile **Creare** și **Potrivire**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8ca98-124">Selectați **Creare** pentru a crea o tranzacție de cheltuieli introdusă manual și pentru a completa valorile care sunt extrase din chitanță.</span><span class="sxs-lookup"><span data-stu-id="8ca98-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8ca98-125">Dacă selectați sistemul **Potrivire** , sistemul încearcă să potrivească o cheltuială existentă cu chitanța.</span><span class="sxs-lookup"><span data-stu-id="8ca98-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8ca98-126">Instalare</span><span class="sxs-lookup"><span data-stu-id="8ca98-126">Installation</span></span>

<span data-ttu-id="8ca98-127">Această caracteristică funcționează în combinație cu caracteristica **Rapoarte de cheltuieli reimaginate** pentru a simplifica experiența cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="8ca98-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="8ca98-128">Această caracteristică este disponibilă numai pentru mediile Tier 2+, care sunt Sandbox și Production.</span><span class="sxs-lookup"><span data-stu-id="8ca98-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="8ca98-129">Pentru a utiliza aceste capabilități avansate de cheltuieli, instalați programul de completare Serviciul de gestionare a cheltuielilor pentru Microsoft Dynamics 365 Finance și activați funcțiile din instanța dvs.</span><span class="sxs-lookup"><span data-stu-id="8ca98-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8ca98-130">Puteți accesa programul de completare din proiectul dvs. din Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8ca98-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8ca98-131">Conectați-vă la LCS și deschideți mediul dorit.</span><span class="sxs-lookup"><span data-stu-id="8ca98-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8ca98-132">Accesați **Toate detaliile**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="8ca98-133">Selectați **Menţine** , sau derulați în jos la FastTab **Programe de completare de mediu**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8ca98-134">Selectați **Instalați un nou program de completare**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8ca98-135">Selectați **Serviciu gestionare cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8ca98-136">Urmați ghidul de instalare și acceptați termenii și condițiile.</span><span class="sxs-lookup"><span data-stu-id="8ca98-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8ca98-137">Selectați **Instalare**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-137">Select **Install**.</span></span>

<span data-ttu-id="8ca98-138">În spațiul de lucru **Managementul caracteristicilor** , activați următoarele caracteristici:</span><span class="sxs-lookup"><span data-stu-id="8ca98-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8ca98-139">Rapoarte de cheltuieli reimaginate</span><span class="sxs-lookup"><span data-stu-id="8ca98-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="8ca98-140">Potriviți automat și creați cheltuieli de la primire</span><span class="sxs-lookup"><span data-stu-id="8ca98-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8ca98-141">Când activați aceste funcții, au loc următoarele acțiuni:</span><span class="sxs-lookup"><span data-stu-id="8ca98-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8ca98-142">Spațiul de lucru existent **Gestionarea cheltuielilor** este înlocuit cu noul spațiu de lucru.</span><span class="sxs-lookup"><span data-stu-id="8ca98-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8ca98-143">Se adaugă un nou element de meniu pentru vizibilitatea câmpului de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="8ca98-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8ca98-144">Puteți deschide încă fosta pagină **Rapoarte de cheltuieli** accesând **Gestionarea cheltuielilor > Cheltuielile mele > Rapoarte de cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="8ca98-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8ca98-145">Fluxurile de lucru și orice aprobări vă duc în continuare la pagina de rapoarte de cheltuieli existente.</span><span class="sxs-lookup"><span data-stu-id="8ca98-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8ca98-146">Chitanțele vor fi procesate prin Microsoft Azure Cognitive Services și metadatele vor fi extrase și adăugate.</span><span class="sxs-lookup"><span data-stu-id="8ca98-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8ca98-147">Se adaugă o opțiune care vă permite să creați un raport de cheltuieli care include chitanțe neatașate potrivite.</span><span class="sxs-lookup"><span data-stu-id="8ca98-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8ca98-148">O opțiune care este adăugată la rapoartele de cheltuieli vă permite să creați o linie de cheltuieli dintr-o chitanță sau să încercați să potriviți o chitanță existentă cu o linie de cheltuieli existentă.</span><span class="sxs-lookup"><span data-stu-id="8ca98-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="8ca98-149">Pentru mai multe informații despre caracteristica reimaginată a rapoartelor de cheltuieli, consultați [Rapoarte de cheltuieli reimaginate](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="8ca98-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8ca98-150">Întrebări frecvente</span><span class="sxs-lookup"><span data-stu-id="8ca98-150">Frequently asked questions</span></span>

<span data-ttu-id="8ca98-151">**Utilizează Microsoft datele mele pentru modelele sale?**</span><span class="sxs-lookup"><span data-stu-id="8ca98-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8ca98-152">Nu, Microsoft a construit un model general învățare programată pentru serviciul său de procesare a chitanțelor.</span><span class="sxs-lookup"><span data-stu-id="8ca98-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8ca98-153">Acest model nu se bazează pe chitanțele pe care le încărcați.</span><span class="sxs-lookup"><span data-stu-id="8ca98-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8ca98-154">**Unde este disponibilă și procesată această caracteristică?**</span><span class="sxs-lookup"><span data-stu-id="8ca98-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8ca98-155">În prezent, Statele Unite sunt acceptate.</span><span class="sxs-lookup"><span data-stu-id="8ca98-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="8ca98-156">**Unde merg chitanțele mele?**</span><span class="sxs-lookup"><span data-stu-id="8ca98-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="8ca98-157">Finance va contacta serviciile cognitive pentru a extrage datele din câmp.</span><span class="sxs-lookup"><span data-stu-id="8ca98-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8ca98-158">Serviciile cognitive vor păstra o copie a chitanței dvs. timp de până la 24 de ore în timp ce are loc procesarea.</span><span class="sxs-lookup"><span data-stu-id="8ca98-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8ca98-159">După finalizarea procesării, Cognitive Services va elimina chitanța.</span><span class="sxs-lookup"><span data-stu-id="8ca98-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8ca98-160">Chitanțele sunt încă stocate în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="8ca98-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8ca98-161">Pentru mai multe informații, consultați [Activați înțelegerea chitanței cu noua capacitate a Recunoscătorului de formulare](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8ca98-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
