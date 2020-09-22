---
title: Linii de oferte bazate pe produs
description: Acest subiect oferă informații despre linii de ofertă pe bază de produs.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754726"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="3b416-103">Linii de oferte bazate pe produs</span><span class="sxs-lookup"><span data-stu-id="3b416-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="3b416-104">Aveți posibilitatea să creați linii de ofertă bazate pe produse în Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3b416-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="3b416-105">Liniile de ofertă bazate pe produse pot fi linii din afara catalogului sau pot fi elemente din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="3b416-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="3b416-106">Catalog de produse</span><span class="sxs-lookup"><span data-stu-id="3b416-106">Product catalog</span></span>

<span data-ttu-id="3b416-107">Produsele dintr-un catalog de produse Dynamics 365 au o unitate și un grup de unități implicite.</span><span class="sxs-lookup"><span data-stu-id="3b416-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="3b416-108">Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care are, de asemenea, aceste atribute.</span><span class="sxs-lookup"><span data-stu-id="3b416-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="3b416-109">Toate produsele dintr-o familie de produse moștenesc același set de atribute.</span><span class="sxs-lookup"><span data-stu-id="3b416-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="3b416-110">De exemplu, o companie vinde licențe de abonament pentru o varietate de software.</span><span class="sxs-lookup"><span data-stu-id="3b416-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="3b416-111">Toate software-ul de abonament are următoarele două atribute:</span><span class="sxs-lookup"><span data-stu-id="3b416-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="3b416-112">Număr de utilizatori</span><span class="sxs-lookup"><span data-stu-id="3b416-112">Number of users</span></span> 
- <span data-ttu-id="3b416-113">Durata abonamentului (în luni)</span><span class="sxs-lookup"><span data-stu-id="3b416-113">Subscription duration (in months)</span></span>

<span data-ttu-id="3b416-114">O modalitate bună de a menține acest tip de catalog este de a crea o familie de produse care este denumită **Software de abonament** și care are **Număr de utilizatori** și **Durata abonamentului** ca atribute.</span><span class="sxs-lookup"><span data-stu-id="3b416-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="3b416-115">Apoi, puteți adăuga produse individuale, cum ar fi **Dynamics 365 Sales** sau **Dynamics 365 Field Service** la familia de produse **Software de abonament**.</span><span class="sxs-lookup"><span data-stu-id="3b416-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="3b416-116">Adăugarea elementelor din catalogul de produse la o ofertă de proiect</span><span class="sxs-lookup"><span data-stu-id="3b416-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="3b416-117">Oferta de proiect și paginile contractului de proiect au secțiuni pentru două tipuri de linii: linii pe bază de proiect și linii pe bază de produs.</span><span class="sxs-lookup"><span data-stu-id="3b416-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="3b416-118">Pentru liniile bazate pe produse, Dynamics 365 este utilizat pentru a adăuga elemente dintr-un catalog de produse la o ofertă.</span><span class="sxs-lookup"><span data-stu-id="3b416-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="3b416-119">Lista verticală din linia ofertei sau din linia de contract de proiect include toate produsele și unitățile din lista de prețuri a produsului care este atașată la ofertă sau la contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="3b416-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="3b416-120">De asemenea, aveți posibilitatea să adăugați produse care nu fac parte din lista de prețuri a produsului citat.</span><span class="sxs-lookup"><span data-stu-id="3b416-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="3b416-121">În plus, puteți selecta produse din alte liste de prețuri sau puteți selecta produse direct din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="3b416-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="3b416-122">Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului.</span><span class="sxs-lookup"><span data-stu-id="3b416-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="3b416-123">Dacă nu este setată o listă de prețuri implicită, prețul este setat la 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="3b416-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="3b416-124">Dacă o linie de ofertă se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3b416-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="3b416-125">Rețineți că o linie de ofertă în Dynamics 365 are un câmp de **Prețuri**.</span><span class="sxs-lookup"><span data-stu-id="3b416-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="3b416-126">Sunt disponibile două valori:</span><span class="sxs-lookup"><span data-stu-id="3b416-126">Two values are available:</span></span>

- <span data-ttu-id="3b416-127">Înlocuire stabilire preț</span><span class="sxs-lookup"><span data-stu-id="3b416-127">Override pricing</span></span>  
- <span data-ttu-id="3b416-128">Utilizați valoarea implicită</span><span class="sxs-lookup"><span data-stu-id="3b416-128">Use default</span></span>

<span data-ttu-id="3b416-129">Dacă setați acest câmp pentru **Înlocuire stabilire preț**, Dynamics 365 nu configurează un preț implicit.</span><span class="sxs-lookup"><span data-stu-id="3b416-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="3b416-130">Trebuie să introduceți un preț pentru produs în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3b416-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="3b416-131">Dacă setați acest câmp pentru a **Utiliza implicit**, Dynamics 365 utilizează prețul implicit de vânzare și blochează câmpul pentru a preveni editarea.</span><span class="sxs-lookup"><span data-stu-id="3b416-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="3b416-132">După ce instalați PSA, prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs pe o ofertă.</span><span class="sxs-lookup"><span data-stu-id="3b416-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="3b416-133">Câmpul **Stabilire preț** este atunci configurat la **Înlocuire stabilire preț** astfel încât puteți edita prețul implicit pe liniile de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3b416-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Configurare înlocuire stabilire preț](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="3b416-135">Factori de cantitate pentru produse</span><span class="sxs-lookup"><span data-stu-id="3b416-135">Quantity factors for products</span></span>

<span data-ttu-id="3b416-136">PSA utilizează factori de cantitate pentru a asista vânzarea de produse pe bază de abonament.</span><span class="sxs-lookup"><span data-stu-id="3b416-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="3b416-137">Pentru produsele bazate pe abonament, cantitatea din linia de contract de ofertă sau de proiect este exprimată ca număr de luni de utilizare.</span><span class="sxs-lookup"><span data-stu-id="3b416-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="3b416-138">De obicei, prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună.</span><span class="sxs-lookup"><span data-stu-id="3b416-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="3b416-139">Cu toate acestea, puteți utiliza alte descrieri de timp în schimb.</span><span class="sxs-lookup"><span data-stu-id="3b416-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="3b416-140">În timpul procesului de vânzări, prețul de pe linia de ofertă este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT.</span><span class="sxs-lookup"><span data-stu-id="3b416-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="3b416-141">Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="3b416-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="3b416-142">Cantitatea utilizată pentru a calcula suma liniei de ofertă este un produs al numărului de utilizatori și numărul de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="3b416-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="3b416-143">Pentru a sprijini acest tip de vânzare, PSA a introdus conceptul de factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="3b416-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="3b416-144">Factorii de cantitate se bazează pe atributele produsului în Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3b416-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="3b416-145">Când configurați proprietăți specifice pentru un produs, PSA vă permite să semnalizați un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="3b416-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="3b416-146">PSA validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="3b416-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="3b416-147">Când un produs pentru care sunt configurate factori de cantitate este adăugat la o linie de ofertă câmpul **Cantitate** din linia de ofertă devine un câmp doar în citire.</span><span class="sxs-lookup"><span data-stu-id="3b416-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="3b416-148">După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, PSA calculează cantitatea liniei de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3b416-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="3b416-149">De exemplu, Dynamics 365 poate avea următoarele proprietăți:</span><span class="sxs-lookup"><span data-stu-id="3b416-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="3b416-150">**Nr. de utilizatori** - numărul de utilizatori</span><span class="sxs-lookup"><span data-stu-id="3b416-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="3b416-151">**Nr. de luni** - numărul de luni de abonament</span><span class="sxs-lookup"><span data-stu-id="3b416-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="3b416-152">**Produs SKU**</span><span class="sxs-lookup"><span data-stu-id="3b416-152">**Product SKU**</span></span> 

<span data-ttu-id="3b416-153">Proprietățile **Nr. de utilizatori** și **Nr. de luni** pot fi marcate ca factori de cantitate prin editarea proprietăților de linie de produs.</span><span class="sxs-lookup"><span data-stu-id="3b416-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Semnalizarea Nr. de utilizatori și Nr. de luni ca factori de calitate](media/basic-guide-11.png)
 
