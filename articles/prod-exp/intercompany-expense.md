---
title: Cheltuieli între companii
description: Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație. În această situație, puteți utiliza caracteristica de cheltuieli între companii pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată lucrarea.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082947"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="21940-104">Cheltuieli între companii</span><span class="sxs-lookup"><span data-stu-id="21940-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21940-105">Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație.</span><span class="sxs-lookup"><span data-stu-id="21940-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="21940-106">În această situație, puteți utiliza caracteristica de cheltuieli între companii pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată lucrarea.</span><span class="sxs-lookup"><span data-stu-id="21940-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="21940-107">Persoana juridică care angajează lucrătorul se numește persoana juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="21940-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="21940-108">Persoana juridică pentru care lucrătorul efectuează cheltuieli se numește persoana juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="21940-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="21940-109">Înainte ca un lucrător să poată crea și depune cheltuieli pentru munca efectuată pentru o altă entitate juridică, în entitatea juridică care împrumută, pe pagina **Parametrii de gestionare a cheltuielilor** , selectați opțiunea **Permiteți liniile de cheltuieli între companii**.</span><span class="sxs-lookup"><span data-stu-id="21940-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="21940-110">Înregistrare fiscală pentru cheltuieli între companii</span><span class="sxs-lookup"><span data-stu-id="21940-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21940-111">Dacă doriți să utilizați grupuri de impozite care sunt asociate cu persoana juridică de împrumut (sursă) în locul entității juridice de împrumut (de destinație) în raportul dvs. de cheltuieli, va trebui să configurați acest lucru în setul de impozitare pe contabilitate.</span><span class="sxs-lookup"><span data-stu-id="21940-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="21940-112">Când parametrul contabil general, **Persoană juridică pentru înregistrarea impozitelor între companii** este setat la **Sursă** și **Aplicați regulile de impozitare a impozitului pe vânzări** este setat la **Nu** , va fi utilizată combinația de impozite pentru persoana juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="21940-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="21940-113">Când același parametru este setat la **Destinaţie** , va fi utilizată combinația fiscală pentru împrumutarea entității juridice.</span><span class="sxs-lookup"><span data-stu-id="21940-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="21940-114">Pentru persoanele juridice din Statele Unite, când parametrul este setat la **Sursă** , câmpul **Impozit pe vânzări de primit** trebuie configurat și pe noua pagină **Grupuri de înregistrare a registrului**.</span><span class="sxs-lookup"><span data-stu-id="21940-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="21940-115">Motorul contabil va utiliza informațiile din acest câmp pentru înregistrarea contabilă legată de impozite.</span><span class="sxs-lookup"><span data-stu-id="21940-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="21940-116">Comportamentul este consecvent pentru liniile de cheltuieli postate cu sau fără un proiect.</span><span class="sxs-lookup"><span data-stu-id="21940-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
