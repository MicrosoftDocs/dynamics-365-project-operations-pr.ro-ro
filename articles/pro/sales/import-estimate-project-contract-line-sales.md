---
title: Importul unei estimări într-o linie de contract bazată pe proiect - simplificat
description: Acest articol oferă informații despre importul estimărilor financiare dintr-un proiect într-o linie de contract.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d6e3bdfeb1ea9de32d6712ac5671be39c243702a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924215"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importul unei estimări într-o linie de contract bazată pe proiect - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Dynamics 365 Project Operations, puteți importa estimări dintr-un proiect pentru o linie de contract bazată pe proiect.

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