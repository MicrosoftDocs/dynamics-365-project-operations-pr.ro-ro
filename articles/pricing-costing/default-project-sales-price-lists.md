---
title: Liste de prețuri implicite
description: Acest subiect furnizează informații despre vânzările implicite și listele de prețuri de cost în Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 04c97429ab8ac769dd22b4127432d80de8fde937
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275598"
---
# <a name="default-price-lists"></a>Liste de prețuri implicite

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

## <a name="sales-price-lists"></a>Liste de prețuri de vânzări

Fiecare ofertă de proiect și contract din Dynamics 365 Project Operations conține o listă de prețuri de vânzare implicită. 

### <a name="price-list-default-on-project-quotes"></a>Listă de prețuri implicită pentru ofertele proiectului
Sistemul finalizează următorul proces pentru a determina ce listă de prețuri va fi implicită pentru o ofertă de proiect:

1. Sistemul analizează listele de prețuri atașate listelor de prețuri ale proiectului contului. 
2. Dacă există liste de prețuri ale proiectului atașate la înregistrarea contului, sistemul analizează listele de prețuri de vânzare atașate parametrilor proiectului care se potrivesc cu moneda ofertei de proiect.
3. Apoi, sistemul verifică eficacitatea datei listelor de prețuri care se potrivesc cu intervalul de date al ofertei de proiect. Mai exact, data la care a fost creată oferta.
4. Dacă există mai multe liste de prețuri care intră în vigoare pentru data ofertei de proiect, toate listele de prețuri sunt implicite în oferta de proiect.
5. Dacă nu există liste de prețuri în vigoare pentru data ofertei de proiect, nu există o listă de prețuri implicită în oferta de proiect. Pe oferta de proiect va apărea un mesaj de avertizare. Mesajul indică faptul că realitățile și estimările proiectului nu vor fi evaluate, deoarece nu sunt atașate liste de prețuri ale proiectului.

### <a name="price-list-default-on-project-contracts"></a>Listă de prețuri implicită pentru contractele proiectului 
Sistemul finalizează următorul proces pentru a determina ce listă de prețuri va fi implicită pentru un contract de proiect:

1. Dacă contractul este creat dintr-o ofertă, listele de prețuri ale proiectului ale ofertei sunt copiate separat și atașate contractului de proiect.
2. Dacă contractul este creat de la zero, sistemul analizează listele de prețuri atașate listelor de prețuri ale proiectului din cont. Dacă nu există liste de prețuri ale proiectului atașate la înregistrarea contului, sistemul caută liste de prețuri de vânzare atașate parametrilor proiectului care se potrivesc cu moneda contractului de proiect.
4. Apoi, sistemul verifică eficacitatea datei listelor de prețuri care se potrivesc cu intervalul de date al contractului de proiect. Mai exact, data la care a fost creat contractul.
5. Dacă există mai multe liste de prețuri care intră în vigoare pentru data contractului, toate listele de prețuri sunt implicite în contract.
6. Dacă nu există liste de prețuri în vigoare pentru data contractului, nicio listă de prețuri a proiectului nu este implicită în contract. Pe contractul de proiect va apărea un mesaj de avertizare. Mesajul indică faptul că realitățile și estimările proiectului nu vor fi evaluate, deoarece nu sunt atașate liste de prețuri ale proiectului.

## <a name="cost-price-lists"></a>Listele de prețuri de cost

Listele de prețuri de cost nu sunt implicite pentru nicio entitate din Project Operations. Determinarea listei de prețuri de cost pentru a fi utilizate pentru costurile proiectului se face întotdeauna în acest moment. Sistemul finalizează următorul proces pentru a determina ce listă de prețuri trebuie utilizată pentru costurile proiectului:

1. Sistemul analizează mai întâi listele de prețuri atașate unității de organizare contractantă a proiectului.
2. Sistemul analizează apoi data efectivității listelor de prețuri care se potrivesc cu data estimării primite sau a liniei reale. În această situație, *linia estimată* se referă la toate cele trei contexte de estimare din Project Operations:

    - Linia de estimare a proiectului
    - Detaliu linie de ofertă
    - Detaliul liniei de contract
  
3. Dacă există mai multe liste de prețuri care sunt valabile pentru data de pe estimarea primită sau reală, este selectată lista de prețuri creată cel mai recent.
4. Dacă nu există liste de prețuri atașate la unitatea de organizare contractantă a proiectului, sistemul analizează listele de prețuri de cost atașate parametrilor proiectului care se potrivesc cu moneda proiectului.
5. Apoi, sistemul analizează data efectivității listelor de prețuri care se potrivesc cu data estimării primite sau a liniei reale. 
6. Dacă există mai multe liste de prețuri care sunt valabile pentru data de pe estimarea primită sau reală, este selectată lista de prețuri creată cel mai recent.
7. Dacă nu există liste de prețuri de cost atașate parametrilor proiectului care să corespundă monedei și datei efective, sistemul face implicită rata de cost la zero (0) pe estimarea de intrare sau pe linia reală.


[!INCLUDE[footer-include](../includes/footer-banner.md)]