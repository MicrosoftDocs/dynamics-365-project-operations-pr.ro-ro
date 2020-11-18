---
title: Crearea unei rezervări de proiect din Panoul de planificare
description: Acest subiect oferă informații despre modul de a crea o rezervare de proiect de la tabloul de planificare.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082813"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Crearea unei rezervări de proiect din Panoul de planificare

Puteți rezerva o resursă pe un proiect direct din fila **Echipă** a proiectului sau generând o cerință de resurse de la atribuirea generică a unui membru al echipei și apoi îndeplinind cerințele generate cu un membru al echipei proiectului.

Puteți rezerva, de asemenea, o resursă pe un proiect direct de la tabloul de planificare. Există trei modalități de a face acest lucru:

- **Rezervarea de la o cerință de resursă generată:** aveți posibilitatea să generați o cerință de resursă după ce creați o resursă generică și atribuiți activități în cadrul unui proiect.

- **Rezervați de la cerința principală:** cerințele primare apar pe panoul de planificare pe fila **Proiect**. 

- **Rezervați de la o cerință de resursă nouă:** aveți posibilitatea să creați o cerință de resursă de la zero și să o asociați cu un proiect. Pe tabloul de planificare, cerința de resursă apare pe fila **Deschidere cerințe**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervarea de la o cerință de resursă generată

Aveți posibilitatea să generați o cerință de resursă generică și să îi atribuiți o activitate sau mai multe activități în cadrul unui proiect. Apoi puteți să generați o cerință de resursă de la membrul de echipă generic. 

1.  Pe tabloul de planificare, această resursă va apărea pe fila **Deschidere cerințe**. Este posibil să trebuiască să utilizați filtre de coloană pe grilă dacă aveți multe cerințele deschise. 

    ![Deschideți fila Cerințe pe panoul Planificare](media/FAQ-Project-Booking-Schedule-Board-1.png "Captură de ecran tablou rezervări și atribuiri")

2. Selectați cerința. Fila **Găsiți disponibilitatea** va apărea în partea de sus a rândului selectat.
 
3. Când selectați fila, modul Asistent de planificare al panoului de planificare se deschide și apoi filtrează resursele disponibile care întrunesc cerințele de resurse. După aceea, puteți rezerva o resursă.

4. Puteți, de asemenea, să glisați și să fixați rândul selectat din partea de jos a tabloului de planificare la o celulă de resursă în grila de mai sus. Atunci când fixați, acesta deschide panoul **Creare rezervare resursă** din partea dreaptă.

    Selectând **Rezervare** se rezervă resursa pe echipa de proiect.

![Panoul Creare rezervare resursă](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervare de la Cerința principală

Crearea unui proiect în Project Service creează automat o cerință de resurse numită Cerință principală. Aceasta este o cerință necompletată, care este folosită pentru a rezerva rapid o resursă cu tabloul de planificare fără a genera o cerință sau a crea una de la zero. Întrucât cerința este necompletată, va trebui să specificați datele, precum și metoda de alocare și orele, dacă este cazul. 

1. Pentru a rezerva o cerință cu Cerința principală, pe tabloul de planificare, selectați fila **Proiect**. Este posibil să fie nevoie să utilizați filtrul de coloană pe coloana **Proiect** dacă aveți multe proiecte.

   ![Filtre de coloană pe panoul de planificare](media/FAQ-Project-Booking-Schedule-Board-2.png "Captură de ecran tablou rezervări și atribuiri")

2. Selectați cerința care are doar numele proiectului ca denumire și are o durată de zero (0).

3. Selectați fila **Găsiți disponibilitatea** care apare pe rând. Aceasta pune panoul Planificare în modul Asistent de planificare și arată resursele disponibile care pot fi rezervate în proiect.

4. Întrucât o **Cerință principală** este o cerință necompletată cu durata zero (0), va trebui să setați durata pe panoul **Creare rezervare resursă** atunci când selectați și rezervați o resursă.

5. Puteți să selectați, de asemenea, **Cerința principală a proiectului** în partea de jos a tabloului de planificare și să o glisați și fixați pe o resursă pentru a o rezerva.
 
    Întrucât **Cerința principală** este o cerință necompletată cu durata zero (0), va trebui să setați durata pe panoul **Creare rezervare resursă** atunci când selectați și rezervați o resursă.
 
    Atunci când rezervați o resursă prin **Cerința principală** pe tabloul de planificare, o adăugați la echipa de proiect fără atribuiri.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervați de la o cerință de resursă nouă
Parcurgeți pașii următori pentru a rezerva dintr-o nouă cerință de resurse. 

1. Accesați **Cerințe resurse** , apoi selectați **Nou** pentru a crea noua cerință de resursă.

2. În fila **Proiect** , selectați un proiect pentru a asocia cerința la proiect.
 
    Pe tabloul de planificare, această cerință nouă se afișează ca **Deschidere cerință** pe care o puteți procesa.

3. Rezervați resursa pentru a o adăuga la echipa de proiect.

4. Acum, că resursa este rezervată, trebuie să atribuiți activități manual.
