---
title: Rezervări versus atribuiri
description: Acest subiect furnizează informații despre diferențele dintre rezervările de resurse și atribuirile de resurse.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279918"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="d0919-103">Rezervări versus atribuiri</span><span class="sxs-lookup"><span data-stu-id="d0919-103">Bookings vs assignments</span></span>

<span data-ttu-id="d0919-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="d0919-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0919-105">Rezervările sunt alocarea fermă sau provizorie de resurse pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="d0919-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="d0919-106">Rezervările ferme consumă capacitatea unei resurse.</span><span class="sxs-lookup"><span data-stu-id="d0919-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="d0919-107">Rezervările reprezintă concepte organizaționale pentru echipe, astfel încât acestea să poată înțelege modul în care resursele vor fi angajate în diferite proiecte.</span><span class="sxs-lookup"><span data-stu-id="d0919-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="d0919-108">Dynamics 365 Project Operations consideră rezervările ca fiind un concept la nivel de proiect.</span><span class="sxs-lookup"><span data-stu-id="d0919-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="d0919-109">Spre deosebire de rezervări, atribuirile sunt angajamentul resurselor la activitățile de proiect în planificarea de proiect.</span><span class="sxs-lookup"><span data-stu-id="d0919-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="d0919-110">Resursele pot fi denumite sau generice.</span><span class="sxs-lookup"><span data-stu-id="d0919-110">The resources can be named or generic.</span></span>  <span data-ttu-id="d0919-111">Când o cerință pentru o resursă derivă din atribuirile de sarcini în cadrul proiectului, Project Operations utilizează schițele de efort ale atribuirii resurselor pentru a construi schițele detaliilor cerințelor de resurse.</span><span class="sxs-lookup"><span data-stu-id="d0919-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="d0919-112">Cu toate acestea, nu se menține o referință la atribuirea resurselor.</span><span class="sxs-lookup"><span data-stu-id="d0919-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="d0919-113">Actualizările rezervărilor derivate din cerința de resurse nu actualizează nicio alocare de resurse.</span><span class="sxs-lookup"><span data-stu-id="d0919-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="d0919-114">De obicei, suma rezervărilor pentru o resursă va fi egală cu suma atribuțiilor resursei pentru una sau mai multe sarcini.</span><span class="sxs-lookup"><span data-stu-id="d0919-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="d0919-115">Cu toate acestea, Project Operations nu pune în aplicare acest acord.</span><span class="sxs-lookup"><span data-stu-id="d0919-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="d0919-116">Vizualizarea **Reconciliere** arată managerului de proiect unde rezervările unei resurse și atribuirile nu sunt de acord.</span><span class="sxs-lookup"><span data-stu-id="d0919-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]