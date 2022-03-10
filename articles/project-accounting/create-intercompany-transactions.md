---
title: Crearea de tranzacții între companii
description: Acest subiect oferă informații despre cum să creați tranzacții între companii.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4ce3a45e5a09b7ac5b5663cf9983e3bed7bf7e0d3fedede2e4524c51069a800b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005496"
---
# <a name="create-intercompany-transactions"></a>Crearea de tranzacții între companii

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Tranzacțiile între companii sunt tranzacții de timp și cheltuieli dintr-un contract de proiect care aparțin unei companii sau unei unități organizaționale, în timp ce resursele din contractul de proiect fac parte dintr-o altă companie sau unitate organizațională.

Când se aprobă o tranzacție între companii, se creează următoarele tranzacții reale

| **Tip de tranzacție** | **Lista de prețuri aplicată** | **Monedă de tranzacționare** |
| --- | --- | --- |
| Cost | Lista de prețuri a costurilor unitare | Moneda pe linia de preț |
| Vânzări nefacturate. Acestea sunt create numai pentru datele reale care sunt asociate cu o linie de contract cu tipul, ora și materialul de facturare. | Lista de prețuri de vânzare pentru contractul de proiect | Monedă pentru contract |
| Cost de unitate resursă | Lista de prețuri unitare pentru alocarea de resurse | Moneda pe linia de preț |
| Vânzări unitare inter-organizaționale | Lista de prețuri a costurilor unitare | Moneda pe linia de preț |

Costul, costul unitar al resurselor și prețurile tranzacțiilor de vânzare ale unităților inter-organizaționale și moneda sunt determinate de **unitate organizațională**. Acest lucru este important de reținut atunci când decideți cum să structurați companiile și unitățile organizaționale în implementarea dvs.

Când creați oportunități, cotații, contract de proiect și înregistrări de proiect, sistemul verifică dacă moneda unității contractante se potrivește cu moneda contabilă a companiei contractante. Când nu sunt la fel, aceste înregistrări nu pot fi create. Moneda unității organizaționale este definită în Dynamics 365 Project Operations accesând **Dataverse** > **Setări** > **Unități organizaționale**. Moneda contabilă a unei companii este definită în Dynamics 365 Finance accesând **Registrul general** > **Configurare registru** > **Registru**. Moneda este sincronizată cu mediul dvs. Dataverse folosind harta Ledgers Dual Write.

Sistemul creează costuri unitare de resurse și rezultate ale vânzărilor de unități interorganizaționale în următoarele situații:

  - Când unitatea de resurse diferă de unitatea contractantă
  - Când compania de resurse diferă de compania contractantă

Cu toate acestea, numai tranzacțiile care au o companie de resurse diferită de firma contractantă vor fi transferate către mediul Dynamics 365 Finance pentru contabilitate suplimentară.

Contabilitatea realității proiectului este înregistrată în jurnalul de integrare a Project Operations din Finanțe. Sistemul creează următoarele linii de jurnal.

| **Tip de tranzacție** | **Entitate juridică** | **Creează tranzacția proiectului la publicare** | **Dimensiunile financiare sunt implicite din** | **Grup implicit de impozitare pe vânzare articol de facturare și grup de impozitare pe vânzare articol de facturare** |
| --- | --- | --- | --- | --- |
| Cost | Nu este adăugat în jurnalul de integrare | N\A | N\A | N\A |
| Vânzări nefacturate | Jurnalul de integrare a persoanelor juridice de împrumut | Da | Project | **Grup de impozitare pe vânzare**: bazat pe **client contract** <br/> **Grup de impozitare pe vânzare articol de facturare**: din categoria curentă a proiectului entității juridice de pe linia jurnalului |
| Cost de unitate resursă | Jurnalul de integrare a persoanelor juridice de creditare | No | Client între companii | **Grup de impozitare pe vânzare**: bazat pe **client între companii** <br/> **Grup de impozitare pe vânzare articol de facturare**: din categoria curentă a proiectului entității juridice de pe linia jurnalului |
| Vânzări inter-organizaționale | Jurnalul de integrare a persoanelor juridice de creditare | No | Client între companii | **Grup de impozitare pe vânzare**: bazat pe **client între companii** <br/> **Grup de impozitare pe vânzare articol de facturare**: din categoria curentă a proiectului entității juridice de pe linia jurnalului |

### <a name="example-intercompany-transactions"></a>Exemplu: crearea de tranzacții între companii

Molly Clark, dezvoltator angajat în GBPM, înregistrează 10 ore de muncă împotriva unui proiect USPM Adventure Works, care este aprobat de managerul de proiect. Costul dezvoltatorului în GBPM este de 88 GBP pe oră. GBPM va factura USPM 120 USD pe oră de dezvoltator. USPM va factura clientul Adventure Works, 200 USD pentru munca efectuată de resursa GBPM. Pentru informații suplimentare, consultați [Configurarea facturării între companii](configure-intercompany-invoicing.md).

1. În Project Operations, accesați **Resurse** și selectați **Molly Clark** din listă. Pe fila **Planificare**, în câmpul **Companie**, selectați **GBPM**.
2. Accesați **Vânzări** > **Clienți** și selectați **Nou** pentru a crea un nou record de clienți pentru Adventure Works.
    1. Setați compania la **USPM**.
    2. Setați **Tipul de relație** la **Client**.
    3. Selectați **Grupul de clienți 10 - intern**.
    4. Setați moneda la **USD**.
    5. Salvaţi înregistrarea.
3. Accesați **Vânzări** > **Contracte de proiect** și creați un nou contract de proiect pentru Adventure Works.
    1. Setați firma proprietară la **USPM** iar unitatea contractantă la **Contoso Robotics SUA**.
    2. Selectați Adventure Works drept client.
    3. Selectați o listă de prețuri a produselor și salvați înregistrarea.
    4. Pe fila **Linii de contract**, creați o nouă linie de contract. Setați orice nume și selectați **Timp și materiale** ca metodă de facturare.
    5. Creați un proiect nou și asociați-l cu această linie de contract.
4. Conectați-vă ca resursă, **Molly Clark**. Accesați **Proiecte** > **Intrări de timp** și creați o intrare de timp pentru proiectul Adventure Works.
5. Conectați-vă ca manager de proiect. Accesați **Proiecte** > **Aprobări** și aprobați tranzacția de introducere a timpului înregistrată de Molly Clark.
6. Navigați la proiectul Adventure Works și selectați **Corelat** > **Date reale**. Sunt create următoarele tranzacții reale.

| **Tip de tranzacție** | **Preț** | **Monedă de tranzacționare** | **Valoare** |
| --- | --- | --- | --- |
| Cost | 120 | USD | 1200 |
| Vânzări nefacturate | 200 | USD | 2000 |
| Cost de unitate resursă | 88 | GBP | 880 |
| Vânzări unitare inter-organizaționale | 120 | USD | 1200 |

7. Conectați-vă ca contabil USPM. Deschideți instanța de finanțare a Project Operations și selectați compania **USPM**. 
8. Accesați **Management de proiect și contabilitate** > **Periodic** > **Project Operations pentru Customer Engagement** > **Import din etapă** și selectați pentru a rula procesul periodic. Acest proces periodic va completa jurnalul de integrare a Project Operations.
9. Accesați **Management de proiect și contabilitate** > **Jurnale** > **Jurnal de integrare a Project Operations** și revizuiți liniile jurnalului. Sistemul creează următoarea linie.

    | **Tip de tranzacție** | **Preț** | **Monedă de tranzacționare** | **Valoare** |
    | --- | --- | --- | --- |
    | Vânzări nefacturate | 200 | USD | 2000 |

    Dacă sistemul este configurat pentru a acumula venituri pentru acest proiect, se afișează următoarele:

    - Debit: Proiect - Valoarea vânzărilor WIP 200 USD
    - Credit: Proiect - Venituri acumulate 200 USD

    Această vânzare fără facturare este acum pregătită pentru facturare. Factura pentru clientul Adventure Works poate fi înregistrată financiar la nevoie.

10. Conectați-vă drept contabil **GBPM**. Deschideți instanța de finanțare a Project Operations și deschideți compania **GBPM**. 
11. Accesați **Management de proiect și contabilitate** > **Periodic** > **Integrarea Project Operations** > **Importați din tabelul de etapizare** și rulați procesul periodic pentru a completa Jurnalul de integrare Project Operations.
12. Accesați **Management de proiect și contabilitate** > **Jurnale** > **Jurnal de integrare a Project Operations** și revizuiți liniile. Sistemul creează următoarele linii.

    | **Tip de tranzacție** | **Preț** | **Monedă de tranzacționare** | **Valoare** |
    | --- | --- | --- | --- |
    | Cost de unitate resursă | 88 | GBP | 880 |
    | Vânzări unitare inter-organizaționale | 120 | USD | 1200 |

    Publicarea acestor înregistrări are ca rezultat următoarele tranzacții cu voucher:

    - Debit: costul proiectului este de 88 GBP
    - Credit: Alocare salarizare 88 GBP

    Dacă sistemul este configurat pentru a acumula venituri între companii se afișează următoarele:

    - Debit: Proiect - Valoarea vânzărilor WIP 120 USD
    - Credit: Proiect - Venituri acumulate 120 USD

    Sistemul este acum gata să creeze o factură client între companii.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
