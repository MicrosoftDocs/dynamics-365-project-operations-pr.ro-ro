---
title: Prezentare generală a dimensiunilor de preț
description: Acest subiect furnizează informații despre dimensiunile de preț în Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898231"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="0202c-103">Prezentare generală a dimensiunilor de preț</span><span class="sxs-lookup"><span data-stu-id="0202c-103">Pricing dimensions overview</span></span>

<span data-ttu-id="0202c-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="0202c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0202c-105">Dimensiunile care sunt utilizate în resursele umane pentru stabilirea prețurilor și a costurilor se încadrează în două categorii:</span><span class="sxs-lookup"><span data-stu-id="0202c-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="0202c-106">Persoane</span><span class="sxs-lookup"><span data-stu-id="0202c-106">People</span></span>
- <span data-ttu-id="0202c-107">Lucru programat</span><span class="sxs-lookup"><span data-stu-id="0202c-107">Planned work</span></span>

<span data-ttu-id="0202c-108">Din acest motiv, există două tipuri de valori de dimensiune de preț disponibile:</span><span class="sxs-lookup"><span data-stu-id="0202c-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="0202c-109">**Seturi de opțiuni**: dimensiuni care sunt enumerări fixe pentru un set de valori.</span><span class="sxs-lookup"><span data-stu-id="0202c-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="0202c-110">**Valori bazate pe entități**: dimensiuni care pot fi un set variat de valori.</span><span class="sxs-lookup"><span data-stu-id="0202c-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="0202c-111">Dimensiuni de preț</span><span class="sxs-lookup"><span data-stu-id="0202c-111">Pricing dimensions</span></span>

<span data-ttu-id="0202c-112">Project Operations Dynamics 365 sunt livrate cu un set implicit de dimensiuni de preț.</span><span class="sxs-lookup"><span data-stu-id="0202c-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="0202c-113">Puteți vizualiza aceste dimensiuni de preț accesând **Operațiuni de preț** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="0202c-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="0202c-114">În înregistrarea parametru, pe fila **Dimensiuni de preț bazate pe volum**, verificați că rolul **, msdyn_resourcecategory** și unitatea organizațională de obținere a resurselor **msdyn_organizationalunit** au câmpurile **Aplicabile vânzărilor** și **Aplicabile costurilor** setate la **Da**.</span><span class="sxs-lookup"><span data-stu-id="0202c-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="0202c-115">Când sunt activate aceste câmpuri, puteți configura prețul și costul pentru fiecare rol și combinație de unitate organizatorică.</span><span class="sxs-lookup"><span data-stu-id="0202c-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="0202c-116">Dacă aveți nevoie de preț sau cost pentru resurse utilizând atribute suplimentare, aveți posibilitatea să creați câmpuri, entități și dimensiuni particularizate.</span><span class="sxs-lookup"><span data-stu-id="0202c-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="0202c-117">Preț timp resurse umane</span><span class="sxs-lookup"><span data-stu-id="0202c-117">Pricing human resource time</span></span>
<span data-ttu-id="0202c-118">Cum o organizație stabilește prețul timpul resurselor umane este adesea o considerație strategică importantă care afectează direct profitabilitatea organizației.</span><span class="sxs-lookup"><span data-stu-id="0202c-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="0202c-119">Lucrați cu echipele de finanțe și cu șefii practicilor atunci când organizația este pregătită să identifice modul în care dorește să configureze ratele de factură și cost pentru timpul resurselor umane.</span><span class="sxs-lookup"><span data-stu-id="0202c-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="0202c-120">Alte considerente de stabilire a prețurilor includ dacă să reutilizați câmpuri sau entități care nu sunt în prezent dimensiuni de preț, dar se aplică ca o dimensiune de preț pentru organizația dvs.</span><span class="sxs-lookup"><span data-stu-id="0202c-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="0202c-121">Câmpuri precum **Categoria de tranzacție** (**msdyn_transactioncategory**) și **Resursă care se poate rezerva** (**bookableresource**) sunt exemple de dimensiuni candidat.</span><span class="sxs-lookup"><span data-stu-id="0202c-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="0202c-122">Luați în considerare dacă dimensiunea de preț ar trebui să fie un tabel sau un set de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="0202c-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="0202c-123">Dacă preconizați modificări ale valorilor unei dimensiuni care va depăși 10 sau 12 și aveți nevoie de atribute suplimentare pentru aceste valori, puteți crea o entitate mai degrabă decât un set de opțiuni.</span><span class="sxs-lookup"><span data-stu-id="0202c-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="0202c-124">Menținerea unui set de opțiuni, cum ar fi adăugarea sau eliminarea valorilor, necesită un administrator sau un dezvoltator, în timp ce adăugarea de noi rânduri la un tabel se poate face de către majoritatea utilizatorilor.</span><span class="sxs-lookup"><span data-stu-id="0202c-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="0202c-125">Următorul exemplu arată ratele de facturare care sunt configurate pe baza rolului și unității de resurse organizaționale la care aparține resursa.</span><span class="sxs-lookup"><span data-stu-id="0202c-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="0202c-126">Ratele de cost sunt de obicei bazate pe banda de salariu a angajatului și unitatea de organizație la care aparțin.</span><span class="sxs-lookup"><span data-stu-id="0202c-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="0202c-127">În acest exemplu, rata de facturare și tabelele ratei de cost va arata în felul următor.</span><span class="sxs-lookup"><span data-stu-id="0202c-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="0202c-128">**Exemple de rate de facturare**</span><span class="sxs-lookup"><span data-stu-id="0202c-128">**Sample bill rates**</span></span>

| <span data-ttu-id="0202c-129">Rol</span><span class="sxs-lookup"><span data-stu-id="0202c-129">Role</span></span>        | <span data-ttu-id="0202c-130">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="0202c-130">Org Unit</span></span>    |<span data-ttu-id="0202c-131">Unitate</span><span class="sxs-lookup"><span data-stu-id="0202c-131">Unit</span></span>      |<span data-ttu-id="0202c-132">Preț</span><span class="sxs-lookup"><span data-stu-id="0202c-132">Price</span></span>      |<span data-ttu-id="0202c-133">Monedă</span><span class="sxs-lookup"><span data-stu-id="0202c-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0202c-134">Dezvoltator</span><span class="sxs-lookup"><span data-stu-id="0202c-134">Developer</span></span>   | <span data-ttu-id="0202c-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0202c-135">Contoso US</span></span>  |<span data-ttu-id="0202c-136">Hour</span><span class="sxs-lookup"><span data-stu-id="0202c-136">Hour</span></span> | <span data-ttu-id="0202c-137">200</span><span class="sxs-lookup"><span data-stu-id="0202c-137">200</span></span>|<span data-ttu-id="0202c-138">USD</span><span class="sxs-lookup"><span data-stu-id="0202c-138">USD</span></span>     |
| <span data-ttu-id="0202c-139">Dezvoltator</span><span class="sxs-lookup"><span data-stu-id="0202c-139">Developer</span></span>   | <span data-ttu-id="0202c-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="0202c-140">Contoso India</span></span> |<span data-ttu-id="0202c-141">Hour</span><span class="sxs-lookup"><span data-stu-id="0202c-141">Hour</span></span>|   <span data-ttu-id="0202c-142">112</span><span class="sxs-lookup"><span data-stu-id="0202c-142">112</span></span>|<span data-ttu-id="0202c-143">USD</span><span class="sxs-lookup"><span data-stu-id="0202c-143">USD</span></span>     |


<span data-ttu-id="0202c-144">**Eșantion de rate de cost**</span><span class="sxs-lookup"><span data-stu-id="0202c-144">**Sample cost rates**</span></span>

| <span data-ttu-id="0202c-145">Bandă de salariu</span><span class="sxs-lookup"><span data-stu-id="0202c-145">Salary Band</span></span>     | <span data-ttu-id="0202c-146">Unitate organizațională</span><span class="sxs-lookup"><span data-stu-id="0202c-146">Org Unit</span></span>    |<span data-ttu-id="0202c-147">Unitate</span><span class="sxs-lookup"><span data-stu-id="0202c-147">Unit</span></span>      |<span data-ttu-id="0202c-148">Preț</span><span class="sxs-lookup"><span data-stu-id="0202c-148">Price</span></span>      |<span data-ttu-id="0202c-149">Monedă</span><span class="sxs-lookup"><span data-stu-id="0202c-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0202c-150">company_Band1 a mea</span><span class="sxs-lookup"><span data-stu-id="0202c-150">My company_Band1</span></span> | <span data-ttu-id="0202c-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0202c-151">Contoso US</span></span>  |<span data-ttu-id="0202c-152">Hour</span><span class="sxs-lookup"><span data-stu-id="0202c-152">Hour</span></span> | <span data-ttu-id="0202c-153">145</span><span class="sxs-lookup"><span data-stu-id="0202c-153">145</span></span>|<span data-ttu-id="0202c-154">USD</span><span class="sxs-lookup"><span data-stu-id="0202c-154">USD</span></span>     |
| <span data-ttu-id="0202c-155">company_Band2 a mea</span><span class="sxs-lookup"><span data-stu-id="0202c-155">My company_Band2</span></span> | <span data-ttu-id="0202c-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="0202c-156">Contoso India</span></span> |<span data-ttu-id="0202c-157">Hour</span><span class="sxs-lookup"><span data-stu-id="0202c-157">Hour</span></span>|   <span data-ttu-id="0202c-158">67</span><span class="sxs-lookup"><span data-stu-id="0202c-158">67</span></span>|<span data-ttu-id="0202c-159">USD</span><span class="sxs-lookup"><span data-stu-id="0202c-159">USD</span></span>     |
