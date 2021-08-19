---
title: Îndeplinirea cerințelor de resurse generice
description: Acest subiect furnizează informații despre cum să rezervați resurse denumite pentru o cerință de resurse generice.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4ff8f74fdaeac9757af8df4803e58a006ebb9fe21a460cf0ffcb35f1a4d6308f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008286"
---
# <a name="generic-resource-requirement-fulfillment"></a>Îndeplinirea cerințelor de resurse generice

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Aveți posibilitatea să rezervați o resursă denumită pentru a înlocui resursa generică care are o cerință de resurse.

1. Pe pagina **Proiecte**, selectați fila **Echipă**.
2. Selectați resursa generică care are o cerință de resurse din listă și apoi selectați **Rezervare**. Sau, deschideți cerința de resurse și apoi selectați **Rezervare**.
3. În pagina **Asistent de planificare**, selectați o resursă denumită pentru a rezerva în echipa de proiect și apoi selectați **Rezervare**.

Când rezervarea este finalizată și îndeplinită de o resursă denumită, resursa generică este înlocuită cu resursa denumită.

Atribuirile din planificare sunt actualizate și cu resursa denumită.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Îndeplinirea unei resurse generice cu mai multe resurse denumite
Îndeplinirea unei cerințe pentru o resursă generică cu mai multe resurse denumite este similară cu atribuirea unei singure resurse denumite. De exemplu, există o activitate cu o durată de cinci zile și 120 de ore de efort. Această activitate nu poate fi finalizată de către o singură resursă care lucrează o zi tipică de opt ore, cinci zile pe săptămână. 

Cerința este de 120 de ore de inginerie robotică timp de cinci zile, ceea ce înseamnă 24 de ore pe zi.

Acesta este un exemplu de moment în care sunt necesare mai multe resurse denumite pentru a îndeplini o solicitare de resurse generice. Va trebui să rezervați mai multe resurse pentru a îndeplini cerința.

Diferența principală în acest scenariu este că resursa generică rămâne pe echipa atribuită activității și membrii echipei de resurse denumiți rezervați nu sunt atribuiți ca parte a poziției. Managerul de proiect poate atribui lucrul după cum este adecvat către resursele denumite. Vizualizarea **Reconciliere** poate ajuta un manager de proiect la defalcarea rezervărilor în mai multe resurse pentru atribuiri de activități. Acest lucru nu se face în mod automat, deoarece în orice scenariu mai complicat decât exemplul simplu de mai sus, cum ar fi în cazul în care aveți un pachet de activități care alcătuiesc cerința sau intenția modului în care managerul de proiect vrea să atribuie trebuie să fie asumată de sistem. Deoarece sistemul nu poate înțelege intenția, este posibil ca ipotezele să fie diferite de cele preconizate și se va produce un rezultat incorect sau imprevizibil. Rezultatul previzibil este că resursa generică rămâne atribuită până când managerul de proiect creează în mod deliberat atribuiri, utilizând vizualizarea **Reconciliere**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]