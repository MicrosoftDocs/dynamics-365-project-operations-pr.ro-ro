---
title: Aprobatori multipli pe un raport de cheltuieli
description: Acest subiect oferă informații despre rapoartele de cheltuieli care necesită aprobarea de către mai multe persoane.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082952"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Aprobatori multipli pe un raport de cheltuieli

[!include [banner](../includes/banner.md)]

În funcție de politicile de aprobare a cheltuielilor organizației dvs., mai mult de o persoană ar trebui să aprobe un raport de cheltuieli care este prezentat de un angajat. Când configurați procesul fluxului de lucru pentru aprobarea raportului de cheltuieli, puteți adăuga elemente de flux de lucru care includ sarcini sau pași pentru unul sau mai mulți aprobatori de rapoarte de cheltuieli. De exemplu, s-ar putea să solicitați ca toate rapoartele de cheltuieli să fie aprobate mai întâi, managerul angajatului care a trimis raportul și apoi de coordonatorul de conturi de plată.

Dacă decideți să solicitați mai mulți aprobatori de rapoarte de cheltuieli, puteți adăuga elementele fluxului de lucru în oricare dintre următoarele moduri:

- Adăugați un element de aprobare care are un singur pas. De exemplu, pasul ar putea necesita ca un raport de cheltuieli să fie atribuit unui grup de utilizatori și să fie aprobat de 50% din membrii grupului de utilizatori.
- Adăugați un element de aprobare care are mai mulți pași. De exemplu, elementul de aprobare poate avea următorii pași:

    1. Managerul angajatului care a depus raportul de cheltuieli îl aprobă.
    2. Grefierul de conturi de plată verifică chitanțele și articolele raportului de cheltuieli.
    3. Proprietarul bugetului aprobă raportul de cheltuieli.

- Adăugați mai multe elemente de aprobare, fiecare dintre acestea având un singur pas. De exemplu, puteți adăuga un element de aprobare separat pentru fiecare dintre pașii următori:

    1. Managerul angajatului aprobă raportul de cheltuieli.
    2. Proprietarul bugetului aprobă raportul de cheltuieli.