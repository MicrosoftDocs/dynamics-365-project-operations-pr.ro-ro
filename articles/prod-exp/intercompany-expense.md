---
title: Cheltuieli între companii
description: Acest subiect oferă informații despre modul de utilizare a cheltuielilor inter-companii pentru a aloca cheltuielile unui lucrător persoanei juridice pentru care a fost efectuată munca.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005086"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c1a56-103">Cheltuieli între companii</span><span class="sxs-lookup"><span data-stu-id="c1a56-103">Intercompany expenses</span></span>

<span data-ttu-id="c1a56-104">Un lucrător care este angajat de o entitate juridică într-o organizație ar putea efectua lucrări pentru o altă entitate juridică din aceeași organizație.</span><span class="sxs-lookup"><span data-stu-id="c1a56-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c1a56-105">Puteți utiliza cheltuielile inter-companii pentru pentru a aloca cheltuielile lucrătorului persoanei juridice pentru care a fost efectuată munca.</span><span class="sxs-lookup"><span data-stu-id="c1a56-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="c1a56-106">Persoana juridică care angajează lucrătorul se numește persoana juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="c1a56-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c1a56-107">Persoana juridică pentru care lucrătorul efectuează cheltuieli se numește persoana juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="c1a56-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c1a56-108">Înainte ca un lucrător să poată crea și trimite cheltuieli inter-companii, trebuie să activați liniile de cheltuieli inter-companii.</span><span class="sxs-lookup"><span data-stu-id="c1a56-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="c1a56-109">Accesând persoana juridică care împrumută, pe pagina **Parametrii de gestionare a cheltuielilor**, selectați **Permiteți liniile de cheltuieli inter-companii**.</span><span class="sxs-lookup"><span data-stu-id="c1a56-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c1a56-110">Înregistrare fiscală pentru cheltuieli între companii</span><span class="sxs-lookup"><span data-stu-id="c1a56-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1a56-111">Înainte de a putea utiliza grupuri de impozite care sunt asociate cu persoana juridică care împrumută (sursă) în locul entității juridice împrumutate (de destinație) în raportul dvs. de cheltuieli, trebuie să activați funcționalitatea în secțiunea de configurare a impozitului pe vânzări din registrul general.</span><span class="sxs-lookup"><span data-stu-id="c1a56-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="c1a56-112">Cand **Persoană juridică pentru înregistrarea impozitelor inter-companii** parametrul este setat la **Sursă** și **Aplicați regulile de impozitare a impozitului pe vânzări** este setat pe **Nu**, se utilizează o combinația de impozite pentru persoana juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="c1a56-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="c1a56-113">Când același parametru este setat la **Destinaţie**, va fi utilizată combinația fiscală pentru împrumutarea entității juridice.</span><span class="sxs-lookup"><span data-stu-id="c1a56-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c1a56-114">Pentru persoanele juridice din Statele Unite, când parametrul este setat la **Sursă**, câmpul **Impozit pe vânzări de primit** trebuie configurat și pe noua pagină **Grupuri de înregistrare a registrului**.</span><span class="sxs-lookup"><span data-stu-id="c1a56-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c1a56-115">Motorul contabil va utiliza informațiile din acest câmp pentru înregistrarea contabilă referitoare la impozite.</span><span class="sxs-lookup"><span data-stu-id="c1a56-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="c1a56-116">Comportamentul este consecvent pentru liniile de cheltuieli postate cu sau fără un proiect.</span><span class="sxs-lookup"><span data-stu-id="c1a56-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]