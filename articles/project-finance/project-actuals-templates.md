---
title: Sincronizarea datelor reale ale proiectului direct din Project Service Automation la jurnalul de integrare a proiectului pentru postare în Finance and Operations
description: Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza datele reale ale proiectului direct de la Microsoft Dynamics 365 Project Service Automation la Finance and Operations.
author: KimANelson
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
ms.assetid: 02ae4986-8e7b-4abe-97d3-cff0904d84de
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7e5aff102226e5eac2ba3de17407eaa4461cd1ac
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754772"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronizarea datelor reale ale proiectului direct din Project Service Automation la jurnalul de integrare a proiectului pentru postare în Finance and Operations

[!include[banner](../includes/banner.md)]

Acest subiect descrie șabloanele și sarcinile de desfășurare care sunt utilizate pentru a sincroniza datele reale ale proiectului direct de la Dynamics 365 Project Service Automation la Dynamics 365 Finance.

Șablonul sincronizează tranzacțiile de la Project Service Automation într-un tabel de etapizare în Finanțe. După finalizarea sincronizării, dvs. **trebuie să** importați datele din tabelul de etapizare în jurnalul de integrare.

> [!NOTE]
> - Integrarea datelor reale ale proiectului este disponibilă începând cu versiunea 8.0.1.
> - Dacă utilizați Enterprise edition 7.3.0 după ce instalați KB 4132657 și KB 4132660, veți putea utiliza șabloanele pentru a integra sarcinile proiectului, categoriile de tranzacții de cheltuieli, estimările orelor, estimările cheltuielilor și datele reale și pentru a configura blocarea funcționalității. Dacă trebuie să resetați distribuțiile contabile, vă recomandăm să instalați și KB 4131710.
> - Dacă utilizați versiunea 7.3.0 și aduceți tranzacții cu taxe de la Project Service Automation, trebuie să instalați KB 4345320 pentru a include aceste taxe în factura proiectului.
> - Dacă introduceți taxe pe vânzări la tranzacții de timp sau cheltuieli în Project Service Automation, trebuie să instalați Project Service Automation actualizarea 7. În caz contrar, datele reale de taxe nu vor fi legate de datele reale aferente timpului sau cheltuielilor și nu vor fi sincronizate cu Finanțe. Pentru mai multe informații, contactați serviciul de asistență.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxul de date pentru Project Service Automation la Finanțe

Soluția de integrare Project Service Automation la Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance. Șabloanele de integrare disponibile cu funcția de integrare a datelor permit fluxul de date despre datele reale ale proiectului de la Project Service Automation la Finance.

Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.

[![Fluxul de date pentru integrarea Project Service Automation cu Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Datele reale ale proiectului din Project Service Automation

### <a name="template-and-tasks"></a>Șabloane și sarcini

Pentru a accesa șabloanele disponibile, în centrul de administrare Microsoft Power Apps, selectați **Proiecte**, apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.

Următorul șablon și sarcinile de desfășurare sunt utilizate pentru a sincroniza datele reale ale proiectului de la Project Service Automation la Finance:

- **Numele șablonului în Integrarea datelor:** datele reale ale proiectului (PSA la Fin și Ops)
- **Numele sarcinilor din proiect:**

    - Valori reale
    - TransactionConnections

### <a name="entity-set"></a>Entitate setată

| Project Service Automation | Finanțe                                   |
|----------------------------|----------------------------------------------------------|
| Valori reale                    | Entitate de integrare pentru datele reale ale proiectului                   |
| Conexiuni de tranzacție    | Entitate de integrare pentru relațiile de tranzacție ale proiectului |

### <a name="entity-flow"></a>Fluxul de entități

Datele reale ale proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu jurnalul de integrare a proiectului în Finanțe. Contabilitatea va fi aplicată pe baza dimensiunilor financiare implicite și a setării de înregistrare.

### <a name="prerequisites"></a>Cerințe preliminare

Înainte ca sincronizarea datelor reale să poată avea loc, trebuie să configurați parametrii de integrare Project Service Automation și să sincronizați proiectele, sarcinile proiectului și categoriile de tranzacții de cheltuieli ale proiectului.

### <a name="power-query"></a>Power Query

În șablonul datelor reale ale proiectului, trebuie să utilizați Microsoft Power Query pentru Excel pentru a finaliza aceste sarcini:

- Transformați tipul de tranzacție în Project Service Automation la tipul de tranzacție corect în Finanțe. Această transformare este deja definită în șablonul datele reale ale proiectului (PSA la Fin și Ops).
- Transformați tipul de facturare în Project Service Automation la tipul de facturare corect în Finanțe. Această transformare este deja definită în șablonul datele reale ale proiectului (PSA la Fin și Ops). Tipul de facturare este apoi mapat la proprietatea liniei, pe baza configurației de pe pagina **Parametri de integrare Project Service Automation**.
- Filtrează la anumite unități organizaționale de resurse care trebuie sincronizate cu acest șablon.
- Dacă timpul între companii sau datele reale ale cheltuielilor între companii vor fi sincronizate cu Finanțele, trebuie să transformați unitatea organizațională a contractului în entitatea juridică corectă din Finanțe. În șablonul date reale ale proiectului (PSA la Fin și Ops), este definită o coloană condițională pe baza datelor demonstrative. Trebuie să actualizați ultima coloană condițională inserată la entitățile juridice corecte. În caz contrar, s-ar putea să apară o eroare de integrare sau tranzacțiile datelor reale incorecte ar putea fi importate în Finanțe.
- Dacă timpul între companii sau cheltuielile datelor reale între companii nu vor fi sincronizate cu Finanțele, trebuie să ștergeți ultima coloană condițională inserată din șablonul dvs. În caz contrar, s-ar putea să apară o eroare de integrare sau tranzacțiile datelor reale incorecte ar putea fi importate în Finanțe.

#### <a name="contract-organizational-unit"></a>Unitate organizațională contract
Pentru a actualiza coloana condițională inserată în șablon, faceți clic pe săgeata **Mapare** pentru a deschide maparea. Selectați linkul **Interogare și filtrare avansate** pentru a deschide Power Query.

- Dacă utilizați șablonul implicit Date reale ale proiectului (PSA la Fin și Ops), în Power Query, selectați ultima **Condiție inserată** din secțiunea **Pași aplicați**. În intrarea **Funcție**, înlocuiți **USSI** cu numele persoanei juridice care ar trebui folosită cu integrarea. Adăugați condiții suplimentare la intrarea **Funcție** după cum doriți și actualizați condiția **else** din **USMF** la persoana juridică corectă.
- Când creați un șablon nou, trebuie să adăugați coloana pentru a accepta timpul și cheltuielile între companii. Selectați **Adăugare coloană condițională**, și introduceți un nume pentru coloană, cum ar fi **LegalEntity**. Introduceți o condiție pentru coloană, unde, dacă **msdyn\_contractorganizationalunitid.msdyn\_name** este \<unitate organizațională\>, atunci \<introduceți persoana juridică\>; altfel este nul.

### <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

Următoarele ilustrații prezintă un exemplu de mapări ale sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.

[![Maparea șabloanelor](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Maparea șabloanelor](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importați din tabelul de etapizare după integrarea din Project Service Automation

Procesul periodic de importare din tabelul de etapizare trebuie executat după sincronizarea datelor reale de la Project Service Automation la Finance. Acest proces va importa tranzacțiile proiectului din tabelul de etapizare în jurnalul de integrare Project Service Automation, unde se aplică contabilitatea și pot fi înregistrate tranzacțiile importate. Vă recomandăm să rulați acest proces în modul lot; poate fi opțional configurat pentru a rula ca un lot recurent.

## <a name="update-actuals-from-finance"></a>Actualizați datele reale de la Finanțe

### <a name="template-and-tasks"></a>Șabloane și sarcini

Următorul șablon și sarcinile de bază sunt utilizate pentru a sincroniza numărul voucherului și taxele de vânzare pentru tranzacțiile de proiect afișate de la Finanțe la Project Service Automation:

- **Numele șablonului în Integrarea datelor:** actualizarea datelor reale ale proiectului (Fin Ops la PSA)
- **Numele sarcinilor din proiect:**

    - Valori reale 
    - TransactionConnections

### <a name="entity-set"></a>Entitate setată

| Finanțe                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entitate de integrare pentru datele reale ale proiectului                   | Valori reale                    |
| Entitate de integrare pentru relațiile de tranzacție ale proiectului | Conexiuni de tranzacție    |

### <a name="entity-flow"></a>Fluxul de entități

Datele reale ale proiectului sunt gestionate în Project Service Automation și sunt sincronizate cu jurnalul de integrare a proiectului în Finanțe. După ce datele reale sunt publicate în Finanțe, acestea sunt actualizate în Project Service Automation cu numărul voucherului de la Finanțe. Dacă s-au adăugat taxe de vânzare în Finanțe, se creează noi date reale de taxare în Project Service Automation.

### <a name="power-query"></a>Power Query

În șablonul de actualizare a datelor reale ale proiectului, trebuie să utilizați Power Query pentru a finaliza aceste sarcini:

- Transformați tipul de tranzacție în Finanțe la tipul de tranzacție corect în Project Service Automation. Această transformare este deja definită în șablonul de actualizare a datelor reale ale proiectului (Fin Ops la PSA).
- Transformați tipul de facturare în Finanțe la tipul de facturare corect în Project Service Automation. Această transformare este deja definită în șablonul de actualizare a datelor reale ale proiectului (Fin Ops la PSA).

### <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

Următoarele ilustrații prezintă exemple de mapări ale sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Finance la Project Service Automation.

[![Maparea șabloanelor](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Maparea șabloanelor](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
