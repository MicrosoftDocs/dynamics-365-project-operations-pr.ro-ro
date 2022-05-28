---
title: Anulați aprobarea intrărilor aprobate anterior
description: Acest subiect explică modul în care un manager de proiect poate anula aprobarea intrărilor de timp, cheltuieli sau utilizare a materialelor aprobate anterior.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584795"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Anulați aprobarea intrărilor aprobate anterior

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Un manager de proiect sau un aprobator care a aprobat anterior intrări privind timpul, cheltuielile sau utilizarea materialelor poate anula aprobarea acelor intrări. 

Urmați acești pași pentru a anula aprobarea unei intrări de timp, cheltuială sau utilizare a materialului aprobată anterior.

1. Accesați **Proiecte** \> **Lucrul meu** \> **Aprobări**.
2. The **Aprobari** Pagina listă arată toate intrările de timp care așteaptă aprobare. Schimbați vizualizarea în **Aprobarile mele din trecut**.
3. Selectați timpul, cheltuielile sau aprobările materiale de anulat. Apoi, în panoul de acțiuni, selectați **Anulați aprobarea**.
4. În caseta de mesaj de confirmare care apare, selectați **Bine** pentru a confirma operația.

> [!IMPORTANT]
> Nu puteți anula aprobarea unei intrări de timp, cheltuieli și utilizare a materialului aprobate anterior, care a fost deja facturată clientului. Dacă încercați, primiți un mesaj care spune că aprobarea nu poate fi anulată deoarece a fost deja facturată. În acest caz, puteți anula aprobarea numai dacă se utilizează o factură corectivă pentru a emite un credit complet sau o rambursare către client pe factura originală.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impactul anulării aprobării unei intrări aprobate anterior

Atunci când o aprobare este anulată, există atât un impact operațional, cât și un impact financiar.

### <a name="operational-impact"></a>Impactul operațional

Dacă aprobarea unei înscrieri este anulată, înregistrarea de aprobare este marcată ca **Trimis**. Starea intrării este schimbată în **Trimis**. În această etapă, un membru al echipei de proiect poate reaminti intrarea fără a trimite o cerere de rechemare.

Aprobatorul poate schimba **Cantitate facturabilă** și **Tip de facturare** valori, apoi aprobați încă o dată intrarea.

### <a name="financial-impact"></a>Impactul financiar

Dacă aprobarea unei înscrieri este anulată, valorile reale corespunzătoare pentru cost și vânzări sunt actualizate în felul următor:

- Câmpul **Stare Ajustare** este actualizat la **Ajustat**.
- Câmpul **Stare Facturare** este actualizat la **Anulat**.

Apoi, intrările de inversare sunt create în tabelul Valori reale. Pentru a crea intrări de inversare, sistemul copiază peste valorile câmpului din valorile reale inițiale. Singurele valori peste care nu se copiază sunt valorile cantitative. Aceste valori sunt inversate în schimb. Valori reale inversate sunt create atât pentru valorile reale **Cost**, cât și **Vânzări nefacturate**. Câmpul **Stare Ajustare** de pe valorile reale inversate este setat la **Neajustabil**, iar câmpul **Stare Facturare** este setat la **Anulat.** Din cauza acestor modificări, restanțele înregistrare de cheltuieli și venituri de pe proiect nu vor mai duce la pentru sumele pe care le reprezintă aceste date reale.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
