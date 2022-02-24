---
title: Estimări financiare pentru materiale în proiecte
description: Acest subiect oferă informații despre definirea sau estimarea materialelor bazate pe proiecte.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788887"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimări financiare pentru materiale în proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations le permite managerilor de proiect să definească costurile materiale bazate pe proiect pentru fiecare proiect sau sarcină. Fiecare estimare de material poate fi asociată cu o sarcină specifică a proiectului. Cheltuielile sunt clasificate în diferite categorii de cheltuieli, care sunt definite la nivel organizațional. Prețurile și costurile pentru fiecare categorie de cheltuieli sunt definite în lista de prețuri. 

Parcurgeți pașii următori pentru a vizualiza, adăuga sau șterge o estimare a materialului proiectului.

1. Accesați **Proiecte** și selectați proiectul pe care doriți să îl actualizați.
2. Pe fila **Estimări materiale**, vizualizați lista estimărilor materialelor proiectului.
3. Selectați **Nouă estimare de material** pentru a crea o nouă estimare de material. Sau selectați o estimare de material pe care să o ștergeți, apoi selectați **Ștergere estimare de material**.

Următorul tabel oferă informații despre câmpurile de pe pagina **Linie de estimare material** de pe un proiect. 

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Activitate | O listă a sarcinilor din proiect. Aceasta include sarcini de rezumat de nod frunză. | Când selectați o sarcină pentru o linie de estimare de material, sunt afectate costul estimat al materialului și vânzările de materiale estimate pentru o sarcină. Dacă acest câmp este gol, estimatul de material este urmărit și sintetizat numai la nivel de proiect. |
| Selectare produs |  Puteți specifica dacă linia estimativă este pentru un produs existent (de catalog) sau un produs din afara catalogului. | Acest câmp determină dacă selectați un produs din catalog sau un produs din afara catalogului. |
| Produs | ID-ul produsului din catalogul de produse. Când selectați un ID de produs, valoarea din câmpul **Selectare Produs** se actualizează automat la **Produs existent**. ID-ul este utilizat pentru a prelua prețurile de cost și de vânzare din lista de prețuri. | Nu există niciun impact în aval pentru acest câmp. |
| Descriere produs din afara catalogului | Un câmp text pentru a introduce numele produsului. Acest câmp trebuie utilizat atunci când este selectat **Din afara catalogului** în câmpul **Selectare Produs**.| Nu există niciun impact în aval pentru acest câmp. |
| Dată de început | Data estimată la care se așteaptă utilizarea materialului. | Nu există niciun impact în aval pentru acest câmp. |
| Grup de unități | Valoarea implicită din acest câmp provine din grupul de unități implicit pentru produsul din catalog. Puteți actualiza acest câmp pentru a selecta un alt grup de unități. | Nu există niciun impact în aval pentru acest câmp. |
| Unitate | Valoarea din acest câmp provine din unitatea implicită a produsului selectat. Puteți actualiza acest câmp pentru a selecta o altă unitate. | Schimbarea unității are ca rezultat un preț unitar și un cost implicit diferit. |
| Cantitate | Cantitatea estimată a produsului care va fi utilizată în proiect. | Nu există niciun impact în aval pentru acest câmp. |
| Cost unitar | Costul unitar al produsului selectat și combinația de unități, așa cum este stabilit în lista de prețuri de cost aplicabilă. | Costul unitar este întotdeauna afișat în moneda costului proiectului. Dacă nu există o configurare de cost unitar pentru combinația de produs și configurare de unitate în lista de prețuri, costul unitar va fi implicit 0,00. |
| Preț unitar | Prețul produsului selectat și combinația de unități, așa cum este stabilit în lista de prețuri de vânzare aplicabilă. | Prețul unitar este întotdeauna afișat în moneda de vânzare a proiectului. Dacă nu există o configurare de cost unitar pentru combinația de produs și configurare de unitate în lista de prețuri, prețul unitar va fi implicit 0,00.|
| Cost total | Valoarea costului care este calculată ca un \*cost unitar al cantității.| Valoarea costului este întotdeauna afișat în moneda costului proiectului. |
| Total vânzări | Valoarea de vânzări calculată ca un \* preț unitar al cantității. | Valoarea vânzărilor este întotdeauna afișată în moneda de vânzare a proiectului. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
