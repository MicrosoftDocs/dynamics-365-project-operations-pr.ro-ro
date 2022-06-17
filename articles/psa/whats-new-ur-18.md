---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 18, V3
description: Acest articol enumeră caracteristicile și remedierile disponibile în Project Service Automation Update Versiunea 18, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918879"
---
# <a name="project-service-automation-update-release-18-v3"></a>Project Service Automation, versiunea actualizată 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și remedierile care sunt noi sau modificate pentru Project Service Automation V3, Actualizare versiunea 18. Această versiune are un număr de versiune V3.10.8.12 și este disponibil în general printr-o autoactualizare în aprilie 2020.

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

- Remediat: când intrările de timp sunt reaprobate (**Aprobare > Anulare >** aprobați din nou), este creat un duplicat real netarifabil.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
