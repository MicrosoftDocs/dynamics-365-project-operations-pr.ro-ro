---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 17, V3
description: Acest subiect listează caracteristicile și corecțiile care sunt disponibile în Project Service Automation V3, versiunea actualizată 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: ba2bc9da1c6e7e2e2628980878f9201b1c732cc03f791f5259bbbd0ee279b31b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006621"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, versiunea actualizată 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.  Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest subiect listează caracteristicile și corecțiile care sunt noi sau modificate pentru PSA V3, Update Release 17. Această versiune are un număr de V3.10.6.34 și este, în general, disponibilă printr-o auto-actualizare în martie 2020.


## <a name="update-release-17"></a>Lansarea de actualizări 17

### <a name="bug-fixes"></a>Remedieri de erori

**General**

- Soluționat: Actualizați Project Service Automation pentru a implementa licențele pentru membrii echipei (Hub-ul de resurse al proiectului va include metadatele planului de servicii pentru membrii echipei 3.x)
 
**Timp și cheltuială**

- Soluționat: nu este posibilă modificarea unei estimări a cheltuielilor de la un preț diferit de zero la zero (0). Modificarea este ignorată.

**Gestionare de proiect**

- Soluționat: S-a adăugat o verificare a valorilor nule pe numele poziției unui membru al echipei.
- Soluționat: câmpul **msdyn_userresourceid** din entitatea **msdyn_resourceassignment** a fost perimat.
- Soluționat: Upgrade-ul de la 2.x la 3.x gestionează acum contururile de efort goale în atribuirile de activități.

**Sales**

- Soluționat: **Invoice.PreValidateInvoiceUpdate** gestionează acum scenariul realocării proprietarilor de înregistrări în mod corespunzător.
- Soluționat: Când clasa de tranzacție este **Timp**, **UnitGroup** este needitabil pentru toate entitățile inclusiv, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, și **ContractLineDetails**. În orice caz, **Unitate** este needitabil doar pentru **JournalLine** și **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]