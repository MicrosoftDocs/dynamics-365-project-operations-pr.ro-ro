---
title: Proiecte cu estimarea veniturilor cu preț fix
description: Acest subiect furnizează informații despre veniturilro la preț fix în proiecte.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531528"
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

