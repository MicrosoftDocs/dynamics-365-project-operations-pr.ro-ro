---
title: Ce este nou sau modificat în Project Service Automation versiunea 3.x etapa 1 2020
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 3 etapa 1 2020.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082742"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="b58e8-103">Ce este nou sau modificat în Project Service Automation versiunea 3 etapa 1 2020</span><span class="sxs-lookup"><span data-stu-id="b58e8-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="b58e8-104">Subiectul subliniază considerentele cheie de actualizare atunci când treceți la cea mai recentă versiune a Project Service Automation (PSA) versiunea 3.x versiunea 1 2020.</span><span class="sxs-lookup"><span data-stu-id="b58e8-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="b58e8-105">Intrare de timp</span><span class="sxs-lookup"><span data-stu-id="b58e8-105">Time entry</span></span>
<span data-ttu-id="b58e8-106">Experiența de intrare în timp a fost extinsă pentru a oferi capabilități pentru prelungirea intrării timpului în mai multe scenarii de clienți.</span><span class="sxs-lookup"><span data-stu-id="b58e8-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="b58e8-107">Aceasta include capacitatea de a adăuga tipuri de intrare, care conduc acum un comportament specific bazat pe numele schemei de câmp **Setări de intrare de timp** , afișat ca **Sursa timpului**.</span><span class="sxs-lookup"><span data-stu-id="b58e8-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="b58e8-108">A fost adăugată o nouă soluție, numită Timp, Cheltuieli, Declarație și Aprobări (TESA) pentru a susține această funcționalitate.</span><span class="sxs-lookup"><span data-stu-id="b58e8-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="b58e8-109">Considerent legat de upgrade</span><span class="sxs-lookup"><span data-stu-id="b58e8-109">Upgrade consideration</span></span>
<span data-ttu-id="b58e8-110">Pentru a sprijini această funcționalitate, rolurile din cadrul PSA au fost actualizate pentru a include noi privilegii.</span><span class="sxs-lookup"><span data-stu-id="b58e8-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="b58e8-111">Aceste privilegii acordă acces de citire la noua entitate, **Setări de intrare de timp**.</span><span class="sxs-lookup"><span data-stu-id="b58e8-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="b58e8-112">Utilizatorilor care necesită capacitatea de a înregistra timp ar trebui să li se acorde rolul de utilizator **Utilizator de intrare în timp** pe lângă rolurile existente.</span><span class="sxs-lookup"><span data-stu-id="b58e8-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="b58e8-113">Acest rol include noua funcționalitate și asigură că intrarea în timp va continua să funcționeze.</span><span class="sxs-lookup"><span data-stu-id="b58e8-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="b58e8-114">În plus, dacă aveți orice module de aplicație personalizate care includ toate formularele pentru entitatea de intrare în timp, vi se va solicita eliminarea **Formular de introducere rapidă a timpului TESA** din modul.</span><span class="sxs-lookup"><span data-stu-id="b58e8-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="b58e8-115">Modificările de intrare de timp extinse în prezent</span><span class="sxs-lookup"><span data-stu-id="b58e8-115">Currently extended time entry changes</span></span>
<span data-ttu-id="b58e8-116">Pentru a reduce impactul asupra utilizatorilor actuali de intrare în timp, această modificare a rolului este singura cerință esențială necesară pentru a continua utilizarea intrării în timp.</span><span class="sxs-lookup"><span data-stu-id="b58e8-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="b58e8-117">Dacă ați creat vizualizări personalizate sau experiențe de intrare în timp separate, trebuie să setați câmpurile **Setare intrare timp** la valoarea corectă PSA.</span><span class="sxs-lookup"><span data-stu-id="b58e8-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
