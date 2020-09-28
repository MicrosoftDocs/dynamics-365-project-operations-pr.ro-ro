---
title: Urmărirea stării unui proiect
description: Cum să urmăriți starea unui proiect în Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754817"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="79285-103">Urmărirea stării unui proiect (Project Service)</span><span class="sxs-lookup"><span data-stu-id="79285-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="79285-104">Utilizați [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] pentru a urmări progresul proiectului unui client.</span><span class="sxs-lookup"><span data-stu-id="79285-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="79285-105">Pe măsură ce angajamentul progreseaz, etapele proiectului se actualizează pentru a reflecta etapa angajamentului:</span><span class="sxs-lookup"><span data-stu-id="79285-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="79285-106">**Nou**</span><span class="sxs-lookup"><span data-stu-id="79285-106">**New**</span></span>    | <span data-ttu-id="79285-107">Când creați un proiect, faza este setată la **Nou**.</span><span class="sxs-lookup"><span data-stu-id="79285-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="79285-108">Dacă ați creat proiectul dintr-un șablon, în această fază, proiectul ar putea avea o planificare, estimări și date de echipă.</span><span class="sxs-lookup"><span data-stu-id="79285-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="79285-109">În caz contrar, aceasta va fi schița proiectului și va trebui să introduceți manual restul de componente ale proiectului.</span><span class="sxs-lookup"><span data-stu-id="79285-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="79285-110">**Ofertă**</span><span class="sxs-lookup"><span data-stu-id="79285-110">**Quote**</span></span>   |      <span data-ttu-id="79285-111">Când asociați un proiect la o ofertă sau creați unul de la o ofertă, faza proiectului este setată la **Ofertă** și datele de început și de sfârșit estimate sunt actualizate, de asemenea.</span><span class="sxs-lookup"><span data-stu-id="79285-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="79285-112">Atunci proiectul este în faza de ofertă, detaliile ofertei se afișează pe fila **Vânzări** din pagina **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="79285-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="79285-113">**Plan**</span><span class="sxs-lookup"><span data-stu-id="79285-113">**Plan**</span></span>   |                                     <span data-ttu-id="79285-114">Atunci când câștigați o ofertă asociată cu un proiect și atunci când angajamentul progresează la faza de contractul, faza proiectului se actualizează la **Plan**.</span><span class="sxs-lookup"><span data-stu-id="79285-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="79285-115">Detaliile contractului se afișează în fila **Vânzări** din pagina **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="79285-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="79285-116">**Terminată**</span><span class="sxs-lookup"><span data-stu-id="79285-116">**Complete**</span></span> |                    <span data-ttu-id="79285-117">Când proiectul este terminat, puteți comuta faza la **Terminată**.</span><span class="sxs-lookup"><span data-stu-id="79285-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="79285-118">Când faza de proiect este setată la Terminată, se înțelege că munca este 100% completă, dar proiectul este menținut deschis pentru orice timp de așteptare sau intrări de cheltuieli ce se vor înregistra.</span><span class="sxs-lookup"><span data-stu-id="79285-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="79285-119">**Închidere**</span><span class="sxs-lookup"><span data-stu-id="79285-119">**Close**</span></span>   |           <span data-ttu-id="79285-120">Atunci când au fost înregistrate toate tranzacțiile pentru proiect și nu vă așteptați să mai fie și altele înregistrate, puteți seta manual etapa la **Închidere**.</span><span class="sxs-lookup"><span data-stu-id="79285-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="79285-121">Când proiectul este setat la **Închidere**, nu mai puteți înregistra tranzacții în proiect și proiectul va fi doar în citire.</span><span class="sxs-lookup"><span data-stu-id="79285-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="79285-122">Pentru a urmări starea unui proiect</span><span class="sxs-lookup"><span data-stu-id="79285-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="79285-123">Accesați **Project Service > Proiecte**.</span><span class="sxs-lookup"><span data-stu-id="79285-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="79285-124">Faceți clic pe proiectul la care doriți să lucrați.</span><span class="sxs-lookup"><span data-stu-id="79285-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="79285-125">În bara din partea de sus a ecranului, selectați săgeata în jos de lângă numele proiectului, apoi faceți clic pe **Monitorizare proiect**.</span><span class="sxs-lookup"><span data-stu-id="79285-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="79285-126">Selectați **Urmărire efort** sau **Urmărire costuri** în lista verticală de deasupra listei de activități.</span><span class="sxs-lookup"><span data-stu-id="79285-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="79285-127">Faceți dublu clic pe orice activitate pentru a o edita.</span><span class="sxs-lookup"><span data-stu-id="79285-127">Double-click any task to edit it.</span></span> <span data-ttu-id="79285-128">De asemenea, puteți să mutați sau să redimensionați barele în diagrama Gantt pentru a modifica timpul și progresul unei activități.</span><span class="sxs-lookup"><span data-stu-id="79285-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="79285-129">Consultați și</span><span class="sxs-lookup"><span data-stu-id="79285-129">See Also</span></span>  
 [<span data-ttu-id="79285-130">Ghidul Managerului de proiect</span><span class="sxs-lookup"><span data-stu-id="79285-130">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)