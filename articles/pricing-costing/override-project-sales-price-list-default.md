---
title: Înlocuirea listelor de prețuri de vânzare pentru proiect
description: Acest subiect oferă informații despre crearea listelor de prețuri de vânzare particularizate.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275553"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="b64ce-103">Înlocuirea listelor de prețuri de vânzare pentru proiect</span><span class="sxs-lookup"><span data-stu-id="b64ce-103">Override project sales price lists</span></span>

<span data-ttu-id="b64ce-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="b64ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="b64ce-105">Liste de prețuri de proiect specifice clientului</span><span class="sxs-lookup"><span data-stu-id="b64ce-105">Customer-specific project price lists</span></span>

<span data-ttu-id="b64ce-106">Acordurile de preț specifice clienților pot fi configurate ca liste de prețuri ale proiectelor într-o înregistrare de cont în Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b64ce-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="b64ce-107">Pentru a configura o listă de prețuri specifice proiectului pentru client, în zona **Vânzări**, navigați la înregistrarea contului.</span><span class="sxs-lookup"><span data-stu-id="b64ce-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="b64ce-108">Deschideți pagina listei **Conturi**.</span><span class="sxs-lookup"><span data-stu-id="b64ce-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="b64ce-109">Găsiți și faceți dublu clic pe o înregistrare de client pentru a deschide pagina de detalii **Cont**.</span><span class="sxs-lookup"><span data-stu-id="b64ce-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="b64ce-110">Pe fila **Liste de prețuri de proiect**, selectați **+ Listă de prețuri de proiect nou**.</span><span class="sxs-lookup"><span data-stu-id="b64ce-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="b64ce-111">Pe pagina **Lista de prețuri a proiectului nou**, selectați o listă de prețuri din meniul derulant.</span><span class="sxs-lookup"><span data-stu-id="b64ce-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="b64ce-112">Numai listele de prețuri care au contextul setat la **Vânzări** și a căror monedă se potrivește cu moneda contului sunt incluse.</span><span class="sxs-lookup"><span data-stu-id="b64ce-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="b64ce-113">Numiți asocierea și apoi selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="b64ce-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="b64ce-114">Este creată o listă de prețuri de proiect specifică clientului.</span><span class="sxs-lookup"><span data-stu-id="b64ce-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="b64ce-115">Această listă de prețuri va fi utilizată la prețurile implicite ale proiectului pentru ofertele de proiecte sau contractele create pentru acest client, atunci când data creată a contractului de ofertă sau a proiectului se încadrează în data efectivității listei de prețuri.</span><span class="sxs-lookup"><span data-stu-id="b64ce-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="b64ce-116">Prețuri particularizate pentru ofertele de proiect</span><span class="sxs-lookup"><span data-stu-id="b64ce-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="b64ce-117">În ofertele proiectului, puteți avea prețuri de proiect care încep cu o listă de preț standard implicită, care este implicită de la client sau de la parametrii proiectului.</span><span class="sxs-lookup"><span data-stu-id="b64ce-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="b64ce-118">Când aveți nevoie de prețuri particularizate pentru lucrări legate de proiect pentru o anumită ofertă, puteți obține acest lucru din listele de prețuri ale proiectului entității asociate.</span><span class="sxs-lookup"><span data-stu-id="b64ce-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="b64ce-119">Parcurgeți pașii următori pentru a configura prețuri de ofertă specifice proiectului.</span><span class="sxs-lookup"><span data-stu-id="b64ce-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="b64ce-120">Deschideți oferta de proiect și selectați fila **Liste de prețuri de proiect**.</span><span class="sxs-lookup"><span data-stu-id="b64ce-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="b64ce-121">În subgrilă, selectați **Creați prețuri particularizate**.</span><span class="sxs-lookup"><span data-stu-id="b64ce-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="b64ce-122">Toate listele de prețuri ale proiectului care sunt atașate la ofertă sunt copiate în listele de prețuri noi.</span><span class="sxs-lookup"><span data-stu-id="b64ce-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="b64ce-123">Numele noilor liste de prețuri reflectă numele ofertelor cu o ștampilă dată-oră pentru momentul în care au fost create aceste liste de prețuri.</span><span class="sxs-lookup"><span data-stu-id="b64ce-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="b64ce-124">Puteți utiliza fiecare dintre aceste liste de prețuri și puteți actualiza prețurile forței de muncă (prețul rolului) și cheltuielile (prețul categoriei).</span><span class="sxs-lookup"><span data-stu-id="b64ce-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="b64ce-125">Aceste prețuri modificate se vor aplica numai acestei oferte de proiect.</span><span class="sxs-lookup"><span data-stu-id="b64ce-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="b64ce-126">Liste de prețuri pe un contract de proiect</span><span class="sxs-lookup"><span data-stu-id="b64ce-126">Price lists on a project contract</span></span>

<span data-ttu-id="b64ce-127">Pe un contract de proiect, prețul proiectului este întotdeauna implicit ca o listă de prețuri personalizată cu numele contractului și ștampila de dată și oră creată atașată la nume.</span><span class="sxs-lookup"><span data-stu-id="b64ce-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="b64ce-128">Acest lucru este adevărat dacă contractul a fost creat atunci când a fost câștigată oferta sau dacă contractul a fost creat de la zero.</span><span class="sxs-lookup"><span data-stu-id="b64ce-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="b64ce-129">Dacă este necesar, puteți elimina această asociere în lista de prețuri personalizată și, în schimb, să asociați o listă de preț standard contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="b64ce-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="b64ce-130">Când asociați o listă de prețuri standard cu listele de prețuri ale proiectului la ofertă sau contract, orice modificare adusă prețurilor din lista de prețuri va avea impact asupra tuturor ofertelor și contractelor care utilizează lista de prețuri.</span><span class="sxs-lookup"><span data-stu-id="b64ce-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]