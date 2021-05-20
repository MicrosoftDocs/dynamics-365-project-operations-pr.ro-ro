---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 31, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945550"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 31. Această versiune are un număr de versiune V3.10.52.77 și este disponibil în general printr-o autoactualizare în mai 2021.

## <a name="update-release-31"></a>Lansarea de actualizări 31

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- Butoanele de comandă pentru introducerea timpului de pe pagina **Resursă ce se poate rezerva** erau confuze.
- O excepție de referință nulă a fost generată în **Project.SetTrackingFields** la aprobarea unei intrări de timp.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- **Creare membru echipă** nu afișează corect setarea metadatelor de configurare a rezervării pentru **Stare rezervare comisă implicită**.
- La actualizarea de la PSA 1.X la 3.X, procesul de actualizare eșuează la **UpgradeResourceRequirements**.


**Vânzări**

S-au remediat următoarele probleme:

- Venitul real convertește sumele în moneda proiectului din grila de urmărire.
- Valoarea implicită a monedei nu este clară la crearea liniilor jurnal, a liniilor de ofertă și a liniilor de contract în scenarii în care moneda de bază a unei organizații diferă de moneda proiectului.
- Interogarea **Validarea de jurnal de corecții în așteptare** nu se filtrează după proiect.
- Vânzările rămase sunt calculate incorect pe un proiect.
- Ofertele pe bază de contact eșuează atunci când sunt create fără o listă de prețuri.
- Când selectați **Confirmați factura** nu este afișat niciun spinner de procesare.
- Când selectați **Creați factura** nu este afișat niciun spinner de procesare.
- Închiderea unei oferte ca pierdută nu anulează rezervările.







