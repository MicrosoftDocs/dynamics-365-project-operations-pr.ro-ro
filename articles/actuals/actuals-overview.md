---
title: Date reale
description: Acest subiect oferă informații despre cum să lucrați cu date reale în Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082786"
---
# <a name="actuals"></a>Date reale 

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Valorile reale reprezintă volumul de lucru care a fost finalizat pe un proiect. Acestea sunt create ca urmare a intrărilor de timp și a cheltuielilor, a înregistrărilor din jurnal și a facturilor.

## <a name="journal-lines-and-time-submission"></a>Liniile de jurnal și remiteri de timp

Pentru mai multe informații despre remiteri de timp, consultați [Prezentare generală a intrării de timp](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Timp și materiale

Atunci când o intrare de timp care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.

### <a name="fixed-price"></a>Preț fix

Atunci când o intrare de timp care este remisă este legată de un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.

### <a name="default-pricing"></a>Tarifare implicită

Logica pentru crearea prețurilor implicite se află pe linia de jurnal. Valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal. Aceste valori includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare.

Câmpurile care afectează tarifarea implicită, cum ar fi **Rol** și **Unitate organizațională** , sunt utilizate pentru a determina prețul corespunzător pe linia de jurnal. Puteți adăuga un câmp personalizat la intrarea în timp. Dacă doriți ca valoarea câmpului să fie propagată în valorile reale, creați câmpul în entitatea Valori reale și utilizați mapări de câmp pentru a copia câmpul din intrarea de timp în valoarea reală.

## <a name="journal-lines-and-basic-expense-submission"></a>Liniile de jurnal și remiterea cheltuielilor de bază

Pentru mai multe informații despre intrări de cheltuială [Prezentare generală a cheltuielii](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Timp și materiale

Atunci când o intrare de cheltuială de bază care este trimisă este legată de un proiect care este mapat la o linie contractuală de timp și materiale, sistemul creează două linii de jurnal, una pentru cost și una pentru vânzările nefacturate.

### <a name="fixed-price"></a>Preț fix

Atunci când o intrare de cheltuială de bază care este remisă este legată de un proiect care este mapat la o linie de contract cu preț fix, sistemul creează o linie de jurnal pentru cost.

### <a name="default-pricing"></a>Tarifare implicită

Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli. Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare. Cu toate acestea, în mod implicit, suma care este introdusă pentru prețul în sine este setată direct pe liniile de jurnal de cheltuieli corelate pentru cost și vânzări.

Intrarea pe categorii a unor prețuri implicite per unitate pe intrările de cheltuieli nu este disponibilă.

## <a name="use-entry-journals-to-record-costs"></a>Utilizați intrările de jurnal pentru a înregistra costurilr

Puteți utiliza intrările de jurnal pentru a înregistra costul sau venitul în material, tarif, timp, cheltuieli sau clase de taxe de tranzacții. Jurnalele pot fi utilizate în următoarele scopuri:

- Înregistrați costul real al materialelor și vânzărilor pe un proiect.
- Mutați valorile reale ale tranzacțiile din alt sistem la Microsoft Dynamics 365 Project Operations.
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
