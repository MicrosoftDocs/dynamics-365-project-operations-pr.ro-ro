---
title: Ce este nou sau schimbat în Project Service Automation versiunea actualizată 17, V3
description: Acest articol listează caracteristicile și remedierile disponibile în Project Service Automation Update Versiunea 17, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915705"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, versiunea actualizată 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Suntem încântați să anunțăm cea mai recentă actualizare pentru aplicația Project Service Automation pentru Dynamics 365. Această versiune include câteva îmbunătățiri importante ale calității, performanței și utilizabilității.  Această versiune este compatibilă cu Dynamics 365 9.x. Pentru a actualiza această versiune, accesați Centrul de administrare pentru Dynamics 365 online, pagina cu soluții pentru a instala actualizarea. Pentru informații suplimentare, consultați: [Instalarea, actualizarea sau eliminarea unei soluții preferate](/power-platform/admin/install-remove-preferred-solution).

Acest articol enumeră caracteristicile și remedierile care sunt noi sau modificate pentru PSA V3, Actualizare Versiunea 17. Această versiune are un număr de V3.10.6.34 și este, în general, disponibilă printr-o auto-actualizare în martie 2020.


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
