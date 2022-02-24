---
title: Performanța planificării resurselor proiectului
description: Acest subiect oferă informații despre cum să îmbunătățim performanța planificării resurselor pentru un număr mare de proiecte.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082779"
---
# <a name="project-resource-scheduling-performance"></a>Performanța planificării resurselor proiectului

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Probleme de performanță legate de programarea resurselor pot apărea atunci când numărul proiectelor ajunge la mii. Pentru a îmbunătăți performanța de planificare a resurselor, este disponibilă o caracteristică care permite utilizatorilor să reducă timpul necesar lansării formularului de disponibilitate a resurselor. În mod specific, acest lucru elimină procesul de sincronizare a acumulării capacității resurselor și utilizează tabelul **ResProjectResource** tabel pentru a accelera căutarea resurselor. Rețineți că tabelul **ResRollup** nu va mai fi folosit.

> [!IMPORTANT]
> Dacă există o dependență fie de procesul de sincronizare de acumulare a capacității resurselor, sau tableul **ResProjectResource**, nu utilizați această caracteristică.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Activați îmbunătățirea performanței planificării resurselor
Pentru a activa îmbunătățirea performanței planificării resurselor, parcurgeți pașii următori.

1. Accesați **Managementul caracteristicilor** > **Toate**, și în lista de caracteristici, găsiți **Activați caracteristica de îmbunătățire a performanței de planificare a resurselor proiectului**.
2. Selectați **Activați acum**.

> [!NOTE]
> Dacă nu puteți găsi caracteristica în listă, selectați **Verificați actualizări** pentru a reîmprospăta lista.

3. Reîmprospătați browserul, apoi accesați **Management de proiect și contabilitate** > **Periodic** > **Resursele proiectului** > **Sincronizați capacitatea calendarelor de resurse în toate companiile**.
4. Setați **Eliminați înregistrările de capacitate existente** la **Da** pentru a elimina datele anterioare. Dacă doriți să generați date incrementale, setați-le la **Nu**.
5. În câmpul **Codul perioadei**, selectați perioada în care ar trebui generate datele. Dacă selectați un cod de perioadă, nu este necesară definirea unei date de începere și de încheiere.
6. Dacă lăsați câmpul **Codul perioadei** necompletat, selectați anumite date de început și sfârșit pentru a genera date.
7. Selectați **OK**.

 > [!NOTE]
 > Aceasta va distribui date generale către tabelul **ResCalendarCapacity** pentru toate companiile din mediul dvs., astfel încât jobul lot trebuie executat doar într-o singură persoană juridică. Datele din această operațiune de lot sunt necesare pentru a calcula capacitatea resurselor prin calendarul asociat.

8. Accesați **Management de proiect și contabilitate** > **Periodic** > **Resursele proiectului** > **Populați resursele proiectului în toate companiile** și apoi selectați **OK**. Acesta este scriptul de actualizare a datelor pentru date generale din tabelele **ResProjectResource**, **ResCalendarDateTimeRange**, și **ResEffectiveDateTimeRange**. Valori pentru câmpul **PSAPRojSchedRole.RootActivity** sunt de asemenea actualizate. Dacă acest lucru nu este executat, veți primi un avertisment atunci când încercați să executați operațiuni de planificare a resurselor.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Dezactivați îmbunătățirea performanței planificării resurselor

1. Accesați **Managementul caracteristicilor** > **Toate**, și căutați **Activați caracteristica de îmbunătățire a performanței de planificare a resurselor proiectului**.
2. Selectați caracteristica, apoi selectați butonul **Dezactivare**.
3. Reîmprospătați browserul.
4. Accesați **Management de proiect și contabilitate** > **Periodic** > **Sincronizare de capacitate** > **Cumulare sincronizare resurse de capacitate**.
5. Pe pagina **Sincronizare de acumulare a capacității** configurați **Eliminați înregistrările de capacitate existente** la **Da** pentru a elimina datele anterioare. Dacă doriți să generați date incrementale, configurați la **Nu**.
6. În câmpul **Codul perioadei**, selectați perioada în care ar trebui generate datele. Dacă selectați un cod de perioadă, nu este necesară definirea unei date de începere și de încheiere.
7. Dacă lăsați câmpul **Codul perioadei** necompletat, selectați anumite date de început și sfârșit pentru a genera date.
8. Selectați **OK**.

> [!NOTE]
> Aceasta va distribui date generale către tabelul **ResRollup** pentru toate companiile din mediul dvs., astfel încât operațiunea de lot trebuie executată doar într-o singură persoană juridică. Această operațiune de lot este necesară pentru toate vizualizările **Disponibilitatea resurselor**. Dacă această operațiune de lot nu este rulată, **ResRollup** datele vor fi generate din mers, ceea ce poate dura timp.
