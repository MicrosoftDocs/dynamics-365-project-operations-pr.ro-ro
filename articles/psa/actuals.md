---
title: Prezentare date reale
description: Acest subiect oferă informații despre valorile reale ale proiectului.
author: rumant
manager: kfend
ms.service: project-operations
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146138"
---
# <a name="actuals-overview"></a>Prezentare date reale

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Valorile reale reprezintă volumul de lucru care a fost finalizat pe un proiect. Valorile reale ale proiectului pot fi urmărite înapoi la documentele lor sursă. Aceste documente sursă includ intrările de timp, intrările cu cheltuieli și intrările în jurnal și, de asemenea, facturile.

![Cum sunt urmărite valorile reale ale proiectului la documentele sursă](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Remiterea unei intrări de timp

În PSA, atunci când o intrare de timp este remisă pentru un proiect care este mapat la o linie de contract pentru timp și materiale, se creează două linii de jurnal. O linie este pentru cost, iar cealaltă linie este pentru vânzările nefacturate. Atunci când o intrare de timp este remisă pentru un proiect care este mapat la o linie de contract cu preț fix, se creează o linie de jurnal doar pentru cost. 

Logica pentru introducerea prețurilor implicite se află în linia de jurnal. Toate valorile de câmp dintr-o intrare de timp sunt copiate în linia de jurnal. Aceste câmpuri includ data tranzacției, linia de contract la care este mapat proiectul și rezultatul privind moneda din lista de prețuri corespunzătoare. 

Câmpurile care afectează prețurile implicite, cum ar fi **Rol** și **Unitate organizațională**, determină introducerea implicită a unui preț corespunzător în linia de jurnal. Dacă adăugați un câmp particularizat în intrarea de timp și doriți ca valoarea câmpului să fie propagată în valorile reale, creați câmpul în entitatea Valori reale și utilizați mapări de câmp pentru a copia câmpul din intrarea de timp în valoarea reală.

## <a name="submitting-an-expense-entry"></a>Remiterea unei intrări de cheltuieli

În PSA, atunci când o intrare de cheltuieli este remisă pentru un proiect care este mapat la o linie de contract pentru timp și materiale, se creează două linii de jurnal. O linie este pentru cost, iar cealaltă linie este pentru vânzările nefacturate. Atunci când o intrare de cheltuieli este remisă pentru un proiect care este mapat la o linie de contract cu preț fix, se creează o linie de jurnal doar pentru cost.

Logica pentru introducerea prețurilor implicite pentru cheltuieli se bazează pe categoria de cheltuieli care este selectată în pagina **Intrare cheltuieli**. Data tranzacției, linia de contract la care este mapat proiectul și moneda sunt toate utilizate pentru a determina lista de prețuri corespunzătoare. Cu toate acestea, pentru prețul în sine, suma pe care utilizatorul a introdus-o este setată direct pe liniile de jurnal de cheltuieli corelate pentru cost și vânzări în mod implicit.

În versiunea curentă de PSA, introducerea pe categorii a unor prețuri implicite per unitate pe intrările de cheltuieli nu este disponibilă.

## <a name="using-entry-journals-to-record-costs"></a>Utilizarea jurnalelor de intrări pentru înregistrarea costurilor

În PSA, jurnalele de intare vă permit să înregistrați costul sau venitul în clasele de tranzacții Materiale, Tarife, Timp, Cheltuieli sau Taxe. Un jurnal are un antet, linii și o acțiune **Confirmare**. Iată câteva scenarii în care este posibil să utilizați un jurnal:

- Trebuie să înregistrați costurile reale ale materialelor și vânzările pe un proiect.
- Trebuie să mutați valori reale privind tranzacțiile dintr-un alt sistem în PSA.
- Trebuie să înregistrați costuri care au avut loc în alt sistem, cum ar fi costurile de achiziție sau subcontractare.

> [!IMPORTANT]
> Utilizarea jurnalelor de intrare pentru a crea actualități ar trebui să fie făcută doar de către un utilizator care este pe deplin conștient de impactul contabil pe care efectivele îl au asupra proiectului. Acest lucru se datorează faptului că aplicația nu validează tipul liniei de jurnal sau prețurile aferente care sunt introduse pe linia jurnalului. Din cauza impactului acestui tip de jurnal, trebuie să aveți precauție adecvată pentru cine are acces la crearea jurnalelor de intrare.     


## <a name="recording-actuals-based-on-project-events"></a>Înregistrarea valorilor reale pe baza evenimentelor proiectului

PSA înregistrează tranzacțiile financiare care apar în timpul unui proiect. Aceste tranzacții sunt înregistrate ca **valori reale**. Tabelele următoare arată diferitele tipuri de valori reale care sunt create, în funcție de faptul dacă proiectul este un proiect pe bază de timp și materiale sau un proiect cu preț fix, este în etapa de prevânzare sau este un proiect intern.

**Resursa aparține aceleiași unități organizatorice ca și unitatea contractantă a proiectului**

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

**Resursa aparține unei unități organizatorice care diferă de unitatea contractantă a proiectului**

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
