---
title: Configurarea Project Operations și integrarea datelor de configurare
description: Acest subiect oferă informații despre setarea și configurarea de hărți cu scriere duală în Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986551"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configurarea Project Operations și integrarea datelor de configurare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect oferă informații despre integrarea cu scriere duală a Project Operations pentru entități de setare și configurare.

## <a name="project-contracts-contract-lines-and-projects"></a>Contracte de proiect, linii de contracte și proiecte

Contractele de proiect, liniile de contract și proiectele sunt create în Dataverse și sincronizate la aplicații Finance and Operations pentru contabilitate suplimentară. Înregistrările din aceste entități pot fi create și șterse numai în Dataverse. Cu toate acestea, atributele de contabilitate, cum ar fi valorile implicite ale grupului de impozite pe vânzări și dimensiunile financiare, pot fi adăugate acestor înregistrări în aplicații Finance and Operations.

  ![Concepte pentru integrarea de contracte de proiect.](./media/1ProjectContract.jpg)

Sunt urmărite activitățile de vânzare pentru clienți potențiali, oportunitățile și ofertele în Dataverse și nu se sincronizează cu aplicații Finance and Operations deoarece nu există nicio contabilitate în aval asociată cu această activitate.

Funcționalitatea contractului de proiect în Dataverse creează o înregistrare a contractului de proiect în aplicații Finance and Operations folosind harta tabelului **Anteturile contractului de proiect (salesorders)**. Salvarea unui contract de proiect în Dataverse pornește, de asemenea, crearea unei înregistrări de entitate client pentru contract de proiect. Această înregistrare este sincronizată cu aplicații Finance and Operations folosind harta de tabel **Sursa de finanțare a proiectului (msdyn\_projectcontractsplitbillingrules)**. Această hartă sincronizează, de asemenea, completările, actualizările și ștergerile clienților din contractul de proiect. Procentele de facturare împărțite între clienții de contract de proiect sunt stăpânite numai în Dataverse și nu sunt sincronizate cu aplicații Finance and Operations.

După crearea unui contract de proiect în Dataverse, contabilul de proiect poate actualiza atributele de contabilitate pentru acest contract de proiect în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Contracte de proiect** > **Configurare** > **Afișare contabilitate implicită**. Contabilul poate revizui atributele operaționale de contract de proiect, cum ar fi data de livrare solicitată și valoarea contractului, selectând ID-ul contractului de proiect în aplicații Finance and Operations care deschid înregistrarea contractului de proiect aferent în Dataverse.

Entitatea de proiect este sincronizată cu aplicații Finance and Operations folosind harta de tabel **Proiecte V2 (msdyn\_projects)**. Contabilul de proiect poate:

  - Examina proiectele în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Toate proiectele**. 
  - Actualizați atributele de contabilitate pentru proiect în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Toate proiectele** > **Configurare** > **Afișare contabilitate implicită**.  
  - Examinați atributele operaționale de proiect, cum ar fi datele estimate de început și de sfârșit, selectând ID-ul de proiect în aplicații Finance and Operations care deschide înregistrarea proiectului aferent în Dataverse.

Un proiect este asociat cu un contract de proiect prin entitatea **Linie de contract de proiect**.

Liniile de contract de proiect în Dataverse creează o regulă de facturare a contractului de proiect în aplicații Finance and Operations folosind harta tabelului **Liniile contractului de proiect (salesorderdetails)**. Metoda de facturare definește tipul regulii de facturare a contractului de proiect în aplicații Finance and Operations:

  - Liniile contractului de proiect cu o metodă de facturare a timpului și a materialului creează o regulă de facturare a timpului și a tipului de material.
  - Liniile contractuale ale metodei de facturare cu preț fix creează o regulă de facturare importantă.

Liniile de contract de proiect pot fi revizuite de către contabilul de proiect în aplicații Finance and Operations accesând **Management de proiect și contabilitate** > **Contracte de proiect** > **Configurat** > **Afișare contabilitate implicită** și prin examinarea detaliilor de pe fila **Linii de contract**. Contabilul poate, de asemenea, să stabilească dimensiuni financiare implicite pentru liniile de contract ale metodei de facturare cu preț fix în această filă.

## <a name="billing-milestones"></a>Jaloane de facturare

Liniile de contract de proiect care utilizează metoda de facturare cu preț fix sunt facturate prin jaloane de facturare. Jaloanele de facturare sunt sincronizate pentru a proiecta tranzacții în cont în aplicații Finance and Operations utilizând harta de tabel **Integrare Project Operations de jaloane linie de contract (msdyn\_contractlinescheduleofvalues)**.

  ![Integrarea jaloanelor de facturare.](./media/2Milestones.jpg)

Contabilul poate revizui tranzacțiile în cont și poate ajusta atributele de contabilitate pentru acele tranzacții accesând **Management de proiect și contabilitate** > **Contracte de proiect** > **Menținere** > **Tranzacții în cont** sau **Management de proiect și contabilitate** > **Toate proiectele** > **Menținere** > **Tranzacții în cont**.

Când creați pentru prima dată o etapă de facturare pentru o anumită linie de contract de proiect, sistemul creează automat un proiect de estimare a venitului cu preț fix pentru proiectul asociat cu această linie de contract. Proiectele de estimare a veniturilor cu preț fix pot fi revizuite accesând **Management de proiect și contabilitate** > **Proiecte cu estimarea veniturilor cu preț fix**.

### <a name="project-tasks"></a>Activitățile proiectului

Sarcinile de proiect sunt sincronizate cu aplicații Finance and Operations prin harta de tabel **Sarcini de proiect (msdyn\_projecttasks)** doar în scop de referință. Operațiile de creare, actualizare și ștergere nu sunt acceptate prin aplicații Finance and Operations.

  ![Integrarea sarcinilor de proiect.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Resursele proiectului

Entitatea **Roluri de resurse de proiect** este sincronizată cu aplicații Finance and Operations folosind harta tabelului **Roluri de resurse de proiect pentru toate companiile (bookableresourcecategories)** doar în scop de referință. Deoarece rolurile de resurse în Dataverse nu sunt specifice companiei, sistemul creează automat înregistrări specifice rolurilor de resurse specifice companiei în aplicații Finance and Operations în mod automat pentru toate entitățile juridice incluse în domeniul integrării cu scriere duală.

![Integrarea rolurilor de resurse.](./media/5Resources.jpg)

Resursele proiectului în Project Operations sunt menținute în Dataverse și nu sunt sincronizate cu aplicații Finance and Operations.

### <a name="transaction-categories"></a>Categorii de tranzacții

Categoriile de tranzacții sunt menținute în Dataverse și sunt sincronizate cu aplicații Finance and Operations folosind harta de tabel **Categorii de tranzacții de proiect (msdyn\_transactioncategories)**. După ce înregistrarea categoriei de tranzacții este sincronizată, sistemul creează automat patru înregistrări de categorii partajate. Fiecare înregistrare corespunde unui tip de tranzacție în aplicații Finance and Operations și le leagă de înregistrarea categoriei de tranzacții.

![Integrarea categoriilor de tranzacții.](./media/4TransactionCategories.jpg)

Utilizarea categoriilor de tranzacții pentru estimări și date reale necesită ca contabilul de proiect sau administratorul de sistem să creeze categorii de proiecte corespunzătoare pentru fiecare entitate juridică. Pentru mai multe informații, consultați [Configurați categoriile de proiect](../project-accounting/configure-project-categories.md).
