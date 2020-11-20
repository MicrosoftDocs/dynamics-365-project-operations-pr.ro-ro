---
title: Maparea proiectelor și activităților într-o linie de ofertă bazată pe proiect
description: Acest subiect oferă informații despre cum să mapați proiectele și sarcinile la o linie de activități bazată pe proiecte.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130728"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="3ddfe-103">Maparea proiectelor și activităților într-o linie de ofertă bazată pe proiect</span><span class="sxs-lookup"><span data-stu-id="3ddfe-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="3ddfe-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="3ddfe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ddfe-105">Pe liniile de ofertă bazate pe proiect, puteți mapa sarcinile specifice unui proiect care este deja asociat cu o linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="3ddfe-106">Când asociați sarcinile la o linie de ofertă, următoarele elemente definite pe linia de ofertă se vor aplica numai acelor activități:</span><span class="sxs-lookup"><span data-stu-id="3ddfe-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="3ddfe-107">Metoda de facturare</span><span class="sxs-lookup"><span data-stu-id="3ddfe-107">Billing method</span></span>
- <span data-ttu-id="3ddfe-108">Opțiuni de posibilitate de tarifare</span><span class="sxs-lookup"><span data-stu-id="3ddfe-108">Chargeability options</span></span>
- <span data-ttu-id="3ddfe-109">Limite de nedepășire</span><span class="sxs-lookup"><span data-stu-id="3ddfe-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="3ddfe-110">Clienți</span><span class="sxs-lookup"><span data-stu-id="3ddfe-110">Customers</span></span>

<span data-ttu-id="3ddfe-111">De exemplu, s-ar putea să aveți un proiect în care o fază este cu preț fix și toate celelalte faze sunt timp și materiale.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="3ddfe-112">În acest caz, puteți asocia prima fază și toate sarcinile sale secundare liniei de ofertă pentru acea fază cu o metodă de facturare cu preț fix.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="3ddfe-113">Apoi, puteți asocia toate celelalte faze liniei de ofertă bazate pe timp și materiale.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="3ddfe-114">Asociați activități la linii de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="3ddfe-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="3ddfe-115">Puteți asocia sarcini cu liniile de ofertă din următoarele locații:</span><span class="sxs-lookup"><span data-stu-id="3ddfe-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="3ddfe-116">Pagina **Proiect** > fila **Facturarea activităților** (optim)</span><span class="sxs-lookup"><span data-stu-id="3ddfe-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="3ddfe-117">Pagina **Linie de ofertă** fila > **Activități taxabile**</span><span class="sxs-lookup"><span data-stu-id="3ddfe-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="3ddfe-118">De pe pagina de proiect</span><span class="sxs-lookup"><span data-stu-id="3ddfe-118">From the Project page</span></span>

<span data-ttu-id="3ddfe-119">Pagina **Proiect** oferă experiența optimă pentru asocierea activităților la liniile de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="3ddfe-120">Puteți utiliza această pagină pentru a selecta mai multe activități și a le asocia pe toate, plus sarcinile secundare, la linia de ofertă selectată.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="3ddfe-121">Pe fila **General** unei linii de ofertă de estimare bazate pe proiect, verificați dacă câmpul **Proiect** este completat.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="3ddfe-122">În câmpul **Activități incluse**, selectați **Numai activități selectate**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="3ddfe-123">Salvați linia de ofertă bazată de proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-123">Save the project-based quote line.</span></span> <span data-ttu-id="3ddfe-124">Când formularul se reîmprospătează, se afișează fila **Activități taxabile**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="3ddfe-125">Pe fila **General**, selectați linkul pentru proiect din câmpul **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="3ddfe-126">Pe pagina **Proiect** selectați fila **Facturare activități**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="3ddfe-127">În a doua grilă, care se aplică configurării de facturare specifice sarcinilor, selectați una sau mai multe sarcini și apoi selectați **Asociați liniile de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="3ddfe-128">În pagina de dialog care apare, selectați o linie de ofertă care afișează liniile de ofertă bazate pe proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="3ddfe-129">În câmpul **Tipul de facturare**, indicați dacă aceste sarcini sunt taxabile sau neimpozabile.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="3ddfe-130">Bifați caseta de selectare pentru a indica dacă asocierea ar trebui să includă sarcini secundare ale sarcinilor selectate.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="3ddfe-131">Bifând caseta se vor asocia sarcinile secundare ale sarcinilor selectate la linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="3ddfe-132">Selectați **OK** pentru a închide dialogul.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="3ddfe-133">Din pagina liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="3ddfe-133">From the Quote line page</span></span>

<span data-ttu-id="3ddfe-134">Puteți asocia sarcinile proiectului pentru a oferta linii din fila **Activități taxabile** pe pagina **Linie de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="3ddfe-135">Locul optim pentru asocierea sarcinilor proiectului la liniile de ofertă este pe fila **Facturarea sarcinilor** pe pagina **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="3ddfe-136">Dacă asociați sarcini din fila **Sarcini taxabile** pe pagina **Linie de ofertă**, trebuie să asociați manual fiecare proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="3ddfe-137">Pe fila **General** a unei linii de ofertă de estimare bazate pe proiect, verificați că este un proiect selectat în câmpul **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="3ddfe-138">În câmpul **Activități incluse**, selectați **Numai activități selectate**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="3ddfe-139">Salvați linia de ofertă bazată de proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-139">Save the project-based quote line.</span></span> <span data-ttu-id="3ddfe-140">Când formularul se reîmprospătează, se afișează fila **Activități taxabile**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="3ddfe-141">Pe fila **Sarcini taxabile**, selectați **Adăugați o sarcină de linie de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="3ddfe-142">Pe pagina **Activitatea liniei de ofertă**, în câmpul **Activități**, selectați sarcina și în câmpul **Tipul de facturare**, selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="3ddfe-143">Închideți pagina.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-143">Close the page.</span></span> <span data-ttu-id="3ddfe-144">Activitatea selectată este acum asociată liniei de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="3ddfe-145">Dezasociați activități din linii de ofertă bazate pe proiect</span><span class="sxs-lookup"><span data-stu-id="3ddfe-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="3ddfe-146">De pe pagina de proiect</span><span class="sxs-lookup"><span data-stu-id="3ddfe-146">From the Project page</span></span>

<span data-ttu-id="3ddfe-147">Această metodă oferă cea mai optimă experiență pentru dezasocierea activităților din linii de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="3ddfe-148">Puteți selecta mai multe activități și le puteți dezasocia pe toate, plus activitățile lor secundare, din linia de ofertă selectată.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="3ddfe-149">Pe fila **General** a unei linii de ofertă de estimare bazate pe proiect, în câmpul **Proiect**, selectați linkul de proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="3ddfe-150">Pe pagina **Proiect** selectați fila **Facturare activități**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="3ddfe-151">În a doua grilă, care se aplică configurării de facturare specifice sarcinilor, selectați una sau mai multe sarcini și apoi selectați **Dezasociați liniile de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="3ddfe-152">În pagina de dialog care apare, selectați o linie de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="3ddfe-153">Bifați caseta de selectare pentru a indica dacă asocierea ar trebui să fie eliminată din activitățile secundare ale activităților selectate.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="3ddfe-154">Bifând caseta se vor dezasocia sarcinile secundare ale sarcinilor selectate la linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="3ddfe-155">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-155">Select **OK**.</span></span> <span data-ttu-id="3ddfe-156">Un mesaj de avertizare vă informează că, dacă eliminați această asociere, orice realitate înregistrată anterior în activitate ar putea fi inversată.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="3ddfe-157">Selectați **OK** pentru a continua și a elimina asocierea dintre activitate și linia de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="3ddfe-158">Din pagina liniei de ofertă</span><span class="sxs-lookup"><span data-stu-id="3ddfe-158">From the Quote line page</span></span>

<span data-ttu-id="3ddfe-159">Puteți dezasocia sarcinile proiectului pentru a oferta linii din fila **Activități taxabile** pe pagina **Linie de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="3ddfe-160">Pe fila **Sarcini taxabile**, selectați **Ștergeți o activitate de linie de ofertă**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="3ddfe-161">Selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-161">Select **OK**.</span></span> <span data-ttu-id="3ddfe-162">Un mesaj de avertizare vă informează că, dacă eliminați această asociere, orice realitate înregistrată anterior în activitate ar putea fi inversată.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="3ddfe-163">Selectați **OK** pentru a continua și a elimina asocierea dintre activitate și linia de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="3ddfe-164">Această procedură nu șterge activtiatea din proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="3ddfe-165">Elimină doar asocierea activității din linia de ofertă bazată pe proiect.</span><span class="sxs-lookup"><span data-stu-id="3ddfe-165">It only removes the task association from the project-based quote line.</span></span>
