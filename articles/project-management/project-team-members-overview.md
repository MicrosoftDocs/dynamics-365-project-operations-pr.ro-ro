---
title: Membrii echipei de proiect
description: Acest subiect oferă informații despre cum să lucrați cu informațiile, atributele și planificarea membrilor echipei de proiect.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908493"
---
# <a name="project-team-members"></a>Membrii echipei de proiect

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Membrii echipei de proiect sunt participanții la proiect care finalizează lucrările la un proiect. Obiectivul grilei membrilor echipei este de a furniza o listă a resurselor numite care sunt angajate în angajament și a membrilor echipei generice care sunt resurse deținătoare de locuri și vor fi încadrate ulterior.

Din grila membrilor echipei, managerul de proiect și ceilalți participanți la proiect au capacitatea de a vedea cine a fost angajat în proiect. De asemenea, pot vizualiza un rezumat al rezervărilor, efortului planificat și alocărilor de resurse individuale. Grila membrilor echipei permite managerilor de proiect să definească cerințele de resurse pentru membrii echipei generice și să gestioneze rezervările membrilor echipei existente.

Următorul tabel listează atributele cheie ale unui membru al echipei de proiect.

| Nume câmp          | Descriere                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metodă de alocare        | Metoda de alocare utilizată pentru a rezerva resurse pentru proiect.                                                                         |
| Tip de facturare             | Selectați dacă membrul echipei este clasificat drept facturabil.                                                                                                                                       |
| Resursă ce se poate rezerva        | Resursa rezervabilă selectată pentru a înlocui resursa generică.                                                                                                                   |
| Stare ștergere            | Starea de ștergere a membrului de echipă pentru a urmări dacă există o solicitare de ștergere trimisă către PSS și dacă PSS trimite răspunsul înapoi cu succes și în fereastra de timp preconizată. |
| Efort total (ore)     | Suma efortului depus de membrii echipei pentru atribuirile lor.                                                                                                                         |
| Efort finalizat (ore) | O urmărire a efortului realizat de membrul echipei în atribuirile sale.                                                                                           |
| Efort rămas (ore) | O urmărire a efortului nefinalizat încă de membrul echipei în atribuirile sale.                                                                                    |
| Terminați                   | Data de sfârșit a apartenenței la echipa de resurse.                                                                                                                                            |
| Ore rezervare fermă        | Orele greu rezervate ale membrului echipei.                                                                                                                                                                |
| Nume poziție            | Numele utilizat pentru a identifica resursa generică.                                                                                                                                   |
| Unitate de finanțare          | Unitatea organizațională a resursei care efectuează lucrarea.                                                                                                                      |
| Aprobator proiect         | Selectați dacă membrul echipei poate aproba orele și cheltuielile.                                                                                                                     |
| Ore obligatorii           | Orele necesare ale membrului echipei din cerința membrului echipei.                                                                                                                       |
| Rol                     | Rolul pe care membrul echipei îl îndeplinește în această echipă.                                                                                                                                |
| Descriere poziție     | Introduceți o descriere a rolului acestui membru al echipei.                                                                                                                             |
| Ore rezervare provizorie        | Orele rezervate provizoriu ale membrului echipei.                                                                                                                                                                 |
| Start                    | Data de început a apartenenței la echipa de resurse.                                                                                                                                          |

Din grila membrilor echipei, pot fi întreprinse următoarele acțiuni:

- **Rezervare**: Pentru organizațiile care execută folosirea metodologiei de rezervare hibridă, acțiunea de carte va permite utilizatorilor să rezerve o resursă numită pe baza cerințelor solicitate generate de membrul echipei generice
- **Generați cerința**: Această acțiune generează cerința.
- **Specificați modelul**: Permite managerilor de proiect să ajusteze contururile cerințelor de resurse la un nivel granular. Managerii de proiect se pot adapta pentru nevoile specifice ale proiectului în cazurile în care distribuția implicită nu se potrivește.
- **Trimite cererea**: Pentru organizațiile care utilizează metodologia centrală a rezervărilor.
- **Editați**: Atributele membrilor echipei pot fi editate, inclusiv unitatea organizațională, rolul și numele poziției.
- **Mențineți rezervările**: Când rezervările de resurse trebuie actualizate, mențineți rezervările permițând managerului de proiect să ajusteze:

    - Start
    - Sfârșit
    - Alocarea efortului total

- **Nou**: Pe lângă adăugarea de resurse direct din planificare, managerii de proiect pot adăuga membrii echipei noi numiți sau generici din grila membrilor echipei.
- **Șterge**: Prin selectarea unuia sau mai multor membri ai echipei, managerul de proiect poate șterge resursele care nu vor mai participa la proiect. Ștergerea unui membru al echipei va șterge, de asemenea, toate atribuirile de resurse asociate și va anula toate rezervările existente.
