---
title: Facturare în Project Service Automation
description: Acest subiect oferă informații despre facturare.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 58259c05939cfe870ce5e36b4a0221cd93b8e8d2b4be582efc9167e82579699e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985516"
---
# <a name="invoicing-in-project-service-automation"></a>Facturare în Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Facturarea Dynamics 365 Project Service Automation este utilă deoarece le oferă managerilor de proiect un al doilea nivel de aprobare înainte de a crea facturi pentru clienți. Primul nivel de aprobare se finalizează când se aprobă intrările de timp și cheltuieli pe care le transmit membrii echipei de proiect.

PSA nu este proiectat pentru a genera facturi orientate spre client, din următoarele motive:

- Nu conține informații fiscale.
- Nu poate converti alte valute în valuta de facturare utilizând ratele de schimb corect configurate.
- Nu se pot formata corect facturi, astfel încât să poată fi imprimate.

În schimb, aveți posibilitatea să utilizați un sistem financiar sau contabil pentru a crea facturi orientate spre client care utilizează informațiile din propunerile de factură care sunt generate în PSA.

## <a name="creating-project-invoices-in-psa"></a>Se creează facturi de proiect în PSA

Facturile de proiect pot fi create pe rând sau în bloc. Aveți posibilitatea să le creați manual sau acestea pot fi configurate astfel încât să fie generate în rulări automate.

### <a name="manually-create-project-invoices-in-psa"></a>Creați manual facturi de proiect în PSA

Din pagina listei **Contracte proiect**, aveți posibilitatea să creați facturi de proiect separat pentru fiecare contract de proiect sau să creați facturi în vrac pentru mai multe contracte de proiect.

Urmați acest pas pentru a crea o factură pentru un anumit contract de proiect.

- Pe pagina de listă **Contracte de proiect**, deschideți un contract de proiect și apoi selectați **Creare factură**.

    ![Crearea facturilor de proiect pentru un anumit contract de proiect.](media/CreateProjectInvoicesOneByOne.png)

    O factură este generată pentru toate tranzacțiile pentru contractul de proiect selectat care au starea **Gata de facturat**. Aceste tranzacții includ timp, cheltuieli, jaloane și linii de contract bazate pe produse.

Parcurgeți acești pași pentru a crea facturi în vrac.

1. Pe pagina de listă **Contracte de proiect**, selectați unul sau mai multe contracte de proiect pentru care trebuie să creați o factură, apoi selectați **Creați facturi de proiect**.

    ![Se creează facturi de proiect în vrac.](media/CreateProjectInvoicesBulk.png)

    Un mesaj de avertizare vă informează că este posibil să existe o întârziere înainte de crearea facturilor. Procesul este, de asemenea, afișat.

2. Selectați **OK** pentru a închide caseta de mesaj.

    O factură este generată pentru toate tranzacțiile pe o linie de contract care au o stare **Gata de facturat**. Aceste tranzacții includ timp, cheltuieli, jaloane și linii de contract bazate pe produse.

3. Pentru a vizualiza facturile care sunt generate, accesați **Vânzări** \> **Facturare** \> **Facturi**. Veți vedea o factură pentru fiecare contract de proiect.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Configurați crearea automată a facturilor de proiect în PSA

Parcurgeți acești pași pentru a configura o rulare factură automată în PSA.

1. Accesați **Project Service** \> **Setări** \> **Lucrări pe roluri**.
2. Creați o lucrare pe loturi și denumiți-o **Creare facturi PSA**. Numele lucrării pe loturi trebuie să includă termenul „Creare facturi”.
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
> Facturarea în lot în Project Service Automation se execută numai pentru liniile de contract de proiect care sunt configurate prin planificarea facturilor. O linie de contract cu o metodă de facturare a prețurilor fixe trebuie să aibă configurate repere. O linie de contract de proiect cu o metodă de facturare a timpului și a materialului va avea nevoie de o planificare a facturilor pe bază de date. Informații despre configurarea frecvențelor de facturare în contextul unui proiect care se bazează pe o linie de ofertă, sunt furnizate în subiect, [Oferte și linii de ofertă](basic-quote-lines.md#invoice-schedule). Același lucru este valabil și pentru o linie de contract bazată pe proiect.      
 
### <a name="edit-a-draft-psa-invoice"></a>Editați o factură PSA schiță

Atunci când creați o factură de proiect schiță, toate tranzacțiile de vânzări nefacturate care au fost create atunci când intrările de timp și cheltuieli care au fost aprobate sunt compilate pe factură. Aveți posibilitatea să efectuați următoarele ajustări în timp ce factura este încă într-o fază schiță:

- Ștergeți sau editați detaliile liniei de facturare.
- Editați și ajustați cantitatea și tipul de facturare.
- Adăugați direct timp, cheltuieli și taxe ca tranzacții pe factură. Puteți utiliza această caracteristică dacă linia de facturare este mapată la o linie de contract care permite aceste clase de tranzacții.

Selectați **Confirmați** pentru a confirma o factură. Acțiunea Confirmați este o acțiune într-o direcție. Când selectați **Confirmați**, sistemul face factura doar în citire și creează valori reale de vânzări facturate din fiecare detaliu de linie de factură pentru fiecare linie de factură. Dacă detaliul de linie pentru factură face referire la o valoare reală de vânzări nefacturate, sistemul inversează, de asemenea, valoarea reală de vânzări nefacturate. (Orice detaliu al liniei de factură care a fost creat dintr-o intrare de timp sau cheltuieli va face referire la o valoare reală de vânzări nefacturate.) Sistemele de integrare ale registrului general pot utiliza această inversare pentru a inversa proiectul în curs (WIP) în scopuri contabile.

### <a name="correct-a-confirmed-psa-invoice"></a>Corectați o factură PSA confirmată

Facturile PSA confirmate pot fi editate (corectate). Când corectați o factură confirmată, se creează o nouă schiță de factură rectificativă. Întrucât ipoteza este că doriți să inversați toate tranzacțiile și cantitățile din factura originală, această factură rectificativă include toate tranzacțiile din factura originală și toate cantitățile de aici sunt 0 (zero).

Dacă tranzacțiile nu necesită corecție, puteți să le eliminați din proiectul de factură rectificativă. Dacă doriți să inversați sau să returnați numai o cantitate parțială, puteți să editați **Cantitatea** în detaliul liniei. Dacă deschideți detaliul de linie factură, puteți să vedeți cantitatea inițială de factură. Aveți posibilitatea să editați apoi cantitatea curentă de factură, astfel încât să fie mai mică sau mai mare decât cantitatea inițială de factură.

Când confirmați o factură rectificativă, valoarea reală a vânzărilor inițiale facturate este inversată și se creează o nouă valoare reală de vânzări facturate. În cazul în care cantitatea a fost redusă, diferența va provoca o nouă valoare reală de vânzări nefacturate pentru a fi create. De exemplu, dacă vânzările facturate inițial au fost de opt ore, iar detaliile liniei facturii rectificative au o cantitate redusă de șase ore, PSA inversează linia de vânzări inițiale facturate și creează două valori reale noi:

- O valoare reală de vânzări facturate timp de șase ore.
- O valoare reală de vânzări nefacturate pentru restul de două ore. Această tranzacție poate fi facturată ulterior sau poate fi marcată ca netaxabilă, în funcție de negocierile cu clientul.


[!INCLUDE[footer-include](../includes/footer-banner.md)]