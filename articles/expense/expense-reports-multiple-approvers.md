---
title: Rapoarte de cheltuieli și mai mulți aprobatori
description: Acest subiect oferă informații despre rapoartele de cheltuieli care necesită aprobarea mai multor persoane.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897106"
---
# <a name="expense-reports-and-multiple-approvers"></a>Rapoarte de cheltuieli și mai mulți aprobatori

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În funcție de politicile de aprobare a cheltuielilor organizației dvs., mai mult de o persoană ar trebui să aprobe un raport de cheltuieli trimis. Când configurați procesul fluxului de lucru pentru aprobarea raportului de cheltuieli, puteți adăuga elemente de flux de lucru care includ sarcini sau pași pentru unul sau mai mulți aprobatori de rapoarte de cheltuieli. De exemplu, s-ar putea să solicitați ca toate rapoartele de cheltuieli să fie aprobate de două persoane separate, managerul angajatului care a trimis raportul și coordonatorul de conturi de plată.

Dacă decideți să solicitați mai mulți aprobatori de rapoarte de cheltuieli, puteți adăuga elementele fluxului de lucru în oricare dintre următoarele moduri:

- Adăugați un element de aprobare care are un singur pas. De exemplu, pasul ar putea necesita ca un raport de cheltuieli să fie atribuit unui grup de utilizatori și să fie aprobat de 50% din membrii grupului de utilizatori.
- Adăugați un element de aprobare care are mai mulți pași. De exemplu, elementul de aprobare poate avea următorii pași:

    1. Managerul angajatului care a depus raportul de cheltuieli îl aprobă.
    2. Grefierul de conturi de plată verifică chitanțele și articolele raportului de cheltuieli.
    3. Proprietarul bugetului aprobă raportul de cheltuieli.

- Adăugați mai multe elemente de aprobare, fiecare dintre acestea având un singur pas. De exemplu, puteți adăuga un element de aprobare separat pentru fiecare dintre pașii următori:

    1. Managerul angajatului aprobă raportul de cheltuieli.
    2. Proprietarul bugetului aprobă raportul de cheltuieli.
