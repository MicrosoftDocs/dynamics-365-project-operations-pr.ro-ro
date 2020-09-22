---
title: Crearea unei liste de preţuri
description: Cum să creați o listă de prețuri în Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754835"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="541d1-103">Crearea unei liste de prețuri (Project Service)</span><span class="sxs-lookup"><span data-stu-id="541d1-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="541d1-104">Listele de prețuri oferă un șablon pe care îl pot utiliza managerii dvs. de cont pentru a crea oferte și proiecte, și pentru a stabili costurile unui proiect.</span><span class="sxs-lookup"><span data-stu-id="541d1-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="541d1-105">Oferă o listă de elemente de linie pentru roluri și cheltuieli și prețul pe care îl veți încasa pentru fiecare.</span><span class="sxs-lookup"><span data-stu-id="541d1-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="541d1-106">Puteți crea mai multe liste de prețuri, ca să puteți păstra structuri diferite de preț pentru regiuni diferite în care vă vindeți produsele sau pentru canale de vânzare diferite.</span><span class="sxs-lookup"><span data-stu-id="541d1-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="541d1-107">Este o idee bună să creați cel puțin o listă de prețuri pentru fiecare monedă în care aveți de gând să vă facturați clienții.</span><span class="sxs-lookup"><span data-stu-id="541d1-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="541d1-108">Pentru a crea estimări financiare pentru lucrul pe care l-ați livrat, asigurați-vă că fiecare proiect are un cost de rezervă și liste de prețuri de vânzări.</span><span class="sxs-lookup"><span data-stu-id="541d1-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="541d1-109">Configurați un cost implicit și o listă de prețuri care se aplică la toate proiectele create în cadrul organizației.</span><span class="sxs-lookup"><span data-stu-id="541d1-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="541d1-110">Listele de prețuri se bazează pe roluri și categorii de cheltuieli, așadar, înainte de a crea o listă de preturi, asigurați-vă că ați configurat deja rolurile și categoriile de cheltuieli pe care doriți să le utilizați când creați lista de prețuri.</span><span class="sxs-lookup"><span data-stu-id="541d1-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="541d1-111">Accesați **Project Service > Liste de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="541d1-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="541d1-112">Faceți clic pe **Nou**.</span><span class="sxs-lookup"><span data-stu-id="541d1-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="541d1-113">În **Context**, selectați dacă lista de prețuri este pentru **Cost**, **Cumpărare** sau **Vânzări**.</span><span class="sxs-lookup"><span data-stu-id="541d1-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="541d1-114">În **Nume**, introduceți un nume pentru lista de prețuri.</span><span class="sxs-lookup"><span data-stu-id="541d1-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="541d1-115">În **Monedă**, selectați moneda pe care o veți utiliza pentru facturare sau costuri.</span><span class="sxs-lookup"><span data-stu-id="541d1-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="541d1-116">În **Unitate de timp**, specificați perioada pentru care se aplică prețul, cum ar fi o zi sau o oră.</span><span class="sxs-lookup"><span data-stu-id="541d1-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="541d1-117">Completați **Dată de început**, **Dată de sfârșit** și **Descriere**, după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="541d1-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="541d1-118">Faceți clic pe **Salvare** pentru a crea înregistrarea, astfel încât să o puteți edita în continuare.</span><span class="sxs-lookup"><span data-stu-id="541d1-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="541d1-119">Pentru a adăuga un preț de rol la lista de prețuri, faceți clic pe **+** sub **Prețuri de rol**.</span><span class="sxs-lookup"><span data-stu-id="541d1-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="541d1-120">În panoul **Preț de rol**, completați detaliile, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="541d1-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="541d1-121">Continuați să adăugați prețuri de roluri după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="541d1-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="541d1-122">După ce ați terminat, faceți clic pe **Salvare** colțul din dreapta jos al ecranului.</span><span class="sxs-lookup"><span data-stu-id="541d1-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="541d1-123">Pentru a adăuga un preț de categorie de cheltuieli la lista de prețuri, faceți clic pe **+** sub **Prețuri de categorie**.</span><span class="sxs-lookup"><span data-stu-id="541d1-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="541d1-124">În panoul **Preț categorie de tranzacție**, completați detaliile, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="541d1-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="541d1-125">Continuați să adăugați prețuri de categorii după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="541d1-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="541d1-126">După ce ați terminat, faceți clic pe **Salvare** colțul din dreapta jos al ecranului.</span><span class="sxs-lookup"><span data-stu-id="541d1-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="541d1-127">Pentru a adăuga elemente de listă de preț în lista de prețuri, faceți clic pe **+** sub **Elemente listă de prețuri**.</span><span class="sxs-lookup"><span data-stu-id="541d1-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="541d1-128">În panoul **Element listă de prețuri**, completați detaliile, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="541d1-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="541d1-129">Continuați să adăugați elemente de listă de prețuri după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="541d1-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="541d1-130">După ce ați terminat, faceți clic pe **Salvare** colțul din dreapta jos al ecranului.</span><span class="sxs-lookup"><span data-stu-id="541d1-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="541d1-131">Pentru a adăuga relații de teritoriu în lista de prețuri, faceți clic pe **+** sub **Relații teritoriale**.</span><span class="sxs-lookup"><span data-stu-id="541d1-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="541d1-132">În fereastra **Conexiune nouă**, completați detaliile, apoi faceți clic pe **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="541d1-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="541d1-133">Continuați să adăugați relații teritoriale după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="541d1-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="541d1-134">După ce ați terminat, faceți clic pe **Salvare** colțul din dreapta jos al ecranului.</span><span class="sxs-lookup"><span data-stu-id="541d1-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="541d1-135">Consultați și</span><span class="sxs-lookup"><span data-stu-id="541d1-135">See Also</span></span>  
 [<span data-ttu-id="541d1-136">Configurați Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="541d1-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
