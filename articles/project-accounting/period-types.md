---
title: Tipuri de perioade
description: Acest subiect oferă informații despre modul de configurare a tipurilor de perioadă pentru estimarea veniturilor.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531527"
---
# <a name="period-types"></a>Tipuri de perioade

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Un tip de perioadă definește frecvența cu care se estimează veniturile dintr-un proiect. Acest subiect oferă informații despre modul de configurare a tipurilor de perioadă pentru estimarea veniturilor. 

## <a name="create-and-work-with-period-types"></a>Crearea și lucrul cu tipuri de perioade
Pentru a crea și a lucra cu tipuri de perioadă, parcurgeți următorii pași:

1. În mediul dvs. Dynamics 365 Finance, accesați **Management de proiect și contabilitate** > **Configurare** > **Estimări** > **Tipuri de perioade**.
2. Selectați **Nou** pentru a crea un nou tip de perioadă. Introduceți un nume și descriere.
3. În câmpul **Frecvență**, selectați o valoare:

    - Dacă selectați **Săptămână**, **Bi-săptămânal**, **Semestrial**, **Lună**, **Zi**, **Sfert**, sau **An**, calendarul va fi folosit pentru a genera perioadele. 
    - Dacă selectați **Perioada contabilă**, perioadele contabile din configurația contabilității generale vor fi utilizate pentru a genera perioade.
    - Dacă selectați **Nelimitat**, puteți specifica perioade personalizate.
4. Selectați înregistrarea tipului de perioadă și apoi selectați **Generați perioade** pentru a crea perioade pentru tipul perioadei. Pe baza frecvenței de perioadă pe care ați selectat-o, este posibil să aveți opțiunea de a specifica o dată de începere sau numărul de perioade de generat.
5. Selectați **Perioade** pentru a revizui perioadele generate.

