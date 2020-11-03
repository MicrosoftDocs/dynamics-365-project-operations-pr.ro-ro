---
title: Prezentare generală a dimensiunilor de preț
description: Acest subiect furnizează informații despre dimensiunile de preț în Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082903"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="e1116-103">Prezentare generală a dimensiunilor de preț</span><span class="sxs-lookup"><span data-stu-id="e1116-103">Pricing dimensions overview</span></span>

<span data-ttu-id="e1116-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="e1116-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1116-105">Dimensiunile care sunt utilizate în resursele umane pentru stabilirea prețurilor și a costurilor se încadrează în două categorii:</span><span class="sxs-lookup"><span data-stu-id="e1116-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="e1116-106">Persoane</span><span class="sxs-lookup"><span data-stu-id="e1116-106">People</span></span>
- <span data-ttu-id="e1116-107">Lucru programat</span><span class="sxs-lookup"><span data-stu-id="e1116-107">Planned work</span></span>

<span data-ttu-id="e1116-108">Din acest motiv, există două tipuri de valori de dimensiune de preț disponibile:</span><span class="sxs-lookup"><span data-stu-id="e1116-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="e1116-109">**Seturi de opțiuni** : dimensiuni care sunt enumerări fixe pentru un set de valori.</span><span class="sxs-lookup"><span data-stu-id="e1116-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e1116-110">**Valori bazate pe entități** : dimensiuni care pot fi un set variat de valori.</span><span class="sxs-lookup"><span data-stu-id="e1116-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e1116-111">Dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="e1116-111">Pricing dimensions</span></span>

<span data-ttu-id="e1116-112">Project Operations Dynamics 365 sunt livrate cu un set implicit de dimensiuni de preț.</span><span class="sxs-lookup"><span data-stu-id="e1116-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e1116-113">Puteți vizualiza aceste dimensiuni de preț accesând **Operațiuni de preț** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="e1116-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="e1116-114">În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum** , verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**.</span><span class="sxs-lookup"><span data-stu-id="e1116-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e1116-115">Când sunt activate aceste câmpuri, puteți configura prețul și costul pentru fiecare rol și combinație de unitate organizatorică.</span><span class="sxs-lookup"><span data-stu-id="e1116-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="e1116-116">Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate.</span><span class="sxs-lookup"><span data-stu-id="e1116-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e1116-117">Preț timp resurse umane</span><span class="sxs-lookup"><span data-stu-id="e1116-117">Pricing human resource time</span></span>
<span data-ttu-id="e1116-118">Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației.</span><span class="sxs-lookup"><span data-stu-id="e1116-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e1116-119">Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.</span><span class="sxs-lookup"><span data-stu-id="e1116-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e1116-120">Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="e1116-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e1116-121">Câmpuri precum **Categoria de tranzacție** ( **msdyn_transactioncategory** ) și **Resursă care se poate rezerva** ( **bookableresource** ) sunt exemple de dimensiuni candidat.</span><span class="sxs-lookup"><span data-stu-id="e1116-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e1116-122">Luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="e1116-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e1116-123">Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, puteți crea o entitate mai degrabă decât un set de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="e1116-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="e1116-124">Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor.</span><span class="sxs-lookup"><span data-stu-id="e1116-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="e1116-125">Următorul exemplu arată ratele de facturare care sunt configurate pe baza rolului și unității de resurse organizaționale la care aparține resursa.</span><span class="sxs-lookup"><span data-stu-id="e1116-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e1116-126">Ratele de cost sunt de obicei bazate pe banda de salariu a angajatului și unitatea de organizație la care aparțin.</span><span class="sxs-lookup"><span data-stu-id="e1116-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e1116-127">În acest exemplu, rata de facturare și tabelele ratei de cost va arata în felul următor.</span><span class="sxs-lookup"><span data-stu-id="e1116-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e1116-128">**Exemple de rate de facturare**</span><span class="sxs-lookup"><span data-stu-id="e1116-128">**Sample bill rates**</span></span>

| <span data-ttu-id="e1116-129">Rol</span><span class="sxs-lookup"><span data-stu-id="e1116-129">Role</span></span>        | <span data-ttu-id="e1116-130">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="e1116-130">Org Unit</span></span>    |<span data-ttu-id="e1116-131">Unitate</span><span class="sxs-lookup"><span data-stu-id="e1116-131">Unit</span></span>      |<span data-ttu-id="e1116-132">Preț</span><span class="sxs-lookup"><span data-stu-id="e1116-132">Price</span></span>      |<span data-ttu-id="e1116-133">Monedă</span><span class="sxs-lookup"><span data-stu-id="e1116-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e1116-134">Dezvoltator</span><span class="sxs-lookup"><span data-stu-id="e1116-134">Developer</span></span>   | <span data-ttu-id="e1116-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e1116-135">Contoso US</span></span>  |<span data-ttu-id="e1116-136">Hour</span><span class="sxs-lookup"><span data-stu-id="e1116-136">Hour</span></span> | <span data-ttu-id="e1116-137">200</span><span class="sxs-lookup"><span data-stu-id="e1116-137">200</span></span>|<span data-ttu-id="e1116-138">USD</span><span class="sxs-lookup"><span data-stu-id="e1116-138">USD</span></span>     |
| <span data-ttu-id="e1116-139">Dezvoltator</span><span class="sxs-lookup"><span data-stu-id="e1116-139">Developer</span></span>   | <span data-ttu-id="e1116-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e1116-140">Contoso India</span></span> |<span data-ttu-id="e1116-141">Hour</span><span class="sxs-lookup"><span data-stu-id="e1116-141">Hour</span></span>|   <span data-ttu-id="e1116-142">112</span><span class="sxs-lookup"><span data-stu-id="e1116-142">112</span></span>|<span data-ttu-id="e1116-143">USD</span><span class="sxs-lookup"><span data-stu-id="e1116-143">USD</span></span>     |


<span data-ttu-id="e1116-144">**Eșantion de rate de cost**</span><span class="sxs-lookup"><span data-stu-id="e1116-144">**Sample cost rates**</span></span>

| <span data-ttu-id="e1116-145">Bandă de salariu</span><span class="sxs-lookup"><span data-stu-id="e1116-145">Salary Band</span></span>     | <span data-ttu-id="e1116-146">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="e1116-146">Org Unit</span></span>    |<span data-ttu-id="e1116-147">Unitate</span><span class="sxs-lookup"><span data-stu-id="e1116-147">Unit</span></span>      |<span data-ttu-id="e1116-148">Preț</span><span class="sxs-lookup"><span data-stu-id="e1116-148">Price</span></span>      |<span data-ttu-id="e1116-149">Monedă</span><span class="sxs-lookup"><span data-stu-id="e1116-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e1116-150">company_Band1 a mea</span><span class="sxs-lookup"><span data-stu-id="e1116-150">My company_Band1</span></span> | <span data-ttu-id="e1116-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e1116-151">Contoso US</span></span>  |<span data-ttu-id="e1116-152">Hour</span><span class="sxs-lookup"><span data-stu-id="e1116-152">Hour</span></span> | <span data-ttu-id="e1116-153">145</span><span class="sxs-lookup"><span data-stu-id="e1116-153">145</span></span>|<span data-ttu-id="e1116-154">USD</span><span class="sxs-lookup"><span data-stu-id="e1116-154">USD</span></span>     |
| <span data-ttu-id="e1116-155">company_Band2 a mea</span><span class="sxs-lookup"><span data-stu-id="e1116-155">My company_Band2</span></span> | <span data-ttu-id="e1116-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="e1116-156">Contoso India</span></span> |<span data-ttu-id="e1116-157">Hour</span><span class="sxs-lookup"><span data-stu-id="e1116-157">Hour</span></span>|   <span data-ttu-id="e1116-158">67</span><span class="sxs-lookup"><span data-stu-id="e1116-158">67</span></span>|<span data-ttu-id="e1116-159">USD</span><span class="sxs-lookup"><span data-stu-id="e1116-159">USD</span></span>     |
