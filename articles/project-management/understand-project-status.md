---
title: Ce este starea unui proiect
description: Acest subiect furnizează informații despre starea atribuită proiectelor în Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127308"
---
# <a name="understand-project-status"></a><span data-ttu-id="a509e-103">Ce este starea unui proiect</span><span class="sxs-lookup"><span data-stu-id="a509e-103">Understand project status</span></span>

<span data-ttu-id="a509e-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="a509e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a509e-105">Secțiunea **Stare** a paginii **Entitate de proiect** furnizează un rezumat al stării unui proiect pe baza costului și efortului.</span><span class="sxs-lookup"><span data-stu-id="a509e-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="a509e-106">Câmpuri rezumat stare</span><span class="sxs-lookup"><span data-stu-id="a509e-106">Status summary fields</span></span>

- <span data-ttu-id="a509e-107">Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului.</span><span class="sxs-lookup"><span data-stu-id="a509e-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="a509e-108">Acest câmp utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere.</span><span class="sxs-lookup"><span data-stu-id="a509e-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="a509e-109">Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut.</span><span class="sxs-lookup"><span data-stu-id="a509e-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="a509e-110">Câmpul **Stare actualizată la** nu este editabil.</span><span class="sxs-lookup"><span data-stu-id="a509e-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="a509e-111">Valoarea din acest câmp este o marcă de timp care indică data ultimei actualizări a stării.</span><span class="sxs-lookup"><span data-stu-id="a509e-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="a509e-112">Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din grila de urmărire.</span><span class="sxs-lookup"><span data-stu-id="a509e-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="a509e-113">Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, aceste câmpuri sunt actualizate la **Avans**.</span><span class="sxs-lookup"><span data-stu-id="a509e-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="a509e-114">Când programul și varianța costului pentru nodul rădăcină sunt negative, aceste câmpuri sunt setate la **În urmă**.</span><span class="sxs-lookup"><span data-stu-id="a509e-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
