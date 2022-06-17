---
title: Tranziții de stare pe un subcontract
description: Acest articol explică tranzițiile de stat pe un subcontract în Microsoft Dynamics 365 Project Operations pe măsură ce subcontractul este creat, executat și închis.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919753"
---
# <a name="state-transitions-on-a-subcontract"></a>Tranziții de stare pe un subcontract 

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Acest articol explică tranzițiile de stat pentru un subcontract în Microsoft Dynamics 365 Project Operations. Fiecare stat este reprezentat fie ca proiect, confirmat, închis sau anulat. Următoarea imagine reprezintă tranzițiile de stare.

![Model de stat de subcontractare](../media/SubconStates.png)  

Următorul tabel oferă o descriere a ceea ce reprezintă fiecare stat în ciclul de viață al unui subcontract în Operațiuni de proiect.

| Stat/Județ/Provincie | Descriere | Tranziții permise |
| --- | --- | --- |
| Schițe | Aceasta reprezintă starea inițială a unui subcontract. Negocierile cu furnizorul sunt în desfășurare. Liniile și prețurile pot suferi modificări. Un subcontract în această stare poate fi utilizat pentru estimarea și personalul necesar pentru resurse și materiale ale proiectului. De asemenea, se poate face referire la timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract în această stare poate fi editat și șters. | Confirmat |
| Confirmat | Aceasta reprezintă etapa unui subcontract după încheierea negocierilor cu furnizorul privind prețurile și articolele rând achiziționate. Cu toate acestea, livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate este încă în desfășurare. Un subcontract în această stare poate fi utilizat pentru estimarea și personalul necesar pentru resurse și materiale ale proiectului. De asemenea, se poate face referire la timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract în această stare nu poate fi editat sau șters. The **Anulare** butonul vă permite să anulați un subcontract confirmat. The **Redeschide** butonul vă permite să redeschideți subcontractul pentru a-l aduce înapoi **Proiect** stare. Folosește **Închide** butonul pentru a închide un subcontract confirmat. | Închisă <br> Anulat <br> Schițe |
| Închisă | Aceasta reprezintă etapa unui subcontract în care livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate este finalizată. Un subcontract în această stare nu mai poate fi utilizat pentru estimarea și personalizarea cerințelor proiectului pentru resurse și materiale. De asemenea, nu mai poate fi referit la timp, cheltuieli și utilizarea materialelor pe un proiect. Un subcontract în această stare nu poate fi editat sau șters. | Fără |
| Anulat | Aceasta reprezintă etapa unui subcontract în care nu mai este necesară livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate. Un subcontract în această stare nu poate fi utilizat pentru estimarea și personalizarea cerințelor proiectului pentru resurse și materiale și nici nu poate fi referit la timp, cheltuieli și utilizarea materialelor pe un proiect. Un subcontract în această stare nu poate fi editat sau șters. | Fără |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
