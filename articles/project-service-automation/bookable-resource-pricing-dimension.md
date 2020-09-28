---
title: Utilizați resursa care se poate rezerva ca dimensiune de tarifare
description: Acest subiect furnizează informații despre utilizarea unei resurse rezervabile ca dimensiune de tarifare.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d147827-dc55-48a5-b3f6-d8b00bd1c7f7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 999f7575d1777077376ba74933654b90fcc504c3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754755"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="47db7-103">Utilizați resursa care se poate rezerva ca dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="47db7-103">Use bookable resource as a pricing dimension</span></span>
<span data-ttu-id="47db7-104">Acest subiect furnizează informații despre utilizarea unei resurse rezervabile ca dimensiune de tarifare.</span><span class="sxs-lookup"><span data-stu-id="47db7-104">This topic provides information about using a bookable resource as a pricing dimension.</span></span> <span data-ttu-id="47db7-105">Înainte de a începe, dacă nu ați creat deja o soluție de dimensiune de preț, va trebui să creați una nouă.</span><span class="sxs-lookup"><span data-stu-id="47db7-105">Before you begin, if you have not already created a pricing dimension solution, you will need to create a new one.</span></span> <span data-ttu-id="47db7-106">Dacă aveți deja o soluție de dimensiune de preț, atunci puteți face modificările în această soluție.</span><span class="sxs-lookup"><span data-stu-id="47db7-106">If you already have a pricing dimension solution, then you can make your changes in that solution.</span></span> <span data-ttu-id="47db7-107">Dacă nu ați creat o nouă soluție de dimensiune de preț pentru organizația dvs., finalizați procedurile din subiectul [Creare câmpuri și entități particularizate](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="47db7-107">If you have not created a new pricing dimension solution for your organization, complete the procedures in the [Create custom fields and entities](create-custom-fields-entities.md) topic.</span></span>

## <a name="add-bookable-resource-to-forms-and-views"></a><span data-ttu-id="47db7-108">Adăugați o resursă rezervabilă la formulare și vizualizări</span><span class="sxs-lookup"><span data-stu-id="47db7-108">Add bookable resource to forms and views</span></span>
<span data-ttu-id="47db7-109">Pentru a face câmpurile vizibile în interfața cu utilizatorul în soluția de dimensiune de tarifare, va trebui să parcurgeți toate formularele și vizualizările entităților cheie Project Service și să adăugați aceste câmpuri la formularele și vizualizările acelor entități.</span><span class="sxs-lookup"><span data-stu-id="47db7-109">To make the fields visible in the UI in the pricing dimension solution, you will need to walk through all of the forms and views of the key Project Service entities and add these fields to the forms and views of those entities.</span></span>
<span data-ttu-id="47db7-110">Următorul tabel este o listă cuprinzătoare a formularelor și vizualizărilor predefinite, enumerate după entitate, care vor trebui actualizate.</span><span class="sxs-lookup"><span data-stu-id="47db7-110">The following table is a comprehensive list of the out-of-the box forms and views, listed by entity, that will need to be updated.</span></span> <span data-ttu-id="47db7-111">Dacă există vizualizări sau formulare suplimentare în particularizările acestor entități, adăugați noile câmpuri și la acelea.</span><span class="sxs-lookup"><span data-stu-id="47db7-111">If there are any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>
<span data-ttu-id="47db7-112">Deschideți exploratorul de soluții pentru soluția de dimensiune de tarifare și apoi faceți clic pe **Publicare toate particularizările**.</span><span class="sxs-lookup"><span data-stu-id="47db7-112">Open Solution Explorer for the pricing dimension solution and then click **Publish All Customizations**.</span></span>


|   <span data-ttu-id="47db7-113">Entitate</span><span class="sxs-lookup"><span data-stu-id="47db7-113">Entity</span></span>        | <span data-ttu-id="47db7-114">Formulare</span><span class="sxs-lookup"><span data-stu-id="47db7-114">Forms</span></span>   |<span data-ttu-id="47db7-115">Vizualizări</span><span class="sxs-lookup"><span data-stu-id="47db7-115">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="47db7-116">Preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="47db7-116">Role Price</span></span>|<span data-ttu-id="47db7-117">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-117">• Information</span></span> |<span data-ttu-id="47db7-118">• Prețuri categorii de resurse active</span><span class="sxs-lookup"><span data-stu-id="47db7-118">• Active Resource Category Prices</span></span><br> <span data-ttu-id="47db7-119">• Vizualizare asociată prețuri categorii de resurse</span><span class="sxs-lookup"><span data-stu-id="47db7-119">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="47db7-120">Adaos de preț pentru rol</span><span class="sxs-lookup"><span data-stu-id="47db7-120">Role Price Markup</span></span>|<span data-ttu-id="47db7-121">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-121">• Information</span></span>|<span data-ttu-id="47db7-122">• Adaos la prețul de rol activ</span><span class="sxs-lookup"><span data-stu-id="47db7-122">• Active Role Price Markup</span></span><br><span data-ttu-id="47db7-123">• Vizualizare asociată adaosului la prețurile de rol</span><span class="sxs-lookup"><span data-stu-id="47db7-123">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="47db7-124">Detaliu linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="47db7-124">Quote line detail</span></span>|<span data-ttu-id="47db7-125">• Informații proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-125">• Project Information</span></span><br><span data-ttu-id="47db7-126">• Creare rapidă proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-126">• Project Quick Create</span></span>|<span data-ttu-id="47db7-127">• Detaliu linie de ofertă activă</span><span class="sxs-lookup"><span data-stu-id="47db7-127">• Active Quote Line Detail</span></span><br><span data-ttu-id="47db7-128">• Detalii de linie ofertă combinate</span><span class="sxs-lookup"><span data-stu-id="47db7-128">• Combined Quote Line Details</span></span><br><span data-ttu-id="47db7-129">• Vizualizare asociată a detaliilor de linie ofertă</span><span class="sxs-lookup"><span data-stu-id="47db7-129">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="47db7-130">Detaliu linie contract pentru proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-130">Project Contract line detail</span></span>|<span data-ttu-id="47db7-131">• Informații proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-131">• Project Information</span></span><br><span data-ttu-id="47db7-132">• Creare rapidă proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-132">• Project Quick Create</span></span>|<span data-ttu-id="47db7-133">• Detalii din linie de contract combinate</span><span class="sxs-lookup"><span data-stu-id="47db7-133">• Combined Contract line Details</span></span><br><span data-ttu-id="47db7-134">• Detalii linie de contract active</span><span class="sxs-lookup"><span data-stu-id="47db7-134">• Active Contract Line Details</span></span><br><span data-ttu-id="47db7-135">• Vizualizare asociată pentru detalii din linia de contract</span><span class="sxs-lookup"><span data-stu-id="47db7-135">• Contract Line Detail associated view</span></span>|
|  <span data-ttu-id="47db7-136">Membru echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-136">Project Team Member</span></span>|<span data-ttu-id="47db7-137">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-137">• Information</span></span><br><span data-ttu-id="47db7-138">• Formular nou</span><span class="sxs-lookup"><span data-stu-id="47db7-138">• New Form</span></span>|<span data-ttu-id="47db7-139">• Membri echipă de proiect activi</span><span class="sxs-lookup"><span data-stu-id="47db7-139">• Active Project Team Members</span></span><br><span data-ttu-id="47db7-140">• Membri echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-140">• Project Team Members</span></span><br><span data-ttu-id="47db7-141">• Vizualizare asociată membri echipă de proiect</span><span class="sxs-lookup"><span data-stu-id="47db7-141">• Project Team members associated View</span></span>|
|  <span data-ttu-id="47db7-142">Intrare de timp</span><span class="sxs-lookup"><span data-stu-id="47db7-142">Time Entry</span></span>|<span data-ttu-id="47db7-143">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-143">• Information</span></span><br><span data-ttu-id="47db7-144">• Creare intrare de timp</span><span class="sxs-lookup"><span data-stu-id="47db7-144">• Create Time Entry</span></span>|<span data-ttu-id="47db7-145">• Intrările mele de timp după dată</span><span class="sxs-lookup"><span data-stu-id="47db7-145">• My Time Entries By Date</span></span><br><span data-ttu-id="47db7-146">• Intrările mele de timp pentru această săptămână</span><span class="sxs-lookup"><span data-stu-id="47db7-146">• My time Entries for this week</span></span><br><span data-ttu-id="47db7-147">• Intrări de timp pentru aprobare.</span><span class="sxs-lookup"><span data-stu-id="47db7-147">• Time entries for approval</span></span>|
|  <span data-ttu-id="47db7-148">Linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="47db7-148">Journal Line</span></span>|<span data-ttu-id="47db7-149">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-149">• Information</span></span><br><span data-ttu-id="47db7-150">• Creare rapidă</span><span class="sxs-lookup"><span data-stu-id="47db7-150">• Quick create</span></span>|<span data-ttu-id="47db7-151">• Linii de jurnal active</span><span class="sxs-lookup"><span data-stu-id="47db7-151">• Active journal lines</span></span><br><span data-ttu-id="47db7-152">• Vizualizare asociată linie de jurnal</span><span class="sxs-lookup"><span data-stu-id="47db7-152">• Journal Line associated view</span></span>|
|  <span data-ttu-id="47db7-153">Detaliu linie factură</span><span class="sxs-lookup"><span data-stu-id="47db7-153">Invoice Line Detail</span></span>|<span data-ttu-id="47db7-154">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-154">• Information</span></span><br><span data-ttu-id="47db7-155">• Creare rapidă</span><span class="sxs-lookup"><span data-stu-id="47db7-155">• Quick create</span></span>|<span data-ttu-id="47db7-156">• Detalii de linie factură active</span><span class="sxs-lookup"><span data-stu-id="47db7-156">• Active Invoice Line Details</span></span><br><span data-ttu-id="47db7-157">• Tranzacții de factură facturabile</span><span class="sxs-lookup"><span data-stu-id="47db7-157">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="47db7-158">• Tranzacții de factură gratuite</span><span class="sxs-lookup"><span data-stu-id="47db7-158">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="47db7-159">• Vizualizare asociată a detaliilor de linie factură</span><span class="sxs-lookup"><span data-stu-id="47db7-159">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="47db7-160">• Tranzacție de factură nefacturabilă</span><span class="sxs-lookup"><span data-stu-id="47db7-160">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="47db7-161">Real</span><span class="sxs-lookup"><span data-stu-id="47db7-161">Actual</span></span>|<span data-ttu-id="47db7-162">• Informații</span><span class="sxs-lookup"><span data-stu-id="47db7-162">• Information</span></span><br><span data-ttu-id="47db7-163">• Valori reale active</span><span class="sxs-lookup"><span data-stu-id="47db7-163">• Active Actuals</span></span>|<span data-ttu-id="47db7-164">• Vizualizare asociată valori reale</span><span class="sxs-lookup"><span data-stu-id="47db7-164">• Actual Associated view</span></span>|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="47db7-165">Configurați resursa care se poate rezerva ca dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="47db7-165">Set up bookable resource as a pricing dimension</span></span>

1. <span data-ttu-id="47db7-166">În interfața web, accesați **Project Service** > **Setări** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="47db7-166">In the web interface, go to **Project Service** > **Settings** > **Parameters**.</span></span> <span data-ttu-id="47db7-167">Pa pagina **Parametri**, în fila **Dimensiuni de tarifare bazate pe sumă**, observați că grila de pe filă afișează înregistrările din entitatea Dimensiuni de tarifare.</span><span class="sxs-lookup"><span data-stu-id="47db7-167">On the **Parameter** page, on the **Amount-Based Pricing Dimensions** tab, notice that the grid on the tab shows the records in the pricing dimensions entity.</span></span> 
2. <span data-ttu-id="47db7-168">Adăugați **Resursă rezervabilă** la această listă de dimensiuni de tarifare ca **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="47db7-168">Add **Bookable Resource** to this list of pricing dimensions as **msdyn_bookableresource**.</span></span> 
3. <span data-ttu-id="47db7-169">Indicați contextul în care resursa care se poate rezerva funcționează ca dimensiune de tarifare și setați valorile **Aplicabilă costurilor** și **Aplicabilă vânzărilor**.</span><span class="sxs-lookup"><span data-stu-id="47db7-169">Indicate the context in which the bookable resource works as a pricing dimension and set the **Applicable to cost** and **Applicable to sales** values.</span></span>
4. <span data-ttu-id="47db7-170">În câmpul **Tip dimensiune**, selectați **Pe bază de sumă**.</span><span class="sxs-lookup"><span data-stu-id="47db7-170">In the **Dimension Type** field, select **Amount-based**.</span></span> 
5. <span data-ttu-id="47db7-171">Selectați prioritatea de cost și de vânzări pentru resursa care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="47db7-171">Select the cost and sales priority for the bookable resource.</span></span> <span data-ttu-id="47db7-172">De obicei, atunci când este inclusă ca o dimensiune de tarifare, o resursă care se poate rezerva are cea mai mare prioritate, așa că setarea acesteia la **1** (sau **0**, în funcție de modul în care numerotați prioritatea) ar asigura acel comportament.</span><span class="sxs-lookup"><span data-stu-id="47db7-172">Typically, when included as a pricing dimension, a bookable resource has the highest priority so setting this to **1** (or **0** depending on how you count the priority) would ensure that behavior.</span></span>

## <a name="set-up-pricing-dimension-field-names"></a><span data-ttu-id="47db7-173">Configurați numele de câmpuri pentru dimensiunea de tarifare</span><span class="sxs-lookup"><span data-stu-id="47db7-173">Set up pricing dimension field names</span></span>

<span data-ttu-id="47db7-174">Când numele câmpului unei dimensiuni de tarifare din tabelul **Preț pentru rol** este diferit de numele său de câmp în oricare dintre celelalte entități unde trebuie să funcționeze valoarea implicită a prețului, înregistrarea dimensiunii de tarifare trebuie să fie informată cu privire la numele diferite.</span><span class="sxs-lookup"><span data-stu-id="47db7-174">When the field name of a pricing dimension in the **Role Price** table is different from its field name in any of the other entities where price defaulting needs to work, the pricing dimension record must be made aware of the different names.</span></span>    
<span data-ttu-id="47db7-175">Pentru resursa care poate fi rezervată, entitatea **Membri echipă de proiect** are un nume de câmp ușor diferit (**msdyn_bookableresourceid**) față de denumirea din entitatea **Preț pentru rol** (**msdyn_ bookableresource**).</span><span class="sxs-lookup"><span data-stu-id="47db7-175">For bookable resource, the **Project Team Members** entity has a slightly different field name (**msdyn_bookableresourceid**) from what it is called on the **Role price** entity (**msdyn_bookableresource**).</span></span> <span data-ttu-id="47db7-176">Înregistrarea dimensiunii de tarifare pentru **msydn_bookableresource** trebuie să fie informată despre acest lucru.</span><span class="sxs-lookup"><span data-stu-id="47db7-176">The pricing dimension record for **msydn_bookableresource** must be made aware of this.</span></span> 
1. <span data-ttu-id="47db7-177">Pentru aceasta, faceți dublu clic pe rândul din grila de **Dimensiuni de tarifare** pentru a deschide pagina de dimensiuni a **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="47db7-177">To do this, double-click the row in the **Pricing Dimensions** grid to open the dimension page of **msdyn_bookableresource**.</span></span>
2. <span data-ttu-id="47db7-178">Pe pagina de dimensiuni, în fila **Corelate**, faceți clic pe **Nume câmpuri de dimensiune de tarifare**.</span><span class="sxs-lookup"><span data-stu-id="47db7-178">On dimension page, on the **Related** tab, click **Pricing Dimension Field Names**.</span></span>

 ![Fila Nume câmpuri de dimensiune de tarifare](media/PD-fieldname.png)

4. <span data-ttu-id="47db7-180">În vizualizarea asociată care se deschide, faceți clic pe **Adăugare nume câmp dimensiune de tarifare nou**.</span><span class="sxs-lookup"><span data-stu-id="47db7-180">On the associated view that opens, click **Add New Pricing Dimension Field Name**.</span></span>

 ![Adăugați nume de câmpuri de dimensiune de tarifare noi](media/Add-NewPD-fieldname.png)


<span data-ttu-id="47db7-182">Acest lucru deschide pagina **Nume câmp dimensiune de tarifare nou** pentru **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="47db7-182">This opens the **New Pricing dimension field name** page for **msdyn_bookableresource**.</span></span> 

5. <span data-ttu-id="47db7-183">Adăugați **msdyn_projectteam** la câmpul **Nume logic al entității** și **msdyn_bookableresourceid** la câmpul **Nume câmp**.</span><span class="sxs-lookup"><span data-stu-id="47db7-183">Add **msdyn_projectteam** to the **Entity Locigal Name** field and **msdyn_bookableresourceid** to the **Field Name** field.</span></span> <span data-ttu-id="47db7-184">Salvaţi înregistrarea.</span><span class="sxs-lookup"><span data-stu-id="47db7-184">Save the record.</span></span>

 ![Formular pentru nume de câmpuri de dimensiune de tarifare noi](media/PD-fieldname-Added.png)