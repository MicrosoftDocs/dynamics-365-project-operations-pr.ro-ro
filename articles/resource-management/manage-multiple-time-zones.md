---
title: Gestionarea fusurilor orare
description: Când este creat un proiect, fusul orar al acestuia se bazează pe fusul orar definit în șablonul de oră de lucru aplicat.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d3fc0453e3038839107a98c4179e6bd4aede95cf4a5fcfe2d52f823b83029485
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988711"
---
# <a name="manage-time-zones"></a>Gestionarea fusurilor orare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


## <a name="projects"></a>Proiecte

Când este creat un proiect, fusul orar al acestuia se bazează pe fusul orar definit în șablonul de oră de lucru aplicat. Pe **Proiectul** datele sunt întotdeauna relative la fusul orar al utilizatorului care este conectat la fiecare filă, cu excepția filei **Activitate**. Când vizualizați structura detaliată a proiectului, datele vor fi întotdeauna afișate în fusul orar al proiectului.

## <a name="tasks"></a>Activități

Când se creează o activitate, ora de începere, ora de încheiere și orele/ziua sunt controlate de programul de lucru al proiectului. De exemplu, dacă o sarcină este creată cu un proiect al cărui fus orar este -8 PST și are următoarele ore de lucru: de la 9:00 la 17:00 de luni până vineri, orice sarcină creată fără o sarcină va respecta ora de început și ora de încheiere a calendarului proiectului.

## <a name="manage-resources-with-time-zones"></a>Gestionați resursele cu fusuri orare

Pentru rezultate precise și predictibile atunci când se utilizează **Extindeți rezervarea**, există două condiții prealabile cheie care trebuie îndeplinite:  

- Utilizatorul trebuie să configureze fusul orar al dispozitivului său pentru a se potrivi cu fusul orar definit în **Setările de personalizare** ale sistemului.
 
  ![Setările fusului orar în Windows 10.](media/reconcile-assignments-03.png)

  ![Setările fusului orar în setările de personalizare.](media/reconcile-assignments-04.png)
 
- Resursa care poate fi rezervată trebuie să aibă cel puțin un minut de timp de lucru care se suprapune contururilor utilizate pentru a defini extensia solicitată. De exemplu, următoarele resurse cu program de lucru care se încadrează între orele 9:00 și 19:00. 

  ![Comparația contururilor resurselor.](media/reconcile-assignments-05.png)

Tabelul următor afișează:

- Un șablon de calendar de proiect
- Resursa A: Această resursă are același calendar și se află în același fus orar cu proiectul. Ora de început a rezervărilor va fi ora 9:00.
- Resursa B: această resursă se află într-un alt fus orar decât proiectul și începe la ora 7:00 în fusul orar al acestora. Cu toate acestea, rezervările vor începe la ora 9:00, deoarece aceasta este cea mai timpurie perioadă de începere a conturului misiunii.
- Resursele C și D: resursele sunt situate în diferite fusuri orare, ambele diferite între ele și de proiect, iar rezervările lor încep nu mai devreme decât orele lor de început disponibile.

|Entity  |Calendar   |
|-|-|
|Șablon de calendar de proiect   | ![calendarul proiectului.](media/reconcile-assignments-06.png) |
|Resursă A  | ![Calendar resursa A.](media/reconcile-assignments-06.png) |
|Resursă B  |  ![Calendar resursa B.](media/reconcile-assignments-07.png) |
|Resursă C  |  ![Calendar resursa C.](media/reconcile-assignments-08.png) |
|Resursă D  | ![Calendar resursa D.](media/reconcile-assignments-09.png)  |
 
Când navigați la vizualizarea **Reconciliere**, sunt afișate alocările de resurse și lipsa de rezervare asociată.

![Vedere de reconciliere înainte de extensie.](media/reconcile-assignments-10.png)

După ce funcționalitatea de rezervare extinsă a fost utilizată pentru fiecare resursă, rezervările sunt extinse cu succes pentru fiecare resursă, deoarece orele de lucru ale fiecărei resurse s-au suprapus cu contururile deficitului.

![Vizualizare de reconciliere după extinderea rezervării.](media/reconcile-assignments-11.png) 

Observați că o privire mai atentă asupra detaliilor rezervărilor arată diferențe în momentul începerii rezervărilor. Rezervările încep nu mai devreme de ora de începere a conturului de atribuire și nici mai devreme de ora de începere disponibilă a resursei.

![Rezervări noi ale resurselor din tabloul de bord.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]