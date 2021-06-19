---
title: Depanare de funcționare în grila de activități
description: Acest subiect oferă informații legate de depanare necesare atunci când lucrați în grila de activități.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213415"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="9c970-103">Depanare de funcționare în grila de activități</span><span class="sxs-lookup"><span data-stu-id="9c970-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="9c970-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="9c970-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c970-105">Acest subiect descrie cum să remediați problemele care ar putea apărea în timp ce lucrați cu gestionarea costurilor.</span><span class="sxs-lookup"><span data-stu-id="9c970-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="9c970-106">Activați module cookie</span><span class="sxs-lookup"><span data-stu-id="9c970-106">Enable cookies</span></span>

<span data-ttu-id="9c970-107">Project Operations are nevoie ca modulele cookie de la terți să fie activate pentru a reda structura detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="9c970-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="9c970-108">Când modulele cookie de terță parte nu sunt activate, în loc să vedeți sarcini, veți vedea o pagină goală când selectați fila **Sarcini** de pe pagina **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="9c970-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Fila goală când modulele cookie de terță parte nu sunt activate](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="9c970-110">Soluție</span><span class="sxs-lookup"><span data-stu-id="9c970-110">Workaround</span></span>
<span data-ttu-id="9c970-111">Pentru browser-ele Microsoft Edge sau Google Chrome, următoarele proceduri descriu cum să actualizați setările browser-ului pentru a activa modulele cookie de terță parte.</span><span class="sxs-lookup"><span data-stu-id="9c970-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="9c970-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9c970-112">Microsoft Edge</span></span>

1. <span data-ttu-id="9c970-113">Deschideți browserul Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9c970-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="9c970-114">În colțul din dreapta sus, selectați **puncte de suspensie** (...), apoi selectați **Setări**.</span><span class="sxs-lookup"><span data-stu-id="9c970-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="9c970-115">La **Module cookie și permisiuni de site**, Selectați **Module cookie-uri și date despre site-uri**.</span><span class="sxs-lookup"><span data-stu-id="9c970-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="9c970-116">Dezactivați opțiunea **Blocați modulele cookie de terță parte**.</span><span class="sxs-lookup"><span data-stu-id="9c970-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="9c970-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="9c970-117">Google Chrome</span></span>

1. <span data-ttu-id="9c970-118">Deschideți browserul Chrome.</span><span class="sxs-lookup"><span data-stu-id="9c970-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="9c970-119">În colțul din dreapta sus, selectați cele trei puncte verticale, apoi selectați **Setări**.</span><span class="sxs-lookup"><span data-stu-id="9c970-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="9c970-120">La **Confidențialitate și securitate**, Selectați **Module cookie-uri și alte date despre site-uri**.</span><span class="sxs-lookup"><span data-stu-id="9c970-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="9c970-121">Selectați **Permiteți toate modulele cookie**.</span><span class="sxs-lookup"><span data-stu-id="9c970-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c970-122">Dacă blocați modulele cookie de terță parte, toate modulele cookie și datele site-urilor de pe alte site-uri vor fi blocate, chiar dacă site-ul este autorizat pe lista dvs. de excepții.</span><span class="sxs-lookup"><span data-stu-id="9c970-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="9c970-123">Punct final PEX</span><span class="sxs-lookup"><span data-stu-id="9c970-123">PEX Endpoint</span></span>

<span data-ttu-id="9c970-124">Project Operations necesită ca un parametru de proiect să facă referire la punctul final PEX.</span><span class="sxs-lookup"><span data-stu-id="9c970-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="9c970-125">Acest punct final este necesar pentru a comunica cu serviciul utilizat pentru a reda structura detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="9c970-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="9c970-126">Dacă parametrul nu este activat, veți primi eroarea „Parametrul proiectului nu este valid”.</span><span class="sxs-lookup"><span data-stu-id="9c970-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="9c970-127">Soluție</span><span class="sxs-lookup"><span data-stu-id="9c970-127">Workaround</span></span>
 ![Câmpul punct final PEX în parametrul proiectului](media/projectparameter.png)

1. <span data-ttu-id="9c970-129">Adăugați câmpul **Punct final PEX** pe pagina **Parametrii proiectului**.</span><span class="sxs-lookup"><span data-stu-id="9c970-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="9c970-130">Actualizați câmpul cu următoarea valoare: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="9c970-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="9c970-131">Eliminați câmpul de pe pagina **Parametrii proiectului**.</span><span class="sxs-lookup"><span data-stu-id="9c970-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="9c970-132">Privilegii de proiect pentru Web</span><span class="sxs-lookup"><span data-stu-id="9c970-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="9c970-133">Project Operations se bazează pe un serviciu de planificare externă.</span><span class="sxs-lookup"><span data-stu-id="9c970-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="9c970-134">Serviciul necesită ca un utilizator să aibă mai multe roluri atribuite pentru a citi și scrie entităților asociate la structura detaliată a proiectului.</span><span class="sxs-lookup"><span data-stu-id="9c970-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="9c970-135">Aceste entități includ sarcini de proiect, alocări de resurse și dependențe de sarcini.</span><span class="sxs-lookup"><span data-stu-id="9c970-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="9c970-136">Dacă un utilizator nu poate reda structura detaliată a proiectului de pe fila **Sarcini** fila, probabil este pentru că Proiect pentru Project Operations nu a fost activat.</span><span class="sxs-lookup"><span data-stu-id="9c970-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="9c970-137">Un utilizator poate primi fie o eroare rol de securitate, fie o eroare legată de refuzul de acces.</span><span class="sxs-lookup"><span data-stu-id="9c970-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="9c970-138">Soluție</span><span class="sxs-lookup"><span data-stu-id="9c970-138">Workaround</span></span>

1. <span data-ttu-id="9c970-139">Accesați vizualizarea **Setări > Securitate > Utilizatori > Utilizatorii aplicației**.</span><span class="sxs-lookup"><span data-stu-id="9c970-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Cititor aplicație](media/applicationuser.jpg)
   
2. <span data-ttu-id="9c970-141">Faceți dublu clic pe înregistrarea utilizatorului aplicației pentru a verifica următoarele:</span><span class="sxs-lookup"><span data-stu-id="9c970-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="9c970-142">Utilizatorul are acces la proiect.</span><span class="sxs-lookup"><span data-stu-id="9c970-142">The user has access to the project.</span></span> <span data-ttu-id="9c970-143">De obicei, această verificare se face prin asigurarea faptului că utilizatorul are rol de securitate **Manager de proiect**.</span><span class="sxs-lookup"><span data-stu-id="9c970-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="9c970-144">Utilizatorul aplicației Microsoft Project există și este configurat corect.</span><span class="sxs-lookup"><span data-stu-id="9c970-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="9c970-145">Dacă acest utilizator nu există deja, puteți crea o nouă înregistrare de utilizator.</span><span class="sxs-lookup"><span data-stu-id="9c970-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="9c970-146">Selectați **Utilizatori noi**.</span><span class="sxs-lookup"><span data-stu-id="9c970-146">Select **New Users**.</span></span> <span data-ttu-id="9c970-147">Schimbați formularul de înregistrare în **Utilizator de aplicație**, apoi adăugați **ID-ul aplicației**.</span><span class="sxs-lookup"><span data-stu-id="9c970-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalii utilizator aplicație](media/applicationuserdetails.jpg)

4. <span data-ttu-id="9c970-149">Verificați dacă utilizatorului i s-a atribuit licența corectă și că serviciul este activat în detaliile abonamentelor de servicii ale licenței.</span><span class="sxs-lookup"><span data-stu-id="9c970-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="9c970-150">Verificați dacă utilizatorul poate deschide project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="9c970-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="9c970-151">Verificați prin parametrii proiectului dacă sistemul indică punctul final corect al proiectului.</span><span class="sxs-lookup"><span data-stu-id="9c970-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="9c970-152">Verificați dacă este creat utilizatorul aplicației de proiect.</span><span class="sxs-lookup"><span data-stu-id="9c970-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="9c970-153">Aplicați următoarele roluri de securitate pentru utilizator:</span><span class="sxs-lookup"><span data-stu-id="9c970-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="9c970-154">Utilizator Dataverse</span><span class="sxs-lookup"><span data-stu-id="9c970-154">Dataverse User</span></span>
  - <span data-ttu-id="9c970-155">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="9c970-155">Project Operations System</span></span>
  - <span data-ttu-id="9c970-156">Sistemul proiectului</span><span class="sxs-lookup"><span data-stu-id="9c970-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="9c970-157">Eroare la actualizarea structurii detaliate a proiectului</span><span class="sxs-lookup"><span data-stu-id="9c970-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="9c970-158">Când se efectuează una sau mai multe actualizări la structura detaliată a proiectului, în cele din urmă modificările eșuează și nu sunt salvate.</span><span class="sxs-lookup"><span data-stu-id="9c970-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="9c970-159">Apare o eroare în grila de programare observând că „Modificarea recentă pe care ați făcut-o nu a putut fi salvată”.</span><span class="sxs-lookup"><span data-stu-id="9c970-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="9c970-160">Soluție</span><span class="sxs-lookup"><span data-stu-id="9c970-160">Workaround</span></span>

1. <span data-ttu-id="9c970-161">Verificați dacă utilizatorului i s-a atribuit licența corectă și că serviciul este activat în detaliile abonamentelor de servicii ale licenței.</span><span class="sxs-lookup"><span data-stu-id="9c970-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="9c970-162">Verificați dacă utilizatorul poate deschide project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="9c970-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="9c970-163">Verificați dacă sistemul indică punctul final corect al proiectului.</span><span class="sxs-lookup"><span data-stu-id="9c970-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="9c970-164">Verificați dacă utilizatorul aplicației de proiect a fost creat.</span><span class="sxs-lookup"><span data-stu-id="9c970-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="9c970-165">Aplicați următoarele roluri de securitate pentru utilizator:</span><span class="sxs-lookup"><span data-stu-id="9c970-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="9c970-166">Utilizator Dataverse sau utilizator de bază</span><span class="sxs-lookup"><span data-stu-id="9c970-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="9c970-167">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="9c970-167">Project Operations System</span></span>
  - <span data-ttu-id="9c970-168">Sistemul proiectului</span><span class="sxs-lookup"><span data-stu-id="9c970-168">Project System</span></span>
  - <span data-ttu-id="9c970-169">Sistemul de scriere dublă al Project Operations (Acest rol este necesar dacă implementați scenariul bazat pe resurse/ne-stocat al Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="9c970-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
