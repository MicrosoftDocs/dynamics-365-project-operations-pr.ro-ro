---
title: Rezervări versus atribuiri
description: Acest subiect furnizează informații despre diferențele dintre rezervările de resurse și atribuirile de resurse.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896026"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="44870-103">Rezervări versus atribuiri</span><span class="sxs-lookup"><span data-stu-id="44870-103">Bookings vs assignments</span></span>

<span data-ttu-id="44870-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="44870-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44870-105">Rezervările sunt alocarea fermă sau provizorie de resurse pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="44870-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="44870-106">Rezervările ferme consumă capacitatea unei resurse.</span><span class="sxs-lookup"><span data-stu-id="44870-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="44870-107">Atribuirile sunt alocarea de resurse pentru activitățile de proiect în planificarea proiectului.</span><span class="sxs-lookup"><span data-stu-id="44870-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="44870-108">Resursele pot fi reale sau generice.</span><span class="sxs-lookup"><span data-stu-id="44870-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="44870-109">În mod ideal, pentru resurse reale, rezervările și atribuirile ar trebui să fie în acord, deoarece acestea nu diferă.</span><span class="sxs-lookup"><span data-stu-id="44870-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="44870-110">Cu toate acestea, Microsoft Dynamics Project Operations nu pune în aplicare acest acord.</span><span class="sxs-lookup"><span data-stu-id="44870-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="44870-111">Vizualizarea **Reconciliere** arată unui manager de proiect locurile în care rezervările și atribuirile unei resurse nu sunt de acord.</span><span class="sxs-lookup"><span data-stu-id="44870-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
