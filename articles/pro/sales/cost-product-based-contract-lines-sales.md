---
title: Linii de contract bazate pe produs de cost - simplificat
description: Acest subiect oferă informații despre creare
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55f74b016b55945433083e11902003cea99f1aa463264cdd95b0aad389592e20
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997351"
---
# <a name="cost-product-based-contract-lines---lite"></a>Linii de contract bazate pe produs de cost - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Liniile contractuale pe bază de produse în Dynamics 365 Project Operations includ câmpul **Preț de cost**, care stochează prețul de cost al produsului pentru calculele de profitabilitate din aval.

Când se creează o linie contractuală bazată pe produs pentru un produs de catalog, costul liniei reiese implicit din câmpul **Cost standard** din catalogul de produse. Câmpul **Cost standard** din catalogul de produse este configurat în moneda de bază a Organizației. Când costul unitar este implicit pe linia contractului, acesta este convertit în moneda de vânzare din contract.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Costul unitar pe o linie de contract pe bază de produs

Având un cost unitar pe o linie de contract bazată pe produse, vă permite a avea costuri diferite ale produsului pentru fiecare vânzare a unei unități. Deși nu sunt întotdeauna necesare, există anumite scenarii în care costul produsului poate fi redus pentru client de către furnizor. Luați în considerare următorul scenariu:

Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale Adatum Corporation. Fabrikam oferă servicii de instalare, dar brațele robotice provin de la Trey Research. Dacă instalarea brațelor robotizate la Adatum Corporation deschide o nouă verticală a industriei pentru brațele de la Trey Research, aceștia ar putea acorda Fabrikam o reducere specială pentru această ofertă. În acest caz, Fabrikam creează o linie contractuală bazată pe produse pentru Brațe robotice. Pentru acest contract se introduce un cost pe unitate. Costul este diferit de costul brațelor robotice de la Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]