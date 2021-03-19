---
title: Crearea unor modele de prognoză pentru bugetele proiectului
description: Acest subiect descrie cum să creați un model de prognoză pentru bugetele rămase.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271053"
---
# <a name="create-forecast-models-for-project-budgets"></a>Crearea unor modele de prognoză pentru bugetele proiectului 

[!include [banner](../includes/banner.md)]

Acest subiect descrie cum să creați un model de prognoză pentru bugetele rămase. Un proiect care este supus controlului bugetar utilizează două tipuri de bugete: original și rămas. Când creați un buget de proiect, trebuie să specificați modelele de prognoză de buget inițiale și rămase care au fost create în pagina **Modele de prognoză**. Bugetele proiectului pe baza modelelor specificate sunt create atunci când vă angajați la bugetul proiectului.

> [!NOTE]
> Un model de prognoză care este utilizat pentru controlul bugetului nu poate avea un submodel sau nu poate fi folosit ca submodel.

1. Selectați **Management de proiect și contabilitate** > **Configurare** > **Prognoze**  > **Modele de prognoză**.
2. Selectați **Nou** pentru a crea un nou model de prognoză, apoi introduceți un număr de ID de model și un nume pentru noul model. 
3. Setați opțiunea **Oprit** pentru **Da** pentru a preveni orice modificare a liniilor de prognoză pentru modelul de prognoză. 
4. Dacă liniile de prognoză cu care este asociat modelul ar trebui să genereze previziuni ale fluxului de numerar în registrul general, setați **Includeți în previziunile fluxurilor de numerar** la **Da.** 
5. Pentru a utiliza data proiectului ca dată a facturii, setați **Data facturii cu prognoză** la **Da**. 
6. În **Tipul bugetului**, selectați unul dintre următoarele tipuri de modele:

   - **Bugetul original**: Utilizați sumele inițiale ale bugetului care sunt angajate atunci când bugetul inițial este creat și aprobat.
   - **Buget rămas**: Utilizați sumele bugetare rămase pe durata proiectului. Soldurile din acest model de prognoză sunt reduse prin tranzacții reale și crescute sau diminuate prin revizuiri bugetare.
   - **Reportare**: Utilizați sumele din bugetul de reportare pentru proiect. Reportarea este un proces opțional care poate fi rulat pentru a transfera sumele neutilizate ale bugetului de la un exercițiu financiar la altul.

7. Setați următoarele opțiuni, după cum este necesar:

   - Activați **Data facturii cu prognoză** pentru a utiliza data proiectului ca dată a facturii.
   - Activați **Prognoza cu WIP** pentru a prognoza pe baza lucrărilor în curs (WIP), apoi selectați tipul de WIP. 
   - Puteți păstra valoarea implicită **Tipul bugetului** ca **Niciuna** sau introduceți un tip nou. Tipul de buget nu poate fi modificat după ce schimbați o înregistrare.     
    > [!NOTE]
    > Dacă modificați tipul de buget implicit, toate celelalte opțiuni nu vor fi disponibile pentru actualizări și nu puteți reutiliza acest model de prognoză. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]