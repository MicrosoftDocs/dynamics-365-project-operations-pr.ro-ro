---
title: Linii de contract bazate pe oportunitate
description: Acest subiect furnizează informații despre elemente de linie de oportunitate pe bază de proiect în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082722"
---
# <a name="product-based-opportunity-lines"></a>Linii de contract bazate pe oportunitate

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Liniile de oportunitate bazate pe produse sunt elemente rând din Oportunitate. Aceste linii sunt livrate clientului ca elemente rând distincte pe eventuala factură fără alte servicii cu valoare adăugată. Cheltuielile și consumul asociate nu sunt urmărite în sarcinile unor proiecte conexe.

Liniile bazate pe produse pot fi articole din catalog sau produse înscrise. Cea mai mare parte a funcționalității pe liniile bazate pe produse ale unei oportunități urmează funcționalitatea oferită de aplicația Dynamics 365 Sales. Pentru mai multe informații despre liniile de oportunitate bazate pe produse, consultați [Adăugați produse la o oportunitate](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Un concept despre liniile de oportunități bazate pe produse, care este specific oportunităților bazate pe proiecte, este **Bugetul clientului**. Utilizați acest câmp pentru a urmări suma pe care clientul este dispus să o plătească pentru elementul rând.

Dacă metoda veniturilor din rezumatul Opportunity este setată la **Calculat de sistem** , valorile bugetului clienților pe linii bazate pe produse și proiecte sunt rezumate pentru a calcula veniturile estimate.
