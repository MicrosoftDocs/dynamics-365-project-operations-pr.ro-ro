---
title: Definirea calendarelor de proiect
description: Acest subiect oferă informații despre cum se aplică un șablon de calendar unui proiect pentru a urmări planificarea proiectului.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999011"
---
# <a name="define-project-calendars"></a>Definirea calendarelor de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Pentru a crea și gestiona un proiect, trebuie să aplicați un șablon de calendar de proiect. Șablonul de calendar definește următoarele atribute de proiect:

- Programul de lucru, inclusiv ora de început și sfârșit
- Zile de lucru
- Excepții din calendar, cum ar fi zilele nelucrătoare

Șablonul de calendar aplicat unui proiect este o copie a șablonului calendarului definit în setările organizației dvs.

> [!NOTE]
> Dacă modificați șablonul de calendar, aceste modificări nu se propagă la planificarea de lucru a proiectului. Pentru a schimba planificarea de lucru a proiectului, trebuie aplicat un nou șablon.

Pentru a crea un șablon de calendar pentru organizația dvs., există două cerințe principale:

- Definiți orele de lucru dorite ale șablonului utilizând o resursă rezervabilă nouă sau existentă.
- Creați un nou șablon de calendar și asociați șablonul cu resursa rezervabilă.

**Definiți orele de lucru ale șablonului**

1. Accesați **Resurse** \> **Resurse**.
2. Creați o nouă resursă pentru a face referință în șablonul calendarului sau selectați o resursă existentă.
3. Selectați fila **Ore de lucru** a resursei și completați instrucțiunile din [Setarea orelor de lucru pentru o resursă](/dynamics365/field-service/set-work-hours-resource.md) pentru a configura regulile calendarului.

**Creați un șablon nou de calendar**

1. Accesați **Setări** \> **Șabloane de calendar**.
2. Selectați **Nou** și introduceți un nume, o descriere și o resursă șablon.

> [!NOTE]
> Când se face referire la o resursă într-un șablon de calendar, o copie a calendarului resursei este asociată cu șablonul de calendar. Dacă modificați orele de lucru ale șablonului copiat, aceste modificări nu se propagă în șablonul de calendar.

Acum aveți posibilitatea să asociați șablonul de lucru cu un șablon de calendar de proiect.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

