---
title: Opțiuni de subcontractare pentru membrii echipei de proiect
description: Acest subiect explică opțiunile de subcontractare pentru membrii echipei de proiect în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903748"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opțiuni de subcontractare pentru membrii echipei de proiect

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

În Microsoft Dynamics 365 Project Operations, puteți evalua opțiunile de subcontractare disponibile pentru unul sau mai mulți membri ai echipei de proiect. Opțiunile de subcontractare disponibile vă permit:

- Creați un nou subcontract și/sau creați noi linii pe un subcontract existent pentru membrii echipei de proiect selectați. 
- Rezervă față de un subcontract deja existent și o linie de subcontractare. 

Puteți alege dintre opțiunile de subcontractare disponibile pentru membrii echipei de proiect generice sau puteți alege dintre membrii echipei de proiect care au fost dotați cu o resursă numită care este un lucrător contractual. 

Nu există opțiuni de subcontractare disponibile pentru următoarele:

- Membrii echipei de proiect care au fost angajați cu un angajat. 
- Membrii echipei de proiect care sunt deja asociați unei linii de subcontractare și subcontractare. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect fără personal

Pentru a revizui și a alege dintre opțiunile de subcontractare disponibile pentru un membru al echipei de proiect generic sau fără personal, urmați acești pași:

1. Selectați una sau mai multe înregistrări ale membrilor echipei de proiect unde resursa este o resursă generică.
2. Asigurați-vă că niciuna dintre înregistrările membrilor echipei de proiect selectate nu sunt deja subcontractate. 
3. Selectați **Opțiuni de subcontractare** pe subgrila membrilor echipei de proiect. The **Opțiuni de subcontractare** se deschide dialogul. 
4. Dacă ați selectat doar o înregistrare a unui membru al echipei de proiect la pasul 1, atunci următoarele opțiuni vor fi disponibile:
    - Creați noi linii de subcontractare. 
    - Rezervare pentru un subcontract existent Dacă ați selectat mai multe înregistrări ale membrilor echipei de proiect la pasul 1, atunci singura opțiune disponibilă este crearea unei noi linii de subcontract.
5. Opțiunea de rezervare pentru o linie de subcontractare existentă vă permite să selectați o linie de subcontractare și de subcontractare pentru care doriți să rezervați. Atunci când selectați o linie de subcontractare pentru rezervarea capacității, trebuie să vă asigurați că linia de subcontractare selectată este pentru timp și că rolul cerut membrului echipei de proiect se potrivește cu rolul achiziționat pe linia de subcontractare.
6. Când selectați să creați noi linii de subcontractare pentru membrii echipei de proiect, sistemul vă va permite să selectați subcontractul pe care doriți să îl creați aceste linii. Subcontractul pe care îl selectați pentru a crea linii noi ar trebui să fie în **Proiect** stare. Cu această opțiune de a crea noi linii de subcontractare pentru membrii echipei de proiect selectați, sistemul va crea o linie de subcontractare pentru timp pentru fiecare membru al echipei de proiect. Rolul, orele și datele vor fi copiate de la membrul echipei de proiect în fiecare linie de subcontractare care este creată. 
7. Când un membru generic al echipei este asociat cu o linie de subcontractare și subcontractare, **Tip muncitor** câmpul de pe rândul generic membru al echipei va fi actualizat la **Muncitor Contractual** si **Valabilitatea subcontractului** valoarea va fi setată la **Valabil**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subcontractarea unui membru al echipei de proiect cu personal

La fel ca membrii echipei generice sau fără personal, puteți vizualiza și opțiunile de subcontractare pentru un membru al echipei de proiect cu personal, atâta timp cât membrul echipei cu personal este un lucrător contractual. Pentru a revizui și a alege dintre opțiunile de subcontractare disponibile pentru un membru al echipei de proiect cu personal sau numit, urmați acești pași:

1. Selectați una sau mai multe înregistrări ale membrilor echipei de proiect în care resursa este un lucrător contractual numit.
2. Asigurați-vă că niciuna dintre înregistrările selectate ale membrilor echipei de proiect nu sunt deja subcontractate. 
3. Selectați **Opțiuni de subcontractare** pe subgrila membrilor echipei de proiect. The **Opțiuni de subcontractare** se deschide dialogul. 
4. Dacă ați selectat doar o înregistrare a unui membru al echipei de proiect la pasul 1, atunci următoarele opțiuni vor fi disponibile:
      - Creați noi linii de subcontractare.
      - Rezervă împotriva unui subcontract existent.
  Dacă ați selectat mai multe înregistrări ale membrilor echipei de proiect la pasul 1, atunci singura opțiune disponibilă este crearea unei noi linii de subcontractare.
5. Opțiunea de rezervare pentru o linie de subcontractare existentă vă permite să selectați o linie de subcontractare și de subcontractare pentru care doriți să rezervați. Atunci când selectați o linie de subcontractare pentru rezervarea capacității, trebuie să vă asigurați de următoarele:
      - Linia de subcontractare selectată este pentru timp. 
      - Rolul cerut membrului echipei de proiect se potrivește cu rolul care a fost achiziționat pe linia de subcontractare. 
      - Vânzătorul căruia este asociat lucrătorul contractual este același cu vânzătorul din subcontract.
6. Când selectați să creați noi linii de subcontractare pentru membrii echipei de proiect, sistemul vă va permite să selectați subcontractul pe care doriți să îl creați aceste linii. Cu această opțiune, ar trebui să vă asigurați că furnizorul căruia îi aparține lucrătorul contractual este același cu furnizorul din subcontract. 
7. Subcontractul pe care îl selectați pentru a crea linii noi ar trebui să fie în **Proiect** stare. Cu această opțiune de a crea noi linii de subcontractare pentru membrii echipei de proiect selectați, sistemul va crea o linie de subcontractare pentru timp pentru fiecare membru al echipei de proiect. Rolul, orele și datele vor fi copiate de la membrul echipei de proiect în fiecare linie de subcontractare care este creată.  
8. Când un membru al echipei numit este asociat cu o linie de subcontractare și subcontractare, **Tip muncitor** câmpul de pe rândul numit membru al echipei va fi actualizat la **Muncitor Contractual** si **Valabilitatea subcontractului** valoarea va fi setată la **Valabil**.

## <a name="re-costing-subcontractor-assignments"></a>Re-costificarea sarcinilor subcontractanților

Atunci când un membru al echipei de proiect (generic sau numit) este conectat la linii de subcontractare folosind **Opțiuni de subcontractare** dialog, orice atribuire a sarcinilor pe care le are membrul echipei vor fi recostate pe baza listei de prețuri de achiziție atașată la subcontract. Pe **Estimări** fila pe **detaliile proiectului** pagina, selectați **Actualizați prețurile** butonul pentru a vedea prețurile și/sau costurile actualizate rezultate din decizia de subcontractare.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
