---
title: Date reale
description: Acest subiect oferă informații despre cum să lucrați cu cifrele reale în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996626"
---
# <a name="actuals"></a>Date reale 

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Valorile reale reprezintă progresul financiar revizuit și aprobat și evoluția planificată a unui proiect. Acestea sunt create ca urmare a aprobării timpului, cheltuielilor, înregistrărilor de utilizare a materialelor, înregistrărilor din jurnal și facturilor.

## <a name="journal-lines-and-time-submission"></a>Liniile de jurnal și remiteri de timp

Pentru mai multe informații despre remiteri de timp, consultați [Prezentare generală a intrării de timp](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Timp și materiale

Atunci când o intrare de timp care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.

### <a name="fixed-price"></a>Preț fix

Atunci când o intrare de timp care este remisă este legată de un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.

### <a name="default-pricing"></a>Tarifare implicită

Logica pentru crearea prețurilor implicite se află pe linia de jurnal. Valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal. Aceste valori includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare.

Câmpurile care afectează stabilirea implicită a prețurilor, cum ar fi **Rol** și **Unitate de resurse**, sunt utilizate pentru a determina prețul adecvat în linia de jurnal. Puteți adăuga un câmp personalizat la intrarea în timp. Dacă doriți ca valoarea câmpului să fie propagată la valorile reale, creați câmpul în tabelele **Valori reale** și **Linie de jurnal**. Utilizați codul personalizat pentru a propaga valoarea câmpului selectat de la introducerea timpului la valori efective prin linia jurnal folosind originile tranzacției. Pentru mai multe informații despre originile tranzacțiilor și conexiuni, consultați [Conectarea valorilor reale la înregistrările originale](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Liniile de jurnal și remiterea cheltuielilor de bază

Pentru mai multe informații despre intrări de cheltuială [Prezentare generală a cheltuielii](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Timp și materiale

Atunci când o intrare de cheltuială de bază care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.

### <a name="fixed-price"></a>Preț fix

Atunci când o intrare de cheltuieli de bază remisă este legată la un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.

### <a name="default-pricing"></a>Tarifare implicită

Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli. Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare. Câmpurile care afectează stabilirea implicită a prețurilor, cum ar fi **Categoria tranzacției** și **Unitate**, sunt utilizate pentru a determina prețul adecvat în linia de jurnal. Cu toate acestea, acest lucru funcționează numai atunci când metoda de stabilire a prețurilor din lista de prețuri este **Preț unitar**. Dacă metoda de stabilire a prețurilor este **La cost** sau **Adaos peste cost**, prețul introdus la crearea înregistrării de cheltuieli este utilizat pentru cost și prețul de pe linia jurnalului de vânzări este calculat pe baza metodei de stabilire a prețurilor. 

Puteți adăuga un câmp personalizat la intrarea de cheltuieli. Dacă doriți ca valoarea câmpului să fie propagată la valorile reale, creați câmpul în tabelele **Valori reale** și **Linie de jurnal**. Utilizați codul personalizat pentru a propaga valoarea câmpului selectat de la introducerea timpului la valori efective prin linia jurnal folosind originile tranzacției. Pentru mai multe informații despre originile tranzacțiilor și conexiuni, consultați [Conectarea valorilor reale la înregistrările originale](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Liniile jurnalului și trimiterea jurnalului de utilizare a materialelor

Pentru mai multe informații despre introducerea cheltuielilor, consultați [Jurnal de utilizare a materialelor](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Timp și materiale

Atunci când o înregistrare de utilizare a materialului trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.

### <a name="fixed-price"></a>Preț fix

Atunci când o intrare remisă de jurnal de utilizare de material este legată de un proiect mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.

### <a name="default-pricing"></a>Tarifare implicită

Logica pentru introducerea prețurilor implicite pentru material se bazează pe combinația de produse și unități. Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare. Câmpurile care afectează stabilirea implicită a prețurilor, cum ar fi **ID produs** și **Unitate**, sunt utilizate pentru a determina prețul adecvat în linia de jurnal. Cu toate acestea, acest lucru funcționează numai pentru produsele din catalog. Pentru produsele din afara catalogului, prețul introdus la crearea înregistrării jurnalului de utilizare a materialului este utilizat pentru cost și prețul de vânzare pe liniile jurnalului. 

Puteți adăuga un câmp personalizat la intrarea **Jurnal de utilizare materiale**. Dacă doriți ca valoarea câmpului să fie propagată la valorile reale, creați câmpul în tabelele **Valori reale** și **Linie de jurnal**. Utilizați codul personalizat pentru a propaga valoarea câmpului selectat de la introducerea timpului la valori efective prin linia jurnal folosind originile tranzacției. Pentru mai multe informații despre originile tranzacțiilor și conexiuni, consultați [Conectarea valorilor reale la înregistrările originale](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utilizați intrările de jurnal pentru a înregistra costurilr

Puteți utiliza intrările de jurnal pentru a înregistra costul sau venitul în material, tarif, timp, cheltuieli sau clase de taxe de tranzacții. Jurnalele pot fi utilizate în următoarele scopuri:

- Mutați valorile reale privind tranzacțiile dintr-un alt sistem în Microsoft Dynamics 365 Project Operations.
- Înregistrați costurile care au avut loc într-un alt sistem. Aceste costuri pot include costuri de achiziție sau subcontractare.

> [!IMPORTANT]
> Aplicația nu validează tipul liniei jurnalului sau prețurile aferente care sunt introduse pe linia jurnalului. Prin urmare, numai un utilizator care este pe deplin conștient de impactul contabil pe care îl au efectele reale asupra proiectului ar trebui să utilizeze jurnale de intrare pentru a crea date reale. Datorită impactului acestui tip de jurnal, ar trebui să alegeți cu atenție cine are acces pentru a crea jurnale de intrare.

## <a name="record-actuals-based-on-project-events"></a>Înregistrați valorile reale pe baza evenimentelor proiectului

Project Operations înregistrează tranzacțiile financiare care apar în timpul unui proiect. Aceste tranzacții sunt înregistrate ca valori reale. Tabelele următoare arată diferitele tipuri de valori reale care sunt create, în funcție de faptul dacă proiectul este un proiect pe bază de timp și materiale sau un proiect cu preț fix, este în etapa de prevânzare sau este un proiect intern.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Resursa aparține aceleiași unități organizatorice ca și unitatea contractantă a proiectului

<table>
<thead>
<tr>
<th rowspan="3">Eveniment</th>
<th colspan="4">Proiect facturabil sau vândut</th>
<th rowspan="3">Proiect în etapa de prevânzare</th>
<th rowspan="3">Proiect intern</th>
</tr>
<tr>
<th colspan="2">Timp și materiale</th>
<th colspan="2">Preț fix</th>
</tr>
<tr>
<th>Reale</th>
<th>Monedă de tranzacționare</th>
<th>Preț fix</th>
<th>Monedă de tranzacționare</th>
</tr>
</thead>
<tbody>
<tr>
<td>Este creată o intrare de timp.</td>
<td colspan="6">Nicio activitate în entitatea Valori reale</td>
</tr>
<tr>
<td>Este remisă o intrare de timp.</td>
<td colspan="6">Nicio activitate în entitatea Valori reale</td>
</tr>
<tr>
<td rowspan="2">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</td>
<td>Cost real</td>
<td>Moneda unității contractante</td>
<td rowspan="2">Cost real</td>
<td rowspan="2">Moneda unității contractante
<td rowspan="2">Cost real</td>
<td rowspan="2">Cost real</td>
</tr>
<tr>
<td>Valoare reală vânzări nefacturate – taxabilă</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="3">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</td>
<td>Cost real</td>
<td>Moneda unității contractante</td>
<td rowspan="3">Cost real</td>
<td rowspan="3">Moneda unității contractante</td>
<td rowspan="3">Cost real</td>
<td rowspan="3">Cost real</td>
</tr>
<tr>
<td>Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Valoare reală vânzări nefacturate – netaxabile pentru diferență</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="2">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</td>
<td>Inversare vânzări nefacturate</td>
<td>Monedă contract pentru proiect</td>
<td rowspan="2">Vânzări facturate pentru jalon</td>
<td rowspan="2">Monedă contract pentru proiect</td>
<td rowspan="2">Nu se aplică</td>
<td rowspan="2">Nu se aplică</td>
</tr>
<tr>
<td>Vânzări facturate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="3">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</td>
<td>Inversare vânzări nefacturate</td>
<td>Monedă contract pentru proiect</td>
<td rowspan="3">Nu se aplică</td>
<td rowspan="3">Nu se aplică</td>
<td rowspan="3">Nu se aplică</td>
<td rowspan="3">Nu se aplică</td>
</tr>
<tr>
<td>Vânzări facturate – taxabile pentru noua cantitate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Vânzări facturate – netaxabile pentru diferență</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="2">O factură este corectată pentru a mări cantitatea tarifabilă.</td>
<td>Vânzări facturate – inversare</td>
<td>Monedă contract pentru proiect</td>
<td rowspan="5">
<ul>
<li>Inversare vânzări facturate pentru jalon</li>
<li>Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></li>
</ul>
</td>
<td rowspan="5">Monedă contract pentru proiect</td>
<td rowspan="5">Nu se aplică</td>
<td rowspan="5">Nu se aplică</td>
</tr>
<tr>
<td>Vânzări facturate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="3">O factură este corectată pentru a micșora cantitatea tarifabilă.</td>
<td>Vânzări facturate – inversare</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Vânzări facturate pentru noua cantitate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Vânzări nefacturate – taxabile pentru diferență</td>
<td>Monedă contract pentru proiect</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Resursa aparține unei unități organizatorice care diferă de unitatea contractantă a proiectului

<table>
<thead>
<tr>
<th rowspan="3">Eveniment</th>
<th colspan="4">Proiect facturabil sau vândut</th>
<th rowspan="3">Proiect în etapa de prevânzare</th>
<th rowspan="3">Proiect intern</th>
</tr>
<tr>
<th colspan="2">Timp și materiale</th>
<th colspan="2">Preț fix</th>
</tr>
<tr>
<th>Reale</th>
<th>Monedă de tranzacționare</th>
<th>Preț fix</th>
<th>Monedă de tranzacționare</th>
</tr>
</thead>
<tbody>
<tr>
<td>Este creată o intrare de timp.</td>
<td colspan="6">Nicio activitate în entitatea Valori reale</td>
</tr>
<tr>
<td>Este remisă o intrare de timp.</td>
<td colspan="6">Nicio activitate în entitatea Valori reale</td>
</tr>
<tr>
<td rowspan="4">Timpul este aprobat și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</td>
<td>Cost real</td>
<td>Moneda unității contractante</td>
<td rowspan="4">Cost real</td>
<td rowspan="4">Moneda unității contractante</td>
<td rowspan="4">Cost real</td>
<td rowspan="4">Cost real</td>
</tr>
<tr>
<td>Valoare reală vânzări nefacturate – taxabilă</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Cost de unitate resursă</td>
<td>Monedă unitate resursă</td>
</tr>
<tr>
<td>Vânzări inter-organizaționale</td>
<td>Moneda unității contractante</td>
</tr>
<tr>
<td rowspan="5">Timpul este aprobat și o reducere a orelor facturabile apare în timpul aprobării.</td>
<td>Cost real</td>
<td>Moneda unității contractante</td>
<td rowspan="5">Cost real</td>
<td rowspan="5">Moneda unității contractante</td>
<td rowspan="5">Cost real</td>
<td rowspan="5">Cost real</td>
</tr>
<tr>
<td>Cost de unitate resursă</td>
<td>Monedă unitate resursă</td>
</tr>
<tr>
<td>Vânzări inter-organizaționale</td>
<td>Moneda unității contractante</td>
</tr>
<tr>
<td>Valoare reală vânzări nefacturate – taxabile pentru noua cantitate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Valoare reală vânzări nefacturate – netaxabile pentru diferență</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="2">O factură este confirmată și nicio modificare sau creștere a orelor facturabile nu apare în timpul aprobării.</td>
<td>Inversare vânzări nefacturate</td>
<td>Monedă contract pentru proiect</td>
<td rowspan="2">Vânzări facturate pentru jalon</td>
<td rowspan="2">Monedă contract pentru proiect</td>
<td rowspan="2">Nu se aplică</td>
<td rowspan="2">Nu se aplică</td>
</tr>
<tr>
<td>Vânzări facturate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="3">O factură este confirmată și o reducere a orelor facturabile apare în timpul aprobării.</td>
<td>Inversare vânzări nefacturate</td>
<td>Monedă contract pentru proiect</td>
<td rowspan="3">Nu se aplică</td>
<td rowspan="3">Nu se aplică</td>
<td rowspan="3">Nu se aplică</td>
<td rowspan="3">Nu se aplică</td>
</tr>
<tr>
<td>Vânzări facturate – taxabile pentru noua cantitate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Vânzări facturate – netaxabile pentru diferență</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="2">O factură este corectată pentru a mări cantitatea tarifabilă.</td>
<td>Vânzări facturate – inversare</td>
<td>Monedă contract pentru proiect</td>
<td rowspan="5">
<ul>
<li>Inversare vânzări facturate pentru jalon</li>
<li>Modificarea stării jalonului de la <strong>Facturat</strong> la <strong>Gata de facturare</strong></li>
</ul>
</td>
<td rowspan="5">Monedă contract pentru proiect</td>
<td rowspan="5">Nu se aplică</td>
<td rowspan="5">Nu se aplică</td>
</tr>
<tr>
<td>Vânzări facturate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td rowspan="3">O factură este corectată pentru a micșora cantitatea tarifabilă.</td>
<td>Vânzări facturate – inversare</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Vânzări facturate pentru noua cantitate</td>
<td>Monedă contract pentru proiect</td>
</tr>
<tr>
<td>Vânzări nefacturate – taxabile pentru diferență</td>
<td>Monedă contract pentru proiect</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
