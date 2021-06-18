---
title: Închiderea unei oferte - simplificat
description: Acest subiect furnizează informații despre închiderea unei oferte în Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994151"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="f02a0-103">Închiderea unei oferte - simplificat</span><span class="sxs-lookup"><span data-stu-id="f02a0-103">Close a quote - lite</span></span>

<span data-ttu-id="f02a0-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="f02a0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f02a0-105">O ofertă de proiect poate fi închisă drept câștigată sau pierdută.</span><span class="sxs-lookup"><span data-stu-id="f02a0-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="f02a0-106">O ciornă a ofertei poate fi închisă deoarece operațiunile de activare și revizuire a cotațiilor nu sunt acceptate în Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f02a0-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="f02a0-107">Închideți o ofertă drept Câștigată</span><span class="sxs-lookup"><span data-stu-id="f02a0-107">Close a quote as Won</span></span>

<span data-ttu-id="f02a0-108">Când închideți o ofertă de proiect drept Câștigat, starea este setată pe Închis și motivul pentru această stare este Câștigat.</span><span class="sxs-lookup"><span data-stu-id="f02a0-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="f02a0-109">Închiderea ofertei face oferta de proiect doar în citire și creează o schiță de contract de proiect care conține informațiile despre ofertă.</span><span class="sxs-lookup"><span data-stu-id="f02a0-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="f02a0-110">Deoarece o ofertă închisă nu poate fi redeschisă, un dialog de confirmare vă va confirma modificările.</span><span class="sxs-lookup"><span data-stu-id="f02a0-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="f02a0-111">Dacă oferta este atașată unei oportunități, orice alte oferte ale proiectului cu ocazia se închid automat ca Pierdute.</span><span class="sxs-lookup"><span data-stu-id="f02a0-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="f02a0-112">Impactul financiar al închiderii unei oferte drept câștigată</span><span class="sxs-lookup"><span data-stu-id="f02a0-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="f02a0-113">Dacă există date reale de timp pentru un proiect în timp ce este încă atașat la cironă de ofertă, se înregistrează doar costul timpului sau cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="f02a0-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="f02a0-114">După închiderea unei oferte ca câștigat, aplicația va refactoriza costurile prin inversarea costurilor mai vechi și recrearea costurilor noi.</span><span class="sxs-lookup"><span data-stu-id="f02a0-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="f02a0-115">Aplicația va procesa aceste costuri reale pe baza metodei de facturare a liniei contractului de proiect asociat.</span><span class="sxs-lookup"><span data-stu-id="f02a0-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="f02a0-116">În cazul în care valorile reale ale costurilor fac referire la o linie de contract de timp și materiale, sunt create valorile reale de vânzare neînregistrate în contabilitate corespunzătoare pentru momentul când se închid ofertele și se creează contractul de proiect.</span><span class="sxs-lookup"><span data-stu-id="f02a0-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="f02a0-117">În cazul în care valorile reale ale costurilor fac referire la o linie de contract cu preț fix, aplicația va înceta să reproceseze valorile reale ale costurilor care se bazează pe regulile de facturare divizată pentru clienții contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="f02a0-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="f02a0-118">Închiderea unei oferte drept pierdută:</span><span class="sxs-lookup"><span data-stu-id="f02a0-118">Closing a quote as lost:</span></span>

<span data-ttu-id="f02a0-119">Când închideți o ofertă de proiect ca Pierdut, starea este setată pe Închis și motivul pentru această stare este Pierdut.</span><span class="sxs-lookup"><span data-stu-id="f02a0-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="f02a0-120">Închiderea ofertei face ca oferta de proiect să fie doar în citire.</span><span class="sxs-lookup"><span data-stu-id="f02a0-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="f02a0-121">Deoarece o ofertă închisă nu poate fi redeschisă și înainte de a închide o ofertă, un dialog de confirmare vă va confirma modificările.</span><span class="sxs-lookup"><span data-stu-id="f02a0-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="f02a0-122">Dacă oferta proiectului care este închisă ca Pierdut face referire la un proiect pe oricare dintre liniile sale, și respectivul proiect va fi marcat ca Închis.</span><span class="sxs-lookup"><span data-stu-id="f02a0-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="f02a0-123">Orice rezervare de resurse începând cu ziua respectivă este anulată.</span><span class="sxs-lookup"><span data-stu-id="f02a0-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="f02a0-124">În Project Operations, închiderea unei cotații ca Câștigat sau Pierdut nu va avea un impact asupra stării oportunității, care va rămâne deschisă până când va fi închisă manual.</span><span class="sxs-lookup"><span data-stu-id="f02a0-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]