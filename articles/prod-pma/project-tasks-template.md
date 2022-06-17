---
title: Sincronizați sarcinile de proiect direct de la Project Service Automation la Finanțe și Operațiuni
description: Acest articol descrie șablonul și sarcina de bază care sunt utilizate pentru a sincroniza sarcinile de proiect direct din Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7b8ba77bbb08052952a8a557bb71300652dca3b2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931161"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizați sarcinile de proiect direct de la Project Service Automation la Finanțe și Operațiuni

[!include[banner](../includes/banner.md)]

Acest articol descrie șablonul și sarcina de bază care sunt utilizate pentru a sincroniza sarcinile de proiect direct din Dynamics 365 Project Service Automation la Dynamics 365 Finance.

> [!NOTE]
> - Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.
> - Dacă utilizați Enterprise edition 7.3.0, după ce instalați KB 4132657 și KB 4132660, veți putea utiliza șabloanele pentru a integra sarcinile proiectului, categoriile de tranzacții de cheltuieli, estimările orelor, estimările cheltuielilor și datele reale și pentru a configura blocarea funcționalității. Dacă trebuie să resetați distribuțiile contabile, vă recomandăm să instalați și KB 4131710.
> - Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxul de date pentru Project Service Automation la Finanțe

Soluția de integrare Project Service Automation la Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance. Șablonul de integrare disponibil cu funcția de integrare a datelor permite fluxul de date despre sarcinile proiectului de la Project Service Automation la Finance.

Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.

[![Fluxul de date pentru integrarea Project Service Automation cu Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Șablon și sarcină

Pentru a accesa șablonul, în centrul de administrare Microsoft Power Apps, selectați **Proiecte**, apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.

Următorul șablon și sarcina de desfășurare sunt utilizate pentru a sincroniza sarcini de proiect de la Project Service Automation la Finance:

- **Numele șablonului în Integrarea datelor:** Sarcini de proiect (PSA la Fin și Ops)
- **Numele sarcinii din proiect:** Sarcini de proiect

Înainte de a putea avea loc sincronizarea sarcinilor proiectului, trebuie să sincronizați contractele și proiectele proiectului.

## <a name="entity-set"></a>Entitate setată

| Project Service Automation | Finanțe                             |
|----------------------------|-------------------------------------|
| Activități de proiect              | Entitate de integrare pentru sarcina proiectului |

## <a name="entity-flow"></a>Fluxul de entități

Sarcinile proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu Finanțarea ca activități de proiect.

## <a name="prerequisites-and-mapping-setup"></a>Cerințe preliminare și configurare a mapării

Înainte de a putea avea loc sincronizarea sarcinilor proiectului, trebuie să sincronizați contractele și proiectele proiectului.

## <a name="power-query"></a>Power Query

Trebuie să utilizați Microsoft Power Query pentru ca Excel să filtreze datele dacă această condiție este îndeplinită:

- Aveți înregistrări specifice resurselor într-o sarcină de proiect.

Dacă trebuie să utilizați Power Query, urmați acest ghid:

- Șablonul Sarcini de proiect (PSA la Fin și Ops) are un filtru implicit care exclude înregistrările specifice resurselor dintr-o sarcină de proiect prin setarea filtrului pe **IsLineTask** la **Fals**. Dacă vă creați propriul șablon, trebuie să adăugați acest filtru.

## <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.

[![Maparea șabloanelor.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]