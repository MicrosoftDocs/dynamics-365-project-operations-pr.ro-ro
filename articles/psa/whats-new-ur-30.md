---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 30, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 30, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 07ca20425d05d1d638d9b2b8c3425562e39dd6627916794d1ad8441f00658459
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987001"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution.md).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 30. Această versiune are un număr de versiune V3.10.51.61 și este disponibil în general printr-o autoactualizare în aprilie 2021.

## <a name="update-release-30"></a>Lansarea de actualizări 30

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- O eroare apare atunci când creați și salvați o intrare de timp pe pagina **Creare rapidă** dacă câmpul **Rol** este eliminat.
- Filtrul de introducere a timpului aplică un operator de filtrare greșit.
- Fișele de timp copiate nu sunt afișate automat când selectați **Copiați săptămâna** pe controlul de intrare a timpului.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- Când extindeți o rezervare, starea rezervării atribuită rezervării hard este incorectă. Extinderea unei rezervări respectă starea rezervării definită ca **Angajat** în metadatele de configurare a rezervării.
- Când nu este specificată o stare de rezervare validă, mesajul de eroare nu este localizat corect.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Proiectele nu pot fi create într-o monedă și includ sarcini conexe într-o altă monedă.

**Vânzări**

S-au remediat următoarele probleme:

- Când se copiază o listă de prețuri, prețurile nu sunt actualizate.
- Închiderea unei cotații ca câștigat eșuează atunci când detaliile despre costuri au o valoare pentru origine.
- Pe entitatea **Activitatea proiectului**, **Cost estimat** a fost redenumit în **Cost planificat (bază)**.
- O excepție de referință nulă este generată atunci când facturile sunt create sau șterse.
