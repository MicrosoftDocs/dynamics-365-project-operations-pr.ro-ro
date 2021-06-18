---
title: Prezentare generală a utilizării resurselor
description: Acest subiect furnizează informații despre vizualizarea utilizării resurselor în Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000811"
---
# <a name="resource-utilization-overview"></a>Prezentare generală a utilizării resurselor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Resursele pot avea o utilizare facturabilă țintă. Această utilizare țintă este definită ca un atribut al rolului implicit al unei resurse, fie setat pe înregistrarea resursei individuale care se poate rezerva. Calculele de utilizare se bazează pe orele efective pe care le-au raportat resursele utilizând intrările de timp aprobate.

Următoarele formule sunt utilizate pentru a calcula utilizarea:

  - Utilizare facturabilă = Ore efective taxabile ÷ Capacitate resursă.
  - Utilizare non-facturabilă = Timp real cu ID-ul de facturare = non-exigibil, Complementar sau Indisponibil ÷ capacitate resursă
  - Intern = Timp real fără contract de vânzare ÷ Capacitate resursă
  - Capacitate resursă = Ore de lucru resursă – Absent de la birou – zile nelucrătoare

Puteți găsi vizualizarea de **Utilizare resurse** în panoul **Resurse**.

Fiecare celulă din grilă reprezintă procentul de utilizare facturabil al resursei într-o perioadă, cum ar fi o zi, o săptămână sau o lună. Următoarele formule sunt utilizate pentru a colora celulele:

  - **Verde**: utilizare facturabilă >= utilizarea țintă a resursei
  - **Galben**: utilizare țintă – 20 <= utilizare facturabilă < utilizare țintă
  - **Roșu**: utilizare facturabilă < utilizare țintă – 20

Deoarece vizualizarea **Utilizare resurse** se bazează pe tabloul de planificare, aveți posibilitatea să utilizați capacitățile de filtrare ale tabloului de planificare pentru a filtra rezultatele.

Grila necesită să setați o utilizare țintă fie pe rol, fie pe resursa individuală. Pentru a face această configurare, accesați **Resurse** > **Roluri resurse**.

În plus, un rol implicit trebuie să fie atribuit fiecărei resurse care se poate rezerva. Accesați **Resurse** > **Resurse**. În fila **Project Service**, verificați că este definit un rol de resursă și că câmpul **Este implicit** este setat la **Da**. Aveți posibilitatea să adăugați roluri suplimentare acolo unde **Este implicit** = **Nu**. Rolul unde **Este implicit** = **Da** este utilizat pentru a evalua utilizarea resursei față de obiectivul pentru rolul respectiv.

În fila **Project Service**, puteți seta, de asemenea, o utilizare țintă individuală pentru resursă. Calculul utilizării folosește apoi acea utilizare țintă pentru a evalua ținta resursei în locul țintei rolului implicit al resursei.

Utilizarea este afișată numai pentru o resursă numai în cazul în care resursa are aprobat timp facturabil în perioada afișată în grilă.


[!INCLUDE[footer-include](../includes/footer-banner.md)]