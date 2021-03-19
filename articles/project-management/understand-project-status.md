---
title: Ce este starea unui proiect
description: Acest subiect oferă informații despre starea atribuită proiectelor în Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286488"
---
# <a name="understand-project-status"></a>Ce este starea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Secțiunea **Stare** a paginii **Entitate de proiect** furnizează un rezumat al stării unui proiect pe baza costului și efortului.


## <a name="status-summary-fields"></a>Câmpuri rezumat stare

- Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului. Acest câmp utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere. 
- Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut. 
- Câmpul **Stare actualizată la** nu este editabil. Valoarea din acest câmp este o marcă de timp care indică data ultimei actualizări a stării.
- Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din grila de urmărire. Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, aceste câmpuri sunt actualizate la **Avans**. Când programul și varianța costului pentru nodul rădăcină sunt negative, aceste câmpuri sunt setate la **În urmă**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]