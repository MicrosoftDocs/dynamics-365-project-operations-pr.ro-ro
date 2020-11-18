---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 18, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082750"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, versiunea actualizată 18, V3

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru Project Service Automation V3, versiunea actualizată 18. Această versiune are un număr de versiune V3.10.8.12 și este disponibil în general printr-o autoactualizare în aprilie 2020.

## <a name="update-release-18"></a>Lansarea de actualizări 18

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

- Remediat: fluxurile **Retragere** . **Cerere** și **Anulare aprobare** declanșează excepții cu mesaje de eroare neclare.
- Remediat: când **Anulare aprobare** eșuează pentru o cheltuială, nu este declanșată o eroare de excepție relevantă.
- Remediat: grila de introducere a timpului gestionează în mod incorect zilele nelucrătoare în Australia, după trecerea la ora de vară (DST) în octombrie.
- Remediat: o logică implicită incorectă împiedică remiterea cheltuielilor.
- Remediat: când aprobarea intrării de timp nu reușește, aprobarea rămâne într-o stare de **Asteptare**.
- Remediat: erori SQL la aprobările în bloc (blocare deadlock/expirare).
- Remediat: probleme semnificative de performanță în experiența utilizatorului, cauzate de actualizarea membrilor echipei în timp ce aprobă înregistrările de timp.

**Gestionare de proiect**

- Remediat: notificarea pentru fusul orar a fost mutată din vizualizarea **Reconciliere** la formularul principal **Proiect**.
- Remediat: șablonul Calendar nu este ales implicit corect atunci când se deschide un nou formular de proiect.
- Remediat: pentru browserele bazate pe Chromium, utilizatorii nu pot selecta cu ușurință sarcinile predecesoare pentru a le șterge.
- Remediat: crearea sau copierea **Proiect din șablon gol** preia atribuiri fără legătură.
- Remediat: în cazuri specifice Microsoft Edge, crearea unei noi atribuiri din grila de sarcini duce la crearea de înregistrări duplicate.
- Remediat: în modul manual, utilizatorii nu pot actualiza datele de începere a activității pentru a fi mai târzii decât data salvată curentă.

**Gestionarea resurselor**

- Remediat: vizualizarea **Reconciliere** rândul subtotal calculează incorect variația rezervărilor după extinderea rezervărilor.
- Remediat: vizualizarea **Reconciliere** afișează incorect atribuirile resurselor atunci când resursa rezervabilă are un calendar care nu se potrivește cu calendarul proiectului.

**Sales**

- Remediat: când intrările de timp sunt reaprobate ( **Aprobare > Anulare >** aprobați din nou), este creat un duplicat real netarifabil.