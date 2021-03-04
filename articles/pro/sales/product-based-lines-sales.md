---
title: Linii de contract bazate pe oportunitate - simplificat
description: Acest subiect furnizează informații despre elemente de linie de oportunitate pe bază de proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764969"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="e873d-103">Linii de contract bazate pe oportunitate - simplificat</span><span class="sxs-lookup"><span data-stu-id="e873d-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="e873d-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="e873d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e873d-105">Liniile de oportunitate bazate pe produse sunt elemente rând din Oportunitate.</span><span class="sxs-lookup"><span data-stu-id="e873d-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="e873d-106">Aceste elemente de rând distincte se află pe eventuala factură care este furnizată clientului.</span><span class="sxs-lookup"><span data-stu-id="e873d-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="e873d-107">Factura nu include alte servicii suplimentare.</span><span class="sxs-lookup"><span data-stu-id="e873d-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="e873d-108">Cheltuielile și consumul asociate nu sunt urmărite în sarcinile unor proiecte conexe.</span><span class="sxs-lookup"><span data-stu-id="e873d-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="e873d-109">Liniile bazate pe produse pot fi articole din catalog sau produse înscrise.</span><span class="sxs-lookup"><span data-stu-id="e873d-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="e873d-110">Cea mai mare parte a funcționalității pe liniile bazate pe produse ale unei oportunități urmează funcționalitatea oferită de aplicația Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e873d-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="e873d-111">Pentru mai multe informații despre liniile de oportunitate bazate pe produse, consultați [Adăugați produse la o oportunitate](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="e873d-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="e873d-112">**Bugetul clientului** este un concept specific rândurilor de oportunități bazate pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="e873d-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="e873d-113">Câmpul **Bugetul clientului** urmărește suma pe care clientul este dispus să o plătească pentru un articol.</span><span class="sxs-lookup"><span data-stu-id="e873d-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="e873d-114">Când metoda veniturilor din rezumatul de oportunității este **Calculată de sistem**, valorile bugetului pentru un client de-a lungul liniilor de oportunitate sunt sintetizate pentru a calcula venitul estimat.</span><span class="sxs-lookup"><span data-stu-id="e873d-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

