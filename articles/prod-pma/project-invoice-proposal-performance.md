---
title: Performanța propunerilor de facturi pentru proiect
description: Acest subiect oferă informații despre îmbunătățirile de performanță pentru propunerile de facturi ale proiectului.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005721"
---
# <a name="project-invoice-proposal-performance"></a>Performanța propunerilor de facturi pentru proiect

[!include [banner](../includes/banner.md)]

Când creați o nouă propunere de facturare, este posibil să întâmpinați probleme de performanță pe măsură ce crește numărul de proiecte și subproiecte. Pentru a îmbunătăți performanța, este disponibilă o caracteristică care reduce timpul necesar pentru crearea unei noi propuneri de facturare pentru tranzacțiile de proiect afișate.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Activați îmbunătățirea performanței propuenrilor de facturi pentru proiect
Pentru a activa caracteristica de îmbunătățire a performanței propunerii de facturare a proiectului, parcurgeți pașii următori.

1.  Accesați **Managementul caracteristicilor** > **Toate**. În lista de funcții, localizați **Îmbunătățirea performanței propunerii de factură a proiectului**.
2.  Selectați **Activați acum**.
3.  Reîmprospătați browserul, apoi creați o nouă propunere de facturare.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Dezactivați îmbunătățirea performanței propuenrilor de facturi pentru proiect
Terminați următorii pași pentru a dezactiva îmbunătățirea performanței propunerii de facturare a proiectului.

1.  Accesați **Managementul caracteristicilor** > **Toate**. În lista de funcții, localizați **Îmbunătățirea performanței propunerii de factură a proiectului**.
2.  Selectați **Dezactivare**.
3.  Reîmprospătați browserul.

> [!NOTE]
> Performanța propunerilor de factură nu poate fi aplicată atunci când regulile de facturare sunt activate.
> 
> În timpul procesului pe lot pentru a crea propuneri de facturare, numărul de sarcini secundare va împărți sarcinile la un număr maxim, pe baza numărului de contracte cu tranzacții facturabile, indiferent de ceea ce ați introdus. De exemplu, dacă introduceți **3** pentru numărul de subactivități pentru crearea de propuneri de facturi în lot și există doar două contracte cu tranzacții facturabile, sunt create doar două subactivități.
