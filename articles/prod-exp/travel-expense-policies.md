---
title: Configurarea politicilor de cheltuieli
description: Puteți configura politicile de cheltuieli pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieși și cereri de călătorie în Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650109"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="d2109-103">Configurarea politicilor de cheltuieli</span><span class="sxs-lookup"><span data-stu-id="d2109-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2109-104">Puteți defini politicile pe care lucrătorii dvs. trebuie să le urmeze atunci când introduc și depun rapoarte de cheltuieli și cereri de călătorie.</span><span class="sxs-lookup"><span data-stu-id="d2109-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="d2109-105">Implementarea politicilor de cheltuieli vă poate ajuta să gestionați eficient cheltuielile.</span><span class="sxs-lookup"><span data-stu-id="d2109-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="d2109-106">De exemplu, puteți seta o politică pentru cheltuielile hoteliere din New York, care prevede că cheltuielile pe noapte nu pot depăși USD 250.</span><span class="sxs-lookup"><span data-stu-id="d2109-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="d2109-107">Dacă un lucrător depune un raport de cheltuieli sau o cerere de călătorie în care tariful camerei depășește această sumă, sistemul va notifica</span><span class="sxs-lookup"><span data-stu-id="d2109-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="d2109-108">Lucrătorului că suma poliței pentru cheltuială a fost depășită.</span><span class="sxs-lookup"><span data-stu-id="d2109-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="d2109-109">Puteți configura mesajul pe care muncitorul îl va primi atunci când</span><span class="sxs-lookup"><span data-stu-id="d2109-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="d2109-110">definiți politica.</span><span class="sxs-lookup"><span data-stu-id="d2109-110">define the policy.</span></span>      
        
<span data-ttu-id="d2109-111">Puteți defini trei tipuri de politici:</span><span class="sxs-lookup"><span data-stu-id="d2109-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="d2109-112">Avertizare - Permite lucrătorului să depună un raport de cheltuieli sau o cerere de călătorie, dar cheltuielile vor fi marcate pentru toți aprobatorii și</span><span class="sxs-lookup"><span data-stu-id="d2109-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="d2109-113">pentru raportare ulterioară.</span><span class="sxs-lookup"><span data-stu-id="d2109-113">for later reporting.</span></span>        

- <span data-ttu-id="d2109-114">Eroare - Solicită lucrătorului să revizuiască cheltuiala pentru a se conforma politicii înainte de a trimite raportul de cheltuieli sau cererea de călătorie.</span><span class="sxs-lookup"><span data-stu-id="d2109-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="d2109-115">Justificare - Solicită lucrătorului sau unui manager să introducă o justificare pentru depășirea sumei poliței înainte de a trimite raportul de cheltuieli sau cererea de călătorie.</span><span class="sxs-lookup"><span data-stu-id="d2109-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="d2109-116">Sfaturi de politică</span><span class="sxs-lookup"><span data-stu-id="d2109-116">Policy tips</span></span>
<span data-ttu-id="d2109-117">Iată câteva sugestii care vă pot ajuta atunci când creați noi politici pentru gestionarea cheltuielilor.</span><span class="sxs-lookup"><span data-stu-id="d2109-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="d2109-118">Politicile sunt cu dată efectivă și nu vor intra în vigoare dacă politica este creată cu o dată după data la care s-a produs cheltuiala.</span><span class="sxs-lookup"><span data-stu-id="d2109-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="d2109-119">De exemplu, dacă creați o politică nouă astăzi pentru a impune o cheltuială maximă de masă de $50, atunci orice cheltuieli existente introduse începând de ieri nu vor fi comparate cu această politică.</span><span class="sxs-lookup"><span data-stu-id="d2109-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="d2109-120">Când creați o politică pentru o categorie de cheltuieli care poate fi detaliată, luați în considerare adăugarea unei condiții pentru tipul de linie de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="d2109-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="d2109-121">Unele politici, cum ar fi solicitarea unei chitanțe, pot să nu aibă sens pentru liniile detaliate și ar trebui să fie aplicate numai liniei antetului sau unei linii nedefinite.</span><span class="sxs-lookup"><span data-stu-id="d2109-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="d2109-122">Politicile de gestionare a cheltuielilor sunt evaluate în mod implicit în raport cu entitatea sursă.</span><span class="sxs-lookup"><span data-stu-id="d2109-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="d2109-123">Pentru scenariile între companii, puteți seta politica care urmează să fie evaluată în raport cu entitatea de destinație (entitatea care împrumută).</span><span class="sxs-lookup"><span data-stu-id="d2109-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="d2109-124">Pentru a rula politicile împotriva entității de destinație, activați caracteristica „Evaluați politica de cheltuieli împotriva împrumutului entității juridice” în spațiul de lucru **Gestionarea caracteristicilor**.</span><span class="sxs-lookup"><span data-stu-id="d2109-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="d2109-125">Când se evaluează politicile</span><span class="sxs-lookup"><span data-stu-id="d2109-125">When to evaluate policies</span></span>

<span data-ttu-id="d2109-126">În parametrii de gestionare a cheltuielilor, există opțiunea ca fie să evaluați politicile de gestionare a cheltuielilor atunci când este salvată o linie, sau când este trimis un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="d2109-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="d2109-127">Dacă alegeți să evaluați când este salvată o linie, aceasta asigură că utilizatorii vor avea o vizibilitate mai timpurie a ceea ce trebuie să facă pentru a completa raportul de cheltuieli dintr-o dată.</span><span class="sxs-lookup"><span data-stu-id="d2109-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="d2109-128">În caz contrar, puteți întârzia evaluarea politicii și puteți economisi timp dacă aveți validare la final, în timpul trimiterii la fluxul de lucru.</span><span class="sxs-lookup"><span data-stu-id="d2109-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
