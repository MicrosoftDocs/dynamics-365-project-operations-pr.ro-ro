---
title: Tranziții de stare pe un subcontract
description: Acest articol explică tranzițiile de stare pe un subcontract în Microsoft Dynamics 365 Project Operations pe măsură ce subcontractul este creat, executat și închis.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522943"
---
# <a name="state-transitions-on-a-subcontract"></a>Tranziții de stare pe un subcontract 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest articol explică tranzițiile de stare pe un subcontract în Microsoft Dynamics 365 Project Operations. Fiecare stare este reprezentată fie ca schiță, confirmat, închis sau anulat. Următoarea imagine reprezintă tranzițiile de stare.

![Model de stare de subcontractare](../media/SubconStates.png)  

Următorul tabel oferă o descriere a ceea ce reprezintă fiecare stare în ciclul de viață al unui subcontract în Project Operations.

| Stat/Județ/Provincie | Descriere | Tranziții permise |
| --- | --- | --- |
| Schițe | Aceasta reprezintă starea inițială a unui subcontract. Negocierile cu furnizorul sunt în curs. Liniile și prețurile pot suferi modificări. Un subcontract în această stare poate fi utilizat pentru estimarea și încadrarea cerințelor necesare pentru resurse și materiale ale proiectului. De asemenea, aceasta poate constitui o referință pentru timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract în această stare poate fi editat și șters. | Confirmată |
| Confirmată | Aceasta reprezintă etapa unui subcontract după încheierea negocierilor cu furnizorul privind prețurile și articolele de linie achiziționate. Cu toate acestea, livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate este încă în curs. Un subcontract în această stare poate fi utilizat pentru estimarea și încadrarea cerințelor necesare pentru resurse și materiale ale proiectului. De asemenea, aceasta poate constitui o referință pentru timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract în această stare nu poate fi editat sau șters. Butonul **Anulare** vă permite să anulați un subcontract confirmat. Butonul **Redeschidere** vă permite să redeschideți subcontractul pentru a-l aduce înapoi la starea de **Schiță**. Utilizați butonul **Închidere** pentru a închide un subcontract confirmat. | Închisă <br> Anulat <br> Schițe |
| Închisă | Aceasta reprezintă etapa unui subcontract în care livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate este finalizată. Un subcontract în această stare nu mai poate fi utilizat pentru estimarea și încadrarea cerințelor necesare pentru resurse și materiale ale proiectului. De asemenea, aceasta nu mai poate constitui o referință pentru timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract în această stare nu poate fi editat sau șters. | Fără |
| Anulat | Aceasta reprezintă etapa unui subcontract în care livrarea efectivă a materialelor și/sau a lucrărilor de către resursele subcontractate nu mai este necesară. Un subcontract în această stare nu poate fi utilizat pentru estimarea și încadrarea cerințelor proiectului pentru resurse și materiale și nici nu poate fi utilizat ca referință pentru timp, cheltuieli și utilizarea materialelor într-un proiect. Un subcontract în această stare nu poate fi editat sau șters. | Fără |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
