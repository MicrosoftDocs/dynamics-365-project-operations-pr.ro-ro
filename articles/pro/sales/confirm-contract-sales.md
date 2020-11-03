---
title: Confirmarea unui contract de proiect
description: Acest subiect oferă informații despre cum să confirmați un contract în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082916"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="49f96-103">Confirmarea unui contract de proiect</span><span class="sxs-lookup"><span data-stu-id="49f96-103">Confirm a project contract</span></span>

<span data-ttu-id="49f96-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="49f96-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="49f96-105">Un contract de proiect în Dynamics 365 Project Operations poate fi activ cu un motiv de **Confirmat** , sau închis cu un motiv de **Pierdut**.</span><span class="sxs-lookup"><span data-stu-id="49f96-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed** , or closed with a reason of **Lost**.</span></span> <span data-ttu-id="49f96-106">Când confirmați un contract de proiect, starea se actualizează de la **Schiță** la **Activ** iar motivul de stare este **Confirmat**.</span><span class="sxs-lookup"><span data-stu-id="49f96-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="49f96-107">Un contract activ sau închis nu poate fi editat sau redeschis.</span><span class="sxs-lookup"><span data-stu-id="49f96-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="49f96-108">Impactul financiar al confirmării unui contract de proiect</span><span class="sxs-lookup"><span data-stu-id="49f96-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="49f96-109">După confirmarea unui contract de proiect, aplicația recalculează costurile prin inversarea costurilor mai vechi și creând costuri noi.</span><span class="sxs-lookup"><span data-stu-id="49f96-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="49f96-110">Noile costuri efective sunt apoi procesate pe baza metodei de facturare a liniei contractului de proiect asociat.</span><span class="sxs-lookup"><span data-stu-id="49f96-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="49f96-111">În cazul în care costurile reale fac referire la o linie contractuală de timp și materiale, aplicația recreează automat efectele corespunzătoare de vânzări nefacturate.</span><span class="sxs-lookup"><span data-stu-id="49f96-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="49f96-112">În cazul în care costurile reale fac referire la o linie de contract cu preț fix, aplicația încetează să reproceseze costurile reale.</span><span class="sxs-lookup"><span data-stu-id="49f96-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="49f96-113">Limitele care nu trebuie depășite, configurarea taxării, precum și stabilirea prețurilor și a costurilor pentru datele reale sunt evaluate și apoi actualizate ca parte a procesului de confirmare.</span><span class="sxs-lookup"><span data-stu-id="49f96-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="49f96-114">Închideți un contract de proiect ca pierdut</span><span class="sxs-lookup"><span data-stu-id="49f96-114">Close a project contract as lost</span></span>

<span data-ttu-id="49f96-115">Când închideți un contract de proiect ca pierdut, starea contractului este actualizată la **Închis** iar motivul de stare este **Pierdut**.</span><span class="sxs-lookup"><span data-stu-id="49f96-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="49f96-116">Contractul de proiect devine doar în citire.</span><span class="sxs-lookup"><span data-stu-id="49f96-116">The project contract becomes read-only.</span></span> <span data-ttu-id="49f96-117">Apare un dialog de confirmare înainte de finalizarea modificărilor, deoarece nu puteți redeschide un contract de proiect închis.</span><span class="sxs-lookup"><span data-stu-id="49f96-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="49f96-118">Dacă contractul de proiect închis ca pierdut face referire la un proiect pe liniile sale, acel proiect este de asemenea marcat ca închis.</span><span class="sxs-lookup"><span data-stu-id="49f96-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="49f96-119">Orice rezervare de resurse începând cu ziua respectivă este anulată.</span><span class="sxs-lookup"><span data-stu-id="49f96-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="49f96-120">Orice vânzări reale nefacturate din contractul de proiect care nu sunt deja pe factură vor fi anulate.</span><span class="sxs-lookup"><span data-stu-id="49f96-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="49f96-121">În Dynamics 365 Project Operations, închiderea unui contract de proiect ca pierdut nu va avea impact asupra stării oportunității asociate.</span><span class="sxs-lookup"><span data-stu-id="49f96-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="49f96-122">Oportunitatea va rămâne deschisă și trebuie închisă manual.</span><span class="sxs-lookup"><span data-stu-id="49f96-122">The opportunity will remain open and must be manually closed.</span></span>
