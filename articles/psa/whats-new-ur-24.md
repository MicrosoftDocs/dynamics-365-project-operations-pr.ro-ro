---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 24, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948930"
---
# <a name="project-service-automation-update-release-24-v3"></a>Project Service Automation, versiunea actualizată 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 24. Această versiune are un număr de versiune V 3.10.42.43 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2020.

## <a name="update-release-24"></a>Lansarea de actualizări 24

### <a name="bug-fixes"></a>Remedieri de erori

**Sales**

S-au remediat următoarele probleme:

- Problemă la stabilirea listei de prețuri implicite a produselor.
- Performanța câștigului Ofertei este lentă din cauza listei de prețuri încorporate și a copiilor înregistrărilor de prețuri de roluri.
- **Contract proiect/Hub de vânzări** > **Linie produs/Cantitate linie comandă** este rotunjit automat la cel mai apropiat număr întreg.
- Creșteți la privilegiile de sistem atunci când citiți listele de prețuri.
- Copiați câmpurile de adresă ale clientului **address1_freighttermscode** și **address1_shippingmethodcode** la Ofertă/Comandă. 


**Timp și cheltuială**

S-au remediat următoarele probleme:

- **Grila de introducere timp** nu acceptă comportamentul de timp **Numai dată**.
- **Intrare timp** nu se reîmprospătează automat. Este necesară o reîmprospătare manuală.
- Nu se pot importa intrările de timp dintr-o atribuire atunci când există o pauză (0 ore) în atribuirile unei resurse.
- Când creați o intrare de timp, setați startul identic cu **msdyn_date**.
- Reactivați editarea în bloc pentru introducerea timpului.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- Încercarea de a actualiza starea unei rezervări inter-zile fără o cerință va genera o excepție de referință nulă.
- Eroare la încărcarea **Vizualizare reconciliere**.


**Gestionare de proiect**

S-au remediat următoarele probleme:

- În **Planificare proiect**, la schimbarea de la **Manual** la **Auto**, salvarea automată nu se finalizează.
- Costurile cheltuielilor nu ar trebui să se calculeze în raport cu varianța pe **Grila de urmărire a proiectului**.
- Comportament neconstant pentru coloanele **Etichetă estimativă** în timpul încărcării versus schimbarea tipului **Fază de timp**.
- Este posibil ca costul real al unui proiect să nu reflecte totalurile din **Valori reale**.
- **Data estimată de finalizare** de pe fila **Rezumat** nu se potrivește cu **Planificare WBS**.
- **Actualizați orele reale** pe outdent nu funcționează corect.
- Un manager de proiect în afara rădăcinii **BU** nu poate crea un proiect.
- Modificările activității sau categoriei pe **Estimări de cheltuieli** nu sunt persistente.
- **Copie contract** copiază planificările facturilor și starea de rulare.
- Butonul **Actualizați datele reale** calculează incorect activitățile de rezumat.
- Program de completare Microsoft Project: Remediați eroarea de referință nulă dacă un membru al echipei are o unitate de resurse goală.



[!INCLUDE[footer-include](../includes/footer-banner.md)]