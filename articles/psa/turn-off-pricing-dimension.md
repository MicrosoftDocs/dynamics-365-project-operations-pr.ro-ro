---
title: Dezactivarea unei dimensiuni de tarifare
description: Acest articol arată cum se configurează dimensiunile de tarifare în soluția Project service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 81c3cfaad8dc8d057985b509f20c3ba31de45e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913175"
---
# <a name="turn-off-a-pricing-dimension"></a>Dezactivarea unei dimensiuni de tarifare

[!include [banner](../includes/psa-now-project-operations.md)]

Poate fi necesar să revizuiți și să actualizați strategia de tarifare la fiecare câțiva ani. Orice actualizări pe care le efectuați pot necesita dezactivarea unei dimensiuni de tarifare existente și crearea uneia noi. De exemplu, este posibil să fi tarifat în trecut în funcție de **Rol**, dar acum ați decis să tarifați în funcție de **Experiența de lucru**. Acest lucru vă poate solicita să dezactivați **Rol** ca dimensiune de tarifare și să creați **Experiență de lucru** ca noua dimensiune de tarifare. 

Dezactivarea unei dimensiuni de tarifare, indiferent dacă este predefinită sau personalizată, se poate face prin setarea câmpurilor **Aplicabil la costuri** și **Aplicabil la vânzări** ale dimensiunii de tarifare la **Nu**.

Cu toate acestea, atunci când procedați astfel, este posibil să primiți următorul mesaj de eroare.

![Eroare de proces de business probabil atunci când dezactivați o dimensiune de tarifare.](media/Business-Process-Error.png)


Acest mesaj de eroare indică faptul că există înregistrări de preț care au fost parametrizate anterior pentru dimensiunea care este dezactivată. Toate înregistrările **Preț rol** și **Adaos preț rol** care se referă la o dimensiune trebuie șterse înainte ca aplicabilitatea dimensiunii să fie setată la **Nu**. Această regulă se aplică atât dimensiunilor de tarifare predefinite, cât și oricăror dimensiuni de preț particularizate pe care le-ați creat. Motivul pentru această validare se datorează faptului că Project service are o constrângere că fiecare înregistrare de **Preț de rol** trebuie să aibă o combinație unică de dimensiuni. De exemplu, pe o listă de prețuri numită **Rate de cost SUA 2018**, aveți următoarele rânduri de **Preț rol**. 

| Titlu standard         | Unitate organizațională    |Unitate   |Preț  |Monedă  |
| -----------------------|-------------|-------|-------|----------|
| Inginer sisteme|Contoso US|Hour| 100|USD|
| Inginer sisteme senior|Contoso US|Hour| 150| USD|


Când dezactivați **Titlu standard** ca dimensiunea de tarifare, iar motorul de tarifare Project Service caută un preț, acesta va utiliza numai valoarea **Unității organizaționale** din contextul de intrare. Dacă **Unitatea organizațională** din contextul de intrare este „Contoso US", rezultatul va fi non-determinist, deoarece ambele rânduri se vor potrivi. Pentru a evita acest scenariu, atunci când creați înregistrări de **Preț de rol**, Project Service validează unicitatea combinației de dimensiuni. Dacă dimensiunea este dezactivată după crearea înregistrărilor de **Preț de rol**, această restricție poate fi încălcată. Prin urmare, este necesar ca înainte de a dezactiva o dimensiune să ștergeți toate rândurile **Preț rol** și **Adaos preț rol** care au această valoare de dimensiune populată.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
