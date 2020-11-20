---
title: Actualizarea costului estimat la finalizare
description: Acest subiect oferă informații despre actualizarea proiecției efortului asupra unui proiect.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127218"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="753be-103">Actualizarea costului estimat la finalizare</span><span class="sxs-lookup"><span data-stu-id="753be-103">Update estimate at completion</span></span>

<span data-ttu-id="753be-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="753be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="753be-105">Este un lucru obișnuit ca un manager de proiect să revizuiască estimările inițiale ale unei activități.</span><span class="sxs-lookup"><span data-stu-id="753be-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="753be-106">Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind starea actuală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="753be-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="753be-107">Cu toate acestea, nu recomandăm ca managerii de proiect să modifice numerele de referință, pentru că referința proiectului reprezintă sursa stabilită de adevăr pentru planificarea proiectului și estimarea de cost și toți participanții direct interesați ai proiectului s-au pus de acord în această privință.</span><span class="sxs-lookup"><span data-stu-id="753be-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="753be-108">Există două modalități prin care un manager de proiect poate reproiecta efortul asupra activităților:</span><span class="sxs-lookup"><span data-stu-id="753be-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="753be-109">Suprascrie estimarea implicită pentru a finaliza (ETC) cu o nouă estimare a efortului efectiv rămase pe activitate.</span><span class="sxs-lookup"><span data-stu-id="753be-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="753be-110">Suprascrie procentul progresului implicit cu o nouă estimare a progresului real asupra activității.</span><span class="sxs-lookup"><span data-stu-id="753be-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="753be-111">Fiecare dintre aceste abordări cauzează o recalculare a activității ETC, estimarea la realizare (EAC) și procentajul de progres, precum și varianța de efort proiectată pentru o activitate.</span><span class="sxs-lookup"><span data-stu-id="753be-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="753be-112">EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt recalculate, și produce o nouă proiecție a varianței efortului.</span><span class="sxs-lookup"><span data-stu-id="753be-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
