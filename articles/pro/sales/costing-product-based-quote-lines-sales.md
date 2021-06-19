---
title: Linii de oferte bazate pe produs de cost
description: Acest subiect oferă informații despre aplicarea unui preț de cost unei linii de ofertă pe bază de produs.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003466"
---
# <a name="costing-product-based-quote-lines"></a>Linii de oferte bazate pe produs de cost

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


Linii de ofertă bazate pe produse din Dynamics 365 Project Operations au și un câmp **Preț de cost**. Acest câmp este utilizat pentru a urmări prețul de cost al produsului pe linia de ofertă și pentru calculele de profitabilitate din aval.

Atunci când se creează o linie de ofertă bazată pe produs pentru un produs din catalog, costul liniei de ofertă bazată pe produs este implicit de la **Cost standard** din catalogul de produse. Câmpul de cost standard din catalogul de produse este configurat în moneda de bază a Organizației. Costul unitar implicit pe linia de cotare bazată pe produs este convertit în moneda de vânzare din cotare.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Costul unitar pe o linie de ofertă pe bază de produs

Scopul de a avea un cost unitar pe o linie de ofertă bazată pe produs este de a permite costuri diferite pentru un produs pentru fiecare vânzare. Acesta nu este un scenariu tipic, dar uneori costul produsului poate fi redus de furnizor, în funcție de clientul vânzării finale.

De exemplu:

Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale A Datum Corporation. Fabrikam oferă servicii de instalare, dar brațele robotizate sunt achiziționate de la robotica Trey. Dacă instalarea brațelor robotizate la A Datum Corporation deschide o nouă verticală a industriei pentru brațele robotizate ale lui Trey, Trey ar putea acorda Fabrikam o reducere specială pentru această ofertă.

În acest caz, Fabrikam va crea o linie de cotare bazată pe produse pentru Robotic Arms și va introduce un cost unitar special pentru acest preț. Acest cost este diferit de costul standard al Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]