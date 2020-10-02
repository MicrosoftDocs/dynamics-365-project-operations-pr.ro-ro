---
title: Configurați fluxuri de lucru pentru gestionarea cheltuielilor
description: Puteți configura un proces de flux de lucru care este utilizat pentru a revizui și aproba documentele de călătorie și cheltuieli.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896566"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurați fluxuri de lucru pentru gestionarea cheltuielilor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Puteți configura un proces de flux de lucru pentru a revizui și aproba documentele de călătorie și cheltuieli. Puteți defini fluxuri de lucru pentru rapoarte de cheltuieli, cereri de călătorie și cereri de avans în numerar.

Un flux de lucru reprezintă un proces de afaceri și definește modul în care un document circulă prin sistem. Fluxul de lucru indică, de asemenea, cine trebuie să finalizeze o sarcină sau să aprobe un document. Există mai multe avantaje ale utilizării sistemului de flux de lucru în organizația dvs.:

- **Procese consistente**: Puteți defini procesul de aprobare pentru documente specifice, cum ar fi cereri de achiziții și rapoarte de cheltuieli. Utilizarea sistemului de flux de lucru vă asigură că documentele sunt procesate și aprobate într-un mod consecvent și eficient.
- **Vizibilitatea procesului**: Puteți urmări statutul, istoricul și valorile de performanță ale unei instanțe specifice de flux de lucru. Acest lucru vă ajută să determinați dacă ar trebui făcute modificări ale fluxului de lucru pentru a îmbunătăți eficiența.
- **Lista de lucru centralizată**: utilizatorii pot vizualiza o listă de lucru centralizată pentru a vizualiza sarcinile fluxului de lucru și aprobările atribuite acestora. 

## <a name="workflow-types"></a>Tipuri de flux de lucru

Următorul tabel listează tipurile de fluxuri de lucru în care puteți crea **Managementul cheltuielilor**.


|              <strong>Tip</strong>              |                   <strong>Utilizați acest tip pentru</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Auto aprobarea raportului de cheltuieli</strong> |            Creați fluxuri de lucru de aprobare pentru rapoartele de cheltuieli.             |
|  <strong>Publicarea automată a rapoartelor de cheltuieli</strong>   |        Creați fluxuri de lucru automate de publicare pentru rapoartele de cheltuieli.        |
|       <strong>Element de linie de cheltuială</strong>        |     Creați fluxuri de lucru de aprobare pentru elemente de linie pe rapoartele de cheltuieli.      |
| <strong>Publicare automată de element de cheltuială de linie</strong> | Creați fluxuri de lucru de publicare automată pentru elemente de linie pe rapoartele de cheltuieli. |
|       <strong>Cerere de călătorie</strong>       |          Creați fluxuri de lucru de aprobare pentru cererile de călătorie.           |
|      <strong>Solicitare de avans în numerar</strong>      |         Creați fluxuri de lucru de aprobare pentru solicitări de avans în numerar.          |
|        <strong>Recuperarea impozitului TVA</strong>        | Creați fluxuri de lucru de aprobare pentru recuperarea taxei pe valoarea adăugată (TVA).  |
