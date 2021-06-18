---
title: Prezentare generală a liniilor de contract bazate pe produs - simplificat
description: Acest subiect oferă informații despre linii de contract pe bază de produs.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994556"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="1820a-103">Prezentare generală a liniilor de contract bazate pe produs - simplificat</span><span class="sxs-lookup"><span data-stu-id="1820a-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="1820a-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="1820a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1820a-105">Aveți posibilitatea să creați linii de contract bazate pe produse în Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1820a-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="1820a-106">Liniile de contract bazate pe produse pot fi linii create manual sau pot fi elemente din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="1820a-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="1820a-107">Catalog de produse</span><span class="sxs-lookup"><span data-stu-id="1820a-107">Product catalog</span></span>

<span data-ttu-id="1820a-108">Produsele din catalogul de produse au o unitate și un grup de unități implicite.</span><span class="sxs-lookup"><span data-stu-id="1820a-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="1820a-109">Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care are, de asemenea, aceste atribute.</span><span class="sxs-lookup"><span data-stu-id="1820a-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="1820a-110">Toate produsele dintr-o familie de produse moștenesc același set de atribute.</span><span class="sxs-lookup"><span data-stu-id="1820a-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="1820a-111">De exemplu, o companie vinde licențe de abonament pentru mai multe feluri de software.</span><span class="sxs-lookup"><span data-stu-id="1820a-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="1820a-112">Toate software-ul de abonament are următoarele două atribute:</span><span class="sxs-lookup"><span data-stu-id="1820a-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="1820a-113">Numărul de utilizatori</span><span class="sxs-lookup"><span data-stu-id="1820a-113">Number of users</span></span>
- <span data-ttu-id="1820a-114">Durata abonamentului (în luni)</span><span class="sxs-lookup"><span data-stu-id="1820a-114">Subscription duration (in months)</span></span>

<span data-ttu-id="1820a-115">Pentru a menține acest tip de catalog, creați o familie de produse denumită **Abonament de software**.</span><span class="sxs-lookup"><span data-stu-id="1820a-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="1820a-116">Adăugați atributele, **Număr de utilizatori** și **Durata abonamentului** la familia de produse.</span><span class="sxs-lookup"><span data-stu-id="1820a-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="1820a-117">Apoi, adăugați produse individuale la familia de produse **Abonament de software**.</span><span class="sxs-lookup"><span data-stu-id="1820a-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="1820a-118">Adăugați elementele catalogului de produse la un contract de proiect</span><span class="sxs-lookup"><span data-stu-id="1820a-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="1820a-119">Contractele de proiecte au secțiuni pentru două tipuri de linii, pe bază de proiect și pe bază de produs.</span><span class="sxs-lookup"><span data-stu-id="1820a-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="1820a-120">Liniile bazate pe produse includ toate produsele și unitățile din lista de prețuri a produselor din contract.</span><span class="sxs-lookup"><span data-stu-id="1820a-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="1820a-121">Pot fi adăugate produse care nu fac parte dintr-o listă de prețuri de produse de contract.</span><span class="sxs-lookup"><span data-stu-id="1820a-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="1820a-122">Puteți selecta produse din alte liste de prețuri sau direct din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="1820a-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="1820a-123">Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului.</span><span class="sxs-lookup"><span data-stu-id="1820a-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="1820a-124">Dacă nu este setată o listă de prețuri implicită, prețul este setat la 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1820a-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="1820a-125">Dacă o linie de contract se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linie.</span><span class="sxs-lookup"><span data-stu-id="1820a-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="1820a-126">O linie contractuală are câmpul **Prețuri** cu cele două valori:</span><span class="sxs-lookup"><span data-stu-id="1820a-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="1820a-127">**Înlocuire stabilire preț**</span><span class="sxs-lookup"><span data-stu-id="1820a-127">**Override pricing**</span></span>
- <span data-ttu-id="1820a-128">**Utilizați valoarea implicită**</span><span class="sxs-lookup"><span data-stu-id="1820a-128">**Use default**</span></span>

<span data-ttu-id="1820a-129">Dacă configurați câmpul **Prețuri** la **Înlocuire preț**, prețul implicit nu este configurat.</span><span class="sxs-lookup"><span data-stu-id="1820a-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="1820a-130">Introduceți un preț pentru produsul de pe linia de contract.</span><span class="sxs-lookup"><span data-stu-id="1820a-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="1820a-131">Dacă setați câmpul la **Utilizare implicit**, se folosește prețul de vânzare implicit și câmpul nu poate fi editat.</span><span class="sxs-lookup"><span data-stu-id="1820a-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="1820a-132">După ce instalați Project Operations, prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs pe un contract.</span><span class="sxs-lookup"><span data-stu-id="1820a-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="1820a-133">Câmpul **Stabilire preț** este atunci configurat la **Înlocuire preț** astfel încât puteți edita prețul implicit pe liniile de contract.</span><span class="sxs-lookup"><span data-stu-id="1820a-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="1820a-134">Aceasta este o suprascriere specifică Project Operations la comportamentul liniilor bazate pe produse în Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="1820a-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]