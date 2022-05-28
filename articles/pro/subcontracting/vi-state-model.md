---
title: Tranziții de stat pe o factură de furnizor
description: Acest subiect explică tranzițiile de stare pe o factură de furnizor în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584703"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Tranziții de stat pe o factură de furnizor

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest subiect explică tranzițiile de stare pe o factură de furnizor în Microsoft Dynamics 365 Project Operations. Sunt utilizate următoarele stări: **Proiect**, **revizuire**, **·**, **asteptare**, și **Anulat**.

Următoarele ilustrații arată tranzițiile de stare.

![Modelul de tranziție a stării de subcontractare.](../media/VI_State_Model.jpg)

Următorul tabel explică ce reprezintă fiecare stare în ciclul de viață al unei facturi de furnizor în Operațiuni de proiect.

| Stat/Județ/Provincie | Descriere | Tranziții permise |
| --- | --- | --- |
| Schițe | Această stare este starea inițială a unei facturi de furnizor. Liniile și prețurile pot fi modificate. O factură de furnizor în această stare poate fi editată și ștearsă. | In proces |
| În curs de revizuire | Această stare reprezintă starea de procesare a unei facturi de furnizor. Cel puțin o linie de factură de furnizor are o stare de verificare de **În curs**. | Confirmat, în așteptare |
| Confirmat | Această stare reprezintă etapa unei facturi de furnizor în care aplicația a creat costuri reale pentru fiecare linie de factură de furnizor. Orice costuri reale legate care au fost corelate cu liniile de factură a furnizorului au fost inversate și înlocuite cu costurile reale din acele linii de factură a furnizorului. O factură de furnizor în această stare nu poate fi editată sau ștearsă. Puteți folosi **Anulare** butonul pentru a anula o factură de furnizor confirmată. Acțiunea Anulare inversează impactul acțiunii Confirmare. | Anulat |
| În așteptare | <p>Această stare reprezintă o etapă a unei facturi de furnizor în care factura de furnizor nu se poate muta din cauza unei probleme cu factura sau starea furnizorului. O factură de furnizor în această stare nu poate fi confirmată, anulată, editată sau ștearsă.</p><p>Puteți utiliza acțiunea Redeschidere pentru a muta factura furnizorului în **Proiect** sau **În revizuire** stat. Dacă cel puțin o linie de pe factura furnizorului are o stare de verificare de **În curs** sau **Complet**, factura furnizorului va fi redeschisă în **În revizuire** stat. Dacă toate rândurile de pe factura furnizorului au o stare de verificare de **Nu a început**, factura furnizorului va fi redeschisă în **Proiect** stat.</p> | Schiță, În revizuire |
| Anulat | Această stare reprezintă etapa unui subcontract în care nu mai este necesară livrarea efectivă a materialelor și/sau a lucrărilor prin resurse subcontractate. Un subcontract în această stare nu poate fi utilizat pentru estimarea și personalizarea cerințelor proiectului pentru resurse și materiale și, de asemenea, nu poate fi referit la timp, cheltuieli și utilizarea materialelor pentru un proiect. Un subcontract în această stare nu poate fi editat sau șters. | Fără |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
