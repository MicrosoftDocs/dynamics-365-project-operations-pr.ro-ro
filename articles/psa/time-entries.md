---
title: Creare intrări de timp
description: Acest subiect oferă informații despre modul de creare a intrărilor de timp.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
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
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082887"
---
# <a name="create-time-entries"></a><span data-ttu-id="db9a1-103">Creare intrări de timp</span><span class="sxs-lookup"><span data-stu-id="db9a1-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="db9a1-104">În versiunile anterioare de Dynamics 365 Project Service Automation, intrările de timp erau introduse săptămânal.</span><span class="sxs-lookup"><span data-stu-id="db9a1-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="db9a1-105">În versiunea 3 a Project Service Automation, intrările de timp sunt introduse zilnic.</span><span class="sxs-lookup"><span data-stu-id="db9a1-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="db9a1-106">Cu toate acestea, după ce au fost create câteva intrări de timp, aveți posibilitatea să le creați sau să le copiați în vrac.</span><span class="sxs-lookup"><span data-stu-id="db9a1-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="db9a1-107">Creați o intrare de timp</span><span class="sxs-lookup"><span data-stu-id="db9a1-107">Create a time entry</span></span>

<span data-ttu-id="db9a1-108">Urmați acești pași pentru a crea o intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="db9a1-109">În pagina **Intrări timp** , selectați **Nou**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="db9a1-110">În caseta de dialog **Creare rapidă: intrare timp** , introduceți durata intrării de timp în minute, ore sau zile.</span><span class="sxs-lookup"><span data-stu-id="db9a1-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="db9a1-111">Durata trebuie introdusă în formatul următor: *x* minute, *x* ore sau *x* zile.</span><span class="sxs-lookup"><span data-stu-id="db9a1-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="db9a1-112">Orele și zilele pot fi introduse și ca valori zecimale, de exemplu, *x.x* ore sau *x.x* zile.</span><span class="sxs-lookup"><span data-stu-id="db9a1-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="db9a1-113">Selectați tipul de intrare de timp și proiectul în care introduceți intrarea de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="db9a1-114">În câmpul **Activitate proiect** , găsiți activitatea pentru această intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db9a1-115">Dacă creați o intrare de timp pentru o activitate care nu este atribuită unui utilizator, în câmpul **activitate proiect** , selectați butonul **Căutare** , selectați **Schimbare vizualizare** , apoi selectați **Toate activitățile de proiect active** pentru a lista toate activitățile.</span><span class="sxs-lookup"><span data-stu-id="db9a1-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="db9a1-116">Introduceți o descriere, dacă este necesară o descriere, apoi selectați **Salvare și închidere**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="db9a1-117">După ce intrarea de timp este creată și salvată, o puteți edita în grila de intrare de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="db9a1-118">Grila de intrare de timp acceptă două formate:</span><span class="sxs-lookup"><span data-stu-id="db9a1-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="db9a1-119">Aveți posibilitatea să introduceți intrările de timp în format **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="db9a1-120">Acest format este apoi convertit în ore și fracții.</span><span class="sxs-lookup"><span data-stu-id="db9a1-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="db9a1-121">Aveți posibilitatea să introduceți direct ore și fracții.</span><span class="sxs-lookup"><span data-stu-id="db9a1-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="db9a1-122">Rețineți că fracțiunile unei ore nu sunt minute.</span><span class="sxs-lookup"><span data-stu-id="db9a1-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="db9a1-123">Prin urmare, 1,5 ore reprezintă 1 oră și 30 de minute.</span><span class="sxs-lookup"><span data-stu-id="db9a1-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="db9a1-124">Aceeași regulă se aplică fracțiunilor unei zile.</span><span class="sxs-lookup"><span data-stu-id="db9a1-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="db9a1-125">O zi este de 24 de ore, iar 0,5 zile reprezintă 12 ore.</span><span class="sxs-lookup"><span data-stu-id="db9a1-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="db9a1-126">Creare în bloc de intrări de timp</span><span class="sxs-lookup"><span data-stu-id="db9a1-126">Bulk create time entries</span></span>

<span data-ttu-id="db9a1-127">După ce au fost create câteva înregistrări de timp, le puteți copia pentru a crea în bloc înregistrări de timp suplimentare.</span><span class="sxs-lookup"><span data-stu-id="db9a1-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="db9a1-128">În pagina **Intrări timp** , selectați **Copiere săptămână**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="db9a1-129">În grupul de câmpuri **De la perioada** , în câmpurile **Data de început** și **Data de sfârșit** , definiți intervalul de date din care să copiați înregistrările de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="db9a1-130">În grupul de câmpuri **Până la perioada** , în câmpul **Data de început** , specificați data pentru care să creați înregistrări de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="db9a1-131">Selectați **Copiere** pentru a crea o copie a intrărilor de timp care corespund zilei săptămânii indicate în grupul de câmpuri **Până la perioada**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="db9a1-132">De exemplu, înregistrarea de timp pentru ziua de luni de săptămâna trecută este copiată pentru lunea săptămânii indicate în grupul de câmpuri **Până la perioada**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="db9a1-133">Importați date pentru intrările de timp</span><span class="sxs-lookup"><span data-stu-id="db9a1-133">Import data for time entries</span></span>

<span data-ttu-id="db9a1-134">Aveți posibilitatea să importați date din rezervările și activitățile de proiect.</span><span class="sxs-lookup"><span data-stu-id="db9a1-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="db9a1-135">Când importați date, aveți posibilitatea să specificați intervalul de date al rezervărilor de importat și apoi să selectați în mod explicit rezervările care ar trebui create ca intrări de timp **Schiță**.</span><span class="sxs-lookup"><span data-stu-id="db9a1-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="db9a1-136">Grupați după, sortați, căutați și filtrați capacități</span><span class="sxs-lookup"><span data-stu-id="db9a1-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="db9a1-137">Aveți posibilitatea să grupați și să filtrați intrările de timp după dimensiunile specificate în coloane.</span><span class="sxs-lookup"><span data-stu-id="db9a1-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="db9a1-138">În câmpul **Grupare după** , selectați dimensiunea de utilizat pentru filtrarea intrărilor de timp.</span><span class="sxs-lookup"><span data-stu-id="db9a1-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="db9a1-139">De asemenea, aveți posibilitatea să sortați înregistrările de intrări de timp în ordine crescătoare sau descrescătoare utilizând săgeata de sortare de pe titlurile coloanelor.</span><span class="sxs-lookup"><span data-stu-id="db9a1-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="db9a1-140">În plus, aveți posibilitatea să afișați sau să ascundeți intrările selectând butonul **Filtru** de pe titlurile coloanelor, apoi, în caseta **Căutare** , introduceți textul care ar trebui utilizat pentru a căuta intrările de timp după numele proiectului, activitatea proiectului, intrarea de timp sau resursă.</span><span class="sxs-lookup"><span data-stu-id="db9a1-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
