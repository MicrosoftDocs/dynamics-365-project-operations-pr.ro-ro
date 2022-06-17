---
title: Tipuri de perioade
description: Acest articol oferă informații despre cum să configurați tipurile de perioade pentru estimarea veniturilor.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930977"
---
# <a name="period-types"></a>Tipuri de perioade

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Un tip de perioadă definește frecvența cu care se estimează veniturile dintr-un proiect. Acest articol oferă informații despre cum să configurați tipurile de perioade pentru estimarea veniturilor. 

## <a name="create-and-work-with-period-types"></a>Crearea și lucrul cu tipuri de perioade
Pentru a crea și a lucra cu tipuri de perioadă, parcurgeți următorii pași:

1. În mediul dvs. Dynamics 365 Finance, accesați **Management de proiect si contabilitate** > **Înființat** > **Estimări** > **Tipuri de perioade**.
2. Selectați **Nou** pentru a crea un nou tip de perioadă. Introduceți un nume și descriere.
3. În câmpul **Frecvență**, selectați o valoare:

    - Dacă selectați **Săptămână**, **Bi-săptămânal**, **Semestrial**, **Lună**, **Zi**, **Sfert**, sau **An**, calendarul va fi folosit pentru a genera perioadele. 
    - Dacă selectați **Perioada contabilă**, perioadele contabile din configurația contabilității generale vor fi utilizate pentru a genera perioade.
    - Dacă selectați **Nelimitat**, puteți specifica perioade personalizate.
4. Selectați înregistrarea tipului de perioadă și apoi selectați **Generați perioade** pentru a crea perioade pentru tipul perioadei. Pe baza frecvenței de perioadă pe care ați selectat-o, este posibil să aveți opțiunea de a specifica o dată de începere sau numărul de perioade de generat.
5. Selectați **Perioade** pentru a revizui perioadele generate.



[!INCLUDE[footer-include](../includes/footer-banner.md)]