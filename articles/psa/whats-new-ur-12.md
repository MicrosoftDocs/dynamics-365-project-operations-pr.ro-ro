---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 12, V3
description: Acest articol oferă informații despre noutățile din Project Service Automation Update Versiunea 12, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922651"
---
# <a name="project-service-automation-update-release-12-v3"></a>Project Service Automation, versiunea actualizată 12, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA). Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol enumeră caracteristicile și remedierile care sunt noi sau modificate pentru Project Service Automation V3, Update Release 12. Această versiune are un număr de V3.10.2.34 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2019.

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
