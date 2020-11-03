---
title: Configurarea componentelor tarifabile ale unei linii de ofertă
description: Acest subiect oferă informații despre configurarea componentelor taxabile și netaxabile pe o linie de ofertă bazată pe proiect.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082917"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurarea componentelor tarifabile ale unei linii de ofertă

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O linie de ofertă bazată pe proiecte are conceptul de componente *incluse* și componente *taxabile*.

Componentele incluse sunt supuse la:

  - Metoda de facturare și împărțirea clienților
  - Limite de nedepășire 
  - Setările frecvenței facturilor definite pe linia de ofertă bazată pe proiect

Un subset al componentelor incluse poate fi marcat ca taxabil folosind câmpul **Tip de facturare**. Câmpul **Tip de facturare** este un set de opțiuni care permite următoarele valori în contextul unei linii de ofertă:

  - Taxabil
  - Netaxabil

Componentele taxabile pot fi definite pe sarcini, roluri și categorii de tranzacții.

Taxabilitatea este definită pentru sarcinile pentru linia de ofertă și se aplică tuturor claselor de tranzacții incluse pe acea linie. Dacă câmpul **Includeți activități** este setat la **Întregul proiect** sau este necompletat, fila **Sarcini taxabile** nu este disponibilă.

Taxabilitatea este definită pe roluri pentru o linie de ofertă și se aplică numai pentru clasa tranzacției **Timp**. Dacă câmpul **Includeți timpul** de pe o linie de ofertă de contract este setat la **Nu** , fila **Roluri tarifabile** nu este disponibilă.

Taxabilitatea este definită pe categorii de tranzacții pentru o linie de ofertă și se aplică numai pentru clasa tranzacției **Cheltuială**. Dacă câmpul **Includeți cheltuieli** de pe o linie de ofertă de contract este setat la **Nu** , fila **Categorii tarifabile** nu este disponibilă.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Actualizați o sarcină de proiect pentru a fi taxabilă sau netaxabilă

O sarcină de proiect poate fi taxabilă sau netaxabilă în contextul unei linii specifice de ofertă bazate pe proiect, ceea ce face posibilă următoarea configurare:

Dacă o linie de ofertă bazată pe proiect include **Timp** și sarcina **T1** , sarcina este asociată liniei de ofertă ca taxabilă. Dacă există o a doua linie de ofertă care include **Cheltuieli** , puteți asocia sarcina **T1** pe linia de ofertă ca netaxabilă. Rezultatul este că tot timpul înregistrat în sarcină este taxabil și toate cheltuielile înregistrate în sarcină sunt netaxabile.

Tipul de facturare al unei sarcini poate fi configurat pe fila **Sarcini taxabile** a unei linii de ofertă bazată pe proiect prin actualizarea câmpului **Tipul de facturare** în subgrila **Linia de ofertă proiect**. Alternativ, puteți actualiza tipul de facturare pentru o activitate de proiect în câmpul **Tipul de facturare** din sub-grila sarcinii de configurare a facturării a unui proiect care arată liniile de ofertă asociate unei sarcini.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizați un rol pentru a fi taxabil sau netaxabil

Un rol poate fi taxabil sau netaxabil în contextul unei linii specifice de ofertă pe bază de proiect.

Tipul de facturare al unui rol poate fi configurat pe fila **Roluri taxabile** a unei linii de ofertă bazată pe proiect prin actualizarea câmpului **Tipul de facturare** în subgrila **Roluri tarifabile**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizați o categorie de tranzacții pentru a fi taxabilă sau netaxabilă

O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie de ofertă.

Tipul de facturare al unei tranzacții poate fi configurat pe fila **Categorii tarifabile** a unei linii de ofertă bazată pe proiect prin actualizarea câmpului **Tipul de facturare** în subgrila **Categorii tarifabile**.

### <a name="resolve-chargeability"></a>Rezolvați taxarea
O estimare sau una reală creată pentru timp va fi considerată taxabilă dacă **Timp** este inclus pe linia de ofertă și dacă **Sarcina** și **Rol** sunt configurate ca taxabile pe linia de ofertă.

O estimare sau una reală creată pentru cheltuială va fi considerată taxabilă dacă **Cheltuiala** este inclusă pe linia de ofertă și dacă categoriile **Sarcina** și **Categorie tranzacție** sunt configurate ca taxabile pe linia de ofertă.

| Include timpul | Include cheltuielile | Activități incluse | Rol | Categorie | Activitate | Facturare |
| --- | --- | --- | --- | --- | --- | --- |
| Da | Da | Întregul proiect | Taxabil | Taxabil | Nu se poate seta | Facturare la un timp real: Taxabil </br>Tipul de facturare pentru cheltuieli reale: Taxabil |
| Da | Da | Numai activități selectate | Taxabil | Taxabil | Taxabil | Facturare la un timp real: Taxabil</br>Tipul de facturare pentru cheltuieli reale: Taxabil |
| Da | Da | Numai activități selectate | Netaxabil | Taxabil | Taxabil | Facturare la un timp real: Netaxabil</br>Tipul de facturare pentru cheltuieli reale: Taxabil |
| Da | Da | Numai activități selectate | Taxabil | Taxabil | Netaxabil | Facturare la un timp real: Netaxabil</br> Tipul de facturare pentru cheltuieli reale: Netaxabil |
| Da | Da | Numai activități selectate | Netaxabil | Taxabil | Netaxabil | Facturare la un timp real: Netaxabil</br> Tipul de facturare pentru cheltuieli reale: Netaxabil |
| Da | Da | Numai activități selectate | Netaxabil | Netaxabil | Taxabil | Facturare la un timp real: Netaxabil</br> Tipul de facturare pentru cheltuieli reale: Netaxabil |
| Nicio | Da | Întregul proiect | Nu se poate seta | Taxabil | Nu se poate seta | Facturare la un timp real: Nu este disponibil </br>Tipul de facturare pentru cheltuieli reale: Taxabil |
| Nicio | Da | Întregul proiect | Nu se poate seta | Netaxabil | Nu se poate seta | Facturare la un timp real: Nu este disponibil </br>Tipul de facturare pentru cheltuieli reale: Netaxabil |
| Da | Nicio | Întregul proiect | Taxabil | Nu se poate seta | Nu se poate seta | Facturare la un timp real: Taxabil</br>Tipul de facturare pentru cheltuieli reale: Indisponibil |
| Da | Nicio | Întregul proiect | Netaxabil | Nu se poate seta | Nu se poate seta | Facturare la un timp real: Netaxabil </br>Tipul de facturare pentru cheltuieli reale: Indisponibil |
