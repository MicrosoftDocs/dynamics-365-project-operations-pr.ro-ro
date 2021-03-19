---
title: Tipuri de perioade
description: Acest subiect oferă informații despre modul de configurare a tipurilor de perioadă pentru estimarea veniturilor.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287298"
---
# <a name="period-types"></a><span data-ttu-id="f0e96-103">Tipuri de perioade</span><span class="sxs-lookup"><span data-stu-id="f0e96-103">Period types</span></span>

<span data-ttu-id="f0e96-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="f0e96-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f0e96-105">Un tip de perioadă definește frecvența cu care se estimează veniturile dintr-un proiect.</span><span class="sxs-lookup"><span data-stu-id="f0e96-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="f0e96-106">Acest subiect oferă informații despre modul de configurare a tipurilor de perioadă pentru estimarea veniturilor.</span><span class="sxs-lookup"><span data-stu-id="f0e96-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="f0e96-107">Crearea și lucrul cu tipuri de perioade</span><span class="sxs-lookup"><span data-stu-id="f0e96-107">Create and work with period types</span></span>
<span data-ttu-id="f0e96-108">Pentru a crea și a lucra cu tipuri de perioadă, parcurgeți următorii pași:</span><span class="sxs-lookup"><span data-stu-id="f0e96-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="f0e96-109">În mediul dvs. Dynamics 365 Finance, accesați **Management de proiect și contabilitate** > **Configurare** > **Estimări** > **Tipuri de perioade**.</span><span class="sxs-lookup"><span data-stu-id="f0e96-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="f0e96-110">Selectați **Nou** pentru a crea un nou tip de perioadă.</span><span class="sxs-lookup"><span data-stu-id="f0e96-110">Select **New** to create new period type.</span></span> <span data-ttu-id="f0e96-111">Introduceți un nume și descriere.</span><span class="sxs-lookup"><span data-stu-id="f0e96-111">Enter a name and description.</span></span>
3. <span data-ttu-id="f0e96-112">În câmpul **Frecvență**, selectați o valoare:</span><span class="sxs-lookup"><span data-stu-id="f0e96-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="f0e96-113">Dacă selectați **Săptămână**, **Bi-săptămânal**, **Semestrial**, **Lună**, **Zi**, **Sfert**, sau **An**, calendarul va fi folosit pentru a genera perioadele.</span><span class="sxs-lookup"><span data-stu-id="f0e96-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="f0e96-114">Dacă selectați **Perioada contabilă**, perioadele contabile din configurația contabilității generale vor fi utilizate pentru a genera perioade.</span><span class="sxs-lookup"><span data-stu-id="f0e96-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="f0e96-115">Dacă selectați **Nelimitat**, puteți specifica perioade personalizate.</span><span class="sxs-lookup"><span data-stu-id="f0e96-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="f0e96-116">Selectați înregistrarea tipului de perioadă și apoi selectați **Generați perioade** pentru a crea perioade pentru tipul perioadei.</span><span class="sxs-lookup"><span data-stu-id="f0e96-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="f0e96-117">Pe baza frecvenței de perioadă pe care ați selectat-o, este posibil să aveți opțiunea de a specifica o dată de începere sau numărul de perioade de generat.</span><span class="sxs-lookup"><span data-stu-id="f0e96-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="f0e96-118">Selectați **Perioade** pentru a revizui perioadele generate.</span><span class="sxs-lookup"><span data-stu-id="f0e96-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]