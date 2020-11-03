---
title: Configurarea integrării Project Operations per entitate juridică
description: Acest subiect furnizează informații despre configurarea integrării după entitatea juridică în Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096767"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="215e0-103">Configurarea integrării Project Operations per entitate juridică</span><span class="sxs-lookup"><span data-stu-id="215e0-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="215e0-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="215e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="215e0-105">Acest subiect vă prezintă pașii necesari pentru configurarea Dynamics 365 Project Operations pe entitate juridică.</span><span class="sxs-lookup"><span data-stu-id="215e0-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="215e0-106">Activați tastele de caracteristică în Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="215e0-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="215e0-107">Parcurgeți pașii următori pentru a activa funcțiile necesare.</span><span class="sxs-lookup"><span data-stu-id="215e0-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="215e0-108">În Dynamics 365 Finance, accesați spațiul de lucru **Gestionarea caracteristicilor**.</span><span class="sxs-lookup"><span data-stu-id="215e0-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="215e0-109">În **Listă de caracteristici** , găsiți și activați următoarele caracteristici:</span><span class="sxs-lookup"><span data-stu-id="215e0-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="215e0-110">**Activați mai multe linii contractuale pentru un proiect**</span><span class="sxs-lookup"><span data-stu-id="215e0-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="215e0-111">**Activați Project Operations pe Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="215e0-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="215e0-112">Dacă nu vedeți **Taste funcționale** afișat, verificați dacă versiunea dvs. de finanțare îndeplinește cerința de versiune minimă (versiunea aplicației 10.0.13 cu toate actualizările de calitate aplicate sau mai mare).</span><span class="sxs-lookup"><span data-stu-id="215e0-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="215e0-113">Selectați **Verifică pentru actualizări** pentru a reîmprospăta lista de funcții.</span><span class="sxs-lookup"><span data-stu-id="215e0-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="215e0-114">Definiți scenariul de implementare a Project Operations pentru o entitate juridică</span><span class="sxs-lookup"><span data-stu-id="215e0-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="215e0-115">Puteți activa Project Operations pe Dynamics 365 Customer Engagement la un nivel de entitate juridică.</span><span class="sxs-lookup"><span data-stu-id="215e0-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="215e0-116">Puteți avea o singură persoană juridică folosind Project Operations pe Dynamics 365 Customer Engagement pentru resurse/scenarii bazate pe stoc.</span><span class="sxs-lookup"><span data-stu-id="215e0-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="215e0-117">În același mediu, puteți avea o altă entitate juridică care utilizează Project Operations pentru scenarii stocate/comandă de producție.</span><span class="sxs-lookup"><span data-stu-id="215e0-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="215e0-118">În Dynamics 365 Finance, accesați **Gestionarea proiectelor și contabilitate** > **Configurare** > **Gestionare globală de proiect și parametri de contabilitate**.</span><span class="sxs-lookup"><span data-stu-id="215e0-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="215e0-119">În lista persoanelor juridice disponibile, selectați entitățile în care sunt activate mai multe linii contractuale și Project Operations pe caracteristicile Dynamics 365 Customer Engagement vor fi activate.</span><span class="sxs-lookup"><span data-stu-id="215e0-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="215e0-120">Lăsați persoanele juridice care vor folosi Project Operations pentru scenarii stocate/comandă de producție neselectate.</span><span class="sxs-lookup"><span data-stu-id="215e0-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="215e0-121">O entitate juridică poate fi selectată numai dacă nu are proiecte existente.</span><span class="sxs-lookup"><span data-stu-id="215e0-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="215e0-122">Configurați Gestionarea proiectului și parametrii de contabilitate</span><span class="sxs-lookup"><span data-stu-id="215e0-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="215e0-123">Fiecare persoană juridică care folosește Project Operations pe Dynamics 365 Customer Engagement are nevoie de un set de parametri impliciti.</span><span class="sxs-lookup"><span data-stu-id="215e0-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="215e0-124">Acești parametri sunt configurați pe fila **Project Operations** de pe pagina **Managementul proiectului și parametrii contabili**.</span><span class="sxs-lookup"><span data-stu-id="215e0-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="215e0-125">Parametrii sunt:</span><span class="sxs-lookup"><span data-stu-id="215e0-125">The parameters are:</span></span>

  - <span data-ttu-id="215e0-126">**Tip implicit de facturare** : Project Operations utilizează un set fix de valori implicite de tip facturare care trebuie mapate la proprietățile liniei Finanțare.</span><span class="sxs-lookup"><span data-stu-id="215e0-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="215e0-127">Creați o înregistrare pentru fiecare tip de facturare: **Nespecificat** , **Taxabil** , **Netaxabil** , **Gratuit** , și **Nu e disponibil**.</span><span class="sxs-lookup"><span data-stu-id="215e0-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="215e0-128">**Categorii de proiecte implicite** : Selectați categoriile implicite de proiect care vor fi utilizate pentru fiecare tip de tranzacție.</span><span class="sxs-lookup"><span data-stu-id="215e0-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="215e0-129">Aceste valori implicite vor fi utilizate în **Jurnal de integrare a Project Operations** și în estimări în care nu este specificată nicio categorie de tranzacții pentru proiectul real.</span><span class="sxs-lookup"><span data-stu-id="215e0-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="215e0-130">**Prognoze** : Selectați modelul de prognoză care va fi utilizat pentru estimări de timp și cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="215e0-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
