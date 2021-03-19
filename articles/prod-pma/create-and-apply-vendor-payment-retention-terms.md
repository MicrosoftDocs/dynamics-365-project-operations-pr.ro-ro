---
title: Crearea și aplicarea condițiilor de reținere a plăților către furnizor
description: Acest subiect oferă informații despre cum să configurați și să mențineți termenii de retenție pentru plățile furnizorilor.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270963"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="a483e-103">Crearea și aplicarea condițiilor de reținere a plăților către furnizor</span><span class="sxs-lookup"><span data-stu-id="a483e-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="a483e-104">Configurarea condițiilor de păstrare a plăților pentru furnizori pentru un proiect este utilă atunci când organizația dvs. dorește să rețină o parte din plățile efectuate către un furnizor.</span><span class="sxs-lookup"><span data-stu-id="a483e-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="a483e-105">De exemplu, atunci când doriți să rețineți plata către un furnizor până când produsele livrate îndeplinesc așteptările dvs.</span><span class="sxs-lookup"><span data-stu-id="a483e-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="a483e-106">Condițiile de păstrare a plăților furnizorului pot fi specificate atunci când negociați un contract de furnizor.</span><span class="sxs-lookup"><span data-stu-id="a483e-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="a483e-107">Crearea condițiilor de reținere a plăților către furnizor</span><span class="sxs-lookup"><span data-stu-id="a483e-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="a483e-108">Puteți introduce procentul plății furnizorului pentru păstrare și procentul sumelor reținute anterior care urmează să fie eliberate.</span><span class="sxs-lookup"><span data-stu-id="a483e-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="a483e-109">Sumele sunt reținute automat pe facturile furnizorului până când contractul atinge starea de finalizare specificată.</span><span class="sxs-lookup"><span data-stu-id="a483e-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="a483e-110">După ce configurați termenii de reținere, îi puteți aplica oricărui proiect pentru acel furnizor.</span><span class="sxs-lookup"><span data-stu-id="a483e-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="a483e-111">Urmați pașii următori pentru a configura și a menține termenii de reținere pentru plățile furnizorilor.</span><span class="sxs-lookup"><span data-stu-id="a483e-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="a483e-112">Accesați **Management de proiect și contabilitate** > **Retenție** > **Condiții de reținere a plăților către furnizor**.</span><span class="sxs-lookup"><span data-stu-id="a483e-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="a483e-113">Selectați **Nou** pentru a adăuga un nou termen de reținere a furnizorului.</span><span class="sxs-lookup"><span data-stu-id="a483e-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="a483e-114">Valoarea **ID-ul regulii** pentru noul termen este introdusă automat.</span><span class="sxs-lookup"><span data-stu-id="a483e-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="a483e-115">Introduceți o scurtă descriere în câmpul **Descriere** și pe **Termeni** al FastTab, selectați **Adăugați linie** pentru a introduce valori de termen pentru următoarele:</span><span class="sxs-lookup"><span data-stu-id="a483e-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="a483e-116">**Procentul de unități livrate**: Introduceți un procent de finalizare pentru termen.</span><span class="sxs-lookup"><span data-stu-id="a483e-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="a483e-117">Sumele sunt reținute automat pe facturile furnizorului până când etapa de finalizare a proiectului este egală cu procentul specificat.</span><span class="sxs-lookup"><span data-stu-id="a483e-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="a483e-118">De exemplu, dacă introduceți 50,00, sumele sunt reținute până când proiectul este finalizat cu 50%.</span><span class="sxs-lookup"><span data-stu-id="a483e-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="a483e-119">**Procent de păstrat**: Introduceți un procent din suma facturii furnizorului care urmează să fie reținută.</span><span class="sxs-lookup"><span data-stu-id="a483e-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="a483e-120">De exemplu, dacă introduceți 10,00, atunci 10 la sută din suma pe o factură de furnizor este reținută până când proiectul atinge procentul de finalizare stabilit în **Câmpul procentului de unități livrate**.</span><span class="sxs-lookup"><span data-stu-id="a483e-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="a483e-121">**Procent de eliberat**: Selectați **Adăugați linie** pentru a introduce un procent din sumele reținute anterior care urmează să fie eliberate pentru nivelul selectat de finalizare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="a483e-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="a483e-122">Dacă aveți mai mult de o etapă pentru niveluri diferite de finalizare a proiectului, introduceți o linie separată de termen de retenție pentru furnizor pentru fiecare regulă de retenție.</span><span class="sxs-lookup"><span data-stu-id="a483e-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="a483e-123">Fiecare linie poate specifica un procent de retenție diferit și un procent de eliberare diferit pentru fiecare nivel desemnat de finalizare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="a483e-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="a483e-124">După ce creați termeni de retenție a furnizorului pentru un furnizor, puteți aplica termenii unui proiect.</span><span class="sxs-lookup"><span data-stu-id="a483e-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="a483e-125">Aplicați condițiile de retenție ale furnizorilor unui proiect</span><span class="sxs-lookup"><span data-stu-id="a483e-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="a483e-126">Accesați **Management de proiect și contabilitate** > **Proiecte** > **Toate proiectele** și deschideți un proiect din pagina listei de proiecte.</span><span class="sxs-lookup"><span data-stu-id="a483e-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="a483e-127">Pe **Acorduri de vânzător** FastTab, selectați **Adăugați linie**.</span><span class="sxs-lookup"><span data-stu-id="a483e-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="a483e-128">În **Câmpul codului contului**, selectați una dintre următoarele opțiuni:</span><span class="sxs-lookup"><span data-stu-id="a483e-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="a483e-129">**Tabel**: Termenii de retenție a furnizorilor se aplică unui singur furnizor.</span><span class="sxs-lookup"><span data-stu-id="a483e-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="a483e-130">**Grup**: Termenii de retenție a furnizorilor se aplică tuturor furnizorilor dintr-un grup de furnizori.</span><span class="sxs-lookup"><span data-stu-id="a483e-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="a483e-131">**Toți**: Condiții de retenție a furnizorilor se aplică tuturor furnizorilor.</span><span class="sxs-lookup"><span data-stu-id="a483e-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="a483e-132">În **Câmpul Furnizor/Grupul de furnizori**, selectați furnizorul sau grupul de furnizori cărora li se aplică condițiile de retenție a furnizorilor.</span><span class="sxs-lookup"><span data-stu-id="a483e-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="a483e-133">Dacă ați selectat **Toți** în pasul anterior, acest câmp nu este disponibil.</span><span class="sxs-lookup"><span data-stu-id="a483e-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="a483e-134">În câmpul **Condiții de retenție a furnizorilor**, selectați termenii de retenție pe care i-ați creat în procedura anterioară.</span><span class="sxs-lookup"><span data-stu-id="a483e-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="a483e-135">Dacă proiectul are, de asemenea, condiții cu plată la plată (PWP) stabilite pentru furnizor, introduceți procentul de prag pentru proiect în câmpul **Procentul de prag PWP**.</span><span class="sxs-lookup"><span data-stu-id="a483e-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="a483e-136">Condițiile de retenție a furnizorului sunt, de asemenea, afișate pe comenzile de cumpărare pe care le creați pentru furnizor.</span><span class="sxs-lookup"><span data-stu-id="a483e-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]