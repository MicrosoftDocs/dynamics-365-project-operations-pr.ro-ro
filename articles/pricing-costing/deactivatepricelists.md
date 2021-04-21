---
title: Dezactivarea listelor de prețuri
description: Acest subiect explică cum să dezactivați sau să eliminați listele de prețuri neutilizate sau vechi.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701964"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="2d170-103">Dezactivarea listelor de prețuri</span><span class="sxs-lookup"><span data-stu-id="2d170-103">Deactivate price lists</span></span> 

<span data-ttu-id="2d170-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="2d170-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2d170-105">Pentru a elimina listele de prețuri vechi sau neutilizate din Dynamics 365 Project Operations, trebuie să parcurgeți doi pași.</span><span class="sxs-lookup"><span data-stu-id="2d170-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="2d170-106">Eliminați sau ștergeți lista de prețuri din anumite pagini.</span><span class="sxs-lookup"><span data-stu-id="2d170-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="2d170-107">Dezactivați sau ștergeți lista de prețuri din listele de prețuri active de pe pagina **Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="2d170-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="2d170-108">Trebuie să parcurgeți ambii pași pentru a elimina complet o listă de prețuri.</span><span class="sxs-lookup"><span data-stu-id="2d170-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="2d170-109">Numai efectuarea pasului 2, care este ștergerea sau dezactivarea directă a listei de prețuri din vizualizarea Listelor de preț active, nu este suficientă.</span><span class="sxs-lookup"><span data-stu-id="2d170-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="2d170-110">De asemenea, trebuie să ștergeți asocierea acestei liste de prețuri din toate locurile menționate la pasul 1.</span><span class="sxs-lookup"><span data-stu-id="2d170-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="2d170-111">Ștergeți lista de prețuri din anumite pagini</span><span class="sxs-lookup"><span data-stu-id="2d170-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="2d170-112">Pentru a șterge o listă de prețuri din Project Operations, accesați următoarele pagini:</span><span class="sxs-lookup"><span data-stu-id="2d170-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="2d170-113">Pagina **Parametri liste de prețuri** > fila **Liste de prețuri**</span><span class="sxs-lookup"><span data-stu-id="2d170-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="2d170-114">Pagina **Unitate organizațională** > grila **Liste de prețuri**</span><span class="sxs-lookup"><span data-stu-id="2d170-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="2d170-115">Pagina **Cont** > grila **Liste de prețuri ale proiectului**</span><span class="sxs-lookup"><span data-stu-id="2d170-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="2d170-116">Pagina **Oferte proiect** > grila **Liste de prețuri ale proiectului**: Acest lucru se aplică tuturor ofertelor de proiect active.</span><span class="sxs-lookup"><span data-stu-id="2d170-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="2d170-117">Pagina **Contracte proiect** > grila **Liste de prețuri ale proiectului**: Acest lucru se aplică tuturor contractelor de proiect active.</span><span class="sxs-lookup"><span data-stu-id="2d170-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="2d170-118">Pentru fiecare pagină, trebuie să selectați lista de prețuri pe care doriți să o ștergeți, apoi să selectați **Ștergere**.</span><span class="sxs-lookup"><span data-stu-id="2d170-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="2d170-119">Ștergeți sau dezactivați lista de prețuri din pagina Liste de prețuri</span><span class="sxs-lookup"><span data-stu-id="2d170-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="2d170-120">Pentru a șterge o listă de prețuri din listele de prețuri active, accesați **Vânzări** > **Clienți** > **Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="2d170-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="2d170-121">Selectați lista de prețuri pe care doriți să o ștergeți și apoi selectați **Ștergere**.</span><span class="sxs-lookup"><span data-stu-id="2d170-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="2d170-122">Dacă lista de prețuri face trimitere la orice tranzacții existente, nu o veți putea șterge.</span><span class="sxs-lookup"><span data-stu-id="2d170-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="2d170-123">Dacă se întâmplă acest lucru, puteți dezactiva lista de prețuri, astfel încât să nu apară în nicio vizualizare.</span><span class="sxs-lookup"><span data-stu-id="2d170-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="2d170-124">Pentru a dezactiva lista de prețuri, selectați din nou lista de prețuri, apoi selectați **Dezactivare**.</span><span class="sxs-lookup"><span data-stu-id="2d170-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
