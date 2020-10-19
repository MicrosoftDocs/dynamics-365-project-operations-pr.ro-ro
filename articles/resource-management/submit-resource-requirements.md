---
title: Remiterea unei solicitări de resursă
description: Aveți posibilitatea să trimiteți o cerință de resursă generată ca o solicitare de resursă. Solicitarea este apoi trimisă către un manager de resurse pentru îndeplinire.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961738"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="b53cd-104">Remiterea unei solicitări de resursă</span><span class="sxs-lookup"><span data-stu-id="b53cd-104">Submit a resource request</span></span>

<span data-ttu-id="b53cd-105">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="b53cd-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b53cd-106">Aveți posibilitatea să trimiteți o cerință de resursă generată ca o solicitare de resursă.</span><span class="sxs-lookup"><span data-stu-id="b53cd-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="b53cd-107">Solicitarea este apoi trimisă către un manager de resurse pentru îndeplinire.</span><span class="sxs-lookup"><span data-stu-id="b53cd-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="b53cd-108">În Dynamics 365 Project Operations, pe pagina **Proiecte**, selectați fila **Echipă** pentru a vizualiza o listă de resurse care pot fi rezervate.</span><span class="sxs-lookup"><span data-stu-id="b53cd-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="b53cd-109">Selectați resursa generică care are o cerință de resurse din listă și apoi faceți clic pe **Remitere cerere**.</span><span class="sxs-lookup"><span data-stu-id="b53cd-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="b53cd-110">Statutul de cerere al membrului generic de echipă se va schimba la **Remis**.</span><span class="sxs-lookup"><span data-stu-id="b53cd-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="b53cd-111">După ce solicitarea este îndeplinită, resursa generică va fi înlocuită de o resursă numită dacă managerul de resurse îndeplinește solicitarea cu rezervarea unei resurse numite.</span><span class="sxs-lookup"><span data-stu-id="b53cd-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="b53cd-112">În caz contrar, dacă managerul de resurse propune o resursă denumită, resursa generică rămâne în echipă și starea solicitării se va modifica la **Necesită revizuire**.</span><span class="sxs-lookup"><span data-stu-id="b53cd-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
