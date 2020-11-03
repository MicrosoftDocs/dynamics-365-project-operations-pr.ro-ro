---
title: Închideți oferte
description: Acest subiect furnizează informații despre închiderea unei oferte în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082717"
---
# <a name="close-quotes"></a><span data-ttu-id="3a747-103">Închideți oferte</span><span class="sxs-lookup"><span data-stu-id="3a747-103">Close quotes</span></span> 

<span data-ttu-id="3a747-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="3a747-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3a747-105">O ofertă de proiect poate fi închisă drept câștigată sau pierdută.</span><span class="sxs-lookup"><span data-stu-id="3a747-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="3a747-106">Operațiunile de activare și revizuire asupra ofertelor nu sunt acceptate în Microsoft Dynamics 365 Project Operations, așa că o schiță de ofertă poate fi închisă.</span><span class="sxs-lookup"><span data-stu-id="3a747-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="3a747-107">Închideți o ofertă drept Câștigată</span><span class="sxs-lookup"><span data-stu-id="3a747-107">Close a quote as Won</span></span>

<span data-ttu-id="3a747-108">Închiderea unei oferte de proiect drept Câștigată va închide oferta cu starea setată la Închisă și motivul de stare setat la Câștigat.</span><span class="sxs-lookup"><span data-stu-id="3a747-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="3a747-109">Închiderea ofertei face oferta de proiect doar în citire și creează o schiță de contract de proiect care conține informațiile despre ofertă.</span><span class="sxs-lookup"><span data-stu-id="3a747-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="3a747-110">Deoarece o ofertă închisă nu poate fi redeschisă, un dialog de confirmare Există un dialog de confirmare înainte de efectuarea modificărilor, deoarece o ofertă închisă nu poate fi redeschisă și modificările sunt ireversibile.</span><span class="sxs-lookup"><span data-stu-id="3a747-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="3a747-111">Dacă oferta este atașată unei oportunități, orice alte oferte ale proiectului cu ocazia se închid automat ca Pierdute.</span><span class="sxs-lookup"><span data-stu-id="3a747-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="3a747-112">Impactul financiar al închiderii unei oferte drept câștigată</span><span class="sxs-lookup"><span data-stu-id="3a747-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="3a747-113">Dacă au existat date reale pentru timpul înregistrat pe un proiect în timp ce acesta este încă atașat la o schiță de ofertă, se înregistrează doar costul timpului sau cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="3a747-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="3a747-114">După închiderea unei oferte ca câștigat, aplicația va refactoriza costurile prin inversarea costurilor mai vechi și recrearea costurilor noi.</span><span class="sxs-lookup"><span data-stu-id="3a747-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="3a747-115">Aplicația va procesa aceste costuri reale pe baza metodei de facturare a liniei contractului de proiect asociat.</span><span class="sxs-lookup"><span data-stu-id="3a747-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="3a747-116">În cazul în care costurile reale fac referire la o linie contractuală de timp și materiale, sistemul va crea în mod automat cifre de vânzări corespondente nefacturate pentru momentul în care se închide oferta și se creează contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="3a747-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="3a747-117">În cazul în care costurile reale se referă la o linie contractuală cu preț fix, aplicația va înceta să reproceseze costurile reale pe baza regulilor de facturare împărțite pentru clienții contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="3a747-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="3a747-118">Închiderea unei oferte drept pierdută:</span><span class="sxs-lookup"><span data-stu-id="3a747-118">Closing a quote as lost:</span></span>

<span data-ttu-id="3a747-119">Închiderea unei oferte de proiect drept Pierdut va seta starea cotației la Închis și motiv stare la Pierdut.</span><span class="sxs-lookup"><span data-stu-id="3a747-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="3a747-120">Închiderea ofertei face ca oferta de proiect să fie doar în citire.</span><span class="sxs-lookup"><span data-stu-id="3a747-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="3a747-121">Deoarece o ofertă închisă nu poate fi redeschisă și înainte de a închide o ofertă, un dialog de confirmare vă va confirma modificările.</span><span class="sxs-lookup"><span data-stu-id="3a747-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="3a747-122">Dacă oferta de proiect care este închisă ca Pierdută are un proiect la care se face referire pe oricare dintre liniile sale, acel proiect este de asemenea marcat ca Închis și orice rezervare de resurse din acea zi înainte este anulată.</span><span class="sxs-lookup"><span data-stu-id="3a747-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="3a747-123">În Project Operations, închiderea unei cotații ca Câștigat sau Pierdut nu va avea un impact asupra stării oportunității, care va rămâne deschisă până când va fi închisă manual.</span><span class="sxs-lookup"><span data-stu-id="3a747-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
