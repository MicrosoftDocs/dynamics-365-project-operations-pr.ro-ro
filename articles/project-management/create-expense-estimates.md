---
title: Estimări financiare pentru cheltuieli în proiecte
description: Acest subiect furnizează informații despre definirea sau estimarea cheltuielilor bazate pe proiecte.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f4d42724af61aa241671e8dacacbe2be5a7d531f55c2025a89ff777ac41e9b67
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987856"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimări financiare pentru cheltuieli în proiecte
_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations le permite managerilor de proiect să definească cheltuielile bazate pe proiect pentru fiecare proiect sau pentru o sarcină. Fiecare element de cheltuieli poate fi asociat cu o sarcină specifică a proiectului. Cheltuielile sunt clasificate în diferite categorii de cheltuieli, care sunt definite la nivel organizațional. Prețurile și costurile pentru fiecare categorie de cheltuieli sunt definite în lista de prețuri. 

Parcurgeți pașii următori pentru a vizualiza, adăuga sau șterge o cheltuială a proiectului.

1. Accesați **Proiecte**, și selectați proiectul la care doriți să lucrați.
2. Selectați fila **Estimări ale proiectului** și vizualizați lista cheltuielilor proiectului.
3. Selectați **Cheltuieli noi** pentru a adăuga o cheltuială. Sau selectați o cheltuială de șters, apoi selectați **Ștergeți cheltuiala**.

Următorul tabel oferă informații despre câmpurile de pe pagina **Linie de estimare cheltuieli** de pe un proiect. 

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Activitate | O listă a sarcinilor din proiect. Aceasta include sarcini de rezumat de nod frunză. | Selectarea unei sarcini pentru o linie estimativă de cheltuieli va avea un impact asupra costului estimat al cheltuielilor și al vânzărilor estimate ale cheltuielilor pentru o sarcină. Dacă acest câmp este lăsat necompletat, estimatul de cheltuieli este urmărit și sintetizat numai la nivel de proiect. |
| Categorie | O listă a categoriilor de tranzacții care au legate categorii de cheltuieli în aplicație. | Selectarea unei categorii determină stabilirea prețurilor și a costurilor pe linia de estimare a cheltuielilor. |
| Dată de început | Data prognozată la care va avea loc cheltuiala. | Nu există niciun impact în aval pentru acest câmp. |
| Grup de unități | Valoarea implicită din acest câmp provine din grupul de unități configurat ca implicit pentru categoria selectată. Puteți actualiza acest câmp pentru a selecta un alt grup de unități. | Nu există niciun impact în aval pentru acest câmp. |
| Unitate | Valoarea din acest câmp devine implicit unitatea implicită a categoriei selectate. Puteți actualiza acest câmp pentru a selecta o altă unitate. | Schimbarea unității are ca rezultat un preț unitar și un cost implicit diferit. |
| Cantitate | Cantitatea cheltuielii estimate pe care o veți suporta. | Nu există niciun impact în aval pentru acest câmp. |
| Cost unitar | Costul unitar al categoriei selectate și combinația de unități, așa cum este stabilit în lista de prețuri de cost aplicabilă | Costul unitar este întotdeauna afișat în moneda costului proiectului. |
| Preț unitar | Prețul produsului selectat și categoria și combinația de unități, așa cum este configurat în lista de prețuri de vânzare aplicabilă. | Prețul unitar este întotdeauna afișat în moneda de vânzare a proiectului. |
| Cost total | Valoarea costului care este calculată ca un \*cost unitar al cantității.| Valoarea costului este întotdeauna afișat în moneda costului proiectului. |
| Total vânzări | Valoarea de vânzări calculată ca un \* preț unitar al cantității. | Valoarea vânzărilor este întotdeauna afișată în moneda de vânzare a proiectului. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
