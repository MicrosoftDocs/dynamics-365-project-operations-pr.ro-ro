---
title: Comenzi de vânzare pentru proiecte de timp și materiale
description: Acest subiect explică cum să creați comenzi de vânzare bazate pe proiecte pentru proiecte de timp și materiale.
author: KimANelson
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
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754700"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Comenzi de vânzare pentru proiecte de timp și materiale

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Acest subiect descrie cum să creați o comandă de vânzare pentru un proiect. Comenzile de vânzare pot fi create numai pentru proiecte de tip **timp și material**.

Dacă un proiect de timp și materiale are mai multe surse de finanțare în contractul de proiect, trebuie să activați parametrul **Permiteți comenzi de vânzare pentru proiecte cu mai multe surse de finanțare** pe pagina **Managementul proiectului și parametrii contabili**. 

> [!NOTE]
> - Suportul pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare este disponibil începând cu versiunea aplicației 10.0.2 și mai nouă.
> - Parametrul pentru a permite asistența pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare va fi eliminat în valul de lansare din aprilie 2020, după care funcționalitatea va fi întotdeauna activată.

Puteți crea comenzi de vânzare bazate pe proiecte în două moduri:

- Accesați proiectul în sine. În panoul de acțiuni, selectați **Gestionați > Sarcini articol > Comandă de vânzare**. Informațiile despre proiect vor fi implicite pentru comanda de vânzare din proiect. Dacă contractul de proiect are mai multe surse de finanțare, va trebui să selectați sursa de finanțare pentru a seta clientul pentru comanda de vânzare. Dacă există o singură sursă de finanțare pentru proiect, clientul va fi setat automat.
- Accesați pagina de listă **Comanda toate vânzările** și creați o nouă comandă de vânzări. Va trebui să selectați proiectul pentru comanda de vânzare. După selectarea proiectului, clientul va fi setat din sursa de finanțare sau va trebui să selectați sursa de finanțare dacă contractul de proiect are mai multe surse de finanțare.

