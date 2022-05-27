---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 16, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 16, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5651f8b3a2ddf406fcfd7a4e21901c53789fa4ed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577389"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, versiunea actualizată 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.  Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea unei soluții preferate](/dynamics365/project-service/upgrade-psa-home-page).
Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 16. Această versiune are un număr de V3.10.6.34 și este, în general, disponibilă printr-o auto-actualizare în ianuarie 2020.


## <a name="update-release-16"></a>Lansarea de actualizări 16

### <a name="bug-fixes"></a>Remedieri de erori

-   Timp și cheltuială

    -   Soluționat: Utilizatorii care încearcă să trimită intrări de timp și cheltuieli șterse pentru aprobări vor primi acum mesaje de eroare relevante.

-   Gestionare de proiect

    -   Soluționat: Unitățile de resurse definite pentru membrii echipei din șabloane sunt respectate cu șabloanele care se aplică unui nou proiect.

    -   Soluționat: o gestionare îmbunătățită a realocării proprietății înregistrărilor.

    -   Soluționat: proiectele care sunt în proces de copiere nu vor putea fi copiate până la finalizarea tuturor operațiunilor de copiere.

-   Gestionarea de resurse

    -   Soluționat: Extinderea rezervărilor gestionează acum duratele scurte corect și nu mai creează zero ore pentru rezervările extinse.

    -   Soluționat: Vizualizarea de reconciliere se face acum când fusul orar al proiectului este +5:30 GMT și timpul de utilizare al utilizatorului este diferit.

-   Sales

    -   Soluționat: Când un proiect mapat la o linie de contract este eliminat și un nou proiect este mapat, înregistrările efective ale noului proiect nu erau reevaluate pe baza regulilor de facturare și prețuri definite pe linia contractului. Acest lucru a fost soluționat în această versiune. Prețurile și înregistrările efective ale proiectului nou mapat vor fi inversate și re-create în mod corect pe baza regulilor de stabilire a prețurilor și de facturare a liniei de contract. Ca urmare, înregistrările reale ale proiectului care nu a fost mapat vor fi reevaluate și re-create.

    -   Soluționat: validarea suplimentară a fost adăugată la linia estimativă în câmpul **Cantitate** pentru a se asigura că valorile nule nu persistă.

    -   Soluționat: Când datele reale au fost actualizate pe un proiect, a fost adăugat un buton de actualizare în formularul principal al proiectului, pentru a permite utilizatorilor să resincronizeze datele reale.

    -   Soluționat: Când utilizatorii trec de la 2.X la 3.X, proiectele cu o valoare NULL pentru numele proiectului vor fi permise.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
