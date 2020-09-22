---
title: Ce este nou sau modificat în Project Service Automation versiunea 3.x etapa 1 2020
description: Acest subiect oferă informații despre ceea ce este nou și schimbat în Project Service Automation versiunea 3 etapa 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754741"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Ce este nou sau modificat în Project Service Automation versiunea 3 etapa 1 2020
Subiectul subliniază considerentele cheie de actualizare atunci când treceți la cea mai recentă versiune a Project Service Automation (PSA) versiunea 3.x versiunea 1 2020.

## <a name="time-entry"></a>Intrare de timp
Experiența de intrare în timp a fost extinsă pentru a oferi capabilități pentru prelungirea intrării timpului în mai multe scenarii de clienți. Aceasta include capacitatea de a adăuga tipuri de intrare, care conduc acum un comportament specific bazat pe numele schemei de câmp **Setări de intrare de timp**, afișat ca **Sursa timpului**.

### <a name="upgrade-consideration"></a>Considerent legat de upgrade
Pentru a sprijini această funcționalitate, rolurile din cadrul PSA au fost actualizate pentru a include noi privilegii. Aceste privilegii acordă acces de citire la noua entitate, **Setări de intrare de timp**.

Utilizatorilor care necesită capacitatea de a înregistra timp ar trebui să li se acorde rolul de utilizator **Utilizator de intrare în timp** pe lângă rolurile existente. Acest rol include noua funcționalitate și asigură că intrarea în timp va continua să funcționeze.

### <a name="currently-extended-time-entry-changes"></a>Modificările de intrare de timp extinse în prezent
Pentru a reduce impactul asupra utilizatorilor actuali de intrare în timp, această modificare a rolului este singura cerință esențială necesară pentru a continua utilizarea intrării în timp. Dacă ați creat vizualizări personalizate sau experiențe de intrare în timp separate, trebuie să setați câmpurile **Setare intrare timp** la valoarea corectă PSA.
