---
title: Liste de prețuri implicite
description: Acest articol furnizează informații despre vânzările implicite și listele de prețuri de cost în Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410278"
---
# <a name="default-price-lists"></a>Liste de prețuri implicite

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

## <a name="sales-price-lists"></a>Liste de prețuri de vânzări

Fiecare ofertă de proiect și contract din Dynamics 365 Project Operations conține o listă de prețuri de vânzare implicită. 

### <a name="price-list-default-on-project-quotes"></a>Listă de prețuri implicită pentru ofertele proiectului
Sistemul finalizează următorul proces pentru a determina ce listă de prețuri va fi implicită pentru o ofertă de proiect:

1. Sistemul analizează listele de prețuri atașate listelor de prețuri ale proiectului contului. 
1. Dacă nu există liste de prețuri ale proiectului atașate la înregistrarea contului, sistemul analizează listele de prețuri de vânzare atașate parametrilor proiectului care se potrivesc cu moneda ofertei de proiect.
1. Apoi, sistemul verifică eficacitatea datei listelor de prețuri care se potrivesc cu intervalul de date al ofertei de proiect. Mai exact, data la care a fost creată oferta.
1. Dacă există mai multe liste de prețuri care intră în vigoare pentru data ofertei de proiect, toate listele de prețuri sunt implicite în oferta de proiect.
1. Dacă nu există liste de prețuri în vigoare pentru data ofertei de proiect, nu există o listă de prețuri implicită în oferta de proiect. Pe oferta de proiect va apărea un mesaj de avertizare. Mesajul indică faptul că realitățile și estimările proiectului nu vor fi evaluate, deoarece nu sunt atașate liste de prețuri ale proiectului.

### <a name="price-list-default-on-project-contracts"></a>Listă de prețuri implicită pentru contractele proiectului 
Sistemul finalizează următorul proces pentru a determina ce listă de prețuri va fi implicită pentru un contract de proiect:

1. Dacă contractul este creat dintr-o ofertă, listele de prețuri ale proiectului ale ofertei sunt copiate separat și atașate contractului de proiect.
1. Dacă contractul este creat de la zero, sistemul analizează listele de prețuri atașate listelor de prețuri ale proiectului din cont. Dacă nu există liste de prețuri ale proiectului atașate la înregistrarea contului, sistemul caută liste de prețuri de vânzare atașate parametrilor proiectului care se potrivesc cu moneda contractului de proiect.
1. Apoi, sistemul verifică eficacitatea datei listelor de prețuri care se potrivesc cu intervalul de date al contractului de proiect. Mai exact, data la care a fost creat contractul.
1. Dacă există mai multe liste de prețuri care intră în vigoare pentru data contractului, toate listele de prețuri sunt implicite în contract.
1. Dacă nu există liste de prețuri în vigoare pentru data contractului, nicio listă de prețuri a proiectului nu este implicită în contract. Pe contractul de proiect va apărea un mesaj de avertizare. Mesajul indică faptul că realitățile și estimările proiectului nu vor fi evaluate, deoarece nu sunt atașate liste de prețuri ale proiectului.

## <a name="cost-price-lists"></a>Listele de prețuri de cost

Listele de prețuri de cost nu sunt implicite pentru nicio entitate din Project Operations. Stabilirea listei de prețuri de cost care urmează a fi utilizate pentru costurile proiectului se face întotdeauna pe tranzacție. Sistemul finalizează următorul proces pentru a determina ce listă de prețuri trebuie utilizată pentru costurile proiectului:

1. Sistemul analizează listele de prețuri atașate unității organizaționale contractante a proiectului.
1. Apoi, sistemul analizează data de intrare în vigoare a listelor de prețuri care se potrivesc cu data contextului estimat sau a contextului real primit.

    - *Contextul estimat* se referă la oricare dintre cele trei contexte de estimare din Project Operations:

        - Linia de estimare a proiectului
        - Detaliu linie de ofertă
        - Detaliul liniei de contract

    - *Contextul real* se referă la oricare dintre cele trei surse de valori reale din Project Operations:

       - Liniile de jurnal de intrare care sunt create manual sau liniile de jurnal de corecție care sunt create într-un jurnal de corecție
       - Liniile de jurnal care sunt create în timpul trimiterii jurnalellor de timp, cheltuieli sau utilizare a materialelor
       - Detaliu linie factură

    Când Project Operations se potrivește cu data de intrare în vigoare a liniei de jurnal de intrare sau a detaliilor liniei de facturare în *contextul real*, utilizează câmpul **Dată tranzacție**.

    - Dacă există mai multe liste de prețuri care sunt în vigoare pentru data contextului estimat sau a contextului real primit, este selectată lista de prețuri creată cel mai recent.
    - Dacă nu sunt liste de prețuri atașate la unitatea organizațională contractantă a proiectului, sistemul analizează listele de prețuri de cost care sunt atașate parametrilor proiectului care se potrivesc cu moneda proiectului.

## <a name="enable-multi-currency-cost-price-list"></a>Activați lista cu prețuri de cost în mai multe monede

Această setare poate fi găsită la **Setări** \> **Parametri**. Valoarea implicită este **Nu**.

Când această setare este activată (adică valoarea este setată la **Da**), sistemul se comportă în felul următor:

- Permite ca listele de prețuri de cost în orice monedă să fie asociate unității organizaționale. De exemplu, o listă de prețuri de cost în moneda EUR poate fi atașată unei unități organizaționale în moneda USD. Sistemul va continua să valideze că listele de prețuri de cost care sunt atașate unei unități organizaționale nu au date de intrare in vigoare suprapuse.
- Validează faptul că listele de prețuri de cost care sunt atașate parametrilor proiectului nu au date de intrare în vigoare suprapuse, chiar dacă au monede diferite. Acest comportament diferă de comportamentul implicit (adică, comportamentul manifestat când valoarea este setată la **Nu**). În comportamentul implicit, numai listele de prețuri de cost care au **aceeași** monedă sunt validate pentru a nu suprapune data intrării în vigoare.
- Pentru un context de tranzacție de intrare, acesta determină lista de prețuri de cost numai pe baza datei de intrare în vigoare. Acest comportament diferă de comportamentul implicit, în care sistemul selectează lista de prețuri de cost care se potrivește atât cu moneda proiectului, cât și cu data de intrare în vigoare.

Datorită acestor schimbări de comportament, clienții Project Operations vor putea menține o listă globală de prețuri de cost care va fi relevantă pentru întreaga companie. Nu vor trebui să aibă liste de prețuri în fiecare monedă de operațiuni. Lista globală de prețuri va avea dată de valabilitate și va permite stabilirea ratelor de cost în orice monedă pentru o anumită combinație de valori ale dimensiunii de preț. Moneda listei de prețuri de cost este folosită numai pentru a introduce valori implicite când sunt create înregistrări pentru elementele **Prețuri de rol**, **Prețuri de categorie** și **Listă de prețuri**. Nu se va utiliza pentru stabilirea listei de prețuri.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
