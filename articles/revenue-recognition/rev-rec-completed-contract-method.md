---
title: Gestionarea estimărilor de venituri
description: Acest subiect oferă informații despre cum să lucrați cu estimările de venituri pentru proiecte.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531525"
---
# <a name="manage-revenue-estimates"></a>Gestionarea estimărilor de venituri

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Puteți crea, calcula, posta, inversa sau elimina estimările veniturilor. Puteți face acest lucru fie manual, fie utilizând un proces periodic. Acest subiect oferă informații despre cum să lucrați cu estimările de venituri pentru proiecte.

### <a name="manage-revenue-estimates-manually"></a>Gestionarea manuală a estimărilor de venituri

În cadrul proiectului de estimare a veniturilor cu preț fix sau pagina **Interogare estimativă** (**Management de proiect și contabilitate** > **Rapoarte și anchete** > **Estimări de anchete și rapoarte**), selectați **Estimări**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Gestionați estimările veniturilor utilizând un proces periodic

Accesați **Management de proiect și contabilitate** > **Periodic** > **Estimări** și selectați procesul corespunzător.

## <a name="create-a-revenue-estimate"></a>Creați o estimare a veniturilor

Parcurgeți următorii pași pentru a crea o estimare de venituri. 

1. Accesați **Management de proiect și contabilitate** > **Periodic** > **Estimări**.
2. Selectați **Nou**. Pe pagina **Estimarea creării**, selectați următorii parametri:

   - **Codul perioadei**: Acest cod determină frecvența cu care sunt postate estimările.
   - **Data estimării**: Data procesării devizului.
   - **Continuu**: Bifați această casetă de selectare pentru a crea estimări numai dacă estimările au fost înregistrate în perioada anterioară sau dacă estimarea este prima estimare care a fost creată. Dacă nu este selectat, estimările sunt create chiar dacă estimările nu au fost înregistrate în perioada anterioară.
   - **Metoda costului de finalizare**: Definiți cum să estimați lucrările rămase ale proiectului. Pentru mai multe informații, consultați [Costul finalizării metodelor](cost-complete-methods.md).
   - **Metoda de finalizare**: Selectați o metodă de finalizare din următoarele opțiuni:
     - **Automat**: Procentul de finalizare este calculat automat și pe baza liniilor de cost incluse în calcul. Șablonul de costuri definește liniile de cost care sunt incluse.
     - **Manual**: Procentul de finalizare este egal cu procentul de finalizare al ultimei estimări. După crearea estimării, puteți schimba **Calcul manual** pe pagina **Estimări**.
     - **Din șablonul de cost**: O combinație între metodele automate și manuale. Această opțiune este setată automat sau manual, în funcție de valoarea implicită din șablonul de cost.
   - **Model de prognoză**: Selectați un model de prognoză pentru estimare.
   - **Imprimați lista estimărilor**: Creați și afișați o listă estimativă. Lista conține starea funcției curente. Puteți imprima orice avertismente despre estimare în raport. Următoarele condiții determină apariția avertismentelor în lista estimativă:
     - Un procent de finalizare mai mare de 100%.
     - Un procent de finalizare mai mic de zero procente.
     - O sumă negativă în coloana **De terminat**.
     - O estimare fără suma corespondentă a contractului.
     - O estimare fără estimare a costurilor atașate.
   - **Afișați Infolog**: Selectați această opțiune pentru a primi un mesaj care conține informații despre proiectele estimate care au fost procesate la executarea operațiunii.


## <a name="post-wip-or-accruals"></a>Postează WIP sau acumulări

După evaluarea estimărilor, acestea sunt menținute, scăzute sau crescute. Puteți posta WIP atunci când lucrați cu principiul de evaluare **Contract finalizat** sau afișați acumularile atunci când lucrați cu principiul de evaluare **Procent finalizat**.
  
Starea perioadei estimative se schimbă de la **Creată** la **Postată**.

## <a name="reverse-wip-or-accruals"></a>Reversul WIP sau acumulări

Utilizați opțiunea inversă pentru a credita WIP sau acumularile deja înregistrate, apoi creați estimări pentru perioada respectivă.

> [!NOTE]
> Pentru a inversa o perioadă care se află între alte perioade, inversați perioadele de estimare necesare și apoi repostați-le. Deoarece toate perioadele ulterioare depind de estimările din perioada anterioară, nu săriți peste perioade.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Eliminați proiectul estimativ și terminați proiectul

Ultimul pas al procesului de estimare este eliminarea proiectului de estimare și încheierea proiectului cu preț fix atunci când procentul de finalizare atinge 100%.

Au loc următoarele atunci când rulați eliminarea:

- Pentru un proiect cu preț fix cu un contract finalizat, valorile WIP se elimină din conturile de sold și se înregistrează în conturile de profit și pierdere.
- Pentru un proiect cu preț fix cu un procent finalizat, acumulările sunt eliminate din conturile de profit și pierdere.

Estimarea schimbă starea la **Eliminat**.

> [!NOTE]
> În cazuri speciale, procentul se poate extinde dincolo de 100%. Când se întâmplă acest lucru, reduceți procentul de finalizare utilizând **Setați costul pentru a finaliza metoda zero** pentru a ajunge la 100 la sută.

## <a name="reverse-elimination"></a>Eliminare inversă

1. Accesați **Management de proiect și contabilitate** > **Periodic** > **Estimări** > **Eliminare inversată**. 
2. Pe panoul de acțiune, pe fila **Proces**, în grupul **Menţine**, selectați **Estimare**. 
3. Selectați **Eliminare inversă**.

Utilizați această pagină pentru a inversa toate eliminările cu o dată estimată specificată și cu o stare estimată de **Eliminat**. Starea tranzacției se schimbă după ce selectați câmpurile corespunzătoare.

De asemenea, acest lucru schimbă automat starea proiectului în **În curs** dacă etapa proiectului este setată la finalizată. Starea estimată a perioadei proiectului revine la **Postat**.
