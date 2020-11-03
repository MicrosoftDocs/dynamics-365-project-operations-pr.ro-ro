---
title: Crearea unei facturi proforma manuale
description: Acest subiect furnizează informații despre crearea unei facturi proforma manuale în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/20/2020
ms.locfileid: "4083025"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="9a8e7-103">Crearea unei facturi proforma manuale</span><span class="sxs-lookup"><span data-stu-id="9a8e7-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="9a8e7-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="9a8e7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a8e7-105">În Dynamics 365 Project Operations, facturile proforma pot fi create manual, după cum este necesar.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="9a8e7-106">Puteți crea manual o factură proforma din pagina listei **Contracte de proiect** sau din pagina de detalii **Contract de proiect**.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="9a8e7-107">Pagina listă contracte de proiect</span><span class="sxs-lookup"><span data-stu-id="9a8e7-107">Project Contracts list page</span></span>

<span data-ttu-id="9a8e7-108">Din pagina de listă **Contracte de proiect** , selectați unul sau mai multe contracte de proiect și creați facturi pentru toate înregistrările selectate.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="9a8e7-109">Sistemul verifică pentru a vedea care dintre contractele de proiect selectate are restanțe **Gata de facturare** înainte de data de astăzi.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="9a8e7-110">Din aceste contracte, sistemul creează proiecte de facturi proforma.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="9a8e7-111">Dacă un contract de proiect are mai mulți clienți, poate exista o factură creată pentru fiecare client și mai multe facturi pentru fiecare contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="9a8e7-112">Toate facturile de proiect create sunt disponibile pe pagina **Factură fiscală** din secțiunea **Facturare** din zona **Vânzări**.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="9a8e7-113">Pagina de detalii contract de proiect</span><span class="sxs-lookup"><span data-stu-id="9a8e7-113">Project Contract details page</span></span>

<span data-ttu-id="9a8e7-114">O factură proforma poate fi creată și din pagina de detalii **Contract de proiect** , care creează factura pentru acel contract specific de proiect.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="9a8e7-115">Sistemul verifică dacă contractul de proiect are o restanță **Gata de facturare** înainte de data de astăzi.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="9a8e7-116">Din aceste contracte, sistemul creează proiecte de facturi proforma pe baza numărului de clienți de pe fiecare linie de contract.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="9a8e7-117">Când este creată o singură factură proforma, se deschide pagina **Factura fiscala**.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="9a8e7-118">Dacă există mai multe facturi create pentru acel contract de proiect, atunci pagina listă **Facturi** se deschide pentru a afișa toate facturile create.</span><span class="sxs-lookup"><span data-stu-id="9a8e7-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
