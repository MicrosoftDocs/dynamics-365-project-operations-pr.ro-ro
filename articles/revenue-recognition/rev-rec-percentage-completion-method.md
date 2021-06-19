---
title: Proiecte cu estimarea veniturilor cu preț fix
description: Acest subiect furnizează informații despre veniturilro la preț fix în proiecte.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013816"
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