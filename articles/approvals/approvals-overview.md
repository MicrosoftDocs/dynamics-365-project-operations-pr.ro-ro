---
title: Prezentare generală a aprobărilor
description: Acest subiect oferă informații despre lucrul cu aprobări în Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368671"
---
# <a name="approvals-overview"></a><span data-ttu-id="08980-103">Prezentare generală a aprobărilor</span><span class="sxs-lookup"><span data-stu-id="08980-103">Approvals overview</span></span>

<span data-ttu-id="08980-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="08980-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="08980-105">Trimiterile de timp, cheltuieli și utilizare a materialelor se deplasează printr-un flux de lucru de aprobare.</span><span class="sxs-lookup"><span data-stu-id="08980-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="08980-106">După ce înregistrările sunt aprobate, tranzacțiile sunt înregistrate în realitate sau timpul este înregistrat în planificare.</span><span class="sxs-lookup"><span data-stu-id="08980-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="08980-107">Flux de lucru de aprobări</span><span class="sxs-lookup"><span data-stu-id="08980-107">Approvals workflow</span></span>
<span data-ttu-id="08980-108">Când creați și trimiteți o intrare de timp, cheltuială sau utilizare a materialului, se creează o înregistrare de aprobare.</span><span class="sxs-lookup"><span data-stu-id="08980-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="08980-109">Aprobatorul de proiect sau managerul examinează și aprobă intrarea.</span><span class="sxs-lookup"><span data-stu-id="08980-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="08980-110">Dacă intrarea este legată de un proiect, valorile reale vor fi create atunci când sunt aprobate.</span><span class="sxs-lookup"><span data-stu-id="08980-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="08980-111">Acest lucru permite urmărirea costurilor și a facturării.</span><span class="sxs-lookup"><span data-stu-id="08980-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="08980-112">Aprobă o intrare</span><span class="sxs-lookup"><span data-stu-id="08980-112">Approve an entry</span></span>
<span data-ttu-id="08980-113">Pagina **Aprobări** vă permite să comutați între diferite vizualizări, astfel încât să puteți vizualiza diferitele tipuri de aprobări.</span><span class="sxs-lookup"><span data-stu-id="08980-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="08980-114">Accesați pagina **Aprobări** și selectați **Cheltuieli**, **Timp**, **Utilizarea materialelor** sau **Retrageri**.</span><span class="sxs-lookup"><span data-stu-id="08980-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="08980-115">Examinați fiecare aprobare și selectați-le pe care doriți să le aprobați.</span><span class="sxs-lookup"><span data-stu-id="08980-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="08980-116">Selectați **Aprobare** pentru a aproba intrările selectate.</span><span class="sxs-lookup"><span data-stu-id="08980-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="08980-117">Sistemul procesează aceste intrări și creează date reale.</span><span class="sxs-lookup"><span data-stu-id="08980-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="08980-118">Respingeți o intrare</span><span class="sxs-lookup"><span data-stu-id="08980-118">Reject an entry</span></span>
<span data-ttu-id="08980-119">În calitate de aprobator de proiect, poate fi necesar să trimiteți o intrare înapoi unui utilizator pentru corectare.</span><span class="sxs-lookup"><span data-stu-id="08980-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="08980-120">Accesați pagina **Aprobări** și selectați intrarea de respins.</span><span class="sxs-lookup"><span data-stu-id="08980-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="08980-121">Selectați **Respinge**.</span><span class="sxs-lookup"><span data-stu-id="08980-121">Select **Reject**.</span></span>
3. <span data-ttu-id="08980-122">Opțional, adăugați un comentariu în caseta de dialog **Comentarii de respingere** pentru a informa utilizatorul de ce este respinsă intrarea.</span><span class="sxs-lookup"><span data-stu-id="08980-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="08980-123">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="08980-123">Select **OK**.</span></span> <span data-ttu-id="08980-124">Intrarea va fi returnată utilizatorului.</span><span class="sxs-lookup"><span data-stu-id="08980-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="08980-125">Anulați aprobarea</span><span class="sxs-lookup"><span data-stu-id="08980-125">Cancel approval</span></span>
<span data-ttu-id="08980-126">În unele cazuri, poate fi necesar să anulați o înregistrare aprobată anterior.</span><span class="sxs-lookup"><span data-stu-id="08980-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="08980-127">Anularea unei înregistrări aprobate anterior va avea un impact financiar.</span><span class="sxs-lookup"><span data-stu-id="08980-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="08980-128">Aprobarea solicitărilor de retragere</span><span class="sxs-lookup"><span data-stu-id="08980-128">Approving recall requests</span></span>
<span data-ttu-id="08980-129">În unele cazuri, este posibil ca un consultant să trebuiască să retragă o înregistrare aprobată anterior.</span><span class="sxs-lookup"><span data-stu-id="08980-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="08980-130">Anularea unei înregistrări aprobate anterior va avea un impact financiar.</span><span class="sxs-lookup"><span data-stu-id="08980-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="08980-131">Aprobatorul de proiect este obligat să aprobe retragerea pentru a inversa tranzacția în Valori reale.</span><span class="sxs-lookup"><span data-stu-id="08980-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="08980-132">Specificați aprobatori de proiect</span><span class="sxs-lookup"><span data-stu-id="08980-132">Specify Project approvers</span></span>
<span data-ttu-id="08980-133">Fiecare proiect are un număr de membri ai echipei de proiect.</span><span class="sxs-lookup"><span data-stu-id="08980-133">Each project has a number of project team members.</span></span> <span data-ttu-id="08980-134">Puteți specifica ce membri ai echipei sunt, de asemenea, aprobatori de proiect.</span><span class="sxs-lookup"><span data-stu-id="08980-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="08980-135">Accesați pagina **Proiecte** și deschideți proiectul din listă.</span><span class="sxs-lookup"><span data-stu-id="08980-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="08980-136">Pe fila **Echipă**, selectați membrul echipei care va fi aprobator de proiect și apoi selectați **Editați**.</span><span class="sxs-lookup"><span data-stu-id="08980-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="08980-137">Configurați câmpul **Aprobator de proiect** la **Da**.</span><span class="sxs-lookup"><span data-stu-id="08980-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="08980-138">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="08980-138">Select **Save**.</span></span>
5. <span data-ttu-id="08980-139">Repetați pașii 2-4 pentru a adăuga aprobatori de proiect adiționali.</span><span class="sxs-lookup"><span data-stu-id="08980-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="08980-140">Configurați managerul utilizatorului</span><span class="sxs-lookup"><span data-stu-id="08980-140">Configure the user's manager</span></span>

1. <span data-ttu-id="08980-141">Accesați **Setări** > **Securitate** > **Utilizatori**.</span><span class="sxs-lookup"><span data-stu-id="08980-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="08980-142">Selectați utilizatorul căruia îi atribuiți un manager și în zona **Informații despre organizație**, selectați managerul din listă.</span><span class="sxs-lookup"><span data-stu-id="08980-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="08980-143">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="08980-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
