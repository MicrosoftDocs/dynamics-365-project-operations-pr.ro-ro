---
title: Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini
description: Acest subiect oferă informații despre rezervarea resurselor numite pentru echipe de proiect și atribuirea lor către activități.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e947986a-e83a-42f4-813e-c82bdfbec33c
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 079ba299f912c75f9ed739d4b6aa3c63189d11d0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754698"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezervați resurse rezervabile numite la o echipă de proiect și atribuiți sarcini 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Puteți adăuga o resursă numită echipei dvs. de proiect, rezervând-o direct pe echipă. Pentru a face acest lucru, efectuați următorii pași.

1. În Project Service Automation, accesați **Proiecte** și selectați și deschideți proiectul pentru care faceți rezervarea.
2. Pe pagina **Proiect**, în fila **Echipă**, faceți clic pe **Nou**. 

![Adăugarea unui membru al echipei din fila echipă](media/RM-how-to-1.png)

3. În caseta de dialog **Creare rapidă membru echipă proiect**, selectați resursa care se poate rezerva. Câmpul **Rol** se va popula cu rolul implicit al resursei, dacă aceasta are unul atribuit. Aveți posibilitatea să schimbați rolul, dacă este necesar. 
4. Selectați datele de la și până la care resursa va fi necesară și selectați metoda de alocare a capacității resursei. 
5. Dacă doriți ca membrul echipei să fie un aprobator de proiect, selectați **Da** în câmpul **Aprobator proiect**. Acest lucru va însemna că membrul echipei poate aproba intrările de timp și cheltuieli remise pentru acest proiect. 
6. Faceţi clic pe **Salvare**.

![Adăugarea unui membru al echipei în formularul de creare rapidă](media/RM-how-to-2.png)


Acum aveți posibilitatea să atribuiți resursa rezervată activităților din proiect. Pe pagina **Proiect**, faceți clic pe fila **Planificare** pentru a atribui activități la noua resursă. Selectorul de resurse care este lansat din câmpul **Resurse** din grila de activități va afișa membrii echipei pe care îi puteți selecta.

![Atribuirea unui membru al echipei la o activitate din fila planificare](media/RM-how-to-3.png)

În versiunea 3 pentru Project Service Automation (PSA), rezervările de resurse și atribuirile de activități nu sunt strâns cuplate. Aceasta înseamnă că atunci când utilizați selectorul de resurse din planificare, aveți posibilitatea să atribuiți activități membrilor echipei pentru mai multe ore decât acoperă rezervările lor pe proiect.
Puteți vedea diferențele dintre rezervările membrilor echipei și atribuiri în fila **Echipă** sau în fila **Reconciliere resurse**. De asemenea, aveți posibilitatea să reconciliați diferențele dintre rezervări și atribuiri pentru resurse la un nivel mai detaliat.

![Fila Reconciliere resurse](media/RM-how-to-4.png)

De asemenea, puteți utiliza selectorul de resurse în fila **Planificare** pentru a căuta și selecta resurse rezervabile care nu fac deja parte din echipa de proiect. Acestea sunt afișate în selectorul de resurse ca **Alte resurse**.

![Atribuirea unei resurse de membru non-echipă la o activitate](media/RM-how-to-5.png)

Când faceți acest lucru, resursa este adăugată la echipa de proiect și atribuită sarcinii, dar nu sunt generate rezervări.

![Membru al echipei cu atribuiri și fără rezervări](media/RM-how-to-6.png)

Aveți posibilitatea să utilizați capacitatea Extindere rezervare a filei **Reconciliere** sau **Tablou de planificare** pentru a rezerva capacitatea resursei la proiect.

![Extinderea rezervărilor pentru un membru al echipei în fila reconciliere resurse](media/RM-how-to-7.png)

După ce un membru al echipei este rezervat în cadrul proiectului dvs., aveți posibilitatea să utilizați Menține rezervările sau să utilizați direct Tabloul de planificare pentru a gestiona rezervările acestuia.
