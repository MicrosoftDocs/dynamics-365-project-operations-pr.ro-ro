---
title: De ce nu pot să șterg înregistrările din entitatea Valori reale?
description: Acest subiect furnizează informații despre motivul pentru care nu puteți șterge înregistrările din entitatea Valori reale.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286083"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="e7be3-103">De ce nu pot șterge înregistrări din entitatea Valori reale?</span><span class="sxs-lookup"><span data-stu-id="e7be3-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e7be3-104">Project Service Automation (PSA) nu vă permite să ștergeți valorile reale deoarece acestea servesc ca sursă de adevăr pentru tranzacțiile care au implicații financiare pentru sistemele din aval, cum ar fi registrul general.</span><span class="sxs-lookup"><span data-stu-id="e7be3-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="e7be3-105">Dacă valorile reale ar putea fi șterse, integritatea tranzacțiilor de raportare financiară ar putea fi pusă la îndoială.</span><span class="sxs-lookup"><span data-stu-id="e7be3-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="e7be3-106">Pentru a stabili o pistă de audit, clienții ar trebui să utilizeze jurnale pentru a crea tranzacții compensatoare.</span><span class="sxs-lookup"><span data-stu-id="e7be3-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]