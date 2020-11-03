---
title: Corelarea unei chitanțe cu o cheltuială folosind OCR
description: Acest subiect oferă informații despre procesarea recunoașterii optice a caracterelor (OCR) pentru chitanțe.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082761"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="2b5c0-103">Corelarea unei chitanțe cu o cheltuială folosind OCR</span><span class="sxs-lookup"><span data-stu-id="2b5c0-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="2b5c0-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="2b5c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b5c0-105">Introducerea cheltuielilor a fost îmbunătățită prin introducerea procesării de recunoaștere optică a caracterelor (OCR) pentru chitanțe.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="2b5c0-106">Această funcționalitate este concepută pentru a îmbunătăți experiența utilizatorului la crearea rapoartelor de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="2b5c0-107">Caracteristici cheie</span><span class="sxs-lookup"><span data-stu-id="2b5c0-107">Key features</span></span>

- <span data-ttu-id="2b5c0-108">Sistemul extrage numele comerciantului, data și suma totală din chitanțe.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="2b5c0-109">Sistemul va încerca să potrivească chitanțele neatașate cu tranzacțiile de cheltuieli neatașate.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="2b5c0-110">Puteți crea tranzacții de cheltuieli introduse manual din chitanțe.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="2b5c0-111">Atașați chitanțe la un raport de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="2b5c0-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="2b5c0-112">Pentru a atașa automat chitanțe care includ tranzacții cu cardul de credit atunci când este creat un raport de cheltuieli, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="2b5c0-113">Deschideți spațiul de lucru **Gestionarea cheltuielilor**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="2b5c0-114">Pe fila **Chitanțe** , verificați dacă există chitanțe neatașate.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="2b5c0-115">De asemenea, puteți încărca chitanțe pe fila **Chitanțe**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="2b5c0-116">Pe fila **Cheltuieli** , verificați dacă există cheltuieli neatașate.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="2b5c0-117">De obicei, administratorul cheltuielilor importă aceste cheltuieli de la furnizorul cardului de credit.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="2b5c0-118">Selectați **Nou raport de cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-118">Select **New expense report**.</span></span> <span data-ttu-id="2b5c0-119">Observați că puteți include cheltuieli și chitanțe și acum, atunci când creați un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="2b5c0-120">Dacă adăugați atât cheltuieli, cât și chitanțe, se declanșează corelarea automată a chitanțelor cu cheltuielile.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="2b5c0-121">Creați sau potriviți chitanțe la un raport de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="2b5c0-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="2b5c0-122">Pentru a crea o cheltuială sau pentru a potrivi o cheltuială dintr-o chitanță, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="2b5c0-123">Pe un raport de cheltuieli, pe fila **Chitanțe** , atașați o chitanță selectând **Adăugați chitanțe**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="2b5c0-124">Sub imaginea încărcată a chitanței, observați opțiunile **Creare** și **Potrivire**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="2b5c0-125">Selectați **Creare** pentru a crea o tranzacție de cheltuieli introdusă manual și pentru a completa valorile care sunt extrase din chitanță.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="2b5c0-126">Dacă selectați sistemul **Potrivire** , sistemul încearcă să potrivească o cheltuială existentă cu chitanța.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-126">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="2b5c0-127">Instalare</span><span class="sxs-lookup"><span data-stu-id="2b5c0-127">Installation</span></span>

<span data-ttu-id="2b5c0-128">Pentru a utiliza aceste capabilități avansate de cheltuieli, instalați programul de completare Serviciul de gestionare a cheltuielilor pentru Microsoft Dynamics 365 Finance și activați funcțiile din instanța dvs.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="2b5c0-129">Puteți accesa programul de completare din proiectul dvs. din Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2b5c0-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="2b5c0-130">Conectați-vă la LCS și deschideți mediul dorit.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="2b5c0-131">Accesați **Toate detaliile**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="2b5c0-132">Selectați **Menţine** , sau derulați în jos la FastTab **Programe de completare de mediu**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-132">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="2b5c0-133">Selectați **Instalați un nou program de completare**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="2b5c0-134">Selectați **Serviciu gestionare cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="2b5c0-135">Urmați ghidul de instalare și acceptați termenii și condițiile.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="2b5c0-136">Selectați **Instalare**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-136">Select **Install**.</span></span>

<span data-ttu-id="2b5c0-137">În spațiul de lucru **Managementul caracteristicilor** , activați următoarele caracteristici:</span><span class="sxs-lookup"><span data-stu-id="2b5c0-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="2b5c0-138">Rapoarte de cheltuieli reimaginate</span><span class="sxs-lookup"><span data-stu-id="2b5c0-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="2b5c0-139">Potriviți automat și creați cheltuieli de la primire</span><span class="sxs-lookup"><span data-stu-id="2b5c0-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="2b5c0-140">Când activați aceste funcții, au loc următoarele acțiuni:</span><span class="sxs-lookup"><span data-stu-id="2b5c0-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="2b5c0-141">Spațiul de lucru existent **Gestionarea cheltuielilor** este înlocuit cu noul spațiu de lucru.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2b5c0-142">Se adaugă un nou element de meniu pentru vizibilitatea câmpului de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2b5c0-143">Puteți deschide încă fosta pagină **Rapoarte de cheltuieli** accesând **Gestionarea cheltuielilor > Cheltuielile mele > Rapoarte de cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="2b5c0-144">Fluxurile de lucru și orice aprobări vă duc în continuare la pagina de rapoarte de cheltuieli existente.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="2b5c0-145">Chitanțele vor fi procesate prin Microsoft Azure Cognitive Services și metadatele vor fi extrase și adăugate.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="2b5c0-146">Se adaugă o opțiune care vă permite să creați un raport de cheltuieli care include chitanțe neatașate potrivite.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="2b5c0-147">O opțiune care este adăugată la rapoartele de cheltuieli vă permite să creați o linie de cheltuieli dintr-o chitanță sau să încercați să potriviți o chitanță existentă cu o linie de cheltuieli existentă.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2b5c0-148">Întrebări frecvente</span><span class="sxs-lookup"><span data-stu-id="2b5c0-148">Frequently asked questions</span></span>

<span data-ttu-id="2b5c0-149">**Utilizează Microsoft datele mele pentru modelele sale?**</span><span class="sxs-lookup"><span data-stu-id="2b5c0-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="2b5c0-150">Nu, Microsoft a construit un model general învățare programată pentru serviciul său de procesare a chitanțelor.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="2b5c0-151">Acest model nu se bazează pe chitanțele pe care le încărcați.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="2b5c0-152">**Unde este disponibilă și procesată această caracteristică?**</span><span class="sxs-lookup"><span data-stu-id="2b5c0-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="2b5c0-153">În prezent, Statele Unite sunt acceptate.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="2b5c0-154">**Unde merg chitanțele mele?**</span><span class="sxs-lookup"><span data-stu-id="2b5c0-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="2b5c0-155">Finance va contacta serviciile cognitive pentru a extrage datele din câmp.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="2b5c0-156">Serviciile cognitive vor păstra o copie a chitanței dvs. timp de până la 24 de ore în timp ce are loc procesarea.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="2b5c0-157">După finalizarea procesării, Cognitive Services va elimina chitanța.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="2b5c0-158">Chitanțele sunt încă stocate în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="2b5c0-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="2b5c0-159">Pentru mai multe informații, consultați [Activați înțelegerea chitanței cu noua capacitate a Recunoscătorului de formulare](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="2b5c0-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
