---
title: Configurați gestionarea cheltuielilor
description: Acest articol descrie considerațiile și deciziile pe care trebuie să le luați în timpul procesului de planificare înainte de a configura gestionarea cheltuielilor în Microsoft Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9424b8aaf867254bde085cffaa649c846920cc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934013"
---
# <a name="configure-expense-management"></a>Configurați gestionarea cheltuielilor

Acest articol descrie considerațiile și deciziile pe care trebuie să le luați în timpul procesului de planificare înainte de a configura gestionarea cheltuielilor. În Gestionarea cheltuielilor, puteți stoca informații despre metodele de plată, cererile de călătorie, rapoartele de cheltuieli, politicile și așa mai departe.

Deoarece multe dintre deciziile pe care le luați atunci când vă planificați configurația pentru gestionarea cheltuielilor se bazează pe ierarhia și structura financiară a organizației dvs., trebuie să consultați documentele de planificare pentru acele domenii.

## <a name="intercompany-expenses"></a>Cheltuieli între companii

Când activați cheltuielile între companii, permiteți persoanelor juridice și angajaților să suporte cheltuieli în numele altei persoane juridice și să colecteze plata de la entitatea juridică de angajare din cadrul organizației dvs. De exemplu, un angajat al persoanei juridice A finalizează un proiect pentru persoana juridică B, iar proiectul suportă cheltuieli legate de călătorie. Dacă sunt activate cheltuielile între companii, angajatul poate depune apoi un raport de cheltuieli care va înregistra cheltuielile către persoana juridică B, iar cheltuielile trebuie apoi plătite de persoana juridică A. Dacă organizația dvs. nu are mai multe persoane juridice, nu aveți nu trebuie să permită cheltuielile între companii.

**Decizie:** Doriți să activați cheltuielile între companii?

## <a name="financial-management"></a>Gestiune financiară

Managementul cheltuielilor este strâns integrat cu managementul financiar al organizației dumneavoastră. O mulțime de configurații pentru gestionarea cheltuielilor se vor baza pe deciziile pe care le-ați luat cu privire la finanțele organizației dvs. Următoarele secțiuni descriu diferitele domenii care necesită planificare și decizii, pe baza deciziilor financiare și a îndrumărilor organizației dvs. din partea echipei de conducere.

### <a name="per-diems"></a>Diurne

Trebuie să definiți dietele angajaților pe care le oferă organizația dvs. Deoarece diurnele sunt utilizate în mod obișnuit pentru acoperirea cheltuielilor, cum ar fi mesele, cazarea și alte cheltuieli accidentale, puteți crea reguli pentru indemnizațiile per diem pe care le oferă organizația dvs. ratele diurnei se pot baza pe perioada anului, locația călătoriei sau ambele. Când definiți o regulă de diurnă, puteți specifica că un procent din rata diemului va fi reținut dacă un lucrător primește mese sau servicii gratuite. De asemenea, puteți defini nivelurile de rate de diurnă pentru a configura numărul minim și maxim de ore pentru care poate fi aplicat diurnei pentru călătoria unui lucrător.

**Decizii**

- Reguli implicite pentru diurnă pentru prima și ultima zi:

    - Care este numărul minim de ore pe care un angajat îl poate solicita pentru o zi și totuși primește o diurnă?
    - Există o reducere a sumei oferite pentru mesele din prima zi și ultima zi? Dacă există o reducere, care este procentul reducerii?
    - Există o reducere a sumei oferite pentru un hotel pentru prima zi și ultima zi? Dacă există o reducere, care este procentul reducerii?
    - Există o reducere a sumei oferite pentru alte cheltuieli care sunt percepute pentru prima zi și ultima zi? Dacă există o reducere, care este procentul reducerii?

- Reguli implicite de dirună:

    - Există o reducere procentuală a indemnizației per diem pentru fiecare masă dacă, de exemplu, masa este gratuită? Dacă există o reducere, care este procentul reducerii pentru fiecare masă?
    - Reducerea meselor este calculată pe zi, pe călătorie sau în funcție de numărul de mese pe zi?
    - Sumele diurnelor trebuie rotunjite în mod obișnuit sau rotunjite în sus?
    - Sunt diurnele calculate pe o perioadă de 24 de ore sau într-o zi calendaristică?

- Regulile de diurnă care se bazează pe locație:

    - Tarifele diurnei variază în funcție de locație? Ce locații sunt incluse?
    - Dacă tarifele diurnei variază în funcție de locație, pentru fiecare locație, ce procentaj este prevăzut pentru următoarele tipuri de cheltuieli:

        - Mese
        - Hotel
        - Alte cheltuieli

### <a name="expense-management-journals-and-accounts"></a>Jurnalele și conturile de gestionare a cheltuielilor

Gestionarea cheltuielilor necesită utilizarea mai multor jurnale și conturi. Trebuie să decideți, de exemplu, dacă același cont este utilizat pentru avansuri de numerar și litigii legate de cardul de credit.

**Decizii**

- În ce jurnal contabil sunt afișate rapoartele de cheltuieli aprobate?
- Ce cont este utilizat pentru avansuri de numerar?
- Ar trebui ca avansurile de numerar să fie înregistrate imediat?

### <a name="payment-methods"></a>Metode de plată

Atunci când permiteți angajaților să suporte cheltuieli în numele afacerii dvs., trebuie să definiți metodele de plată pe care angajații au voie să le folosească. De exemplu, puteți permite angajaților să folosească numerar sau un card de credit corporativ. De asemenea, puteți permite angajaților să utilizeze carduri de credit personale și apoi să le rambursați angajaților. Trebuie să luați următoarele decizii pentru fiecare metodă de plată pe care o permiteți.

**Decizii**

- Ce metode de plată sunt permise?
- Cine deține cheltuielile cu metoda de plată?
- Există un tip de cont compensat? Dacă există un tip de cont compensat, ce este?
- Dacă există un tip de cont compensat, care este contul?
- Dacă metoda de plată este un card de credit, metoda de plată ar trebui utilizată numai cu tranzacțiile importate?

### <a name="expense-categories-and-shared-categories"></a>Categorii de cheltuieli și categorii partajate

Când angajații creează un raport de cheltuieli, fiecare cheltuială pe care o înregistrează trebuie să fie asociată unei categorii de cheltuieli. Categoriile de cheltuieli sunt derivate din categorii comune care pot fi partajate între entitățile juridice din organizația dvs. Aceste categorii pot fi, de asemenea, partajate în managementul de proiect și contabilitate, în funcție de modul în care este definită organizația dvs. Pe baza definiției organizației dvs. și a îndrumărilor din partea echipei de implementare, trebuie să determinați dacă categoriile care sunt utilizate în gestionarea cheltuielilor vor fi utilizate numai în gestionarea cheltuielilor sau dacă ar trebui să fie partajate între Gestionarea proiectului și contabilitate și Gestionarea cheltuielilor. Rețineți că aceste categorii pot fi împărțite între Proiect și Cheltuială sau Proiect și Producție, dar nu între Cheltuială și Producție. Trebuie să luați următoarele decizii pentru fiecare categorie de cheltuieli.

**Decizii**

- Care este categoria de cheltuieli? Exemplele includ categorii pentru zboruri, hotel sau kilometraj.
- Categoria de cheltuieli poate fi utilizată și în managementul proiectelor și contabilitate?
- Care este tipul de cheltuieli?
- Care este metoda de plată implicită pentru categoria de cheltuieli?
- Cheltuielile din categoria cheltuielilor trebuie să fie detaliate?
- Care este contul principal implicit pentru categoria de cheltuieli?
- Care este grupul implicit de impozitare pe vânzări pentru categoria de cheltuieli?
- Sunt permise metode de plată suplimentare pentru categoria de cheltuieli? Dacă sunt permise metode de plată suplimentare, care sunt acestea?
- Există subcategorii în această categorie de cheltuieli? Dacă sunt subcategorii, trebuie să luați și următoarele decizii:

    - Există vreuna dintre subcategoriile excluse din recuperarea impozitelor?
    - Care este grupul de taxe pe vânzări de articole din subcategorii?

Dacă categoria de cheltuieli este utilizată și în managementul de proiect și contabilitate, răspundeți la întrebările rămase. În caz contrar, treceți la secțiunea următoare.

- Ce conturi de costuri vor fi utilizate pentru următoarele cheltuieli?

    - Cost
    - Alocare stat de plată
    - WIP-valoare de cost
    - Cost-element
    - WIP-valoare de cost-element
    - Pierderi acumulate
    - WIP-pierderi acumulate

- Ce conturi de venituri vor fi utilizate pentru următoarele?

    - Venituri facturate
    - Venit acumulat-valoarea vânzărilor
    - WIP-valoarea vânzărilor
    - Producție de venituri acumulate
    - WIP-producție
    - Venituri acumulate-profit
    - WIP-profit
    - Venituri acumulate-abonament
    - WIP-abonament

### <a name="taxes"></a>Impozite

Pentru taxele legate de cheltuieli, trebuie să determinați ce este inclus sau activat în rapoartele de cheltuieli.

**Decizii**

- Impozitul pe vânzări este inclus în sumele cheltuielilor?
- Ar trebui să se permită recuperarea impozitelor la cheltuieli?

    > [!NOTE]
    > Când planificați registrul general, dacă ați decis să aplicați impozitul pe vânzări în SUA și să utilizați regulile fiscale, nu puteți activa recuperarea impozitului pe cheltuieli. (Pentru a aplica impozitul pe vânzări în SUA și a utiliza regulile fiscale, setați opțiunea **Aplicați regulile privind impozitarea pe vânzări** la **Da**.)

## <a name="policies"></a>Politici

Prin crearea politicilor de raportare a cheltuielilor, vă puteți ajuta organizația să economisească timp și bani atunci când angajații suportă cheltuieli în numele acesteia. Politicile contribuie la garantarea faptului că angajații rămân în buget, furnizează toate informațiile necesare și cheltuiesc bani numai după cum au nevoie. Trebuie să luați următoarele decizii pentru fiecare politică de raportare a cheltuielilor și pentru fiecare politică de aprobare a raportului de cheltuieli pe care o creați.

**Decizii**

- Care este numele politicii?
- Pentru ce este politica de cheltuieli?
- Dacă ați decis anterior să activați cheltuielile între companii, la ce companii din organizația dvs. se va aplica această politică?
- Când devine eficientă politica?
- Când expiră politica?
- Care este regula politicii?
- Care este rezultatul regulii politicii?


[!INCLUDE[footer-include](../includes/footer-banner.md)]