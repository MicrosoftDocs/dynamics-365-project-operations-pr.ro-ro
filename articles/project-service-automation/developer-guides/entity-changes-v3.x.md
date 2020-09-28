---
title: Modificări de entitate, control și interfață cu utilizatorul (Project Service Automation 3.x)
description: Acest subiect descrie modificările soluției pentru Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754775"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a><span data-ttu-id="7a0fc-103">Modificări de entitate, control și interfață cu utilizatorul (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-103">Entity, control, and user interface changes (Project Service Automation 3.x)</span></span>
<span data-ttu-id="7a0fc-104">Odată cu lansarea Microsoft Dynamics Project Service Automation (PSA) 3.x, s-au efectuat multe modificări la nivelul entităților, controalelor, vizualizărilor și interfeței cu utilizatorul.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-104">With the release of Microsoft Dynamics Project Service Automation (PSA) 3.x, many changes have been made to the entities, controls, views, and user interface.</span></span> <span data-ttu-id="7a0fc-105">Acest subiect oferă informații despre aceste modificări importante.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-105">This topic provides information about these important changes.</span></span>

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a><span data-ttu-id="7a0fc-106">Relațiile părinte-fiu pentru documentul de vânzări, linia documentului de vânzări, entitățile detalii de linie document de vânzări</span><span class="sxs-lookup"><span data-stu-id="7a0fc-106">Parent-child relationships for sales document, sales document line, sales document line detail entities</span></span>
<span data-ttu-id="7a0fc-107">În versiunile de Dynamics 365 Project Service Automation (PSA) lansate înainte de versiunea 3.0, anumite relații dintre documentele de vânzări, liniile de document de vânzări și entitățile detalii de linie document de vânzări au fost implementate prin câmpuri de șir care ar deține o reprezentare a șirului de GUID a entității afiliate.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-107">In versions of Dynamics 365 Project Service Automation (PSA) released prior to version 3.0, some of the relationships between sales documents, sales document lines, and sales document line detail entities were implemented through string fields that would hold a string representation of GUID of the related entity.</span></span> <span data-ttu-id="7a0fc-108">Acest lucru s-a datorat limitărilor de platformă care necesită cod particularizat semnificativ pe partea server și client a soluției pentru a face aceste relații să funcționeze similar cu relațiile tipice de entitate Dynamics CRM și pentru a face ca aceste câmpuri șir să acționeze sub formă de câmpuri de căutare.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-108">This was due to platform limitations that required significant custom code on the server and client sides of the solution to make those relationships work similar to typical Dynamics CRM entity relationships and to make string fields act like lookup fields.</span></span>

<span data-ttu-id="7a0fc-109">PSA 3.0 a fost actualizat pentru a profita de noile relații între entități între entitățile document de vânzări și de linie de document de vânzări.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-109">PSA 3.0 has been updated to leverage the new entity relationships between sales document and sales document line entities.</span></span>

<span data-ttu-id="7a0fc-110">Întrucât câmpurile de căutare pot fi utilizate acum pentru a indica referințe la entități, câmpurile care au deținut valoarea șir a GUID-ului entității corelate în versiunile anterioare nu mai sunt necesare și, prin urmare, au fost perimate.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-110">Because lookup fields can now be used to indicate references to entities, the fields that held the string value of the GUID of the related entity in previous versions are no longer needed and therefore have been deprecated.</span></span> <span data-ttu-id="7a0fc-111">Codul pe partea server și client particularizat care gestionează relațiile definite de câmpuri șir moștenite este și el perimat.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-111">The custom client and server side code that handles the relationships defined by legacy string fields has also been deprecated.</span></span>

### <a name="entity-schema-changes"></a><span data-ttu-id="7a0fc-112">Modificările schemei de entitate</span><span class="sxs-lookup"><span data-stu-id="7a0fc-112">Entity schema changes</span></span>
<span data-ttu-id="7a0fc-113">Următorul tabel furnizează o listă unu-la-unu a câmpurilor de șir perimate și a noilor câmpuri de căutare pentru entități.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-113">The following table provides a one-to-one list of the deprecated string fields and the new lookup fields for the entities.</span></span> 

 <span data-ttu-id="7a0fc-114">Entitate</span><span class="sxs-lookup"><span data-stu-id="7a0fc-114">Entity</span></span> |   <span data-ttu-id="7a0fc-115">Câmp perimat (șir)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-115">Deprecated field (String)</span></span> | <span data-ttu-id="7a0fc-116">Câmp nou (căutare)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-116">New field (Lookup)</span></span>
--- | --- | ---
<span data-ttu-id="7a0fc-117">invoicedetail (linie factură)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-117">invoicedetail (Invoice Line)</span></span> |  <span data-ttu-id="7a0fc-118">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-118">msdyn_contractline</span></span> |    <span data-ttu-id="7a0fc-119">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-119">msdyn_contractlineid</span></span>
<span data-ttu-id="7a0fc-120">msdyn_actual (Actual)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-120">msdyn_actual (Actual)</span></span> | <span data-ttu-id="7a0fc-121">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-121">msdyn_salescontractline</span></span> |   <span data-ttu-id="7a0fc-122">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-122">msdyn_salescontractlineid</span></span>
<span data-ttu-id="7a0fc-123">msdyn_contractlineinvoiceschedule (Planificare facturi linie contract de proiect)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-123">msdyn_contractlineinvoiceschedule (Project Contract Line Invoice Schedule)</span></span> |    <span data-ttu-id="7a0fc-124">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-124">msdyn_contractline</span></span> |    <span data-ttu-id="7a0fc-125">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-125">msdyn_contractlineid</span></span>
<span data-ttu-id="7a0fc-126">msdyn_contractlinescheduleofvalue (Jalon linie contract de proiect)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-126">msdyn_contractlinescheduleofvalue (Project Contract Line Milestone)</span></span> |   <span data-ttu-id="7a0fc-127">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-127">msdyn_contractline</span></span> |    <span data-ttu-id="7a0fc-128">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-128">msdyn_contractlineid</span></span>
<span data-ttu-id="7a0fc-129">msdyn_fact (fact)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-129">msdyn_fact (Fact)</span></span> | <span data-ttu-id="7a0fc-130">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-130">msdyn_salescontractline</span></span> |   <span data-ttu-id="7a0fc-131">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-131">msdyn_salescontractlineid</span></span>
<span data-ttu-id="7a0fc-132">msdyn_invoicelinetransaction (Detaliu linie factură)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-132">msdyn_invoicelinetransaction (Invoice Line Detail)</span></span> | <span data-ttu-id="7a0fc-133">msdyn_invoiceline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-133">msdyn_invoiceline</span></span> <br> <span data-ttu-id="7a0fc-134">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-134">msdyn_salescontractline</span></span> | <span data-ttu-id="7a0fc-135">msdyn_invoicelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-135">msdyn_invoicelineid</span></span> <br> <span data-ttu-id="7a0fc-136">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-136">msdyn_salescontractlineid</span></span>
<span data-ttu-id="7a0fc-137">msdyn_journalline (linie de jurnal)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-137">msdyn_journalline (Journal Line)</span></span> |  <span data-ttu-id="7a0fc-138">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-138">msdyn_salescontractline</span></span> |   <span data-ttu-id="7a0fc-139">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-139">msdyn_salescontractlineid</span></span>
<span data-ttu-id="7a0fc-140">msdyn_orderlineresourcecategory (Categorie de resurse linie contract de proiect)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-140">msdyn_orderlineresourcecategory (Project Contract Line Resource Category)</span></span> | <span data-ttu-id="7a0fc-141">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-141">msdyn_salescontractline</span></span> |   <span data-ttu-id="7a0fc-142">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-142">msdyn_contractlineid</span></span>
<span data-ttu-id="7a0fc-143">msdyn_orderlinetransaction (Detaliu linie contract pentru proiect)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-143">msdyn_orderlinetransaction (Project Contract Line Detail)</span></span> | <span data-ttu-id="7a0fc-144">msdyn_salescontractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-144">msdyn_salescontractline</span></span> |   <span data-ttu-id="7a0fc-145">msdyn_salescontractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-145">msdyn_salescontractlineid</span></span>
<span data-ttu-id="7a0fc-146">msdyn_orderlinetransactioncategory (Categorie de tranzacții linie contract de proiect)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-146">msdyn_orderlinetransactioncategory (Project Contract Line Transaction Category)</span></span> |   <span data-ttu-id="7a0fc-147">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-147">msdyn_contractline</span></span> |    <span data-ttu-id="7a0fc-148">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-148">msdyn_contractlineid</span></span>
<span data-ttu-id="7a0fc-149">msdyn_orderlinetransactionclassification (Clasificare de tranzacții linie contract de proiect)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-149">msdyn_orderlinetransactionclassification (Project Contract Line Transaction Classification)</span></span> |   <span data-ttu-id="7a0fc-150">msdyn_contractline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-150">msdyn_contractline</span></span> |    <span data-ttu-id="7a0fc-151">msdyn_contractlineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-151">msdyn_contractlineid</span></span>
<span data-ttu-id="7a0fc-152">msdyn_quotelineinvoiceschedule (Planificare factură linie de ofertă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-152">msdyn_quotelineinvoiceschedule (Quote Line Invoice Schedule)</span></span> |  <span data-ttu-id="7a0fc-153">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-153">msdyn_quoteline</span></span> |   <span data-ttu-id="7a0fc-154">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-154">msdyn_quotelineid</span></span>
<span data-ttu-id="7a0fc-155">msdyn_quotelineresourcecategory (Categorie de resurse linie de ofertă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-155">msdyn_quotelineresourcecategory (Quote Line Resource Category)</span></span> |    <span data-ttu-id="7a0fc-156">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-156">msdyn_quoteline</span></span> |   <span data-ttu-id="7a0fc-157">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-157">msdyn_quotelineid</span></span>
<span data-ttu-id="7a0fc-158">msdyn_quotelinescheduleofvalue (Jalon linie de ofertă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-158">msdyn_quotelinescheduleofvalue (Quote Line Milestone)</span></span> | <span data-ttu-id="7a0fc-159">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-159">msdyn_quoteline</span></span> |   <span data-ttu-id="7a0fc-160">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-160">msdyn_quotelineid</span></span>
<span data-ttu-id="7a0fc-161">msdyn_quotelinetransaction (Detaliu linie de ofertă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-161">msdyn_quotelinetransaction (Quote Line Detail)</span></span> |    <span data-ttu-id="7a0fc-162">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-162">msdyn_quoteline</span></span> |   <span data-ttu-id="7a0fc-163">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-163">msdyn_quotelineid</span></span>
<span data-ttu-id="7a0fc-164">msdyn_quotelinetransactioncategory (Categorie de tranzacții linie de ofertă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-164">msdyn_quotelinetransactioncategory (Quote Line Transaction Category)</span></span> |  <span data-ttu-id="7a0fc-165">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-165">msdyn_quoteline</span></span> |   <span data-ttu-id="7a0fc-166">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-166">msdyn_quotelineid</span></span>
<span data-ttu-id="7a0fc-167">msdyn_quotelinetransactionclassification (Clasificare de tranzacții linie de ofertă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-167">msdyn_quotelinetransactionclassification (Quote Line Transaction Classification)</span></span> |  <span data-ttu-id="7a0fc-168">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-168">msdyn_quoteline</span></span> |   <span data-ttu-id="7a0fc-169">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-169">msdyn_quotelineid</span></span>
<span data-ttu-id="7a0fc-170">SalesOrderDetail (Linie de comandă)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-170">SalesOrderDetail (Order Line)</span></span> | <span data-ttu-id="7a0fc-171">msdyn_quotelineid</span><span class="sxs-lookup"><span data-stu-id="7a0fc-171">msdyn_quotelineid</span></span> | <span data-ttu-id="7a0fc-172">msdyn_quoteline</span><span class="sxs-lookup"><span data-stu-id="7a0fc-172">msdyn_quoteline</span></span> 

### <a name="deprecated-custom-views-and-controls"></a><span data-ttu-id="7a0fc-173">Vizualizări și controale particularizate perimate</span><span class="sxs-lookup"><span data-stu-id="7a0fc-173">Deprecated custom views and controls</span></span>
<span data-ttu-id="7a0fc-174">Următoarele vizualizări și controale particularizate și artefactele lor corelate au fost perimate.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-174">The following custom views and controls, and their related artifacts, have been deprecated.</span></span>

- <span data-ttu-id="7a0fc-175">Vizualizare posibilitate de tarifare.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-175">Chargeability view.</span></span>
- <span data-ttu-id="7a0fc-176">Controalele grilă particularizate pentru afișarea detaliilor liniei de ofertă în pagina **Informații proiect** pentru linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-176">Custom grid controls for showing quote line details on the **Project Information** page for the quote line.</span></span>
- <span data-ttu-id="7a0fc-177">Controale grilă particularizate pentru afișarea detaliilor liniei de contract de proiect pe pagina **Informații proiect** pentru linia comenzii de vânzare.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-177">Custom grid controls for showing project contract line details on the **Project Information** page for the sales order line.</span></span>

> [!NOTE]
> <span data-ttu-id="7a0fc-178">Pentru lista completă a resurselor perimate, consultați [Resurse web perimate în Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-178">For the full list of deprecated resources, see [Deprecated Web resources in Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)</span></span>

## <a name="unified-client-interface-app-module"></a><span data-ttu-id="7a0fc-179">Modul de aplicație Unified Client Interface</span><span class="sxs-lookup"><span data-stu-id="7a0fc-179">Unified Client Interface App Module</span></span>
<span data-ttu-id="7a0fc-180">Odată cu introducerea de modulelor de aplicație Unified Client Interface (UCI), intrările de hartă de site PSA au fost eliminate din sistem.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-180">With the introduction of Unified Client Interface (UCI) App Modules, the PSA site map entries have been removed from the system.</span></span>  
<span data-ttu-id="7a0fc-181">Funcționalitatea legată de comutarea formularului pentru Oportunitate, Ofertă, Comandă, Factură a fost perimată întrucât nu mai este necesară deoarece modulul de aplicație UCI include numai versiunile PSA ale formularelor.</span><span class="sxs-lookup"><span data-stu-id="7a0fc-181">Functionality related to form switching for Opportunity, Quote, Order, Invoice has been deprecated as it is no longer required because the UCI App Module includes only PSA versions of the forms.</span></span>  

<span data-ttu-id="7a0fc-182">Următoarele resurse web au fost perimate:</span><span class="sxs-lookup"><span data-stu-id="7a0fc-182">The following web resources have been deprecated:</span></span>

- <span data-ttu-id="7a0fc-183">msdyn_\SalesDocument\SalesDocumentFormLoader.js</span><span class="sxs-lookup"><span data-stu-id="7a0fc-183">msdyn_\SalesDocument\SalesDocumentFormLoader.js</span></span>
- <span data-ttu-id="7a0fc-184">msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js</span><span class="sxs-lookup"><span data-stu-id="7a0fc-184">msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js</span></span>

> [!NOTE]
> <span data-ttu-id="7a0fc-185">Pentru lista completă a resurselor perimate, consultați [Resurse web învechite în Project Service Automation v3.x.](../developer-guides/web-resources-deprecated-v3.x.md)</span><span class="sxs-lookup"><span data-stu-id="7a0fc-185">For the full list of deprecated resources, see [Deprecated Web resources in Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).</span></span>

