---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 29, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010486"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 29. Această versiune are numărul de versiune V3.10.47.7 și este în general disponibilă printr-o actualizare automată în februarie 2021.

## <a name="update-release-29"></a>Lansarea de actualizări 29

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- Utilizatorii nu pot vizualiza orele de lucru înregistrate în zilele nelucrătoare în grila de introducere a timpului.
- Intrările de cheltuieli aprobate pot fi editate în grilă.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Lipsa logicii de validare pentru a asigura orele de efort de atribuire a resurselor nu poate fi negativă.
- Acțiunea personalizată, **AtribuireResursePentruSarcină** actualizează toate câmpurile în loc să actualizeze doar câmpurile modificate.
- Când copiați un proiect într-un mediu cu inserturi sau fluxuri de lucru înregistrate pe evenimentul **CreațiProiect**, atributul **msdyn_bulkgenerationstatus** nu este actualizat dacă **CopiațiWBSLaProiect** eșuează.
- Când extindeți calendarul proiectului, zilele lucrătoare nu sunt sortate în ordine crescătoare, cauzând eșecul unor actualizări ale sarcinilor proiectului.
- Schimbarea managerului de proiect pe un proiect existent declanșează logica implicită a unității organizaționale.

**Vânzări**

S-au remediat următoarele probleme:

- Fila **Executarea contractului** de pe pagina **Contract** eșuează în mod silențios în timpul inițializării când nu există linii de contract.