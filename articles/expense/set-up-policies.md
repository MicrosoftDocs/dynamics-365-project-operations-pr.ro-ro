---
title: Definiți politicile de cheltuieli
description: Puteți defini politicile de cheltuieli pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieli și cereri de călătorie.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896656"
---
# <a name="define-expense-policies"></a><span data-ttu-id="0a5bf-103">Definiți politicile de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="0a5bf-103">Define expense policies</span></span>

<span data-ttu-id="0a5bf-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="0a5bf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0a5bf-105">Puteți defini politicile pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieli și cereri de călătorie.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="0a5bf-106">Implementarea politicilor de cheltuieli vă poate ajuta să gestionați eficient cheltuielile.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="0a5bf-107">De exemplu, puteți seta o politică pentru cheltuielile hoteliere din New York, care prevede că cheltuielile pe noapte nu pot depăși USD 250.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="0a5bf-108">Dacă un lucrător depune un raport de cheltuieli sau o cerere de călătorie în cazul în care tariful camerei depășește această sumă, sistemul va notifica</span><span class="sxs-lookup"><span data-stu-id="0a5bf-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="0a5bf-109">Lucrătorului că suma poliței pentru cheltuială a fost depășită.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="0a5bf-110">Puteți configura mesajul pe care muncitorul îl va primi atunci când</span><span class="sxs-lookup"><span data-stu-id="0a5bf-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="0a5bf-111">definiți politica.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-111">define the policy.</span></span>      
        
<span data-ttu-id="0a5bf-112">Puteți defini trei tipuri de politici:</span><span class="sxs-lookup"><span data-stu-id="0a5bf-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="0a5bf-113">**Avertizare**: Permite lucrătorului să depună un raport de cheltuieli sau o cerere de călătorie, dar cheltuielile vor fi marcate pentru toți aprobatorii și</span><span class="sxs-lookup"><span data-stu-id="0a5bf-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="0a5bf-114">pentru raportare ulterioară.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-114">for later reporting.</span></span>        

- <span data-ttu-id="0a5bf-115">**Eroare**: Solicită lucrătorului să revizuiască cheltuiala pentru a se conforma politicii înainte de a trimite raportul de cheltuieli sau cererea de călătorie.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="0a5bf-116">**Justificare**: Solicită lucrătorului sau unui manager să introducă o justificare pentru depășirea sumei poliței înainte de a trimite raportul de cheltuieli sau cererea de călătorie.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="0a5bf-117">Sfaturi de politică</span><span class="sxs-lookup"><span data-stu-id="0a5bf-117">Policy tips</span></span>
<span data-ttu-id="0a5bf-118">Iată câteva sugestii care vă pot ajuta atunci când creați noi politici pentru gestionarea cheltuielilor:</span><span class="sxs-lookup"><span data-stu-id="0a5bf-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="0a5bf-119">Politicile intră în vigoare, ceea ce înseamnă că o politică nu va intra în vigoare dacă este creată cu o dată după data la care s-a produs cheltuiala.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="0a5bf-120">De exemplu, creați astăzi o nouă politică pentru a impune o cheltuială maximă de masă de $50.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="0a5bf-121">Orice cheltuieli existente introduse începând de ieri nu vor fi comparate cu această politică.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="0a5bf-122">Când creați o politică pentru o categorie de cheltuieli care poate fi detaliată, luați în considerare adăugarea unei condiții pentru tipul de linie de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="0a5bf-123">Este posibil ca unele politici, cum ar fi solicitarea unei chitanțe, să nu aibă sens pentru liniile detaliate.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="0a5bf-124">În această situație, politica se aplică numai liniei de antet sau unei linii ne-detaliate.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="0a5bf-125">Politicile de gestionare a cheltuielilor sunt evaluate în mod implicit în raport cu entitatea sursă.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="0a5bf-126">Pentru scenariile între companii, puteți seta politica care urmează să fie evaluată în raport cu entitatea de destinație (entitatea care împrumută).</span><span class="sxs-lookup"><span data-stu-id="0a5bf-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="0a5bf-127">Pentru a rula politicile împotriva entității de destinație, activați caracteristica **Evaluați politica de cheltuieli împotriva împrumutului entității juridice** în spațiul de lucru **Gestionarea caracteristicilor**.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="0a5bf-128">Când se evaluează politicile</span><span class="sxs-lookup"><span data-stu-id="0a5bf-128">When to evaluate policies</span></span>

<span data-ttu-id="0a5bf-129">În parametrii de gestionare a cheltuielilor, puteți selecta să evaluați politicile de gestionare a cheltuielilor atunci când este salvată o linie sau când este trimis un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="0a5bf-130">Dacă alegeți să evaluați când este salvată o linie, utilizatorii vor avea o vizibilitate mai timpurie a ceea ce trebuie să facă pentru a completa raportul de cheltuieli dintr-o dată.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="0a5bf-131">În caz contrar, puteți întârzia evaluarea politicii și puteți economisi timp validând la final, în timpul trimiterii la fluxul de lucru.</span><span class="sxs-lookup"><span data-stu-id="0a5bf-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
