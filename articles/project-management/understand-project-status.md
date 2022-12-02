---
title: Ce este starea unui proiect
description: Acest articol oferă informații despre starea atribuită proiectelor în Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 86cb60b634b62af23f39720c0452dca82ff3ad26
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923617"
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