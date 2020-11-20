---
title: Configurarea integrării cardului de credit
description: Acest subiect explică cum să importați și să mențineți tranzacțiile cu cardul de credit legate de cheltuieli.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120873"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="38123-103">Configurarea integrării cardului de credit</span><span class="sxs-lookup"><span data-stu-id="38123-103">Set up credit card integration</span></span>

<span data-ttu-id="38123-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="38123-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="38123-105">Tranzacțiile legate de cheltuieli cu cardul de credit pot fi configurate astfel încât să fie importate automat într-un program recurent.</span><span class="sxs-lookup"><span data-stu-id="38123-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="38123-106">Alternativ, tranzacțiile pot fi importate manual, după cum sunt necesare.</span><span class="sxs-lookup"><span data-stu-id="38123-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="38123-107">Tranzacțiile cu cardul de credit sunt importate prin intermediul entității de date privind tranzacțiile cu cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="38123-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="38123-108">Importați tranzacții cu cardul de credit</span><span class="sxs-lookup"><span data-stu-id="38123-108">Import credit card transactions</span></span>

1. <span data-ttu-id="38123-109">Pe pagina **Tranzacții cu cardul de credit**, selectați **Tranzacții de import**.</span><span class="sxs-lookup"><span data-stu-id="38123-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="38123-110">Dacă deschideți gestionarea datelor pentru prima dată, sistemul trebuie să actualizeze lista entităților de date înainte de a putea continua.</span><span class="sxs-lookup"><span data-stu-id="38123-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="38123-111">În câmpul **Nume**, introduceți o descriere unică a lucrării de import.</span><span class="sxs-lookup"><span data-stu-id="38123-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="38123-112">În câmpul **Format de date sursă**, selectați formatul fișierului care conține tranzacțiile cu cardul de credit de importat.</span><span class="sxs-lookup"><span data-stu-id="38123-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="38123-113">Selectați **Încărcare**, apoi găsiți și selectați fișierul de importat.</span><span class="sxs-lookup"><span data-stu-id="38123-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="38123-114">După ce fișierul a fost încărcat, validați maparea fișierului tranzacției cu cardul de credit și coloanele entității de date privind tranzacțiile cu cardul de credit, selectând linkul **Vizualizare hartă** pe dală.</span><span class="sxs-lookup"><span data-stu-id="38123-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="38123-115">Dacă există erori de mapare sau dacă trebuie să modificați maparea, efectuați modificările de mapare fie din fila **Vizualizare mapare** sau fila **Detalii de mapare**.</span><span class="sxs-lookup"><span data-stu-id="38123-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="38123-116">Pentru a automatiza tranzacțiile cu cardul de credit, selectați **Creați o operațiune de date recurente**.</span><span class="sxs-lookup"><span data-stu-id="38123-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="38123-117">Puteți seta apoi recurența care definește cât de des ar trebui importate tranzacțiile cu cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="38123-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="38123-118">Când ați terminat, selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="38123-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="38123-119">Pentru a importa fișierul selectat acum, selectați **Import**.</span><span class="sxs-lookup"><span data-stu-id="38123-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="38123-120">Dacă apar erori în timpul importului, puteți vizualiza jurnalul de execuție sau datele de etapizare pentru a vedea erorile pe care trebuie să le remediați pentru a garanta un import reușit.</span><span class="sxs-lookup"><span data-stu-id="38123-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="38123-121">Dacă trebuie să importați mai mult de un format de fișier, trebuie să creați lucrări de import separate pentru fiecare tip de format.</span><span class="sxs-lookup"><span data-stu-id="38123-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="38123-122">Reatribuiți tranzacțiile cu cardul de credit pentru angajații reziliați</span><span class="sxs-lookup"><span data-stu-id="38123-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="38123-123">După ce o înregistrare a angajatului este terminată, contul Active Directory Domain Services (AD DS) al angajatului este dezactivat.</span><span class="sxs-lookup"><span data-stu-id="38123-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="38123-124">Cu toate acestea, ar putea exista tranzacții active cu cardul de credit care trebuie în continuare cheltuite și rambursate.</span><span class="sxs-lookup"><span data-stu-id="38123-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="38123-125">De la pagina **Tranzacții cu cardul de credit**, puteți reatribui angajatul pentru orice tranzacție cu cardul de credit în cazul în care angajatul asociat a fost reziliat.</span><span class="sxs-lookup"><span data-stu-id="38123-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="38123-126">Selectați una sau mai multe tranzacții cu cardul de credit, apoi selectați **Reatribuiți tranzacțiile**.</span><span class="sxs-lookup"><span data-stu-id="38123-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="38123-127">Apoi puteți selecta un alt angajat căruia să îi atribuiți tranzacțiile cu cardul de credit.</span><span class="sxs-lookup"><span data-stu-id="38123-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="38123-128">După ce tranzacțiile cu cardul de credit au fost realocate, acestea pot fi selectate pentru un raport de cheltuieli și plătite prin procesul obișnuit de rambursare a raportului de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="38123-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
