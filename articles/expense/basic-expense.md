---
title: Intrare cheltuieli (simplificată)
description: Acest subiect oferă informații despre cum să lucrați cu intrarea cheltuielilor într-o implementare simplificată.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121098"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="4920a-103">Intrare cheltuieli (simplificată)</span><span class="sxs-lookup"><span data-stu-id="4920a-103">Expense entry (lite)</span></span>

<span data-ttu-id="4920a-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="4920a-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4920a-105">Gestionarea cheltuielilor de bază sau simplă este capacitatea de a înregistra cheltuieli simple.</span><span class="sxs-lookup"><span data-stu-id="4920a-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="4920a-106">Puteți înregistra cheltuielile pentru un proiect, iar apoi aprobatorul de proiect le va revizui și aproba.</span><span class="sxs-lookup"><span data-stu-id="4920a-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="4920a-107">Pentru mai multe informații despre capacitățile de cheltuieli din Dynamics 365 Project Operations, consultați [Prezentare generală a cheltuielilor](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4920a-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="4920a-108">Captează o cheltuială de bază</span><span class="sxs-lookup"><span data-stu-id="4920a-108">Capture a basic expense</span></span>

<span data-ttu-id="4920a-109">Vă puteți captura cheltuielile, astfel încât să le puteți trimite aprobatorului.</span><span class="sxs-lookup"><span data-stu-id="4920a-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="4920a-110">Accesați **Cheltuieli** și selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="4920a-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="4920a-111">Pe pagina **Cheltuieli noi**, introduceți informațiile necesare despre cheltuieli, apoi selectați **Salvați**.</span><span class="sxs-lookup"><span data-stu-id="4920a-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="4920a-112">Remite o cheltuială de bază</span><span class="sxs-lookup"><span data-stu-id="4920a-112">Submit a basic expense</span></span>

<span data-ttu-id="4920a-113">După ce ați terminat de capturat toate cheltuielile și sunteți gata să le aprobați, trebuie să le trimiteți.</span><span class="sxs-lookup"><span data-stu-id="4920a-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="4920a-114">Accesați **Cheltuieli** și selectați o cheltuială.</span><span class="sxs-lookup"><span data-stu-id="4920a-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="4920a-115">Sau selectați toate cheltuielile folosind caseta de selectare din antet.</span><span class="sxs-lookup"><span data-stu-id="4920a-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="4920a-116">Selectați **Remitere**.</span><span class="sxs-lookup"><span data-stu-id="4920a-116">Select **Submit**.</span></span> <span data-ttu-id="4920a-117">Sistemul procesează intrările selectate și apoi creează cereri de aprobare a cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="4920a-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="4920a-118">Retrageți o cheltuială de bază</span><span class="sxs-lookup"><span data-stu-id="4920a-118">Recall a basic expense</span></span>

<span data-ttu-id="4920a-119">Când trimiteți o cheltuială din greșeală, o puteți retrage.</span><span class="sxs-lookup"><span data-stu-id="4920a-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="4920a-120">Timpul necesar pentru recuperarea unei înregistrări de cheltuieli depinde de etapa de aprobare a acesteia.</span><span class="sxs-lookup"><span data-stu-id="4920a-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="4920a-121">Dacă aprobatorul nu a aprobat încă înregistrarea, retragerea poate avea loc imediat.</span><span class="sxs-lookup"><span data-stu-id="4920a-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="4920a-122">Cu toate acestea, dacă înregistrarea a fost deja aprobată, aprobatorului i se cere să aprobe retragerea și să inverseze tranzacțiile.</span><span class="sxs-lookup"><span data-stu-id="4920a-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="4920a-123">Accesați **Cheltuieli**, apoi, în lista de cheltuieli, selectați cheltuiala de retras.</span><span class="sxs-lookup"><span data-stu-id="4920a-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="4920a-124">Selectați **Retragere**.</span><span class="sxs-lookup"><span data-stu-id="4920a-124">Select **Recall**.</span></span> <span data-ttu-id="4920a-125">Dacă înregistrarea cheltuielilor nu a fost încă aprobată, sistemul o retrage imediat.</span><span class="sxs-lookup"><span data-stu-id="4920a-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="4920a-126">Dacă înregistrarea cheltuielilor a fost deja aprobată, se creează o cerere de retragere pentru a notifica aprobatorului că doriți să inversați cheltuielile.</span><span class="sxs-lookup"><span data-stu-id="4920a-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="4920a-127">Aprobatorul va confirma apoi că se poate face inversarea, iar intrarea va fi returnată.</span><span class="sxs-lookup"><span data-stu-id="4920a-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="4920a-128">Șterge o cheltuială de bază</span><span class="sxs-lookup"><span data-stu-id="4920a-128">Delete a basic expense</span></span>

<span data-ttu-id="4920a-129">Cheltuielile care nu au fost încă trimise pot fi șterse.</span><span class="sxs-lookup"><span data-stu-id="4920a-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="4920a-130">Pentru a șterge o cheltuială care a fost deja trimisă, trebuie mai întâi să o retrageți.</span><span class="sxs-lookup"><span data-stu-id="4920a-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="4920a-131">Consultați și</span><span class="sxs-lookup"><span data-stu-id="4920a-131">See also</span></span>

- [<span data-ttu-id="4920a-132">Prezentare generală a aprobărilor</span><span class="sxs-lookup"><span data-stu-id="4920a-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
