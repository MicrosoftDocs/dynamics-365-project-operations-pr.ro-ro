---
title: Unități și grupuri de unități
description: Acest subiect oferă informații despre cum să creați unități și grupuri de unități în Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277353"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="8cfd3-103">Unități și grupuri de unități</span><span class="sxs-lookup"><span data-stu-id="8cfd3-103">Units and unit groups</span></span>

<span data-ttu-id="8cfd3-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="8cfd3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8cfd3-105">Unitățile sunt cantitățile sau măsurătorile în care vă vindeți produsele sau serviciilor.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="8cfd3-106">De exemplu, dacă vindeți produse pentru grădinărit, puteți vinde semințele în unități de tip pachete, cutii și paleți.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="8cfd3-107">Un grup de unitate este o colecție de unități diferite.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="8cfd3-108">Pentru a finaliza pașii din acest subiect, asigurați-vă că ați fost atribuit rolului de administrator de sistem sau de manager Sales Professional sau că aveți permisiuni echivalente.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="8cfd3-109">Crearea unui grup de unităţi</span><span class="sxs-lookup"><span data-stu-id="8cfd3-109">Create a unit group</span></span>

1. <span data-ttu-id="8cfd3-110">În harta site-ului, selectați **Unități**.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="8cfd3-111">Selectați **Nou**, și în caseta de dialog **Creați un grup de unități**, introduceți numele unității.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="8cfd3-112">În câmpul **Unitate primară**, introduceți cea mai joasă unitate comună de măsură în care se va vinde produsul.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="8cfd3-113">De exemplu, puteți introduce „bucată” sau „uncie”.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="8cfd3-114">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="8cfd3-115">Adăugați unități la un grup de unități</span><span class="sxs-lookup"><span data-stu-id="8cfd3-115">Add units to a unit group</span></span>

1. <span data-ttu-id="8cfd3-116">Deschideți un grup de unități și pe fila **Legate de**, selectați **Unități**.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="8cfd3-117">Veți vedea că unitatea principală este adăugată deja.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="8cfd3-118">Selectați **Adăugați o unitate nouă**, și pe pagina **Creare rapidă: unitate**, în câmpul **Nume**, introduceți numele unității.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="8cfd3-119">În câmpul **Cantitate**, introduceți cantitatea pe care o va conține unitatea.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="8cfd3-120">De exemplu, dacă o cutie conține două bucăți, introduceți „2”.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="8cfd3-121">În câmpul **Unitate de bază**, selectați o unitate de bază pentru a stabili cea mai mică unitate de măsură pentru unitate.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="8cfd3-122">De exemplu, puteți selecta „Bucată”.</span><span class="sxs-lookup"><span data-stu-id="8cfd3-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="8cfd3-123">Selectați **Salvare**:</span><span class="sxs-lookup"><span data-stu-id="8cfd3-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]