---
title: Definirea calendarelor de resurse
description: Acest subiect furnizează informații despre cum să definiți calendarele orelor de lucru pentru resurse în Project Operations.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5ac834e16afc2f559bee6e10434f7015e8a8e51f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012196"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="d5498-103">Definirea calendarelor de resurse</span><span class="sxs-lookup"><span data-stu-id="d5498-103">Define resource calendars</span></span>

<span data-ttu-id="d5498-104">_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_</span><span class="sxs-lookup"><span data-stu-id="d5498-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5498-105">Fiecare resursă rezervabilă care lucrează la un proiect trebuie să aibă un calendar al orelor de lucru pentru a defini disponibilitatea acestora.</span><span class="sxs-lookup"><span data-stu-id="d5498-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="d5498-106">Orele de lucru pentru o resursă pot fi definite în două moduri:</span><span class="sxs-lookup"><span data-stu-id="d5498-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="d5498-107">Definiți regulile de calendar individuale pentru o resursă</span><span class="sxs-lookup"><span data-stu-id="d5498-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="d5498-108">Aplicați un șablon de calendar existent pentru resursă</span><span class="sxs-lookup"><span data-stu-id="d5498-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="d5498-109">Definiți orele de lucru ale unei resurse</span><span class="sxs-lookup"><span data-stu-id="d5498-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="d5498-110">Pe meniul **Resurse**, selectați **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="d5498-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="d5498-111">Din vizualizarea grilă, selectați aplicația corespunzătoare **Resursă rezervabilă**.</span><span class="sxs-lookup"><span data-stu-id="d5498-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="d5498-112">Pe pagina **Detalii despre resurse**, selectați fila **Ore de lucru**. În mod implicit, calendarul resurselor rezervabile implicit este programul de lucru al șablonului implicit de oră de lucru definit pentru organizație.</span><span class="sxs-lookup"><span data-stu-id="d5498-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="d5498-113">Pentru a actualiza programul de lucru, faceți clic dreapta pe data de începere a regulii calendaristice propuse care urmează să fie definită.</span><span class="sxs-lookup"><span data-stu-id="d5498-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="d5498-114">Utilizați meniul regulii calendarului pentru a defini o regulă calendaristică pentru o anumită zi, restul seriei sau întregul calendar.</span><span class="sxs-lookup"><span data-stu-id="d5498-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="d5498-115">După selectarea opțiunii, puteți defini:</span><span class="sxs-lookup"><span data-stu-id="d5498-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="d5498-116">Ziua săptămânii în care se vor aplica programele de lucru.</span><span class="sxs-lookup"><span data-stu-id="d5498-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="d5498-117">Orele de lucru din fiecare zi.</span><span class="sxs-lookup"><span data-stu-id="d5498-117">The working times within each day.</span></span>
    - <span data-ttu-id="d5498-118">Fusul orar local pentru regula de calendar.</span><span class="sxs-lookup"><span data-stu-id="d5498-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="d5498-119">Dacă este cazul, pentru regulă se poate specifica și timpul de lucru.</span><span class="sxs-lookup"><span data-stu-id="d5498-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="d5498-120">Aplicarea unui șablon de calendare unei resurse</span><span class="sxs-lookup"><span data-stu-id="d5498-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="d5498-121">Pe meniul **Resurse**, selectați **Resurse**.</span><span class="sxs-lookup"><span data-stu-id="d5498-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="d5498-122">Din vizualizarea grilă, selectați până la 25 de **Resurse rezervabile** pentru a actualiza.</span><span class="sxs-lookup"><span data-stu-id="d5498-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="d5498-123">Selectați **Setați Calendar** și o fereastră de dialog vă va solicita cu o listă de șabloane de ore de lucru disponibile.</span><span class="sxs-lookup"><span data-stu-id="d5498-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="d5498-124">Selectați șablonul pe care doriți să îl utilizați și apoi selectați **Aplicare**.</span><span class="sxs-lookup"><span data-stu-id="d5498-124">Select the template you want to use, and then select **Apply**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]