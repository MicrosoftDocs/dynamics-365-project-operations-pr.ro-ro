---
title: Estimări de resurse
description: Acest subiect furnizează informații despre cum sunt calculate estimările de resurse în Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127390"
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
