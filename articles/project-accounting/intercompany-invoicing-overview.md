---
title: Prezentare generală a facturării între companii
description: Acest subiect oferă informații și exemple despre facturarea între companii pentru proiecte.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369391"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="a7178-103">Prezentare generală a facturării între companii</span><span class="sxs-lookup"><span data-stu-id="a7178-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="a7178-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="a7178-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a7178-105">Organizația dvs. ar putea avea mai multe divizii, filiale și alte entități juridice care își transferă produse și servicii reciproc pentru proiecte.</span><span class="sxs-lookup"><span data-stu-id="a7178-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="a7178-106">Entitatea juridică care furnizează serviciul sau produsul se numește *entitate juridică de creditare*.</span><span class="sxs-lookup"><span data-stu-id="a7178-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="a7178-107">Entitatea juridică care primește serviciul sau produsul se numește *entitate juridică de împrumut*.</span><span class="sxs-lookup"><span data-stu-id="a7178-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="a7178-108">Următoarea ilustrație prezintă un scenariu tipic în care două persoane juridice, Contoso Robotics SUA (entitatea juridică care împrumută) și Contoso Robotics UK (entitatea juridică care împrumută) împarte resurse pentru a livra un proiect pentru client, Adventure works.</span><span class="sxs-lookup"><span data-stu-id="a7178-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="a7178-109">Pentru acest scenariu, Contoso Robotics SUA este contractat pentru livrarea lucrărilor către Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="a7178-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Facturare între companii](./media/IntercompanyScenario.png) 

<span data-ttu-id="a7178-111">Dynamics 365 Project Operations utilizează următorul flux pentru a procesa tranzacții între companii:</span><span class="sxs-lookup"><span data-stu-id="a7178-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="a7178-112">Resursele de la entitatea juridică care acordă împrumuturi înregistrează tranzacțiile între timp sau cheltuieli între companii prin rezervarea timpului și cheltuielilor pentru proiectele din entitatea juridică care împrumută.</span><span class="sxs-lookup"><span data-stu-id="a7178-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="a7178-113">Costurile de timp și cheltuieli sunt înregistrate în societatea de creditare utilizând lista de prețuri de cost unitare a companiei de împrumut.</span><span class="sxs-lookup"><span data-stu-id="a7178-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="a7178-114">Tranzacțiile de vânzare nefacturate între companii sunt înregistrate în societatea de creditare utilizând lista de prețuri de cost unitare a companiei de împrumut.</span><span class="sxs-lookup"><span data-stu-id="a7178-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="a7178-115">Veniturile necontabilizate se înregistrează în compania împrumutată utilizând lista de prețuri de vânzare a contractului de proiect.</span><span class="sxs-lookup"><span data-stu-id="a7178-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="a7178-116">Clientul poate fi facturat atunci când se înregistrează venituri nefacturate.</span><span class="sxs-lookup"><span data-stu-id="a7178-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="a7178-117">Clientul nu trebuie să aștepte până la finalizarea procesării facturilor între companii.</span><span class="sxs-lookup"><span data-stu-id="a7178-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="a7178-118">Facturile clienților între companii sunt create periodic în cadrul companiei de creditare.</span><span class="sxs-lookup"><span data-stu-id="a7178-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="a7178-119">Facturile sunt create manual sau utilizând un proces automat automat.</span><span class="sxs-lookup"><span data-stu-id="a7178-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="a7178-120">Se poate crea o singură factură pentru fiecare entitate juridică care împrumută sau se pot crea facturi separate prin proiect.</span><span class="sxs-lookup"><span data-stu-id="a7178-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="a7178-121">Atunci când factura clientului între companii este înregistrată în entitatea juridică de creditare, se creează factura de vânzător în așteptare corespunzătoare în entitatea juridică de împrumut.</span><span class="sxs-lookup"><span data-stu-id="a7178-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="a7178-122">Costurile din factura furnizorului în așteptare vor fi înregistrate în caseta de proiect la înregistrarea facturii.</span><span class="sxs-lookup"><span data-stu-id="a7178-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="a7178-123">Următoarea diagramă ilustrează facturarea între companii, în ceea ce privește evenimentele contabile și înregistrările preconizate în registrul general.</span><span class="sxs-lookup"><span data-stu-id="a7178-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Flux între companii](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="a7178-125">Resurse suplimentare</span><span class="sxs-lookup"><span data-stu-id="a7178-125">Additional resources</span></span>

- [<span data-ttu-id="a7178-126">Configurarea facturării între companii</span><span class="sxs-lookup"><span data-stu-id="a7178-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="a7178-127">Înregistrarea tranzacțiilor între companii</span><span class="sxs-lookup"><span data-stu-id="a7178-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="a7178-128">Crearea de facturi de client și furnizor între companii</span><span class="sxs-lookup"><span data-stu-id="a7178-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]