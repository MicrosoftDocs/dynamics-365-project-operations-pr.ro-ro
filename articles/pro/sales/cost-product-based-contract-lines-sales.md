---
title: Linii de contract bazate pe produs de cost - simplificat
description: Acest subiect oferă informații despre creare
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3def4c330dc9aadbf5ff806ef7682fbfd1072e4b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599285"
---
# <a name="cost-product-based-contract-lines---lite"></a>Linii de contract bazate pe produs de cost - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Liniile contractuale pe bază de produse în Dynamics 365 Project Operations includ câmpul **Preț de cost**, care stochează prețul de cost al produsului pentru calculele de profitabilitate din aval.

Când se creează o linie contractuală bazată pe produs pentru un produs de catalog, costul liniei reiese implicit din câmpul **Cost standard** din catalogul de produse. Câmpul **Cost standard** din catalogul de produse este configurat în moneda de bază a Organizației. Când costul unitar este implicit pe linia contractului, acesta este convertit în moneda de vânzare din contract.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Costul unitar pe o linie de contract pe bază de produs

Având un cost unitar pe o linie de contract bazată pe produse, vă permite a avea costuri diferite ale produsului pentru fiecare vânzare a unei unități. Deși nu sunt întotdeauna necesare, există anumite scenarii în care costul produsului poate fi redus pentru client de către furnizor. Luați în considerare următorul scenariu:

Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale Adatum Corporation. Fabrikam oferă servicii de instalare, dar brațele robotice provin de la Trey Research. Dacă instalarea brațelor robotizate la Adatum Corporation deschide o nouă verticală a industriei pentru brațele de la Trey Research, aceștia ar putea acorda Fabrikam o reducere specială pentru această ofertă. În acest caz, Fabrikam creează o linie contractuală bazată pe produse pentru Brațe robotice. Pentru acest contract se introduce un cost pe unitate. Costul este diferit de costul brațelor robotice de la Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]