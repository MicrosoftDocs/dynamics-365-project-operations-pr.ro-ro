---
title: Propuneți resurse de proiect
description: Acest subiect furnizează informații despre modul de propunere a resurselor de proiect.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdb0dcb2-4421-4ee1-b97d-89a8cdefbd8d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3a7f7c15c3c7a3c39f2b7b9eeb88b9cf0cfdc220
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754824"
---
# <a name="propose-project-resources"></a>Propuneți resurse de proiect

Managerii de resurse pot propune o resursă către managerul de proiect utilizând o solicitare de resurse.

1. Din grila de solicitări sau din cererea în sine,selectați **Găsire resurse**.
2. În pagina **Asistent planificare**, selectați resursa, apoi, în panoul **Creare rezervare resursă**, în câmpul **Stare rezervare**, selectați **Rezervare.**

    ![Resursa propusă selectată.](media/Resource-Management-image62.png)

Apar următoarele actualizări de stare:

- În pagina **Asistent programare**, indicatorii de stare sunt actualizați pentru a indica faptul că rezervarea este propusă, nu rezervată ferm.

    ![Indicatori de stare pentru rezervarea propusă pe pagina Asistent programări](media/Resource-Management-image63.png)

- La solicitarea de resurse, starea se modifică la **Necesită revizuire**.

    ![Starea solicitării de resurse se modifică la Necesită revizuire.](media/Resource-Management-image64.png)

- În fila **Echipă** a proiectului, valoarea de **Stare solicitare** a membrului generic al echipei este schimbată la **Necesită revizuire**.

    ![Starea de solicitare a membrului generic al echipei este schimbată la Necesită revizuire pe fila Echipă.](media/Resource-Management-image48.png)

Managerul de proiect poate accepta sau respinge propunerea.

Atunci când managerii de resurse procesează solicitările de resurse, pot utiliza oricare dintre următoarele abordări:

- Propun mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a îndeplini orele necesare. Orele propuse sunt apoi împărțite între mai multe resurse care pot satisface orele necesare. În acest scenariu, orele nu se pot suprapune.
- Propun mai puține resurse decât sunt necesare. În acest scenariu, capacitatea de resurse propusă este mai mică decât orele necesare pe care le-a indicat solicitantul. Prin urmare, atunci când solicitantul acceptă resursele propuse, este creată o cerință de resursă neîndeplinită pentru a captura cererea rămasă.
- Rezervă mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a finaliza lucrarea.
- Rezervă mai puține resurse decât sunt necesare. În acest scenariu, orele rezervate sunt mai puține decât orele necesare. Sistemul vă ghidează să propuneți resurse în loc de rezervări, astfel încât solicitantul să poată verifica și urmări cererea rămasă.

## <a name="billable-utilization"></a>Utilizarea facturabilă

Resursele pot avea o utilizare facturabilă țintă. Această utilizare țintă este fie definită ca un atribut al rolului implicit al unei resurse, fie setat pe înregistrarea resursei individuale care se poate rezerva. Calculele de utilizare se bazează pe orele efective pe care le-au raportat resursele utilizând intrările de timp aprobate.

Următoarele formule sunt utilizate pentru a calcula utilizarea:

- Utilizare facturabilă = Ore efective taxabile ÷  Capacitate resursă.
- Utilizare non-facturabilă = Timp real cu ID-ul de facturare = non-exigibil, Complementar sau Indisponibil ÷ capacitate resursă
- Intern = Timp real fără contract de vânzare ÷ Capacitate resursă
- Capacitate resursă = Ore de lucru resursă – Absent de la birou – zile nelucrătoare

Puteți găsi vizualizarea de **Utilizare resurse** în panoul **Resurse**.

![Vizualizarea utilizării resurselor](media/Resource-Management-image65.png)

Fiecare celulă din grilă reprezintă procentul de utilizare facturabil al resursei într-o perioadă, cum ar fi o zi, o săptămână sau o lună. Următoarele formule sunt utilizate pentru a colora celulele:

- **Verde:** Utilizare facturabilă \>= Utilizarea țintă a resursei.
- **Galben:** Utilizare țintă – 20 \<= Utilizare facturabilă \< Utilizare țintă.
- **Roșu:** Utilizare facturabilă \< utilizare țintă – 20.

Deoarece vizualizarea **Utilizare resurse** se bazează pe tabloul de planificare, aveți posibilitatea să utilizați capacitățile de filtrare ale tabloului de planificare pentru a filtra rezultatele.

Grila necesită să setați o utilizare țintă fie pe rol, fie pe resursa individuală. Pentru a face această configurare, accesați **Resurse**\> **Roluri resurse**.

În plus, un rol implicit trebuie să fie atribuit fiecărei resurse care se poate rezerva. Accesați **Resurse**\> **Resurse**. În fila **Project Service**, verificați că este definit un rol de resursă și că câmpul **Este implicit** pentru acesta este setat la **Da**. Aveți posibilitatea să adăugați roluri suplimentare acolo unde **Este implicit = Nu**. Rolul în care **Este implicit = da** este utilizat pentru a evalua utilizarea resursei față de obiectivul pentru rolul respectiv.

![Set de roluri implicite](media/Resource-Management-image67.png)

În fila **Project Service**, puteți seta, de asemenea, o utilizare țintă individuală pentru resursă. Calculul utilizării folosește apoi acea utilizare țintă pentru a evalua ținta resursei în locul țintei rolului implicit al resursei.

Utilizarea este afișată pentru o resursă numai în cazul în care resursa are aprobat timp taxabil în perioada afișată în grilă.

## <a name="resource-availability"></a>Disponibilitatea resursei

Este esențial ca managerii de resurse să poată vizualiza disponibilitatea resurselor și să actualizeze rezervările. în unele cazuri, nu există nicio cerere formală (cerere de resurse), dar un manager de resurse trebuie să răspundă la o cerere neplanificată care vine prin canale, cum ar fi un e-mail, apel telefonic sau mesaj instant. Managerii de resurse utilizează tabloul de planificare pentru a actualiza resursele și rezervările.

Programul de lucru al resurselor se utilizează ca bază pentru calcularea disponibilității unei resurse. Rezervările de resurse consumă capacitatea resurselor.

![Bord de planificare](media/Resource-Management-image68.png)

Consiliul de planificare utilizează culori și umbrire pentru a afișa rezervările, disponibilitatea și rezervările excedentare și, de asemenea, starea rezervărilor. O setare din setările panoului de planificare vă permite să afișați o legendă.

În cazul în care o săgeată orientată spre dreapta apare lângă o resursă individuală care se poate rezerva în tabloul de planificare, resursa poate fi extinsă pentru a afișa detalii despre activitatea pe care este rezervată resursa.

![Resursă care poate fi rezervată extinsă în panoul de planificare](media/Resource-Management-image69.png)

Deoarece Dynamics 365 Project Service Automation utilizează motorul Universal Resource Scheduling, dacă aveți instalat și Dynamics 365 Field Service, puteți vizualiza detaliile rezervărilor de resurse pentru proiecte, comenzi de lucru și orice alte entități la care ați extins programarea.

![Detalii privind rezervările de resurse pentru proiecte și comenzi de lucru](media/Resource-Management-image70.png)

Pentru a vizualiza mai multe detalii despre o resursă individuală, faceți clic cu butonul din dreapta pe acesta pentru a deschide fișa resursei.

![Cardul de resurse](media/Resource-Management-image71.png)
