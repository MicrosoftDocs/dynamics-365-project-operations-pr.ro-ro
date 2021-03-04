---
title: Aprobatori multipli pe un raport de cheltuieli
description: Acest subiect oferă informații despre rapoartele de cheltuieli care necesită aprobarea de către mai multe persoane.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960622"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="83b54-103">Aprobatori multipli pe un raport de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="83b54-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="83b54-104">În funcție de politicile de aprobare a cheltuielilor organizației dvs., mai mult de o persoană ar trebui să aprobe un raport de cheltuieli care este prezentat de un angajat.</span><span class="sxs-lookup"><span data-stu-id="83b54-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="83b54-105">Când configurați procesul fluxului de lucru pentru aprobarea raportului de cheltuieli, puteți adăuga elemente de flux de lucru care includ sarcini sau pași pentru unul sau mai mulți aprobatori de rapoarte de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="83b54-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="83b54-106">De exemplu, s-ar putea să solicitați ca toate rapoartele de cheltuieli să fie aprobate mai întâi, managerul angajatului care a trimis raportul și apoi de coordonatorul de conturi de plată.</span><span class="sxs-lookup"><span data-stu-id="83b54-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="83b54-107">Dacă decideți să solicitați mai mulți aprobatori de rapoarte de cheltuieli, puteți adăuga elementele fluxului de lucru în oricare dintre următoarele moduri:</span><span class="sxs-lookup"><span data-stu-id="83b54-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="83b54-108">Adăugați un element de aprobare care are un singur pas.</span><span class="sxs-lookup"><span data-stu-id="83b54-108">Add one approval element that has one step.</span></span> <span data-ttu-id="83b54-109">De exemplu, pasul ar putea necesita ca un raport de cheltuieli să fie atribuit unui grup de utilizatori și să fie aprobat de 50% din membrii grupului de utilizatori.</span><span class="sxs-lookup"><span data-stu-id="83b54-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="83b54-110">Adăugați un element de aprobare care are mai mulți pași.</span><span class="sxs-lookup"><span data-stu-id="83b54-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="83b54-111">De exemplu, elementul de aprobare poate avea următorii pași:</span><span class="sxs-lookup"><span data-stu-id="83b54-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="83b54-112">Managerul angajatului care a depus raportul de cheltuieli îl aprobă.</span><span class="sxs-lookup"><span data-stu-id="83b54-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="83b54-113">Grefierul de conturi de plată verifică chitanțele și articolele raportului de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="83b54-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="83b54-114">Proprietarul bugetului aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="83b54-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="83b54-115">Adăugați mai multe elemente de aprobare, fiecare dintre acestea având un singur pas.</span><span class="sxs-lookup"><span data-stu-id="83b54-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="83b54-116">De exemplu, puteți adăuga un element de aprobare separat pentru fiecare dintre pașii următori:</span><span class="sxs-lookup"><span data-stu-id="83b54-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="83b54-117">Managerul angajatului aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="83b54-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="83b54-118">Proprietarul bugetului aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="83b54-118">The budget owner approves the expense report.</span></span>
