---
title: Utilizați un câmp existent în Project Service ca dimensiune de tarifare
description: Acest subiect furnizează informații despre utilizarea câmpurilor Project Service existente ca dimensiuni de tarifare.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754752"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="158b0-103">Utilizați un câmp existent în Project Service ca dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="158b0-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="158b0-104">Project Service Automation (PSA) are multe câmpuri pe entitatea **Date reale**, care pot fi utilizate ca dimensiuni de tarifare pentru prețuri bazate pe resurse în organizațiile de proiect.</span><span class="sxs-lookup"><span data-stu-id="158b0-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="158b0-105">De exemplu, un câmp comun este **Resursă care se poate rezerva**.</span><span class="sxs-lookup"><span data-stu-id="158b0-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="158b0-106">Companiile mai mici, care au mai puțin de 20-30 de resurse facturabile pot descoperi că este o abordare mai simplă să aibă rate de facturare și de cost specifice pentru fiecare resursă.</span><span class="sxs-lookup"><span data-stu-id="158b0-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="158b0-107">Cu toate acestea, pe măsură ce forța de muncă facturabilă crește, acest lucru ar putea deveni nerealist de susținut, deoarece ratele de cost de facturare ale resurselor încep să varieze pe măsură ce resursele sunt promovate, capătă mai multă experiență sau dobândesc un set de abilități diferite.</span><span class="sxs-lookup"><span data-stu-id="158b0-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="158b0-108">Deoarece această abordare încă funcționează pentru companii de o anumită dimensiune, consultați subiectul, [Utilizarea unei resurse care poate fi rezervată ca dimensiune de preț](bookable-resource-pricing-dimension.md) pentru a înțelege cum poate fi utilizat un câmp Project Service existent ca dimensiune de preț.</span><span class="sxs-lookup"><span data-stu-id="158b0-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="158b0-109">Un alt exemplu este acela al categoriei de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="158b0-109">Another example is that of transaction category.</span></span> <span data-ttu-id="158b0-110">Clienții și Implementatorii au utilizat categoria de tranzacții în PSA pentru a clasifica munca și pentru a folosi câmpul pentru preț și cost pe baza categoriei de lucru.</span><span class="sxs-lookup"><span data-stu-id="158b0-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="158b0-111">Pentru mai multe informații, consultați [Utilizarea categoriei de tranzacții ca dimensiune de preț](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="158b0-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
