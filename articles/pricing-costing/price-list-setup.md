---
title: Configurarea listelor de prețuri
description: Acest subiect oferă informații despre cum să configurați listele de de prețuri de cost și vânzare.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 34ee7bb157426507ec7ca8c031f5cb552e85099b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275508"
---
# <a name="set-up-price-lists"></a>Configurarea listelor de prețuri

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Listele de prețuri din Dynamics 365 Project Operations reprezintă un catalog de tarife. Tarifele exprimă costurile, vânzările și ratele facturilor. În funcție de faptul dacă lista de prețuri exprimă rate de cost sau de vânzări și facturi, contextul listei de prețuri este **Vânzări** sau **Cost**.

Următoarele extensii sunt specifice Project Operations și sunt aplicate listelor de prețuri din Dynamics 365 Sales.

- **Context**: Acest câmp are valorile acceptate, **Cost** și **Vânzări**. Valoarea, **Achiziție** nu este acceptată. Setați contextul la **Cost** pentru a face o listă de prețuri de cost sau pentru a seta contextul la **Vânzări** pentru o listă de prețuri de vânzare. Listele de prețuri de cost rezolvă prețul pentru tipul de cost din înregistrările estimative și reale. Listele de prețuri de vânzare rezolvă prețul înregistrărilor estimate și reale ale tipurilor de vânzări nefacturate și facturate.
- **Unitatea de timp**: Aceasta este unitatea de timp implicită pentru care prețul este stabilit în respectivul tabel **Preț de rol** pentru această listă de prețuri.
- **Entitate listă prețuri**: Acest câmp ascuns este de către Project Operations pentru a diferenția listele de prețuri care sunt specifice ofertelor sau contractului de cele care sunt standard și aplicabile la nivel global.

## <a name="price-list-header"></a>Antet listă de prețuri

Următorul tabel include câmpurile de pe fila **General** a unei liste de prețuri care sunt unice pentru operațiunile de proiect sau care au modificări semnificative în comportament din listele de prețuri din vânzări.

| Câmp | Locație | Descriere | Impactul din aval |
| --- | --- | --- | --- |
| Nume | Fila **General** și formulare **Creare rapidă** | Identitatea listei de prețuri. | Lista de prețuri este afișată cu această valoare pe toate listele de pagini și opțiuni verticale.|
| Context | Fila **General** și formulare **Creare rapidă** | Acest câmp poate fi setat la **Cost** sau **Vânzări**. | O listă de prețuri setată la **Cost** este utilizată pentru a căuta prețul pentru estimări ale costurilor și costuri reale. O listă de prețuri setată la **Vânzări** este utilizată pentru a căuta prețul pentru vânzări ale costurilor și datelor reale de vânzări. Numai listele de prețuri care au contextul setat la **Vânzări** pot fi atașate la o listă de prețuri pentru clienți, oferte de proiecte și contracte de proiecte. |
| Data de început | Fila **General** și formulare **Creare rapidă** | Data de începere a perioadei în care lista de prețuri este efectivă. | Cu câmpul **Data de sfârșit**, acest câmp este utilizat pentru a determina care listă de prețuri este aplicabilă pentru o anumită estimare sau linie reală. |
| Data de sfârșit | Fila **General** și formulare **Creare rapidă** | Data de sfârșit a perioadei în care lista de prețuri este efectivă. | Cu câmpul **Data de început**, acest câmp este utilizat pentru a determina care listă de prețuri este aplicabilă pentru o anumită estimare sau linie reală. |
| Monedă | Fila **General** și formulare **Creare rapidă** | Acest câmp este utilizat pentru a seta moneda implicită pentru fiecare rol, categorie sau linie de articole din lista de prețuri aferentă acestei liste de prețuri. | Pe listele de prețuri **Vânzări**, rolurile, categoriile sau liniile de articole din lista de prețuri nu pot fi create în altă monedă decât această monedă. Pe listele de prețuri de **Cost**, puteți crea o linie de preț rol în orice monedă. Moneda definită aici este utilizată ca implicită. Configurarea utilizatorului care are legătură cu prețurile de rol poate anula această valoare pentru a permite configurarea ratei costului forței de muncă în orice monedă. Tarifele de cost ale categoriilor și costurile articolelor din lista de prețuri pot fi setate numai în moneda definită aici. |
| Unitate de timp | Fila **General** și formulare **Creare rapidă** | Acest câmp este utilizat pentru a seta unitatea de timp implicită pentru fiecare rol, aferentă acestei liste de prețuri. | Această valoare a câmpului este utilizată numai la configurarea prețului rolului asociat. Pe listele de prețuri **Cost** și **Vânzări**, puteți crea o linie de preț de rol în orice unitate de timp. Unitatea de timp definită aici este utilizată ca implicită. Configurarea utilizatorului care are legătură cu prețurile de rol poate anula această valoare pentru a permite configurarea ratei de facturare în orice unitate de timp. |
| Descriere | Fila **General** și formulare **Creare rapidă** | Acesta este un câmp text și vă permite să furnizați o descriere pe mai multe linii a listei de prețuri. | Acest câmp este afișat în vizualizări **Asociate** pe lista de prețuri din diferite entități care au liste de prețuri conexe. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]