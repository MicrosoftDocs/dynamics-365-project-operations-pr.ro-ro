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
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993116"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>De ce nu pot șterge înregistrări din entitatea Valori reale?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) nu vă permite să ștergeți valorile reale deoarece acestea servesc ca sursă de adevăr pentru tranzacțiile care au implicații financiare pentru sistemele din aval, cum ar fi registrul general. Dacă valorile reale ar putea fi șterse, integritatea tranzacțiilor de raportare financiară ar putea fi pusă la îndoială. Pentru a stabili o pistă de audit, clienții ar trebui să utilizeze jurnale pentru a crea tranzacții compensatoare.



[!INCLUDE[footer-include](../includes/footer-banner.md)]