---
title: Sincronizați estimările proiectului direct din Project Service Automation în Finance and Operations
description: Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza estimările orare ale proiectului și estimările cheltuielilor proiectului direct de la Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082924"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizați estimările proiectului direct din Project Service Automation în Finance and Operations

[!include[banner](../includes/banner.md)]

Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza estimările orare ale proiectului și estimările cheltuielilor proiectului direct de la Dynamics 365 Project Service Automation la Dynamics 365 Finance.

> [!NOTE]
> - Integrarea sarcinilor proiectului, categoriile tranzacțiilor de cheltuieli, estimările orelor, estimările cheltuielilor și blocarea funcționalității sunt disponibile în versiunea 8.0.
> - Integrarea datelor reale este disponibilă din cu versiunea 8.0.1 sau mai nouă.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxul de date pentru Project Service Automation la Finanțe

Soluția de integrare Project Service Automation la Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance. Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de date despre estimările orare ale proiectului și estimările cheltuielilor proiectului de la Project Service Automation la Finance.

Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.

[![Fluxul de date pentru integrarea Project Service Automation cu Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimări orare de proiect

### <a name="template-and-tasks"></a>Șabloane și sarcini

Pentru a accesa șabloanele disponibile, în centrul de administrare Microsoft Power Apps, selectați **Proiecte** , apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.

Următorul șablon și sarcinile de desfășurare sunt utilizate pentru a sincroniza estimările orare ale proiectului de la Project Service Automation la Finance:

- **Numele șablonului în Integrarea datelor:** estimările orare ale proiectului (PSA la Fin și Ops)
- **Numele sarcinilor din proiect:**

    - Relațiile de tranzacție
    - Estimări de cheltuieli

### <a name="entity-set"></a>Entitate setată

| Project Service Automation | Finanțe                                       |
|----------------------------|-----------------------------------------------|
| Activitățile proiectului              | Entitate de integrare pentru estimările orare ale proiectului |

### <a name="entity-flow"></a>Fluxul de entități

Estimările orare ale proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu Finanțarea ca prognozele orare de proiect.

### <a name="prerequisites"></a>Cerințe preliminare

Înainte de a putea avea loc sincronizarea estimărilor orare ale proiectului, trebuie să sincronizați proiectele, sarcinile proiectului și categoriile de tranzacții de cheltuieli ale proiectului.

### <a name="power-query"></a>Power Query

În șablonul estimărilor orare ale proiectului, trebuie să utilizați Microsoft Power Query pentru Excel pentru a finaliza aceste sarcini:

- Setați ID-ul implicit al modelului de prognoză care va fi utilizat atunci când integrarea creează prognoze orare noi.
- Filtrează orice înregistrare specifică resursei în sarcina care va eșua integrarea în prognozele orare.
- Filtrează orice rânduri de categorii de tranzacții goale. Nerespectarea completării acestei sarcini poate duce la prognoze orare incorecte.

#### <a name="set-the-default-forecast-model-id"></a>Setați ID-ul modelului de prognoză implicit

Pentru a actualiza ID-ul de model de prognoză implicit în șablon, faceți clic pe săgeata **Mapare** pentru a deschide maparea. Apoi selectați linkul **Interogare și filtrare avansate**.

- Dacă utilizați șablonul implicit estimări orare ale proiectului (PSA la Fin și Ops), selectați **Condiția inserată** în lista de **Pași aplicați**. În intrarea **Funcție** , înlocuiți **O\_forecast** cu numele de ID model prognoză care ar trebui folosit cu integrarea. Șablonul implicit are un ID de model de prognoză din datele demonstrative.
- Când creați un șablon nou, trebuie să adăugați această coloană. În Power Query, selectați **Adăugare coloană condițională** , și introduceți un nume pentru coloana nouă, cum ar fi **ModelID**. Introduceți condiția pentru coloană, unde, dacă activitatea Project nu este nulă, atunci \<enter the forecast model ID\>; altfel nul.

#### <a name="filter-out-resource-specific-records"></a>Filtrați înregistrările specifice resurselor

Șablonul estimărilor orare ale proiectului (PSA to Fin și Ops) are un filtru implicit care elimină orice înregistrare specifică resursei. Dacă vă creați propriul șablon, trebuie să adăugați acest filtru. Selectați linkul **Interogare și filtrare avansate** pentru a filtra pe coloana **msdyn\_islinetask** astfel încât numai înregistrările **False** să fie incluse.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrați rândurile de categorii de tranzacții goale

Trebuie să adăugați un filtru pentru a elimina toate rândurile care au categorii de tranzacții goale. Această sarcină este necesară, indiferent dacă utilizați șablonul implicit sau creați propriul șablon. Acest filtru elimină orice rânduri rezumative din Project Service Automation care ar putea determina prognozele orare în Finanțe să fie incorecte. Selectați linkul **Interogare și filtrare avansate** pentru a filtra înregistrările nule în coloana **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

Următoarea ilustrație prezintă un exemplu de mapare a sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.

[![Activitate de mapare a șabloanelor în integrarea datelor](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimări de cheltuieli proiect

### <a name="template-and-tasks"></a>Șabloane și sarcini

Următorul șablon și sarcinile de desfășurare sunt utilizate pentru a sincroniza estimările cheltuielilor proiectului de la Project Service Automation la Finance:

- **Numele șablonului în Integrarea datelor:** estimările cheltuielilor proiectului (PSA la Fin și Ops)
- **Numele sarcinilor din proiect:**

    - Relațiile de tranzacție 
    - Estimări de cheltuieli

### <a name="entity-set"></a>Entitate setată

| Project Service Automation | Finanțe                                                  |
|----------------------------|----------------------------------------------------------|
| Conexiuni de tranzacție    | Entitate de integrare pentru relațiile de tranzacție ale proiectului |
| Linii estimate             | Entitate de integrare pentru estimările cheltuielilor proiectului         |

### <a name="entity-flow"></a>Fluxul de entități

Estimările cheltuielilor proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu Finanțarea ca prognozele cheltuielilor de proiect.

### <a name="prerequisites"></a>Cerințe preliminare

Înainte de a putea avea loc sincronizarea estimărilor cheltuielilor proiectului, trebuie să sincronizați proiectele, sarcinile proiectului și categoriile de tranzacții de cheltuieli ale proiectului.

### <a name="power-query"></a>Power Query

În șablonul de actualizare a estimărilor cheltuielilor proiectului, trebuie să utilizați Power Query pentru a finaliza următoarele sarcini:

- Filtrați pentru a include numai înregistrările de linie de estimări de cheltuieli.
- Setați ID-ul implicit al modelului de prognoză care va fi utilizat atunci când integrarea creează prognoze orare noi.
- Transformați tipurile de facturare.
- Transformați tipurile de tranzacții.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrați pentru a include numai liniile de estimări de cheltuieli

Șablonul de estimare a cheltuielilor proiectului (PSA la Fin și Ops) are un filtru implicit care include numai liniile de cheltuieli în integrare. Dacă vă creați propriul șablon, trebuie să adăugați acest filtru. Selectați sarcina **Relații de tranzacție** , apoi faceți clic pe săgeata **Mapare** pentru a deschide maparea. Selectați linkul **Interogare și filtrare avansate**. Filtrați coloana **msdyn\_transactiontype1** astfel încât să includă numai **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Setați ID-ul modelului de prognoză implicit

Pentru a actualiza ID-ul de model de prognoză implicit în șablon, selectați sarcina **Estimări de cheltuieli** , și apoi faceți clic pe săgeata **Mapare** pentru a deschide maparea. Selectați linkul **Interogare și filtrare avansate**.

- Dacă utilizați șablonul implicit estimările cheltuielilor proiectului (PSA la Fin și Ops), în Power Query, selectați prima **Condiție inserată** din secțiunea **Pași aplicați**. În intrarea **Funcție** , înlocuiți **O\_forecast** cu numele de ID model prognoză care ar trebui folosit cu integrarea. Șablonul implicit are un ID de model de prognoză din datele demonstrative.
- Când creați un șablon nou, trebuie să adăugați această coloană. În Power Query, selectați **Adăugare coloană condițională** , și introduceți un nume pentru coloana nouă, cum ar fi **ModelID**. Introduceți condiția pentru coloană, unde, dacă ID-ul liniei Estimate nu este nulă, atunci \<enter the forecast model ID\>; altfel nul.

#### <a name="transform-the-billing-types"></a>Transformați tipurile de facturare

Șablonul estimare a cheltuielilor proiectului (PSA la Fin și Ops) include o coloană condițională care este utilizată pentru a transforma tipurile de facturare care sunt primite de la Project Service Automation în timpul integrării. Dacă vă creați propriul șablon, trebuie să adăugați această coloană condițională. Selectați linkul **Interogare și filtrare avansate** și apoi selectați **Adăugare coloană condițională**. Introduceți un nume pentru noua coloană, cum ar fi **BillingType**. Apoi, introduceți următoarea condiție:

Dacă **msdyn\_billingtype** = 192350000, atunci **NonChargeable**  
altfel dacă **msdyn\_billingtype** = 192350001, atunci **Chargeable**  
altfel dacă **msdyn\_billingtype** = 192350002, atunci **Complimentary**  
altfel **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformați tipurile de tranzacții

Șablonul estimare a cheltuielilor proiectului (PSA la Fin și Ops) include o coloană condițională care este utilizată pentru a transforma tipurile de tranzacție care sunt primite de la Project Service Automation în timpul integrării. Dacă vă creați propriul șablon, trebuie să adăugați această coloană condițională. Selectați linkul **Interogare și filtrare avansate** și apoi selectați **Adăugare coloană condițională**. Introduceți un nume pentru noua coloană, cum ar fi **TransactionType**. Apoi, introduceți următoarea condiție:

Dacă **msdyn\_transactiontypecode** = 192350000, atunci **Cost**  
altfel dacă **msdyn\_transactiontypecode** = 192350005, atunci **Sales**  
altfel **null**

### <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

Următoarele ilustrații prezintă exemple de mapări ale sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.

[![Șablon de mapare a tranzacțiilor estimate pentru cheltuieli](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Șablon de mapare a estimărilor de cheltuieli](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]