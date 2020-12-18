---
title: Proiecte cu estimarea veniturilor cu preț fix
description: Acest subiect furnizează informații despre veniturilro la preț fix în proiecte.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531528"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="52bbe-103">Proiecte cu estimarea veniturilor cu preț fix</span><span class="sxs-lookup"><span data-stu-id="52bbe-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="52bbe-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="52bbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="52bbe-105">Când creați o linie de contract de proiect cu următoarele atribute în Dynamics 365 Project Operations pe Microsoft Dataverse, sistemul creează automat un proiect de estimare a venitului la preț fix.</span><span class="sxs-lookup"><span data-stu-id="52bbe-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="52bbe-106">Informațiile din acest proiect se bazează pe următoarele:</span><span class="sxs-lookup"><span data-stu-id="52bbe-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="52bbe-107">O metodă de facturare cu preț fix.</span><span class="sxs-lookup"><span data-stu-id="52bbe-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="52bbe-108">Un proiect asociat.</span><span class="sxs-lookup"><span data-stu-id="52bbe-108">An associated project.</span></span>
  - <span data-ttu-id="52bbe-109">Cel puțin o etapă definită pe fila **Planificarea facturilor** de pe pagina **Linia contractului de proiect**.</span><span class="sxs-lookup"><span data-stu-id="52bbe-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="52bbe-110">Revizuiți proiecte cu estimarea veniturilor cu preț fix</span><span class="sxs-lookup"><span data-stu-id="52bbe-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="52bbe-111">Pentru a revizui proiectele de estimare a veniturilor cu preț fix, parcurgeți următorii pași:</span><span class="sxs-lookup"><span data-stu-id="52bbe-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="52bbe-112">În mediul Dynamics 365 Finance, accesați **Managementul proiectelor și contabilitate** > **Proiecte** > **Proiecte de estimare a veniturilor cu preț fix**.</span><span class="sxs-lookup"><span data-stu-id="52bbe-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="52bbe-113">Selectați proiectul pe care doriți să îl vizualizați și faceți dublu clic pe **Estimarea ID-ului proiectului** pentru a deschide înregistrarea și a revizui detaliile proiectului.</span><span class="sxs-lookup"><span data-stu-id="52bbe-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="52bbe-114">Extindeți fila **Proiect**. Veți vedea un proiect în grila **Proiecte selectate**.</span><span class="sxs-lookup"><span data-stu-id="52bbe-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="52bbe-115">Sistemul îl folosește ca proiect implicit, deoarece este proiectul asociat liniei contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="52bbe-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="52bbe-116">Pentru a schimba asocierea, selectați proiecte suplimentare și adăugați-le la grila **Proiecte selectate**.</span><span class="sxs-lookup"><span data-stu-id="52bbe-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="52bbe-117">Dacă sunt selectate mai multe proiecte în această grilă, finalizarea procentuală a proiectului și estimările veniturilor sunt calculate împreună pentru toate proiectele selectate.</span><span class="sxs-lookup"><span data-stu-id="52bbe-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="52bbe-118">Costul proiectului, profilul veniturilor, șablonul de cost și codul perioadei pot fi setate manual.</span><span class="sxs-lookup"><span data-stu-id="52bbe-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="52bbe-119">Dacă nu sunt setate manual, valorile sunt implicite în timpul primului calcul estimativ pentru proiect utilizând regulile configurate pentru profilurile de cost și venituri ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="52bbe-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

