---
title: Cum particularizez fluxul de business Fazele proiectului?
description: Generalități despre particularizarea fluxului de business Fazele proiectului.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f95677c56b745bf7900ad503596c93f1e722281
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286173"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="024a5-103">Cum particularizez fluxul de business Fazele proiectului?</span><span class="sxs-lookup"><span data-stu-id="024a5-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="024a5-104">Există o limitare cunoscută în versiunile anterioare ale aplicației Project Service, și anume faptul că numele de faze în fluxul de business Fazele Proiectului trebuie să corespundă exact numele așteptate în engleză (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="024a5-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="024a5-105">În caz contrar, logica de business, care se bazează pe numele de faze din limba engleză, nu funcționează conform așteptărilor.</span><span class="sxs-lookup"><span data-stu-id="024a5-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="024a5-106">De aceea nu vedeți acțiuni familiare cum ar fi **Comutare proces** sau **Editare proces** disponibile pe formularul de proiect iar particularizarea fluxului de business nu este încurajată.</span><span class="sxs-lookup"><span data-stu-id="024a5-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="024a5-107">Această limitare a fost tratată în versiunea 2.4.5.48 și ulterioară.</span><span class="sxs-lookup"><span data-stu-id="024a5-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="024a5-108">Acest articol oferă soluții sugerate în cazul în care aveți nevoie să particularizați fluxul de business implicit pentru versiunile anterioare.</span><span class="sxs-lookup"><span data-stu-id="024a5-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="024a5-109">Logica de business cere o potrivire exactă cu numele de fază din limba engleză</span><span class="sxs-lookup"><span data-stu-id="024a5-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="024a5-110">Fluxul de business Fazele proiectului include logică de business care conduce la următoarele comportamente în aplicație:</span><span class="sxs-lookup"><span data-stu-id="024a5-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="024a5-111">Atunci când proiectul este asociat cu o ofertă, codul setează fluxul de business la faza **Quote** (ofertă).</span><span class="sxs-lookup"><span data-stu-id="024a5-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="024a5-112">Atunci când proiectul este asociat cu un contract, codul setează fluxul de business la faza **Plan** (planificare).</span><span class="sxs-lookup"><span data-stu-id="024a5-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="024a5-113">Când fluxul de business avansează la faza **Close** (închidere), înregistrarea proiectului este dezactivată.</span><span class="sxs-lookup"><span data-stu-id="024a5-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="024a5-114">Când proiectul este dezactivat, formularul de proiect și structura detaliată a proiectului (WBS) sunt setate la acces doar de citire, rezervările resurselor specifice sunt eliberate, iar orice liste de prețuri asociate sunt dezactivate.</span><span class="sxs-lookup"><span data-stu-id="024a5-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="024a5-115">Această logică de business se bazează pe numele în limba engleză pentru fazele de proiect.</span><span class="sxs-lookup"><span data-stu-id="024a5-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="024a5-116">Această dependență de numele de fază din limba engleză este motivul principal pentru care nu este încurajată personalizarea fluxului de business Faze proiect, precum și motivul pentru care nu puteți vedea acțiunile comune de flux de business precum **Comutare proces** sau **Editare proces** pe entitatea proiectului.</span><span class="sxs-lookup"><span data-stu-id="024a5-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="024a5-117">Ce se întâmplă în cazul în care numele de fază nu corespund numelor din engleză?</span><span class="sxs-lookup"><span data-stu-id="024a5-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="024a5-118">În aplicația Project Service versiunea 1.x pe platforma 8.2, atunci numele de fază din fluxul de business nu corespund precis numelor de fază din limba engleză, se sare logica de business care stabilește faza corectă pentru oferte sau contracte sau cea care închide proiectul.</span><span class="sxs-lookup"><span data-stu-id="024a5-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="024a5-119">Nu există se afișează mesaje de eroare.</span><span class="sxs-lookup"><span data-stu-id="024a5-119">No error messages are displayed.</span></span> <span data-ttu-id="024a5-120">Prin urmare, se pare că aveți posibilitatea să particularizați fluxul de business Faze proiect.</span><span class="sxs-lookup"><span data-stu-id="024a5-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="024a5-121">Cu toate acestea, veți vedea că nu va funcționa niciunul dintre procesele automate pentru oferte, contracte și închiderea proiectului.</span><span class="sxs-lookup"><span data-stu-id="024a5-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="024a5-122">În aplicația Project Service versiunea 2.4.4.30 sau mai veche pe platforma 9.0, a existat o schimbare arhitecturală semnificativă la fluxurile de business, care a necesitat o rescriere a logicii de business a fluxului de business.</span><span class="sxs-lookup"><span data-stu-id="024a5-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="024a5-123">Ca urmare, în cazul în care numele de faze ale procesului nu corespund cu numele în engleză așteptate, primiți un mesaj de eroare.</span><span class="sxs-lookup"><span data-stu-id="024a5-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="024a5-124">Prin urmare, în cazul în care doriți să particularizați fluxul de business Faze proiect pentru entitatea de proiect, puteți adăuga doar faze noi la fluxul de business implicit pentru entitatea proiectului, păstrând fazele **Quotes** (oferte), **Plan** (planificare) și **Close** (închidere) așa cum sunt.</span><span class="sxs-lookup"><span data-stu-id="024a5-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="024a5-125">Această restricție asigură că nu veți primi erori de la logica de business, care se așteaptă la numele de faze în limba engleză fluxul de business.</span><span class="sxs-lookup"><span data-stu-id="024a5-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="024a5-126">În versiunea 2.4.5.48 sau ulterioară, logica de business descrisă în acest articol a fost eliminată din fluxul de business implicit pentru entitatea de proiect.</span><span class="sxs-lookup"><span data-stu-id="024a5-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="024a5-127">Actualizarea la versiunea respectivă sau ulterioară vă va permite să personalizați sau să înlocuiți fluxul de business implicit cu unul propriu.</span><span class="sxs-lookup"><span data-stu-id="024a5-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="024a5-128">Soluții pentru versiunile anterioare</span><span class="sxs-lookup"><span data-stu-id="024a5-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="024a5-129">Dacă actualizarea nu este posibilă, aveți posibilitatea să particularizați fluxul de business Faze proiect pentru entitatea de proiect într-unul dintre următoarele două moduri:</span><span class="sxs-lookup"><span data-stu-id="024a5-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="024a5-130">Adăugați faze suplimentare la configurația implicită, păstrând numele de fază în limba engleză pentru **Quote** (ofertă), **Plan** (planificare) și **Close** (închidere).</span><span class="sxs-lookup"><span data-stu-id="024a5-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Captură de ecran cu adăugarea de faze la configurația implicită](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="024a5-132">Creați-vă propriul flux de business și faceți din acesta fluxul de business principal pentru entitatea de proiect, lucru care vă permite să aveți orice nume de fază doriți.</span><span class="sxs-lookup"><span data-stu-id="024a5-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="024a5-133">Cu toate acestea, dacă doriți să utilizați aceleași faze de proiect standard **Ofertă**, **Planificare** și **Închidere**, trebuie să faceți unele particularizări care sunt implicate de numele de fază personalizate.</span><span class="sxs-lookup"><span data-stu-id="024a5-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="024a5-134">Logica mai complexă se află la închiderea proiectului, pe care îl puteți încă declanșa prin simpla dezactivare a înregistrării proiectului.</span><span class="sxs-lookup"><span data-stu-id="024a5-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Particularizare BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="024a5-136">Considerente suplimentare pentru aplicația Project Service versiunea 2.4.4.30 sau mai veche pe platforma 9.0</span><span class="sxs-lookup"><span data-stu-id="024a5-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="024a5-137">În Project Service 2.4.4.30 sau mai timpuriu pe platforma 9.0, la un flux de business personalizat câmpul **Nume fază** din entitatea proiectului utilizată în diagrama **Proiect după fază** și vizualizările listă de proiecte de listă nu se actualizează, deoarece este cuplat la fluxul implicit de business Faze proiect.</span><span class="sxs-lookup"><span data-stu-id="024a5-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="024a5-138">Puteți remedia această problemă cu etapele de mai jos:</span><span class="sxs-lookup"><span data-stu-id="024a5-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="024a5-139">Adăugați un câmp personalizat pentru a capta faza de flux de business curentă care este actualizată pe măsură ce utilizatorul avansează prin fluxul de business.</span><span class="sxs-lookup"><span data-stu-id="024a5-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="024a5-140">Modificați diagrama **Proiect după fază** pentru a lucra cu câmpul dumneavoastră particularizat în loc de configurația implicită.</span><span class="sxs-lookup"><span data-stu-id="024a5-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="024a5-141">Pași pentru a vă crea propriul flux de business pentru entitatea de proiect</span><span class="sxs-lookup"><span data-stu-id="024a5-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="024a5-142">Pentru a vă crea propriul flux de business pentru entitatea de proiect, faceți următoarele:</span><span class="sxs-lookup"><span data-stu-id="024a5-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="024a5-143">Accesați **Setări** > **Centru procese**.</span><span class="sxs-lookup"><span data-stu-id="024a5-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="024a5-144">Nu copiați fluxul de business Faze proiect deoarece acest lucru copiază și logica de business a Project Service.</span><span class="sxs-lookup"><span data-stu-id="024a5-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Creare proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="024a5-146">Utilizați Proiectantul de procese pentru a crea numele de fază pe care le doriți.</span><span class="sxs-lookup"><span data-stu-id="024a5-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="024a5-147">Dacă doriți aceeași funcționalitate cu fazele implicite pentru **Ofertă**, **Planificare** și **Închidere**, va trebui să creați acest lucru pe baza numelor de fază ale fluxului dvs. de business personalizat.</span><span class="sxs-lookup"><span data-stu-id="024a5-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Captură de ecran cu Proiectantul de Procese utilizat pentru personalizarea BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="024a5-149">În Proiectantul de procese, faceți clic pe **Ordonare fluxuri de proces** pentru a face ca fluxul de business personalizat să fie fluxul de business primar pentru entitatea proiectului, mutându-l deasupra fluxului de business Faze proiect în partea de sus a listei.</span><span class="sxs-lookup"><span data-stu-id="024a5-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="024a5-150">Captură de ecran cu utilizarea Ordonare fluxuri de proces</span><span class="sxs-lookup"><span data-stu-id="024a5-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="024a5-151">Pașii de mai jos se aplică pentru aplicația Project Service 2.4.4.30 sau anterioară pe platforma 9.0</span><span class="sxs-lookup"><span data-stu-id="024a5-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="024a5-152">Adăugați un câmp nou personalizat la entitatea de proiect pentru a capta fazele personalizate în fluxul dvs. de business personalizat.</span><span class="sxs-lookup"><span data-stu-id="024a5-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="024a5-153">Veți avea nevoie să adăugați logica de business (plugin/flux de lucru) pentru a actualiza acest câmp atunci când se actualizează faza pe fluxul de business personalizat.</span><span class="sxs-lookup"><span data-stu-id="024a5-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Captură de ecran cu personalizarea entității Proiect](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="024a5-155">Modificați diagrama **Proiect după fază** pentru a vă utiliza noul câmp personalizat pentru faze.</span><span class="sxs-lookup"><span data-stu-id="024a5-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Captură de ecran cu utilizarea diagramei Proiect după fază](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="024a5-157">Modificați orice vizualizări pentru entitatea de proiect, astfel încât să includă noul dumneavoastră câmp personalizat pentru faze.</span><span class="sxs-lookup"><span data-stu-id="024a5-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Captură de ecran cu modificarea vizualizărilor pe entitatea proiectului](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]