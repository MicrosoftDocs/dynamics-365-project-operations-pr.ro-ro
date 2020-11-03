---
title: Estimări de resurse
description: Acest subiect furnizează informații despre cum sunt calculate estimările de resurse în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082716"
---
# <a name="resource-estimates"></a>Estimări de resurse

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Estimările resurselor provin din eforturi în etape temporale care sunt definite în structura detaliată a proiectului împreună cu dimensiunile de preț aplicabile. De obicei, calculul este **rata/oră pentru fiecare rol x ore.** Efortul pe etape pentru fiecare resursă este stocat în înregistrarea de alocare a resurselor. Prețul este stocat într-o listă de prețuri predefinită. Conversia unității se aplică pe baza listei de prețuri aplicabile.

![Estimări de resursă](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Prețul de cost implicit și valuta de cost

Prețurile de cost sunt implicite din Unitatea Organizațională.

## <a name="default-bill-rate-and-sales-currency"></a>Rata de facturare implicită și moneda de vânzare

Prețurile de vânzare se aplică o dată pe tranzacție. Ierarhia pentru lista de prețuri de vânzare implicită este următoarea:

1. Organizație
2. Client
3. Ofertă/contract
