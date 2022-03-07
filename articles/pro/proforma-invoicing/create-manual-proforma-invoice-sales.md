---
title: Facturi proforma de proiect
description: Acest subiect oferă informații despre facturile de proiect proforma în Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3d02728ce682781eb8816e0c2239cf62f88adfa8c5d2a0aab280be053c2a5ae6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992941"
---
# <a name="proforma-project-pnvoices"></a>Facturi proforma de proiect

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Facturarea prin proformă pentru proiect este utilă deoarece le oferă managerilor de proiect un al doilea nivel de aprobare înainte de a crea facturi pentru clienți. Primul nivel de aprobare se finalizează când se aprobă intrările de timp, cheltuieli și materiale pe care le transmit membrii echipei de proiect.

Implementarea Dynamics 365 Project Operations Lite nu este concepută pentru a genera facturi orientate către clienți. Următoarea listă arată de ce nu se pot genera facturi:

- Nu conține informații fiscale.
- Nu se pot converti alte monede în moneda de facturare.
- Nu se pot formata corect facturile pentru tipărire.

În schimb, aveți posibilitatea să utilizați un sistem financiar sau contabil pentru a crea facturi orientate spre client care utilizează informațiile din propunerile de factură generate.

## <a name="creating-project-invoices"></a>Se creează facturi de proiect

Facturile de proiect pot fi create pe rând sau în bloc. Aveți posibilitatea să le creați manual sau acestea pot fi configurate astfel încât să fie generate în rulări automate.

### <a name="manually-create-project-invoices"></a>Creați manual facturi de proiect 

Pe pagina listei **Contracte proiect**, aveți posibilitatea să creați facturi de proiect separat pentru fiecare contract de proiect sau să creați facturi în vrac pentru mai multe contracte de proiect.

   - Pentru a crea o factură pentru un anumit contract de proiect, pe pagina de listă **Contracte de proiect**, deschideți un contract de proiect, apoi selectați **Creare factură**.

   O factură este generată pentru toate tranzacțiile pentru contractul de proiect selectat care au starea **Gata de facturat**. Aceste tranzacții includ timp, cheltuieli, materiale, repere, linii de contract bazate pe produse și alte linii jurnal de vânzări nefacturate care ar fi putut fi confirmate.

Pentru a crea facturi în masă:

1. Pe pagina de listă **Contracte de proiect**, selectați unul sau mai multe contracte de proiect pentru a crea o factură, apoi selectați **Creați facturi de proiect**.
2. Un mesaj de avertizare vă informează că este posibil să existe o întârziere înainte de crearea facturilor. Procesul este, de asemenea, afișat. Selectați **OK** pentru a închide caseta de mesaj.

   O factură este generată pentru toate tranzacțiile pe o linie de contract care au o stare **Gata de facturat**. Aceste tranzacții includ timp, cheltuieli, materiale, repere, linii de contract bazate pe produse și alte linii jurnal de vânzări nefacturate care ar fi putut fi confirmate.

3. Vizualizați facturile care sunt generate accesând **Vânzări** \> **Facturare** \> **Facturi**. Veți vedea o factură pentru fiecare contract de proiect.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurați crearea automată a facturilor de proiect 

Parcurgeți acești pași pentru a configura o rulare factură automată.

1. Accesați **Setări** \> **Operațiuni de lot**.
2. Creați o operațiune de lot și denumiți-o **Project Operations de creare facturi**. Numele lucrării pe loturi trebuie să includă termenul „Creare facturi”.
3. În câmpul **Tip lucrare**, selectați **Niciuna.** În mod implicit, opțiunile **Frecvența zilnică** și **Este activ** sunt setate la **Da**.
4. Selectați **Rulați fluxul de lucru**. În caseta de dialog **Căutare înregistrare**, veți vedea următoarele fluxuri de lucru:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selectați **ProcessRunCaller**, apoi selectați **Adăugare**.
6. În următoarea casetă de dialog, selectați **OK**. Un flux de lucru **Stare de repaus** este urmat de un fux de lucru **Proces**.

    De asemenea, puteți selecta **ProcessRunner** în pasul 5. Apoi, când selectați **OK**, un flux de lucru **Proces** este urmat de un flux de lucru **Stare de repaus**.

Fluxurile de lucru **ProcessRunCaller** și **ProcessRunner** creează facturi. **ProcessRunCaller** apelează **ProcessRunner**. **ProcessRunner** este fluxul de lucru care creează facturile. Acest flux de lucru trece prin toate liniile de contract pentru care trebuie create facturile și creează facturile. Pentru a determina liniile de contract pentru care trebuie create facturile, fluxul de lucru analizează datele de rulare a facturii pentru liniile de contract. Dacă liniile de contract care aparțin unui contract au aceeași dată de rulare a facturii, tranzacțiile sunt combinate într-o singură factură care are două linii de factură. Dacă nu există tranzacții pentru care să fie create facturi, nu se creează facturi.

După ce **ProcessRunner** a terminat să ruleze, apelează **ProcessRunCaller**, oferă ora de sfârșit și este închis. **ProcessRunCaller** pornește apoi un cronometru care rulează timp de 24 de ore de la ora de sfârșit specificată. La sfârșitul cronometru, **ProcessRunCaller** este închis.

Lucrarea proces de lot pentru crearea facturilor este o lucrare recurentă. Dacă acest proces de lot rulează de mai multe ori, sunt create mai multe instanțe ale lucrării și se pot cauza erori. Pentru a evita această problemă, porniți procesul de lot doar o singură dată și reporniți numai dacă se oprește rularea.

> [!NOTE]
> Facturarea în serie se execută numai pentru liniile de contract ale proiectului care sunt configurate de planurile de facturare. O linie de contract cu o metodă de facturare a prețurilor fixe trebuie să aibă configurate repere. O linie de contract de proiect cu o metodă de facturare a timpului și a materialului va avea nevoie de o planificare a facturilor pe bază de date. Același lucru este valabil și pentru o linie de contract bazată pe proiect.      
 
### <a name="edit-a-draft-invoice"></a>Editați o schiță de factură

Atunci când creați o factură de proiect schiță, toate tranzacțiile de vânzări nefacturate care au fost create atunci când intrările de timp și cheltuieli care au fost aprobate sunt compilate pe factură. Aveți posibilitatea să efectuați următoarele ajustări în timp ce factura este încă într-o fază schiță:

- Ștergeți sau editați detaliile liniei de facturare.
- Editați și ajustați cantitatea și tipul de facturare.
- Adăugați direct timp, cheltuieli, materiale și taxe ca tranzacții pe factură. Puteți utiliza această caracteristică dacă linia de facturare este mapată la o linie de contract care permite aceste clase de tranzacții.

Selectați **Confirmați** pentru a confirma o factură. Această acțiune este o acțiune într-o direcție. Când selectați **Confirmați**, factura devine doar în citire și creează valori reale de vânzări facturate din fiecare detaliu de linie de factură pentru fiecare linie de factură. Dacă detaliul de linie pentru factură face referire la o valoare reală de vânzări nefacturate, se inversează și valoarea reală de vânzări nefacturate. Orice detaliu al liniei de factură care a fost creat dintr-o intrare de timp, cheltuială sau utilizare a materialului va face referire la o vânzare reală nefacturată. Sistemele de integrare a registrului general pot utiliza această inversare pentru a inversa lucrările în curs ale proiectului (WIP) în scopuri contabile.

### <a name="correct-a-confirmed-invoice"></a>Corectați o factură confirmată

Facturile PSA confirmate pot fi editate. Când corectați o factură confirmată, se creează o nouă schiță de factură rectificativă. Întrucât ipoteza este că doriți să inversați toate tranzacțiile și cantitățile din factura originală, această factură rectificativă include toate tranzacțiile din factura originală și toate cantitățile de aici sunt zero.

Dacă există tranzacții care nu necesită corecție, puteți să le eliminați din proiectul de factură rectificativă. Dacă doriți să inversați sau să returnați numai o cantitate parțială, puteți să editați **Cantitatea** în detaliul liniei. Dacă deschideți detaliul de linie factură, puteți să vedeți cantitatea inițială de factură. Aveți posibilitatea să editați apoi cantitatea curentă de factură, astfel încât să fie mai mică sau mai mare decât cantitatea inițială de factură.

Când confirmați o factură rectificativă, valoarea reală a vânzărilor inițiale facturate este inversată și se creează o nouă valoare reală de vânzări facturate. În cazul în care cantitatea a fost redusă, diferența va provoca o nouă valoare reală de vânzări nefacturate pentru a fi create. De exemplu, dacă vânzarea facturată inițial a fost de opt ore și detaliile liniei de factură de corectare are o cantitate redusă de șase ore, liniile facturate originale sunt inversate și sunt create două noi valori reale:

- O valoare reală de vânzări facturate timp de șase ore.
- O valoare reală de vânzări nefacturate pentru restul de două ore. Această tranzacție poate fi facturată ulterior sau poate fi marcată ca netaxabilă, în funcție de negocierile cu clientul.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
