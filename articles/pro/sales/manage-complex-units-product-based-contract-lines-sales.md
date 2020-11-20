---
title: Gestionarea unităților complexe pentru liniile de contract bazate pe produse - simplificat
description: Acest subiect oferă informații despre sprijinirea vânzării produselor bazate pe abonament.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177391"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="d1b8f-103">Gestionarea unităților complexe pentru liniile de contract bazate pe produse - simplificat</span><span class="sxs-lookup"><span data-stu-id="d1b8f-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="d1b8f-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="d1b8f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1b8f-105">Dynamics 365 Project Operations utilizează factori de cantitate pentru a asista vânzarea de produse pe bază de abonament.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="d1b8f-106">Pentru produsele bazate pe abonament, cantitatea din linia de contract sau proiect este exprimată ca număr de luni de utilizare.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="d1b8f-107">Prețul software-ului de abonament este stocat în catalogul ca prețul pe utilizator pe lună.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="d1b8f-108">În timpul procesului de vânzări, prețul de pe linia de contract este, de obicei, prețul per utilizator, pe lună, care a fost negociat și actualizat de către agentul de vânzări IT.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="d1b8f-109">Fiecare afacere are un număr diferit de utilizatori și un număr diferit de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="d1b8f-110">Cantitatea utilizată pentru a calcula suma liniei de contract este un produs al numărului de utilizatori și numărul de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="d1b8f-111">Pentru a sprijini acest tip de vânzare, Project Operations acceptă conceptul de *factori de cantitate*.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="d1b8f-112">Factorii de cantitate se bazează pe atributele produsului.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="d1b8f-113">Când configurați proprietăți specifice pentru un produs, puteți semnaliza un subset al acelor proprietăți sau toate proprietățile, ca factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="d1b8f-114">Project Operations validează că numai proprietățile numerice sau proprietățile produsului care au un tip de date numerice sunt marcate ca factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="d1b8f-115">Când un produs cu factori de cantitate configurați este adăugat la o linie de contract, câmpul **Cantitate** devine numai în citire.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="d1b8f-116">După ce introduceți valori pentru proprietățile produsului care sunt factori de cantitate, Project Operations calculează cantitatea liniei de contract.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="d1b8f-117">De exemplu, Dynamics 365 Sales poate avea următoarele proprietăți:</span><span class="sxs-lookup"><span data-stu-id="d1b8f-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="d1b8f-118">**Nr. de utilizatori**: numărul de utilizatori.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="d1b8f-119">**Nr. de luni**: numărul de luni de abonament.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="d1b8f-120">**SKU produs**: Unitatea de stocare a stocului (SKU) pentru produs.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="d1b8f-121">Proprietățile **Nr. de utilizatori** și **Nr. de luni** pot fi marcate ca factori de cantitate prin editarea proprietăților de linie de produs.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="d1b8f-122">Pentru a crea factori de cantitate din proprietățile produsului, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="d1b8f-123">Pe **Project Operations**, selectați **Vânzări-Produse**.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="d1b8f-124">Deschideți produsul pentru care trebuie să setați factori de cantitate.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="d1b8f-125">Asigurați-vă că produsul are proprietăți deja configurate.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="d1b8f-126">Pe pagina **Informații de proiect**, selectați fila **Factori de cantitate**.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="d1b8f-127">În subgrilă selectați **+ Calcul de câmp nou**.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="d1b8f-128">Introduceți numele **Factorului Cantitate** și selectați valoarea proprietății care se mapează la calculul câmpului.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="d1b8f-129">Salvați și închideți formulatul.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-129">Save and close the form.</span></span>
7. <span data-ttu-id="d1b8f-130">Repetați pașii 2-6 pentru toate proprietățile care împreună vor constitui cantitatea pentru linia contractuală bazată pe produs.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="d1b8f-131">Cu setarea factorilor de cantitate, atunci când utilizatorul creează o linie contractuală pentru acest produs, cantitatea liniei contractuale este blocată.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="d1b8f-132">Cantitatea este apoi calculată ca produs al valorilor proprietății pentru acea linie contractuală.</span><span class="sxs-lookup"><span data-stu-id="d1b8f-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
