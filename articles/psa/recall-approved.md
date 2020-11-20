---
title: Retragerea înregistrărilor aprobate de timp sau cheltuieli
description: Acest subiect oferă informații despre cum să retrageți o operațiune de timp sau cheltuieli aprobată anterior.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120558"
---
# <a name="recall-approved-time-or-expense-entries"></a>Retragerea înregistrărilor aprobate de timp sau cheltuieli

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un membru al echipei de proiect sau o altă persoană care depune o înregistrare de timp sau cheltuială poate retrage acea înregistrare de timp sau cheltuială după ce a fost aprobată. Procesul de retragere a unei înregistrări de timp sau cheltuieli aprobate are două etape:

1. Un depunător cere o retragere.
2. Un aprobator aprobă retragerea.

## <a name="request-a-recall"></a>Solicitați o retragere

Urmați acești pași pentru a solicita o retragere a unei înregistrări de timp sau cheltuieli aprobate.

1. Pentru înregistrările de timp, accesați **Proiecte**\> **Munca mea** \> **Înregistrare timp**.

    -sau-

    Pentru înregistrările de cheltuieli, accesați **Proiecte**\> **Munca mea** \> **Cheltuieli**.

2. Pentru înregistrările de timp, selectați toate înregistrările de timp pentru o anumită combinație a unui proiect și a unei activități. Alternativ, în grilă, selectați celulele individuale pentru timp la o anumită dată pentru un anumit proiect.

    -sau-

    Pentru înregistrările de cheltuieli, selectați rândul pentru înregistrarea de cheltuieli de retras.

3. Selectați **Retragere**. Apare o casetă de dialog de confirmare. Dacă înregistrările de timp și cheltuieli selectate au fost deja aprobate, vi se solicită să introduceți un motiv pentru retragere.
4. Introduceți un motiv pentru retragere apoi selectați **OK** pentru a confirma operațiunea. Sistemul trimite persoanei care a aprobat înregistrările o cerere de aprobare a retragerii.

> [!NOTE]
> Deși înregistrările aprobate de timp și cheltuieli pot fi retrase dacă un timp sau o cheltuială aprobată a fost deja facturată clientului, nu se poate crea o solicitare de retragere. Un utilizator care încearcă să creeze o solicitare de retragere va primi un mesaj care afirmă că timpul sau cheltuiala nu poate fi retras/ă, deoarece a fost deja facturat/ă.

## <a name="approve-or-reject-a-recall-request"></a>Aprobarea sau respingerea unei solicitări de retragere

Urmați acești pași pentru a aproba sau respinge o solicitare de retragere.

1. Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.
2. Pe pagina cu lista **Aprobări**, modificați vizualizarea la **Cereri de retragere de aprobat**. Este afișată o listă de solicitări de retragere trimise.
3. Selectați una sau mai multe înregistrări, apoi selectați fie **Aprobare**, fie **Respingere**.
4. Dacă ați selectat **Aprobare**, primiți un mesaj de avertizare care explică impactul aprobării. Selectați **OK** pentru a confirma operațiunea. Solicitarea de retragere este aprobată

    -sau-

    Dacă ați selectat **Respingere**, solicitarea de retragere este respinsă.

> [!NOTE]
> Ca atunci când se solicită o retragere, atunci când o retragere este aprobată, sistemul verifică orice activitate de facturare pe înregistrările de timp sau cheltuieli. Dacă o înregistrare a fost deja facturată sau dacă este pe un proiect de factură, aprobatorul va primi un mesaj de eroare care spune că timpul sau cheltuiala nu pot fi aprobate pentru retragere, deoarece au fost deja facturate.

## <a name="impact-of-a-recall-request"></a>Impactul unei solicitări de retragere

Atunci când se retrage o aprobare, există atât un impact operațional, cât și un impact financiar.

### <a name="operational-impact"></a>Impactul operațional

Dacă se aprobă o solicitare de retragere, înregistrarea de aprobare este marcată **Respinsă**. Starea înregistrării se modifică fie în **Returnată**, fie în **Respinsă**, în funcție de faptul dacă este o înregistrare de timp sau o înregistrare de cheltuieli.

Membrul echipei de proiect poate vizualiza înregistrările, poate, edita și apoi remite înregistrările sau poate șterge înregistrările în întregime.

Dacă o solicitare de retragere este respinsă, starea înregistrării rămâne **Aprobată**, iar înregistrarea nu poate fi editată de membrul echipei de proiect sau de aprobatorul proiectului.

### <a name="financial-impact"></a>Impactul financiar

Dacă se aprobă o solicitare de retragere, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:

- Câmpul **Stare Ajustare** este actualizat la **Ajustat**.
- Câmpul **Stare Facturare** este actualizat la **Anulat**.

Apoi, intrările de inversare sunt create în tabelul Valori reale. Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale. Singurele valori peste care nu se copiază sunt valorile cantitative. Aceste valori sunt inversate în schimb. Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**. Câmpul **Stare Ajustare** de pe valorile reale inversate este setat la **Neajustabil**, iar câmpul **Stare Facturare** este setat la **Anulat.** Din cauza acestor modificări, restanțele înregistrare de cheltuieli și venituri de pe proiect nu vor mai duce la pentru sumele pe care le reprezintă aceste date reale.

Dacă o cerere de retragere este respinsă, nu există niciun impact financiar asupra proiectului.

## <a name="changes-to-time-entry-records"></a>Modificări la înregistrări de intrări de timp

Următoarea ilustrație arată modificările care apar pentru înregistrările de timp aprobate atunci când sunt retrase.

![Tranziții de stare Înregistrare timp](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Modificări la înregistrări de înregistrări de cheltuieli

Următoarea ilustrație arată modificările care apar pentru înregistrările de cheltuieli aprobate atunci când sunt retrase.

![Tranziții de stare Înregistrare cheltuieli](media/ExpenseEntryStateTransitions.png)
