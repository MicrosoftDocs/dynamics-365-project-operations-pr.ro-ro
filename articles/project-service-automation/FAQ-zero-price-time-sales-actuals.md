---
title: De ce prețul pentru timpul de vânzare real revine la zero?
description: Detectarea motivului pentru care prețul pentru timpul de vânzare real revine la zero.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 202ee371-2863-4bcf-918c-212d7293faa8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 04ab519955b55088d85bdf36c3a90835f70ea501
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754767"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a><span data-ttu-id="3be4d-103">De ce prețul pentru timpul de vânzare real revine la zero?</span><span class="sxs-lookup"><span data-stu-id="3be4d-103">Why is price defaulting to zero on time sales actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3be4d-104">Acest FAQ se aplică valorilor reale în cazul în care clasa de tranzacție este setată pe Timp și tipul de tranzacție este Vânzări nefacturate.</span><span class="sxs-lookup"><span data-stu-id="3be4d-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Unbilled Sales.</span></span> <span data-ttu-id="3be4d-105">Următoarele trei verificări vă vor ajuta să detectați motivul pentru care prețul (rata de facturare) este setat implicit pe 0 pe timpul de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-105">The following three checks will help you troubleshoot why price (bill rate) is defaulting to 0 on time sales actuals.</span></span>

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a><span data-ttu-id="3be4d-106">Verificarea 1: Identificarea listei de prețuri de vânzare pentru proiect</span><span class="sxs-lookup"><span data-stu-id="3be4d-106">Check 1: Identify the sales price list for the project</span></span>

<span data-ttu-id="3be4d-107">Găsiți proiectul din domeniul proiectului efectiv și mergeți la pagina proiectului.</span><span class="sxs-lookup"><span data-stu-id="3be4d-107">Find the project from the project field of the actual and go to the project page.</span></span> <span data-ttu-id="3be4d-108">Apoi, mergeți la fila Vânzări și pe grila de linii de contract proiect, faceți clic pe legătură în câmpul Contractul proiectului.</span><span class="sxs-lookup"><span data-stu-id="3be4d-108">Then go to the Sales tab and on Project Contract lines grid, click on the link in the Project Contract field.</span></span> <span data-ttu-id="3be4d-109">Pagina Contractul proiectului se va deschide.</span><span class="sxs-lookup"><span data-stu-id="3be4d-109">The project Contract page will open.</span></span> <span data-ttu-id="3be4d-110">Pe pagina Contractul proiectului, mergeți la fila Liste de prețuri proiect. Verificați dacă există cel puțin o listă de prețuri atașată aici.</span><span class="sxs-lookup"><span data-stu-id="3be4d-110">On the Project Contract page, go to the Project Price Lists tab. Check if there is at least one price list attached here.</span></span> <span data-ttu-id="3be4d-111">În cazul în care nu este atașată nicio listă de prețuri în grila de liste de prețuri proiect a contractului proiectului, ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="3be4d-111">If there is no price list attached in the Project Price Lists grid of the Project Contract you have isolated the problem.</span></span> <span data-ttu-id="3be4d-112">Atașați o listă de prețuri la grila de liste de prețuri a proiectului.</span><span class="sxs-lookup"><span data-stu-id="3be4d-112">Attach a price list to the Project Price lists grid.</span></span> <span data-ttu-id="3be4d-113">Listele de prețuri care sunt autorizate să fie atașate aici ar trebui să aibă câmpul context setat pe Vânzări și câmpul monedă din lista de prețuri trebuie să corespundă cu câmpul monedă din contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="3be4d-113">The price lists allowed to be attached here should have the context field set to Sales and the currency field on the price list should match the currency field on the Project Contract.</span></span> <span data-ttu-id="3be4d-114">Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă vânzările nefacturate afișează efectiv un preț valid.</span><span class="sxs-lookup"><span data-stu-id="3be4d-114">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the unbilled sales actual shows a valid price.</span></span> 

<span data-ttu-id="3be4d-115">Dacă aveți una sau mai multe liste de prețuri atașate în grila listei de prețuri a proiectului din contractul proiectului, mergeți la următoarea verificare a documentului.</span><span class="sxs-lookup"><span data-stu-id="3be4d-115">If you have one or more price lists attached in the Project Price Lists grid of the Project Contract, proceed to the next check in the document.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a><span data-ttu-id="3be4d-116">Verificarea 2: Listele de prețuri identificate mai sus sunt valabile pentru data specifică a timpului de vânzare real?</span><span class="sxs-lookup"><span data-stu-id="3be4d-116">Check 2: Are any of the price lists identified above valid for the specific date of the time sales actual?</span></span>

<span data-ttu-id="3be4d-117">Pentru ca Project Service să ia în considerare o listă de prețuri pentru prețul implicit, lista de prețuri respectivă trebuie să se aplice pentru data timpului de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-117">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time sales actual.</span></span> <span data-ttu-id="3be4d-118">Verificați următoarele pentru a vedea dacă lista (listele) de prețuri identificate mai sus sunt aplicabile:</span><span class="sxs-lookup"><span data-stu-id="3be4d-118">Check the following to see if the price list(s) identified above are applicable:</span></span>
- <span data-ttu-id="3be4d-119">Verificați dacă datele de început și de sfârșit din fila generală pentru listele de prețuri atașate nu sunt necompletate.</span><span class="sxs-lookup"><span data-stu-id="3be4d-119">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="3be4d-120">În cazul în care datele de început și de sfârșit de pe listele de prețuri identificate anterior sunt necompletate, ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="3be4d-120">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="3be4d-121">Faceți o notă în câmpul dată de început pe timpul de vânzare real și verificați dacă oricare dintre listele de prețuri identificate se aplică pentru această dată.</span><span class="sxs-lookup"><span data-stu-id="3be4d-121">Make a note of the start date field on your time sales actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="3be4d-122">De exemplu, data timpului de vânzare real ar trebui să se încadreze între data de început și data de sfârșit pe lista de prețuri.</span><span class="sxs-lookup"><span data-stu-id="3be4d-122">For example, the date of the time sales actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="3be4d-123">În cazul în care nu există nicio listă de prețuri care să acopere data pe timpul de vânzare real, ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="3be4d-123">If there is no price list that covers that date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="3be4d-124">Modificați datele de început și de sfârșit din lista de prețuri pentru a vă asigura că lista de prețuri cuprinde data timpului de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-124">Modify the start and end dates of the price list to ensure that the price list covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="3be4d-125">În cazul în care există mai mult de o listă de prețuri care să acopere data pe timpul de vânzare real, ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="3be4d-125">If there is more than one price list that covers the date on the time sales actual, you have isolated the problem.</span></span> <span data-ttu-id="3be4d-126">Puteți remedia acest lucru prin editarea datelor de început și sfârșit din listele de prețuri, astfel încât să existe doar o listă de prețuri, care să acopere data timpului de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-126">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time sales actual.</span></span> 
    - <span data-ttu-id="3be4d-127">În cazul în care există doar o listă de prețuri, care să acopere data timpului de vânzare real, treceți la Verificarea 3.</span><span class="sxs-lookup"><span data-stu-id="3be4d-127">If there is only one price list that covers that date of the time sales actual, go to Check 3.</span></span>
<span data-ttu-id="3be4d-128">Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă timpul de vânzare real afișează un preț valid.</span><span class="sxs-lookup"><span data-stu-id="3be4d-128">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a><span data-ttu-id="3be4d-129">Verificarea 3: Există un preț în lista de prețuri pentru dimensiunile tarifare pe timpul de vânzare real?</span><span class="sxs-lookup"><span data-stu-id="3be4d-129">Check 3: Is there a price in the price list for the pricing dimensions on the time sales actual?</span></span>

<span data-ttu-id="3be4d-130">În cazul în care ați finalizat cu succes Verificările 1 și 2, ar trebui să aveți acum doar o singură listă de prețuri, care se aplică pentru data timpului de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-130">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time sales actual.</span></span> <span data-ttu-id="3be4d-131">Deschideți această listă de prețuri și navigați la fila Prețuri rol. Asigurați-vă că există un rând în grilă pentru dimensiunile de stabilire a prețului pe timpul de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-131">Open this Price List and navigate to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the Time sales actual.</span></span>

<span data-ttu-id="3be4d-132">Dacă nu există niciun rând în grila de preț rol pentru dimensiunile de stabilire a prețului pe timpul de vânzare real, atunci ați izolat problema.</span><span class="sxs-lookup"><span data-stu-id="3be4d-132">If there is no row in the role price grid for the pricing dimensions on the time sales actual, then you have isolated the problem.</span></span> <span data-ttu-id="3be4d-133">Creați un rând în grila de Prețuri rol pentru dimensiunile tarifare pe timpul de vânzare real.</span><span class="sxs-lookup"><span data-stu-id="3be4d-133">Create a row in the Role prices grid for the pricing dimensions on your time sales actual.</span></span> <span data-ttu-id="3be4d-134">Odată ce ați făcut remedierile necesare, recreați o intrare de timp, aprobați-o și verificați dacă timpul de vânzare real afișează un preț valid.</span><span class="sxs-lookup"><span data-stu-id="3be4d-134">Once this is done, recreate time entry, approve it, and verify that the time sales actual shows a valid price.</span></span>

<span data-ttu-id="3be4d-135">Dacă nu vedeți în continuare un preț valid pe timpul de vânzare real după ce ați efectuat cele trei verificări de mai sus, vă rugăm să solicitați un tichet de asistență.</span><span class="sxs-lookup"><span data-stu-id="3be4d-135">If you still don't see a valid price on your time sales actual after following the three checks above, please log a support ticket.</span></span> 
