---
title: Importul unei estimări într-o linie de contract bazată pe proiect - simplificat
description: Acest subiect oferă informații despre cum să importați estimările financiare dintr-un proiect într-o linie de contract.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177481"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importul unei estimări într-o linie de contract bazată pe proiect - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Dynamics 365 Project Operations, puteți importa estimări dintr-un proiect într-o linie de contract bazată pe proiect.

1. Verificați dacă a fost compeltat câmpul **Proiect** de pe linia de contract bazată pe proiect.
2. Pe fila **Detalii linie contract**, pe subgrilă, selectați **Importați din estimarea de proiect**. Se deschide o pagină de dialog cu opțiuni de rezumare. Opțiunile de rezumare disponibile sunt, **Clasa tranzacției**, **Categorie**, **Rol**, și **Activitate de proiect**.
3. Pe baza selecției de rezumare, estimările din proiect pentru toate clasele de tranzacții și activitățile incluse pe această linie de contract sunt copiate. Pentru a verifica ce clase de tranzacții sunt incluse, pe fila **General** de pe linia de contract pe bază de proiect, verificați valorile din câmpurile **Includeți timpul**, **Includeți cheltuielile** și **Includeți taxe**. 
4. Pentru a vedea ce sarcini sunt incluse, selectați fila **Activități taxabile** de pe linia de contract. Pe baza activităților asociate care au câmpul **Clase de tranzacții incluse** setate la **Da**, toate estimările pentru acele combinații de activități și clase de tranzacții sunt importate pe linia de contract.

Când importați estimări, sistemul are prețurile implicite pe baza listelor de prețuri de proiect atașate la contract și tipul de facturare configurat pe linia de contract. Dacă o activitate, rol sau o categorie este configurată pe linia de contract drept ne-taxabilă, linia de estimări importată pentru acel rol sau categorie nu este taxabilă și nu se va adăuga la valoarea contractată a liniei de contract.

Când o linie de contract are detalii despre linie, **Valoarea de contract** și câmpurile **Taxe estimate** de pe linia de contract sunt rezumate și nu pot fi editate.

Când sunt selectate mai multe opțiuni de rezumare, sistemul încearcă să rezume prin toate opțiunile selectate. Rezultatul rezultatului are ca rezultat mai multe linii contractuale importate decât dacă selectați o singură opțiune de rezumare.

De exemplu, dacă proiectul are următoarele linii estimate pentru cheltuieli:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| Activitatea B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Activitatea C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Când utilizatorul selectează pentru a rezuma în funcție de **Clasa de Tranzacție**, următoarele informații vor fi importate:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Când utilizatorul selectează pentru a rezuma în funcție de **Clasa de Tranzacție** și **Categorie**, următoarele informații vor fi importate:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Când utilizatorul selectează să rezume de **Clasa de tranzacție**, **Categorie** și **Activitate de nod de frunză** vor fi importate următoarele. Observați că acest rezultat este același cu ce este pe proiect:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| Activitatea B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Activitatea C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]