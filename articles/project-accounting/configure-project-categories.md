---
title: Configurarea categoriilor de proiecte
description: Acest subiect furnizează informații despre configurarea categoriilor de proiect.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995186"
---
# <a name="configure-project-categories"></a><span data-ttu-id="03120-103">Configurarea categoriilor de proiecte</span><span class="sxs-lookup"><span data-stu-id="03120-103">Configure project categories</span></span>

<span data-ttu-id="03120-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="03120-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="03120-105">Operațiunile de proiect oferă capabilități solide pentru clasificarea veniturilor și cheltuielilor pe proiecte.</span><span class="sxs-lookup"><span data-stu-id="03120-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="03120-106">Categoriile oferă posibilitatea de a raporta și analiza tranzacțiile proiectului și de a conduce postarea în registrul general.</span><span class="sxs-lookup"><span data-stu-id="03120-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="03120-107">Următoarea diagramă ilustrează corelația dintre categoriile de tranzacții, categoriile partajate și categoriile de proiecte.</span><span class="sxs-lookup"><span data-stu-id="03120-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="03120-108">Categoriile de tranzacții sunt gruparea de bază pentru tranzacțiile proiectului.</span><span class="sxs-lookup"><span data-stu-id="03120-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="03120-109">În cadrul grupării respective, există un set de categorii partajate care pot fi partajate între aplicații și module.</span><span class="sxs-lookup"><span data-stu-id="03120-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="03120-110">Intrând și mai în detaliu, categoriile de proiecte sunt cel mai granular nivel de categorii.</span><span class="sxs-lookup"><span data-stu-id="03120-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="03120-111">Categoriile de proiecte sunt specifice entității juridice, modulului și aplicației.</span><span class="sxs-lookup"><span data-stu-id="03120-111">Project categories are specific to legal entity, module, and application.</span></span>

![Corelația dintre categoriile de tranzacții, categoriile partajate și categoriile de proiecte](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="03120-113">Categorii de tranzacții</span><span class="sxs-lookup"><span data-stu-id="03120-113">Transaction categories</span></span>

<span data-ttu-id="03120-114">Categoriile de tranzacții reprezintă gruparea de bază pentru tranzacțiile proiectului și nu sunt specifice companiei sau tipului de tranzacție.</span><span class="sxs-lookup"><span data-stu-id="03120-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="03120-115">De exemplu, Contoso Robotics utilizează categoriile de proiectare, călătorie, instalare și tranzacții de servicii pentru a grupa tranzacțiile proiectului.</span><span class="sxs-lookup"><span data-stu-id="03120-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="03120-116">Categoriile de tranzacții sunt definite în modulul Project Operations.</span><span class="sxs-lookup"><span data-stu-id="03120-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="03120-117">Accesați **Setări** \> **Categorii de tranzacții** pentru a deschide formularul.</span><span class="sxs-lookup"><span data-stu-id="03120-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="03120-118">Creați o nouă categorie de tranzacții fie selectând **Nou** sau selectând **Importați din Excel**.</span><span class="sxs-lookup"><span data-stu-id="03120-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="03120-119">Categorii partajate</span><span class="sxs-lookup"><span data-stu-id="03120-119">Shared categories</span></span>

<span data-ttu-id="03120-120">Dynamics 365 folosește conceptul de categorii partajate pentru a clasifica cheltuielile în diferite aplicații, cum ar fi Dynamics 365 Finance, Dynamics 365 Supply Chain și Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="03120-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="03120-121">Pentru fiecare categorie de tranzacții creată, Project Operationst creează automat patru categorii comune partajate: Ore, Cheltuieli, Taxe și Articol.</span><span class="sxs-lookup"><span data-stu-id="03120-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="03120-122">Puteți examina și ajusta categoriile partajate accesând **Management de proiect și contabilitate** \> **Configurare** \> **Categorii** \> **Categorii partajate**.</span><span class="sxs-lookup"><span data-stu-id="03120-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="03120-123">Categorii de proiecte</span><span class="sxs-lookup"><span data-stu-id="03120-123">Project categories</span></span>

<span data-ttu-id="03120-124">Categoriile de proiecte reprezintă cel mai granular nivel de configurare a categoriilor și trebuie configurate separat și pentru fiecare companie, de către un contabil de proiect.</span><span class="sxs-lookup"><span data-stu-id="03120-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="03120-125">Accesați **Management de proiect și contabilitate** \> **Configurare** \> **Categorii** \> **Categorii de proiecte**.</span><span class="sxs-lookup"><span data-stu-id="03120-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="03120-126">Selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="03120-126">Select **New**.</span></span>
3. <span data-ttu-id="03120-127">Selectați **ID categorie** din categoria partajat pe care ați creat-o în secțiunea anterioară.</span><span class="sxs-lookup"><span data-stu-id="03120-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="03120-128">Project Operations permit utilizarea numai a acelor categorii partajate care sunt asociate cu categoriile de tranzacții.</span><span class="sxs-lookup"><span data-stu-id="03120-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="03120-129">Selectați un grup de categorii.</span><span class="sxs-lookup"><span data-stu-id="03120-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="03120-130">Grupuri de categorie</span><span class="sxs-lookup"><span data-stu-id="03120-130">Category groups</span></span>

<span data-ttu-id="03120-131">Grupurile de categorii sunt folosite pentru a partaja proprietăți, în principal postarea profilurilor, între categoriile de proiecte conexe.</span><span class="sxs-lookup"><span data-stu-id="03120-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="03120-132">Trebuie să existe cel puțin un grup de categorii pentru fiecare tip de tranzacție și fiecărei categorii de proiect i se atribuie un grup.</span><span class="sxs-lookup"><span data-stu-id="03120-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="03120-133">Specificațiile de înregistrare din Project Operations sunt definite de regulile profilului de cost și de venit al proiectului, categoriile de proiecte și grupurile de categorii.</span><span class="sxs-lookup"><span data-stu-id="03120-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="03120-134">Puteți configura grupuri de categorii accesând **Management de proiect și contabilitate** \> **Configurare** \> **Categorii** \> **Grupuri de categorii**.</span><span class="sxs-lookup"><span data-stu-id="03120-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]