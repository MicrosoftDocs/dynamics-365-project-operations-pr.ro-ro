---
title: Configurarea creării automate a facturilor
description: Acest subiect oferă informații despre cum să configurați sistemul pentru a genera facturi automat.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122448"
---
# <a name="configure-automatic-invoice-creation"></a>Configurarea creării automate a facturilor

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_


Finalizați pașii următori pentru a configura o rulare automată a facturilor în operațiunile proiectului Dynamics 365.

1. Accesați **Setări** > **Operațiuni de lot**.
2. Creați o operațiune de lot și denumiți-o **Project Operations creați facturi**. Numele operațiunii de lot trebuie să includă cuvintele „creare facturi”.
3. În câmpul **Tip lucrare**, selectați **Fără**. În mod implicit, opțiunile **Frecvența zilnică** și **Este activ** sunt setate la **Da**.
4. Selectați **Rulați fluxul de lucru**. În caseta de dialog **Căutare înregistrare**, veți vedea trei fluxuri de lucru:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selectați **ProcessRunCaller**, apoi selectați **Adăugare**.
6. În următoarea casetă de dialog, selectați **OK**. Un flux de lucru **Stare de repaus** este urmat de un fux de lucru **Proces**.

  > [!NOTE]
  > De asemenea, puteți selecta **ProcessRunner** în pasul 5. Apoi, când selectați **OK**, un flux de lucru **Proces** este urmat de un flux de lucru **Stare de repaus**.

Fluxurile de lucru **ProcessRunCaller** și **ProcessRunner** creează facturi. **ProcessRunCaller** apelează **ProcessRunner**. **ProcessRunner** este fluxul de lucru care creează de fapt facturile. Trece prin toate liniile de contract pentru care trebuie create facturile și creează facturi pentru acele linii. Pentru a determina liniile de contract pentru care trebuie create facturile, lucrarea analizează datele de rulare a facturii pentru liniile de contract. Dacă liniile de contract care aparțin unui contract au aceeași dată de rulare a facturii, tranzacțiile sunt combinate într-o singură factură care are două linii de factură. Dacă nu există tranzacții pentru care să fie create facturi, lucrarea ignoră crearea facturii.

După ce **ProcessRunner** a terminat să ruleze, apelează **ProcessRunCaller**, oferă ora de sfârșit și este închis. **ProcessRunCaller** pornește apoi un cronometru care rulează timp de 24 de ore de la ora de sfârșit specificată. La sfârșitul cronometru, **ProcessRunCaller** este închis.

Lucrarea proces de lot pentru crearea facturilor este o lucrare recurentă. Dacă acest proces de lot rulează de mai multe ori, sunt create mai multe instanțe ale lucrării și cauzează erori. De aceea, ar trebui să porniți procesul de lot doar o singură dată și ar trebui să îl reporniți numai dacă se oprește rularea.

> [!NOTE]
> Facturarea în serie se execută numai pentru liniile de contract ale proiectului care sunt configurate de planurile de facturare. O linie de contract cu o metodă de facturare a prețurilor fixe trebuie să aibă configurate repere. O linie de contract de proiect cu o metodă de facturare a timpului și a materialului va avea nevoie de o planificare a facturilor pe bază de date. Același lucru este valabil și pentru o linie de contract bazată pe proiect.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]