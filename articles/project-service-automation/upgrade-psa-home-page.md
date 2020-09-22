---
title: Actualizare pagină de pornire
description: Acest subiect arată unde se găsesc informații importante despre caracteristicile noi și modificate din Dynamics 365 Project Service Automation, precum și procesul de upgrade la cea mai nouă versiune.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754781"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="31fe5-103">Actualizare pagină de pornire</span><span class="sxs-lookup"><span data-stu-id="31fe5-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="31fe5-104">Faceți upgrade de la PSA versiunea 2.x sau 1.x la versiunea 3.x</span><span class="sxs-lookup"><span data-stu-id="31fe5-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="31fe5-105">Instanțe noi</span><span class="sxs-lookup"><span data-stu-id="31fe5-105">New instances</span></span>

<span data-ttu-id="31fe5-106">Începând cu 17 mai 2019, la selectarea Project Service Automation în timpul asigurării accesului unei instanțe noi, versiunea 3.x este instalată în mod implicit.</span><span class="sxs-lookup"><span data-stu-id="31fe5-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="31fe5-107">Instanțe existente</span><span class="sxs-lookup"><span data-stu-id="31fe5-107">Existing instances</span></span>

<span data-ttu-id="31fe5-108">Anterior, clienții care au o instanță de PSA versiunea 2.x și trebuiau să facă upgrade la versiunea 3.x, care este versiunea unificată bazată pe interfață client (UCI) de PSA, trebuiau să contacteze Asistența Microsoft și să furnizeze detaliile instanței lor astfel încât serviciul de asistență să poată activa instanța pentru upgrade la versiunea 3.x.</span><span class="sxs-lookup"><span data-stu-id="31fe5-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="31fe5-109">Începând cu 1 martie 2020, clienții care au o instanță a PSA versiunea 2.x și au nevoie să facă upgrade la versiunea 3.x, vor putea să își actualizeze instanțele direct din portalul de administrare, fără să fie nevoiți să contacteze Asistența Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31fe5-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="31fe5-110">PSA versiunea 3.x include modificări semnificative.</span><span class="sxs-lookup"><span data-stu-id="31fe5-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="31fe5-111">Acesta a fost construit pe cadrul de Interfață unificată pentru a ajuta la furnizarea unei experiențe de utilizator îmbunătățite.</span><span class="sxs-lookup"><span data-stu-id="31fe5-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="31fe5-112">Aplicația reproiectată oferă o interfață de utilizator (UI) consecventă, uniformă și respectă principiile de proiectare adaptabile pentru vizualizarea optimă pe orice dimensiune de ecran sau dispozitiv.</span><span class="sxs-lookup"><span data-stu-id="31fe5-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="31fe5-113">Au existat și alte modificări în cadrul aplicației.</span><span class="sxs-lookup"><span data-stu-id="31fe5-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="31fe5-114">Unele dintre zonele care au fost schimbate includ stabilirea prețurilor, rezervarea și alocarea resurselor, a timpului, a cheltuielilor și a aprobărilor.</span><span class="sxs-lookup"><span data-stu-id="31fe5-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="31fe5-115">Înainte de a începe procesul de actualizare, vă recomandăm să completați următoarele activități:</span><span class="sxs-lookup"><span data-stu-id="31fe5-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="31fe5-116">Verificați dacă pe instanța identificată sunt instalate atât Dynamics 365 Field Service, cât și Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="31fe5-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="31fe5-117">Dacă ambele soluții sunt instalate, trebuie să planificați să le actualizați pe amândouă înainte de a relua utilizarea regulată a instanței.</span><span class="sxs-lookup"><span data-stu-id="31fe5-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="31fe5-118">Examinați cu atenție următoarele subiecte.</span><span class="sxs-lookup"><span data-stu-id="31fe5-118">Carefully review the following topics.</span></span> <span data-ttu-id="31fe5-119">Conștientizarea și înțelegerea modificărilor dintre versiuni vă vor ajuta cu procesul de actualizare.</span><span class="sxs-lookup"><span data-stu-id="31fe5-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="31fe5-120">Aceste subiecte oferă informații despre schimbările majore în PSA, împreună cu considerente și recomandări pentru planificarea actualizării la versiunea 3.x.</span><span class="sxs-lookup"><span data-stu-id="31fe5-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="31fe5-121">Ce este nou sau modificat în Project Service Automation versiunea 3</span><span class="sxs-lookup"><span data-stu-id="31fe5-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="31fe5-122">Considerente legate de upgrade - Project Service Automation versiunea 2.x sau 1.x până la versiunea 3</span><span class="sxs-lookup"><span data-stu-id="31fe5-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="31fe5-123">Actualizați-vă instanța sandbox pentru a evalua modificările din implementare înainte de a vă actualiza instanța de producție.</span><span class="sxs-lookup"><span data-stu-id="31fe5-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="31fe5-124">După ce ați revizuit subiectele care au fost menționate mai sus și sunteți gata să actualizați la PSA versiunea 3.x sau versiunea bazată pe UCI, trimiteți o solicitare de asistență Microsoft pentru a face actualizarea disponibilă din centrul de administrare.</span><span class="sxs-lookup"><span data-stu-id="31fe5-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="31fe5-125">În cererea dumneavoastră, furnizați detaliile instanței dvs.</span><span class="sxs-lookup"><span data-stu-id="31fe5-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="31fe5-126">Versiuni mai vechi de PSA (PSA versiunea 2.x) într-o instanță nou creată</span><span class="sxs-lookup"><span data-stu-id="31fe5-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="31fe5-127">De la 17 mai 2019, toate instanțele noi vor avea UCI ca client implicit.</span><span class="sxs-lookup"><span data-stu-id="31fe5-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="31fe5-128">Pentru alinierea cu această modificare, se va furniza implicit accesul pentru PSA versiunea 3.x și Field Service versiunea 8.x, deoarece aceste versiuni sunt proiectate să funcționeze cu clientul UCI.</span><span class="sxs-lookup"><span data-stu-id="31fe5-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="31fe5-129">Începând cu 1 martie 2020, clienții Dynamics PSA nu vor mai putea crea medii noi cu versiuni mai vechi de PSA, de exemplu versiunea PSA 2.x sau mai veche.</span><span class="sxs-lookup"><span data-stu-id="31fe5-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="31fe5-130">Orice nou mediu va avea doar versiunea 3.x a PSA.</span><span class="sxs-lookup"><span data-stu-id="31fe5-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="31fe5-131">Pentru cea mai bună experiență când utilizați versiunile mai vechi ale Field Service și ale aplicațiilor PSA, accesați pagina **Setări sistem** și, la câmpul **Utilizați numai noua Interfață unificată (recomandat)**, selectați **Nu**, deoarece aceste versiuni nu sunt proiectate să se încarce corect în UCI.</span><span class="sxs-lookup"><span data-stu-id="31fe5-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="31fe5-132">După ce ați dezactivat UCI, aveți posibilitatea să deschideți și să executați aceste versiuni de Field Service și PSA utilizând vechiul client web.</span><span class="sxs-lookup"><span data-stu-id="31fe5-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> <span data-ttu-id="31fe5-133">Pentru instrucțiuni despre cum se dezactivează clientul UCI, consultați [Activați numai Interfață unificată](../admin/enable-unified-interface-only.md).</span><span class="sxs-lookup"><span data-stu-id="31fe5-133">For instructions about how to turn off the UCI client, see [Enable unified interface only](../admin/enable-unified-interface-only.md).</span></span>
