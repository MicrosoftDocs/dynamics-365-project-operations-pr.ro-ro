---
title: Configurarea tarifelor de cost și de vânzare pentru produsele din catalog
description: Acest subiect oferă informații despre modul de configurare al ratei de cost și vânzări pentru elemente dintr-un catalog de produse.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082863"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="f8e60-103">Configurarea tarifelor de cost și de vânzare pentru produsele din catalog</span><span class="sxs-lookup"><span data-stu-id="f8e60-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="f8e60-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="f8e60-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f8e60-105">Configurarea prețurilor pentru articolele din catalogul de produse în Dynamics 365 Project Operations este aceeași ca în Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f8e60-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="f8e60-106">Deoarece produsele nu pot fi estimate sau utilizate în proiecte în Project Operations, nu este necesar să stabiliți prețurile din catalogul de produse pe listele de prețuri ale proiectelor pentru ofertele și contractele.</span><span class="sxs-lookup"><span data-stu-id="f8e60-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="f8e60-107">Prețurile din catalogul de produse trebuie stabilite în câmpul **Prețul produsului** al unei cotații, a unui contract sau a unui cont.</span><span class="sxs-lookup"><span data-stu-id="f8e60-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="f8e60-108">Nu setați prețurile din catalogul de produse în listele de prețuri ale proiectului pentru aceste entități.</span><span class="sxs-lookup"><span data-stu-id="f8e60-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="f8e60-109">Listele de prețuri ale proiectului sunt exclusive pentru Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f8e60-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="f8e60-110">Există o logică de afaceri specifică aplicației care copiază listele de preț dintr-o ofertă într-un contract.</span><span class="sxs-lookup"><span data-stu-id="f8e60-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="f8e60-111">Rezultatul este o listă de prețuri de proiect specifică pentru un contract.</span><span class="sxs-lookup"><span data-stu-id="f8e60-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="f8e60-112">Operația de copiere poate întârzia procesul de câștigare a ofertei dacă lista de prețuri a proiectului din ofertă devine prea mare.</span><span class="sxs-lookup"><span data-stu-id="f8e60-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="f8e60-113">Listele de prețuri ale produselor nu sunt copiate pentru a crea liste de prețuri personalizate în contracte.</span><span class="sxs-lookup"><span data-stu-id="f8e60-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="f8e60-114">Aceasta înseamnă că listele de prețuri ale produselor nu au impact asupra performanței procesului de câștigare a ofertelor.</span><span class="sxs-lookup"><span data-stu-id="f8e60-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
