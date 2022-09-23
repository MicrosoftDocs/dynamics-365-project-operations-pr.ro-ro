---
title: Subcontractarea gestionării în Project Operations
description: Acest articol oferă o prezentare generală a procesului de gestionare a subcontractelor de la capăt la capăt, de obicei, în organizațiile bazate pe proiecte.
author: rumant
ms.date: 09/14/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b2e4518f77b2099f9818ea56623be9efb20b01f4
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522341"
---
# <a name="subcontract-management-in-project-operations"></a>Subcontractarea gestionării în Project Operations


_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest articol oferă o prezentare generală a procesului de gestionare a subcontractelor de la capăt la capăt în organizațiile bazate pe proiecte. Subcontractarea de servicii urmează de obicei un flux de business prezentat în următoarea diagramă.

![Fluxul procesului de subcontractare](../media/SubcontractingProcessFlow.png)

următoarea listă prezintă o descriere pas cu pas a procesului de subcontractare.

1. Managerul de proiect creează un subcontract cu un furnizor. În mod implicit, listele de prețuri atașate la înregistrarea furnizorului sunt utilizate pentru subcontract. Contul de furnizor are un tip de relație **Vânzător** sau **Furnizor**.
2. Managerul de proiect poate detalia toate achizițiile ca elemente de linie pe subcontract. Liniile de subcontract pot fi pentru timp, cheltuieli sau produse. Clasa de tranzacție care a liniei de subcontract stabilește pentru ce este linia.
3. Managerul de cont al furnizorului și managerul de proiect pot itera subcontractul. Prețurile pot fi ajustate în listele de prețuri de achiziție atașate subcontractului.
4. În acest moment sau mai târziu în proces, dacă linia de subcontract este pentru timp, managerul contului de furnizor asociază persoanele de contact ale furnizorului cu fiecare linie de subcontract. Această asociere oferă informații managerului de proiect care lucrează la subcontract. Când o persoană de contact a furnizorului este asociată cu o linie de subcontract, sistemul creează automat o resursă ce se poate rezerva din contact, dacă o resursă ce se poate rezerva nu există deja.
5. Metoda de facturare pe fiecare linie de subcontract poate fi **Preț fix** sau **Timp și material**. Pentru liniile de subcontract cu preț fix, se configurează o planificare de facturare bazată pe jaloane.
6.  După ce un subcontract este înființat și negocierea se încheie, acesta este confirmat. Subcontractele confirmate nu pot fi editate, dar dacă apar modificări un subcontract poate fi „redeschis pentru editări”, ceea ce setează starea din **Confirmat** înapoi în **Schiță** iar negocierile pot fi redeschise. 
7.  Când creați un membru generic al echipei într-un proiect, membrul echipei poate fi asociat unei linii de subcontract. Acest lucru indică necesitatea de a-i acorda membrului generic al echipei capacitatea de subcontractant.
8.  Membrii desemnați ai echipei pot fi creați direct pe un proiect sau creați rezervându-i cu ajutorul experiențelor de planificare a resurselor. Dacă un membru desemnat al echipei de proiect este un lucrător contractual, este posibil să îl asociați unei linii de subcontract. Aceasta va reduce capacitatea disponibilă pe o linie de subcontract.
9.  Resursele subcontractanților pot înregistra timp, cheltuieli și utilizarea materialelor pentru proiecte și sarcinile proiectului și apoi pot fi supuse aprobării. Acest lucru este similar pentru angajați. La înregistrarea timpului, un lucrător contractual poate selecta un anumit subcontract și o anumită linie de subcontract.
10. După aprobare, timpul aprobat per subcontracte va înregistra costurile efective ale proiectului în funcție de prețul de achiziție al lucrătorului contractual sau de rolul pe care l-a îndeplinit în proiect.
11. Facturile furnizorului și elementele rândurilor de factură a furnizorului pot fi înregistrate în sistem pentru munca efectuată de resursele furnizorului sau produsele livrate de furnizor. Liniile de facturare ale furnizorului trebuie să fie specifice unui proiect și pentru o clasă de tranzacție de timp, cheltuială, produs/material, jalon sau taxă. Opțional, liniile de facturare ale furnizorului pot face referire la o linie de subcontract.
12. Sistemul va asocia automat la factura furnizorului toate costurile reale care corespund liniei și proiectului de subcontract. Acest lucru va facilita un proces de verificare și potrivire în trei direcții.
13. Managerul de proiect poate apoi să revizuiască valorile reale ale proiectului, potrivite automat, să elimine sau să adauge alte costuri reale ale proiectului și să finalizeze procesul de verificare.
14. Finalizarea procesului de verificare pe toate liniile va marca factura furnizorului ca fiind **Gata pentru plată**. În această etapă, factura și liniile furnizorului pot fi transferate către un sistem de Contabilitate sau Furnizori pentru a procesa plata către furnizor. Costurile proiectului înregistrate anterior vor fi inversate și costurile efective din linia de facturare a furnizorului vor fi înregistrate pe proiect.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Linii de subcontract bazate pe cantitate și linii de subcontract bazate pe muncă

O linie de subcontract se poate baza pe cantitate sau pe muncă. 

Când o linie de subcontract este **bazată pe cantitate**, cantitatea achiziționată pe linia de subcontract pentru timp, cheltuială sau material poate fi utilizată în orice proiect.

Când o linie de subcontract este **bazată pe muncă**, linia de subcontract se mapează la un volum de lucru reprezentat de un nod în planul de proiect. Valoarea liniei de subcontract este suma tuturor componentelor necesare pentru a livra volumul de lucru respectiv. Acestea sunt modelate ca detalii ale liniei de subcontract și pot fi o colecție de timp, cheltuieli sau materiale. Pentru o linie de subcontract bazată pe muncă, linia de subcontract este, de asemenea, dedicată unui singur proiect. Aceste tipuri de subcontracte nu sunt suportate în prezent de Operațiunile de Proiect.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

