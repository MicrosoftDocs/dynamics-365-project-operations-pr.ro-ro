---
title: Seturi de aprobare
description: Acest articol explică cum să lucrați cu seturi de aprobare, solicitări și subseturile acelor operațiuni.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524932"
---
# <a name="approval-sets"></a>Seturi de aprobare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Aprobarea stabilește cererile de aprobare de grup împreună în subseturi mai mici de operațiuni. Această grupare permite procesarea aprobărilor după proiect, într-o ordine specifică, și permite reîncercarea și secvențierea. Gruparea cererilor de aprobare îmbunătățește fiabilitatea și trasabilitatea procesării aprobării pentru volume mari de aprobări.

Seturile de aprobare indică starea generală de procesare a înregistrărilor lor conexe. Când o înregistrare de aprobare este procesată utilizând un set de aprobare, înregistrarea se mută din **Trimis** în **Aprobat** și nu mai este legată de setul de aprobare. Dacă o înregistrare eșuează atunci când este trimisă spre aprobare, înregistrarea rămâne în starea de **Trimis** iar setul de aprobare este marcat ca eșuat. Setul de aprobare înregistrează mesajul de eroare al eșecului.

## <a name="processing-approvals-and-approval-sets"></a>Procesarea aprobărilor și seturilor de aprobare
Aprobările aflate în coadă pentru procesare sunt vizibile în vizualizarea **Procesarea aprobărilor**. Sistemul procesează toate înregistrările asincron de mai multe ori, inclusiv reîncercarea unei aprobări dacă încercările anterioare au eșuat.

Câmpul **Durata de viață a setului de aprobare** înregistrează numărul de încercări rămase de procesare a setului înainte ca acesta să fie marcat ca eșuat.

Seturile de aprobare sunt procesate prin activarea periodică pe baza a **Cloud Flow** numit **Serviciu de proiect - Programează în mod recurent seturi de aprobare a proiectelor**. Aceasta se găsește în **Soluţie** numit **Operațiuni de proiect**. 

Asigurați-vă că fluxul este activat parcurgând următorii pași.

1. În calitate de administrator, conectați-vă la [flow.microsoft.com](https://powerautomate.microsoft.com).
2. În colțul din dreapta sus, comutați la mediul pentru care utilizați Dynamics 365 Project Operations.
3. Selectați **Soluții** pentru a enumera soluțiile care sunt instalate în mediu.
4. În lista de soluții, selectați **Operațiuni de proiect**.
5. Schimbați filtrul de la **Toate** la **Cloud Flows**.
6. Verificați că **Serviciu de proiect – Programează în mod recurent seturi de aprobare a proiectelor** fluxul este setat la **Pe**. Dacă nu este, selectați fluxul, apoi selectați **Porniți**.
7. Verificați dacă procesarea are loc la fiecare cinci minute, examinând **Joburi de sistem** lista în **Setări** zona din cadrul operațiunilor dvs. de proiect Dataverse mediu inconjurator.

## <a name="failed-approvals-and-approval-sets"></a>Aprobări eșuate și seturi de aprobare
Vizualizarea **Aprobări nereușite** listează toate aprobările care necesită intervenția utilizatorului. Deschideți jurnalele de seturi de aprobare asociate pentru a identifica cauza eșecului.
Selectarea **Reîncercați** adaugă la numărul de durată de viață al setului de aprobare, mută setul de aprobare înapoi la o stare de **Procesare**, și încearcă să proceseze înregistrările rămase.

## <a name="configure-approval-sets"></a>Configurați seturi de aprobare

### <a name="enable-the-approval-sets-feature"></a>Activați caracteristica Seturi de aprobare
Înainte de a activa funcția Seturi de aprobări, verificați dacă nu există aprobări în curs de procesare. După ce această funcție este activată, nu poate fi dezactivată.

- Accesați pagina **Parametrii proiectului** și selectați **Controlul caracteristicilor** > **Activați aprobările moderne**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurarea pragului asincron 
Când sunt create seturi de aprobare, procesarea se mută în fundal atunci când numărul selectat de înregistrări pentru aprobare depășește pragul indicat. Utilizați câmpul **Prag asincron** pentru a configura când procesarea aprobării ar trebui să fie executată sincron sau asincron. Selectați una dintre următoarele valori:

  - Zero: toate solicitările ar trebui procesate asincron. 
  - Numere mai mari decât zero: aprobările sunt procesate asincron numai atunci când numărul de aprobări trimise depășește această valoare.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
