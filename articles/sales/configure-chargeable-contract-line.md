---
title: Configurarea componentelor tarifabile ale unei linii de contract bazate pe proiect
description: Acest subiect oferă informații despre componentele incluse, taxabile și netaxabile pe linii de contract.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128711"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurarea componentelor tarifabile ale unei linii de contract bazate pe proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

O linie de contract bazată pe proiecte are conceptul de componente incluse, taxabile și netaxabile.

Componentele incluse sunt supuse metodei de facturare, împărțirii clienților, limitelor care nu trebuie depășite și setărilor de frecvență a facturilor definite pe linia de contract pe bază de proiect.

Un subset al componentelor incluse poate fi marcat ca taxabil actualizând câmpul **Tip de facturare**.

Componentele taxabile pot fi definite pe roluri și categorii de tranzacții.

Pentru o linie de contract de proiect, taxabilitatea definită pentru un rol se aplică numai pentru clasa tranzacției **Timp**. Dacă **Includeți timpul** de pe o linie de contract este setat la **Nu**, fila **Roluri tarifabile** nu este disponibilă.

Taxabilitatea definită pe categorii de tranzacții pentru o linie de contract de proiect se aplică numai pentru clasa tranzacției **Cheltuială**. Dacă **Includeți cheltuieli** de pe o linie de contract este setat la **Nu**, fila **Categorii tarifabile** nu este disponibilă.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizați un rol pentru a fi taxabil sau netaxabil

Un rol poate fi taxabil sau netaxabil pe o anumită linie de contract bazată pe proiect.

Pe fila **Roluri tarifabile** unei linii contractuale bazate pe proiecte, pe subgrila **Categorii tarifabile**, în **Tipul de facturare**, actualizați tipul de facturare pentru un rol.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizați o categorie de tranzacții pentru a fi taxabilă sau netaxabilă

O categorie de tranzacție poate fi taxabilă sau netaxabilă pe o anumită linie de contract bazată pe proiect.

Pe fila **Categorii tarifabile** a unei linii contractuale bazate pe proiect, pe subgrila **Categorii tarifabile**, în **Tipul de facturare**, actualizați tipul de facturare pentru un rol.

### <a name="resolve-chargeability"></a>Rezolvați taxarea

O estimare sau una reală creată pentru timp va fi considerată taxabilă dacă Timp este inclus pe linia contractului și dacă Rol este configurat ca taxabil pe linia contractului.

O estimare sau una reală creată pentru cheltuială va fi considerată taxabilă dacă Cheltuiala este inclusă pe linia contractului și dacă categoria Tranzacție este configurată ca taxabilă pe linia contractului.

| Include timpul | Include cheltuiala | Rol | Categorie | Activitate |
| --- | --- | --- | --- | --- |
| Da | Da | Taxabil | Taxabil | Facturare la un timp real: Taxabil </br>Tipul de facturare pentru o cheltuială reală: Taxabil |
| Da | Da | Netaxabil | Taxabil | Facturare la un timp real: Netaxabil </br>Tipul de facturare pentru o cheltuială reală: Taxabil |
| Da | Da | Netaxabil | Netaxabil | Facturare la un timp real: Netaxabil </br>Tipul de facturare pentru o cheltuială reală: Netaxabil |
| Nicio | Da | Nu se poate seta | Taxabil | Facturare la un timp real: Nu este disponibil </br>Tipul de facturare pentru o cheltuială reală: Taxabil |
| Nicio | Da | Nu se poate seta | Netaxabil | Facturare la un timp real: Nu este disponibil </br>Tipul de facturare pentru o cheltuială reală: Netaxabil |
| Da | Nicio | Taxabil | Nu se poate seta | Facturare la un timp real: Taxabil </br>Tipul de facturare pentru o cheltuială reală: Indisponibil |
| Da | Nicio | Netaxabil | Nu se poate seta | Facturare la un timp real: Netaxabil </br> Tipul de facturare pentru o cheltuială reală: Indisponibil |


[!INCLUDE[footer-include](../includes/footer-banner.md)]