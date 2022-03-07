---
title: Seturi de aprobări
description: Acest subiect oferă informații despre setul de aprobări, cereri și subseturile acelor operațiuni.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e57944b3031ff8b6da163125bb6668875ae77bd06f23a5b8c4ef06f396210e4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995506"
---
# <a name="approval-sets"></a>Seturi de aprobări

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aprobarea stabilește cererile de aprobare de grup împreună în subseturi mai mici de operațiuni. Această grupare permite procesarea aprobărilor în ordine de către proiect și permite reîncercarea și secvențierea. Gruparea îmbunătățește fiabilitatea și trasabilitatea procesării aprobărilor pentru volume mari de aprobări.

Seturile de aprobare indică starea generală de procesare a înregistrărilor lor conexe. Când o înregistrare de aprobare este procesată utilizând un set de aprobare, înregistrarea se mută de la **Trimis** la **Aprobat** și este deconectat de la setul de aprobare. Dacă o înregistrare eșuează atunci când este trimisă spre aprobare, înregistrarea rămâne în starea de **Trimis** iar setul de aprobare este marcat ca eșuat. Setul de aprobare înregistrează mesajul de eroare al eșecului.

## <a name="processing-approvals-and-approval-sets"></a>Procesarea aprobărilor și seturilor de aprobare
Aprobările aflate în coadă pentru procesare sunt vizibile în vizualizarea **Procesarea aprobărilor**. Sistemul încearcă să proceseze toate intrările de mai multe ori asincron, inclusiv reîncercarea unei aprobări dacă încercările anterioare au eșuat.

Câmpul **Durata de viață a setului de aprobare** înregistrează numărul de încercări rămase de procesare a setului înainte ca acesta să fie marcat ca eșuat.

## <a name="failed-approvals-and-approval-sets"></a>Aprobări eșuate și seturi de aprobare
Vizualizarea **Aprobări eșuate** listează toate aprobările care necesită intervenția utilizatorului. Deschideți jurnalele de seturi de aprobare asociate pentru a identifica cauza eșecului.
Selectarea **Reîncercați** adaugă la numărul de durată de viață al setului de aprobare, mută setul de aprobare înapoi la o stare de **Procesare**, și încearcă să proceseze înregistrările rămase.

## <a name="configure-approval-sets"></a>Configurați seturi de aprobare

###  <a name="enable-the-approval-sets-feature"></a>Activați caracteristica Seturi de aprobare
Înainte de a activa funcția Seturi de aprobări, verificați dacă nu există aprobări în curs de procesare.

- Accesați pagina **Parametrii proiectului** și selectați **Controlul caracteristicilor** > **Activați aprobările moderne**.

### <a name="turn-off-the-approval-sets-feature"></a>Dezactivați caracteristica Seturi de aprobare
Înainte de a dezactiva funcția Seturi de aprobări, verificați dacă nu există aprobări în curs de procesare.

- Accesați pagina **Parametrii proiectului** și selectați **Controlul caracteristicilor** > **Dezactivați aprobările moderne**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurarea pragului asincron 
Când sunt create seturi de aprobare, procesarea se mută în fundal atunci când numărul selectat de înregistrări pentru aprobare depășește pragul indicat. Utilizați câmpul **Prag asincron** pentru a configura când procesarea aprobării ar trebui să fie executată sincron sau asincron.
Valorile valide sunt:

  - Zero: toate solicitările ar trebui procesate asincron. 
  - Numere mai mari decât zero: aprobările sunt procesate asincron numai atunci când numărul de aprobări trimise depășește această valoare.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
