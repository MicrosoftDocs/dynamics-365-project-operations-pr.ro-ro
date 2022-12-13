---
title: Linii de oferte bazate pe produs de cost
description: Acest articol oferă informații despre aplicarea unui preț de cost unei linii de ofertă pe bază de produs.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825627"
---
# <a name="costing-product-based-quote-lines"></a>Linii de oferte bazate pe produs de cost

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Linii de ofertă bazate pe produse din Dynamics 365 Project Operations au și un câmp **Preț de cost**. Acest câmp este utilizat pentru a urmări prețul de cost al produsului pe linia de ofertă și pentru calculele de profitabilitate din aval.

Atunci când se creează o linie de ofertă bazată pe produs pentru un produs din catalog, costul liniei de ofertă bazată pe produs este implicit de la **Cost standard** din catalogul de produse. Câmpul de cost standard din catalogul de produse este configurat în moneda de bază a Organizației. Costul unitar implicit pe linia de cotare bazată pe produs este convertit în moneda de vânzare din cotare.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Costul unitar pe o linie de ofertă pe bază de produs

Scopul de a avea un cost unitar pe o linie de ofertă bazată pe produs este de a permite costuri diferite pentru un produs pentru fiecare vânzare. Acesta nu este un scenariu tipic, dar uneori costul produsului poate fi redus de furnizor, în funcție de clientul vânzării finale.

De exemplu:

Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale A Datum Corporation. Fabrikam oferă servicii de instalare, dar brațele robotizate sunt achiziționate de la robotica Trey. Dacă instalarea brațelor robotizate la A Datum Corporation deschide o nouă verticală a industriei pentru brațele robotizate ale lui Trey, Trey ar putea acorda Fabrikam o reducere specială pentru această ofertă.

În acest caz, Fabrikam va crea o linie de cotare bazată pe produse pentru Robotic Arms și va introduce un cost unitar special pentru acest preț. Acest cost este diferit de costul standard al Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
