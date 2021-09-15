---
title: Revizuirea resurselor propuse
description: Acest subiect furnizează informații despre modul de propunere a resurselor de proiect.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b3077f98052fcac9989a81b2fab12fa30d65d970
ms.sourcegitcommit: ebcaec7806ee8aee1323ef532d5b7735d27edd04
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403810"
---
# <a name="review-proposed-resources"></a>Revizuirea resurselor propuse

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Managerii de resurse pot propune o resursă către managerul de proiect utilizând o solicitare de resurse.

Pentru a examina resursele propuse, urmați acești pași:

1. Din grila **Solicitare** sau din solicitarea în sine,selectați **Găsire resurse**.
2. Pe pagina **Asistent planificare**, selectați resursa și apoi confirmați că toate orele propuse sunt incluse în rezervarea propusă.
3. În panoul **Creare rezervare de resurse**, setați câmpul **Stare rezervare** în **Propus**, apoi selectați **Rezervare**.

    > [!NOTE]
    > Setarea **Stării rezervării** în **Propus** nu rezervă definitiv resursa și nu înlocuiește resursa generică cu membrul desemnat al echipei.

    Apar următoarele actualizări de stare:

    - În pagina **Asistent planificare**, indicatorii de stare sunt actualizați pentru a indica faptul că rezervarea este propusă, nu rezervată ferm.
    - La solicitarea de resurse, starea se modifică la **Necesită revizuire**.
    - În fila **Echipă** a proiectului, valoarea de **Stare solicitare** a membrului generic al echipei este schimbată la **Necesită revizuire**.

Managerul de proiect poate accepta sau respinge propunerea.

Atunci când managerii de resurse procesează solicitările de resurse, pot utiliza oricare dintre următoarele abordări:

- Propun mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a îndeplini orele necesare. Orele propuse sunt apoi împărțite între mai multe resurse care pot satisface orele necesare. În acest scenariu, orele nu se pot suprapune.
- Propun mai puține resurse decât sunt necesare. În acest scenariu, capacitatea de resurse propusă este mai mică decât orele necesare pe care le-a indicat solicitantul. Atunci când solicitantul acceptă resursele propuse, este creată o cerință de resursă neîndeplinită pentru a captura cererea rămasă.
- Rezervă mai multe resurse pentru a satisface cererea dacă nu este disponibilă nicio resursă unică pentru a finaliza lucrarea.
- Rezervă mai puține resurse decât sunt necesare. În acest scenariu, orele rezervate sunt mai puține decât orele necesare. Sistemul vă ghidează să propuneți resurse în loc de rezervări, astfel încât solicitantul să poată verifica și urmări cererea rămasă.

## <a name="resource-availability"></a>Disponibilitatea resursei

Managerii de resurse trebuie să poată vizualiza disponibilitatea resurselor și să actualizeze rezervările. În unele cazuri, nu există o cerere formală (cerere de resurse). Cu toate acestea, un manager de resurse trebuie să răspundă unei cereri neplanificate care vine prin alte canale, cum ar fi e-mailuri, apeluri telefonice sau mesaje instant. Managerii de resurse utilizează **Tabloul de planificare** pentru a actualiza resursele și rezervările.

Programul de lucru al resurselor se utilizează pentru calcularea disponibilității unei resurse. Rezervările de resurse consumă capacitatea resurselor.

**Tabloul de planificare** folosește culori și umbrire pentru a afișa rezervările, disponibilitatea și rezervările excedentare, precum și starea rezervărilor. O setare de pe **Tabloul de planificare** vă permite să afișați o legendă.

În cazul în care lângă o resursă individuală care se poate rezerva în **Tabloul de planificare** apare o săgeată orientată spre dreapta, resursa poate fi extinsă pentru a afișa detalii despre activitatea pe care este rezervată resursa.

Deoarece Dynamics 365 Project Operations utilizează motorul Universal Resource Scheduling, dacă aveți instalat și Dynamics 365 Field Service, puteți vizualiza detaliile rezervărilor de resurse pentru proiecte, comenzi de lucru și orice alte entități la care ați extins programarea.

Pentru a vizualiza detalii suplimentare despre o resursă individuală, faceți clic pe ea cu butonul din dreapta pentru a deschide fișa resursei.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
