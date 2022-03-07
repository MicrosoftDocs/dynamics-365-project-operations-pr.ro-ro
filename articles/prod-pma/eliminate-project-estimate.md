---
title: Eliminarea unei estimări de proiect
description: Acest subiect oferă informații despre eliminarea unei estimări de proiect după finalizarea acestuia.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a7c9f5a03e3b5e9ad43e23c6174a820088025dc8419ae4f80d247d69e80c8038
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994111"
---
# <a name="eliminate-a-project-estimate"></a>Eliminarea unei estimări de proiect

[!include [banner](../includes/banner.md)]

Estimările proiectului furnizează perspectiva financiară a lucrului estimat și planificat pentru un proiect. Pentru a lucra cu estimări pentru un proiect, trebuie să atașați proiectul la un proiect de estimare. Un proiect de estimare se bazează întotdeauna pe un proiect existent, cu toate acestea, mai multe proiecte se pot referi la un singur proiect de estimare. Numai proiectele cu preț fix și investițiile pot fi atașate la proiectele estimate, iar proiectele respective trebuie să aparțină aceluiași grup de proiecte ca și proiectul estimativ.

Pentru a elimina un proiect de estimare, acesta trebuie să fie complet. Următorii pași explică modul de eliminare a unei estimări.

1. Accesați **Gestionarea proiectului și contabilitate** > **Toate proiectele** și deschideți proiectul. 
2. Pe fila **Administrați**, selectați **Estimări**, și pe pagina **Estimare** selectați **Eliminare**.
3. Pe pagina **Eliminați estimarea** pe fila **General**, setați următoarele opțiuni:

   - **Codul perioadei**: Selectați codul perioadei pentru a alege proiectele estimate corespunzătoare. 
   - **Data estimării**: Selectați data estimativă adecvată pentru eliminare.
   - **Eliminați cu avertismente WIP**: Activați această opțiune pentru a furniza notificări atunci când va fi eliminată o estimare asociată cu o lucrare în curs (WIP). Când această opțiune nu este activată, eliminarea nu poate continua dacă există tranzacții care nu sunt estimate. 
   > [!NOTE]
   > Această opțiune este disponibilă numai atunci când eliminarea este aplicată unui proiect estimativ. Nu este disponibil dacă utilizați postări periodice. Această setare funcționează cu setările de pe fila **Estimare** de pe pagina **Parametrii proiectului**, în câmpul de grup **Permiteți eliminarea atunci când există tranzacții care nu sunt estimate**.
   - **Puneți seta la Finalizat** : Activați această opțiune pentru a seta etapa proiectului estimativ la **Terminat** după ce executați eliminarea.
   - **Imprimați lista estimărilor**: Selectați informațiile care urmează să fie incluse la imprimarea listei estimative.
   - **Afișați Infolog**: Activați această opțiune pentru a afișa Infolog.
   - **Data postării**: Alegeți data de înregistrare a registrului estimativ.

4.  Selectați **OK**.
5. După finalizarea procesului de eliminare, proiectul estimat eliminat este afișat cu o valoare negativă. 

Dacă nu ați intenționat să eliminați o estimare, puteți selecta estimarea eliminată și selectați **Eliminare inversă**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]