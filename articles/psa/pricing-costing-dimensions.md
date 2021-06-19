---
title: Pagină principală prețuri și dimensiuni de cost
description: Acest subiect oferă o prezentare generală a dimensiunilor prețurilor.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009271"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="f9130-103">Pagină principală prețuri și dimensiuni de cost</span><span class="sxs-lookup"><span data-stu-id="f9130-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f9130-104">Dimensiunile utilizate pentru stabilirea prețurilor și costurilor forței de muncă în organizațiile bazate pe proiecte sunt influențate de următoarele atribute:</span><span class="sxs-lookup"><span data-stu-id="f9130-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="f9130-105">Oamenii care fac o muncă similară cu experiența, rolul sau geografia lor</span><span class="sxs-lookup"><span data-stu-id="f9130-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="f9130-106">Lucrarea care trebuie efectuată similară cu complexitatea sau ora din zi</span><span class="sxs-lookup"><span data-stu-id="f9130-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="f9130-107">Având în vedere natura tipică a acestor atribute de lucru și persoanele necesare pentru a efectua lucrarea, există două tipuri de valori ale dimensiunii prețurilor disponibile în Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="f9130-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="f9130-108">**Seturi de opțiuni** - atribute care sunt enumerări fixe pentru un set de valori.</span><span class="sxs-lookup"><span data-stu-id="f9130-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f9130-109">**Valori bazate pe entități** - Atribute care pot avea un set variat de valori care sunt finite, dar se pot schimba în timp.</span><span class="sxs-lookup"><span data-stu-id="f9130-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f9130-110">Dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="f9130-110">Pricing dimensions</span></span>

<span data-ttu-id="f9130-111">PSA livrează cu un set implicit de dimensiuni de stabilire a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="f9130-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f9130-112">Le puteți vizualiza accesând **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="f9130-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="f9130-113">În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum**, verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**.</span><span class="sxs-lookup"><span data-stu-id="f9130-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f9130-114">Acest lucru vă va permite să configurați prețul și costul pentru fiecare rol și combinație de unitate organizatorică.</span><span class="sxs-lookup"><span data-stu-id="f9130-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captură de ecran a parametrilor Project Service cu „Aplicabil vânzărilor” evidențiat](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="f9130-116">Dacă ați utilizat câmpurile predefinite de unitate de rol și organizaționale ca dimensiuni ale prețurilor la versiunea 3 a PSA, nu va exista nicio modificare observabilă.</span><span class="sxs-lookup"><span data-stu-id="f9130-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="f9130-117">Puteți continua să utilizați Project Service ca de obicei.</span><span class="sxs-lookup"><span data-stu-id="f9130-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="f9130-118">Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate.</span><span class="sxs-lookup"><span data-stu-id="f9130-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="f9130-119">Pentru mai multe informații, consultați următoarele subiecte, însă rețineți că trebuie să finalizați procedurile în ordinea de mai jos:</span><span class="sxs-lookup"><span data-stu-id="f9130-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="f9130-120">Crearea câmpurilor și entităților particularizate</span><span class="sxs-lookup"><span data-stu-id="f9130-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="f9130-121">Adăugarea câmpurilor particularizate la parametrizarea prețurilor și la entitățile tranzacționale</span><span class="sxs-lookup"><span data-stu-id="f9130-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="f9130-122">Configurarea câmpurilor particularizate ca dimensiuni de preț </span><span class="sxs-lookup"><span data-stu-id="f9130-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="f9130-123">Actualizați atributele inserturilor pentru a include noi dimensiuni de tarifare</span><span class="sxs-lookup"><span data-stu-id="f9130-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="f9130-124">Preț timp resurse umane</span><span class="sxs-lookup"><span data-stu-id="f9130-124">Pricing human resource time</span></span>
<span data-ttu-id="f9130-125">Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației.</span><span class="sxs-lookup"><span data-stu-id="f9130-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f9130-126">Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.</span><span class="sxs-lookup"><span data-stu-id="f9130-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f9130-127">Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="f9130-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f9130-128">Câmpuri precum **Categoria de tranzacție** (**msdyn_transactioncategory**) și **Resursă care se poate rezerva** (**bookableresource**) sunt exemple de dimensiuni candidat.</span><span class="sxs-lookup"><span data-stu-id="f9130-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f9130-129">Luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="f9130-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f9130-130">Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, ați putea crea o entitate mai degrabă decât un set de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="f9130-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="f9130-131">Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor de business.</span><span class="sxs-lookup"><span data-stu-id="f9130-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="f9130-132">Următorul exemplu arată ratele de facturare care sunt configurate pe baza rolului și unității de resurse organizaționale la care aparține resursa.</span><span class="sxs-lookup"><span data-stu-id="f9130-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f9130-133">Ratele de cost sunt de obicei bazate pe banda de salariu a angajatului și unitatea de organizație la care aparțin.</span><span class="sxs-lookup"><span data-stu-id="f9130-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f9130-134">În acest exemplu, rata de facturare și tabelele ratei de cost va arata în felul următor.</span><span class="sxs-lookup"><span data-stu-id="f9130-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f9130-135">**Exemple de rate de facturare**</span><span class="sxs-lookup"><span data-stu-id="f9130-135">**Sample bill rates**</span></span>

| <span data-ttu-id="f9130-136">Rol</span><span class="sxs-lookup"><span data-stu-id="f9130-136">Role</span></span>        | <span data-ttu-id="f9130-137">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="f9130-137">Org Unit</span></span>    |<span data-ttu-id="f9130-138">Unitate</span><span class="sxs-lookup"><span data-stu-id="f9130-138">Unit</span></span>      |<span data-ttu-id="f9130-139">Preț</span><span class="sxs-lookup"><span data-stu-id="f9130-139">Price</span></span>      |<span data-ttu-id="f9130-140">Monedă</span><span class="sxs-lookup"><span data-stu-id="f9130-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f9130-141">Dezvoltator</span><span class="sxs-lookup"><span data-stu-id="f9130-141">Developer</span></span>   | <span data-ttu-id="f9130-142">Contoso SUA</span><span class="sxs-lookup"><span data-stu-id="f9130-142">Contoso US</span></span>  |<span data-ttu-id="f9130-143">Oră</span><span class="sxs-lookup"><span data-stu-id="f9130-143">Hour</span></span> | <span data-ttu-id="f9130-144">200</span><span class="sxs-lookup"><span data-stu-id="f9130-144">200</span></span>|<span data-ttu-id="f9130-145">USD</span><span class="sxs-lookup"><span data-stu-id="f9130-145">USD</span></span>     |
| <span data-ttu-id="f9130-146">Dezvoltator</span><span class="sxs-lookup"><span data-stu-id="f9130-146">Developer</span></span>   | <span data-ttu-id="f9130-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f9130-147">Contoso India</span></span> |<span data-ttu-id="f9130-148">Oră</span><span class="sxs-lookup"><span data-stu-id="f9130-148">Hour</span></span>|   <span data-ttu-id="f9130-149">112</span><span class="sxs-lookup"><span data-stu-id="f9130-149">112</span></span>|<span data-ttu-id="f9130-150">USD</span><span class="sxs-lookup"><span data-stu-id="f9130-150">USD</span></span>     |


<span data-ttu-id="f9130-151">**Eșantion de rate de cost**</span><span class="sxs-lookup"><span data-stu-id="f9130-151">**Sample cost rates**</span></span>

| <span data-ttu-id="f9130-152">Bandă de salariu</span><span class="sxs-lookup"><span data-stu-id="f9130-152">Salary Band</span></span>     | <span data-ttu-id="f9130-153">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="f9130-153">Org Unit</span></span>    |<span data-ttu-id="f9130-154">Unitate</span><span class="sxs-lookup"><span data-stu-id="f9130-154">Unit</span></span>      |<span data-ttu-id="f9130-155">Preț</span><span class="sxs-lookup"><span data-stu-id="f9130-155">Price</span></span>      |<span data-ttu-id="f9130-156">Monedă</span><span class="sxs-lookup"><span data-stu-id="f9130-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f9130-157">company_Band1 a mea</span><span class="sxs-lookup"><span data-stu-id="f9130-157">My company_Band1</span></span> | <span data-ttu-id="f9130-158">Contoso SUA</span><span class="sxs-lookup"><span data-stu-id="f9130-158">Contoso US</span></span>  |<span data-ttu-id="f9130-159">Oră</span><span class="sxs-lookup"><span data-stu-id="f9130-159">Hour</span></span> | <span data-ttu-id="f9130-160">145</span><span class="sxs-lookup"><span data-stu-id="f9130-160">145</span></span>|<span data-ttu-id="f9130-161">USD</span><span class="sxs-lookup"><span data-stu-id="f9130-161">USD</span></span>     |
| <span data-ttu-id="f9130-162">company_Band2 a mea</span><span class="sxs-lookup"><span data-stu-id="f9130-162">My company_Band2</span></span> | <span data-ttu-id="f9130-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="f9130-163">Contoso India</span></span> |<span data-ttu-id="f9130-164">Oră</span><span class="sxs-lookup"><span data-stu-id="f9130-164">Hour</span></span>|   <span data-ttu-id="f9130-165">67</span><span class="sxs-lookup"><span data-stu-id="f9130-165">67</span></span>|<span data-ttu-id="f9130-166">USD</span><span class="sxs-lookup"><span data-stu-id="f9130-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]