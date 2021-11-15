---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 37, V3
description: Acest subiect listează caracteristicile și remedierile disponibile în Actualizarea Microsoft Dynamics 365 Project Service Automation, versiunea 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727620"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 37, V3. Această versiune are un număr de versiune V3.10.58.120 și este, în general, disponibilă printr-o actualizare automată în noiembrie 2021.

## <a name="update-release-37"></a>Lansarea de actualizări 37

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**
- Utilizatorii nu pot șterge o intrare de timp prin ștergerea celulei.
- Vizualizarea **Aprobarea mea eșuată** conține numai aprobări de proiecte cu statutul de **Trimis**.

**Gestionarea proiectelor**
- Utilizatorii primesc o eroare de excepție de referință nulă atunci când deschid un proiect în programul de completare Microsoft desktop, dacă numele poziției membrului echipei de proiect este gol.
- Nu există un buton de **Salvare** de pe pagina **Activitatea proiectului** astfel încât utilizatorii să nu poată salva modificările aduse înregistrărilor sarcinilor.
- Utilizatorii nu pot șterge un proiect care are o sarcină asociată unei oferte cu un statut de **Câștigat**.

**Vânzări**
- Câmpul **Valută** de pe pagina **Proiect** este actualizată pentru a se potrivi cu moneda șablonului aplicat.
- Costul este calculat incorect pentru sarcinile care au mai multe monede.
