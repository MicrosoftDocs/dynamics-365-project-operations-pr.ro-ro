---
title: Configurarea tarifelor de cost și de vânzare pentru produsele din catalog - simplificat
description: Acest subiect oferă informații despre modul de configurare al ratei de cost și vânzări pentru elemente dintr-un catalog de produse.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004350"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="b0021-103">Configurarea tarifelor de cost și de vânzare pentru produsele din catalog - simplificat</span><span class="sxs-lookup"><span data-stu-id="b0021-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="b0021-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="b0021-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b0021-105">Configurarea prețurilor pentru articolele din catalogul de produse în Dynamics 365 Project Operations este la fel ca în Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b0021-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b0021-106">În Project Operations, produsele nu pot fi estimate sau utilizate în proiecte, astfel încât prețurile din catalogul de produse nu trebuie să fie stabilite pe listele de prețuri ale proiectelor pentru oferte și contracte.</span><span class="sxs-lookup"><span data-stu-id="b0021-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b0021-107">Utilizați câmpul **Prețul produsului** al unei oferte, al unui contract sau al unui cont pentru a stabili prețurile din catalogul de produse.</span><span class="sxs-lookup"><span data-stu-id="b0021-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="b0021-108">Nu setați prețurile din catalogul de produse în listele de prețuri ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="b0021-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="b0021-109">Listele de prețuri ale proiectului sunt exclusive pentru Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b0021-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b0021-110">Logica de afaceri specifică aplicației copiază listele de preț dintr-o ofertă într-un contract.</span><span class="sxs-lookup"><span data-stu-id="b0021-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b0021-111">Rezultatul este o listă de prețuri de proiect specifică pentru un contract.</span><span class="sxs-lookup"><span data-stu-id="b0021-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b0021-112">Operația de copiere poate întârzia procesul de câștigare a ofertei dacă lista de prețuri a proiectului din ofertă devine prea mare.</span><span class="sxs-lookup"><span data-stu-id="b0021-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b0021-113">Listele de prețuri ale produselor nu sunt copiate pentru a crea liste de prețuri personalizate în contracte.</span><span class="sxs-lookup"><span data-stu-id="b0021-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b0021-114">Deoarece nu este implicată nicio operație de copiere, performanța procesului de ofertare nu este afectată.</span><span class="sxs-lookup"><span data-stu-id="b0021-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]