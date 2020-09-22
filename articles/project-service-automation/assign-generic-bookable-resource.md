---
title: Atribuirea de resurse generice rezervabile unei activități și unei echipe de proiect
description: Acest subiect oferă informații despre rezervarea resurselor generice pentru activități și echipe de proiect.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754841"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Atribuiți resurse generice care se pot rezerva unei activități și generați cerințe de resurse 

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

