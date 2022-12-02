---
title: Subcontractarea membrilor echipei de proiect
description: Acest articol explică modul de subcontractare a membrilor echipei de proiect în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522811"
---
# <a name="subcontracting-project-team-members"></a>Subcontractarea membrilor echipei de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În Microsoft Dynamics 365 Project Operations, puteți alege să subcontractați membri ai echipei de proiect încadrați sau neîncadrați.

- Membrii echipei de proiect neîncadrați au o resursă generică alocată.
- Membrii încadrați ai echipei au o resursă numită atribuită.

Când legați un membru al echipei de proiect la o linie de subcontractare, orice atribuire a sarcinilor pe care le are membrul echipei vor fi recalculate pe baza listei de prețuri de achiziție atașată subcontractului.  Pe fila **Estimări** de pe pagina **Detalii proiect**, selectați butonul **Actualizare prețuri** pentru a vedea prețurile și/sau calculul costurilor actualizate rezultate din decizia de subcontractare. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect neîncadrat
Pagina **Detalii despre membrii echipei** are câmpuri de subcontract și de linie de subcontractare care permit unui manager de proiect să exprime modul în care ar dori să atragă capacitatea necesară dintr-un subcontract. Pentru a subcontracta un membru al echipei de proiect ca resursă generică, urmați acești pași:

1.  Alegeți un subcontract pe pagina **Detaliu membru al echipei**.

2.  Puteți doar selecta subcontractele cu starea **Schiță** sau **Confirmat**. Subcontractele cu starea **Închis** sau **Anulat** nu pot fi selectate. 

3.  Câmoul **Linie de subcontractare** devine vizibil după ce selectați un subcontract.

4.  În câmpul **Linie de subcontractare**, puteți selecta doar linii de subcontractare care sunt pentru timp. Nu puteți selecta linii de subcontractare pentru cheltuieli sau materiale.

5.  Rolul pentru înregistrarea membrilor echipei de proiect trebuie să se potrivească cu rolul de pe linia de subcontractare. Acest lucru asigură că timpul pentru rolul care este estimat pe proiect este același rol care este achiziționat pe linia de subcontractare. 

Când un membru generic al echipei este asociat cu un subcontract și cu o linie de subcontractare, câmpul **Tip lucrător** de pe rândul de membru generic al echipei va fi actualizat la **Lucrător contractual** și **Validitate subcontract** va fi setată la **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect încadrat
La fel ca în cazul membrilor generici sau neîncadrați ai echipei, capacitatea de membru încadrat al echipei necesară pentru un proiect poate fi, de asemenea, legată de un subcontract. Pentru a subcontracta un membru numit al echipei de proiect, urmați acești pași:

1.  Asigurați-vă că resursa numită este configurată ca resursă care poate fi rezervată, de tip lucrător contractual. De asemenea, asigurați-vă că câmpul **Furnizor** din resursa care poate fi rezervată se potrivește cu furnizorul din subcontractul pe care îl selectați. 

2.  Puteți doar selecta subcontractele în starea **Schiță** sau **Confirmat**. Subcontractele cu starea **Închis** sau **Anulat** nu pot fi selectate. 

3.  Câmoul **Linie de subcontractare** devine vizibil după ce selectați un subcontract.

4.  În câmpul **Linie de subcontractare**, puteți selecta doar linii de subcontractare care sunt pentru timp. Nu puteți selecta linii de subcontractare pentru cheltuieli sau materiale.

5.  Rolul pentru înregistrarea membrilor echipei de proiect trebuie să se potrivească cu rolul de pe linia de subcontractare. Acest lucru asigură că timpul pentru rolul care este estimat pe proiect este același rol care este achiziționat pe linia de subcontractare. 

Membrii numiți ai echipei de proiect care sunt configurați ca tip de lucrător contractual de **Resursă ce poate fi rezervată** vor fi afișați cu o stare de validitate a subcontractului de **Invalid** dacă nu sunt legați de un subcontract. Când un membru numit al echipei este asociat cu un subcontract și cu o linie de subcontractare, câmpul **Tip lucrător** din rândul de membru al echipei se va actualizat la **Lucrător contractual** și **Validitate subcontract** va fi setată la **Valid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
