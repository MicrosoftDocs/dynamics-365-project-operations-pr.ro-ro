---
title: Revizuirea resurselor propuse
description: Acest subiect furnizează informații despre modul de propunere a resurselor de proiect.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fa0515b9d6a0023c05c37d2bcfa6a403f48927cb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279288"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="d1148-103">Revizuirea resurselor propuse</span><span class="sxs-lookup"><span data-stu-id="d1148-103">Review proposed resources</span></span>

<span data-ttu-id="d1148-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="d1148-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1148-105">Managerii de resurse pot propune o resursă către managerul de proiect utilizând o solicitare de resurse.</span><span class="sxs-lookup"><span data-stu-id="d1148-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="d1148-106">Din grila de solicitări sau din cererea în sine,selectați **Găsire resurse**.</span><span class="sxs-lookup"><span data-stu-id="d1148-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="d1148-107">În pagina **Asistent planificare**, selectați resursa, apoi, în panoul **Creare rezervare resursă**, în câmpul **Stare rezervare**, selectați **Rezervare.**</span><span class="sxs-lookup"><span data-stu-id="d1148-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="d1148-108">Apar următoarele actualizări de stare:</span><span class="sxs-lookup"><span data-stu-id="d1148-108">The following status updates occur:</span></span>

- <span data-ttu-id="d1148-109">În pagina **Asistent programare**, indicatorii de stare sunt actualizați pentru a indica faptul că rezervarea este propusă, nu rezervată ferm.</span><span class="sxs-lookup"><span data-stu-id="d1148-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="d1148-110">La solicitarea de resurse, starea se modifică la **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="d1148-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="d1148-111">În fila **Echipă** a proiectului, valoarea de **Stare solicitare** a membrului generic al echipei este schimbată la **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="d1148-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="d1148-112">Managerul de proiect poate accepta sau respinge propunerea.</span><span class="sxs-lookup"><span data-stu-id="d1148-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="d1148-113">Atunci când managerii de resurse procesează solicitările de resurse, pot utiliza oricare dintre următoarele abordări:</span><span class="sxs-lookup"><span data-stu-id="d1148-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="d1148-114">Propun mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a îndeplini orele necesare.</span><span class="sxs-lookup"><span data-stu-id="d1148-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="d1148-115">Orele propuse sunt apoi împărțite între mai multe resurse care pot satisface orele necesare.</span><span class="sxs-lookup"><span data-stu-id="d1148-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="d1148-116">În acest scenariu, orele nu se pot suprapune.</span><span class="sxs-lookup"><span data-stu-id="d1148-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="d1148-117">Propun mai puține resurse decât sunt necesare.</span><span class="sxs-lookup"><span data-stu-id="d1148-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="d1148-118">În acest scenariu, capacitatea de resurse propusă este mai mică decât orele necesare pe care le-a indicat solicitantul.</span><span class="sxs-lookup"><span data-stu-id="d1148-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="d1148-119">Prin urmare, atunci când solicitantul acceptă resursele propuse, este creată o cerință de resursă neîndeplinită pentru a captura cererea rămasă.</span><span class="sxs-lookup"><span data-stu-id="d1148-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="d1148-120">Rezervă mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a finaliza lucrarea.</span><span class="sxs-lookup"><span data-stu-id="d1148-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="d1148-121">Rezervă mai puține resurse decât sunt necesare.</span><span class="sxs-lookup"><span data-stu-id="d1148-121">Book fewer resources than are required.</span></span> <span data-ttu-id="d1148-122">În acest scenariu, orele rezervate sunt mai puține decât orele necesare.</span><span class="sxs-lookup"><span data-stu-id="d1148-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="d1148-123">Sistemul vă ghidează să propuneți resurse în loc de rezervări, astfel încât solicitantul să poată verifica și urmări cererea rămasă.</span><span class="sxs-lookup"><span data-stu-id="d1148-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="d1148-124">Disponibilitatea resursei</span><span class="sxs-lookup"><span data-stu-id="d1148-124">Resource availability</span></span>

<span data-ttu-id="d1148-125">Este esențial ca managerii de resurse să poată vizualiza disponibilitatea resurselor și să actualizeze rezervările.</span><span class="sxs-lookup"><span data-stu-id="d1148-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="d1148-126">în unele cazuri, nu există nicio cerere formală (cerere de resurse), dar un manager de resurse trebuie să răspundă la o cerere neplanificată care vine prin canale, cum ar fi un e-mail, apel telefonic sau mesaj instant.</span><span class="sxs-lookup"><span data-stu-id="d1148-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="d1148-127">Managerii de resurse utilizează tabloul de planificare pentru a actualiza resursele și rezervările.</span><span class="sxs-lookup"><span data-stu-id="d1148-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="d1148-128">Programul de lucru al resurselor se utilizează ca bază pentru calcularea disponibilității unei resurse.</span><span class="sxs-lookup"><span data-stu-id="d1148-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="d1148-129">Rezervările de resurse consumă capacitatea resurselor.</span><span class="sxs-lookup"><span data-stu-id="d1148-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="d1148-130">Consiliul de planificare utilizează culori și umbrire pentru a afișa rezervările, disponibilitatea și rezervările excedentare și, de asemenea, starea rezervărilor.</span><span class="sxs-lookup"><span data-stu-id="d1148-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="d1148-131">O setare din setările panoului de planificare vă permite să afișați o legendă.</span><span class="sxs-lookup"><span data-stu-id="d1148-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="d1148-132">În cazul în care o săgeată orientată spre dreapta apare lângă o resursă individuală care se poate rezerva în tabloul de planificare, resursa poate fi extinsă pentru a afișa detalii despre activitatea pe care este rezervată resursa.</span><span class="sxs-lookup"><span data-stu-id="d1148-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="d1148-133">Deoarece Dynamics 365 Project Operations utilizează motorul Universal Resource Scheduling, dacă aveți instalat și Dynamics 365 Field Service, puteți vizualiza detaliile rezervărilor de resurse pentru proiecte, comenzi de lucru și orice alte entități la care ați extins programarea.</span><span class="sxs-lookup"><span data-stu-id="d1148-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="d1148-134">Pentru a vizualiza mai multe detalii despre o resursă individuală, faceți clic cu butonul din dreapta pe acesta pentru a deschide fișa resursei.</span><span class="sxs-lookup"><span data-stu-id="d1148-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]