---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 32, V3
description: Acest articol listează caracteristicile și remedierile disponibile în Project Service Automation Update Versiunea 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 5124137c24da9b579ee1365524d66d9135b2d420
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912899"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Ce este nou sau schimbat în Project Service Automation versiunea actualizată 32, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Microsoft Dynamics 365 Project Service Automation. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Este compatibil cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați pagina de soluții online din Centrul de administrare pentru Dynamics 365 și instalați actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și remedierile care sunt noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 32. Această versiune are un număr de versiune V3.10.53.108 și este, în general, disponibilă prin auto-actualizare în iunie 2021.

## <a name="update-release-32"></a>Lansarea de actualizări 32

### <a name="bug-fixes"></a>Remedieri de erori

#### <a name="general"></a>General

- Atunci când o actualizare majoră eșuează, numai punctele principale de intrare ale aplicației ar trebui blocate, pentru a se asigura că entitățile partajate sunt încă accesibile.

#### <a name="time-and-expense"></a>Timp și cheltuială

S-au remediat următoarele probleme:

- **TimeEntriesImportFromResourceAssignment** nu menține timpii de început și de sfârșit ai porțiunii de sector a alocării resurselor.
- Când selectați **Deschideți intrarea** pe grila **Intrare în timp**, este posibil să vi se împiedice selectarea altor formulare.
- În timp ce importați alocări la intrări de timp, interogarea codului clientului poate genera o adresă URL lungă care nu reușește interogarea.
- În grila **Intrare de timp**, după ce o valoare este ștearsă dintr-o celulă, focalizarea nu rămâne în grilă.
- Butonul **Respinge** a fost eliminat din vizualizarea **Aprobări de procesare** pentru aprobări moderne.
- Stabilitatea și performanța aprobării în bloc a timpului sunt afectate de blocaje și de eșecul de a gestiona în mod adecvat personalizările care sunt legate de entitatea **Intrare de timp**.

#### <a name="project-planning"></a>Planificare de proiect

- O excepție de referință nulă este generată atunci când actualizați un proiect care are o valoare nulă în câmpul **Unitatea Contractantă**.
- **Reîmprospătați totalul proiectului** calculează incorect costul rămas și vânzările rămase pe un proiect.
- Calculele de tarifare redundante afectează performanțele legate de actualizările contururilor de alocare a resurselor.

#### <a name="resource-management"></a>Gestionarea de resurse

A fost rezolvată următoarea problemă:

- Când capacitatea calendaristică a unei resurse rezervabile este mai mare de 1, Project Service Automation recunoaște incorect capacitatea ca 0 (zero). Prin urmare, apare o buclă infinită în vizualizarea planificării.

#### <a name="sales"></a>Vânzări

S-au remediat următoarele probleme:

- Când se creează o linie de jurnal care are un tip de tranzacție particularizat, apare următoarea excepție de referință nulă: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Rolurile și categoriile care sunt inactivate înainte ca o ofertă să fie copiată nu ar trebui adăugate la rolurile și categoriile cu taxă ale ofertelor nou copiate.
- Data documentului și data contabilă nu sunt aliniate cu data de început care este furnizată pe un detaliu al liniei de factură care este creat direct pe o schiță de factură.
- Excepțiile de referință nulă sunt generate în scenarii care sunt legate de inactivarea rolurilor și categoriilor înainte de copierea unei cotații.
- Acțiunea **Actualizați prețurile** asupra **Proiecte** nu actualizează estimările cheltuielilor și estimările de materiale.
