---
title: Importul și menținerea tranzacțiilor cu cardul de credit
description: Acest subiect explică cum să importați și să mențineți tranzacțiile cu cardul de credit legate de cheltuieli. Aceste tranzacții pot fi configurate astfel încât să fie importate automat într-o planificare recurentă sau să poată fi importate manual, după cum sunt necesare.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271593"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="46641-104">Importul și menținerea tranzacțiilor cu cardul de credit</span><span class="sxs-lookup"><span data-stu-id="46641-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="46641-105">Tranzacțiile legate de cheltuieli cu cardul de credit pot fi configurate astfel încât să fie importate automat într-un program recurent.</span><span class="sxs-lookup"><span data-stu-id="46641-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="46641-106">Alternativ, tranzacțiile pot fi importate manual, după cum sunt necesare.</span><span class="sxs-lookup"><span data-stu-id="46641-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="46641-107">Tranzacțiile cu cardul de credit sunt importate prin intermediul entității de date privind tranzacțiile cu cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="46641-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="46641-108">Pentru mai multe informații despre entitățile de date, consultați [Entități de date](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="46641-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="46641-109">Importați tranzacții cu cardul de credit</span><span class="sxs-lookup"><span data-stu-id="46641-109">Import credit card transactions</span></span>

1. <span data-ttu-id="46641-110">Pe pagina **Tranzacții cu cardul de credit**, selectați **Tranzacții de import**.</span><span class="sxs-lookup"><span data-stu-id="46641-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="46641-111">Dacă deschideți gestionarea datelor pentru prima dată, sistemul trebuie să actualizeze lista entităților de date înainte de a putea continua.</span><span class="sxs-lookup"><span data-stu-id="46641-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="46641-112">În câmpul **Nume**, introduceți o descriere unică a lucrării de import.</span><span class="sxs-lookup"><span data-stu-id="46641-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="46641-113">În câmpul **Format de date sursă**, selectați formatul fișierului care conține tranzacțiile cu cardul de credit de importat.</span><span class="sxs-lookup"><span data-stu-id="46641-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="46641-114">Selectați **Încărcare**, apoi găsiți și selectați fișierul de importat.</span><span class="sxs-lookup"><span data-stu-id="46641-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="46641-115">După ce fișierul a fost încărcat, validați maparea fișierului tranzacției cu cardul de credit și coloanele entității de date privind tranzacțiile cu cardul de credit, selectând linkul **Vizualizare hartă** pe dală.</span><span class="sxs-lookup"><span data-stu-id="46641-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="46641-116">Dacă există erori de mapare sau dacă trebuie să modificați maparea, efectuați modificările de mapare fie din fila **Vizualizare mapare** sau fila **Detalii de mapare**.</span><span class="sxs-lookup"><span data-stu-id="46641-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="46641-117">Pentru a automatiza tranzacțiile cu cardul de credit, selectați **Creați o operațiune de date recurente**.</span><span class="sxs-lookup"><span data-stu-id="46641-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="46641-118">Puteți seta apoi recurența care definește cât de des ar trebui importate tranzacțiile cu cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="46641-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="46641-119">Când ați terminat, selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="46641-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="46641-120">Pentru a importa fișierul selectat acum, selectați **Import**.</span><span class="sxs-lookup"><span data-stu-id="46641-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="46641-121">Dacă apar erori în timpul importului, puteți vizualiza jurnalul de execuție sau datele de etapizare pentru a vedea erorile pe care trebuie să le remediați pentru a garanta un import reușit.</span><span class="sxs-lookup"><span data-stu-id="46641-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="46641-122">Dacă trebuie să importați mai mult de un format de fișier, trebuie să creați lucrări de import separate pentru fiecare tip de format.</span><span class="sxs-lookup"><span data-stu-id="46641-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="46641-123">Reatribuiți tranzacțiile cu cardul de credit pentru angajații reziliați</span><span class="sxs-lookup"><span data-stu-id="46641-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="46641-124">După ce o înregistrare a angajatului este terminată, contul Active Directory Domain Services (AD DS) al angajatului este dezactivat.</span><span class="sxs-lookup"><span data-stu-id="46641-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="46641-125">Cu toate acestea, ar putea exista tranzacții active cu cardul de credit care trebuie în continuare cheltuite și rambursate.</span><span class="sxs-lookup"><span data-stu-id="46641-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="46641-126">De la pagina **Tranzacții cu cardul de credit**, puteți reatribui angajatul pentru orice tranzacție cu cardul de credit în cazul în care angajatul asociat a fost reziliat.</span><span class="sxs-lookup"><span data-stu-id="46641-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="46641-127">Selectați una sau mai multe tranzacții cu cardul de credit, apoi selectați **Reatribuiți tranzacțiile**.</span><span class="sxs-lookup"><span data-stu-id="46641-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="46641-128">Apoi puteți selecta un alt angajat căruia să îi atribuiți tranzacțiile cu cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="46641-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="46641-129">După ce tranzacțiile cu cardul de credit au fost realocate, acestea pot fi selectate pentru un raport de cheltuieli și plătite prin procesul obișnuit de rambursare a raportului de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="46641-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]