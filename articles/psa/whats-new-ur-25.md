---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 25, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2d24403b1bf6a06cc138de3f0158f675f6d3b6ec
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581529"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și remedierile noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 25 Această versiune are un număr de compilare de V 3.10.43.76 și este, în general, disponibilă prin auto-actualizare în octombrie 2020.

## <a name="update-release-25"></a>Lansarea de actualizări 25

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

A fost rezolvată următoarea problemă:

- Diagrama de introducere a timpului care arată date suplimentare pe baza unui interval prea mare de recuperare.

**Gestionarea resurselor**

A fost rezolvată următoarea problemă:

- A fost adăugat codul de implementare a pachetului Package Deployer pentru a omite importarea patch-urilor Universal Resource Scheduling dacă există deja o versiune superioară de patch-uri.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Corecții de rotunjire și discrepanțe de curs valutar care rezultă în costuri planificate incorecte în grila de urmărire a proiectului.
- Sprijiniți capacitatea de a afișa două sau mai multe grile de reacție pe formularul **Proiect**.
- Validare oferită pentru a aborda capacitatea de a atribui o sarcină după data de încheiere a calendarului, ceea ce duce la o alocare a resurselor eșuată.
- Îmbunătățirea gestionării erorilor pentru a aborda excepția de referință nulă generată din următoarele:

    - **PreValidateProjectTeamMemberCreate** insert
    - **PreValidateProjectTaskCreate** când se creează o sarcină de proiect fără un proiect asociat
    - **PreProjectTeamMemberCreate** insert
    - **PostProjectTeamMemberDelete** insert
    - **PreValidateProjectTaskDelete** insert

**Sales**

S-au remediat următoarele probleme:

- Îmbunătățirea gestionării erorilor pentru a aborda excepțiile de referință nule generate de **Copiați proiectul: estimări HelperResource Management**.
- **Nu este pregătit pentru facturare** pe o **Restanță de facturare de timp și materiale** nu șterge starea de facturare.
- S-au corectat butoanele **Prețuri** etichetate greșit pe filele **Prețul rolului** și **Articole din catalog**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
