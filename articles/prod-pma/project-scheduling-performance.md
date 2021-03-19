---
title: Performanța planificării resurselor proiectului
description: Acest subiect oferă informații despre cum să îmbunătățim performanța planificării resurselor pentru un număr mare de proiecte.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289024"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="12f35-103">Performanța planificării resurselor proiectului</span><span class="sxs-lookup"><span data-stu-id="12f35-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="12f35-104">Probleme de performanță legate de programarea resurselor pot apărea atunci când numărul proiectelor ajunge la mii.</span><span class="sxs-lookup"><span data-stu-id="12f35-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="12f35-105">Pentru a îmbunătăți performanța de planificare a resurselor, este disponibilă o caracteristică care permite utilizatorilor să reducă timpul necesar lansării formularului de disponibilitate a resurselor.</span><span class="sxs-lookup"><span data-stu-id="12f35-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="12f35-106">În mod specific, acest lucru elimină procesul de sincronizare a acumulării capacității resurselor și utilizează tabelul **ResProjectResource** tabel pentru a accelera căutarea resurselor.</span><span class="sxs-lookup"><span data-stu-id="12f35-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="12f35-107">Rețineți că tabelul **ResRollup** nu va mai fi folosit.</span><span class="sxs-lookup"><span data-stu-id="12f35-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12f35-108">Dacă există o dependență fie de procesul de sincronizare de acumulare a capacității resurselor, sau tableul **ResProjectResource**, nu utilizați această caracteristică.</span><span class="sxs-lookup"><span data-stu-id="12f35-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="12f35-109">Activați îmbunătățirea performanței planificării resurselor</span><span class="sxs-lookup"><span data-stu-id="12f35-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="12f35-110">Pentru a activa îmbunătățirea performanței planificării resurselor, parcurgeți pașii următori.</span><span class="sxs-lookup"><span data-stu-id="12f35-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="12f35-111">Accesați **Managementul caracteristicilor** > **Toate**, și în lista de caracteristici, găsiți **Activați caracteristica de îmbunătățire a performanței de planificare a resurselor proiectului**.</span><span class="sxs-lookup"><span data-stu-id="12f35-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="12f35-112">Selectați **Activați acum**.</span><span class="sxs-lookup"><span data-stu-id="12f35-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="12f35-113">Dacă nu puteți găsi caracteristica în listă, selectați **Verificați actualizări** pentru a reîmprospăta lista.</span><span class="sxs-lookup"><span data-stu-id="12f35-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="12f35-114">Reîmprospătați browserul, apoi accesați **Management de proiect și contabilitate** > **Periodic** > **Resursele proiectului** > **Sincronizați capacitatea calendarelor de resurse în toate companiile**.</span><span class="sxs-lookup"><span data-stu-id="12f35-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="12f35-115">Setați **Eliminați înregistrările de capacitate existente** la **Da** pentru a elimina datele anterioare.</span><span class="sxs-lookup"><span data-stu-id="12f35-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="12f35-116">Dacă doriți să generați date incrementale, setați-le la **Nu**.</span><span class="sxs-lookup"><span data-stu-id="12f35-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="12f35-117">În câmpul **Codul perioadei**, selectați perioada în care ar trebui generate datele.</span><span class="sxs-lookup"><span data-stu-id="12f35-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="12f35-118">Dacă selectați un cod de perioadă, nu este necesară definirea unei date de începere și de încheiere.</span><span class="sxs-lookup"><span data-stu-id="12f35-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="12f35-119">Dacă lăsați câmpul **Codul perioadei** necompletat, selectați anumite date de început și sfârșit pentru a genera date.</span><span class="sxs-lookup"><span data-stu-id="12f35-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="12f35-120">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="12f35-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="12f35-121">Aceasta va distribui date generale către tabelul **ResCalendarCapacity** pentru toate companiile din mediul dvs., astfel încât jobul lot trebuie executat doar într-o singură persoană juridică.</span><span class="sxs-lookup"><span data-stu-id="12f35-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="12f35-122">Datele din această operațiune de lot sunt necesare pentru a calcula capacitatea resurselor prin calendarul asociat.</span><span class="sxs-lookup"><span data-stu-id="12f35-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="12f35-123">Accesați **Management de proiect și contabilitate** > **Periodic** > **Resursele proiectului** > **Populați resursele proiectului în toate companiile** și apoi selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="12f35-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="12f35-124">Acesta este scriptul de actualizare a datelor pentru date generale din tabelele **ResProjectResource**, **ResCalendarDateTimeRange**, și **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="12f35-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="12f35-125">Valori pentru câmpul **PSAPRojSchedRole.RootActivity** sunt de asemenea actualizate.</span><span class="sxs-lookup"><span data-stu-id="12f35-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="12f35-126">Dacă acest lucru nu este executat, veți primi un avertisment atunci când încercați să executați operațiuni de planificare a resurselor.</span><span class="sxs-lookup"><span data-stu-id="12f35-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="12f35-127">Dezactivați îmbunătățirea performanței planificării resurselor</span><span class="sxs-lookup"><span data-stu-id="12f35-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="12f35-128">Accesați **Managementul caracteristicilor** > **Toate**, și căutați **Activați caracteristica de îmbunătățire a performanței de planificare a resurselor proiectului**.</span><span class="sxs-lookup"><span data-stu-id="12f35-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="12f35-129">Selectați caracteristica, apoi selectați butonul **Dezactivare**.</span><span class="sxs-lookup"><span data-stu-id="12f35-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="12f35-130">Reîmprospătați browserul.</span><span class="sxs-lookup"><span data-stu-id="12f35-130">Refresh your browser.</span></span>
4. <span data-ttu-id="12f35-131">Accesați **Management de proiect și contabilitate** > **Periodic** > **Sincronizare de capacitate** > **Cumulare sincronizare resurse de capacitate**.</span><span class="sxs-lookup"><span data-stu-id="12f35-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="12f35-132">Pe pagina **Sincronizare de acumulare a capacității** configurați **Eliminați înregistrările de capacitate existente** la **Da** pentru a elimina datele anterioare.</span><span class="sxs-lookup"><span data-stu-id="12f35-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="12f35-133">Dacă doriți să generați date incrementale, configurați la **Nu**.</span><span class="sxs-lookup"><span data-stu-id="12f35-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="12f35-134">În câmpul **Codul perioadei**, selectați perioada în care ar trebui generate datele.</span><span class="sxs-lookup"><span data-stu-id="12f35-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="12f35-135">Dacă selectați un cod de perioadă, nu este necesară definirea unei date de începere și de încheiere.</span><span class="sxs-lookup"><span data-stu-id="12f35-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="12f35-136">Dacă lăsați câmpul **Codul perioadei** necompletat, selectați anumite date de început și sfârșit pentru a genera date.</span><span class="sxs-lookup"><span data-stu-id="12f35-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="12f35-137">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="12f35-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="12f35-138">Aceasta va distribui date generale către tabelul **ResRollup** pentru toate companiile din mediul dvs., astfel încât operațiunea de lot trebuie executată doar într-o singură persoană juridică.</span><span class="sxs-lookup"><span data-stu-id="12f35-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="12f35-139">Această operațiune de lot este necesară pentru toate vizualizările **Disponibilitatea resurselor**.</span><span class="sxs-lookup"><span data-stu-id="12f35-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="12f35-140">Dacă această operațiune de lot nu este rulată, **ResRollup** datele vor fi generate din mers, ceea ce poate dura timp.</span><span class="sxs-lookup"><span data-stu-id="12f35-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]