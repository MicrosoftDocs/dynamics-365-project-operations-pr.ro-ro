---
title: Dezactivarea listelor de prețuri
description: Acest subiect explică cum să dezactivați sau să eliminați listele de prețuri neutilizate sau vechi.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d5d6cf6b4b097c08edca5a3235ed1b438a0eae2d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001351"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="aa53c-103">Dezactivarea listelor de prețuri</span><span class="sxs-lookup"><span data-stu-id="aa53c-103">Deactivate price lists</span></span> 

<span data-ttu-id="aa53c-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="aa53c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="aa53c-105">Pentru a elimina listele de prețuri vechi sau neutilizate din Dynamics 365 Project Operations, trebuie să parcurgeți doi pași.</span><span class="sxs-lookup"><span data-stu-id="aa53c-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="aa53c-106">Eliminați sau ștergeți lista de prețuri din anumite pagini.</span><span class="sxs-lookup"><span data-stu-id="aa53c-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="aa53c-107">Dezactivați sau ștergeți lista de prețuri din listele de prețuri active de pe pagina **Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="aa53c-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="aa53c-108">Trebuie să parcurgeți ambii pași pentru a elimina complet o listă de prețuri.</span><span class="sxs-lookup"><span data-stu-id="aa53c-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="aa53c-109">Numai efectuarea pasului 2, care este ștergerea sau dezactivarea directă a listei de prețuri din vizualizarea Listelor de preț active, nu este suficientă.</span><span class="sxs-lookup"><span data-stu-id="aa53c-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="aa53c-110">De asemenea, trebuie să ștergeți asocierea acestei liste de prețuri din toate locurile menționate la pasul 1.</span><span class="sxs-lookup"><span data-stu-id="aa53c-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="aa53c-111">Ștergeți lista de prețuri din anumite pagini</span><span class="sxs-lookup"><span data-stu-id="aa53c-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="aa53c-112">Pentru a șterge o listă de prețuri din Project Operations, accesați următoarele pagini:</span><span class="sxs-lookup"><span data-stu-id="aa53c-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="aa53c-113">Pagina **Parametri liste de prețuri** > fila **Liste de prețuri**</span><span class="sxs-lookup"><span data-stu-id="aa53c-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="aa53c-114">Pagina **Unitate organizațională** > grila **Liste de prețuri**</span><span class="sxs-lookup"><span data-stu-id="aa53c-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="aa53c-115">Pagina **Cont** > grila **Liste de prețuri ale proiectului**</span><span class="sxs-lookup"><span data-stu-id="aa53c-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="aa53c-116">Pagina **Oferte proiect** > grila **Liste de prețuri ale proiectului**: Acest lucru se aplică tuturor ofertelor de proiect active.</span><span class="sxs-lookup"><span data-stu-id="aa53c-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="aa53c-117">Pagina **Contracte proiect** > grila **Liste de prețuri ale proiectului**: Acest lucru se aplică tuturor contractelor de proiect active.</span><span class="sxs-lookup"><span data-stu-id="aa53c-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="aa53c-118">Pentru fiecare pagină, trebuie să selectați lista de prețuri pe care doriți să o ștergeți, apoi să selectați **Ștergere**.</span><span class="sxs-lookup"><span data-stu-id="aa53c-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="aa53c-119">Ștergeți sau dezactivați lista de prețuri din pagina Liste de prețuri</span><span class="sxs-lookup"><span data-stu-id="aa53c-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="aa53c-120">Pentru a șterge o listă de prețuri din listele de prețuri active, accesați **Vânzări** > **Clienți** > **Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="aa53c-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="aa53c-121">Selectați lista de prețuri pe care doriți să o ștergeți și apoi selectați **Ștergere**.</span><span class="sxs-lookup"><span data-stu-id="aa53c-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="aa53c-122">Dacă lista de prețuri face trimitere la orice tranzacții existente, nu o veți putea șterge.</span><span class="sxs-lookup"><span data-stu-id="aa53c-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="aa53c-123">Dacă se întâmplă acest lucru, puteți dezactiva lista de prețuri, astfel încât să nu apară în nicio vizualizare.</span><span class="sxs-lookup"><span data-stu-id="aa53c-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="aa53c-124">Pentru a dezactiva lista de prețuri, selectați din nou lista de prețuri, apoi selectați **Dezactivare**.</span><span class="sxs-lookup"><span data-stu-id="aa53c-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
