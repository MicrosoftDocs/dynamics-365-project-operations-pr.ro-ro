---
title: Achiziții de materiale care nu există pe stoc utilizând o factură de vânzător neachitată
description: Acest subiect explică modul de înregistrare a facturilor neachitate de la furnizor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880676"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="2daf8-103">Achiziții de materiale care nu există pe stoc utilizând o factură de vânzător neachitată</span><span class="sxs-lookup"><span data-stu-id="2daf8-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="2daf8-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="2daf8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2daf8-105">Deoarece o companie cumpără materiale care nu sunt stocate pentru un proiect, costurile pot fi înregistrate imediat în raport cu proiectul.</span><span class="sxs-lookup"><span data-stu-id="2daf8-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="2daf8-106">De exemplu, Contoso Robotics SUA realizează un proiect de reînnoire a echipamentelor și are nevoie de licențe de software.</span><span class="sxs-lookup"><span data-stu-id="2daf8-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="2daf8-107">Aceste licențe sunt achiziționate de la un furnizor terță parte.</span><span class="sxs-lookup"><span data-stu-id="2daf8-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="2daf8-108">Folosind Dynamics 365 Finance, funcționarul de conturi furnizori înregistrează un document de factură neachitată a furnizorului și atribuie costurile licenței direct proiectului de reînnoire a echipamentului.</span><span class="sxs-lookup"><span data-stu-id="2daf8-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2daf8-109">Înainte de a utiliza funcționalitatea descrisă în acest subiect, revizuiți și aplicați configurațiile necesare.</span><span class="sxs-lookup"><span data-stu-id="2daf8-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="2daf8-110">Pentru mai multe informații, consultați [Activarea materialelor care nu există pe stoc și a facturilor de la furnizori neachitate](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="2daf8-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="2daf8-111">Postați o factură de vânzător neachitată legată de proiect</span><span class="sxs-lookup"><span data-stu-id="2daf8-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="2daf8-112">Facturile neachitate de la vânzător pot fi înregistrate pe pagina **Facturi de vânzător neachitate** (**Conturi furnizori** > **Facturi** > **Facturi de vânzător neachitate**).</span><span class="sxs-lookup"><span data-stu-id="2daf8-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="2daf8-113">Parcurgeți pașii următori pentru a posta o factură de furnizor neachitată legată de proiect:</span><span class="sxs-lookup"><span data-stu-id="2daf8-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="2daf8-114">Accesați **Conturi furnizori** > **Facturi** și selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="2daf8-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="2daf8-115">În câmpul **Cont de factură**, selectați un furnizor și în câmpul **Număr**, introduceți identificarea facturii furnizorului.</span><span class="sxs-lookup"><span data-stu-id="2daf8-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="2daf8-116">Adăugați o linie la factura furnizorului și în câmpul **Numărul de element**, selectați elementul care nu este stocat cumpărat de la furnizor.</span><span class="sxs-lookup"><span data-stu-id="2daf8-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="2daf8-117">Liniile de facturare ale furnizorului care se bazează pe o categorie de achiziții nu pot fi înregistrate în cadrul proiectului.</span><span class="sxs-lookup"><span data-stu-id="2daf8-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="2daf8-118">Adăugați cantitatea achiziționată.</span><span class="sxs-lookup"><span data-stu-id="2daf8-118">Add the quantity purchased.</span></span> <span data-ttu-id="2daf8-119">Sistemul va completa prețul unitar pe baza configurației prețului articolului care nu este stocat.</span><span class="sxs-lookup"><span data-stu-id="2daf8-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="2daf8-120">Verificați suma totală și alte detalii necesare pe linie.</span><span class="sxs-lookup"><span data-stu-id="2daf8-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="2daf8-121">Pe detaliile liniei, pe fila **Proiect**, selectați ID-ul proiectului în care va fi înregistrat acest element.</span><span class="sxs-lookup"><span data-stu-id="2daf8-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="2daf8-122">Opțional, selectați numărul activității și actualizați categoria de proiect și proprietatea liniei.</span><span class="sxs-lookup"><span data-stu-id="2daf8-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="2daf8-123">Postați factura furnizorului în așteptare.</span><span class="sxs-lookup"><span data-stu-id="2daf8-123">Post pending vendor invoice.</span></span> <span data-ttu-id="2daf8-124">Când factura este publicată, sistemul înregistrează:</span><span class="sxs-lookup"><span data-stu-id="2daf8-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="2daf8-125">Valoarea soldului furnizorului.</span><span class="sxs-lookup"><span data-stu-id="2daf8-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="2daf8-126">Valoare impozit pe vânzări.</span><span class="sxs-lookup"><span data-stu-id="2daf8-126">The sales tax amount.</span></span>
    - <span data-ttu-id="2daf8-127">Costul aferent proiectului este înregistrat în contul de integrare a achizițiilor.</span><span class="sxs-lookup"><span data-stu-id="2daf8-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="2daf8-128">Tranzacția efectivă a proiectului în Dataverse.</span><span class="sxs-lookup"><span data-stu-id="2daf8-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="2daf8-129">Această tranzacție este procesată în continuare folosind [Jurnalul de integrare Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2daf8-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="2daf8-130">Postarea acestui jurnal mută suma din contul de integrare a achizițiilor în contul de cost de proiect.</span><span class="sxs-lookup"><span data-stu-id="2daf8-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
