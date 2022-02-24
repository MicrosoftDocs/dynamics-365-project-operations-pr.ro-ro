---
title: Atribuirea de resurse generice rezervabile unei activități și unei echipe de proiect
description: Acest subiect oferă informații despre rezervarea resurselor generice pentru activități și echipe de proiect.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145418"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Atribuiți resurse generice care se pot rezerva unei activități și generați cerințe de resurse 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pe lângă rezervarea și atribuirea resurselor denumite sau reale proiectului dvs., aveți posibilitatea să atribuiți resurse generice activităților de proiect. Aceste resurse pot servi ca substituenți pentru resursele numite până când sunteți gata să alocați ca personal pentru proiectul dvs. resurse numite. 

1. În Project Service Automation (PSA), deschideți pagina **Proiect** și în fila **Planificare**, introduceți numele de poziție al resursei generice în celula **Resursă** a planificării. Sau, aveți posibilitatea să faceți clic pe pictograma **Resursă** din celulă pentru a deschide selectorul de resurse, apoi introduceți numele resursei generice pe care doriți să o creați.

![Crearea și atribuirea unui membru al echipei generice](media/RM-how-to-9.png)

Acest lucru va deschide panoul **Creare rapidă: membru al echipei de proiect**. 

2. Introduceți rolul și unitatea organizațională a membrului echipei de resurse generice și apoi faceți clic pe **Salvare**.

![Creare rapidă membru al echipei generice](media/RM-how-to-10.png)

3. După ce ați creat noul membru al echipei de resurse generice, acesta este atribuit activității. Aveți posibilitatea să continuați să atribuiți acea resursă generică altor activități din planificarea activităților.

![Atribuirea membrului de echipă generic existent la activități](media/RM-how-to-11.png)

4. După ce ați atribuit resursa generică, aveți posibilitatea să generați o cerință de resursă și să o îndepliniți prin rezervarea directă sau prin trimiterea unei solicitări de resurse către un manager de resurse.

![Generarea unei cerințe pentru un membru al echipei generice](media/RM-how-to-12.png)

În grila de membru al echipei, pe lângă posibilitatea de a utiliza selectorul de resurse așa s-a menționat mai sus, puteți adăuga direct resurse generice. Resursele sunt adăugate cu o cerință de resurse care se bazează pe datele de început/sfârșit și pe metoda de alocare specificată în panoul **Creare rapidă: membru al echipei de proiect**.

Puteți vedea o diferență dacă adăugați direct membrul echipei generice și apoi atribuiți resursei generice mai multe activități decât numărul de ore de care aceasta dispune pentru a le acoperi. Faceți clic pe **Generare cerință** pentru a regenera cerința, în scopul de a echilibra orele necesare și atribuirile.

De asemenea, puteți face clic pe linkul **Cerință resursă** din grila de echipă pentru a deschide cerința și a adăuga competențe, resurse preferate etc.

![Cerință resursă](media/RM-how-to-13.png)

