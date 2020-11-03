---
title: Sincronizarea capacității resurselor
description: Acest subiect oferă informații despre cum să sincronizați capacitatea unei resurse între calendare și proiecte.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082774"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="d9af3-103">Sincronizarea capacității resurselor</span><span class="sxs-lookup"><span data-stu-id="d9af3-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9af3-104">Procesele de sincronizare a resurselor contribuie la garantarea faptului că informațiile pentru calendar și calendarul de bază se transferă în planificarea resurselor proiectului.</span><span class="sxs-lookup"><span data-stu-id="d9af3-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="d9af3-105">Când calendarul este modificat, procesele fac actualizările necesare pentru planificarea resurselor proiectului.</span><span class="sxs-lookup"><span data-stu-id="d9af3-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="d9af3-106">Procesele contribuie, de asemenea, la îmbunătățirea performanței, deoarece informațiile despre resurse ale calendarului sunt sincronizate în avans.</span><span class="sxs-lookup"><span data-stu-id="d9af3-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="d9af3-107">Prin urmare, actualizările informațiilor de planificare a resurselor apar mai rapid.</span><span class="sxs-lookup"><span data-stu-id="d9af3-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="d9af3-108">Vă recomandăm să planificați procesele ca un lot în loc de unul câte unul.</span><span class="sxs-lookup"><span data-stu-id="d9af3-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="d9af3-109">În caz contrar, există riscul ca cineva să uite datele inclusive în care informațiile au fost sincronizate ultima dată.</span><span class="sxs-lookup"><span data-stu-id="d9af3-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="d9af3-110">Dacă datele inclusive nu sunt utilizate, pot apărea lacune în timpul sincronizării datei.</span><span class="sxs-lookup"><span data-stu-id="d9af3-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronizare calendar](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="d9af3-112">Cumulări de sincronizare a capacității resursei</span><span class="sxs-lookup"><span data-stu-id="d9af3-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="d9af3-113">Procesul de sincronizare este conceput pentru a sincroniza toate informațiile din calendarul resurselor.</span><span class="sxs-lookup"><span data-stu-id="d9af3-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="d9af3-114">Aceste informații includ informații de bază despre calendar despre orice modificare a tabelului de capacitate a calendarului de resurse al proiectului.</span><span class="sxs-lookup"><span data-stu-id="d9af3-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="d9af3-115">Dacă în proiect sunt adăugate resurse noi, sincronizarea ajută la garantarea disponibilității informațiilor de calendar actualizate.</span><span class="sxs-lookup"><span data-stu-id="d9af3-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="d9af3-116">Această sincronizare se poate face oricând.</span><span class="sxs-lookup"><span data-stu-id="d9af3-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="d9af3-117">Vă recomandăm să utilizați un lot.</span><span class="sxs-lookup"><span data-stu-id="d9af3-117">We recommend that you use a batch.</span></span> <span data-ttu-id="d9af3-118">Opțiunile sunt disponibile în timpul sincronizării rezervărilor de capacitate.</span><span class="sxs-lookup"><span data-stu-id="d9af3-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="d9af3-119">Selectați **Management de proiect și contabilitate** &gt; **Periodic** &gt; **Sincronizarea capacității** &gt; **Cumulare sincronizare resurse de capacitate**.</span><span class="sxs-lookup"><span data-stu-id="d9af3-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="d9af3-120">Setați opțiunile în tabelul următor.</span><span class="sxs-lookup"><span data-stu-id="d9af3-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="d9af3-121">Opțiune</span><span class="sxs-lookup"><span data-stu-id="d9af3-121">Option</span></span>      | <span data-ttu-id="d9af3-122">Descriere</span><span class="sxs-lookup"><span data-stu-id="d9af3-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="d9af3-123">Codul perioadei</span><span class="sxs-lookup"><span data-stu-id="d9af3-123">Period code</span></span> | <span data-ttu-id="d9af3-124">Opțional, selectați codul intervalului de dată pentru registrul general pentru a seta datele de început și de sfârșit pentru procesul de sincronizare pentru cumulările de capacitate a resurselor.</span><span class="sxs-lookup"><span data-stu-id="d9af3-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="d9af3-125">Data de început</span><span class="sxs-lookup"><span data-stu-id="d9af3-125">Start date</span></span>  | <span data-ttu-id="d9af3-126">Introduceți data de începere pentru procesul de sincronizare pentru cumulările de capacitate a resurselor.</span><span class="sxs-lookup"><span data-stu-id="d9af3-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="d9af3-127">Dată de sfârșit</span><span class="sxs-lookup"><span data-stu-id="d9af3-127">End date</span></span>    | <span data-ttu-id="d9af3-128">Introduceți data de încheiere pentru procesul de sincronizare pentru cumulările de capacitate a resurselor.</span><span class="sxs-lookup"><span data-stu-id="d9af3-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="d9af3-129">[![Proces de sincronizare](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="d9af3-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
