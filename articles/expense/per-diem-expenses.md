---
title: Cheltuieli diurne
description: Acest articol oferă informații despre cum să lucrați cu cheltuielile diurne.
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
> Funcționalitatea descrisă în acest articol este disponibilă pentru utilizatorii vizați ca parte a unei versiuni de previzualizare.

O plată diurnă este o indemnizație zilnică fixă, predeterminată, pe care o companie o plătește angajaților săi pentru cazare (hoteluri), masă și cheltuieli accesorii pe care acești angajați le suportă în timp ce călătoresc la serviciu. Compania plătește această indemnizație angajaților în loc să plătească cheltuielile efective de deplasare. Angajații își pot folosi **Incidental/Altele** alocație diurnă pentru a acoperi bacșișuri, room service, spălătorie sau curățătorie chimică pentru întâlniri importante de afaceri. Rata diurnă poate varia, în funcție de dacă angajatorul alege să ramburseze costul combinat de cazare și masă sau numai pentru costul mesei și cheltuielilor.

Tarifele diurnei se pot baza pe perioada anului, locația călătoriei sau ambele. Când creați o regulă diurnă, puteți specifica că un procent din rata diurnă va fi reținut dacă un angajat primește mese sau servicii gratuite. De asemenea, puteți seta un număr minim de ore și un număr maxim de ore în care rata diurnă poate fi aplicată călătoriei unui angajat.

Diurna este calculată ca alocația totală oferită pe zi minus reducerea de masă (costul meselor gratuite) care este oferită angajatului.

## <a name="configure-per-diems"></a>Configurați diurna

Pentru a configura cheltuielile diurne, urmați acești pași.

1. Mergi la **Managementul cheltuielilor** \> **Înființat** \> **General** \> **Parametrii de gestionare a cheltuielilor**.
2. Pe **Diurnă** fila, în **Calculați reducerea de masă prin** câmp, selectați cum trebuie calculate diurnele:

    - **Tipul de masă pe călătorie** – Calculați diurna în funcție de tipul de masă introdus (mic dejun, prânz sau cină) și de reducerea de masă care este specificată pentru fiecare tip de masă pentru alocația diurnă pe durata călătoriei.
    - **Tip de masă pe zi** – Calculați diurna în funcție de tipul de masă introdus și de reducerea de masă care este specificată pentru fiecare tip de masă pentru indemnizația de diurnă pe zi.
    - **Numărul de mese pe zi** – Calculați diurna în funcție de numărul de mese introduse pe zi și de reducerea de masă pentru numărul de mese care se asigură în fiecare zi.

3. Mergi la **Managementul cheltuielilor** \> **Înființat** \> **Calcule și coduri** \> **Locații diurne**.
4. Adăugați locații în care pot fi utilizate diurne.
5. Pentru fiecare locație pe care o adăugați, pe **Diurne** fila, selectați rata diurnă și moneda care sunt valabile între anumite date de început și de încheiere pentru cazare, masă și alte cheltuieli. Pentru a configura ratele diurne și monedele, accesați **Managementul cheltuielilor** \> **Înființat** \> **Calcule și coduri** \> **Diurne**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Diurne în interfața de cheltuieli reimaginată

Funcția diurnă este acceptată în reimaginat **Managementul cheltuielilor** spațiu de lucru în Microsoft Dynamics 365 Finance versiunea 10.0.25 și ulterioară.

Pentru a activa diurna, urmați acești pași.

1. În **Managementul caracteristicilor** spațiu de lucru, găsiți și selectați **Rapoartele de cheltuieli reimaginate** caracteristică din listă, apoi selectați **Activați acum**.
2. Găsiți și selectați **Diurnă pentru raportul de cheltuieli interfață reimaginată** caracteristică din listă, apoi selectați **Activați acum**.

## <a name="how-the-feature-works"></a>Cum funcționează caracteristica

Această secțiune oferă exemple pentru trei scenarii de configurare. Pentru fiecare exemplu, **Calculați reducerea de masă prin** câmpul este setat la o valoare diferită. Pentru toate cele trei exemple, suma totală care se plătește este aceeași până la aplicarea reducerii de masă. După acest punct, suma totală de plătit diferă pentru fiecare exemplu.

Pentru a crea cheltuiala diurnă care este utilizată pentru toate cele trei exemple, urmați acești pași.

1. Mergi la **Spații de lucru** \> **Managementul cheltuielilor**.
2. Selectați **Un nou raport de cheltuieli** sau selectați un raport de cheltuieli existent.
3. Adăugați o nouă cheltuială. În **Categorie** câmp, selectați **Diurnă**. Selectați locația și datele de început și de sfârșit ale călătoriei dvs. Diurna pentru cazare, masă și accesorii (alte cheltuieli) se calculează pe baza indemnizației zilnice stabilite pentru locația selectată.

    De exemplu, tu selectezi **Redmond (SUA)** ca locatie. Alocația zilnică pentru acea locație este de 150 de dolari SUA (150 USD) pentru cazare, USD 75 pentru mese și USD 5 pentru incidente. Data de începere este 10 ianuarie, iar data de încheiere este 14 ianuarie. Prin urmare, durata selectată este de cinci zile când configurația selectată este zile calendaristice cu ora, iar ora selectată începe și se termină la ora 12:00 la datele de început și de sfârșit. Iată calculele:

    - Suma totală de plătit = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Masa și porțiunea ocazională din suma totală = 5 × (75 + 5) = USD 400

Dacă micul dejun, prânzul și cina au fost oferite în timpul călătoriei, acele mese trebuie luate în considerare ca o reducere de masă.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemplul 1: Diurnă în care reducerile de masă se bazează pe tipul de masă per călătorie

În acest exemplu, reducerea de masă este de 30% pentru micul dejun, 30% pentru prânz și 40% pentru cină. Pe **Parametrii de management al cheltuielilor** pagina, cel **Calculați reducerea de masă prin** câmpul este setat la **Tipul de masă pe călătorie**. Iată calculele dacă angajatului i-au fost oferite trei mic dejun, două prânzuri și zero cine:

- Reducerea mesei = (3 ×\[ 75 × 30%\]) + (2 ×\[ 75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Mese și accesorii = 400 – 112,50 = USD 287.50
- Suma totală de plătit = Total indemnizație – Reducere de masă = 1.150 – 112,50 = USD 1,037.50

![Cheltuială diurnă în cazul în care reducerea de masă se bazează pe tipul de masă per călătorie.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemplul 2: Diurnă în care reducerile de masă se bazează pe tipul de masă pe zi

În acest exemplu, reducerea de masă este de 30% pentru micul dejun, 30% pentru prânz și 40% pentru cină. Pe **Parametrii de management al cheltuielilor** pagina, cel **Calculați reducerea de masă prin** câmpul este setat la **Tip de masă pe zi**. În acest caz, în **Mesele** grilă în **Editați cheltuielile** caseta de dialog, debifați casetele de selectare pentru a indica ce mese vi s-au oferit în timpul călătoriei.

De exemplu, iată calculele dacă micul dejun a fost oferit în primele trei zile ale călătoriei:

- Reducerea mesei zilnice pentru fiecare dintre primele trei zile = 75 × 30% = USD 22.50
- Reducerea totală a mesei = 3 × 22,50 = USD 67.50
- Mese și accesorii pentru zilele 1 până la 3 = 75 – 22.50 = USD 57.50
- Total mese și incidente = Suma meselor și incidentelor pe parcursul a cinci zile = 400 – 67,50 = USD 332.50
- Suma totală de plătit = Suma totală – Reducerea mesei = 1.150 – 67,50 = USD 1,082.50

![Cheltuieli diurne în care reducerea de masă se bazează pe tipul de masă pe zi.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemplul 3: Diurnă în care reducerile de masă se bazează pe numărul de mese pe zi

În acest exemplu, reducerea de masă este calculată pe baza numărului de mese care au fost furnizate pe zi (adică, **Calculați reducerea de masă prin** câmp de pe **Parametrii de management al cheltuielilor** pagina este setată la **Numărul de mese pe zi**). În **Mesele** grilă în **Editați cheltuielile** caseta de dialog, debifați casetele de selectare pentru a indica ce mese au fost furnizate.
În acest caz, reducerea de masă se bazează doar pe numărul de mese oferite, și nu pe tipul de masă (Mic dejun/pranz/cina) oferit.

Iată calculele pentru diurne atunci când alocația zilnică este USD 150 pentru cazare, USD 75 pentru mese și USD 5 pentru incidente:

- **Suma totală de plătit** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **O masa:** Reducerea mesei = 20% = USD 15
- **Doua mese:** Reducerea mesei = 50% = USD 37.50
- **Trei mese:** Reducerea mesei = 100% = USD 75

Iată calculele pentru **indemnizatie de masa si accesorii**, care include USD 5 pentru incidente:

- Ziua 1 - Două mese asigurate = (75 – 37.50) + 5 = 37.50 + 5 = USD 42.50
- Ziua 2 - Două mese asigurate = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Ziua 3 - O masă asigurată = (75 – 15) + 5 = 60 + 5 = USD 65
- Ziua 4 - Zero mese asigurate = (75-0) + 5 = 75 + 5 = USD 80
- Ziua 5 - Trei mese asigurate = (75 – 75) + 5 = 0 + 5 = USD 5

- Total mese și incidente = Mese și incidente pentru Ziua 1+ Ziua 2 +Ziua 3+Ziua 4+ Ziua 5 = USD 235
- Reducerea totală a mesei = Reducerea mesei pentru Ziua 1+ Ziua 2 +Ziua 3+Ziua 4+ Ziua 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Suma totală de plătit = Total alocație – Reducerea totală a mesei = USD 1,150 - USD 165 = USD 985

![Cheltuieli diurne în care reducerea de masă se bazează pe numărul de mese pe zi.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Începând cu versiunea Finance 10.0.23, dacă utilizați interfața de cheltuieli reimaginată, nu puteți crea cheltuieli diurne care au date suprapuse. Dacă încercați, veți primi un mesaj de eroare.
