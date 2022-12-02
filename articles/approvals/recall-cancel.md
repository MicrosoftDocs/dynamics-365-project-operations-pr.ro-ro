---
title: Retragerea intrărilor aprobate anterior
description: Acest articol explică modul în care un membru al echipei de proiect poate solicita retragerea înregistrărilor privind timpul, cheltuielile și utilizarea materialelor trimise și aprobate anterior și cum un manager de proiect poate aproba sau respinge cererile de retragere.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930379"
---
# <a name="recall-previously-approved-entries"></a>Retragerea intrărilor aprobate anterior

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Un membru al echipei de proiect care depune o intrare de timp, cheltuieli sau utilizare a materialelor poate retrage acea intrare după ce a fost aprobată. Procesul de retragere are doi pași principali:

1. Un depunător cere o retragere.
2. Un aprobator aprobă retragerea solicitării.

## <a name="request-a-recall"></a>Solicitați o retragere

Urmați acești pași pentru a solicita o retragere a intrărilor de timp, cheltuieli sau utilizare a materialelor aprobate.

1. Urmați unul dintre acești pași, în funcție de tipul de intrare pe care doriți să o retrageți:

    - Pentru intrările de timp, accesați **Proiecte** \> **Lucrările mele** \> **Intrare de timp** și selectați toate intrările de timp pentru o anumită combinație a unui proiect și a unei activități. Alternativ, în grilă, selectați celulele individuale pentru timp la o anumită dată pentru un anumit proiect.
    - Pentru intrările de cheltuieli, accesați **Proiecte** \> **Lucrările mele** \> **Cheltuieli** și selectați rândul pentru intrarea de cheltuieli de retras.
    - Pentru intrările de utilizare a materialelor, accesați **Proiecte** \> **Lucrările mele** \> **Cheltuieli** și selectați rândul pentru intrarea de utilizare a materialelor de retras.

2. Selectați **Retragere**. Apare o casetă de dialog de confirmare. Dacă intrările de timp, cheltuieli sau utilizare a materialelor selectate au fost deja aprobate, vi se solicită să introduceți un motiv pentru retragere.
3. Introduceți un motiv pentru retragere apoi selectați **OK** pentru a confirma operațiunea. Sistemul trimite persoanei care a aprobat înregistrările o cerere de aprobare a retragerii.

> [!IMPORTANT]
> Nu puteți crea o solicitare de retragere pentru o intrare de timp, cheltuieli și utilizare a materialelor aprobată, care a fost deja facturată clientului. Dacă încercați, veți primi un mesaj care afirmă că intrarea de timp, cheltuieli sau utilizare a materialelor nu poate fi retrasă, deoarece a fost deja facturată. În acest caz, puteți solicita o retragere a intrării numai dacă se utilizează o factură corectivă pentru a emite o creditare completă sau o rambursare către client pe factura originală.

## <a name="approve-or-reject-a-recall-request"></a>Aprobarea sau respingerea unei solicitări de retragere

Urmați acești pași pentru a aproba sau respinge o solicitare de retragere.

1. Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.
2. Pe pagina cu lista **Aprobări**, modificați vizualizarea la **Cereri de retragere de aprobat**. Este afișată o listă de solicitări de retragere trimise.
3. Selectați una sau mai multe înregistrări, apoi selectați fie **Aprobare**, fie **Respingere**.
4. Dacă ați selectat **Aprobare**, primiți un mesaj de avertizare care explică impactul aprobării. Selectați **OK** pentru a confirma operațiunea. Solicitarea de retragere este aprobată.

    -sau-

    Dacă ați selectat **Respingere**, solicitarea de retragere este respinsă.

> [!IMPORTANT]
> Atunci când o retragere este aprobată, ca și atunci când este retrasă, sistemul verifică orice activitate de facturare pe intrările de timp, cheltuieli sau utilizare a materialelor. Dacă o intrare a fost deja facturată sau dacă este pe o schiță de factură, aprobatorul primește un mesaj de eroare care afirmă că timpul sau cheltuiala nu pot fi aprobate pentru retragere deoarece au fost deja facturate. În acest caz, aprobatorul poate aproba retragerea numai dacă se utilizează o factură corectivă pentru a emite o creditare completă sau o rambursare către client pe factura originală.

## <a name="impact-of-a-recall-request"></a>Impactul unei solicitări de retragere

Atunci când se retrage o aprobare, există atât un impact operațional, cât și un impact financiar.

### <a name="operational-impact"></a>Impactul operațional

Dacă se aprobă o solicitare de retragere, înregistrarea de aprobare este marcată **Respinsă**. Starea intrării se modifică fie în **Returnată**, fie în **Respinsă** și depinde dacă este o intrare de timp sau o înregistrare de cheltuieli.

Membrul echipei de proiect poate vizualiza intrările, poate edita și apoi retrimite intrările sau poate șterge complet intrările.

Dacă o solicitare de retragere este respinsă, starea înregistrării rămâne **Aprobată**, iar înregistrarea nu poate fi editată de membrul echipei de proiect sau de aprobatorul proiectului.

### <a name="financial-impact"></a>Impactul financiar

Dacă se aprobă o solicitare de retragere, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:

- Câmpul **Stare Ajustare** este actualizat la **Ajustat**.
- Câmpul **Stare Facturare** este actualizat la **Anulat**.

Apoi, intrările de inversare sunt create în tabelul Valori reale. Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale. Singurele valori peste care nu se copiază sunt valorile cantitative. Aceste valori sunt inversate în schimb. Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**. Câmpul **Stare Ajustare** de pe valorile reale inversate este setat la **Neajustabil**, iar câmpul **Stare Facturare** este setat la **Anulat.** Din cauza acestor modificări, restanțele înregistrare de cheltuieli și venituri de pe proiect nu vor mai duce la pentru sumele pe care le reprezintă aceste date reale.

Dacă o cerere de retragere este respinsă, nu există niciun impact financiar asupra proiectului.

## <a name="changes-to-time-entry-records"></a>Modificări la înregistrări de intrări de timp

Următoarea ilustrație arată modificările care apar pentru intrările de timp aprobate și înregistrările de aprobare corespunzătoare atunci când acestea sunt retrase.

![Tranziții de stare pentru Intrarea de timp.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Modificări la înregistrările de intrare de utilizare a materialelor

Următoarea ilustrație arată modificările care apar pentru intrările de cheltuieli și utilizare a materialelor aprobate și înregistrările de aprobare corespunzătoare atunci când acestea sunt retrase.

![Tranziții de stare pentru Intrarea de cheltuieli.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
