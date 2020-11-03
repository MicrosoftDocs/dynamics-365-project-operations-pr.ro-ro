---
title: Ce este starea unui proiect
description: Acest subiect furnizează informații despre starea atribuită proiectelor în Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082668"
---
# <a name="understand-project-status"></a><span data-ttu-id="345d1-103">Ce este starea unui proiect</span><span class="sxs-lookup"><span data-stu-id="345d1-103">Understand project status</span></span>

<span data-ttu-id="345d1-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="345d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="345d1-105">Secțiunea **Stare** a paginii **Entitate de proiect** furnizează un rezumat al stării unui proiect pe baza costului și efortului.</span><span class="sxs-lookup"><span data-stu-id="345d1-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="345d1-106">Câmpuri rezumat stare</span><span class="sxs-lookup"><span data-stu-id="345d1-106">Status summary fields</span></span>

- <span data-ttu-id="345d1-107">Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="345d1-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="345d1-108">Acest câmp utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere.</span><span class="sxs-lookup"><span data-stu-id="345d1-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="345d1-109">Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut.</span><span class="sxs-lookup"><span data-stu-id="345d1-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="345d1-110">Câmpul **Stare actualizată la** nu este modificabil.</span><span class="sxs-lookup"><span data-stu-id="345d1-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="345d1-111">Valoarea din acest câmp este o marcă de timp care indică data ultimei actualizări a stării.</span><span class="sxs-lookup"><span data-stu-id="345d1-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="345d1-112">Câmpurile **Planificarea performanței** și **Performanță de cost** sunt setate din grila de urmărire.</span><span class="sxs-lookup"><span data-stu-id="345d1-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="345d1-113">Când planificarea și varianța de cost pentru nodul rădăcină din vizualizarea **Urmărire efort** sunt pozitive, aceste câmpuri sunt actualizate la **Avans**.</span><span class="sxs-lookup"><span data-stu-id="345d1-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="345d1-114">Când programul și varianța costului pentru nodul rădăcină sunt negative, aceste câmpuri sunt setate la **În urmă**.</span><span class="sxs-lookup"><span data-stu-id="345d1-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
