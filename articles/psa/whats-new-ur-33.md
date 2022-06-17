---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 33, V3
description: Acest articol enumeră caracteristicile și remedierile disponibile în Project Service Automation Update Versiunea 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: d9c282e8b95b111ce71fb441e4dbb2d04f904e0f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915431"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol enumeră caracteristicile și remedierile care sunt noi sau modificate pentru Project Service Automation V3, Update Release 33. Această versiune are un număr de compilări V3.10.54.98 și este, în general, disponibilă prin auto-actualizare în iulie 2021.

## <a name="update-release-33"></a>Lansarea de actualizări 33

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:

- Două câmpuri blocate, **msdyn_description** și **msdyn_externaldescription**, sunt editabile după trimitere.
- Apare un mesaj de eroare dacă se creează o cheltuială care nu este legată de un proiect.
- Atunci când se creează o intrare de timp, rolul resursei este implicit un rol inactiv.
- Liniile din jurnal asociate cu o cheltuială retrasă și ștearsă nu sunt șterse.
- Pe **Intrare de timp Formular de creare rapidă**, actualizați vizualizarea **Lista sarcinilor proiectului** pentru a schimba data afișată implicit la data de începere a sarcinii.
- Când creați o intrare de timp din fila **Corelate** a resursei rezervabile, intrarea de timp este creată incorect pentru utilizatorul conectat în locul resursei principale rezervabile.
- Se adaugă câmpuri noi la căsuța de dialog **Aprobare în bloc MDD**.

**Planificarea unui proiect**

S-au remediat următoarele probleme:
- Performanță lentă la crearea proiectului atunci când șabloanele pentru orele de lucru la proiect sunt aplicate cu calendare complexe.
- Când data de începere este ulterioară față de data de încheiere, se afișează o eroare pe șablonul de copiere a proiectului din cauza diferențelor în componenta de timp a fiecărui câmp.

**Gestionarea resurselor**

S-au remediat următoarele probleme:
- Un parametru incorect este utilizat în interogarea utilizării resurselor și XML duce la rezultate incorecte ale filtrului pe grila **Utilizarea resurselor**.
- Confirmarea **Extindere rezervări** afișează data incorectă de încheiere a rezervărilor.

**Vânzări**

S-au remediat următoarele probleme:
- Apare un mesaj de eroare dacă se creează un preț de categorie cu valori lipsă.
- Apare un mesaj de eroare dacă se creează o etapă a liniei de contract fără o linie de comandă.
