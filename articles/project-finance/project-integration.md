---
title: Integrare Microsoft Project Client
description: Planificarea și menținerea unui plan de proiect pot fi complexe, astfel încât managerii de proiect trebuie să utilizeze instrumente care îi ajută să gestioneze această sarcină. Integrarea cu Microsoft Project Client oferă suport pentru deschiderea și gestionarea unei structuri detaliate a proiectului.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754806"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="be45f-104">Integrare Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="be45f-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be45f-105">Planificarea și menținerea unui plan de proiect pot fi complexe, astfel încât managerii de proiect trebuie să utilizeze instrumente care îi ajută să gestioneze această sarcină.</span><span class="sxs-lookup"><span data-stu-id="be45f-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="be45f-106">Integrarea cu Microsoft Project Client oferă suport pentru deschiderea și gestionarea unei structuri detaliate a proiectului.</span><span class="sxs-lookup"><span data-stu-id="be45f-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="be45f-107">Managerul de proiect poate publica orice modificări înapoi la structura detaliată a proiectului Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="be45f-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="be45f-108">Dacă utilizați actualizarea din iulie (versiunea 10.0.4), trebuie să instalați KB 4054797 și 4055884.</span><span class="sxs-lookup"><span data-stu-id="be45f-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="be45f-109">Configurați programul de completare Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="be45f-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="be45f-110">Pentru a permite integrarea cu Microsoft Project Client, a Microsoft Dynamics 365 programul de completare trebuie să fie instalat în aplicația client Microsoft Project a utilizatorului.</span><span class="sxs-lookup"><span data-stu-id="be45f-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="be45f-111">Acest lucru se face prin deschiderea **Spațiul de lucru pentru gestionarea proiectelor**.</span><span class="sxs-lookup"><span data-stu-id="be45f-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="be45f-112">•   Faceți clic pe **Configurați programul de completare pentru clientul de proiect** din la secțiunea **Linkuri** > **Configurare** a spațiului de lucru.</span><span class="sxs-lookup"><span data-stu-id="be45f-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="be45f-113">•   Faceți clic pe **Deschidere**, apoi apăsați **Rulare** când vi se solicită.</span><span class="sxs-lookup"><span data-stu-id="be45f-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="be45f-114">Deschideți și editați o structură detaliată a proiectului existentă în Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="be45f-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="be45f-115">Dacă un proiect în Dynamics 365 Finance are deja creată o structură detaliată a proiectului, structura detaliată a proiectului poate fi deschisă în aplicația Microsoft Project Client dacă structura detaliată a proiectului este în starea de schiță.</span><span class="sxs-lookup"><span data-stu-id="be45f-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="be45f-116">Pentru a deschide din pagina **Proiect**, faceți clic pe linkul **Deschideți în Microsoft Project** din fila **Plan**. Această pagină poate fi deschisă și din aplicația Microsoft Project Client făcând clic pe **Deschidere** în fila **Microsoft Dynamics 365**. Selectați **Entitate legală** și **Proiect** din listă.</span><span class="sxs-lookup"><span data-stu-id="be45f-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="be45f-117">Dacă folosiți Internet Explorer ca browser, va trebui să faceți clic pe **Salvare** pentru a deschide manual din locația în care este descărcat fișierul.</span><span class="sxs-lookup"><span data-stu-id="be45f-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="be45f-118">Sau faceți clic pe **Salvare și deschidere** pentru a deschide fișierul în Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="be45f-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="be45f-119">Nu redenumiți numele fișierului atunci când salvați.</span><span class="sxs-lookup"><span data-stu-id="be45f-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="be45f-120">Înainte de a efectua modificări ale fișierului utilizând Microsoft Project Client, trebuie să îl verificați. Faceți clic pe **Verificare** în fila **Microsoft Dynamics 365**. Acest lucru va împiedica ceilalți utilizatori să editeze structura detaliată a proiectului din Finance în același timp.</span><span class="sxs-lookup"><span data-stu-id="be45f-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="be45f-121">Pentru a publica structura detaliată a proiectului după finalizarea oricăror modificări, faceți clic pe **Confirmare** pe fila **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="be45f-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="be45f-122">Dacă o echipă de proiect a fost deja adăugată la proiect în Finance, lista resurselor va fi completată cu membrii echipei.</span><span class="sxs-lookup"><span data-stu-id="be45f-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="be45f-123">Dacă o echipă de proiect nu a fost încă adăugată la proiect, puteți selecta resurse și puteți construi echipa în cadrul Microsoft Project Client făcând clic pe butonul **Resurse** de pe fila **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="be45f-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="be45f-124">Următoarele date vor fi sincronizate înapoi la Finance ca parte a procesului de confirmare:</span><span class="sxs-lookup"><span data-stu-id="be45f-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="be45f-125">•   Numele activității</span><span class="sxs-lookup"><span data-stu-id="be45f-125">•   Task name</span></span>

<span data-ttu-id="be45f-126">•   Data de început</span><span class="sxs-lookup"><span data-stu-id="be45f-126">•   Start date</span></span>

<span data-ttu-id="be45f-127">•   Data de terminare</span><span class="sxs-lookup"><span data-stu-id="be45f-127">•   Finish date</span></span>

<span data-ttu-id="be45f-128">•   Predecesori</span><span class="sxs-lookup"><span data-stu-id="be45f-128">•   Predecessors</span></span>

<span data-ttu-id="be45f-129">•   Numele resurselor</span><span class="sxs-lookup"><span data-stu-id="be45f-129">•   Resource names</span></span>

<span data-ttu-id="be45f-130">•   Categorie</span><span class="sxs-lookup"><span data-stu-id="be45f-130">•   Category</span></span>

<span data-ttu-id="be45f-131">•   Categorie resursă</span><span class="sxs-lookup"><span data-stu-id="be45f-131">•   Resource category</span></span>

<span data-ttu-id="be45f-132">•   Ore de lucru</span><span class="sxs-lookup"><span data-stu-id="be45f-132">•   Work hours</span></span>

<span data-ttu-id="be45f-133">•   Note</span><span class="sxs-lookup"><span data-stu-id="be45f-133">•   Notes</span></span>

<span data-ttu-id="be45f-134">•   Prioritate</span><span class="sxs-lookup"><span data-stu-id="be45f-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="be45f-135">Dacă adăugați alte coloane în fișierul dvs. Microsoft Project Client, acestea nu vor fi salvate în fișier și nu vor fi afișate când fișierul este deschis din nou.</span><span class="sxs-lookup"><span data-stu-id="be45f-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="be45f-136">Creați structura detaliată a proiectului pentru un proiect existent utilizând Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="be45f-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="be45f-137">Pentru a crea o nouă structură detaliată a proiectului utilizând Microsoft Project Client, urmați acești pași:</span><span class="sxs-lookup"><span data-stu-id="be45f-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="be45f-138">Deschideți Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="be45f-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="be45f-139">În fila **Microsoft Dynamics 365**, faceți clic pe **Deschidere**.</span><span class="sxs-lookup"><span data-stu-id="be45f-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="be45f-140">Selectați **Entitatea legală** pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="be45f-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="be45f-141">Selectați **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="be45f-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="be45f-142">Faceți clic pe **Verificare** pe fila **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="be45f-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="be45f-143">Când sunteți gata să publicați în Finance, faceți clic pe **Verificare** pe fila **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="be45f-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="be45f-144">Înlocuiți structura detaliată a proiectului existentă pentru un proiect existent utilizând Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="be45f-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="be45f-145">Pentru a crea o nouă structură detaliată a proiectului utilizând Microsoft Project Client și a înlocui o structură detaliată a proiectului existentă pentru un proiect existent, urmați acești pași:</span><span class="sxs-lookup"><span data-stu-id="be45f-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="be45f-146">Deschideți Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="be45f-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="be45f-147">Creați planificarea în Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="be45f-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="be45f-148">Din fila **Microsoft Dynamics 365**, faceți clic pe **Salvare modificări** > **Înlocuire proiect existent**.</span><span class="sxs-lookup"><span data-stu-id="be45f-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="be45f-149">Selectați **Entitatea legală** pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="be45f-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="be45f-150">Selectați **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="be45f-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="be45f-151">Faceți clic pe **OK**.</span><span class="sxs-lookup"><span data-stu-id="be45f-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="be45f-152">Creați un proiect nou din Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="be45f-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="be45f-153">Deschideți Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="be45f-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="be45f-154">Creați planificarea în Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="be45f-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="be45f-155">Din fila **Microsoft Dynamics 365**, faceți clic pe **Salvare modificări** > **Salvare ca proiect nou**.</span><span class="sxs-lookup"><span data-stu-id="be45f-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="be45f-156">Selectați **Entitatea legală** pentru proiect.</span><span class="sxs-lookup"><span data-stu-id="be45f-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="be45f-157">Introduceți **ID-ul proiectului**, dacă este necesar.</span><span class="sxs-lookup"><span data-stu-id="be45f-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="be45f-158">Introduceți **Numele proiectului**.</span><span class="sxs-lookup"><span data-stu-id="be45f-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="be45f-159">Selectați **Tipul proiectului**, **Grup de proiect** și **ID-ul contractului de proiect**.</span><span class="sxs-lookup"><span data-stu-id="be45f-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="be45f-160">Alternativ, puteți crea un nou contract de proiect făcând clic pe **Nou**.</span><span class="sxs-lookup"><span data-stu-id="be45f-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="be45f-161">Selectați **Calendar** pentru a fi folosit pentru resurse.</span><span class="sxs-lookup"><span data-stu-id="be45f-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="be45f-162">Faceți clic pe **OK**.</span><span class="sxs-lookup"><span data-stu-id="be45f-162">Click **OK**.</span></span>
