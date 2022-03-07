---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 35, V3
description: Acest subiect listează caracteristicile și remedierile disponibile în Actualizarea Microsoft Dynamics 365 Project Service Automation, versiunea 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 53670e2c7f54f8fccf636b2855e190f5f85c6068
ms.sourcegitcommit: 5bb8ca5055deda57e2b1173a2e45c53b15f61d62
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/03/2021
ms.locfileid: "7473280"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 35, V3. Această versiune are numărul de compilare V3.10.56.110 și este disponibilă publicului larg prin actualizare automată în luna septembrie 2021.

## <a name="update-release-35"></a>Lansarea de actualizări 35

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**Timp și cheltuială**

- Aprobatorul de proiect primește o eroare de privilegiu de citire atunci când aprobă intrările de cheltuieli cu rol de **Aprobator de proiect**.
- Aprobatorul de proiect primește o eroare de privilegiu de scriere la **msdyn_projectapproval** când anulează o înregistrare de timp aprobată cu un rol de **Aprobator de proiect**.
- Când selectați **Copiere săptămână** într-o înregistrare de timp în modulul de aplicație Dynamics 365 for phone - Project Resource Hub, apare următoarea eroare: "...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE."
- Politica de **Reîncercare** aprobă automat înregistrările respinse anterior.
- Subgrila **Seturi de aprobare** arată acțiuni din panglică neaplicabile.
- Lipsesc pictogramele pentru **Sarcină de proiect** și **Rol resursă** pentru entitatea **Înregistrare timp**.
- Când importați alocări de resurse, înregistrările de timp importate nu au durata corectă pentru alocările care au fost create prin activități în modul manual.
- **Ștergere** lipsește din pagina **Căutare avansată pentru înregistrări de introducere timp**.
- **Salvare** lipsește din pagina **Informații despre introducerea timpului**. Această problemă împiedică salvarea modificărilor la închiderea paginii.

**Planificarea unui proiect**

- Grilele **Alocare resurse** și **Reconciliere resurse** nu sortează alfabetic atributele grupate.
- Sarcinile nu pot fi create dacă comportamentul datei este personalizat la **Doar dată**.

**Gestionarea resurselor**

- Dacă sunt instalate atât Dynamics 365 Field Service, cât și Project Service Automation, apar probleme de suprapunere atunci când **Vizualizare asociată cu cerința de resurse** este asociat cu o pagină principală.
- Când se face dublu clic pe **Salvare** în caseta de dialog **Creare rapidă membru echipă** , se împiedică crearea cerinței de resurse.

**Vânzări**

- Se generează o excepție dacă ștergeți o activitate asociată cu o ofertă cu starea **Câștigat**.
