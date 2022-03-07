---
title: Sincronizați categoriile de cheltuieli ale proiectului între Finance and Operations și Project Service Automation
description: Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza categoriile de cheltuieli ale proiectului între Microsoft Dynamics 365 Finance și Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 52c79f8b641d4b2df3b30964331633f2487402f8f8d229b540f9544c0f848557
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001131"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronizați categoriile de cheltuieli ale proiectului între Finance and Operations și Project Service Automation

[!include[banner](../includes/banner.md)]

Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza categoriile de cheltuieli ale proiectului între Dynamics 365 Finance și Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.
> - Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.
> - Dacă utilizați Enterprise edition 7.3.0, după ce instalați KB 4132657 și KB 4132660, veți putea utiliza șabloanele pentru a integra sarcinile proiectului, categoriile de tranzacții de cheltuieli, estimările orelor, estimările cheltuielilor și datele reale și pentru a configura blocarea funcționalității. Dacă trebuie să resetați distribuțiile contabile, vă recomandăm să instalați și KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Fluxul de date pentru Project Service Automation și Finance

Soluția de integrare Project Service Automation și Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance. Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de date despre categoriile de cheltuieli de tranzacție ale proiectului între Finance și Project Service Automation.

Când categoriile de cheltuieli ale proiectului sunt stăpânite în Finance, fluxul de integrare este mai întâi din Finance la Project Service Automation. ID-urile de integrare ale categoriilor de cheltuieli ale proiectului sunt apoi actualizate prin sincronizare de la Project Service Automation la Finance.

Când categoriile de cheltuieli ale proiectului sunt stăpânite în Project Service Automation, fluxul de integrare este mai întâi din Project Service Automation la Finance. Categoriile de proiect trebuie să fie deja configurate în Finance înainte de sincronizarea din Project Service Automation. Apoi sincronizați de la Finance înapoi la Project Service Automation și apoi iar de la Project Service Automation la Finance. În acest fel, garantați conectarea categoriilor și că nu sunt create duplicate.

> [!NOTE]
> De obicei, categoriile de cheltuieli ale proiectului sunt stăpânite în Finance. Cu toate acestea, dacă nu sunt, sau când categoriile de cheltuieli au fost deja create în Project Service Automation, trebuie mai întâi să sincronizați utilizând șablonul Categorii de tranzacții de cheltuieli ale proiectului (PSA la Fin și Ops). Apoi sincronizați folosind șablonul categorii de tranzacții de cheltuieli ale proiectului (Fin și Ops la PSA). Apoi, ar trebui să rulați sincronizarea de la Project Service Automation la Finance încă o dată.
>
> Dacă vă sincronizați mai întâi de la Project Service Automation, următoarele cerințe trebuie să fie îndeplinite în Finance înainte ca sincronizarea să fie executată:
>
> - Categoria partajată care se potrivește cu categoria de proiect care este configurată în Project Service Automation trebuie să existe și trebuie activată pentru **Proiect** și pentru **Cheltuieli**.
> - Pentru fiecare entitate juridică din Finance cu care trebuie integrată, trebuie să existe următoarele categorii de proiecte:
>
>     - **Categoria proiectului** există. 
>     - **Folosire în cheltuieli** este activat.
>     - **Activ în jurnal** este activat.
>     - **Tipul tranzacției** este setat la **Cheltuieli**.

Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.

[![Fluxul de date pentru integrarea Project Service Automation cu Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronizare categorii de cheltuieli ale proiectului între Finance și Project Service Automation

### <a name="template-and-task"></a>Șablon și sarcină

Pentru a accesa șablonul, în centrul de administrare Microsoft Power Apps, selectați **Proiecte**, apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.

Următorul șablon și sarcina de desfășurare sunt utilizate pentru a sincroniza categoriile cheltuielilor proiectului de la Finance la Project Service Automation:

- **Numele șablonului în Integrarea datelor:** categoriile de tranzacție ale cheltuielilor proiectului (Fin și Ops la PSA)
- **Numele sarcinii din proiect:** Sincronizați categoriile cu PSA

### <a name="entity-set"></a>Entitate setată

| Finanțe                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entitate de integrare pentru categorii | Categorii de tranzacții     |

### <a name="entity-flow"></a>Fluxul de entități

Categoriile cheltuielilor proiectului sunt gestionate în Finance și sunt sincronizate cu Project Service Automation ca și categorii de tranzacție.

### <a name="power-query"></a>Power Query

Când vă sincronizați cu Project Service Automation, trebuie să utilizați Microsoft Power Query pentru Excel pentru a seta tipul de facturare în categoria tranzacției. Șablonul categorii tranzacții de cheltuieli ale proiectului (Fin și Ops la PSA) oferă o coloană și o mapare implicite. Dacă vă creați propriul șablon, trebuie să adăugați o coloană condițională în Power Query. Urmați acești pași.

1. Faceți clic pe săgeată pentru a deschide maparea activității categoriilor de cheltuieli de proiect în șablonul Categorii de tranzacții de cheltuieli de proiect (Fin și Ops la PSA).
2. Faceți clic pe linkul **Interogare și filtrare avansate** pentru a deschide Power Query.
2. Selectați **Adăugare coloană condițională**.
3. Introduceți un nume pentru noua coloană, cum ar fi **BillingType**.
4. Introduceți următoarea condiție: **dacă CATEGORYID nu este egal cu nul atunci 19235001, altfel nul**.
5. Faceți clic pe **OK** din coloană.
6. Asigurați-vă că ați mapat această nouă coloană pe pagina de mapare.

Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Finance la Project Service Automation.

[![Maparea categoriei de cheltuieli ale proiectului la șablonul Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronizare categorii de cheltuieli ale proiectului între Project Service Automation și Finance

### <a name="template-and-task"></a>Șablon și sarcină

Următorul șablon și sarcina de desfășurare sunt utilizate pentru a sincroniza categoriile cheltuielilor proiectului de la Project Service Automation la Finance:

- **Numele șablonului în Integrarea datelor:** categoriile de tranzacție ale cheltuielilor proiectului (PSA la Fin și Ops)
- **Numele sarcinii din proiect:** Sincronizați categoriile cu Fin Ops

### <a name="entity-set"></a>Entitate setată

| Project Service Automation | Finanțe                           |
|----------------------------|-----------------------------------|
| Categorii de tranzacții     | Entitate de integrare pentru categorii |

### <a name="entity-flow"></a>Fluxul de entități

Categoriile cheltuielilor proiectului sunt gestionate în Finance și sunt sincronizate cu Project Service Automation ca și categorii de tranzacție. Sincronizarea înapoi la actualizările Finance pentru categoriile proiectului din Finance cu ID de integrare de la Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor.

> [!NOTE]
> Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.

[![Maparea șablonului Project Service Automation la Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]