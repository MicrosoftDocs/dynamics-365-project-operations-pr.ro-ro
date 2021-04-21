---
title: Configurarea creării automate a facturilor
description: Acest subiect oferă informații despre setarea și configurarea creării automate a facturilor proforme.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 359c5902e0b6a08ab7fc982095062e4d1816db6c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866832"
---
# <a name="set-up-automatic-invoice-creation"></a>Configurarea creării automate a facturilor 
 
_**Se aplică la:** Implementare Lite - tratarea facturării proforma, Project Operations pentru resurse/scenarii bazate pe altceva decât stocuri_

Puteți configura funcția de creare automată a facturilor în Dynamics 365 Project Operations. Sistemul creează o schiță de factură proforma pe baza programului de facturare pentru fiecare contract de proiect și linie de contract. Programările facturilor sunt configurate la nivelul liniei contractului. Fiecare linie dintr-un contract poate avea un program de facturare distinct sau același program de facturare poate fi inclus pe fiecare linie a contractului.

Când creați o factură, sistemul creează întotdeauna cel puțin o factură per contract de proiect. În unele cazuri, pot exista mai multe facturi create. De exemplu, dacă contractul are mai mulți clienți, se va crea același număr de facturi ca și numărul de clienți care au tranzacții facturabile de facturat în contractul respectiv de proiect.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Înțelegeți cum sunt incluse tranzacțiile pe o factură 

Uneori, fiecare linie de contract bazată pe proiect specifică un program de facturare separat. De exemplu, serviciile de implementare pentru contractul Adatum au următoarele linii contractuale:

- Lucrarea prototip care este un preț fix cu două jaloane create manual.
- Lucrarea de implementare care include timpul și va fi facturată bi-săptămânal, lunea.
- Cheltuielile suportate care trebuie facturate lunar în prima zi de luni a fiecărei luni.

Planificările de facturi definite pentru fiecare dintre aceste două elemente rând arată ca următorul tabel:

| Linie contract | Dată rulare factură | Date de reducere tranzacție | Data datei scadente | Valoare jalon |
| --- | --- | --- | --- | --- |
| Lucrarea prototip | 5 octombrie, luni | - | 5 octombrie, luni | 5000 USD |
| - | 3 noiembrie, marți | - | 3 noiembrie, marți | 12,000 USD |
| Lucrarea de implementare | 5 octombrie, luni | 4 octombrie, duminică | - | - |
| - | 19 octombrie, luni | 18 octombrie, duminică | - | - |
| - | 2 noiembrie, luni | 1 noiembrie, duminică | - | - |
| - | 16 noiembrie, luni | 15 noiembrie, duminică | - | - |
| Cheltuielile suportate | 5 octombrie, luni | 4 octombrie, duminică | - | - |
| - | 2 noiembrie, luni | 1 noiembrie, duminică | - | - |

În acest exemplu când facturarea automată rulează:

- **4 octombrie sau orice altă dată înainte**: Nu se generează nicio factură pentru acest contract deoarece tabelul **Planificare factură** pentru fiecare dintre aceste linii de contract nu au data de 4 octombrie, duminică, ca dată de rulare a facturii.
- **5 octombrie, luni**: Se generează o factură pentru:

    - Lucrarea prototip care include jalonul, dacă este marcat ca **Gata de facturat**.
    - Lucrarea de implementare care include toate tranzacțiile de timp create înainte de data limită a tranzacției de 4 octombrie, duminică, care este marcată ca **Gata de facturat**.
    - Cheltuielile efectuate care includ toate Tranzacțiile de cheltuieli create înainte de data limită a tranzacției de 4 octombrie, duminică, care este marcată ca **Gata de facturat**.
  
- **La 6 octombrie sau orice altă dată înainte de 19 octombrie**: Nu se generează nicio factură pentru acest contract deoarece tabelul **Planificare factură** pentru fiecare dintre aceste linii de contract nu au data de 6 octombrie sau orice altă dată înainte de 19 octombrie ca dată de rulare a facturii.
- **19 octombrie, luni**: Se generează o singură factură pentru lucrările de implementare care include toate tranzacțiile de timp create înainte de data limită a tranzacției de 18 octombrie, duminică, care este marcată ca **Gata de facturat**.
- **2 noiembrie, luni**: Se generează o factură pentru:

    - Lucrarea de implementare care include toate tranzacțiile de timp create înainte de data limită a tranzacției de 1 noiembrie, duminică, care este marcată ca **Gata de facturat**.
    - Cheltuielile efectuate care includ toate Tranzacțiile de cheltuieli create înainte de data limită a tranzacției de 1 noiembrie, duminică, care este marcată ca **Gata de facturat**.

- **3 noiembrie, marți**: Se generează o factură pentru lucrarea prototip care include jalonul important pentru 12000 USD, dacă este marcată ca **Gata de facturat**.

## <a name="configure-automatic-invoicing"></a>Configurați facturarea automată

Parcurgeți pașii următori pentru a configura o rulare factură automată.

1. În **Project Operations**, accesați **Setări** > **Configurare factură recurentă**.
2. Creați o operațiune de lot și denumiți-o **Operațiuni de proiect de creare facturi**. Numele operațiunii de lot trebuie să includă cuvintele „creare facturi”.
3. În câmpul **Tip lucrare**, selectați **Fără**. În mod implicit, câmpurile **Frecvența zilnică** și **Este activ** sunt setate la **Da**.
4. Selectați **Rulați fluxul de lucru**. În caseta de dialog **Căutare înregistrare**, veți vedea trei fluxuri de lucru:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Selectați **ProcessRunCaller**, apoi selectați **Adăugare**.
6. În următoarea casetă de dialog, selectați **OK**. Un flux de lucru **Stare de repaus** este urmat de un fux de lucru **Proces**. 

> [!NOTE]
> De asemenea, puteți selecta **ProcessRunner** în pasul 5. Apoi, când selectați **OK**, un flux de lucru **Proces** este urmat de un flux de lucru **Stare de repaus**.

Fluxurile de lucru **ProcessRunCaller** și **ProcessRunner** creează facturi. **ProcessRunCaller** apelează **ProcessRunner**. **ProcessRunner** este fluxul de lucru care creează de fapt facturile. Fluxul de lucru trece prin toate liniile de contract pentru care trebuie create facturile și creează facturi pentru acele linii. Pentru a determina liniile de contract pentru care trebuie create facturile, lucrarea analizează datele de rulare a facturii pentru liniile de contract. Dacă liniile de contract care aparțin unui contract au aceeași dată de rulare a facturii, tranzacțiile sunt combinate într-o singură factură care are două linii de factură. Dacă nu există tranzacții pentru care să fie create facturi, operațiunea ignoră crearea unei facturi.

După ce **ProcessRunner** a terminat să ruleze, apelează **ProcessRunCaller**, oferă ora de sfârșit și este închis. **ProcessRunCaller** pornește apoi un cronometru care rulează timp de 24 de ore de la ora de sfârșit specificată. La sfârșitul cronometru, **ProcessRunCaller** este închis.

Lucrarea proces de lot pentru crearea facturilor este o lucrare recurentă. Dacă acest proces de lot rulează de mai multe ori, sunt create mai multe instanțe ale lucrării și cauzează erori. De aceea, ar trebui să porniți procesul de lot doar o singură dată și apoi reporniți-l numai dacă se oprește rularea.

> [!NOTE]
> Facturarea în serie în Project Operations se execută numai pentru liniile de contract ale proiectului care sunt configurate de planurile de facturare. O linie de contract cu o metodă de facturare a prețurilor fixe trebuie să aibă configurate repere. O linie de contract de proiect cu o metodă de facturare a timpului și a materialului va avea nevoie de o planificare a facturilor pe bază de date.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
