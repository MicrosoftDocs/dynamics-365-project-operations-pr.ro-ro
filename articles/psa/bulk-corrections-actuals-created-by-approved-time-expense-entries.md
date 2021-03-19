---
title: Corecții în bloc ale datelor reale create prin intrări de timp și cheltuieli aprobate
description: Acest subiect explică modul în care un administrator poate efectua corecții unice sau în bloc la intrările de timp sau cheltuieli aprobate anterior dacă facturarea nu este finalizată.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 17d6648840e27a4e573985af2cdd74c4adf878e1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290914"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="c836d-103">Corecții în bloc ale datelor reale create prin intrări de timp și cheltuieli aprobate</span><span class="sxs-lookup"><span data-stu-id="c836d-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c836d-104">Ocazional, o intrare de timp sau de cheltuială poate fi introdusă incorect.</span><span class="sxs-lookup"><span data-stu-id="c836d-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="c836d-105">De exemplu, un consultant ar putea selecta data greșită atunci când creează o intrare de timp sau ar putea transpune numerele la intrarea unei cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="c836d-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="c836d-106">Dacă un consultant nu poate efectua actualizările intrărilor trimise, un administrator poate corecta direct intrarea pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="c836d-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="c836d-107">Pentru a finaliza procedurile din acest subiect, veți avea nevoie de permisiuni de administrator.</span><span class="sxs-lookup"><span data-stu-id="c836d-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="c836d-108">Intrări de timp aprobate corect</span><span class="sxs-lookup"><span data-stu-id="c836d-108">Correct approved time entries</span></span>     

<span data-ttu-id="c836d-109">Urmați pașii următori pentru a corecta intrările de timp unice sau multiple pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="c836d-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="c836d-110">În zona **Vânzări**, selectați **Tranzacții**, apoi selectați **Timp aprobat**.</span><span class="sxs-lookup"><span data-stu-id="c836d-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="c836d-111">În lista **Timp aprobat**, localizați și selectați una sau mai multe intrări de timp aprobate pentru a fi corectate.</span><span class="sxs-lookup"><span data-stu-id="c836d-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="c836d-112">Puteți utiliza filtrul pentru a localiza intrările conexe.</span><span class="sxs-lookup"><span data-stu-id="c836d-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="c836d-113">De exemplu, puteți filtra pentru un ID de proiect și puteți selecta toate intrările de timp aprobate cu acel ID de proiect.</span><span class="sxs-lookup"><span data-stu-id="c836d-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="c836d-114">Selectați **Corectați intrările**.</span><span class="sxs-lookup"><span data-stu-id="c836d-114">Select **Correct entries**.</span></span> <span data-ttu-id="c836d-115">Un nou jurnal de corecție este creat automat, cu tipul alocat **Corecție de timp**.</span><span class="sxs-lookup"><span data-stu-id="c836d-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="c836d-116">Intrările selectate sunt adăugate în jurnal.</span><span class="sxs-lookup"><span data-stu-id="c836d-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="c836d-117">Din pagina **Jurnal nou**, introduceți o **Descriere** pentru jurnalul de corectare, apoi selectați fila **Corecții intrări de timp**.</span><span class="sxs-lookup"><span data-stu-id="c836d-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="c836d-118">În secțiunea **Valori noi pentru intrările de timp**, actualizați câmpurile cu informațiile corecte, după caz.</span><span class="sxs-lookup"><span data-stu-id="c836d-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="c836d-119">De exemplu, puteți modifica proiectul alocat sau resursa rezervabilă.</span><span class="sxs-lookup"><span data-stu-id="c836d-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="c836d-120">Selectați **Previzualizare**.</span><span class="sxs-lookup"><span data-stu-id="c836d-120">Select **Preview**.</span></span> <span data-ttu-id="c836d-121">În caseta de dialog, selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="c836d-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="c836d-122">Pe fila **Linii de jurnal**, puteți vedea o listă cu datele reale originale care sunt legate de intrările de timp selectate care au fost inversate și liniile corespunzătoare corectate care au fost create.</span><span class="sxs-lookup"><span data-stu-id="c836d-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="c836d-123">Dacă trebuie efectuate corecții suplimentare, repetați pașii 5 și 6.</span><span class="sxs-lookup"><span data-stu-id="c836d-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="c836d-124">Toate datele reale corectate vor avea aceleași valori pe care le-ați selectat în secțiunea **Valori noi pentru intrările de timp**.</span><span class="sxs-lookup"><span data-stu-id="c836d-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="c836d-125">Când corecțiile apar așa cum este așteptat, selectați **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="c836d-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="c836d-126">În caseta de dialog, selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="c836d-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="c836d-127">Reveniți la zona **Vânzări**, selectați **Proiecte**, apoi deschideți proiectul pentru care tocmai ați actualizat intrările de timp.</span><span class="sxs-lookup"><span data-stu-id="c836d-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="c836d-128">Din pagina **Proiecte**, pe fila **Date reale**, vizualizați modificările pe care le-ați făcut.</span><span class="sxs-lookup"><span data-stu-id="c836d-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="c836d-129">Dacă fila **Date reale** nu este vizibilă, selectați **Date reale** > **asociate**.</span><span class="sxs-lookup"><span data-stu-id="c836d-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="c836d-130">În lista **Vizualizare asociată valori reale**, puteți vedea că intrările de timp originale care au fost inversate sunt încă listate, la fel și intrările de timp corectate corespunzătoare.</span><span class="sxs-lookup"><span data-stu-id="c836d-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="c836d-131">De exemplu, în graficul următor, există două elemente linie cu o cantitate de 8,00 care au debite listate în coloana Sumă.</span><span class="sxs-lookup"><span data-stu-id="c836d-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="c836d-132">În plus, există două elemente linie cu o cantitate de -8,00 care arată sumele creditate în coloana Sumă.</span><span class="sxs-lookup"><span data-stu-id="c836d-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="c836d-133">Aceste corecții aduc cantitatea la zero.</span><span class="sxs-lookup"><span data-stu-id="c836d-133">These corrections bring the quantity to zero.</span></span>

![Listă vizualizare asociată valori reale](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="c836d-135">Intrări de cheltuieli aprobate corect</span><span class="sxs-lookup"><span data-stu-id="c836d-135">Correct approved expense entries</span></span>

<span data-ttu-id="c836d-136">Urmați pașii următori pentru a corecta una sau mai multe intrări de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="c836d-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="c836d-137">În zona **Vânzări**, în panoul de navigare din stânga, sub **Tranzacții**, selectați **Cheltuieli aprobate**.</span><span class="sxs-lookup"><span data-stu-id="c836d-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="c836d-138">În lista **Cheltuieli aprobate**, selectați proiectul pe care doriți să îl corectați, apoi selectați **Corectați intrările**.</span><span class="sxs-lookup"><span data-stu-id="c836d-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="c836d-139">Un nou jurnal de corecție va fi creat automat, cu tipul alocat **Corecție de cheltuială**.</span><span class="sxs-lookup"><span data-stu-id="c836d-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="c836d-140">Din pagina **Jurnal nou**, introduceți o **Descriere** pentru corecție și din fila **Corecție cheltuieli**, în secțiunea **Valori noi pentru cheltuieli**, selectați câmpurile de date pe care doriți să le corectați pentru liniile de cheltuieli selectate.</span><span class="sxs-lookup"><span data-stu-id="c836d-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="c836d-141">De exemplu, puteți atribui cheltuielile altui **Proiect**, sau corecta **Categoria de cheltuieli**, **Data cheltuielilor**, sau **Resursă rezervabilă**.</span><span class="sxs-lookup"><span data-stu-id="c836d-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="c836d-142">Selectați **Previzualizare**.</span><span class="sxs-lookup"><span data-stu-id="c836d-142">Select **Preview**.</span></span> <span data-ttu-id="c836d-143">În caseta de dialog, selectați **OK**.</span><span class="sxs-lookup"><span data-stu-id="c836d-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="c836d-144">Verificați corecțiile de pe fila **Linii de jurnal**. Puteți vedea o listă cu datele reale originale care sunt legate de intrările de cheltuieli selectate care au fost inversate și liniile corespunzătoare corectate care au fost create.</span><span class="sxs-lookup"><span data-stu-id="c836d-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="c836d-145">Când valorile corectate apar așa cum este așteptat, selectați **Confirmare**.</span><span class="sxs-lookup"><span data-stu-id="c836d-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="c836d-146">În caseta de dialog, selectați **OK.**</span><span class="sxs-lookup"><span data-stu-id="c836d-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="c836d-147">Dacă valorile nu se afișează așa cum este așteptat, selectați **Anulare** pentru a reveni la lista **Cheltuieli aprobate**.</span><span class="sxs-lookup"><span data-stu-id="c836d-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="c836d-148">Repetați pașii 2 până la 5.</span><span class="sxs-lookup"><span data-stu-id="c836d-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="c836d-149">Datele reale corectate vor avea aceleași valori pe care le-ați selectat în secțiunea **Valori noi pentru cheltuieli**.</span><span class="sxs-lookup"><span data-stu-id="c836d-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="c836d-150">După ce confirmați jurnalul de corecție, navigați înapoi la proiectul sau proiectele pe care le-ați actualizat, pentru a vizualiza modificările.</span><span class="sxs-lookup"><span data-stu-id="c836d-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="c836d-151">În pagina proiectului, pe fila **Date reale**, treceți în revistă **Vizualizare asociată valori reale**.</span><span class="sxs-lookup"><span data-stu-id="c836d-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="c836d-152">Sunt enumerate intrările originale și intrările corectate.</span><span class="sxs-lookup"><span data-stu-id="c836d-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="c836d-153">Următorul grafic arată sumele de intrare pentru cheltuieli originale și sumele corespunzătoare de intrare ale cheltuielilor corectate.</span><span class="sxs-lookup"><span data-stu-id="c836d-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Date reale cheltuieli](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]