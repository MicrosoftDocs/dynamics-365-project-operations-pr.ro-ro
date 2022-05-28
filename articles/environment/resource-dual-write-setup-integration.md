---
title: Configurarea Project Operations și integrarea datelor de configurare
description: Acest subiect oferă informații despre setarea și configurarea de hărți cu scriere duală în Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586911"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configurarea Project Operations și integrarea datelor de configurare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect oferă informații despre integrarea cu scriere duală a Project Operations pentru entități de setare și configurare.

## <a name="project-contracts-contract-lines-and-projects"></a>Contracte de proiect, linii de contracte și proiecte

Contractele de proiect, liniile de contract și proiectele sunt create în Dataverse și sincronizat cu aplicațiile Finanțe și Operațiuni pentru contabilitate suplimentară. Înregistrările din aceste entități pot fi create și șterse numai în Dataverse. Cu toate acestea, atribute contabile, cum ar fi valorile implicite ale grupului de taxe pe vânzări și dimensiunile financiare, pot fi adăugate la aceste înregistrări în aplicațiile Finanțe și Operațiuni.

  ![Concepte pentru integrarea de contracte de proiect.](./media/1ProjectContract.jpg)

Sunt urmărite clienții potențiali pentru activități de vânzări, oportunitățile și cotațiile Dataverse și nu vă sincronizați cu aplicațiile Finance and Operations deoarece nu există o contabilitate în aval asociată cu această activitate.

Funcționalitatea contractului de proiect în Dataverse creează o înregistrare a contractului de proiect în aplicațiile Finanțe și Operațiuni folosind **Antete contract de proiect (comenzi de vânzare)** hartă de masă. Salvarea unui contract de proiect în Dataverse pornește, de asemenea, crearea unei înregistrări de entitate client pentru contract de proiect. Această înregistrare este sincronizată cu aplicațiile Finanțe și Operațiuni folosind **Sursa de finanțare a proiectului (msdyn\_ proiectcontractsdiviziunea de facturare)** hartă de masă. Această hartă sincronizează, de asemenea, completările, actualizările și ștergerile clienților din contractul de proiect. Procentele de facturare împărțite între clienții contractului de proiect sunt stăpânite numai în Dataverse și nu sunt sincronizate cu aplicațiile Finance and Operations.

După ce un contract de proiect este creat în Dataverse, contabilul de proiect poate actualiza atributele contabile pentru acest contract de proiect în aplicațiile Finanțe și operațiuni, accesând **Management de proiect si contabilitate** > **Contracte de proiect** > **Înființat** > **Afișați contabilitatea implicită**. Contabilul poate revizui atributele contractului de proiect operațional, cum ar fi data de livrare solicitată și suma contractului, selectând ID-ul contractului de proiect în aplicațiile Finanțe și operațiuni, care deschide înregistrarea contractului de proiect aferent în Dataverse.

Entitatea de proiect este sincronizată cu aplicațiile Finanțe și Operațiuni folosind **Proiecte V2 (msdyn\_ proiecte)** hartă de masă. Contabilul de proiect poate:

  - Examinați proiecte în aplicațiile Finanțe și Operațiuni accesând **Management de proiect si contabilitate** > **Toate proiectele**. 
  - Actualizați atributele contabile pentru proiect în aplicațiile Finanțe și operațiuni accesând **Management de proiect si contabilitate** > **Toate proiectele** > **Înființat** > **Afișați contabilitatea implicită**.  
  - Examinați atributele operaționale ale proiectului, cum ar fi datele estimate de început și de sfârșit, selectând ID-ul proiectului în aplicațiile Finanțe și operațiuni, care deschide înregistrarea proiectului aferentă în Dataverse.

Un proiect este asociat cu un contract de proiect prin entitatea **Linie de contract de proiect**.

Liniile de contract de proiect în Dataverse creează o regulă de facturare a contractului de proiect în aplicațiile Finanțe și operațiuni folosind **Linii de contract de proiect (detalii comandă de vânzare)** hartă de masă. Metoda de facturare definește tipul de regulă de facturare a contractului de proiect în aplicațiile Finance and Operations:

  - Liniile contractului de proiect cu o metodă de facturare a timpului și a materialului creează o regulă de facturare a timpului și a tipului de material.
  - Liniile contractuale ale metodei de facturare cu preț fix creează o regulă de facturare importantă.

Liniile de contract de proiect pot fi revizuite de contabilul de proiect în aplicațiile Finanțe și operațiuni, accesând **Management de proiect si contabilitate** > **Contracte de proiect** > **Înființat** > **Afișați contabilitatea implicită**, și revizuirea detaliilor de pe **Liniile contractuale** fila. Contabilul poate seta, de asemenea, dimensiuni financiare implicite pentru liniile de contract pentru metoda de facturare cu preț fix din această filă.

## <a name="billing-milestones"></a>Jaloane de facturare

Liniile de contract de proiect care utilizează metoda de facturare cu preț fix sunt facturate prin jaloane de facturare. Etapele de facturare sunt sincronizate pentru a proiecta tranzacțiile în cont în aplicațiile Finanțe și Operațiuni prin utilizarea **Etape ale liniilor de contract de integrare a operațiunilor de proiect (msdyn\_ contractlinesscheduleofvalues)** hartă de masă.

  ![Integrarea jaloanelor de facturare.](./media/2Milestones.jpg)

Contabilul poate revizui tranzacțiile în cont și poate ajusta atributele de contabilitate pentru acele tranzacții accesând **Management de proiect și contabilitate** > **Contracte de proiect** > **Menținere** > **Tranzacții în cont** sau **Management de proiect și contabilitate** > **Toate proiectele** > **Menținere** > **Tranzacții în cont**.

Când creați pentru prima dată o etapă de facturare pentru o anumită linie de contract de proiect, sistemul creează automat un proiect de estimare a venitului cu preț fix pentru proiectul asociat cu această linie de contract. Proiectele de estimare a veniturilor cu preț fix pot fi revizuite accesând **Management de proiect și contabilitate** > **Proiecte cu estimarea veniturilor cu preț fix**.

### <a name="project-tasks"></a>Activitățile proiectului

Sarcinile proiectului sunt sincronizate cu aplicațiile Finanțe și Operațiuni prin intermediul **Sarcini de proiect (msdyn\_ sarcini de proiect)** Harta tabelului doar pentru referință. Crearea, actualizarea și ștergerea operațiunilor nu sunt acceptate prin aplicațiile Finance and Operations.

  ![Integrarea sarcinilor de proiect.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Resursele proiectului

The **Rolurile resurselor proiectului** entitatea este sincronizată cu aplicațiile Finance and Operations folosind **Roluri de resurse de proiect pentru toate companiile (categorii de resurse rezervate)** Harta tabelului doar în scop de referință. Deoarece rolurile de resurse în Dataverse nu sunt specifice companiei, sistemul creează automat înregistrările respective ale rolurilor de resurse specifice companiei în aplicațiile Finance and Operations pentru toate entitățile juridice incluse în domeniul de aplicare a integrării cu dublă scriere.

![Integrarea rolurilor de resurse.](./media/5Resources.jpg)

Resursele proiectului din Operațiunile de proiect sunt menținute în Dataverse și nu sunt sincronizate cu aplicațiile Finance and Operations.

### <a name="transaction-categories"></a>Categorii de tranzacții

Categoriile de tranzacții sunt menținute în Dataverse și sincronizat cu aplicațiile Finance and Operations folosind **Categorii de tranzacții de proiect (msdyn\_ categorii de tranzacții)** hartă de masă. După ce înregistrarea categoriei de tranzacții este sincronizată, sistemul creează automat patru înregistrări de categorii partajate. Fiecare înregistrare corespunde unui tip de tranzacție în aplicațiile Finance and Operations și le leagă la înregistrarea categoriei de tranzacție.

![Integrarea categoriilor de tranzacții.](./media/4TransactionCategories.jpg)

Utilizarea categoriilor de tranzacții pentru estimări și date reale necesită ca contabilul de proiect sau administratorul de sistem să creeze categorii de proiecte corespunzătoare pentru fiecare entitate juridică. Pentru mai multe informații, consultați [Configurați categoriile de proiect](../project-accounting/configure-project-categories.md).
