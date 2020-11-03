---
title: Dezactivarea unei dimensiuni de preț
description: Acest subiect oferă informații despre cum să dezactivați dimensiunile de preț.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a7c91ef70b1dd3697f6a8b5044c6ad4a14c4e74
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082892"
---
# <a name="turning-off-a-pricing-dimension"></a>Dezactivarea unei dimensiuni de preț

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Poate fi necesar să revizuiți și să actualizați strategia de tarifare la fiecare câțiva ani. Orice actualizări pe care le efectuați pot necesita dezactivarea unei dimensiuni de tarifare existente și crearea uneia noi. De exemplu, este posibil să fi tarifat în trecut în funcție de **Rol** , dar acum ați decis să tarifați în funcție de **Experiența de lucru**. Acest lucru vă poate solicita să dezactivați **Rol** ca dimensiune de tarifare și să creați **Experiența de lucru** ca noua dimensiune de tarifare. 

Dezactivarea unei dimensiuni de tarifare, indiferent dacă este predefinită sau personalizată, se poate face prin setarea câmpurilor **Aplicabil la costuri** și **Aplicabil la vânzări** ale dimensiunii de tarifare la **Nu**.

Cu toate acestea, atunci când faceți acest lucru, este posibil să primiți mesajul de eroare, **Dimensiunea prețurilor nu poate fi actualizată sau ștearsă dacă există înregistrări de preț asociate.**

Acest mesaj de eroare indică faptul că există înregistrări de preț care au fost parametrizate anterior pentru dimensiunea care este dezactivată. Toate înregistrările **Preț rol** și **Adaos preț rol** care se referă la o dimensiune trebuie șterse înainte ca aplicabilitatea dimensiunii să fie setată la **Nu**. Această regulă se aplică atât dimensiunilor de tarifare predefinite, cât și oricăror dimensiuni de preț particularizate pe care le-ați creat. Motivul pentru această validare este pentru că înregistrarea **Rol de preț** trebuie să aibă o combinație unică de dimensiuni. De exemplu, pe o listă de prețuri numită **Rate de cost SUA 2018** , aveți următoarele rânduri de **Preț rol**. 

| Titlu standard         | Unitate organizațională    |Unitate   |Preț  |Monedă  |
| -----------------------|-------------|-------|-------|----------|
| Inginer sisteme|Contoso US|Hour| 100|USD|
| Inginer sisteme senior|Contoso US|Hour| 150| USD|


Când dezactivați **Titlu standard** ca dimensiunea de tarifare, iar motorul de tarifare caută un preț, acesta va utiliza numai valoarea **Unității organizaționale** din contextul de intrare. Dacă **Unitatea organizațională** din contextul de intrare este „Contoso US", rezultatul va fi non-determinist, deoarece ambele rânduri se vor potrivi. Pentru a evita acest scenariu, atunci când creați înregistrări de **Preț de rol** , sistemul validează unicitatea combinației de dimensiuni. Dacă dimensiunea este dezactivată după crearea înregistrărilor de **Preț de rol** , această restricție poate fi încălcată. Prin urmare, este necesar ca înainte de a dezactiva o dimensiune să ștergeți toate rândurile **Preț rol** și **Adaos preț rol** care au această valoare de dimensiune populată.
