---
title: Rapoarte de cheltuieli și mai mulți aprobatori
description: Acest subiect oferă informații despre rapoartele de cheltuieli care necesită aprobarea mai multor persoane.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002071"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="91210-103">Rapoarte de cheltuieli și mai mulți aprobatori</span><span class="sxs-lookup"><span data-stu-id="91210-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="91210-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="91210-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91210-105">În funcție de politicile de aprobare a cheltuielilor organizației dvs., mai mult de o persoană ar trebui să aprobe un raport de cheltuieli trimis.</span><span class="sxs-lookup"><span data-stu-id="91210-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="91210-106">Când configurați procesul fluxului de lucru pentru aprobarea raportului de cheltuieli, puteți adăuga elemente de flux de lucru care includ sarcini sau pași pentru unul sau mai mulți aprobatori de rapoarte de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="91210-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="91210-107">De exemplu, s-ar putea să solicitați ca toate rapoartele de cheltuieli să fie aprobate de două persoane separate, managerul angajatului care a trimis raportul și coordonatorul de conturi de plată.</span><span class="sxs-lookup"><span data-stu-id="91210-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="91210-108">Dacă decideți să solicitați mai mulți aprobatori de rapoarte de cheltuieli, puteți adăuga elementele fluxului de lucru în oricare dintre următoarele moduri:</span><span class="sxs-lookup"><span data-stu-id="91210-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="91210-109">Adăugați un element de aprobare care are un singur pas.</span><span class="sxs-lookup"><span data-stu-id="91210-109">Add one approval element that has one step.</span></span> <span data-ttu-id="91210-110">De exemplu, pasul ar putea necesita ca un raport de cheltuieli să fie atribuit unui grup de utilizatori și să fie aprobat de 50% din membrii grupului de utilizatori.</span><span class="sxs-lookup"><span data-stu-id="91210-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="91210-111">Adăugați un element de aprobare care are mai mulți pași.</span><span class="sxs-lookup"><span data-stu-id="91210-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="91210-112">De exemplu, elementul de aprobare poate avea următorii pași:</span><span class="sxs-lookup"><span data-stu-id="91210-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="91210-113">Managerul angajatului care a depus raportul de cheltuieli îl aprobă.</span><span class="sxs-lookup"><span data-stu-id="91210-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="91210-114">Grefierul de conturi de plată verifică chitanțele și articolele raportului de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="91210-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="91210-115">Proprietarul bugetului aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="91210-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="91210-116">Adăugați mai multe elemente de aprobare, fiecare dintre acestea având un singur pas.</span><span class="sxs-lookup"><span data-stu-id="91210-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="91210-117">De exemplu, puteți adăuga un element de aprobare separat pentru fiecare dintre pașii următori:</span><span class="sxs-lookup"><span data-stu-id="91210-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="91210-118">Managerul angajatului aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="91210-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="91210-119">Proprietarul bugetului aprobă raportul de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="91210-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]