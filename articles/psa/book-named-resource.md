---
title: Rezervați resurse denumite din cerințele de resurse
description: Acest subiect furnizează informații despre rezervarea de resurse denumite pentru o cerință de resurse generice.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e929a5fb4c307d3b64d0f7f70203fe20bc6dd4f99e89e039fae0ce8276c69c52
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000501"
---
# <a name="book-named-resources-from-resource-requirements"></a>Rezervați resurse denumite din cerințele de resurse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aveți posibilitatea să rezervați o resursă denumită pentru a înlocui resursa generică care are o cerință de resurse.

1. În Project Service Automation (PSA), pe pagina **Proiecte**, faceți clic pe fila **Echipă**.
2. Selectați resursa generică care are o cerință de resurse din listă și apoi faceți clic pe **Rezervare**. Sau, deschideți cerința de resurse și apoi faceți clic pe **Rezervare**.


![Rezervarea unui membru generic al echipei.](media/RM-how-to-14.png)


3. În pagina **Asistent de planificare**, selectați o resursă denumită pentru a rezerva în echipa de proiect și apoi faceți clic pe **Rezervare**.

![Rezervarea unui membru generic al echipei folosind Asistentul de planificare.](media/RM-how-to-15.png)

Când rezervarea este finalizată și îndeplinită de o resursă denumită, resursa generică este înlocuită cu resursa denumită.

![Membru al echipei denumit înlocuind un membru generic al echipei.](media/RM-how-to-16.png)

Atribuirile din planificare sunt actualizate și cu resursa denumită.

![Membru al echipei denumit atribuit la activități de proiect.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Îndeplinirea unei resurse generice cu mai multe resurse denumite
Îndeplinirea unei cerințe pentru o resursă generică cu mai multe resurse denumite este similară cu atribuirea unei singure resurse denumite. De exemplu, există o activitate cu o durată de cinci zile și 120 de ore de efort. Această activitate nu poate fi finalizată de către o singură resursă care lucrează o zi tipică de opt ore, cinci zile pe săptămână. 

![O activitate care are nevoie de 120 de ore de efort de peste cinci zile.](media/RM-how-to-21.png)

Cerința este de 120 de ore de inginerie robotică timp de cinci zile, ceea ce înseamnă 24 de ore pe zi.

![Cerință pe zi.](media/RM-how-to-22.png)

Acesta este un exemplu de moment în care sunt necesare mai multe resurse denumite pentru a îndeplini o solicitare de resurse generice. Va trebui să rezervați mai multe resurse pentru a îndeplini cerința.

![Rezervarea mai multor resurse pentru a îndeplini cerința.](media/RM-how-to-23.png)

Diferența principală în acest scenariu este că resursa generică rămâne pe echipa atribuită activității și membrii echipei de resurse denumiți rezervați nu sunt atribuiți ca parte a poziției. Managerul de proiect poate atribui lucrul după cum este adecvat către resursele denumite. Vizualizarea **Reconciliere** poate ajuta un manager de proiect la defalcarea rezervărilor în mai multe resurse pentru atribuiri de activități. Acest lucru nu se face în mod automat, deoarece în orice scenariu mai complicat decât exemplul simplu de mai sus, cum ar fi în cazul în care aveți un pachet de activități care alcătuiesc cerința, intenția modului în care managerul de proiect vrea să atribuie trebuie să fie asumată de sistem. Deoarece sistemul nu poate înțelege intenția, sunt șanse ca ipotezele să fie diferite de cele preconizate și să se producă un rezultat incorect sau imprevizibil. Rezultatul previzibil este că resursa generică rămâne atribuită până când managerul de proiect creează în mod deliberat atribuiri, utilizând vizualizarea **Reconciliere**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]