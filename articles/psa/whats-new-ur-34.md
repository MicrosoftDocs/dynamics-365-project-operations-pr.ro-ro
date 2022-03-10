---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 34, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323296"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 34. Această versiune are un număr de compilări V3.10.55.38 și este, în general, disponibilă prin auto-actualizare în iulie 2021.

## <a name="update-release-34"></a>Lansarea de actualizări 34

### <a name="bug-fixes"></a>Remedieri de erori
S-au remediat următoarele probleme.

**General**

- Actualizările generate de editor nu activează noul flux de lucru de aprobare modern.
- Atributele **Starea țintei** și **Tipul acțiunii** lipsesc pe pagina principală **Set de aprobare**.

**Timp și cheltuială**

- Nu s-a putut aproba o cerere de rechemare folosind fluxul modern de aprobare.
- Copierea unei săptămâni de intrări de timp nu funcționează atunci când copiați intrări care nu au legătură cu utilizatorul conectat.

**Planificarea unui proiect**

- Contururile de alocare a resurselor sunt deteriorate atunci când se importă din programul de completare desktop Microsoft Project.

**Gestionarea resurselor**

- Când publicați un proiect din programul de completare client Microsoft Project desktop, data de final a cerințelor existente este modificată.
- Precizia zecimală depășește două poziții zecimale în dialogul de confirmare a rezervărilor extinse.

**Vânzări**

- Când adăugați o linie bazată pe produse cu un produs existent la un contract de proiect, este afișată excepția **cheia nu a fost găsită în dicționar**.
- Clienții potențiali nu pot fi calificați atunci când un tip de comandă este mapat de la un client potențial la o oportunitate.
