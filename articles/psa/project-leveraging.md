---
title: Estimări de vânzări și proiecte
description: Acest subiect furnizează informații despre cum să profitați de planificare și de estimări în procesul de vânzări.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 76e21f80e51e6f3092880dc629ba90b400805486
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148388"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="76ce0-103">Estimări de vânzări și proiecte</span><span class="sxs-lookup"><span data-stu-id="76ce0-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76ce0-104">În timpul procesului de vânzare, aveți posibilitatea să creați estimări de vânzări prin legarea unui proiect la o ofertă de vânzare.</span><span class="sxs-lookup"><span data-stu-id="76ce0-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="76ce0-105">În acest fel, estimarea deterministă poate apărea în timpul procesului de vânzări, pentru a profita de planificarea proiectelor și de capacitățile de estimare.</span><span class="sxs-lookup"><span data-stu-id="76ce0-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="76ce0-106">În cazul în care vânzarea trece, planificarea care a fost utilizată în scopul estimării vânzărilor poate fi utilizată ca bază pentru rafinarea ulterioară a planului de proiect.</span><span class="sxs-lookup"><span data-stu-id="76ce0-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="76ce0-107">Legarea unui proiect la o linie de ofertă</span><span class="sxs-lookup"><span data-stu-id="76ce0-107">Linking a project to a quote line</span></span>

<span data-ttu-id="76ce0-108">Când creați o linie de ofertă bazată pe proiect, aveți posibilitatea să creați un proiect nou sau să asociați un proiect existent pe pagina **Linie ofertă**.</span><span class="sxs-lookup"><span data-stu-id="76ce0-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formularul Linie ofertă](media/project-8.png)
 
<span data-ttu-id="76ce0-110">Când creați un proiect nou din detaliile liniei de ofertă, puteți profita de șabloanele de proiect.</span><span class="sxs-lookup"><span data-stu-id="76ce0-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="76ce0-111">Șabloanele de proiect sunt proiecte model care reprezintă planuri de proiect standard și estimări financiare care sunt tipice într-o organizație.</span><span class="sxs-lookup"><span data-stu-id="76ce0-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="76ce0-112">Ele pot reprezenta, de asemenea, copii ale planurilor de proiect și estimările din proiectele anterioare.</span><span class="sxs-lookup"><span data-stu-id="76ce0-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalii linie de ofertă](media/project-9.png)
  
<span data-ttu-id="76ce0-114">Când creeați proiectul din ofertă, proiectul este asociat automat cu linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="76ce0-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="76ce0-115">Componentele estimărilor într-un proiect</span><span class="sxs-lookup"><span data-stu-id="76ce0-115">Components of estimates in a project</span></span>

<span data-ttu-id="76ce0-116">O planificare vă permite să împărțiți activitatea în activități, să mențineți o ierarhie de activități, să determinați ce resurse sunt necesare pentru a finaliza o activitate și să atribuiți o estimare a efortului necesar pentru finalizarea unei activități.</span><span class="sxs-lookup"><span data-stu-id="76ce0-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="76ce0-117">Puteți defini efortul de lucru și estimările de planificare utilizând câmpurile din fila **Planificare** a paginii **Proiect**.</span><span class="sxs-lookup"><span data-stu-id="76ce0-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="76ce0-118">Deoarece o listă de prețuri este asociată cu proiectul, estimările financiare sunt calculate utilizând costul și prețurile de vânzare care sunt definite în lista de prețuri.</span><span class="sxs-lookup"><span data-stu-id="76ce0-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="76ce0-119">Importarea estimărilor dintr-un proiect într-o ofertă</span><span class="sxs-lookup"><span data-stu-id="76ce0-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="76ce0-120">După ce definiți estimările proiectului, aveți posibilitatea să le importați în linia de ofertă.</span><span class="sxs-lookup"><span data-stu-id="76ce0-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="76ce0-121">În pagina **Detalii linie ofertă**, selectați **Importați din estimările** din panglică pentru a rezuma estimările de proiect după tipul de tranzacție, rol sau nivel de activitate.</span><span class="sxs-lookup"><span data-stu-id="76ce0-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
