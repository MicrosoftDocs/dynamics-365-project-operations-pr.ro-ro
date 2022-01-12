---
title: Eroare de nepotrivire a monedei
description: Acest subiect oferă informații de depanare despre o eroare de nepotrivire valutară care apare atunci când salvați anumite tipuri de înregistrări.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903751"
---
# <a name="currency-mismatch-error"></a>Eroare de nepotrivire a monedei 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Când salvați un proiect, un contract, o ofertă sau o resursă rezervabilă, este posibil să primiți eroarea, **Moneda companiei care deține nu se potrivește cu moneda unității contractante. Alegeți altă companie proprietară sau unitate contractantă pentru a continua**. Acest lucru se datorează faptului că există o nepotrivire valutară între moneda unității contractante pentru înregistrare și moneda companiei proprietare.


## <a name="resolution"></a>Rezolvare

Pentru a rezolva această problemă, procedați în felul următor:
- Verificați moneda unității contractante pentru această înregistrare. Puteți vedea moneda deschizând înregistrarea unității organizaționale și verificând valoarea de pe **General** fila în **Valută** camp.
- Verificați moneda companiei proprietare. Puteți vedea moneda accesând **Legate de** > **Registre mari** în evidența companiei. Faceți dublu clic pe înregistrarea contabilă care este asociată cu compania și verificați valoarea de pe **General** fila în **Moneda contabilă** camp.

Dacă moneda stabilită în unitatea contractantă și înregistrarea contabilă nu se potrivesc, ajustați configurația sau selectați valori diferite când salvați înregistrarea. Sistemul solicită ca aceste înregistrări să se potrivească pentru a asigura fluxurile corecte de facturare între companii. Pentru mai multe informații despre configurațiile intercompanii, consultați [Creați tranzacții între companii](../../project-accounting/create-intercompany-transactions.md).

Dacă înregistrarea companiei nu are asociată nicio înregistrare contabilă, aceasta indică faptul că lipsește o configurație la configurarea mediului. Configurația trebuie corectată de administratorul de sistem. Administratorul de sistem trebuie să acceseze **Configurații cu scriere duală** și opriți și reporniți **Hartă cu dublă scriere Registre** cu sincronizarea inițială a acestei hărți și cerințele ei. Pentru mai multe informații, consultați [versiuni mapări cu scriere duală Project Operations](../../environment/resource-dual-write-maps.md).
