---
title: Utilizați un câmp existent în Project Service ca dimensiune de tarifare
description: Acest subiect furnizează informații despre utilizarea câmpurilor Project Service existente ca dimensiuni de tarifare.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281583"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="246ca-103">Utilizați un câmp existent în Project Service ca dimensiune de tarifare</span><span class="sxs-lookup"><span data-stu-id="246ca-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="246ca-104">Project Service Automation (PSA) are multe câmpuri pe entitatea **Date reale**, care pot fi utilizate ca dimensiuni de tarifare pentru prețuri bazate pe resurse în organizațiile de proiect.</span><span class="sxs-lookup"><span data-stu-id="246ca-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="246ca-105">De exemplu, un câmp comun este **Resursă care se poate rezerva**.</span><span class="sxs-lookup"><span data-stu-id="246ca-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="246ca-106">Companiile mai mici, care au mai puțin de 20-30 de resurse facturabile pot descoperi că este o abordare mai simplă să aibă rate de facturare și de cost specifice pentru fiecare resursă.</span><span class="sxs-lookup"><span data-stu-id="246ca-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="246ca-107">Cu toate acestea, pe măsură ce forța de muncă care lucrează pe bază de onorarii crește, menținerea tarifelor specifice ar putea deveni nerealistă pe măsură ce costul resurselor și sumele facturilor încep să varieze pe măsură ce resursele sunt promovate, câștigă mai multă experiență sau dobândesc un alt set de abilități.</span><span class="sxs-lookup"><span data-stu-id="246ca-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="246ca-108">Deoarece această abordare funcționează în continuare pentru companii de o anumită dimensiune, consultați [Utilizați o resursă care poate fi rezervată ca dimensiune pentru stabilirea prețului](bookable-resource-pricing-dimension.md) pentru a înțelege modul în care un câmp existent în Project Service poate fi folosit ca dimensiune de stabilire a prețurilor.</span><span class="sxs-lookup"><span data-stu-id="246ca-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="246ca-109">Un alt exemplu este acela al categoriei de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="246ca-109">Another example is that of transaction category.</span></span> <span data-ttu-id="246ca-110">Clienții și Implementatorii au utilizat categoria de tranzacții în PSA pentru a clasifica munca și pentru a folosi câmpul pentru preț și cost pe baza categoriei de lucru.</span><span class="sxs-lookup"><span data-stu-id="246ca-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="246ca-111">Pentru mai multe informații, consultați [Utilizarea categoriei de tranzacții ca dimensiune de preț](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="246ca-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]