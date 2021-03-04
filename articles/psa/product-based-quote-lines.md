---
title: Linii de oferte bazate pe produs
description: Acest subiect oferă informații despre linii de ofertă pe bază de produs.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151268"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="4c6c0-103">Linii de oferte bazate pe produs</span><span class="sxs-lookup"><span data-stu-id="4c6c0-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="4c6c0-104">Aveți posibilitatea să creați linii de ofertă bazate pe produse în Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4c6c0-105">Liniile de ofertă bazate pe produse pot fi linii din afara catalogului sau pot fi elemente din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="4c6c0-106">Catalog de produse</span><span class="sxs-lookup"><span data-stu-id="4c6c0-106">Product catalog</span></span>

<span data-ttu-id="4c6c0-107">Produsele dintr-un catalog de produse Dynamics 365 au o unitate și un grup de unități implicite.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="4c6c0-108">Dacă mai multe produse partajează același set de atribute, puteți crea o familie de produse care are, de asemenea, aceste atribute.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="4c6c0-109">Toate produsele dintr-o familie de produse moștenesc același set de atribute.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="4c6c0-110">De exemplu, o companie vinde licențe de abonament pentru o varietate de software.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="4c6c0-111">Toate software-ul de abonament are următoarele două atribute:</span><span class="sxs-lookup"><span data-stu-id="4c6c0-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="4c6c0-112">Număr de utilizatori</span><span class="sxs-lookup"><span data-stu-id="4c6c0-112">Number of users</span></span> 
- <span data-ttu-id="4c6c0-113">Durata abonamentului (în luni)</span><span class="sxs-lookup"><span data-stu-id="4c6c0-113">Subscription duration (in months)</span></span>

<span data-ttu-id="4c6c0-114">O modalitate bună de a menține acest tip de catalog este de a crea o familie de produse care este denumită **Software de abonament** și care are **Număr de utilizatori** și **Durata abonamentului** ca atribute.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="4c6c0-115">Apoi, puteți adăuga produse individuale, cum ar fi **Dynamics 365 Sales** sau **Dynamics 365 Field Service** la familia de produse **Software de abonament**.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="4c6c0-116">Adăugarea elementelor din catalogul de produse la o ofertă de proiect</span><span class="sxs-lookup"><span data-stu-id="4c6c0-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="4c6c0-117">Oferta de proiect și paginile contractului de proiect au secțiuni pentru două tipuri de linii: linii pe bază de proiect și linii pe bază de produs.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="4c6c0-118">Pentru liniile bazate pe produse, Dynamics 365 este utilizat pentru a adăuga elemente dintr-un catalog de produse la o ofertă.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="4c6c0-119">Lista verticală din linia ofertei sau din linia de contract de proiect include toate produsele și unitățile din lista de prețuri a produsului care este atașată la ofertă sau la contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="4c6c0-120">De asemenea, aveți posibilitatea să adăugați produse care nu fac parte din lista de prețuri a produsului citat.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="4c6c0-121">În plus, puteți selecta produse din alte liste de prețuri sau puteți selecta produse direct din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="4c6c0-122">Când selectați produse direct dintr-un catalog de produse, lista de prețuri implicită a acelui produs este utilizată pentru a obține prețul de vânzare al produsului.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="4c6c0-123">Dacă nu este setată o listă de prețuri implicită, prețul este setat la 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4c6c0-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="4c6c0-124">Dacă o linie de ofertă se bazează pe un catalog de produse, aveți posibilitatea să înlocuiți prețul de vânzare direct în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="4c6c0-125">Rețineți că o linie de ofertă în Dynamics 365 are un câmp de **Prețuri**.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="4c6c0-126">Sunt disponibile două valori:</span><span class="sxs-lookup"><span data-stu-id="4c6c0-126">Two values are available:</span></span>

- <span data-ttu-id="4c6c0-127">Înlocuire stabilire preț</span><span class="sxs-lookup"><span data-stu-id="4c6c0-127">Override pricing</span></span>  
- <span data-ttu-id="4c6c0-128">Utilizați valoarea implicită</span><span class="sxs-lookup"><span data-stu-id="4c6c0-128">Use default</span></span>

<span data-ttu-id="4c6c0-129">Dacă setați acest câmp pentru **Înlocuire stabilire preț**, Dynamics 365 nu configurează un preț implicit.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="4c6c0-130">Trebuie să introduceți un preț pentru produs în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="4c6c0-131">Dacă setați acest câmp pentru a **Utiliza implicit**, Dynamics 365 utilizează prețul implicit de vânzare și blochează câmpul pentru a preveni editarea.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="4c6c0-132">După ce instalați PSA, prețurile de vânzare implicite sunt introduse pe liniile bazate pe produs pe o ofertă.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="4c6c0-133">Câmpul **Stabilire preț** este atunci configurat la **Înlocuire stabilire preț** astfel încât puteți edita prețul implicit pe liniile de ofertă.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Configurare înlocuire stabilire preț](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="4c6c0-135">Factori de cantitate pentru produse</span><span class="sxs-lookup"><span data-stu-id="4c6c0-135">Quantity factors for products</span></span>

<span data-ttu-id="4c6c0-136">PSA utilizează factori de cantitate pentru a asista vânzarea de produse pe bază de abonament.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="4c6c0-137">Pentru produsele bazate pe abonament, cantitatea din linia de contract de ofertă sau de proiect este exprimată ca număr de luni de utilizare.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="4c6c0-138">De obicei, prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="4c6c0-139">Cu toate acestea, puteți utiliza alte descrieri de timp în schimb.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="4c6c0-140">În timpul procesului de vânzări, prețul de pe linia de ofertă este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="4c6c0-141">Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="4c6c0-142">Cantitatea utilizată pentru a calcula suma liniei de ofertă este un produs al numărului de utilizatori și numărul de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="4c6c0-143">Pentru a sprijini acest tip de vânzare, PSA a introdus conceptul de factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="4c6c0-144">Factorii de cantitate se bazează pe atributele produsului în Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="4c6c0-145">Când configurați proprietăți specifice pentru un produs, PSA vă permite să semnalizați un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="4c6c0-146">PSA validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="4c6c0-147">Când un produs pentru care sunt configurate factori de cantitate este adăugat la o linie de ofertă câmpul **Cantitate** din linia de ofertă devine un câmp doar în citire.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="4c6c0-148">După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, PSA calculează cantitatea liniei de ofertă.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="4c6c0-149">De exemplu, Dynamics 365 poate avea următoarele proprietăți:</span><span class="sxs-lookup"><span data-stu-id="4c6c0-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="4c6c0-150">**Nr. de utilizatori** - numărul de utilizatori</span><span class="sxs-lookup"><span data-stu-id="4c6c0-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="4c6c0-151">**Nr. de luni** - numărul de luni de abonament</span><span class="sxs-lookup"><span data-stu-id="4c6c0-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="4c6c0-152">**Produs SKU**</span><span class="sxs-lookup"><span data-stu-id="4c6c0-152">**Product SKU**</span></span> 

<span data-ttu-id="4c6c0-153">Proprietățile **Nr. de utilizatori** și **Nr. de luni** pot fi marcate ca factori de cantitate prin editarea proprietăților de linie de produs.</span><span class="sxs-lookup"><span data-stu-id="4c6c0-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Semnalizarea Nr. de utilizatori și Nr. de luni ca factori de calitate](media/basic-guide-11.png)
 
