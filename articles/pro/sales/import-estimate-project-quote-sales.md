---
title: Importarea estimărilor pentru un proiect pentru o linie de ofertă pe bază de proiect
description: Acest subiect oferă informații despre cum să importați estimările dintr-un proiect într-o linie de ofertă.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 224c2265cfcc38dfc2ed74664d38c095feefaca7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082698"
---
# <a name="importing-estimates-for-a-project-to-a-project-based-quote-line"></a>Importarea estimărilor pentru un proiect pentru o linie de ofertă pe bază de proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Dacă un proiect este creat în etapa de pre-vânzare, puteți alege să importați estimarea financiară din proiect în linia de ofertă bazată pe proiect.

1. Asigurați-vă că linia de ofertă bazată pe proiect are informațiile despre proiect în câmpul **Proiect**.
2. Pe fila **Detalii linie de ofertă** , selectați **Importați din estimarea de proiect**.
3. Când se deschide pagina casetei de dialog, selectați una dintre următoarele opțiuni de rezumat.

  - **Clasă de tranzacții**
  - **Categorie**
  - **Rol** 
  - **Activitate de proiect**

Pe baza selecției dvs., estimarea din proiect pentru toate clasele de tranzacții incluse pe această linie de ofertă este copiată. Pentru a verifica ce clase de tranzacții sunt incluse, selectați fila **General** de pe linia de ofertă bazată pe proiect și verificați valorile pentru **Includeți timpul** , **Includeți cheltuielile** și **Includeți taxe**.  Pentru a verifica ce sarcini sunt incluse, selectați fila **Activități taxabile** de pe linia de ofertă.

În funcție de activitățile asociate și clasele de tranzacții incluse, estimările pentru acele combinații de activități și clase de tranzacții sunt importate pe linia de ofertă.

Când importați estimări, sistemul va stabili implicit prețurile pe baza listelor de prețuri ale proiectului atașate la ofertă și a tipului de facturare configurat pe linia de ofertă bazată pe proiect. Dacă o activitate, un rol sau o categorie este configurat pe linia de ofertă bazată pe proiect ca neimpozabilă, linia estimată importată va fi imputabilă și nu se va adăuga la valoarea citată a liniei de ofertă.

Când o linie de ofertă are detalii despre linie, **Valoarea ofertei** și câmpurile **Taxe estimate** de pe linia de ofertă sunt rezumate și nu pot fi editate.

Când sunt selectate mai multe opțiuni de rezumare, sistemul încearcă să rezume prin toate opțiunile selectate. Rezultatul este că ieșirea liniilor de ofertă importate va fi mai mare decât dacă ați selectat o singură opțiune de rezumare.

De exemplu, dacă proiectul ar avea următoarele linii estimate pentru cheltuieli.

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| Activitatea B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Activitatea C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Când utilizatorul selectează pentru a rezuma în funcție de clasa Tranzacție, următoarele informații vor fi importate.

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

Când utilizatorul selectează pentru a rezuma în funcție de clasa de tranzacție și categorie, următoarele informații vor fi importate.

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Când utilizatorul selectează pentru a rezuma în funcție de clasa de tranzacție, categorie și activitatea nod frunză următoarele informații vor fi importate. Observați că acest rezultat este același cu cel din proiect.

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| Activitatea B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Activitatea C | Hotel | 11/1/2020 | 2 | 200 | 400 |