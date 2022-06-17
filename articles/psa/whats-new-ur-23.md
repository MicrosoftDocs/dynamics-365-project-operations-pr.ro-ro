---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 23, V3
description: Acest articol enumeră caracteristicile și remedierile disponibile în Project Service Automation Update Versiunea 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913044"
---
# <a name="project-service-automation-update-release-23-v3"></a>Project Service Automation, versiunea actualizată 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității. Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365, pagina de soluții online pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol listează caracteristicile și remedierile care sunt noi sau modificate pentru Project Service Automation V3, Actualizare Versiunea 23. Această versiune are un număr de versiune V 3.10.34.30 și este, în general, disponibilă printr-o auto-actualizare în august 2020.

## <a name="update-release-23"></a>Lansarea de actualizări 23

### <a name="bug-fixes"></a>Remedieri de erori

**Timp și cheltuială**

S-au remediat următoarele probleme:
- Gestionați cazul marginal în **Ștergere membru echipă proiect** pentru a oferi o excepție semnificativă.
- Importul de activități are ca rezultat un ecran gol de eliminare.

**Gestionarea resurselor**

S-au remediat următoarele probleme:

- **Cardul de resurse al grilei de utilizare a resurselor** afișează date incorecte atunci când scala de timp este mai mare de cinci zile.
- Când clienții creează o resursă rezervabilă, insertul nu reușește să adauge automat resursa la un grup Microsoft Office 365.
- Vizualizarea **Reconciliere** afișează incorect contururile manuale în vizualizarea **Săptămână** sau **Lună**.

**Gestionare de proiect**

S-au remediat următoarele probleme:

- Un număr excesiv de entități **RetrieveMultiple pentru usersettings** cauzează performanțe degradate pentru aprobările de proiect și alte operațiuni.
- Căutarea resurselor grilă **Planificarea activităților** este limitată pentru a afișa doar până la cinci membri ai echipei din echipa proiectului. 
- Căutarea resurselor grilă **Planificarea activităților** nu filtrează resursele inactive.
- Modul manual nu funcționează așa cum era de așteptat în structura de repartizare a lucrărilor de planificare a proiectului.
- Grila **Planificarea activităților** arată **Categorii de tranzacții inactive**.
- Grila **Alocarea resurselor** rotunjește incorect atunci când o activitate are mai multe atribuții.
- Valorile de rotunjire sunt diferite între costul planificat și costul real pentru o singură activitate.

**Sales**

S-au remediat următoarele probleme:

- **Preluați toate categoriile de tranzacții** la dublu clic creează mai multe linii.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
