---
title: Înlocuirea listelor de prețuri de vânzare pentru proiect
description: Acest subiect oferă informații despre crearea listelor de prețuri de vânzare particularizate.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275553"
---
# <a name="override-project-sales-price-lists"></a>Înlocuirea listelor de prețuri de vânzare pentru proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

## <a name="customer-specific-project-price-lists"></a>Liste de prețuri de proiect specifice clientului

Acordurile de preț specifice clienților pot fi configurate ca liste de prețuri ale proiectelor într-o înregistrare de cont în Dynamics 365 Project Operations.

Pentru a configura o listă de prețuri specifice proiectului pentru client, în zona **Vânzări**, navigați la înregistrarea contului.

1. Deschideți pagina listei **Conturi**.
2. Găsiți și faceți dublu clic pe o înregistrare de client pentru a deschide pagina de detalii **Cont**.
3. Pe fila **Liste de prețuri de proiect**, selectați **+ Listă de prețuri de proiect nou**.
4. Pe pagina **Lista de prețuri a proiectului nou**, selectați o listă de prețuri din meniul derulant. Numai listele de prețuri care au contextul setat la **Vânzări** și a căror monedă se potrivește cu moneda contului sunt incluse.
5. Numiți asocierea și apoi selectați **Salvare**. Este creată o listă de prețuri de proiect specifică clientului. Această listă de prețuri va fi utilizată la prețurile implicite ale proiectului pentru ofertele de proiecte sau contractele create pentru acest client, atunci când data creată a contractului de ofertă sau a proiectului se încadrează în data efectivității listei de prețuri.

## <a name="custom-pricing-on-project-quotes"></a>Prețuri particularizate pentru ofertele de proiect

În ofertele proiectului, puteți avea prețuri de proiect care încep cu o listă de preț standard implicită, care este implicită de la client sau de la parametrii proiectului.

Când aveți nevoie de prețuri particularizate pentru lucrări legate de proiect pentru o anumită ofertă, puteți obține acest lucru din listele de prețuri ale proiectului entității asociate.

Parcurgeți pașii următori pentru a configura prețuri de ofertă specifice proiectului.

1. Deschideți oferta de proiect și selectați fila **Liste de prețuri de proiect**.
2. În subgrilă, selectați **Creați prețuri particularizate**.

Toate listele de prețuri ale proiectului care sunt atașate la ofertă sunt copiate în listele de prețuri noi. Numele noilor liste de prețuri reflectă numele ofertelor cu o ștampilă dată-oră pentru momentul în care au fost create aceste liste de prețuri.

Puteți utiliza fiecare dintre aceste liste de prețuri și puteți actualiza prețurile forței de muncă (prețul rolului) și cheltuielile (prețul categoriei). Aceste prețuri modificate se vor aplica numai acestei oferte de proiect.

## <a name="price-lists-on-a-project-contract"></a>Liste de prețuri pe un contract de proiect

Pe un contract de proiect, prețul proiectului este întotdeauna implicit ca o listă de prețuri personalizată cu numele contractului și ștampila de dată și oră creată atașată la nume. Acest lucru este adevărat dacă contractul a fost creat atunci când a fost câștigată oferta sau dacă contractul a fost creat de la zero. Dacă este necesar, puteți elimina această asociere în lista de prețuri personalizată și, în schimb, să asociați o listă de preț standard contractului de proiect.

Când asociați o listă de prețuri standard cu listele de prețuri ale proiectului la ofertă sau contract, orice modificare adusă prețurilor din lista de prețuri va avea impact asupra tuturor ofertelor și contractelor care utilizează lista de prețuri.


[!INCLUDE[footer-include](../includes/footer-banner.md)]