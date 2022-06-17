---
title: Estimări financiare pentru materiale în proiecte
description: Acest articol oferă informații despre definirea sau estimarea materialelor bazate pe proiecte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925723"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimări financiare pentru materiale în proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Dynamics 365 Project Operations le permite managerilor de proiect să definească costurile materiale bazate pe proiect pentru fiecare proiect sau sarcină. Fiecare estimare de material poate fi asociată cu o sarcină specifică a proiectului. Materialele care sunt folosite în proiecte pot fi produse înscrise sau produse din catalogul de produse. Pentru fiecare combinație de produs și unitate, un preț poate fi definit în listele de prețuri ale proiectului pentru vânzări și listele de prețuri ale proiectului pentru cost.  

Parcurgeți pașii următori pentru a vizualiza, adăuga sau șterge o estimare a materialului proiectului.

1. Accesați **Proiecte** și selectați proiectul pe care doriți să îl actualizați.
2. Pe fila **Estimări materiale**, vizualizați lista estimărilor materialelor proiectului.
3. Selectați **Nouă estimare de material** pentru a crea o nouă estimare de material. Sau selectați o estimare de material pe care să o ștergeți, apoi selectați **Ștergere estimare de material**.

Următorul tabel oferă informații despre câmpurile de pe pagina **Linie de estimare material** de pe un proiect. 

| **Câmp** | **Descriere** | **Impactul din aval** |
| --- | --- | --- |
| Activitate | O listă a sarcinilor din proiect. Aceasta include sarcini de rezumat de nod frunză. | Când selectați o sarcină pentru o linie de estimare de material, sunt afectate costul estimat al materialului și vânzările de materiale estimate pentru o sarcină. Dacă acest câmp este gol, estimatul de material este urmărit și sintetizat numai la nivel de proiect. |
| Selectare produs |  Puteți specifica dacă linia estimativă este pentru un produs existent (de catalog) sau un produs din afara catalogului. | Acest câmp determină dacă selectați un produs din catalog sau un produs din afara catalogului. |
| Produs | ID-ul produsului din catalogul de produse. Când selectați un ID de produs, valoarea din câmpul **Selectare Produs** se actualizează automat la **Produs existent**. ID-ul este utilizat pentru a prelua prețurile de cost și de vânzare din lista de prețuri. | Nu există niciun impact din aval pentru acest domeniu. |
| Descriere produs din afara catalogului | Un câmp text pentru a introduce numele produsului. Acest câmp trebuie utilizat atunci când este selectat **Din afara catalogului** în câmpul **Selectare Produs**.| Nu există niciun impact din aval pentru acest domeniu. |
| Data de început | Data estimată la care se așteaptă utilizarea materialului. | Nu există niciun impact din aval pentru acest domeniu. |
| Grup de unități | Valoarea implicită din acest câmp provine din grupul de unități implicit pentru produsul din catalog. Puteți actualiza acest câmp pentru a selecta un alt grup de unități. | Nu există niciun impact din aval pentru acest domeniu. |
| Unitate | Valoarea din acest câmp provine din unitatea implicită a produsului selectat. Puteți actualiza acest câmp pentru a selecta o altă unitate. | Schimbarea unității are ca rezultat un preț unitar și un cost implicit diferit. |
| Cantitate | Cantitatea estimată a produsului care va fi utilizată în proiect. | Nu există niciun impact din aval pentru acest domeniu. |
| Cost unitar | Costul unitar al produsului selectat și combinația de unități, așa cum este stabilit în lista de prețuri de cost aplicabilă. | Costul unitar este întotdeauna afișat în moneda costului proiectului. Dacă nu există o configurare de cost unitar pentru combinația de produs și configurare de unitate în lista de prețuri, costul unitar va fi implicit 0,00. |
| Preț unitar | Prețul produsului selectat și combinația de unități, așa cum este stabilit în lista de prețuri de vânzare aplicabilă. | Prețul unitar este întotdeauna afișat în moneda de vânzare a proiectului. Dacă nu există o configurare de cost unitar pentru combinația de produs și configurare de unitate în lista de prețuri, prețul unitar va fi implicit 0,00.|
| Cost total | Valoarea costului care este calculată ca un \*cost unitar al cantității.| Valoarea costului este întotdeauna afișat în moneda costului proiectului. |
| Total vânzări | Valoarea de vânzări calculată ca un \* preț unitar al cantității. | Valoarea vânzărilor este întotdeauna afișată în moneda de vânzare a proiectului. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
