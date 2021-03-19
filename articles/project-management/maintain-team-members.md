---
title: Menținerea membrilor echipei
description: Acest subiect oferă informații despre rezervarea resurselor numite pentru echipe de proiect și atribuirea lor către activități.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286848"
---
# <a name="maintain-team-members"></a>Menținerea membrilor echipei

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Puteți adăuga o resursă numită echipei dvs. de proiect, rezervând-o direct echipei.

1. În Dynamics 365 Project Operations, accesați **Proiecte** și selectați și deschideți proiectul pentru care faceți rezervarea.
2. Pe pagina **Proiect**, în fila **Echipă**, selectați **Nou**. 
3. În caseta de dialog **Creare rapidă membru echipă proiect**, selectați resursa care se poate rezerva. Câmpul **Rol** se va popula cu rolul implicit al resursei, dacă aceasta are unul atribuit. Aveţi posibilitatea de a schimba rolul. 
4. Selectați datele de la și până la care resursa va fi necesară și selectați metoda de alocare a capacității resursei. 
5. În câmpul **Aprobator de proiect**, selectați **Da** dacă doriți ca membrul echipei să fie aprobator de proiect. Membrul echipei poate aproba intrările de timp și cheltuieli remise pentru acest proiect. 
6. Selectați **Salvare**.

Acum aveți posibilitatea să atribuiți resursa rezervată activităților din proiect. Pe pagina **Proiect**, pe fila **Planificare** atribuiți activități la noua resursă. Selectorul de resurse care este lansat din câmpul **Resurse** din grila de activități va afișa membrii echipei pe care îi puteți selecta.


În Project Operations, rezervările de resurse și atribuțiile de sarcini nu sunt strâns legate. Atunci când utilizați selectorul de resurse din planificare, aveți posibilitatea să atribuiți activități membrilor echipei pentru mai multe ore decât acoperă rezervările lor pe proiect.

Diferențele dintre rezervările și atribuțiile membrilor echipei sunt afișate pe filele **Echipă** și **Reconcilierea resurselor**. De asemenea, puteți reconcilia diferențele dintre rezervări și sarcini pentru resurse la un nivel mai detaliat.

Utilizați selectorul de resurse în fila **Planificare** pentru a căuta și selecta resurse rezervabile care nu fac deja parte din echipa de proiect. Aceste resurse sunt afișate în selectorul de resurse ca **Alte resurse**.

Când faceți o alegere, resursa este adăugată la echipa de proiect și atribuită sarcinii, dar nu sunt generate rezervări.

Aveți posibilitatea să utilizați capacitatea Extindere rezervare a filei **Reconciliere** sau **Tablou de planificare** pentru a rezerva capacitatea resursei la proiect.

După ce un membru al echipei este rezervat în cadrul proiectului dvs., aveți posibilitatea să utilizați **Mențineți rezervările** sau direct **Tablou de planificare** pentru a gestiona rezervările acestuia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]