---
title: Prezentare generală a liniilor de oferte bazate pe produs - simplificat
description: Acest subiect oferă informații despre lucrul cu linii de ofertă bazate pe produs.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178203"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="49c8b-103">Prezentare generală a liniilor de oferte bazate pe produs - simplificat</span><span class="sxs-lookup"><span data-stu-id="49c8b-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="49c8b-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="49c8b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="49c8b-105">Aveți posibilitatea să creați linii de ofertă bazate pe produse în Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="49c8b-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="49c8b-106">Liniile de ofertă bazate pe produse pot fi adăugate manual sau pot fi elemente din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="49c8b-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="49c8b-107">Catalog de produse</span><span class="sxs-lookup"><span data-stu-id="49c8b-107">Product catalog</span></span>

<span data-ttu-id="49c8b-108">Fiecare produs din catalogul de produse are o unitate implicită și un grup de unități.</span><span class="sxs-lookup"><span data-stu-id="49c8b-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="49c8b-109">Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care partajează, de asemenea, aceste atribute.</span><span class="sxs-lookup"><span data-stu-id="49c8b-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="49c8b-110">De exemplu, o companie vinde licențe de abonament pentru mai multe feluri de software.</span><span class="sxs-lookup"><span data-stu-id="49c8b-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="49c8b-111">Toate software-ul de abonament are următoarele două atribute:</span><span class="sxs-lookup"><span data-stu-id="49c8b-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="49c8b-112">Numărul de utilizatori</span><span class="sxs-lookup"><span data-stu-id="49c8b-112">Number of users</span></span>
- <span data-ttu-id="49c8b-113">Durata unui abonament măsurată în luni</span><span class="sxs-lookup"><span data-stu-id="49c8b-113">A subscription duration measured in months</span></span>

<span data-ttu-id="49c8b-114">Pentru a întreține acest tip de catalog, creați o familie de produse numită **Software de abonament** și adăugați numărul de utilizatori și durata abonamentului ca atribute.</span><span class="sxs-lookup"><span data-stu-id="49c8b-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="49c8b-115">Apoi, puteți adăuga produse individuale la familia de produse **Software de abonament**.</span><span class="sxs-lookup"><span data-stu-id="49c8b-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="49c8b-116">Adăugați elemente din catalogul de produse la o ofertă de proiect</span><span class="sxs-lookup"><span data-stu-id="49c8b-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="49c8b-117">Paginile **Ofertă de proiect** și **Contractul de proiect** au secțiuni pentru linii pe bază de proiect și linii pe bază de produs.</span><span class="sxs-lookup"><span data-stu-id="49c8b-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="49c8b-118">Pentru linii pe bază de produs, lista verticală din linia ofertei sau din linia de contract de proiect include toate produsele și unitățile din lista de prețuri a produsului.</span><span class="sxs-lookup"><span data-stu-id="49c8b-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="49c8b-119">De asemenea, aveți posibilitatea să adăugați produse care nu fac parte din lista de prețuri a produsului.</span><span class="sxs-lookup"><span data-stu-id="49c8b-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="49c8b-120">În plus, puteți selecta produse din alte liste de prețuri sau direct din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="49c8b-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="49c8b-121">Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului.</span><span class="sxs-lookup"><span data-stu-id="49c8b-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="49c8b-122">Dacă nu este setată o listă de prețuri implicită, prețul este setat la zero (0).</span><span class="sxs-lookup"><span data-stu-id="49c8b-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="49c8b-123">Când o linie de ofertă se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="49c8b-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="49c8b-124">O linie de ofertă în câmpul **Prețuri** cu două valori disponibile:</span><span class="sxs-lookup"><span data-stu-id="49c8b-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="49c8b-125">**Înlocuire stabilire preț**</span><span class="sxs-lookup"><span data-stu-id="49c8b-125">**Override Pricing**</span></span>
- <span data-ttu-id="49c8b-126">**Utilizare valoare implicită**</span><span class="sxs-lookup"><span data-stu-id="49c8b-126">**Use Default**</span></span>

<span data-ttu-id="49c8b-127">Dacă selectați **Înlocuiți prețurile**, prețul implicit nu este setat.</span><span class="sxs-lookup"><span data-stu-id="49c8b-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="49c8b-128">În schimb, trebuie să introduceți un preț pentru produs în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="49c8b-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="49c8b-129">Dacă selectați **Utilizare implicit**, se folosește prețul de vânzare implicit și câmpul este blocat pentru editare.</span><span class="sxs-lookup"><span data-stu-id="49c8b-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="49c8b-130">Prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs ale unei oferte.</span><span class="sxs-lookup"><span data-stu-id="49c8b-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="49c8b-131">Câmpul **Stabilire preț** este atunci configurat la **Înlocuire preț** astfel încât puteți edita prețul implicit pe liniile de ofertă.</span><span class="sxs-lookup"><span data-stu-id="49c8b-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="49c8b-132">Aceasta este o suprascriere specifică Project Operations la comportamentul liniilor bazate pe produs în Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="49c8b-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
