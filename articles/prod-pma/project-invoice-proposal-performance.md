---
title: Performanța propunerilor de facturi pentru proiect
description: Acest subiect oferă informații despre îmbunătățirile de performanță pentru propunerile de facturi ale proiectului.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269805"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="4dbd9-103">Performanța propunerilor de facturi pentru proiect</span><span class="sxs-lookup"><span data-stu-id="4dbd9-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dbd9-104">Când creați o nouă propunere de facturare, este posibil să întâmpinați probleme de performanță pe măsură ce crește numărul de proiecte și subproiecte.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="4dbd9-105">Pentru a îmbunătăți performanța, este disponibilă o caracteristică care reduce timpul necesar pentru crearea unei noi propuneri de facturare pentru tranzacțiile de proiect afișate.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4dbd9-106">Activați îmbunătățirea performanței propuenrilor de facturi pentru proiect</span><span class="sxs-lookup"><span data-stu-id="4dbd9-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4dbd9-107">Pentru a activa caracteristica de îmbunătățire a performanței propunerii de facturare a proiectului, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="4dbd9-108">Accesați **Managementul caracteristicilor** > **Toate**.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4dbd9-109">În lista de funcții, localizați **Îmbunătățirea performanței propunerii de factură a proiectului**.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4dbd9-110">Selectați **Activați acum**.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="4dbd9-111">Reîmprospătați browserul, apoi creați o nouă propunere de facturare.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="4dbd9-112">Dezactivați îmbunătățirea performanței propuenrilor de facturi pentru proiect</span><span class="sxs-lookup"><span data-stu-id="4dbd9-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="4dbd9-113">Terminați următorii pași pentru a dezactiva îmbunătățirea performanței propunerii de facturare a proiectului.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="4dbd9-114">Accesați **Managementul caracteristicilor** > **Toate**.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="4dbd9-115">În lista de funcții, localizați **Îmbunătățirea performanței propunerii de factură a proiectului**.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="4dbd9-116">Selectați **Dezactivare**.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="4dbd9-117">Reîmprospătați browserul.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="4dbd9-118">Performanța propunerilor de factură nu poate fi aplicată atunci când regulile de facturare sunt activate.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="4dbd9-119">În timpul procesului pe lot pentru a crea propuneri de facturare, numărul de sarcini secundare va împărți sarcinile la un număr maxim, pe baza numărului de contracte cu tranzacții facturabile, indiferent de ceea ce ați introdus.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="4dbd9-120">De exemplu, dacă introduceți **3** pentru numărul de subactivități pentru crearea de propuneri de facturi în lot și există doar două contracte cu tranzacții facturabile, sunt create doar două subactivități.</span><span class="sxs-lookup"><span data-stu-id="4dbd9-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
