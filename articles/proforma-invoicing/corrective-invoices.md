---
title: Facturi corectate
description: Acest subiect oferă informații despre facturi corectate.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898096"
---
# <a name="corrected-invoices"></a>Facturi corectate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Facturile PSA confirmate pot fi editate. Când editați o factură confirmată, se creează o schiță a facturii corectate. Întrucât ipoteza este că doriți să inversați toate tranzacțiile și cantitățile din factura originală, această factură corectată include toate tranzacțiile din factura originală și toate cantitățile de aici sunt zero (0).

Când tranzacțiile nu necesită corecție, puteți să le eliminați din proiectul de factură rectificativă. Pentru a inversa sau returna numai o cantitate parțială, puteți să editați câmpul Cantitate în detaliul liniei. Dacă deschideți detaliul de linie factură, puteți să vedeți cantitatea inițială de factură. Aveți posibilitatea să editați apoi cantitatea curentă de factură, astfel încât să fie mai mică sau mai mare decât cantitatea inițială de factură.

Când confirmați o factură rectificativă, valoarea reală a vânzărilor inițiale facturate este inversată și se creează o nouă valoare reală de vânzări facturate. În cazul în care cantitatea a fost redusă, diferența va provoca o nouă valoare reală de vânzări nefacturate pentru a fi create. De exemplu, dacă vânzarea facturată inițial a fost de opt ore și detaliile liniei de factură corectate are o cantitate redusă de șase ore, liniile facturate origniale sunt inversate și sunt create două noi valori reale:

- O valoare reală de vânzări facturate timp de șase ore.
- O valoare reală de vânzări nefacturate pentru restul de două ore. Această tranzacție poate fi facturată ulterior sau poate fi marcată ca netaxabilă, în funcție de negocierile cu clientul.
