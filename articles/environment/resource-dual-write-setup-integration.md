---
title: Configurarea Project Operations și integrarea datelor de configurare
description: Acest articol oferă informații despre configurarea și configurarea hărților cu dublă scriere Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029167"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configurarea Project Operations și integrarea datelor de configurare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol oferă informații despre integrarea cu scriere duală a Project Operations pentru entitățile de configurare și configurare.

## <a name="project-contracts-contract-lines-and-projects"></a>Contracte de proiect, linii de contracte și proiecte

Contractele de proiect, liniile de contract și proiectele sunt create în Dataverse și sincronizat cu aplicațiile de finanțare și operațiuni pentru contabilitate suplimentară. Înregistrările din aceste entități pot fi create și șterse numai în Dataverse. Cu toate acestea, atribute contabile, cum ar fi valorile implicite ale grupului de taxe pe vânzări și dimensiunile financiare, pot fi adăugate acestor înregistrări în aplicațiile de finanțare și operațiuni.

  ![Concepte pentru integrarea de contracte de proiect.](./media/1ProjectContract.jpg)

Sunt urmărite clienții potențiali, oportunitățile și cotațiile din activitatea de vânzări Dataverse și nu vă sincronizați cu aplicațiile de finanțare și operațiuni, deoarece nu există o contabilitate în aval asociată cu această activitate.

Funcționalitatea contractului de proiect în Dataverse creează o înregistrare a contractului de proiect în aplicațiile de finanțare și operațiuni folosind **Antetele contractelor de proiect (comenzi de vânzare)** hartă de masă. Salvarea unui contract de proiect în Dataverse pornește, de asemenea, crearea unei înregistrări de entitate client pentru contract de proiect. Această înregistrare este sincronizată cu aplicațiile de finanțare și operațiuni folosind **Sursa de finanțare a proiectului (msdyn\_ proiectcontractsdiviziunea de facturare)** hartă de masă. Această hartă sincronizează, de asemenea, completările, actualizările și ștergerile clienților din contractul de proiect. Procentele de facturare împărțite între clienții contractului de proiect sunt stăpânite numai în Dataverse și nu sunt sincronizate cu aplicațiile de finanțare și operațiuni.

După ce un contract de proiect este creat în Dataverse, contabilul de proiect poate actualiza atributele contabile pentru acest contract de proiect în aplicațiile de finanțare și operațiuni, accesând **Management de proiect si contabilitate** > **Contracte de proiect** > **Înființat** > **Afișați contabilitatea implicită**. Contabilul poate revizui atributele contractului de proiect operațional, cum ar fi data de livrare solicitată și suma contractului, selectând ID-ul contractului de proiect în aplicațiile de finanțare și operațiuni, care deschide înregistrarea contractului de proiect aferent în Dataverse.

Entitatea de proiect este sincronizată cu aplicațiile de finanțare și operațiuni folosind **Proiecte V2 (msdyn\_ proiecte)** hartă de masă. Contabilul de proiect poate:

  - Examinați proiecte în aplicațiile de finanțare și operațiuni accesând **Management de proiect si contabilitate** > **Toate proiectele**. 
  - Actualizați atributele contabile pentru proiect în aplicațiile de finanțare și operațiuni accesând **Management de proiect si contabilitate** > **Toate proiectele** > **Înființat** > **Afișați contabilitatea implicită**.  
  - Examinați atributele operaționale ale proiectului, cum ar fi datele estimate de început și de sfârșit, selectând ID-ul proiectului în aplicațiile de finanțare și operațiuni, care deschide înregistrarea proiectului aferentă în Dataverse.

Un proiect este asociat cu un contract de proiect prin entitatea **Linie de contract de proiect**.

Liniile de contract de proiect în Dataverse creează o regulă de facturare a contractului de proiect în aplicațiile de finanțare și operațiuni folosind **Linii de contract de proiect (detalii comandă de vânzare)** hartă de masă. Metoda de facturare definește tipul de regulă de facturare a contractului de proiect în aplicațiile de finanțare și operațiuni:

  - Liniile contractului de proiect cu o metodă de facturare a timpului și a materialului creează o regulă de facturare a timpului și a tipului de material.
  - Liniile contractuale ale metodei de facturare cu preț fix creează o regulă de facturare importantă.

Liniile de contract de proiect pot fi revizuite de contabilul de proiect în aplicațiile de finanțare și operațiuni, accesând **Management de proiect si contabilitate** > **Contracte de proiect** > **Înființat** > **Afișați contabilitatea implicită**, și revizuirea detaliilor de pe **Liniile contractuale** fila. Contabilul poate seta, de asemenea, dimensiuni financiare implicite pentru liniile de contract pentru metoda de facturare cu preț fix din această filă.

## <a name="billing-milestones"></a>Jaloane de facturare

Liniile de contract de proiect care utilizează metoda de facturare cu preț fix sunt facturate prin jaloane de facturare. Etapele de facturare sunt sincronizate pentru a proiecta tranzacțiile în cont în aplicațiile de finanțare și operațiuni prin utilizarea **Etape ale liniilor de contract de integrare a operațiunilor de proiect (msdyn\_ contractlinesscheduleofvalues)** hartă de masă.

  ![Integrarea jaloanelor de facturare.](./media/2Milestones.jpg)

Contabilul poate revizui tranzacțiile în cont și poate ajusta atributele de contabilitate pentru acele tranzacții accesând **Management de proiect și contabilitate** > **Contracte de proiect** > **Menținere** > **Tranzacții în cont** sau **Management de proiect și contabilitate** > **Toate proiectele** > **Menținere** > **Tranzacții în cont**.

Când creați pentru prima dată o etapă de facturare pentru o anumită linie de contract de proiect, sistemul creează automat un proiect de estimare a venitului cu preț fix pentru proiectul asociat cu această linie de contract. Proiectele de estimare a veniturilor cu preț fix pot fi revizuite accesând **Management de proiect și contabilitate** > **Proiecte cu estimarea veniturilor cu preț fix**.

### <a name="project-tasks"></a>Activitățile proiectului

Sarcinile proiectului sunt sincronizate cu aplicațiile de finanțare și operațiuni prin intermediul **Sarcini de proiect (msdyn\_ sarcini de proiect)** Harta tabelului doar pentru referință. Crearea, actualizarea și ștergerea operațiunilor nu sunt acceptate prin aplicațiile de finanțare și operațiuni.

  ![Integrarea sarcinilor de proiect.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Resursele proiectului

The **Rolurile resurselor proiectului** entitatea este sincronizată cu aplicațiile de finanțare și operațiuni folosind **Roluri de resurse de proiect pentru toate companiile (categorii de resurse rezervate)** Harta tabelului doar pentru referință. Deoarece rolurile de resurse în Dataverse nu sunt specifice companiei, sistemul creează automat înregistrările respective ale rolurilor de resurse specifice companiei în aplicațiile financiare și operaționale pentru toate entitățile juridice incluse în domeniul de aplicare a integrării cu dublă scriere.

![Integrarea rolurilor de resurse.](./media/5Resources.jpg)

Resursele proiectului din Operațiunile de proiect sunt menținute în Dataverse și nu sunt sincronizate cu aplicațiile de finanțare și operațiuni.

### <a name="transaction-categories"></a>Categorii de tranzacții

Categoriile de tranzacții sunt menținute în Dataverse și sincronizat cu aplicațiile de finanțare și operațiuni folosind **Categorii de tranzacții de proiect (msdyn\_ categorii de tranzacții)** hartă de masă. După ce înregistrarea categoriei de tranzacții este sincronizată, sistemul creează automat patru înregistrări de categorii partajate. Fiecare înregistrare corespunde unui tip de tranzacție în aplicațiile de finanțare și operațiuni și le leagă la înregistrarea categoriei de tranzacție.

![Integrarea categoriilor de tranzacții.](./media/4TransactionCategories.jpg)

Utilizarea categoriilor de tranzacții pentru estimări și date reale necesită ca contabilul de proiect sau administratorul de sistem să creeze categorii de proiecte corespunzătoare pentru fiecare entitate juridică. Pentru mai multe informații, consultați [Configurați categoriile de proiect](../project-accounting/configure-project-categories.md).
