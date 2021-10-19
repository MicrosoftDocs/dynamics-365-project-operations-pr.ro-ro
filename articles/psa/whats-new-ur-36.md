---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 36, V3
description: Acest subiect listează caracteristicile și remedierile disponibile în Actualizarea Microsoft Dynamics 365 Project Service Automation, versiunea 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606806"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation, versiunea actualizată 36, V3. Această versiune are un număr de V3.10.57.152 și este, în general, disponibilă printr-o auto-actualizare în octombrie 2021.

## <a name="update-release-36"></a>Lansarea de actualizări 36

### <a name="bug-fixes"></a>Remedieri de erori

S-au remediat următoarele probleme.

**General**
- Numele câmpului **Șablon implicit pentru ora de lucru** este tradus incorect pe pagina **Parametrii proiectului**.
- Inserturile Async nu gestionează corect excepțiile legate de **SharedVariableService**.

**Timp și cheltuială**
- Când lipsesc liniile jurnalului sau utilizatorul nu are privilegiile corecte pentru a citi liniile jurnalului, apare o eroare incorectă atunci când aprobările de proiect sunt anulate.
- Utilizatorii nu pot anula o aprobare atunci când o înregistrare de cheltuială sau de timp are mai mult de o aprobare de proiect asociată.
- **Absența** și **Concediu de odihnă** sunt traduse incorect pentru limba chineză într-o căutare pe pagina **Intrare în timp** de creare rapidă.

**Gestionarea resurselor**
- Utilizatorul nu poate căuta resurse în **Asistent de planificare** când modul de vizualizare este setat la **Zi**, **Săptămână**, sau **Lună**.
- Resurselor generice li se permite incorect să aibă nume de poziții goale. 
- Închiderea unui contract ca pierdut nu anulează rezervările viitoare.

**Vânzări**
- Atunci când un mediu are un volum mare de produse, performanța se degradează în grila **Estimarea materialelor**.
- La crearea unui proiect dintr-un șablon, moneda proiectului nu este implicită la unitatea contractantă a managerului de proiect respectiv.
- Sumele reale nu se potrivesc întotdeauna cu ceea ce se reflectă în proiectul datorat, sau sumele devin negative în scenarii de rechemare specifice.
- O eroare apare atunci când asociați un proiect creat din șablonul de proiect la o linie de contract.
- Utilizatorii pot șterge o linie de contract cu etapele de referință, **Gata de facturare** și **Factură creată**. Acest lucru nu ar trebui permis.
- Atunci când estimările sunt importate dintr-un proiect, taxa de detaliere a liniei de ofertă este setată incorect atunci când facturarea bazată pe sarcini este activată pentru linia de ofertă.
- Când adăugați o etapă de facturare cu preț fix, aceasta nu se reflectă în subgrila de referință până când pagina nu este actualizată.
- O excepție de referință nulă este generată atunci când creați un contract de proiect cu un nume de ofertă care este nul.
- Sarcinile în modul manual în care moneda proiectului este diferită de moneda resursei determină estimări incorecte ale prețului.
- Utilizatorii nu își pot aminti o tranzacție care a fost corectată cu succes printr-o factură corectivă.
- Categoriile de tranzacții dezactivate apar în grila **Estimări de cheltuieli**.



