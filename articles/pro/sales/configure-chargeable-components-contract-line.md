---
title: Configurarea componentelor taxabile ale unei linii de contract bazate pe proiect
description: Acest subiect oferă informații despre cum să adăugați componente taxabile la liniile contractuale în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082703"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Configurarea componentelor taxabile ale unei linii de contract bazate pe proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

O linie de contract bazată pe proiecte are componente *incluse* și componente *taxabile*.

Componentele incluse sunt componente care fac obiectul:

  - Metoda de facturare și împărțirea clienților
  - Limite de nedepășire 
  - Setările frecvenței facturilor definite pe linia de contract bazată pe proiect

Un subset al componentelor incluse poate fi marcat ca taxabil folosind câmpul **Tip de facturare**. Câmpul **Tip de facturare** este un set de opțiuni care permite următoarele valori în contextul unei linii contractuale:

  - Taxabil
  - Netaxabil

Componentele taxabile pot fi definite pe sarcini, roluri și categorii de tranzacții.

Taxabilitatea este definită pentru sarcinile pentru o linie de contract de proiect și se aplică tuturor claselor de tranzacții incluse pe linie. Dacă câmpul **Includeți activități** de pe o linie de contract este necompletat sau setat la **Întregul proiect** , fila **Sarcini taxabile** nu va fi disponibilă.

Taxabilitatea definită pe roluri pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Timp**. Dacă câmpul **Includeți timpul** de pe o linie de contract este setat la **Nu** , fila **Roluri tarifabile** nu va fi disponibilă.

Taxabilitatea definită pe categorii de tranzacții pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Cheltuială**. Dacă câmpul **Includeți cheltuielile** este setat la **Nu** , fila **Categorii tarifabile** nu va fi disponibilă.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Actualizați o sarcină de proiect ca fiind taxabilă sau netaxabilă

O sarcină de proiect poate fi taxabilă sau netaxabilă pe o anumită linie contractuală, ceea ce face posibilă următoarea configurare:

Dacă o linie de contract bazată pe proiect include **Timp** și o anumită sarcină, **T1** este asociat acesteia ca taxabil. Dacă există o a doua linie de contract care include **Cheltuieli** , puteți asocia sarcina T1 pe linia contractului ca netaxabilă. Rezultatul este că tot timpul înregistrat în sarcină este taxabil și toate cheltuielile sunt netaxabile.

Tipul de facturare al unei sarcini poate fi configurat pe fila **Sarcini taxabile** a liniei contractului prin actualizarea câmpului **Tipul de facturare** în subgrila sarcinilor liniei de contract. Alternativ, puteți actualiza câmpul **Tipul de facturare** din sub-grila sarcinii Configurarea facturării a unui proiect care arată liniile contractuale asociate unei sarcini.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Actualizați un rol ca fiind taxabil sau netaxabil

Un rol poate fi taxabil sau netaxabil pe o anumită linie contractuală.

Tipul de facturare al unui rol poate fi configurat pe fila **Roluri tarifabile** al unei linii contractuale. Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe sub-grila **Roluri tarifabile**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Actualizați o categorie de tranzacții ca fiind taxabilă sau netaxabilă

O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie contractuală.

Tipul de facturare al unei tranzacții poate fi configurat pe fila **Categorii tarifabile** a unei linii de contract bazate pe proiect. Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe sub-grila **Categorii tarifabile**.

### <a name="resolve-chargeability"></a>Rezolvați taxarea

O estimare sau una reală creată pentru timp va fi considerată taxabilă dacă **Timp** este inclus pe linia contractului și dacă **Sarcina** și **Rol** sunt configurate ca taxabile pe linia contractului.

O estimare sau una reală creată pentru cheltuială este considerată taxabilă dacă **Cheltuiala** este inclusă pe linia contractului și dacă categoriile **Sarcina** și **Tranzacție** sunt configurate ca taxabile pe linia contractului.


| Include timpul | Include cheltuielile | Include activități | Rol           | Categorie       | Activitate                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Da           | Da              | Întregul proiect | Taxabil     | Taxabil     | Facturare la un timp real: **Taxabil** </br> Tipul de facturare pentru cheltuieli reale: **Taxabil**           |
| Da           | Da              | Activități selectate | Taxabil     | Taxabil     | Facturare la un timp real: **Taxabil** </br> Tipul de facturare pentru cheltuieli reale: **Taxabil**           |
| Da           | Da              | Activități selectate | Netaxabil | Taxabil     | Facturare la un timp real: **Netaxabil** </br> Tipul de facturare pentru cheltuieli reale: **Taxabil**       |
| Da           | Da              | Activități selectate | Taxabil     | Taxabil     | Facturare la un timp real: **Netaxabil** </br> Tipul de facturare pentru cheltuieli reale: **Netaxabil** |
| Da           | Da              | Activități selectate | Netaxabil | Taxabil     | Facturare la un timp real: **Netaxabil** </br> Tipul de facturare pentru cheltuieli reale: **Netaxabil** |
| Da           | Da              | Activități selectate | Netaxabil | Netaxabil | Facturare la un timp real: **Netaxabil** </br> Tipul de facturare pentru cheltuieli reale: **Netaxabil** |
| Nicio            | Da              | Întregul proiect | Nu se poate seta   | Taxabil     | Facturare la un timp real: **Nu este disponibil**</br>Tipul de facturare pentru cheltuieli reale: **Taxabil**          |
| Nicio            | Da              | Întregul proiect | Nu se poate seta   | Netaxabil | Facturare la un timp real: **Nu este disponibil**</br> Tipul de facturare pentru cheltuieli reale: **Netaxabil**     |
| Da           | Nicio               | Întregul proiect | Taxabil     | Nu se poate seta   | Facturare la un timp real: **Taxabil** </br> Tipul de facturare pentru cheltuieli reale: **Indisponibil**        |
| Da           | Nicio               | Întregul proiect | Netaxabil | Nu se poate seta   | Facturare la un timp real: **Netaxabil** </br>Tipul de facturare pentru cheltuieli reale: **Indisponibil**   |
