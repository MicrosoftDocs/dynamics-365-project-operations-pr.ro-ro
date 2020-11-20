---
title: Diurne
description: Acest subiect oferă informații despre regulile per diem care sunt utilizate în gestionarea cheltuielilor.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128523"
---
# <a name="per-diems"></a><span data-ttu-id="34e97-103">Diurne</span><span class="sxs-lookup"><span data-stu-id="34e97-103">Per diems</span></span>

<span data-ttu-id="34e97-104">_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_</span><span class="sxs-lookup"><span data-stu-id="34e97-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="34e97-105">O diurnă este o indemnizație care se plătește unui lucrător care călătorește pentru muncă.</span><span class="sxs-lookup"><span data-stu-id="34e97-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="34e97-106">În gestionarea cheltuielilor, puteți crea reguli pentru diurnă pentru diferite situații de călătorie.</span><span class="sxs-lookup"><span data-stu-id="34e97-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="34e97-107">Tarifele diurnei se pot baza pe perioada anului, locația călătoriei sau ambele.</span><span class="sxs-lookup"><span data-stu-id="34e97-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="34e97-108">Când creați o regulă de diurnă, puteți specifica că un procent din rata diemului va fi reținut dacă un lucrător primește mese sau servicii gratuite.</span><span class="sxs-lookup"><span data-stu-id="34e97-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="34e97-109">De asemenea, puteți seta un număr minim și maxim de ore pe care le poate aplica tariful diurnei pentru călătoria unui lucrător.</span><span class="sxs-lookup"><span data-stu-id="34e97-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="34e97-110">Configurație</span><span class="sxs-lookup"><span data-stu-id="34e97-110">Configuration</span></span> 

1. <span data-ttu-id="34e97-111">Pentru a adăuga locații pentru diurnp, accesați **Configurare** > **Calcule și coduri** > **Locații diurnă**.</span><span class="sxs-lookup"><span data-stu-id="34e97-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="34e97-112">Pentru fiecare dintre locațiile adăugate mai sus, selectați o diurnă zilnică și o monedă valabile între o anumită dată de începere și de sfârșit pentru hotel, mese și alte cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="34e97-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="34e97-113">Ratele diurnei și valutele sunt configurate în **Configurare** > **Calcule și coduri** > **Diurne**.</span><span class="sxs-lookup"><span data-stu-id="34e97-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="34e97-114">Pe pagina **Locații diurnă**, configurați nivelurile de diurnă.</span><span class="sxs-lookup"><span data-stu-id="34e97-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="34e97-115">Nivelurile de tarifare a diurnei vă permit să definiți procentul împărțirii unei diurne pentru hotel, masă și alte cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="34e97-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="34e97-116">Pentru a specifica reducerea procentuală a mesei pentru micul dejun, prânz sau cină, actualizați câmpurile de pe pagina **Parametrii de gestionare a cheltuielilor** pe fila **Diurnă**.</span><span class="sxs-lookup"><span data-stu-id="34e97-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="34e97-117">Trimiteți cheltuielile folosind diurna</span><span class="sxs-lookup"><span data-stu-id="34e97-117">Submit expenses using per diem</span></span>
<span data-ttu-id="34e97-118">Pentru a trimite cheltuieli cu diurnele, utilizați categoria de cheltuieli **Diurnă** atunci când creați un raport de cheltuieli.</span><span class="sxs-lookup"><span data-stu-id="34e97-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="34e97-119">Introduceți **Diurnă data de la**, **Diurnă data până la**, și **Locație diurnă**.</span><span class="sxs-lookup"><span data-stu-id="34e97-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="34e97-120">Suma va fi calculată pe baza ratelor diurnei pentru locația selectată, iar reducerea mesei va fi calculată pe baza nivelurilor tarifelor diurne.</span><span class="sxs-lookup"><span data-stu-id="34e97-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
