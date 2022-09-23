---
title: Postarea rapoartelor de cheltuieli
description: Acest articol explică cum să postezi rapoarte de cheltuieli.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524885"
---
# <a name="post-expense-reports"></a>Postarea rapoartelor de cheltuieli

După ce un raport de cheltuieli a fost aprobat și transferat în jurnalul general, acesta poate fi postat. Când postați un raport de cheltuieli, sunt identificate cheltuielile care sunt eligibile pentru recuperarea taxei pe valoarea adăugată (TVA). Sarcina de verificare și recuperare a plăților TVA este atribuită angajatului care este responsabil de verificarea raportului de cheltuieli.

În cazul în care cheltuielile aferente unui raport de cheltuieli sunt imputate unei alte companii decât compania care angajează angajatul, trebuie să verificați atât compania dacă aceste cheltuieli sunt datorate, cât și compania de la care sunt datorate. De exemplu, angajatul care a depus un raport de cheltuieli lucrează pentru compania DAT, dar a perceput o cheltuială companiei DIR. În acest caz, DAT este compania căreia i se datorează cheltuiala, iar DIR este compania de la care este datorată cheltuiala. După ce verificați aceste linii de jurnal, puteți posta liniile de cheltuieli în registrul general.

Pentru a publicare un raport de cheltuieli, pe pagina **Rapoarte de cheltuieli aprobate**, selectați raportul de cheltuieli, apoi, în panoul de acțiuni, selectați **Publicare**.

De asemenea, puteți publica toate rapoartele de cheltuieli în listă în același timp. Selectați toate rapoartele de cheltuieli, apoi selectați **Publicare**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Activați funcția Abilitatea de a încărca obligația de cheltuieli în moneda furnizorului pentru metoda de plată în numerar

The **Posibilitatea de a înregistra datoria de cheltuieli în moneda vânzătorului pentru metoda de plată în numerar** caracteristica permite ca rapoartele de cheltuieli să fie postate într-o monedă a furnizorului pentru metoda de plată în numerar.

În prezent, atunci când trimiteți cheltuieli de numerar, rapoartele de cheltuieli sunt înregistrate în moneda contabilă. Din cauza conversiei sumei între moneda tranzacției, moneda contabilă și moneda furnizorului, o sumă incorectă este plătită furnizorilor dacă data tranzacției a cheltuielii și data reală a plății au cursuri de schimb diferite.

Această caracteristică va asigura că soldul furnizorului este înregistrat în moneda furnizorului atunci când raportul de cheltuieli este publicat.

1. Accesați **Spații de lucru** \> **Gestionare caracteristică**.
2. În listă, găsiți și selectați **Posibilitatea de a înregistra datoria de cheltuieli în moneda vânzătorului pentru metoda de plată în numerar**, apoi selectați **Activați acum**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
