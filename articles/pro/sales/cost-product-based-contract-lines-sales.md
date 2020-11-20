---
title: Linii de contract bazate pe produs de cost - simplificat
description: Acest subiect oferă informații despre creare
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177256"
---
# <a name="cost-product-based-contract-lines---lite"></a>Linii de contract bazate pe produs de cost - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Linii de contract bazate pe produs din Dynamics 365 Project Operations includ câmpul **Preț de cost**, care stochează prețul de cost al produsului pentru calculele de profitabilitate din aval.

Atunci când se creează o linie de contract bazată pe produs pentru un produs din catalog, costul liniei de contract bazată pe produs este implicit de la câmpul **Cost standard** din catalogul de produse. Câmpul **Cost standard** din catalogul de produse este configurat în moneda de bază a Organizației. Când costul unitar este implicit pe linia contractului, acesta este convertit în moneda de vânzare din contract.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Costul unitar pe o linie de contract pe bază de produs

Având un cost unitar pe o linie de contract bazată pe produse, vă permite a avea costuri diferite ale produsului pentru fiecare vânzare a unei unități. Deși nu sunt întotdeauna necesare, există anumite scenarii în care costul produsului poate fi redus pentru client de către furnizor. Luați în considerare următorul scenariu:

Fabrikam Robotics instalează brațe robotizate pe liniile de asamblare ale Adatum Corporation. Fabrikam oferă servicii de instalare, dar brațele robotizate sunt achiziționate de la Trey Research. Dacă instalarea brațelor robotizate la Adatum Corporation deschide o nouă verticală a industriei pentru brațele de la Trey Research, aceștia ar putea acorda Fabrikam o reducere specială pentru această ofertă. În acest caz, Fabrikam creează o linie contractuală bazată pe produse pentru Robotic Arms și introduce un cost pe unitate pentru acest contract, care este diferit de costul standard al brațelor robotizate de la Trey Research.
