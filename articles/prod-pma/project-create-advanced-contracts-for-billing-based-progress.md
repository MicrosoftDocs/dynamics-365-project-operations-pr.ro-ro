---
title: Crearea de contracte avansate pentru facturare pe baza progresului
description: Acest subiect explică modul de creare a contractelor de proiect, astfel încât să puteți genera facturi pentru clienți, pe baza unui procent din lucrările finalizate.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289519"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="c01c0-103">Crearea de contracte avansate pentru facturare pe baza progresului</span><span class="sxs-lookup"><span data-stu-id="c01c0-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c01c0-104">Acest subiect explică modul de creare a contractelor de proiect, astfel încât să puteți crea facturi pentru clienți, pe baza unui procent din lucrările finalizate.</span><span class="sxs-lookup"><span data-stu-id="c01c0-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="c01c0-105">Sumele facturii sunt calculate automat pentru categoriile bugetare de lucru pe care le-ați configurat pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="c01c0-106">Momentul facturii este stabilit atunci când negociați contractul de proiect cu clientul.</span><span class="sxs-lookup"><span data-stu-id="c01c0-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="c01c0-107">Utilizați procedurile din acest subiect pentru a configura un contract, un proiect asociat și regulile de facturare care calculează sumele facturii pentru categoriile de lucrări bugetare pe care le-ați configurat pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="c01c0-108">După ce ați creat contractul și proiectul, puteți configura detaliile proiectului.</span><span class="sxs-lookup"><span data-stu-id="c01c0-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="c01c0-109">De exemplu, puteți defini activități și atribui lucrători la proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="c01c0-110">Exemplu</span><span class="sxs-lookup"><span data-stu-id="c01c0-110">Example</span></span>

<span data-ttu-id="c01c0-111">Organizația dvs. este o firmă de dezvoltare software.</span><span class="sxs-lookup"><span data-stu-id="c01c0-111">Your organization is a software development firm.</span></span> <span data-ttu-id="c01c0-112">Sunteți de acord să dezvoltați un pachet de contabilitate a salariilor pentru un client pentru o taxă totală de 20.000 de dolari SUA (USD).</span><span class="sxs-lookup"><span data-stu-id="c01c0-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="c01c0-113">Organizația dvs. este de acord să factureze clientul pe măsură ce completați procente specifice din proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="c01c0-114">Configurați următoarele categorii de proiecte pentru lucrare, astfel încât să le puteți utiliza în procesul de facturare:</span><span class="sxs-lookup"><span data-stu-id="c01c0-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="c01c0-115">Consultanță</span><span class="sxs-lookup"><span data-stu-id="c01c0-115">Consulting</span></span>
- <span data-ttu-id="c01c0-116">Proiect</span><span class="sxs-lookup"><span data-stu-id="c01c0-116">Design</span></span>
- <span data-ttu-id="c01c0-117">Instalare</span><span class="sxs-lookup"><span data-stu-id="c01c0-117">Installation</span></span>

<span data-ttu-id="c01c0-118">Puteți, de asemena, să configurați reguli de facturare care calculează automat sumele facturii pentru procentul de muncă de proiect finalizat în fiecare categorie.</span><span class="sxs-lookup"><span data-stu-id="c01c0-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="c01c0-119">Managerul bugetului creează un buget pentru categoriile de proiecte.</span><span class="sxs-lookup"><span data-stu-id="c01c0-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="c01c0-120">Cantitatea lucrărilor finalizate este calculată automat ca procent din munca efectivă în comparație cu sumele bugetate.</span><span class="sxs-lookup"><span data-stu-id="c01c0-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c01c0-121">Cerințe preliminare</span><span class="sxs-lookup"><span data-stu-id="c01c0-121">Prerequisites</span></span>

<span data-ttu-id="c01c0-122">Înainte de a crea un proiect care utilizează reguli de facturare, trebuie să configurați secvențele numerice pentru regulile de facturare și un jurnal de taxe care este utilizat pentru a înregistra facturări de progres.</span><span class="sxs-lookup"><span data-stu-id="c01c0-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="c01c0-123">Accesați **Gestionarea proiectelor și contabilitate** \> **Configurare** \> **Gestionarea proiectelor și parametrii contabili**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="c01c0-124">Pe pagina **Managementul proiectului și parametrii contabili**, pe fila **Secvențe numerice**, configurați secvența numerică pe care doriți să o utilizați atunci când sunt create regulile de facturare.</span><span class="sxs-lookup"><span data-stu-id="c01c0-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="c01c0-125">Accesați **Gestionarea proiectului și contabilitate** \> **Jurnale** \> **Taxă**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="c01c0-126">Pe pagina **Jurnal cu taxe**, selectați **Nou** și introduceți numele jurnalului.</span><span class="sxs-lookup"><span data-stu-id="c01c0-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="c01c0-127">Creați un contract pentru facturarea progresivă</span><span class="sxs-lookup"><span data-stu-id="c01c0-127">Create a contract for progress billings</span></span>

<span data-ttu-id="c01c0-128">Folosiți această procedură pentru a crea un contract de proiect pentru un proiect cu preț fix.</span><span class="sxs-lookup"><span data-stu-id="c01c0-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="c01c0-129">Creați o factură de proiect atunci când lucrările finalizate la proiect ating un procent specificat.</span><span class="sxs-lookup"><span data-stu-id="c01c0-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="c01c0-130">Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Contracte de proiect**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="c01c0-131">Pe pagina **Contracte de proiect**, selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="c01c0-132">În caseta de dialog **Noul contract de proiect**, setați următoarele câmpuri:</span><span class="sxs-lookup"><span data-stu-id="c01c0-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="c01c0-133">**Nume**</span><span class="sxs-lookup"><span data-stu-id="c01c0-133">**Name**</span></span>
    - <span data-ttu-id="c01c0-134">**Tip de finanțare**</span><span class="sxs-lookup"><span data-stu-id="c01c0-134">**Funding type**</span></span>
    - <span data-ttu-id="c01c0-135">**Sursă de finanțare**</span><span class="sxs-lookup"><span data-stu-id="c01c0-135">**Funding source**</span></span>
    - <span data-ttu-id="c01c0-136">**Moneda de vânzare** - În mod implicit, această monedă este utilizată pentru facturile clienților care sunt asociate cu contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="c01c0-137">Cu toate acestea, puteți modifica moneda de vânzare pe o anumită factură de client.</span><span class="sxs-lookup"><span data-stu-id="c01c0-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="c01c0-138">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-138">Select **OK**.</span></span> <span data-ttu-id="c01c0-139">Informațiile sunt copiate în antetul paginii **Contracte de proiect**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="c01c0-140">Pe pagina **Contracte de proiect**, completați restul informațiilor necesare pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="c01c0-141">Creați un proiect pentru facturarea progresivă</span><span class="sxs-lookup"><span data-stu-id="c01c0-141">Create a project for progress billings</span></span>

<span data-ttu-id="c01c0-142">Urmați acești pași pentru a crea un proiect și orice subproiecte care sunt asociate cu un contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="c01c0-143">Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Toate proiectele**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="c01c0-144">Pe pagina **Toate proiectele**, selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="c01c0-145">În caseta de dialog **Proiect nou**, în câmpul **Tipul proiectului**, selectați **Timp și material**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="c01c0-146">Selectați un grup de proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-146">Select a project group.</span></span> <span data-ttu-id="c01c0-147">Un grup de proiect definește informațiile de înregistrare pentru proiectele care sunt atribuite grupului.</span><span class="sxs-lookup"><span data-stu-id="c01c0-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="c01c0-148">Selectați **Creați un proiect**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-148">Select **Create project**.</span></span>
6. <span data-ttu-id="c01c0-149">După crearea proiectului, setați etapa proiectului la **În proces**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="c01c0-150">Creați un buget pentru un proiect</span><span class="sxs-lookup"><span data-stu-id="c01c0-150">Create a budget for a project</span></span>

<span data-ttu-id="c01c0-151">Categoriile de buget sunt utilizate pentru a calcula automat sumele de facturi pentru procentul de muncă finalizat pentru fiecare categorie.</span><span class="sxs-lookup"><span data-stu-id="c01c0-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="c01c0-152">Urmați acești pași pentru a crea categorii de buget pentru costurile estimate.</span><span class="sxs-lookup"><span data-stu-id="c01c0-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="c01c0-153">Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Toate proiectele**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="c01c0-154">Pe pagina **Toate proiectele**, selectați și deschideți proiectul dorit.</span><span class="sxs-lookup"><span data-stu-id="c01c0-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="c01c0-155">Pe pagina **Proiecte**, pe panoul de acțiune, pe fila **Plan**, în grupul **Buget**, selectați **Bugetul proiectului**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="c01c0-156">Pe pagina **Bugetul proiectului**, introduceți un cost estimat pentru fiecare categorie din proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="c01c0-157">Creați reguli de facturare pentru facturarea progresivă</span><span class="sxs-lookup"><span data-stu-id="c01c0-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="c01c0-158">Accesați **Gestionarea proiectului și contabilitate** \> **Proiecte** \> **Contracte de proiect**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="c01c0-159">Pe pagina **Contracte de proiect**, selectați și deschideți un contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="c01c0-160">Pe pagina contractului de proiect, pe FastTab **Regulile de facturare**, selectați **Adăugare**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="c01c0-161">Pe pagina **Regula de facturare**, în câmpul **Tip de linie**, selectați **Progres**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="c01c0-162">Pe FastTab **Detalii despre linia regulii de facturare**, în **Valoarea contractului**, introduceți valoarea totală a contractului.</span><span class="sxs-lookup"><span data-stu-id="c01c0-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="c01c0-163">În câmpul **Categorie**, selectați categoria în care să înregistrați tranzacția cu taxă.</span><span class="sxs-lookup"><span data-stu-id="c01c0-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="c01c0-164">În câmpul **Proiect**, selectați proiectul care utilizează această regulă de facturare.</span><span class="sxs-lookup"><span data-stu-id="c01c0-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="c01c0-165">Opțional: atribuiți regula de facturare proiectelor suplimentare.</span><span class="sxs-lookup"><span data-stu-id="c01c0-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="c01c0-166">Pe FastTab **Proiect**, în secțiunea **Proiecte disponibile**, selectați un proiect, apoi selectați butonul săgeată dreapta pentru a adăuga proiectul la secțiunea **Proiecte selectate**.</span><span class="sxs-lookup"><span data-stu-id="c01c0-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="c01c0-167">Opțional: calculați suma procentuală pe care clientul o reține din plăți pe o factură.</span><span class="sxs-lookup"><span data-stu-id="c01c0-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="c01c0-168">Pe FastTab **Condiții de plată a retenției**, selectați sursa de finanțare și apoi, în câmpul **Procentul de retenție**, introduceți procentul de retenție.</span><span class="sxs-lookup"><span data-stu-id="c01c0-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="c01c0-169">Repetați acești pași pentru a crea reguli de facturare suplimentare pentru contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="c01c0-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]