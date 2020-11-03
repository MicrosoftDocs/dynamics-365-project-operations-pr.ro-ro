---
title: Estimări de cheltuieli
description: Acest subiect furnizează informații despre definirea sau estimarea cheltuielilor bazate pe proiecte.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082718"
---
# <a name="expense-estimates"></a><span data-ttu-id="0e4d8-103">Estimări de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="0e4d8-103">Expense estimates</span></span>
<span data-ttu-id="0e4d8-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="0e4d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e4d8-105">Împreună cu definirea estimărilor bazate pe resurse, Dynamics 365 Project Operations permite managerilor de proiect să definească cheltuielile bazate pe proiect pentru fiecare proiect.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="0e4d8-106">Fiecare articol de cheltuială poate fi asociat cu o anumită activitate de proiect sau categorie de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="0e4d8-107">Categoriile de cheltuieli sunt de obicei definite la nivel organizațional.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="0e4d8-108">Prețurile pentru fiecare categorie de cheltuieli sunt de obicei definite în următoarea ierarhie:</span><span class="sxs-lookup"><span data-stu-id="0e4d8-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="0e4d8-109">Organizație</span><span class="sxs-lookup"><span data-stu-id="0e4d8-109">Organization</span></span>
- <span data-ttu-id="0e4d8-110">Client</span><span class="sxs-lookup"><span data-stu-id="0e4d8-110">Customer</span></span>
- <span data-ttu-id="0e4d8-111">Ofertă/contract</span><span class="sxs-lookup"><span data-stu-id="0e4d8-111">Quote/contract</span></span>

<span data-ttu-id="0e4d8-112">Parcurgeți pașii următori pentru a vizualiza, adăuga sau șterge o cheltuială a proiectului.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="0e4d8-113">Accesați **Proiecte** , și selectați proiectul la care doriți să lucrați.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="0e4d8-114">Selectați fila **Estimări ale proiectului** și vizualizați lista cheltuielilor proiectului.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="0e4d8-115">Selectați **Cheltuieli noi** pentru a adăuga o cheltuială.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="0e4d8-116">Sau selectați o cheltuială de șters, apoi selectați **Ștergeți cheltuiala**.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="0e4d8-117">Următoarele atribute sunt definite pentru fiecare element rând de cheltuieli:</span><span class="sxs-lookup"><span data-stu-id="0e4d8-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="0e4d8-118">**Categorie** : Grupările comune utilizate pentru a descrie toate cheltuielile suportate pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="0e4d8-119">**Data de început** : Data la care se estimează că va fi efectuată cheltuiala.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="0e4d8-120">**Cantitate** : Numărul estimat de articole de cheltuieli pentru o anumită categorie.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="0e4d8-121">**Preț de cost unitar** : Prețul unitar utilizat pentru calcularea costului cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="0e4d8-122">**Preț unitar de vânzare** : Prețul unitar utilizat pentru calcularea prețurilor de vânzare a cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="0e4d8-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

