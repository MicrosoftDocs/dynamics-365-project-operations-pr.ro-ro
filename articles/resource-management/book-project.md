---
title: Rezervarea pentru un proiect
description: Acest articol furnizează informații despre rezervarea unei resurse pe un proiect.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928539"
---
# <a name="book-to-a-project"></a>Rezervarea pentru un proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Există momente în care un manager de proiect sau un manager de resurse va trebui să aloce o resursă proiectului fără a fi definită o cerință specifică de la un membru al echipei generice. Acest lucru poate fi realizat într-unul din cele trei moduri.

- Rezervați din grila de membru de echipă
- Rezervarea din tabloul de planificare
- Rezervați din formularul **Proiect**

## <a name="book-from-the-team-member-grid"></a>Rezervați din grila de membru de echipă

Dacă organizația dvs. funcționează în modul hibrid de alocare a resurselor, managerul de proiect poate rezerva o resursă direct la proiect, parcurgând pașii următori.

1. Din proiect, accesați grila membrilor echipei și selectați **Nou**.
2. Definiți numele poziției și rolul resursei.
3. Selectați resursa care se poate rezerva din căutarea disponibilă.
4. După ce selectați resursa, definiți următoarele informații de câmp pentru a rezerva resursa:

    - Dată de început
    - Data de terminare
    - Metodă de alocare
    - Ore, dacă este cazul
    - Aprobator de proiect

6. Selectați **Salvare și închidere**

## <a name="book-from-the-schedule-board"></a>Rezervarea din tabloul de planificare

Atunci când un manager de resurse trebuie să rezerve o resursă direct la un proiect, acesta poate folosi tabloul de planificare și cerința proiectului. Cerința proiectului este o cerință de resurse care este întotdeauna disponibilă pentru a fi rezervată. Parcurgeți pașii următori pentru a rezerva direct la un formular de proiect din panoul de planificare.

1. Navigați la tabloul de planificare și în pagina din stânga, filtrați pentru resursele pe care le luați în considerare pentru cerință.
2. În panoul de jos, selectați fila **Proiect** pentru a vizualiza o listă cu cerințele proiectului.
3. Trageți cerința pe o resursă și definiți următoarele informații:

    - Data de început
    - Data de terminare
    - Starea rezervării
    - Metodă de rezervare
    - Durată
   
   > [!NOTE]
   > În prezent, Dynamics 365 Project Operations nu acceptă tabloul de planificare.   

## <a name="book-from-the-project-form"></a>Rezervați din formularul Proiect

În calitate de manager de proiect, este posibil să trebuiască să rezervați o resursă la un proiect, dar să cunoașteți doar criteriile, mai degrabă decât numele resursei. Parcurgeți pașii următori pentru a utiliza asistentul de planificare pentru a găsi o resursă bazată pe orice atribute disponibile ale resursei. 

1. Navigați la proiect și selectați **Rezervare** pentru a deschide Asistentul de planificare.
2. Folosind filtrele din partea stângă a Asistentului de planificare, restrângeți criteriile și selectați **Căutare.**
3. Pe baza resurselor returnate în rezultate, puteți rezerva o resursă.

> [!NOTE]
> Această metodă nu creează nicio rezervare pentru resursă. În schimb, adaugă resursa la echipă. După ce membrul echipei a fost adăugat la proiect, managerul de proiect poate utiliza menținerea rezervărilor sau extinde rezervările pentru a adăuga rezervările necesare la resursă.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
