---
title: Anularea intrărilor de timp și cheltuieli aprobate anterior
description: Acest subiect oferă informații despre cum să anulați o tranzacție de timp și cheltuieli de proiect aprobată anterior.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ea816040570cc8f6ddf3c5ec8a74ac092fc68b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082971"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Anularea intrărilor de timp sau cheltuieli aprobate anterior

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

În cea mai recentă versiune de Dynamics 365 Project Service Automation, aprobatorii pot anula intrările de timp sau cheltuieli pe care le-au aprobat anterior.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Anularea unei intrări de timp sau cheltuieli aprobată anterior

Urmați acești pași pentru a anula o intrare de timp sau cheltuieli aprobată anterior de dvs.

1. Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.
2. Pe pagina cu lista **Aprobări** , modificați vizualizarea la **Aprobările mele anterioare**. Este afișată o listă a intrărilor de timp și cheltuieli pe care le-ați aprobat anterior.
3. Selectați una sau mai multe intrări, apoi selectați **Anulați aprobarea**. Primiți un mesaj de avertizare.
4. Selectați **OK** pentru a anula aprobarea.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Înțelegeți impactul anularii unei aprobări de intrare de timp sau cheltuieli

Atunci când o aprobare este anulată, există atât un impact operațional, cât și un impact financiar.

### <a name="operational-impact"></a>Impactul operațional

Pe partea de operațiuni, atunci când o aprobare este anulată, starea înregistrării este resetată **Schiță** și aprobarea nu mai apare în vizualizarea **Aprobările mele anterioare**. În schimb, aprobarea anulată apare fie în vizualizarea **Intrări de timp pentru aprobare** , fie în vizualizarea **Intrări de cheltuieli pentru aprobare** , în funcție de dacă a fost o intrare de timp sau o intrare de cheltuieli. În plus, starea intrării de timp sau de cheltuieli corelată este modificată la **Remisă** , astfel încât intrarea corelată este în concordanță cu aprobările care au o stare de **Schiță**.

Ca aprobator, aveți posibilitatea să editați unele dintre câmpurile unei aprobări care are starea **Schiță**. Aceste câmpuri includ **Tip de facturare** și **Ore facturabile pentru intrările de timp**. După ce efectuați modificări, aveți posibilitatea să aprobați din nou înregistrarea. Alternativ, puteți respinge intrarea. Dacă respingeți aprobarea unei intrări de timp, starea intrării se modifică la **Returnat**. Dacă respingeți aprobarea unei intrări de cheltuieli, starea se modifică la **Returnat**. Din punct de vedere funcțional, intrările returnate și respinse se comportă la fel ca o intrare care are starea **Schiță**. Un membru al echipei de proiect poate face orice modificări necesare intrării și apoi remite intrarea pentru aprobare, sau poate șterge intrarea în întregime.

### <a name="financial-impact"></a>Impactul financiar

Un proiect este, de asemenea, afectat financiar atunci când o aprobare este anulată. Mai întâi, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:

- Starea de ajustare este setată la **Ajustat**.
- Starea de facturare este setată la **Anulat**.

Apoi, intrările de inversare sunt create în tabelul Valori reale. Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale. Singurele valori peste care nu se copiază sunt valorile cantitative. Aceste valori sunt inversate în schimb. Valori reale inversate sunt create atât pentru valorile reale **Cost** , cât și **Vânzări nefacturate**. Câmpul **Stare ajustare** din valorile reale inversate este setat la **Neajustabil** , iar starea de facturare este setată la **Anulat**.

După efectuarea acestor modificări, suma înregistrată ca fiind cheltuită pe proiect și restanțele de venituri de pe proiect nu vor mai totaliza sumele pe care le reprezintă aceste date reale.