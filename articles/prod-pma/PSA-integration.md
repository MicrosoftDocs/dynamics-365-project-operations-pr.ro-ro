---
title: Prezentare generală Project Service Automation
description: Acest articol oferă informații despre Dynamics 365 Project Service Automation la soluția de integrare Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96fdb31b7b1d4f33cb565cf902039f72a3f90fd7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929597"
---
# <a name="project-service-automation-overview"></a>Prezentare generală Project Service Automation

[!include[banner](../includes/banner.md)]


Soluția de integrare Project Service Automation to Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțe din Dynamics 365 Finance și Dynamics 365 Project Service Automation prin Common Data Service. Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de proiecte, contracte de proiect, linii de contracte de proiect, repere de linii de contracte de proiect, sarcini de proiect, categorii de tranzacții de cheltuieli, estimări de oră și estimări de cheltuieli de la Project Service Automation până la finanțe.

> [!NOTE]
> - Dacă utilizați versiunea 7.3.0, trebuie să instalați KB 4074835. Veți putea apoi să integrați proiecte cu preț fix.
> - Dacă utilizați versiunea 7.3.0 și aduceți tranzacții cu taxe de la Project Service Automation, trebuie să instalați KB 4345320 pentru a include aceste taxe în factura proiectului.
> - Dacă utilizați versiunea 8.0, veți putea utiliza integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității.
> - Dacă utilizați versiunea 8.0.1 sau o versiune ulterioară, veți putea sincroniza datele reale.

Înainte de a putea integra Project Service Automation Finance, trebuie să configurați parametrii de integrare Project Service Automation. Pentru informații suplimentare, consultați [Parametri de integrare Project Service Automation](PSA-parameters.md).

Această soluție de integrare permite sincronizarea directă în următoarele scenarii:

- Mențineți contractele de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.
- Creați proiecte în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.
- Mențineți liniile de contract de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.
- Mențineți jaloanele de linii de contract de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.
- Mențineți sarcinile de proiect în Project Service Automation și sincronizați-le direct de la Project Service Automation la Finance.
- Mențineți categoriile de tranzacții de cheltuieli în Finance și sincronizați-le direct din Finance la Project Service Automation.
- Creați estimări orare de proiect în Project Service Automation și sincronizați-le direct din Project Service Automation în Finance.
- Creați estimări de cheltuieli de proiect în Project Service Automation și sincronizați-le direct din Project Service Automation în Finance.
- Creați durata proiectului, cheltuielile și taxele reale în Project Service Automation și creați tranzacții de proiect în jurnalul de integrare Project Service Automation, astfel încât să poată fi postate în Finanțe.

## <a name="data-synchronization"></a>Sincronizarea datelor

Următoarea ilustrație arată cum sunt sincronizate datele ca parte a integrării dintre Project Service Automation și Finance.

> [!NOTE]
> Nu toate șabloanele sunt disponibile în prezent. Șabloanele vor fi lansate pe măsură ce sunt completate.

[![Integrarea Project Service Automation cu Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Cerințe de sistem pentru Finance

Pentru a utiliza soluția de integrare Project Service Automation to Finance, trebuie să instalați Enterprise edition 7.3 cu platforma de actualizare 12 sau mai recentă.

## <a name="system-requirements-for-project-service-automation"></a>Cerințe de sistem pentru Project Service Automation

Pentru a utiliza soluția de integrare Project Service Automation to Finance, trebuie să instalați următoarele componente:

- Dynamics 365 Project Service Automation versiunea 9.0.0.0 sau ulterioară
- Soluția de perspectivă către numerar pentru Dynamics 365 Sales, versiunea 1.14.0.0 (v14) sau o versiune ulterioară
- Soluție Project Automation Service to Finance pentru Dynamics 365 Project Service Automation versiunea 1.0.0.0 sau o versiune ulterioară

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instalați soluția de integrare Project Service Automation to Finance în instanța dvs. Project Service Automation

Descărcați soluția de integrare Project Service Automation to Finance [Centrul de descărcare Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) și urmați instrucțiunile incluse în soluție.


[!INCLUDE[footer-include](../includes/footer-banner.md)]