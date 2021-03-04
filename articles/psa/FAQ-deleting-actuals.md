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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148973"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="61013-103">De ce nu pot șterge înregistrări din entitatea Valori reale?</span><span class="sxs-lookup"><span data-stu-id="61013-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="61013-104">Project Service Automation (PSA) nu vă permite să ștergeți valorile reale deoarece acestea servesc ca sursă de adevăr pentru tranzacțiile care au implicații financiare pentru sistemele din aval, cum ar fi registrul general.</span><span class="sxs-lookup"><span data-stu-id="61013-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="61013-105">Dacă valorile reale ar putea fi șterse, integritatea tranzacțiilor de raportare financiară ar putea fi pusă la îndoială.</span><span class="sxs-lookup"><span data-stu-id="61013-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="61013-106">Pentru a stabili o pistă de audit, clienții ar trebui să utilizeze jurnale pentru a crea tranzacții compensatoare.</span><span class="sxs-lookup"><span data-stu-id="61013-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

