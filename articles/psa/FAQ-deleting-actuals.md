---
title: De ce nu pot să șterg înregistrările din entitatea Valori reale?
description: Acest subiect furnizează informații despre motivul pentru care nu puteți șterge înregistrările din entitatea Valori reale.
author: JPBurrows
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002886"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>De ce nu pot șterge înregistrări din entitatea Valori reale?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) nu vă permite să ștergeți valorile reale deoarece acestea servesc ca sursă de adevăr pentru tranzacțiile care au implicații financiare pentru sistemele din aval, cum ar fi registrul general. Dacă valorile reale ar putea fi șterse, integritatea tranzacțiilor de raportare financiară ar putea fi pusă la îndoială. Pentru a stabili o pistă de audit, clienții ar trebui să utilizeze jurnale pentru a crea tranzacții compensatoare.



[!INCLUDE[footer-include](../includes/footer-banner.md)]