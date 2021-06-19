---
title: Planificarea de cheltuieli al anchetei Federal Awards
description: Acest subiect oferă informații despre ancheta privind planificarea de cheltuieli al Federal Awards.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010081"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d8b0b-103">Planificarea de cheltuieli al anchetei Federal Awards</span><span class="sxs-lookup"><span data-stu-id="d8b0b-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8b0b-104">Potrivit Circularei Biroului de Management și Buget A-133, agențiile care primesc fonduri federale sunt supuse cerințelor de audit, care sunt, de asemenea, cunoscute sub numele de audituri unice.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="d8b0b-105">Procesul de audit este utilizat pentru raportarea recurentă a veniturilor și cheltuielilor subvențiilor federale.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="d8b0b-106">O parte a raportului de audit unic include planificarea de cheltuieli al Federal Awards (SEFA).</span><span class="sxs-lookup"><span data-stu-id="d8b0b-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="d8b0b-107">Ancheta privind cheltuielile pentru Federal Awards include titlul și numărul Catalogului de asistență internă federală (CFDA), numărul grantului, anul acordării grantului, numele agenției federale care furnizează fondurile și numele permisului prin entitate.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="d8b0b-108">Ancheta este pentru o anumită perioadă.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="d8b0b-109">De obicei, acea perioadă este aceeași cu perioada situației financiare, care este un exercițiu financiar.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="d8b0b-110">Ancheta include subvenții care au date de proiecție în intervalul de date selectat.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="d8b0b-111">Coloana **Agenția de finanțare** a anchetei arată clientul subvenționat sau, pentru o subvenție de trecere, agenția care acordă grantul.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="d8b0b-112">Pentru o subvenție de trecere, coloana **Agenție de trecere** arată clientul de grant.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="d8b0b-113">Dacă grantul nu este un grant de trecere, coloana **Agenție de trecere** este necompletată.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="d8b0b-114">Configurați clusterele CFDA</span><span class="sxs-lookup"><span data-stu-id="d8b0b-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="d8b0b-115">Trebuie să configurați clusterele CFDA care pot fi asociate cu numerele CFDA în ancheta privind planificarea de cheltuieli a Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d8b0b-116">Accesați **Management de proiect și contabilitate \> Configurare \> granturi \> Catalogul grupurilor federale de asistență internă**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="d8b0b-117">Selectați **Nou** pentru a crea un cluster CFDA.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="d8b0b-118">Introduceți numele clusterului.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="d8b0b-119">Selectați **Salvare** pentru a vă salva modificările.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="d8b0b-120">Configurați numerele CFDA</span><span class="sxs-lookup"><span data-stu-id="d8b0b-120">Set up CFDA numbers</span></span>

<span data-ttu-id="d8b0b-121">Trebuie să configurați numerele CFDA care pot fi adăugate granturile și incluse în ancheta de planificare a cheltuielilor a Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="d8b0b-122">Accesați **Management de proiect și contabilitate \> Configurare \> granturi \> Catalogul numerelor federale de asistență internă**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="d8b0b-123">Selectați **Nou** pentru a crea un număr CFDA.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="d8b0b-124">În coloana **Număr**, introduceți numărul CFDA.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="d8b0b-125">Apăsați tasta **Tab**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="d8b0b-126">În coloana **Descriere**, introduceți titlu CFDA.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="d8b0b-127">Apăsați tasta **Tab**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="d8b0b-128">Opțional: în câmpul **Cluster de program**, adăugați clusterul CFDA corespunzător.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="d8b0b-129">Selectați **Salvare** pentru a vă salva modificările.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d8b0b-130">Configurați granturi pentru a raporta pentru ancheta privind planificarea de cheltuieli al Federal Awards</span><span class="sxs-lookup"><span data-stu-id="d8b0b-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d8b0b-131">Accesați **Management de proiect și contabilitate \> granturi \> granturi** și selectați o subvenție existentă.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="d8b0b-132">Pe FilaRapidă **Configurare**, în câmpul **Catalogul asistenței interne federale**, atribuiți numărul CFDA.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="d8b0b-133">Numărul CFDA al grantului determină clusterul CFDA pentru raportare.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="d8b0b-134">Pe FastTab **Informații de contact**, introduceți informațiile despre concedent urmând acești pași:</span><span class="sxs-lookup"><span data-stu-id="d8b0b-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="d8b0b-135">În câmpul **Client de grant**, introduceți clientul care este responsabil pentru grant.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="d8b0b-136">Pentru un grant existent, aceste informații ar putea fi deja introduse.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="d8b0b-137">Indicați dacă clientul grantului este finanțatorul.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="d8b0b-138">Dacă clientul de grant este finanțatorul, lăsați caseta de selectare **Trecere** liberă.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="d8b0b-139">Dacă un alt client este finanțatorul, iar clientul de subvenție este responsabil pentru cheltuirea și urmărirea banilor, selectați caseta de bifare **Trecere**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="d8b0b-140">Dacă ați selectat caseta de bifare **Trecere** din pasul anterior, în câmpul **Agenția de finanțare**, introduceți clientul care a furnizat grantul.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="d8b0b-141">Agenția care acordă grantul și clientul care acordă grantul nu pot fi același client.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="d8b0b-142">Iată un exemplu de subvenție de trecere:</span><span class="sxs-lookup"><span data-stu-id="d8b0b-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="d8b0b-143">Guvernul federal a finanțat un proiect de infrastructură pentru un stat.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="d8b0b-144">Guvernul federal a dat banii statului pentru a-i cheltui.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="d8b0b-145">În acest caz, guvernul federal este agenția care acordă, iar statul este clientul care acordă grantul.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="d8b0b-146">Când porniți prima dată funcția, numerele inițiale CFDA vor fi introduse utilizând numerele existente pe subvenții.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="d8b0b-147">Excludeți subvențiile din raportarea SEFA pe baza tipului de subvenție</span><span class="sxs-lookup"><span data-stu-id="d8b0b-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="d8b0b-148">Accesați **Gestionarea proiectului și contabilitate \> Configurare \> Granturi \> Tipuri de granturi**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="d8b0b-149">Pe FilaRapidă **Informații implicite**, selectați caseta de bifat **Excludeți din planificarea de cheltuieli Granturile federale**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="d8b0b-150">Selectați **Salvare** pentru a vă salva modificările.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="d8b0b-151">Rulați Planificarea de cheltuieli al anchetei Federal Awards</span><span class="sxs-lookup"><span data-stu-id="d8b0b-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="d8b0b-152">Accesați **Management de proiect și contabilitate \> Cereri și rapoarte \> Anchetă de grant \> Planificarea de cheltuieli al premiilor federale**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="d8b0b-153">În secțiunea **Parametri**, urmați acești pași:</span><span class="sxs-lookup"><span data-stu-id="d8b0b-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="d8b0b-154">În câmpul **Interval de date**, selectați codul pentru intervalul de date.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="d8b0b-155">Alternativ, în câmpurile **Data de la** și **La data**, definiți intervalul de date.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="d8b0b-156">Opțional: pentru a include numai tranzacții facturate ca venituri în anchetă, setați **Includeți numai veniturile facturate** opțiune pentru **Da**.</span><span class="sxs-lookup"><span data-stu-id="d8b0b-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="d8b0b-157">Coloane</span><span class="sxs-lookup"><span data-stu-id="d8b0b-157">Columns</span></span>

<span data-ttu-id="d8b0b-158">Ancheta privind planificarea cheltuielilor pentru Federal Awards include următoarele coloane:</span><span class="sxs-lookup"><span data-stu-id="d8b0b-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="d8b0b-159">Catalogul denumirii clusterului de asistență internă federală</span><span class="sxs-lookup"><span data-stu-id="d8b0b-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="d8b0b-160">Agenția de finanțare</span><span class="sxs-lookup"><span data-stu-id="d8b0b-160">Grantor agency</span></span>
- <span data-ttu-id="d8b0b-161">Agenție de trecere</span><span class="sxs-lookup"><span data-stu-id="d8b0b-161">Pass-through agency</span></span>
- <span data-ttu-id="d8b0b-162">Numele grantului</span><span class="sxs-lookup"><span data-stu-id="d8b0b-162">Grant name</span></span>
- <span data-ttu-id="d8b0b-163">ID-ul grantului</span><span class="sxs-lookup"><span data-stu-id="d8b0b-163">Grant ID</span></span>
- <span data-ttu-id="d8b0b-164">ID-ul aplicației de grant</span><span class="sxs-lookup"><span data-stu-id="d8b0b-164">Grant application ID</span></span>
- <span data-ttu-id="d8b0b-165">Catalogul asistenței interne federale</span><span class="sxs-lookup"><span data-stu-id="d8b0b-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="d8b0b-166">Chitanțe</span><span class="sxs-lookup"><span data-stu-id="d8b0b-166">Receipts</span></span>
- <span data-ttu-id="d8b0b-167">Cheltuieli</span><span class="sxs-lookup"><span data-stu-id="d8b0b-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]