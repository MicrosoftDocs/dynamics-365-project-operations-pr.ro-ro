---
title: Rezervări versus atribuiri
description: Acest articol oferă informații despre diferențele dintre rezervările de resurse și alocările de resurse.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3410a45ce8401905dc162db66b0975e4aa3350dc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918603"
---
# <a name="bookings-vs-assignments"></a>Rezervări versus atribuiri

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Rezervările sunt alocarea fermă sau provizorie de resurse pentru un proiect. Rezervările ferme consumă capacitatea unei resurse. Rezervările reprezintă concepte organizaționale pentru echipe, astfel încât acestea să poată înțelege modul în care resursele vor fi angajate în diferite proiecte. Dynamics 365 Project Operations consideră rezervările ca fiind un concept la nivel de proiect. 

Spre deosebire de rezervări, atribuirile sunt angajamentul resurselor la activitățile de proiect în planificarea de proiect. Resursele pot fi denumite sau generice.  Când o cerință pentru o resursă derivă din atribuirile de sarcini în cadrul proiectului, Project Operations utilizează schițele de efort ale atribuirii resurselor pentru a construi schițele detaliilor cerințelor de resurse. Cu toate acestea, nu se menține o referință la atribuirea resurselor. Actualizările rezervărilor derivate din cerința de resurse nu actualizează nicio alocare de resurse.

De obicei, suma rezervărilor pentru o resursă va fi egală cu suma atribuțiilor resursei pentru una sau mai multe sarcini. Cu toate acestea, Project Operations nu pune în aplicare acest acord. Vizualizarea **Reconciliere** arată managerului de proiect unde rezervările unei resurse și atribuirile nu sunt de acord.




[!INCLUDE[footer-include](../includes/footer-banner.md)]