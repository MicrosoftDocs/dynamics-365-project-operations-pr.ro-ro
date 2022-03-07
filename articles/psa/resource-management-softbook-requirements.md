---
title: Cerințe de rezervare provizorie
description: Acest subiect oferă informații despre modul de creare a rezervărilor provizorii.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007026"
---
# <a name="soft-book-requirements"></a>Cerințe de rezervare provizorie

[!include [banner](../includes/psa-now-project-operations.md)]

O cerință de resurse poate fi rezervată ferm. O rezervare fermă creează o propunere care consumă capacitatea unei resurse. Propunerea este apoi trimisă înapoi solicitantului spre aprobare. O rezervare provizorie adaugă temporar o resursă la o echipă de proiect și are o stare diferită în panoul de planificare, dar nu consumă capacitatea resursei. Pentru a rezerva provizoriu o resursă din tabloul de planificare, setați câmpul **stare rezervare** la **Provizoriu**.

![Starea de rezervare este setată la Provizoriu.](media/Resource-Management-image77.png)

Când fila **Echipă** este în vizualizarea **Membri denumiți ai echipei**, resursa apare acolo. Orele de rezervare provizorie sunt raportate în coloana **Ore rezervate provizoriu**.

![Orele rezervate provizoriu în vizualizarea membrilor numiți ai echipei.](media/Resource-Management-image78.png)

Membrii echipei rezervați provizoriu pot fi atribuiți sarcinilor.

![Membru al echipei rezervat provizoriu atribuit unei sarcini.](media/Resource-Management-image79.png)

În fila **Reconciliere**, nu sunt afișate rezervări pentru o resursă cu rezervare provizorie, deoarece fila **Reconciliere** ia în considerare numai rezervările ferme.

![Resursă cu rezervare provizorie fără rezervări în fila reconciliere.](media/Resource-Management-image80.png)

> [!NOTE]
> Nu se poate rezerva provizoriu o resursă dintr-o cerință care a fost generată de un membru de echipă generic.

În panoul de planificare, este utilizată o colorare diferită pentru rezervările provizorii pentru o resursă.

![Rezervare provizorie în panoul de planificare.](media/Resource-Management-image81.png)

Pentru a converti o rezervare provizorie într-o rezervare fermă, pe panoul de planificare, faceți clic dreapta pe rezervarea provizorie, apoi selectați **Modificare stare** \> **Rezervare fermă** \> **Ferm**.

![Schimbarea stării rezervării la Ferm.](media/Resource-Management-image82.png)

Rezervarea este schimbată, iar starea se modifică în panoul de planificare. Deoarece starea rezervării este acum **Ferm**, resursa este afișată ca fiind rezervată, iar capacitatea și disponibilitatea acesteia sunt ajustate.

Puteți utiliza aceeași metodă pentru a anula o rezervare fermă sau o rezervare provizorie din panoul de planificare.

Pentru a converti o resursă care este rezervată provizoriu în rezervată ferm pe fila **Echipă** a proiectului, selectați resursa și apoi selectați **Confirmare**.

![Confirmare comandă.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]