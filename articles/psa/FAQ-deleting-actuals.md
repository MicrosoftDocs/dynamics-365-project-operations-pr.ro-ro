---
title: De ce nu pot să șterg înregistrările din entitatea Valori reale?
description: Acest subiect furnizează informații despre motivul pentru care nu puteți șterge înregistrările din entitatea Valori reale.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082922"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="005ec-103">De ce nu pot șterge înregistrări din entitatea Valori reale?</span><span class="sxs-lookup"><span data-stu-id="005ec-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="005ec-104">Project Service Automation (PSA) nu vă permite să ștergeți valorile reale deoarece acestea servesc ca sursă de adevăr pentru tranzacțiile care au implicații financiare pentru sistemele din aval, cum ar fi registrul general.</span><span class="sxs-lookup"><span data-stu-id="005ec-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="005ec-105">Dacă valorile reale ar putea fi șterse, integritatea tranzacțiilor de raportare financiară ar putea fi pusă la îndoială.</span><span class="sxs-lookup"><span data-stu-id="005ec-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="005ec-106">Pentru a stabili o pistă de audit, clienții ar trebui să utilizeze jurnale pentru a crea tranzacții compensatoare.</span><span class="sxs-lookup"><span data-stu-id="005ec-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

