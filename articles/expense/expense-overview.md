---
title: Prezentare generală a cheltuielilor
description: Acest subiect oferă informații despre lucrul cu funcționalitatea cheltuieli în Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c4e2f441e1c4b1bcba5bca292b8075b4334a004d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276588"
---
# <a name="expense-home-page"></a><span data-ttu-id="ec86b-103">Pagina principală a cheltuielilor</span><span class="sxs-lookup"><span data-stu-id="ec86b-103">Expense home page</span></span>

<span data-ttu-id="ec86b-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="ec86b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ec86b-105">Dynamics 365 Project Operations sprijină capacitatea de procesare a cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="ec86b-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="ec86b-106">Procesarea cheltuielilor are loc cu sau fără proiecte utilizând un flux de lucru personalizabil de politici, categorii de tranzacții și aprobări.</span><span class="sxs-lookup"><span data-stu-id="ec86b-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="ec86b-107">În Project Operations, există două modele de implementare acceptate pentru cheltuieli:</span><span class="sxs-lookup"><span data-stu-id="ec86b-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="ec86b-108">**Completă**: Implementarea completă este disponibilă pentru **Project Operations pentru resurse/scenarii care nu sunt bazate pe stoc** sau **Project Operations pentru scenarii bazate pe comenzi de producție**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="ec86b-109">**De bază**: Implementarea de bază este disponibilă pentru **Project Operations pentru resurse/scenarii bazate pe stoc** și **Implementare simplă - gestionați facturarea proforma**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="ec86b-110">Integral</span><span class="sxs-lookup"><span data-stu-id="ec86b-110">Full</span></span> 
<span data-ttu-id="ec86b-111">Implementarea completă a cheltuielilor oferă o aplicare completă a politicilor care include posibilitatea de a crea politici, cum ar fi:</span><span class="sxs-lookup"><span data-stu-id="ec86b-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="ec86b-112">Limite de categorii de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="ec86b-112">Expense category limits</span></span>
  - <span data-ttu-id="ec86b-113">Călătorie</span><span class="sxs-lookup"><span data-stu-id="ec86b-113">Travel</span></span>
  - <span data-ttu-id="ec86b-114">Per diem</span><span class="sxs-lookup"><span data-stu-id="ec86b-114">Per diem</span></span>
  - <span data-ttu-id="ec86b-115">Importuri card de credit</span><span class="sxs-lookup"><span data-stu-id="ec86b-115">Credit card imports</span></span>
  - <span data-ttu-id="ec86b-116">Primirea recunoașterii optice a caracterelor</span><span class="sxs-lookup"><span data-stu-id="ec86b-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="ec86b-117">De bază</span><span class="sxs-lookup"><span data-stu-id="ec86b-117">Basic</span></span> 
<span data-ttu-id="ec86b-118">Scenariul de implementare a cheltuielilor de bază vă permite doar să înregistrați cheltuielile de bază pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="ec86b-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="ec86b-119">Pentru informații suplimentare, consultați [Intrare cheltuială (simplificată)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="ec86b-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="ec86b-120">Determinarea Implementării de cheltuială</span><span class="sxs-lookup"><span data-stu-id="ec86b-120">Determine your Expense deployment</span></span>
<span data-ttu-id="ec86b-121">Pentru a determina dacă executați implementarea de gestionare a cheltuielilor de bază, verificați dacă adresa URL se termină cu **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="ec86b-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]