---
title: Configurarea tarifelor de cost și de vânzare pentru produsele din catalog
description: Acest subiect oferă informații despre modul de configurare al ratei de cost și vânzări pentru elemente dintr-un catalog de produse.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082863"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Configurarea tarifelor de cost și de vânzare pentru produsele din catalog

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_


Configurarea prețurilor pentru articolele din catalogul de produse în Dynamics 365 Project Operations este aceeași ca în Dynamics 365 Sales.

Deoarece produsele nu pot fi estimate sau utilizate în proiecte în Project Operations, nu este necesar să stabiliți prețurile din catalogul de produse pe listele de prețuri ale proiectelor pentru ofertele și contractele.

Prețurile din catalogul de produse trebuie stabilite în câmpul **Prețul produsului** al unei cotații, a unui contract sau a unui cont. Nu setați prețurile din catalogul de produse în listele de prețuri ale proiectului pentru aceste entități. Listele de prețuri ale proiectului sunt exclusive pentru Project Operations. Există o logică de afaceri specifică aplicației care copiază listele de preț dintr-o ofertă într-un contract. Rezultatul este o listă de prețuri de proiect specifică pentru un contract. Operația de copiere poate întârzia procesul de câștigare a ofertei dacă lista de prețuri a proiectului din ofertă devine prea mare. Listele de prețuri ale produselor nu sunt copiate pentru a crea liste de prețuri personalizate în contracte. Aceasta înseamnă că listele de prețuri ale produselor nu au impact asupra performanței procesului de câștigare a ofertelor.
