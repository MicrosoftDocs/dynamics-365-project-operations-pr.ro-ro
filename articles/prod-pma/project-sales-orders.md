---
title: Comenzi de vânzare pentru proiecte de timp și materiale
description: Acest subiect explică cum să creați comenzi de vânzare bazate pe proiecte pentru proiecte de timp și materiale.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082781"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Comenzi de vânzare pentru proiecte de timp și materiale

[!include[banner](../includes/banner.md)]

Acest subiect descrie cum să creați o comandă de vânzare pentru un proiect. Comenzile de vânzare pot fi create numai pentru proiecte de tip **timp și material**.

Dacă un proiect de timp și materiale are mai multe surse de finanțare în contractul de proiect, trebuie să activați parametrul **Permiteți comenzi de vânzare pentru proiecte cu mai multe surse de finanțare** pe pagina **Managementul proiectului și parametrii contabili**. 

> [!NOTE]
> - Suportul pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare este disponibil începând cu versiunea aplicației 10.0.2 și mai nouă.
> - Parametrul pentru a permite asistența pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare va fi eliminat în valul de lansare din aprilie 2020, după care funcționalitatea va fi întotdeauna activată.

Puteți crea comenzi de vânzare bazate pe proiecte în două moduri:

- Accesați proiectul în sine. În panoul de acțiuni, selectați **Gestionați > Sarcini articol > Comandă de vânzare**. Informațiile despre proiect vor fi implicite pentru comanda de vânzare din proiect. Dacă contractul de proiect are mai multe surse de finanțare, va trebui să selectați sursa de finanțare pentru a seta clientul pentru comanda de vânzare. Dacă există o singură sursă de finanțare pentru proiect, clientul va fi setat automat.
- Accesați pagina de listă **Comanda toate vânzările** și creați o nouă comandă de vânzări. Va trebui să selectați proiectul pentru comanda de vânzare. După selectarea proiectului, clientul va fi setat din sursa de finanțare sau va trebui să selectați sursa de finanțare dacă contractul de proiect are mai multe surse de finanțare.

