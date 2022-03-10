---
title: Facturi proforme
description: Acest subiect oferă informații despre facturile proforma în Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2050a313fe530065341410d60801b13eb958cb32ae24eb4a0a71ab7ea5061881
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995641"
---
# <a name="proforma-invoices"></a>Facturi proforme

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Facturarea prin proformă este utilă deoarece le oferă managerilor de proiect un al doilea nivel de aprobare înainte de a crea facturi pentru clienți. Primul nivel de aprobare se finalizează când se aprobă intrările de timp, cheltuieli și materiale pe care le transmit membrii echipei de proiect. Facturile proforme confirmate sunt disponibile în modulul de contabilitate a proiectelor din Project Operations. Contabilii de proiect pot efectua actualizări suplimentare, cum ar fi impozitul pe vânzări, contabilitatea și aspectul facturilor.


## <a name="creating-project-invoices"></a>Se creează facturi de proiect

Facturile de proiect pot fi create pe rând sau în bloc. Aveți posibilitatea să le creați manual sau acestea pot fi configurate astfel încât să fie generate în rulări automate.

### <a name="manually-create-project-invoices"></a>Creați manual facturi de proiect 

Din pagina listei **Contracte proiect**, aveți posibilitatea să creați facturi de proiect separat pentru fiecare contract de proiect sau să creați facturi în vrac pentru mai multe contracte de proiect.

Urmați acest pas pentru a crea o factură pentru un anumit contract de proiect.

- Pe pagina de listă **Contracte de proiect**, deschideți un contract de proiect și apoi selectați **Creare factură**.

    O factură este generată pentru toate tranzacțiile pentru contractul de proiect selectat care au starea **Gata de facturat**. Aceste tranzacții includ linii de jurnal cu privire la timp, cheltuieli, materiale, repere și alte linii de jurnal de vânzări nefacturate.

Parcurgeți acești pași pentru a crea facturi în vrac.

1. Pe pagina de listă **Contracte de proiect**, selectați unul sau mai multe contracte de proiect pentru care trebuie să creați o factură, apoi selectați **Creați facturi de proiect**.

    Un mesaj de avertizare vă informează că este posibil să existe o întârziere înainte de crearea facturilor. Procesul este, de asemenea, afișat.

2. Selectați **OK** pentru a închide caseta de mesaj.

    O factură este generată pentru toate tranzacțiile pe o linie de contract care au o stare **Gata de facturat**. Aceste tranzacții includ linii de jurnal cu privire la timp, cheltuieli, materiale, repere și alte linii de jurnal de vânzări nefacturate.

3. Pentru a vizualiza facturile care sunt generate, accesați **Vânzări** \> **Facturare** \> **Facturi**. Veți vedea o factură pentru fiecare contract de proiect.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurați crearea automată a facturilor de proiect 

Parcurgeți acești pași pentru a configura o rulare factură automată.

1. Accesați **Setări** \> **Operațiuni de lot**.
2. Creați o operațiune de lot și denumiți-o **Project Operations de creare facturi**. Numele lucrării pe loturi trebuie să includă termenul „Creare facturi”.
3. În câmpul **Tip lucrare**, selectați **Niciuna.** În mod implicit, opțiunile **Frecvența zilnică** și **Este activ** sunt setate la **Da**.
4. Selectați **Rulați fluxul de lucru**. În caseta de dialog **Căutare înregistrare**, veți vedea trei fluxuri de lucru:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Selectați **ProcessRunCaller**, apoi selectați **Adăugare**.
6. În următoarea casetă de dialog, selectați **OK**. Un flux de lucru **Stare de repaus** este urmat de un fux de lucru **Proces**.

    De asemenea, puteți selecta **ProcessRunner** în pasul 5. Apoi, când selectați **OK**, un flux de lucru **Proces** este urmat de un flux de lucru **Stare de repaus**.

Fluxurile de lucru **ProcessRunCaller** și **ProcessRunner** creează facturi. **ProcessRunCaller** apelează **ProcessRunner**. **ProcessRunner** este fluxul de lucru care creează de fapt facturile. Trece prin toate liniile de contract pentru care trebuie create facturile și creează facturi pentru acele linii. Pentru a determina liniile de contract pentru care trebuie create facturile, lucrarea analizează datele de rulare a facturii pentru liniile de contract. Dacă liniile de contract care aparțin unui contract au aceeași dată de rulare a facturii, tranzacțiile sunt combinate într-o singură factură care are două linii de factură. Dacă nu există tranzacții pentru care să fie create facturi, lucrarea ignoră crearea facturii.

După ce **ProcessRunner** a terminat să ruleze, apelează **ProcessRunCaller**, oferă ora de sfârșit și este închis. **ProcessRunCaller** pornește apoi un cronometru care rulează timp de 24 de ore de la ora de sfârșit specificată. La sfârșitul cronometru, **ProcessRunCaller** este închis.

Lucrarea proces de lot pentru crearea facturilor este o lucrare recurentă. Dacă acest proces de lot rulează de mai multe ori, sunt create mai multe instanțe ale lucrării și cauzează erori. De aceea, ar trebui să porniți procesul de lot doar o singură dată și ar trebui să îl reporniți numai dacă se oprește rularea.

> [!NOTE]
> Facturarea în serie se execută numai pentru liniile de contract ale proiectului care sunt configurate de planurile de facturare. O linie de contract cu o metodă de facturare a prețurilor fixe trebuie să aibă configurate repere. O linie de contract de proiect cu o metodă de facturare a timpului și a materialului va avea nevoie de o planificare a facturilor pe bază de date. Același lucru este valabil și pentru o linie de contract bazată pe proiect.      
 
### <a name="edit-a-draft-invoice"></a>Editați o schiță de factură

Atunci când creați o factură de proiect schiță, toate tranzacțiile de vânzări nefacturate care au fost create atunci când intrările de timp, cheltuieli și utilizare de materiale au fost aprobate și sunt introduse pe factură. Aveți posibilitatea să efectuați următoarele ajustări în timp ce factura este încă într-o fază schiță:

- Ștergeți sau editați detaliile liniei de facturare.
- Editați și ajustați cantitatea și tipul de facturare.

Selectați **Confirmați** pentru a confirma o factură. Acțiunea Confirmați este o acțiune într-o direcție. Când selectați **Confirmați**, sistemul face factura doar în citire și creează valori reale de vânzări facturate din fiecare detaliu de linie de factură pentru fiecare linie de factură. Dacă detaliul de linie pentru factură face referire la o valoare reală de vânzări nefacturate, sistemul inversează, de asemenea, valoarea reală de vânzări nefacturate. (Orice detaliu al liniei de factură care a fost creat dintr-o intrare de timp sau cheltuieli va face referire la o valoare reală de vânzări nefacturate.) Sistemele de integrare ale registrului general pot utiliza această inversare pentru a inversa proiectul în curs (WIP) în scopuri contabile.

### <a name="correct-a-confirmed-invoice"></a>Corectați o factură confirmată

Facturile confirmate pot fi editate (corectate). Când corectați o factură confirmată, se creează o nouă schiță de factură rectificativă. Întrucât ipoteza este că doriți să inversați toate tranzacțiile și cantitățile din factura originală, această factură rectificativă include toate tranzacțiile din factura originală și toate cantitățile de aici sunt 0 (zero).

Dacă tranzacțiile nu necesită corecție, puteți să le eliminați din proiectul de factură rectificativă. Dacă doriți să inversați sau să returnați numai o cantitate parțială, puteți să editați **Cantitatea** în detaliul liniei. Dacă deschideți detaliul de linie factură, puteți să vedeți cantitatea inițială de factură. Aveți posibilitatea să editați apoi cantitatea curentă de factură, astfel încât să fie mai mică sau mai mare decât cantitatea inițială de factură.

Când confirmați o factură rectificativă, valoarea reală a vânzărilor inițiale facturate este inversată și se creează o nouă valoare reală de vânzări facturate. În cazul în care cantitatea a fost redusă, diferența va provoca o nouă valoare reală de vânzări nefacturate pentru a fi create. De exemplu, dacă vânzarea facturată inițial a fost de opt ore și detaliile liniei de factură de corectare are o cantitate redusă de șase ore, liniile facturate origniale sunt inversate și sunt create două noi valori reale:

- O valoare reală de vânzări facturate timp de șase ore.
- O valoare reală de vânzări nefacturate pentru restul de două ore. Această tranzacție poate fi facturată ulterior sau poate fi marcată ca netaxabilă, în funcție de negocierile cu clientul.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
