---
title: Ce este starea unui proiect
description: Acest subiect furnizează informații despre starea atribuită proiectelor în Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082668"
---
# <a name="understand-project-status"></a>Ce este starea unui proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Secțiunea **Stare** a paginii **Entitate de proiect** furnizează un rezumat al stării unui proiect pe baza costului și efortului.


## <a name="status-summary-fields"></a>Câmpuri rezumat stare

- Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului. Acest câmp utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere. 
- Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut. 
- Câmpul **Stare actualizată la** nu este modificabil. Valoarea din acest câmp este o marcă de timp care indică data ultimei actualizări a stării.
- Câmpurile **Planificarea performanței** și **Performanță de cost** sunt setate din grila de urmărire. Când planificarea și varianța de cost pentru nodul rădăcină din vizualizarea **Urmărire efort** sunt pozitive, aceste câmpuri sunt actualizate la **Avans**. Când programul și varianța costului pentru nodul rădăcină sunt negative, aceste câmpuri sunt setate la **În urmă**.
