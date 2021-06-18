---
title: Menținerea membrilor echipei
description: Acest subiect oferă informații despre rezervarea resurselor numite pentru echipe de proiect și atribuirea lor către activități.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 00312c5a701768e0042e7e0236477c192690ded3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998651"
---
# <a name="maintain-team-members"></a><span data-ttu-id="c4cfd-103">Menținerea membrilor echipei</span><span class="sxs-lookup"><span data-stu-id="c4cfd-103">Maintain team members</span></span>

<span data-ttu-id="c4cfd-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="c4cfd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c4cfd-105">Puteți adăuga o resursă numită echipei dvs. de proiect, rezervând-o direct echipei.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="c4cfd-106">În Dynamics 365 Project Operations, accesați **Proiecte** și selectați și deschideți proiectul pentru care faceți rezervarea.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="c4cfd-107">Pe pagina **Proiect**, în fila **Echipă**, selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="c4cfd-108">În caseta de dialog **Creare rapidă membru echipă proiect**, selectați resursa care se poate rezerva.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="c4cfd-109">Câmpul **Rol** se va popula cu rolul implicit al resursei, dacă aceasta are unul atribuit.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="c4cfd-110">Aveţi posibilitatea de a schimba rolul.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-110">You can change the role.</span></span> 
4. <span data-ttu-id="c4cfd-111">Selectați datele de la și până la care resursa va fi necesară și selectați metoda de alocare a capacității resursei.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="c4cfd-112">În câmpul **Aprobator de proiect**, selectați **Da** dacă doriți ca membrul echipei să fie aprobator de proiect.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="c4cfd-113">Membrul echipei poate aproba intrările de timp și cheltuieli remise pentru acest proiect.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="c4cfd-114">Selectați **Salvare**.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-114">Select **Save**.</span></span>

<span data-ttu-id="c4cfd-115">Acum aveți posibilitatea să atribuiți resursa rezervată activităților din proiect.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="c4cfd-116">Pe pagina **Proiect**, pe fila **Planificare** atribuiți activități la noua resursă.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="c4cfd-117">Selectorul de resurse care este lansat din câmpul **Resurse** din grila de activități va afișa membrii echipei pe care îi puteți selecta.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="c4cfd-118">În Project Operations, rezervările de resurse și atribuțiile de sarcini nu sunt strâns legate.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="c4cfd-119">Atunci când utilizați selectorul de resurse din planificare, aveți posibilitatea să atribuiți activități membrilor echipei pentru mai multe ore decât acoperă rezervările lor pe proiect.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="c4cfd-120">Diferențele dintre rezervările și atribuțiile membrilor echipei sunt afișate pe filele **Echipă** și **Reconcilierea resurselor**.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="c4cfd-121">De asemenea, puteți reconcilia diferențele dintre rezervări și sarcini pentru resurse la un nivel mai detaliat.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="c4cfd-122">Utilizați selectorul de resurse în fila **Planificare** pentru a căuta și selecta resurse rezervabile care nu fac deja parte din echipa de proiect.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="c4cfd-123">Aceste resurse sunt afișate în selectorul de resurse ca **Alte resurse**.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="c4cfd-124">Când faceți o alegere, resursa este adăugată la echipa de proiect și atribuită sarcinii, dar nu sunt generate rezervări.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="c4cfd-125">Aveți posibilitatea să utilizați capacitatea Extindere rezervare a filei **Reconciliere** sau **Tablou de planificare** pentru a rezerva capacitatea resursei la proiect.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="c4cfd-126">După ce un membru al echipei este rezervat în cadrul proiectului dvs., aveți posibilitatea să utilizați **Mențineți rezervările** sau direct **Tablou de planificare** pentru a gestiona rezervările acestuia.</span><span class="sxs-lookup"><span data-stu-id="c4cfd-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]