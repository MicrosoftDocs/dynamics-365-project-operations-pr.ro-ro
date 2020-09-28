---
title: Utilizarea categoriei de tranzacții ca dimensiune de preț
description: Acest subiect furnizează informații despre utilizarea unei categorii de tranzacții ca dimensiune de preț.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754816"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="40f73-103">Utilizarea categoriei de tranzacții ca dimensiune de preț</span><span class="sxs-lookup"><span data-stu-id="40f73-103">Use transaction category as a pricing dimension</span></span>
<span data-ttu-id="40f73-104">Acest subiect arată cum se utilizează o categorie de tranzacții ca dimensiune de preț.</span><span class="sxs-lookup"><span data-stu-id="40f73-104">This topic shows how to use a transaction category as a pricing dimension.</span></span> <span data-ttu-id="40f73-105">Înainte de a începe, dacă nu ați creat deja o soluție de dimensiune de preț, va trebui să creați una nouă.</span><span class="sxs-lookup"><span data-stu-id="40f73-105">Before you begin, if you have not already created a pricing dimension solution, you will need to create a new one.</span></span> <span data-ttu-id="40f73-106">Dacă aveți deja o soluție de dimensiune de preț, atunci puteți face modificările în această soluție.</span><span class="sxs-lookup"><span data-stu-id="40f73-106">If you already have a pricing dimension solution, then you can make your changes in that solution.</span></span> <span data-ttu-id="40f73-107">Dacă nu ați creat o nouă soluție de dimensiune de preț pentru organizația dvs., finalizați procedurile din subiectul [Creare câmpuri și entități particularizate](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="40f73-107">If you have not created a new pricing dimension solution for your organization, complete the procedures in the [Create custom fields and entities](create-custom-fields-entities.md) topic.</span></span>

## <a name="add-transaction-category-to-forms-and-views"></a><span data-ttu-id="40f73-108">Adăugați o categorie de tranzacții la formulare și vizualizări</span><span class="sxs-lookup"><span data-stu-id="40f73-108">Add transaction category to forms and views</span></span>
<span data-ttu-id="40f73-109">Pentru a face categoria de tranzacții vizibilă în interfața cu utilizatorul în soluția de dimensiune de preț, va trebui să parcurgeți toate formularele și vizualizările entităților cheie și să adăugați aceste câmpuri la formularele și vizualizările acelor entități.</span><span class="sxs-lookup"><span data-stu-id="40f73-109">To make transaction category visible in the UI in the pricing dimension solution, you will need to walk through all the forms and views of the key entities and add these fields to the forms and views of those entities.</span></span>
<span data-ttu-id="40f73-110">Următorul tabel este o listă cuprinzătoare a formularelor și vizualizărilor predefinite, listate per entitate, care vor trebui actualizate cu noile câmpuri.</span><span class="sxs-lookup"><span data-stu-id="40f73-110">The following table is a comprehensive list of the out-of-the box forms and views, listed by entity, that will need to be updated with the new fields.</span></span> <span data-ttu-id="40f73-111">Dacă există vizualizări sau formulare suplimentare în particularizările acestor entități, adăugați noile câmpuri și la acelea.</span><span class="sxs-lookup"><span data-stu-id="40f73-111">If there any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>

|  <span data-ttu-id="40f73-112">Entitate</span><span class="sxs-lookup"><span data-stu-id="40f73-112">Entity</span></span>        | <span data-ttu-id="40f73-113">Formulare</span><span class="sxs-lookup"><span data-stu-id="40f73-113">Forms</span></span>     |<span data-ttu-id="40f73-114">Vizualizări</span><span class="sxs-lookup"><span data-stu-id="40f73-114">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="40f73-115">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="40f73-115">Role Price</span></span>|<span data-ttu-id="40f73-116">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-116">• Information</span></span> |<span data-ttu-id="40f73-117">• Prețuri categorii de resurse active</span><span class="sxs-lookup"><span data-stu-id="40f73-117">• Active Resource Category Prices</span></span><br> <span data-ttu-id="40f73-118">• Vizualizare asociată prețuri categorii de resurse</span><span class="sxs-lookup"><span data-stu-id="40f73-118">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="40f73-119">Adaos de preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="40f73-119">Role Price Markup</span></span>|<span data-ttu-id="40f73-120">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-120">• Information</span></span>|<span data-ttu-id="40f73-121">• Adaos la prețul de rol activ</span><span class="sxs-lookup"><span data-stu-id="40f73-121">• Active Role Price Markup</span></span><br><span data-ttu-id="40f73-122">• Vizualizare asociată adaosului la prețurile de rol</span><span class="sxs-lookup"><span data-stu-id="40f73-122">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="40f73-123">Detaliu linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="40f73-123">Quote line detail</span></span>|<span data-ttu-id="40f73-124">• Informații proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-124">• Project Information</span></span><br><span data-ttu-id="40f73-125">• Creare rapidă proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-125">• Project Quick Create</span></span>|<span data-ttu-id="40f73-126">• Detaliu linie de ofertă activă</span><span class="sxs-lookup"><span data-stu-id="40f73-126">• Active Quote Line Detail</span></span><br><span data-ttu-id="40f73-127">• Detalii de linie ofertă combinate</span><span class="sxs-lookup"><span data-stu-id="40f73-127">• Combined Quote Line Details</span></span><br><span data-ttu-id="40f73-128">• Vizualizare asociată a detaliilor de linie ofertă</span><span class="sxs-lookup"><span data-stu-id="40f73-128">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="40f73-129">Detaliu linie contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-129">Project Contract line detail</span></span>|<span data-ttu-id="40f73-130">• Informații proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-130">• Project Information</span></span><br><span data-ttu-id="40f73-131">• Creare rapidă proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-131">• Project Quick Create</span></span>|<span data-ttu-id="40f73-132">• Detalii din linie de contract combinate</span><span class="sxs-lookup"><span data-stu-id="40f73-132">• Combined Contract line Details</span></span><br><span data-ttu-id="40f73-133">• Detalii linie de contract active</span><span class="sxs-lookup"><span data-stu-id="40f73-133">• Active Contract Line Details</span></span><br><span data-ttu-id="40f73-134">• Vizualizare asociată pentru detalii din linia de contract</span><span class="sxs-lookup"><span data-stu-id="40f73-134">• Contract Line Detail associated view</span></span>|
|  <span data-ttu-id="40f73-135">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-135">Project Team Member</span></span>|<span data-ttu-id="40f73-136">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-136">• Information</span></span><br><span data-ttu-id="40f73-137">• Formular nou</span><span class="sxs-lookup"><span data-stu-id="40f73-137">• New Form</span></span>|<span data-ttu-id="40f73-138">• Membri echipă de proiect activi</span><span class="sxs-lookup"><span data-stu-id="40f73-138">• Active Project Team Members</span></span><br><span data-ttu-id="40f73-139">• Membri echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-139">• Project Team Members</span></span><br><span data-ttu-id="40f73-140">• Vizualizare asociată membri echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="40f73-140">• Project Team members associated View</span></span>|
|  <span data-ttu-id="40f73-141">Intrare de timp</span><span class="sxs-lookup"><span data-stu-id="40f73-141">Time Entry</span></span>|<span data-ttu-id="40f73-142">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-142">• Information</span></span><br><span data-ttu-id="40f73-143">• Creare intrare de timp</span><span class="sxs-lookup"><span data-stu-id="40f73-143">• Create Time Entry</span></span>|<span data-ttu-id="40f73-144">• Intrările mele de timp după dată</span><span class="sxs-lookup"><span data-stu-id="40f73-144">• My Time Entries By Date</span></span><br><span data-ttu-id="40f73-145">• Intrările mele de timp pentru această săptămână</span><span class="sxs-lookup"><span data-stu-id="40f73-145">• My time Entries for this week</span></span><br><span data-ttu-id="40f73-146">• Intrări de timp pentru aprobare.</span><span class="sxs-lookup"><span data-stu-id="40f73-146">• Time entries for approval</span></span>|
|  <span data-ttu-id="40f73-147">Linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="40f73-147">Journal Line</span></span>|<span data-ttu-id="40f73-148">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-148">• Information</span></span><br><span data-ttu-id="40f73-149">• Creare rapidă</span><span class="sxs-lookup"><span data-stu-id="40f73-149">• Quick create</span></span>|<span data-ttu-id="40f73-150">• Linii de jurnal active</span><span class="sxs-lookup"><span data-stu-id="40f73-150">• Active journal lines</span></span><br><span data-ttu-id="40f73-151">• Vizualizare asociată linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="40f73-151">• Journal Line associated view</span></span>|
|  <span data-ttu-id="40f73-152">Detaliu linie factură</span><span class="sxs-lookup"><span data-stu-id="40f73-152">Invoice Line Detail</span></span>|<span data-ttu-id="40f73-153">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-153">• Information</span></span><br><span data-ttu-id="40f73-154">• Creare rapidă</span><span class="sxs-lookup"><span data-stu-id="40f73-154">• Quick create</span></span>|<span data-ttu-id="40f73-155">• Detalii de linie factură active</span><span class="sxs-lookup"><span data-stu-id="40f73-155">• Active Invoice Line Details</span></span><br><span data-ttu-id="40f73-156">• Tranzacții de factură facturabile</span><span class="sxs-lookup"><span data-stu-id="40f73-156">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="40f73-157">• Tranzacții de factură gratuite</span><span class="sxs-lookup"><span data-stu-id="40f73-157">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="40f73-158">• Vizualizare asociată a detaliilor de linie factură</span><span class="sxs-lookup"><span data-stu-id="40f73-158">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="40f73-159">• Tranzacție de factură nefacturabilă</span><span class="sxs-lookup"><span data-stu-id="40f73-159">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="40f73-160">Real</span><span class="sxs-lookup"><span data-stu-id="40f73-160">Actual</span></span>|<span data-ttu-id="40f73-161">• Informații</span><span class="sxs-lookup"><span data-stu-id="40f73-161">• Information</span></span><br><span data-ttu-id="40f73-162">• Valori reale active</span><span class="sxs-lookup"><span data-stu-id="40f73-162">• Active Actuals</span></span>|<span data-ttu-id="40f73-163">• Vizualizare asociată valori reale</span><span class="sxs-lookup"><span data-stu-id="40f73-163">• Actual Associated view</span></span>|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="40f73-164">Configurarea categoriei de tranzacții ca dimensiune de preț</span><span class="sxs-lookup"><span data-stu-id="40f73-164">Set up transaction category as a pricing dimension</span></span>

1. <span data-ttu-id="40f73-165">În interfața web, accesați **Project Service** > **Setări** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="40f73-165">In the web interface, go to **Project Service** > **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="40f73-166">Pa pagina **Parametri**, pe fila **Dimensiuni prețuri bazate pe sumă**, observați că grila de pe filă afișează înregistrările din entitatea **Dimensiuni preț**.</span><span class="sxs-lookup"><span data-stu-id="40f73-166">On the **Parameters** page, on the **Amount-Based Pricing Dimensions** tab, note the grid on the tab shows the records in the **Pricing Dimensions** entity.</span></span>
3. <span data-ttu-id="40f73-167">Adăugați **Categorie de tranzacții** la această listă și setați câmpurile **Aplicabil la cost** și **Aplicabil la vânzare** la **Da**.</span><span class="sxs-lookup"><span data-stu-id="40f73-167">Add **Transaction Category** to this list and set the **Applicable to Cost** and **Applicable to Sale** fields set to **Yes**.</span></span>
4. <span data-ttu-id="40f73-168">În câmpul **Tip dimensiune** selectați **Bazat pe sumă**, apoi selectați prioritatea pentru **Categoria de tranzacții** referitoare la cost și vânzări.</span><span class="sxs-lookup"><span data-stu-id="40f73-168">In the **Dimension Type** field, select **Amount-based**, and then select the priority for **Transaction Category** related to cost and sales.</span></span>