---
title: Linii de contract bazate pe oportunitate - simplificat
description: Acest subiect furnizează informații despre elemente de linie de oportunitate pe bază de proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176355"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="e5a04-103">Linii de contract bazate pe oportunitate - simplificat</span><span class="sxs-lookup"><span data-stu-id="e5a04-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="e5a04-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="e5a04-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5a04-105">Liniile de oportunitate bazate pe produse sunt elemente rând din Oportunitate.</span><span class="sxs-lookup"><span data-stu-id="e5a04-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="e5a04-106">Aceste linii sunt livrate clientului ca elemente rând distincte pe eventuala factură fără alte servicii cu valoare adăugată.</span><span class="sxs-lookup"><span data-stu-id="e5a04-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="e5a04-107">Cheltuielile și consumul asociate nu sunt urmărite în sarcinile unor proiecte conexe.</span><span class="sxs-lookup"><span data-stu-id="e5a04-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="e5a04-108">Liniile bazate pe produse pot fi articole din catalog sau produse înscrise.</span><span class="sxs-lookup"><span data-stu-id="e5a04-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="e5a04-109">Cea mai mare parte a funcționalității pe liniile bazate pe produse ale unei oportunități urmează funcționalitatea oferită de aplicația Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e5a04-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="e5a04-110">Pentru mai multe informații despre liniile de oportunitate bazate pe produse, consultați [Adăugați produse la o oportunitate](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="e5a04-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="e5a04-111">Un concept despre liniile de oportunități bazate pe produse, care este specific oportunităților bazate pe proiecte, este **Bugetul clientului**.</span><span class="sxs-lookup"><span data-stu-id="e5a04-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="e5a04-112">Utilizați acest câmp pentru a urmări suma pe care clientul este dispus să o plătească pentru elementul rând.</span><span class="sxs-lookup"><span data-stu-id="e5a04-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="e5a04-113">Dacă metoda veniturilor din rezumatul Opportunity este setată la **Calculat de sistem**, valorile bugetului clienților pe linii bazate pe produse și proiecte sunt rezumate pentru a calcula veniturile estimate.</span><span class="sxs-lookup"><span data-stu-id="e5a04-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
