---
title: Navigarea în interfața cu utilizatorul
description: Acest subiect oferă informații despre gestionarea proiectului în Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127533"
---
# <a name="navigating-the-user-interface"></a>Navigarea în interfața cu utilizatorul

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

## <a name="overview"></a>Prezentare generală

Formularul principal al proiectului este separat în mai multe file. Fiecare filă reprezintă un nivel diferit de detaliu în cadrul proiectului.

- **Rezumat**: furnizează o descriere a proiectului și cumulează atât performanța planificată, cât și cea reală a proiectului.

    ![Fila și câmpurile Rezumat](media/navigation7.png)

- **Activități**: furnizează detalii cu privire la structura detaliată a proiectului reprezentată de o vizualizare grilă, vizualizare panou și un gantt.

    ![Fila și câmpurile activitate](media/navigation8.png)

- **Echipă**: Oferă detalii cu privire la participanții la proiect. Efortul atribuit fiecărui membru al echipei este, de asemenea, rezumat în acest punct de vedere.

    ![Fila și câmpurile echipă](media/navigation9.png)

- **Alocări de resurse**: Oferă o imagine în timp a efortului pentru fiecare resursă a unui proiect.

    ![Fila și câmpurile de alocare a resurselor](media/navigation10.png)

- **Reconcilierea resurselor**: Oferă o vedere în etape temporale a diferențelor dintre atribuțiile fiecărei resurse denumite și rezervările acestora.

    ![Fila și câmpurile de reconciliere resursă](media/navigation11.png)

- **Estimări**: Oferă o vizualizare pe etape a costurilor și estimărilor de vânzări ale unui proiect.

    ![Fila și câmpurile estimări](media/navigation12.png)

- **Urmărirea**: Oferă o vizualizare care arată progresul sarcinilor în structura detaliată a proiectului pentru efort, cost și vânzări.

    ![Fila și câmpurile urmărire](media/navigation13.png)

- **Vânzări**: Oferă legături profunde către ofertele și contractele asociate proiectului.

- **Estimări de cheltuieli**: Oferă o grilă care definește cheltuielile proiectului pe baza categoriilor de cheltuieli organizaționale.

    ![Fila și câmpurile estimări de cheltuieli](media/navigation14.png)

## <a name="grid-controls"></a>Comenzi ale grilei

Următorul este o scurtă prezentare generală a controalelor tipice găsite în diferitele file de planificare a proiectului.

### <a name="refresh"></a>Reîmprospătați

**Reîmprospătare**: regăsește cele mai recente date de pe server dacă s-au produs modificări după încărcarea grilei.

![Butonul Reîmprospătare](media/navigation7.png)

### <a name="group-by"></a>Grupare după

**Grupare după**: actualizează gruparea rândurilor din grilă pentru a reflecta resursele, rolurile sau categoriile pe baza nevoilor utilizatorului.

![Grupare după butoane](media/navigation6.png)

### <a name="previousnext"></a>Anteriorul/următorul

**Anterior**/**Următorul**: Actualizați perioadele de timp vizibile pe grilele cu etape temporale.

![Butoanele Anterior și Următorul](media/navigation2.png)

### <a name="timescale"></a>Scală timp

**Scală timp**: Modificați agregarea datelor pe etape între zile, săptămâni, luni și ani.

![Buton Scală timp](media/navigation3.png)

### <a name="expand"></a>Extindeți

**Extinde**: Redați grila vizibilă pe ecran complet oferind mai multă capacitate de a vedea roluri suplimentare.

![Buton Extindere](media/navigation4.png)

### <a name="time-phase-by"></a>Scală timp după

**Etapare după**: Actualizați gruparea rândurilor din grilă pentru a reflecta estimările de cost pentru estimările vânzărilor. Acest control se aplică și scriptului estimativ și grilei de urmărire.

![Buton de etapare după](media/navigation0.png)

### <a name="add-column"></a>Adăugare coloană

**Adăugați coloană**: Permite utilizatorului să definească coloanele vizibile din grilă. Doar coloanele care nu sunt disponibile pot fi adăugate la grilele din formularul **Planificarea proiectului**.

![Adăugați buton de coloană](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]