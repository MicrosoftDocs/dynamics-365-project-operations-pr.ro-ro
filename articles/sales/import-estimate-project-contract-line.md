---
title: Importul unei estimări într-o linie de contract bazată pe proiect
description: Acest subiect oferă informații despre cum să importați estimările dintr-un proiect într-o linie de contract.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea513ca8126eadbf563f3c6cb3e966f81703ae805d12881f865cdc1dd77e191d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990106"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importul unei estimări într-o linie de contract bazată pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

În Dynamics 365 Project Operations, puteți importa estimări dintr-un proiect pentru o linie de contract bazată pe proiect.

1. Verificați dacă este completat câmpul **Proiect** de pe linia de contract bazată pe proiect.
2. Pe fila **Detalii linie contract**, pe subgrilă, selectați **Importați din estimarea de proiect**. Se deschide o pagină de dialog cu opțiuni de rezumare. Opțiunile de rezumare disponibile sunt, **Clasa tranzacției**, **Categorie**, **Rol**, și **Activitatea de proiect**. Pe baza selecțiilor pentru rezumare, estimările din proiect pentru toate clasele de tranzacții incluse pe această linie de contract sunt copiate. 
3. Pentru a verifica ce clase de tranzacții sunt incluse, pe fila **General** de pe linia de contract, verificați valorile din câmpurile **Includeți timpul**, **Includeți cheltuielile** și **Includeți taxe**.

Când importați estimări, aplicația are prețurile implicite pe baza listelor de prețuri de proiect atașate la contract și tipul de facturare configurat pe linia de contract. Dacă un rol sau o categorie este configurată pe linia de contract drept ne-taxabilă, linia de estimări importată pentru acel rol sau categorie nu este taxabilă și nu se va adăuga la valoarea contractată a liniei de contract.

Când o linie de contract are detalii despre linie, **Valoarea de contract** și câmpurile **Taxe estimate** de pe linia de contract sunt rezumate și nu pot fi editate.

Când sunt selectate mai multe opțiuni de rezumare, sistemul încearcă să rezume prin toate opțiunile selectate. Rezultatul rezultatului are ca rezultat mai multe linii contractuale importate decât dacă selectați o singură opțiune de rezumare.

De exemplu, dacă proiectul ar avea următoarele linii estimate pentru cheltuieli:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| Activitatea B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Activitatea C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Când utilizatorul selectează pentru a rezuma în funcție de **Clasa de Tranzacție**, următoarele informații vor fi importate:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Când utilizatorul selectează pentru a rezuma în funcție de **Clasa de Tranzacție** și **Categorie**, următoarele informații vor fi importate:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Când utilizatorul selectează să rezume de **Clasa de tranzacții**, **Categorie** și **Activitate de nod de frunză** vor fi importate următoarele. Observați că acest rezultat este același cu cel din proiect:

| Activitate | Categorie | Data | Cantitate | Preț unitar | Sumă |
| --- | --- | --- | --- | --- | --- |
| Activitatea A | Biletele de avion | 10/1/2020 | 4 | 400 | 1600 |
| Activitatea B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Activitatea C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]