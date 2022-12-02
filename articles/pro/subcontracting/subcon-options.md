---
title: Opțiuni de subcontractare pentru membrii echipei de proiect
description: Acest articol explică opțiunile de subcontractare pentru membrii echipei de proiect în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522294"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opțiuni de subcontractare pentru membrii echipei de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

În Microsoft Dynamics 365 Project Operations, puteți evalua opțiunile de subcontractare disponibile pentru unul sau mai mulți membri ai echipei de proiect. Opțiunile de subcontractare disponibile vă permit să:

- Creați un nou subcontract și/sau să creați noi linii pe un subcontract existent pentru membrii echipei de proiect selectați. 
- Rezervați pentru un subcontract și o linie de subcontractare existente deja. 

Puteți alege dintre opțiunile de subcontractare disponibile pentru membrii generici ai echipei de proiect sau puteți alege dintre membrii echipei de proiect care au fost alocați la o resursă numită care este un lucrător contractual. 

Nu există opțiuni de subcontractare disponibile pentru următoarele:

- Membrii echipei de proiect care au fost încadrați cu un angajat. 
- Membrii echipei de proiect care sunt deja asociați unui subcontract sau unei linii de subcontractare. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect neîncadrat

Pentru a revizui și a alege dintre opțiunile de subcontractare disponibile pentru un membru generic sau neîncadrat al echipei de proiect, urmați acești pași:

1. Selectați una sau mai multe înregistrări ale membrilor echipei de proiect în care resursa este o resursă generică.
2. Asigurați-vă că niciuna dintre înregistrările membrilor echipei de proiect selectate nu sunt deja subcontractate. 
3. Selectați **Opțiuni de subcontractare** pe subgrila membrilor echipei de proiect. Caseta de dialog **Opțiuni subcontractare** se deschide. 
4. Dacă ați selectat doar o înregistrare a unui membru al echipei de proiect la pasul 1, atunci următoarele opțiuni vor fi disponibile:
    - Creați noi linii de subcontractare. 
    - Rezervați pentru un subcontract existent. Dacă ați selectat mai multe înregistrări ale membrilor echipei de proiect la pasul 1, atunci singura opțiune disponibilă este crearea unor noi linii de subcontract.
5. Opțiunea de rezervare pentru o linie de subcontractare existentă vă permite să selectați un subcontract sau o linie de subcontractare pentru care doriți să rezervați. Când selectați o linie de subcontractare pentru rezervarea capacității, trebuie să vă asigurați că linia de subcontractare selectată este pentru timp și că rolul solicitat membrului echipei de proiect se potrivește cu rolul achiziționat pe linia de subcontractare.
6. Când selectați să creați noi linii de subcontractare pentru membrii echipei de proiect, sistemul vă va permite să selectați subcontractul pe care doriți creați aceste linii. Subcontractul pe care îl selectați pentru a crea linii noi ar trebui să aibă starea **Schiță**. Cu această opțiune de a crea noi linii de subcontractare pentru membrii echipei de proiect selectați, sistemul va crea o linie de subcontractare pentru timp pentru fiecare membru al echipei de proiect. Rolul, orele și datele vor fi copiate de la membrul echipei de proiect în fiecare linie de subcontractare care este creată. 
7. Când un membru generic al echipei este asociat cu un subcontract și o linie de subcontractare, câmpul **Tip lucrător** de pe rândul de membru generic al echipei va fi actualizat la **Lucrător contractual** si valoarea **Validitate subcontract** va fi setată la **Valid**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect încadrat

La fel ca membrii generici ai echipei sau neîncadrați, puteți vizualiza și opțiunile de subcontractare pentru un membru al echipei de proiect încadrat, atâta timp cât membrul încadrat al echipei este un lucrător contractual. Pentru a revizui și a alege dintre opțiunile de subcontractare disponibile pentru un membru încadrat sau numit al echipei de proiect, urmați acești pași:

1. Selectați una sau mai multe înregistrări ale membrilor echipei de proiect în care resursa este un lucrător contractual numit.
2. Asigurați-vă că niciuna dintre înregistrările membrilor echipei de proiect selectate nu sunt deja subcontractate. 
3. Selectați **Opțiuni de subcontractare** pe subgrila membrilor echipei de proiect. Caseta de dialog **Opțiuni subcontractare** se deschide. 
4. Dacă ați selectat doar o înregistrare a unui membru al echipei de proiect la pasul 1, atunci următoarele opțiuni vor fi disponibile:
      - Creați noi linii de subcontractare.
      - Rezervați pentru o linie de subcontractare existentă.
  Dacă ați selectat mai multe înregistrări ale membrilor echipei de proiect la pasul 1, atunci singura opțiune disponibilă este crearea unor noi linii de subcontract.
5. Opțiunea de rezervare pentru o linie de subcontractare existentă vă permite să selectați un subcontract sau o linie de subcontractare pentru care doriți să rezervați. Atunci când selectați o linie de subcontractare pentru rezervarea capacității, trebuie să vă asigurați de următoarele:
      - Linia de subcontractare selectată este pentru timp. 
      - Rolul cerut membrului echipei de proiect se potrivește cu rolul care a fost achiziționat pe linia de subcontractare. 
      - Furnizorul căruia îi este asociat lucrătorul contractual este același cu furnizorul din subcontract.
6. Când selectați să creați noi linii de subcontractare pentru membrii echipei de proiect, sistemul vă va permite să selectați subcontractul pe care doriți creați aceste linii. Cu această opțiune, ar trebui să vă asigurași că furnizorul căruia îi este aparține lucrătorul contractual este același cu furnizorul din subcontract. 
7. Subcontractul pe care îl selectați pentru a crea linii noi ar trebui să aibă starea **Schiță**. Cu această opțiune de a crea noi linii de subcontractare pentru membrii echipei de proiect selectați, sistemul va crea o linie de subcontractare pentru timp pentru fiecare membru al echipei de proiect. Rolul, orele și datele vor fi copiate de la membrul echipei de proiect în fiecare linie de subcontractare care este creată.  
8. Când un membru numit al echipei este asociat cu un subcontract și o linie de subcontractare, câmpul **Tip lucrător** de pe rândul de membru numit al echipei va fi actualizat la **Lucrător contractual** si valoarea **Validitate subcontract** va fi setată la **Valid**.

## <a name="re-costing-subcontractor-assignments"></a>Recalcularea costurilor sarcinilor subcontractanților

Când un membru al echipei de proiect (generic sau numit) este conectat la liniile de subcontractare folosind caseta de dialog **Opțiuni de subcontractare**, orice atribuire a sarcinilor pe care le are membrul echipei va fi recalculată pe baza listei de prețuri de achiziție atașată la subcontract. Pe fila **Estimări** de pe pagina **Detalii proiect**, selectați butonul **Actualizare prețuri** pentru a vedea prețurile și/sau calculul costurilor actualizate rezultate din decizia de subcontractare.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
