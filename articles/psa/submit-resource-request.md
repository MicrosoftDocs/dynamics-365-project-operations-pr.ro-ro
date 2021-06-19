---
title: Remiterea unei solicitări de resurse
description: Acest subiect furnizează informații despre remiterea unei solicitări pentru o resursă de proiect.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013186"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="15fd3-103">Remiterea unei solicitări de resurse</span><span class="sxs-lookup"><span data-stu-id="15fd3-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="15fd3-104">Aveți posibilitatea să trimiteți o cerință de resursă generată ca o solicitare de resursă.</span><span class="sxs-lookup"><span data-stu-id="15fd3-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="15fd3-105">Solicitarea este apoi trimisă către un manager de resurse pentru îndeplinire.</span><span class="sxs-lookup"><span data-stu-id="15fd3-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="15fd3-106">În Project Service Automation (PSA), pe pagina **Proiecte**, faceți clic pe fila **Echipă** pentru a vizualiza o listă de resurse care pot fi rezervate.</span><span class="sxs-lookup"><span data-stu-id="15fd3-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="15fd3-107">Selectați resursa generică care are o cerință de resurse din listă și apoi faceți clic pe **Remitere cerere**.</span><span class="sxs-lookup"><span data-stu-id="15fd3-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Remiterea unei solicitări de resurse](media/RM-how-to-18.png)

<span data-ttu-id="15fd3-109">Statutul de cerere al membrului generic de echipă se va schimba la **Remis**.</span><span class="sxs-lookup"><span data-stu-id="15fd3-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="15fd3-110">După ce solicitarea este îndeplinită de managerul de resurse, resursa generică va fi înlocuită de o resursă numită dacă managerul de resurse îndeplinește solicitarea cu rezervarea unei resurse numite.</span><span class="sxs-lookup"><span data-stu-id="15fd3-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="15fd3-111">În caz contrar, resursa generică va rămâne în echipă și starea solicitării se va modifica la **Necesită revizuire**, dacă managerul de resurse a propus o resursă numită.</span><span class="sxs-lookup"><span data-stu-id="15fd3-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]