---
title: Cheltuieli diurne
description: Acest articol oferă informații despre cum să lucrați cu cheltuielile pentru diurnă.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923203"
---
# <a name="per-diem-expenses"></a>Cheltuieli diurne

> [!IMPORTANT] 
> Funcționalitatea descrisă în acest articol este disponibilă pentru utilizatorii vizați ca parte a unei versiuni preliminare.

O plată pentru diurnă reprezintă o indemnizație zilnică fixă, prestabilită, pe care o companie o plătește angajaților săi pentru cazare (hoteluri), masă și cheltuieli suplimentare pe care respectivii angajați le suportă în timp ce călătoresc în interes de serviciu. Compania plătește această indemnizație angajaților în loc să plătească cheltuielile efective de deplasare. Angajații își pot folosi indemnizația zilnică **Cheltuieli suplimentare/Altele** pentru a acoperi bacșișuri, room service, spălătorie sau servicii de curățatorie chimică pentru întâlniri importante de afaceri. Tariful de diurnă poate varia, în funcție de alegerea angajatoruljui de a rambursa costul combinat de cazare și masă sau numai costul meselor și al cheltuielilor suplimentare.

Tarifele diurnei se pot baza pe perioada anului, locația călătoriei sau ambele. Când creați o regulă de diurnă, puteți specifica că un procent din tariful de diurnă va fi reținut dacă un angajat primește mese sau servicii gratuite. De asemenea, puteți seta un număr minim de ore și un număr maxim de ore la care se poate aplica tariful de diurnă pentru deplasarea unui angajat.

Diurna este calculată ca indemnizația totală care este oferită pe zi minus reducerea de masă (costul meselor gratuite) care este oferită angajatului.

## <a name="configure-per-diems"></a>Configurarea diurnei

Pentru a configura cheltuielile pentru diurnă, urmați acești pași:

1. Accesați **Managementul cheltuielilor** \> **Configurare** \> **General** \> **Parametrii de gestionare a cheltuielilor**.
2. Pe fila **Diurnă**, în câmpul **Calculați reducerea de masă prin**, selectați cum trebuie calculate diurnele:

    - **Tipul de masă pe deplasare** – Calculați diurna în funcție de tipul de masă introdus (mic dejun, prânz sau cină) și de reducerea de masă care este specificată pentru fiecare tip de masă pentru indemnizația pentru diurnă pe durata deplasării.
    - **Tipul de masă pe zi** – Calculați diurna în funcție de tipul de masă introdus (mic dejun, prânz sau cină) și de reducerea de masă care este specificată pentru fiecare tip de masă pentru indemnizația pentru diurnă pe zi.
    - **Numărul de mese pe zi** – Calculați diurna în funcție de numărul de mese introduse pe zi și de reducerea de masă pentru numărul de mese care se asigură în fiecare zi.

3. Accesați **Managementul cheltuielilor** \> **Configurare** \> **Calcule și coduri** \> **Locații diurne**.
4. Adăugați locații în care pot fi utilizate diurnele.
5. Pentru fiecare locație pe care o adăugați, pe fila **Diurne** selectați tariful pentru diurnă și moneda care este valabilă între anumite date de începere și de sfârșit pentru cazare, mese și alte cheltuieli. Pentru a configura tarifele pentru diurnă și monedele, accesați **Managementul cheltuielilor** \> **Configurare** \> **Calcule și coduri** \> **Diurne**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Diurne în interfața de cheltuieli reimaginată

Funcția diurnă este acceptată în spațiul de lucru reimaginat **Managementul cheltuielilor** în Microsoft Dynamics 365 Finance, versiunea 10.0.25 și ulterioară.

Pentru a activa diurnele, urmați acești pași.

1. În spațiul de lucru **Managementul caracteristicilor**, găsiți și selectați caracteristica în lista **Rapoarte de cheltuieli reimaginate**, apoi selectați **Activați acum**.
2. Găsiți și selectați caracteristica în lista **Diurne pentru interfața reimaginată pentru rapoarte de cheltuieli**, apoi selectați **Activați acum**.

## <a name="how-the-feature-works"></a>Cum funcționează caracteristica

Această secțiune oferă exemple pentru trei scenarii de configurare. Pentru fiecare exemplu, câmpul **Calculați reducerea de masă prin** este setat la o valoare diferită. Pentru toate cele trei exemple, suma totală care se plătește este aceeași până la aplicarea reducerii de masă. După acest punct, suma totală de plătit diferă pentru fiecare exemplu.

Pentru a crea cheltuiala pentru diurnă care este utilizată pentru toate cele trei exemple, urmați acești pași.

1. Accesați **Spații de lucru** \> **Managementul cheltuielilor**.
2. Selectați **Raport de cheltuieli nou** sau selectați un raport de cheltuieli existent.
3. Adăugarea unei cheltuieli noi În câmpul **Categorie**, selectați **Diurnă**. Selectați locația și datele de început și de sfârșit ale călătoriei dvs. Diurna pentru cazare, masă și cheltuieli suplimentare (alte cheltuieli) se calculează pe baza indemnizației zilnice stabilite pentru locația selectată.

    De exemplu, dvs. selectați **Redmond (S.U.A)** ca locație. Indemnizația zilnică pentru acea locație este de 150 de dolari S.U.A. (150 USD) pentru cazare, 75 USD pentru mese și 5 USD pentru cheltuieli suplimentare. Data de începere este 10 ianuarie, iar data de încheiere este 14 ianuarie. Prin urmare, durata selectată este de cinci zile când configurația selectată este zile calendaristice cu ora, iar ora selectată începe și se termină la ora 12:00 la datele de început și de sfârșit. Iată calculele:

    - Suma totală de plătit = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Masa și porțiunea pentru cheltuieli suplimentare din suma totală = 5 × (75 + 5) = 400 USD

Dacă micul dejun, prânzul și cina au fost oferite în timpul călătoriei, acele mese trebuie luate în considerare ca o reducere pentru masă.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemplul 1: Diurnă în care reducerile pentru masă se bazează pe tipul de masă per călătorie

În acest exemplu, reducerea pentru masă este de 30% pentru micul dejun, 30% pentru prânz și 40% pentru cină. Pe pagina **Parametrii de gestionare a cheltuielilor**, câmpul **Calculați reducerea de masă prin** este setat la **Tipul de masă per călătorie**. Iată calculele dacă angajatului i-au fost oferite trei mese de tip mic dejun, două prânzuri și zero mese de tip cină:

- Reducerea pentru masă = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Mese și cheltuieli suplimentare = 400 – 112,50 = 287,50 USD
- Suma totală de plată = Total indemnizație – Reducere pentru masă = 1.150 – 112,50 = 1.037,50 USD

![Cheltuială pentru diurnă în care reducerea pentru masă se bazează pe tipul de masă per deplasare.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemplul 2: Diurnă în care reducerile pentru masă se bazează pe tipul de masă pe zi

În acest exemplu, reducerea pentru masă este de 30% pentru micul dejun, 30% pentru prânz și 40% pentru cină. Pe pagina **Parametrii de gestionare a cheltuielilor**, câmpul **Calculați reducerea de masă prin** este setat la **Tipul de masă pe zi**. În acest caz, în grila **Mese** în caseta de dialog **Editați cheltuielile**, debifați casetele de selectare pentru a indica ce mese vi s-au oferit în timpul călătoriei.

De exemplu, iată calculele dacă micul dejun a fost oferit în primele trei zile ale călătoriei:

- Reducerea zilnică pentru masă pentru fiecare dintre primele trei zile = 75 × 30% = 22,50 USD
- Reducerea totală pentru masă = 3 × 22,50 = 67,50 USD
- Mese și cheltuielile suplimentare pentru zilele 1 până la 3 = 75 – 22,50 = 57,50 USD
- Total mese și cheltuieli suplimentare = Suma meselor și cheltuielilor suplimentare pe parcursul a cinci zile = 400 – 67,50 = 332,50 USD
- Suma totală de plată = Suma totală – Reducere pentru masă = 1.150 – 67,50 = 1.082,50 USD

![Cheltuială pentru diurnă în care reducerea pentru masă se bazează pe tipul de masă pe zi.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemplul 3: Diurnă în care reducerile pentru masă se bazează numărul de mese pe zi

În acest exemplu, reducerea de masă este calculată pe baza numărului de mese care au fost oferite pe zi (mai exact, câmpul **Calculați reducerea pentru masă prin** de pe pagina **Parametrii de gestionare a cheltuielilor** este setat la **Numărul de mese pe zi**). În grila **Mese** în caseta de dialog **Editați cheltuielile**, debifați casetele de selectare pentru a indica ce mese vi s-au oferit.
În acest caz, reducerea pentru masă se bazează doar pe # de mese oferite și nu pe tipul de masă (Mic dejun/prânz/cină) oferit.

Iată calculele pentru diurne când indemnizația zilnică este de 150 USD pentru cazare, 75 USD pentru masă și 5 USD pentru cheltuieli suplimentare:

- **Suma totală de plată** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **O masă:** Reducerea pentru masă = 20% = 15 USD
- **Două mese:** Reducerea pentru masă = 50% = 37,50 USD
- **Trei mese:** Reducerea pentru masă = 100% = 75 USD

Iată calculele pentru **indemnizația pentru masă și cheltuieli suplimentare**, care include 5 USD pentru cheltuielile suplimentare:

- Ziua 1 – Două mese asigurate = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Ziua 2 – Două mese asigurate = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Ziua 3 – O masă asigurată = (75 – 15) + 5 = 60 + 5 = 65 USD
- Ziua 4 – Zero mese asigurate = (75 – 0) + 5 = 75 + 5 = 80 USD
- Ziua 5 – Trei mese asigurate = (75 – 75) + 5 = 0 + 5 = 5 USD

- Total mese și cheltuieli suplimentare = Mese și cheltuieli suplimentare pentru Ziua 1 + Ziua 2 + Ziua 3 + Ziua 4 + Ziua 5 = 235 USD
- Reducerea totală pentru masă = Reducerea pentru masă pentru Ziua 1 + Ziua 2 + Ziua 3 + Ziua 4 + Ziua 5 = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Suma totală de plată = Total indemnizație – Total reducere pentru masă = 1.150 – 165 = 985 USD

![Cheltuială pentru diurnă în care reducerea pentru masă se bazează pe numărul de mese pe zi.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Începând cu versiunea Finance 10.0.23, dacă utilizați interfața de cheltuieli reimaginată, nu puteți crea cheltuieli diurne care au date suprapuse. Dacă încercați, veți primi un mesaj de eroare.
