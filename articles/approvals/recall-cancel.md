---
title: Reamintim intrările aprobate anterior
description: Acest subiect explică modul în care un membru al echipei de proiect poate solicita retragerea înregistrărilor privind timpul, cheltuielile și utilizarea materialelor trimise și aprobate anterior și cum un manager de proiect poate aproba sau respinge cererile de retragere.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586589"
---
# <a name="recall-previously-approved-entries"></a>Reamintim intrările aprobate anterior

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Un membru al echipei de proiect care trimite o înregistrare privind timpul, cheltuiala sau utilizarea materialului poate reaminti acea înregistrare după ce a fost aprobată. Procesul de retragere are două etape principale:

1. Un depunător cere o retragere.
2. Un autorizator aprobă cererea de retragere.

## <a name="request-a-recall"></a>Solicitați o retragere

Urmați acești pași pentru a solicita o retragere a intrărilor aprobate privind timpul, cheltuielile sau utilizarea materialelor.

1. Urmați unul dintre acești pași, în funcție de tipul de intrare pe care doriți să o reamintiți:

    - Pentru intrări de timp, accesați **Proiecte** \> **Munca mea** \> **Intrarea timpului**, și selectați toate intrările de timp pentru o combinație specifică a unui proiect și a unei sarcini. Alternativ, în grilă, selectați celulele individuale pentru timp la o anumită dată pentru un anumit proiect.
    - Pentru intrări de cheltuieli, accesați **Proiecte** \> **Munca mea** \> **Cheltuieli**, și selectați rândul pentru înregistrarea cheltuielilor de rechemat.
    - Pentru intrări privind utilizarea materialului, accesați **Proiecte** \> **Munca mea** \> **Jurnal de utilizare a materialelor**, și selectați rândul pentru intrarea de utilizare a materialului de rememorat.

2. Selectați **Retragere**. Apare o casetă de dialog de confirmare. Dacă intrările selectate privind timpul, cheltuielile sau utilizarea materialului au fost deja aprobate, vi se solicită să introduceți un motiv pentru retragere.
3. Introduceți un motiv pentru retragere apoi selectați **OK** pentru a confirma operațiunea. Sistemul trimite persoanei care a aprobat înregistrările o cerere de aprobare a retragerii.

> [!IMPORTANT]
> Nu puteți crea o cerere de retragere pentru o intrare aprobată de timp, cheltuială sau utilizare a materialului care a fost deja facturată clientului. Dacă încercați, primiți un mesaj care afirmă că înregistrarea de timp, cheltuieli sau utilizare a materialului nu poate fi reamintită deoarece a fost deja facturată. În acest caz, puteți solicita retragerea înregistrării numai dacă se utilizează o factură corectivă pentru a emite un credit complet sau o rambursare către client pe factura originală.

## <a name="approve-or-reject-a-recall-request"></a>Aprobarea sau respingerea unei solicitări de retragere

Urmați acești pași pentru a aproba sau respinge o solicitare de retragere.

1. Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.
2. Pe pagina cu lista **Aprobări**, modificați vizualizarea la **Cereri de retragere de aprobat**. Este afișată o listă de solicitări de retragere trimise.
3. Selectați una sau mai multe înregistrări, apoi selectați fie **Aprobare**, fie **Respingere**.
4. Dacă ați selectat **Aprobare**, primiți un mesaj de avertizare care explică impactul aprobării. Selectați **OK** pentru a confirma operațiunea. Solicitarea de retragere este aprobată.

    -sau-

    Dacă ați selectat **Respingere**, solicitarea de retragere este respinsă.

> [!IMPORTANT]
> Atunci când o retragere este aprobată, la fel ca atunci când este solicitată, sistemul verifică orice activitate de facturare în ceea ce privește intrările de timp, cheltuieli sau utilizare materiale. Dacă o intrare a fost deja facturată sau dacă se află pe o ciornă de factură, aprobatorul primește un mesaj de eroare care afirmă că timpul sau cheltuiala nu pot fi aprobate pentru rechemare deoarece au fost deja facturate. În acest caz, aprobatorul poate aproba retragerea numai dacă se utilizează o factură corectivă pentru a emite un credit complet sau o rambursare către client pe factura originală.

## <a name="impact-of-a-recall-request"></a>Impactul unei solicitări de retragere

Atunci când se retrage o aprobare, există atât un impact operațional, cât și un impact financiar.

### <a name="operational-impact"></a>Impactul operațional

Dacă se aprobă o solicitare de retragere, înregistrarea de aprobare este marcată **Respinsă**. Starea intrării este schimbată în oricare **Întors** sau **Respins**, în funcție de faptul că este o intrare de timp sau o intrare de cheltuială sau de utilizare a materialului.

Membrul echipei de proiect poate vizualiza intrările, edita și apoi retrimite intrări sau poate șterge complet intrări.

Dacă o solicitare de retragere este respinsă, starea înregistrării rămâne **Aprobată**, iar înregistrarea nu poate fi editată de membrul echipei de proiect sau de aprobatorul proiectului.

### <a name="financial-impact"></a>Impactul financiar

Dacă se aprobă o solicitare de retragere, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:

- Câmpul **Stare Ajustare** este actualizat la **Ajustat**.
- Câmpul **Stare Facturare** este actualizat la **Anulat**.

Apoi, intrările de inversare sunt create în tabelul Valori reale. Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale. Singurele valori peste care nu se copiază sunt valorile cantitative. Aceste valori sunt inversate în schimb. Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**. Câmpul **Stare Ajustare** de pe valorile reale inversate este setat la **Neajustabil**, iar câmpul **Stare Facturare** este setat la **Anulat.** Din cauza acestor modificări, restanțele înregistrare de cheltuieli și venituri de pe proiect nu vor mai duce la pentru sumele pe care le reprezintă aceste date reale.

Dacă o cerere de retragere este respinsă, nu există niciun impact financiar asupra proiectului.

## <a name="changes-to-time-entry-records"></a>Modificări la înregistrări de intrări de timp

Următoarea ilustrație arată modificările care apar pentru intrările de timp aprobate și înregistrările de aprobare corespunzătoare atunci când sunt rechemate.

![Tranziții de stare de intrare în timp.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Modificări ale înregistrărilor privind cheltuielile și utilizarea materialelor

Următoarea ilustrație arată modificările care apar pentru înregistrările de cheltuieli aprobate și de utilizare a materialelor și înregistrările de aprobare corespunzătoare atunci când sunt rechemate.

![Tranziții de stare de intrare a cheltuielilor.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
