---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 12, V3
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 12, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 5f05488a652f7a699aaa5d8e644eae38d7083f404d3c461cdaabd1915b1a710a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004506"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, versiunea actualizată 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA). Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 12. Această versiune are un număr de V3.10.2.34 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2019.

## <a name="update-release-12"></a>Lansarea de actualizări 12

### <a name="bug-fixes"></a>Remedieri de erori

- Timp și cheltuială

    - Remediat: Mesajele de eroare la intrarea în timp au fost actualizate cu un context mai relevant.
    - Remediat: Grila de intrare a timpului și programul afișează corect bara de defilare verticală când este necesar.
    - Remediat: intrările de cost și timp remise pot fi aprobate.
    - Remediat: a fost corectat mesajul de dialog de confirmare a aprobării pentru a reflecta starea aprobării la schimbarea din **Aprobat** la **Înscris**.
    - Remediat: câmpurile **Preț**, **Unitate** și **Cantitate** sunt acum blocate în înregistrarea cheltuieli după ce a fost aprobată.

- Gestionare de proiect

    - Remediat: formularul principal acțiune **Nou** pe **Membru al echipei** a fost eliminat.
    - Remediat: Alocările de resurse au fost actualizate pentru a contoriza erorile de rotunjire inexacte, care duc la o schimbare a datei de încheiere a unei activități.
    - Remediat: în grila de sarcini, pentru utilizator vor apărea erori relevante din partea serverului.
    - Remediat: Numele membrului echipei este acum redat în selecția persoanelor în sarcină în loc de numele poziției.

- Gestionarea de resurse

    - Remediat: Detaliile privind cerințele de resurse pentru proiectele create dintr-un șablon folosesc acum calendarul de proiect.
    - Remediat: Abilitățile și competențele implicit acum de la datele de master de rol la cerința de resursă creată pentru acel rol.

- Sales

    - Remediat: ID-uri de duplicare ale obiectului găsite pe formularul **Contract principal**.
    - Remediat: Logica a fost actualizată pentru a face vizibilă fila **Analiza ofertelor**, astfel încât să afișeze configurația de metadate a filei.
    - Remediat: data contabilității înregistrării efective vine acum de la data intrării timpului/cheltuielilor și nu a datei aprobării.


[!INCLUDE[footer-include](../includes/footer-banner.md)]