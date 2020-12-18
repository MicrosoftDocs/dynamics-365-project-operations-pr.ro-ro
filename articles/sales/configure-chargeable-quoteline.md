---
title: Configurarea componentelor tarifabile ale unei linii de ofertă pe bază de proiect
description: Acest subiect oferă informații despre componentele incluse, taxabile și neimpozabile pe liniile de ofertă bazate pe proiecte.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642558"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurarea componentelor tarifabile ale unei linii de ofertă pe bază de proiect

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

O linie de ofertă bazată pe proiecte poate include componente și componente cu taxă.

Componentele incluse sunt supuse metodei de facturare, împărțirilor clienților, limitelor care nu trebuie depășite și setărilor de frecvență a facturilor definite pe linia de ofertă bazată pe proiect.
Un subset al componentelor incluse poate fi marcat ca taxabil folosind **Tip de facturare**. Puteți selecta una dintre următoarele opțiuni în câmpul **Tip de facturare** în contextul unei linii de ofertă:

   - Taxabil
   - Netaxabil

Componentele taxabile pot fi definite pe categorii de roluri și tranzacții.

Taxabilitatea care este definită pentru roluri pentru o linie de ofertă a proiectului se aplică numai pentru clasa tranzacției **Timp**. Dacă o linie de ofertă a proiectului are **Includeți timpul** = **Nu**, fila **Roluri taxabile** nu este disponibilă.

Taxabilitatea care este definită pe categorii de tranzacții pentru o linie de ofertă a proiectului se aplică numai pentru clasa tranzacției **Cheltuială**. Dacă o linie de ofertă a proiectului are **Includeți cheltuieli** = **Nu**, fila **Categorii taxabile** nu este disponibilă.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Actualizați un rol pentru a fi taxabil sau netaxabil
Un rol poate fi taxabil sau neimpozabil pe o linie de ofertă bazată pe proiect. Tipul de facturare pentru un rol poate fi configurat pe **Roluri taxabile** fila unei linii de ofertă bazate pe proiect. Pentru a face acest lucru, actualizați **Tipul de facturare** pe subgrila **Roluri facturabile**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Actualizați o categorie de tranzacții pentru a fi taxabilă sau netaxabilă
O categorie de tranzacție poate fi facturabilă sau nefacturabilă pe o linie de ofertă bazată pe proiect. Tipul de facturare pe o tranzacție poate fi configurat pe fila **Roluri facturabile** unei linii de ofertă bazate pe proiect. Pentru a face acest lucru, actualizați câmpul **Tipul de facturare** pe subgrila **Categorii facturabile**. 

## <a name="resolve-chargeability"></a>Rezolvați taxarea

O estimare sau reală creată pentru timp va fi considerată facturabilă numai dacă timpul este inclus pe linia de ofertă și dacă rolul este configurat ca facturabil.
O estimare sau o dată reală creată pentru o cheltuială va fi considerată facturabilă doar dacă cheltuiala este inclusă pe o linie de ofertă și dacă categoria de tranzacție este configurată drept facturabilă pe linia de ofertă. Tabelul următor arată modul în care taxa de încărcare este implicită pentru fiecare dată reală. Valorile implicite se bazează pe componentele incluse și pe tipul de facturare care este configurat pe linia de ofertă.

| Include timpul | Include cheltuiala | Rol | Categorie | Activitate |
| --- | --- | --- | --- | --- |
| Da | Da | Taxabil | Taxabil | Facturare la un timp real: Taxabil </br>Tipul de facturare pentru o cheltuială reală: Taxabil |
| Da | Da | Netaxabil | Taxabil | Facturare la un timp real: Netaxabil </br>Tipul de facturare pentru o cheltuială reală: Taxabil |
| Da | Da | Netaxabil | Netaxabil | Facturare la un timp real: Netaxabil </br>Tipul de facturare pentru o cheltuială reală: Netaxabil |
| Nicio | Da | Nu se poate seta | Taxabil | Facturare la un timp real: Nu este disponibil </br>Tipul de facturare pentru o cheltuială reală: Taxabil |
| Nicio | Da | Nu se poate seta | Netaxabil | Facturare la un timp real: Nu este disponibil </br>Tipul de facturare pentru o cheltuială reală: Netaxabil |
| Da | Nicio | Taxabil | Nu se poate seta | Facturare la un timp real: Taxabil </br>Tipul de facturare pentru o cheltuială reală: Indisponibil |
| Da | Nicio | Netaxabil | Nu se poate seta | Facturare la un timp real: Netaxabil </br> Tipul de facturare pentru o cheltuială reală: Indisponibil |
