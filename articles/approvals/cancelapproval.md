---
title: Anularea aprobării pentru intrările aprobate anterior
description: Acest articol explică modul în care un manager de proiect poate anula aprobarea intrărilor de timp, cheltuieli sau utilizare a materialelor aprobate anterior.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930471"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Anularea aprobării pentru intrările aprobate anterior

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Un manager de proiect sau aprobator care a aprobat anterior intrări de timp, cheltuieli sau utilizare a materialelor poate anula aprobarea acelor intrări. 

Urmați acești pași pentru a anula aprobarea unei intrări de timp, cheltuieli sau utilizare a materialelor anterioare.

1. Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.
2. Pagina listă **Aprobări** afișează toate intrările de timp care așteaptă aprobare. Schimbați vizualizarea în **Aprobările mele anterioare**.
3. Selectați timpul, cheltuielile sau aprobările materiale de anulat. Apoi, în Panoul acțiuni, selectați **Anulare aprobare**.
4. În caseta de mesaj de confirmare care apare, selectați **OK** pentru a confirma operațiunea.

> [!IMPORTANT]
> Nu puteți anula aprobarea unei intrări de timp, cheltuieli și utilizare a materialului aprobate anterior, care a fost deja facturată clientului. Dacă încercați, primiți un mesaj care spune că aprobarea nu poate fi anulată deoarece a fost deja facturată. În acest caz, puteți anula aprobarea numai dacă se utilizează o factură corectivă pentru a emite o creditare completă sau o rambursare către client pe factura originală.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impactul anulării aprobării unei înregistrări aprobate anterior

Atunci când o aprobare este anulată, există atât un impact operațional, cât și un impact financiar.

### <a name="operational-impact"></a>Impactul operațional

Dacă aprobarea unei intrări este anulată, înregistrarea de aprobare este marcată ca **Remisă**. Starea intrării este schimbată în **Remisă**. În această etapă, un membru al echipei de proiect poate retrage intrarea fără a trimite o cerere de retragere.

Aprobatorul poate schimba valorile **Cantitate facturabilă** și **Tip de facturare**, apoi poate aproba încă o dată intrarea.

### <a name="financial-impact"></a>Impactul financiar

Dacă aprobarea unei intrări este anulată, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în modul următor:

- Câmpul **Stare Ajustare** este actualizat la **Ajustat**.
- Câmpul **Stare Facturare** este actualizat la **Anulat**.

Apoi, intrările de inversare sunt create în tabelul Valori reale. Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale. Singurele valori peste care nu se copiază sunt valorile cantitative. Aceste valori sunt inversate în schimb. Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**. Câmpul **Stare Ajustare** de pe valorile reale inversate este setat la **Neajustabil**, iar câmpul **Stare Facturare** este setat la **Anulat.** Din cauza acestor modificări, restanțele înregistrare de cheltuieli și venituri de pe proiect nu vor mai duce la pentru sumele pe care le reprezintă aceste date reale.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
