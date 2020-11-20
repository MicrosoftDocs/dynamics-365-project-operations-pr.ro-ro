---
title: Valori implicite pentru dimensiunile financiare
description: Acest subiect oferă informații despre cum să configurați valorile implicite ale dimensiunii financiare.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131898"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="6a8f7-103">Valori implicite pentru dimensiunile financiare</span><span class="sxs-lookup"><span data-stu-id="6a8f7-103">Financial dimension defaults</span></span>

<span data-ttu-id="6a8f7-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="6a8f7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6a8f7-105">Dynamics 365 Project Operations utilizează [Dimensiuni financiare](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) cadru în Dynamics 365 Finance pentru a oferi informații suplimentare cu privire la tranzacțiile cu contabilitate de proiect și contabilitate generală.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="6a8f7-106">Dimensiunile financiare implicite pot fi stabilite pentru un client, o sursă de finanțare a proiectului, o etapă importantă, o linie de contract de proiect sau un proiect.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="6a8f7-107">Definiți dimensiunile financiare implicite pentru un client</span><span class="sxs-lookup"><span data-stu-id="6a8f7-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="6a8f7-108">Valorile implicite ale dimensiunii clienților sunt specificate în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="6a8f7-109">Completați următorii pași pentru a seta valorile implicite ale dimensiunii.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="6a8f7-110">Accesați **Conturi clienți** > **Clienți** > **Toți clienții**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="6a8f7-111">Pe pagina **Clienți**, pe fila **Dimensiuni financiare**, setați valorile dimensiunii financiare pentru un anumit client.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="6a8f7-112">Definiți dimensiunile financiare implicite pentru contracte de proiect</span><span class="sxs-lookup"><span data-stu-id="6a8f7-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="6a8f7-113">Contractele de proiect sunt create și menținute în Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="6a8f7-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="6a8f7-114">Atributele contabile pentru contractele de proiect sunt stabilite în module **Management de proiect și contabilitate** în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="6a8f7-115">Stabiliți dimensiunile financiare pentru o sursă de finanțare a proiectului</span><span class="sxs-lookup"><span data-stu-id="6a8f7-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="6a8f7-116">Accesați **Gestionarea proiectului și contabilitate** > **Proiecte** > **Contracte de proiect**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="6a8f7-117">Selectați înregistrarea pe care doriți să o actualizați și pe fila **Contract de proiect**, selectați **Afișați contabilitatea implicită**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="6a8f7-118">Extindeți **Informații conexe** și selectați fila **Surse de finanțare**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="6a8f7-119">Setați valorile implicite ale dimensiunii financiare.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="6a8f7-120">Observați că dimensiunile financiare sunt implicite din contul clientului.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="6a8f7-121">Stabiliți dimensiunile financiare pentru o linie de contract de proiect</span><span class="sxs-lookup"><span data-stu-id="6a8f7-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="6a8f7-122">Accesați **Gestionarea proiectului și contabilitate** > **Proiecte** > **Contracte de proiect**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="6a8f7-123">Selectați înregistrarea pe care doriți să o actualizați și pe fila **Contract de proiect**, selectați **Afișați contabilitatea implicită**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="6a8f7-124">Extindeți **Informații conexe** și selectați fila **Linii de contract**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="6a8f7-125">Setați valorile implicite ale dimensiunii financiare.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="6a8f7-126">Valorile implicite ale dimensiunii financiare sunt aplicabile și pot fi utilizate numai cu liniile contractuale cu preț fix (etapă de referință).</span><span class="sxs-lookup"><span data-stu-id="6a8f7-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="6a8f7-127">Aceste valori implicite sunt utilizate pentru tranzacțiile aferente proiectului și liniile de facturare aferente.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="6a8f7-128">Definiți dimensiunile financiare implicite pentru proiecte</span><span class="sxs-lookup"><span data-stu-id="6a8f7-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="6a8f7-129">Proiectele sunt create și menținute în CDS.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="6a8f7-130">Atributele contabile pentru proiectele sunt stabilite în module **Management de proiect și contabilitate** în Finanțe.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="6a8f7-131">Accesați **Managementul proiectelor și contabilitate** > **Proiecte** > **Toate proiectele**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="6a8f7-132">Selectați înregistrarea pe care doriți să o actualizați și pe fila **Proiect**, selectați **Afișați contabilitatea implicită**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="6a8f7-133">Extindeți **Informații conexe** și selectați fila **Configurare**.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="6a8f7-134">Setați valorile implicite ale dimensiunii financiare.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="6a8f7-135">Observați că dimensiunile financiare sunt implicite din contul clientului.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="6a8f7-136">În cazul în care proiectul este asociat cu o linie contractuală cu mai mulți clienți contractuali ai proiectului, clientul principal este utilizat la dimensiunile financiare implicite.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="6a8f7-137">Dimensiunile financiare implicite ale proiectului sunt utilizate pentru a seta valorile implicite ale liniei jurnalului pentru tranzacțiile de timp, cheltuială și taxă din **Jurnal de integrare a operațiunilor de proiect** și pe liniile de facturare aferente proiectului.</span><span class="sxs-lookup"><span data-stu-id="6a8f7-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
