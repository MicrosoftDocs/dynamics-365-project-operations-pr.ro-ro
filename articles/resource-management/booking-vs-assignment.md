---
title: Rezervări versus atribuiri
description: Acest subiect furnizează informații despre diferențele dintre rezervările de resurse și atribuirile de resurse.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008466"
---
# <a name="bookings-vs-assignments"></a>Rezervări versus atribuiri

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Rezervările sunt alocarea fermă sau provizorie de resurse pentru un proiect. Rezervările ferme consumă capacitatea unei resurse. Rezervările reprezintă concepte organizaționale pentru echipe, astfel încât acestea să poată înțelege modul în care resursele vor fi angajate în diferite proiecte. Dynamics 365 Project Operations consideră rezervările ca fiind un concept la nivel de proiect. 

Spre deosebire de rezervări, atribuirile sunt angajamentul resurselor la activitățile de proiect în planificarea de proiect. Resursele pot fi denumite sau generice.  Când o cerință pentru o resursă derivă din atribuirile de sarcini în cadrul proiectului, Project Operations utilizează schițele de efort ale atribuirii resurselor pentru a construi schițele detaliilor cerințelor de resurse. Cu toate acestea, nu se menține o referință la atribuirea resurselor. Actualizările rezervărilor derivate din cerința de resurse nu actualizează nicio alocare de resurse.

De obicei, suma rezervărilor pentru o resursă va fi egală cu suma atribuțiilor resursei pentru una sau mai multe sarcini. Cu toate acestea, Project Operations nu pune în aplicare acest acord. Vizualizarea **Reconciliere** arată managerului de proiect unde rezervările unei resurse și atribuirile nu sunt de acord.




[!INCLUDE[footer-include](../includes/footer-banner.md)]