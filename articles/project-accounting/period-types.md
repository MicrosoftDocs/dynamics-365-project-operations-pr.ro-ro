---
title: Tipuri de perioade
description: Acest subiect oferă informații despre modul de configurare a tipurilor de perioadă pentru estimarea veniturilor.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 487e3de7895ca0752e6c9033c7bb7007ba89301c01e6205b3bc8a7d750724bc9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998791"
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]