---
title: Subcontractarea membrilor echipei de proiect
description: Acest articol explică cum să subcontractați membrii echipei de proiect în Microsoft Dynamics 365 Project Operations.
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

În Microsoft Dynamics 365 Project Operations, puteți alege să subcontractați membri ai echipei de proiect fără personal sau personal.

- Membrii echipei de proiect fără personal au o resursă generică alocată.
- Membrii echipei cu personal au o resursă numită atribuită.

Când legați un membru al echipei de proiect la o linie de subcontractare, orice atribuire a sarcinilor pe care le are membrul echipei vor fi decontate pe baza listei de prețuri de achiziție atașată subcontractului.  Pe **Estimări** fila de pe **detaliile proiectului** pagina, selectați **Actualizați prețurile** butonul pentru a vedea prețurile și/sau costurile actualizate rezultate din decizia de subcontractare. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect fără personal
The **Detalii despre membrii echipei** pagina are câmpuri de subcontractare și subcontractare care permit unui manager de proiect să exprime modul în care ar dori să atragă capacitatea necesară dintr-un subcontract. Pentru a subcontracta un membru al echipei de proiect ca resursă generică, urmați acești pași:

1.  Alegeți un subcontract pe **Detaliu membru al echipei** pagină.

2.  Puteți selecta doar subcontracte cu **Proiect** sau **Confirmat** stare. **Închis** sau **Anulat** subcontractele nu pot fi selectate. 

3.  The **Linia de subcontractare** câmpul devine vizibil după ce selectați un subcontract.

4.  În **Linia de subcontractare** câmp, puteți selecta doar linii de subcontractare care sunt pentru timp. Nu puteți selecta linii de subcontractare pentru cheltuieli sau material.

5.  Rolul pentru înregistrarea membrilor echipei de proiect trebuie să se potrivească cu rolul de pe linia de subcontractare. Acest lucru asigură că timpul pentru rolul care este estimat pe proiect este același rol care este achiziționat pe linia de subcontractare. 

Când un membru generic al echipei este asociat cu o linie de subcontractare și subcontractare, **Tip muncitor** câmpul de pe rândul generic membru al echipei va fi actualizat la **Muncitor Contractual** și **Valabilitatea subcontractului** va fi setat la **Valabil**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect cu personal
La fel ca membrii echipei generice sau fără personal, capacitatea de membru al echipei cu personal necesară pentru un proiect poate fi, de asemenea, legată de un subcontract. Pentru a subcontracta un membru numit al echipei de proiect, urmați acești pași:

1.  Asigurați-vă că resursa numită este configurată ca resursă rezervabilă de tip lucrător contractual. De asemenea, asigurați-vă că **Furnizor** câmpul din resursa rezervabilă se potrivește cu furnizorul din subcontractul pe care îl selectați. 

2.  Puteți selecta doar subcontracte în **Proiect** sau **Confirmat** stare. **Închis** sau **Anulat** subcontractele nu pot fi selectate. 

3.  The **Linia de subcontractare** câmpul devine vizibil după ce selectați un subcontract.

4.  În **Linia de subcontractare** câmp, puteți selecta doar linii de subcontractare care sunt pentru timp. Nu puteți selecta linii de subcontractare pentru cheltuieli sau material.

5.  Rolul pentru înregistrarea membrilor echipei de proiect trebuie să se potrivească cu rolul de pe linia de subcontractare. Acest lucru asigură că timpul pentru rolul care este estimat pe proiect este același rol care este achiziționat pe linia de subcontractare. 

Membrii echipei de proiect numiți care sunt configurați ca un tip de lucrător contractual **Resursa rezervabila** va fi afișat cu o stare de valabilitate a subcontractului de **Invalid** dacă nu sunt legate de un subcontract. Când un membru numit al echipei de proiect este asociat cu o linie de subcontractare și subcontractare, **Tip muncitor** câmpul din rândul membru al echipei se va actualiza la **Muncitor Contractual** și **Valabilitatea subcontractului** va fi setat la **Valabil**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
