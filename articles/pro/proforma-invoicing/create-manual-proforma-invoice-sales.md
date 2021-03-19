---
title: Crearea unei facturi proforma manuale - simplificat
description: Acest subiect furnizează informații despre crearea unei facturi proforma manuale în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274203"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="e101a-103">Crearea unei facturi proforma manuale - simplificat</span><span class="sxs-lookup"><span data-stu-id="e101a-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="e101a-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="e101a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e101a-105">În Dynamics 365 Project Operations, facturile proforme pot fi create manual, după necesități.</span><span class="sxs-lookup"><span data-stu-id="e101a-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="e101a-106">Puteți crea manual o factură proforma din pagina listei **Contracte de proiect** sau din pagina de detalii **Contract de proiect**.</span><span class="sxs-lookup"><span data-stu-id="e101a-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="e101a-107">Pagina listă contracte de proiect</span><span class="sxs-lookup"><span data-stu-id="e101a-107">Project Contracts list page</span></span>

<span data-ttu-id="e101a-108">Din pagina de listă **Contracte de proiect**, selectați unul sau mai multe contracte de proiect și creați facturi pentru toate înregistrările selectate.</span><span class="sxs-lookup"><span data-stu-id="e101a-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="e101a-109">Sistemul verifică să vadă care dintre contractele de proiecte are un registru **Gata de facturat** cu o dată anterioară celei de azi.</span><span class="sxs-lookup"><span data-stu-id="e101a-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e101a-110">Din aceste contracte, sistemul creează proiecte de facturi proforma.</span><span class="sxs-lookup"><span data-stu-id="e101a-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="e101a-111">Dacă un contract de proiect are mai mulți clienți, poate exista o factură creată pentru fiecare client și mai multe facturi pentru fiecare contract de proiect.</span><span class="sxs-lookup"><span data-stu-id="e101a-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="e101a-112">Toate facturile de proiect create sunt disponibile pe pagina **Factură fiscală** din secțiunea **Facturare** din zona **Vânzări**.</span><span class="sxs-lookup"><span data-stu-id="e101a-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="e101a-113">Pagina de detalii contract de proiect</span><span class="sxs-lookup"><span data-stu-id="e101a-113">Project Contract details page</span></span>

<span data-ttu-id="e101a-114">O factură proformă poate fi creată și din pagina de detalii a **Contract de proiect**.</span><span class="sxs-lookup"><span data-stu-id="e101a-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="e101a-115">Sistemul verifică dacă contractul de proiect are un registru **Gata de facturat** cu dată anterioară celei de azi.</span><span class="sxs-lookup"><span data-stu-id="e101a-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="e101a-116">Din aceste contracte, sistemul creează proiecte de facturi proforma pe baza numărului de clienți de pe fiecare linie de contract.</span><span class="sxs-lookup"><span data-stu-id="e101a-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="e101a-117">Când este creată o singură factură proforma, se deschide pagina **Factura fiscala**.</span><span class="sxs-lookup"><span data-stu-id="e101a-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="e101a-118">În cazul în care sunt create mai multe facturi pentru respectivul contract de proiect, se deschide pagina care conține lista de **Facturi** pentru a afișa toate facturile create.</span><span class="sxs-lookup"><span data-stu-id="e101a-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]