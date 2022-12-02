---
title: Tranziții de stare pe o factură de furnizor
description: Acest articol explică tranzițiile de stare pe o factură de furnizor în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261059"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Tranziții de stare pe o factură de furnizor

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol explică tranzițiile de stare pe o factură de furnizor în Microsoft Dynamics 365 Project Operations. Sunt utilizate următoarele stări: **Schiță**, **În curs de revizuire**, **Confirmat**, **În așteptare** și **Anulat**.

Următoarele ilustrații afișează tranzițiile de stare.

![Model de tranziție de stare a unui subcontract.](../media/VI_State_Model.jpg)

Următorul tabel explică ce anume reprezintă fiecare stare în ciclul de viață al unei facturi de furnizor în Project Operations.

| Stat/Județ/Provincie | Descriere | Tranziții permise |
| --- | --- | --- |
| Schițe | Această stare este starea inițială a unei facturi de furnizor. Liniile și prețurile pot fi modificate. O factură de furnizor în această stare poate fi editată și ștearsă. | În curs de procesare |
| În curs de revizuire | Această stare reprezintă starea de procesare a unei facturi de furnizor. Cel puțin o linie de factură de furnizor are o stare de verificare de **În curs**. | Confirmat, În așteptare |
| Confirmată | Această stare reprezintă etapa unei facturi de furnizor în care aplicația a creat costuri reale pentru fiecare linie de factură de furnizor. Orice costuri reale legate care au fost corelate cu liniile de factură de furnizor au fost inversate și înlocuite cu costurile reale din acele linii de factură furnizor. O factură de furnizor în această stare nu poate fi editată sau ștearsă. Puteți folosi butonul **Anulare** pentru a anula o factură de furnizor confirmată. Acțiunea Anulare inversează impactul acțiunii Confirmare. | Anulat |
| În așteptare | <p>Această stare reprezintă o etapă a unei facturi de furnizor în care factura de furnizor nu se poate muta din cauza unei probleme cu factura sau starea furnizorului. O factură de furnizor în această stare nu poate fi confirmată, anulată, editată sau ștearsă.</p><p>Puteți folosi acțiunea Redeschidere pentru a muta factura furnizorului la starea **Schiță** sau **În curs de revizuire**. Dacă cel puțin o linie de pe factura de furnizor are o stare de verificare de **În curs** sau **Finalizat**, factura furnizorului va fi redeschisă în starea **În curs de revizuire**. Dacă toate rândurile de pe factura furnizorului au o stare de verificare de **Neînceput**, factura furnizorului va fi redeschisă în starea **Schiță**.</p> | Schiță, În curs de revizuire |
| Anulat | Aceasta stare reprezintă etapa unui subcontract în care livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate nu mai este solicitată. Un subcontract în această stare nu poate fi utilizat pentru estimarea și încadrarea cerințelor proiectului pentru resurse și materiale și, de asemenea, nu poate fi utilizat ca referință pentru timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract aflat în această stare nu poate fi editat sau șters. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
