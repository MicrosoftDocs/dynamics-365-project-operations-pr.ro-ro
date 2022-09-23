---
title: Integrarea gestionării cheltuielilor
description: Acest articol oferă informații despre integrarea raportului de cheltuieli în Operațiuni de proiect folosind scriere dublă.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da37adcf63a10b9f245283d377e70fd08b3aa9c5
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528020"
---
# <a name="expense-management-integration"></a>Integrarea gestionării cheltuielilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol oferă informații despre integrarea rapoartelor de cheltuieli în Operațiunile de proiect [implementarea integrală a cheltuielilor](../expense/expense-overview.md) folosind dual-write.

## <a name="expense-categories"></a>Categorii de cheltuieli

Într-o implementare completă a cheltuielilor, categoriile de cheltuieli sunt create și menținute în aplicațiile de finanțare și operațiuni. Pentru a crea o nouă categorie de cheltuieli, parcurgeți următorii pași:

1. În Microsoft Dataverse creeați o categorie **Tranzacție**. Integrarea cu dublă scriere va sincroniza această categorie de tranzacții cu aplicațiile de finanțare și operațiuni. Pentru mai multe informații, consultați [Configurarea categoriilor de proiecte](/dynamics365/project-operations/project-accounting/configure-project-categories) și [Configurarea Project Operations și integrarea datelor de configurare](resource-dual-write-setup-integration.md). Ca rezultat al acestei integrări, sistemul creează patru înregistrări de categorii partajate în aplicațiile de finanțare și operațiuni.
2. În Finanțe, accesați **Gestionarea cheltuielilor** > **Configurare** > **Categorii partajate** și selectați o categorie partajată cu o clasă de tranzacție **Cheltuieli**. Setați parametrul **Poate fi folosit în Cheltuieli** la **True** și definiți tipul de cheltuială de utilizat.
3. Folosind această înregistrare de categorie partajată, creați o nouă categorie de cheltuieli accesând **Gestionarea cheltuielilor** > **Configurare** > **Categorii de cheltuieli** și selectând **Nou**. Când înregistrarea este salvată, scrierea duală utilizează harta tabelului, **Entitatea privind exportul categoriilor de cheltuieli în proiectul de integrare Project Operations (msdyn\_expensecategories)** pentru a sincroniza această înregistrare cu Dataverse.

  ![Integrarea categoriilor de cheltuieli.](./media/DW6ExpenseCategories.png)

Categoriile de cheltuieli din aplicațiile de finanțare și operațiuni sunt specifice companiei sau entității juridice. Există înregistrări separate, corespunzătoare, specifice entității juridice Dataverse. Atunci când un manager de proiect estimează cheltuielile, nu poate selecta categoriile de cheltuieli care au fost create pentru un proiect care este deținut de o companie diferită de compania care deține proiectul la care lucrează. 

## <a name="expense-reports"></a>Rapoarte de cheltuieli

Rapoartele de cheltuieli sunt create și aprobate în aplicațiile de finanțare și operațiuni. Pentru mai multe informații, consultați [Creați și procesați rapoarte de cheltuieli în Dynamics 365 Project Operations](/training/modules/create-process-expense-reports/). După ce raportul de cheltuieli este aprobat de managerul de proiect este afișat în registrul general. În Project Operations, liniile de raportare a cheltuielilor legate de proiect sunt înregistrate folosind reguli speciale de publicare:

  - Costul aferent proiectului (inclusiv impozitul nerecuperabil) nu este înregistrat imediat în contul de cost al proiectului în registrul general, ci este înregistrat în contul de integrare a cheltuielilor. Acest cont este configurat în **Management de proiect și contabilitate** > **Configurare** > **Management de proiect și parametrii contabili**, fila **Project Operations pe Dynamics 365 Customer engagement**.
  - Scrierea duală se sincronizează la Dataverse folosind harta de tabel **Entitatea privind exportul de cheltuieli în proiectul de integrare Project Operations (msdyn\_expenses)**.
  - Subregistrul de impozit, subregistrul furnizorului și alte înregistrări financiare sunt înregistrate după caz, în momentul înregistrării raportului de cheltuieli.

  ![Integrarea rapoartelor de cheltuieli.](./media/DW6ExpenseReports.png)

Când o înregistrare este scrisă în entitatea **Cheltuieli** în Dataverse, sistemul declanșează procesul automatizat de aprobare a înregistrării. Dacă este necesar, starea procesului de aprobare automată poate fi revizuită în Dataverse accesând **Setări avansate** > **Sistem** > **Procese de sistem**. După finalizarea aprobării, înregistrările clasei tranzacțiilor de cheltuieli sunt create în entitatea **Actualități**.

Datele reale legate de cheltuieli sunt apoi procesate utilizând harta tabelului cu scriere duală **Valori reale privind integrarea în Project Operations (msdyn\_actuals)**. Pentru mai multe informații, consultați [Estimări de proiect și valori reale](resource-dual-write-estimates-actuals.md).

Procesul periodic, **Import din etapă** creează linii de jurnal legate de rapoarte de cheltuieli în jurnalul de integrare Project Operations. Contul compensat este implicit cu contul de integrare a cheltuielilor. Jurnalul de integrare Postare șterge soldul contului pentru tranzacția de cheltuieli și mută suma cheltuielilor în contul de cost al proiectului. Sistemul creează, de asemenea, tranzacții subregistru de proiect în scopuri de facturare în aval și de recunoaștere a veniturilor.
