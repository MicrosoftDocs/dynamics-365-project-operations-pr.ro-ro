---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 15, V3
description: Acest articol oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea de actualizare 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: b87cae2cd8913457c2931d1661a57509d1398d29
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915659"
---
# <a name="project-service-automation-update-release-15-v3"></a>Project Service Automation, versiunea actualizată 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Dynamics 365 Project Service Automation (PSA). Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online și accesați pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, versiunea de actualizare 15. Această versiune are un număr de V3.10.5.28 și este, în general, disponibilă printr-o auto-actualizare în ianuarie 2020.

## <a name="update-release-15"></a>Lansarea de actualizări 15 

### <a name="enhancements"></a>Îmbunătățiri

- Gestionare de proiect

### <a name="bug-fixes"></a>Remedieri de erori

- Timp și cheltuială

  - Soluție: Adăugați gestionarea erorilor la încărcare în vizualizarea de reconciliere.
  - Soluție: Hub Resource Project: Redenumește **Cantitate** pentru a reduce ambiguitatea.
  - Remediat: Reglați vizualizarea **Copiere Coloane intrare de timp** pentru a include tipul.
  - Remediat: editarea duratei de intrare a timpului în vizualizarea grilei folosind numere zecimale are ca rezultat o eroare necunoscută pentru unele numere.

- Gestionare de proiect

  - Remediat: Meniul derulant pentru **Folosiți în Urmărirea vizualizării** acum se extinde pe baza lățimii opțiunilor.
  - Remediat: Când gestionați proiecte în fusul orar +13, calculele sarcinilor pot afișa rezultate inexacte.
  - Remediat: **Ora de terminare a membrilor echipei** a fost corectat la utilizarea unui calendar de 24 de ore.
  - Remediat: a fost reactivat **FTB** în formularul principal **msdyn_project**.
  - Remediat: calculul misiunilor nu mai ignoră într-o zi.
  - Remediat: Un nou banner de notificări a fost adăugat la formularul de proiect atunci când fusul orar diferă între utilizator și proiect.

- Sales

  - Remediat: căutarea categoriei estimării cheltuielilor poate fi utilizată pentru a filtra duplicatele.
  - Remediat: Cod **PluginDomain.ExecuteInTryCatchBlock (..)** nu mai ascunde originea excepției.
  - Remediat: Nu mai primiți un mesaj de eroare **Cercetare proiect** în formularul **Linie de ofertă** când există mai mult de 1000 de proiecte.
  - Remediat: gria **Estimări** pentru estimările forței de muncă și estimările cheltuielilor afișează acum simbolul corect al monedei.
  - Remediat: După ce o organizație actualizează PSA de la Update Release 14 la Update Release 15, fila **Planificare** nu mai apare la fel de goală pe formularul **Proiect**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
