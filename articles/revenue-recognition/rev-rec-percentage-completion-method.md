---
title: Proiecte cu estimarea veniturilor cu preț fix
description: Acest subiect furnizează informații despre veniturilro la preț fix în proiecte.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 451f0403f0111b5ea4de6c91b54eae157830e413d3a21f23bd841a66905e147b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006441"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Proiecte cu estimarea veniturilor cu preț fix 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Când creați o linie de contract de proiect cu următoarele atribute în Dynamics 365 Project Operations pe Microsoft Dataverse, sistemul creează automat un proiect de estimare a venitului la preț fix. Informațiile din acest proiect se bazează pe următoarele:

  - O metodă de facturare cu preț fix.
  - Un proiect asociat.
  - Cel puțin o etapă definită pe fila **Planificarea facturilor** de pe pagina **Linia contractului de proiect**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revizuiți proiecte cu estimarea veniturilor cu preț fix
Pentru a revizui proiectele de estimare a veniturilor cu preț fix, parcurgeți următorii pași:

1. În mediul Dynamics 365 Finance, accesați **Managementul proiectelor și contabilitate** > **Proiecte** > **Proiecte de estimare a veniturilor cu preț fix**.
2. Selectați proiectul pe care doriți să îl vizualizați și faceți dublu clic pe **Estimarea ID-ului proiectului** pentru a deschide înregistrarea și a revizui detaliile proiectului.
3. Extindeți fila **Proiect**. Veți vedea un proiect în grila **Proiecte selectate**. Sistemul îl folosește ca proiect implicit, deoarece este proiectul asociat liniei contractului de proiect. 
4. Pentru a schimba asocierea, selectați proiecte suplimentare și adăugați-le la grila **Proiecte selectate**. Dacă sunt selectate mai multe proiecte în această grilă, finalizarea procentuală a proiectului și estimările veniturilor sunt calculate împreună pentru toate proiectele selectate.

  Costul proiectului, profilul veniturilor, șablonul de cost și codul perioadei pot fi setate manual. Dacă nu sunt setate manual, valorile sunt implicite în timpul primului calcul estimativ pentru proiect utilizând regulile configurate pentru profilurile de cost și venituri ale proiectului.



[!INCLUDE[footer-include](../includes/footer-banner.md)]