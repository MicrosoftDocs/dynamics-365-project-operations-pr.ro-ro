---
title: Sincronizați contractele de proiect și proiectele direct din Project Service Automation la Finance and Operations
description: Acest subiect descrie șablonul și activitățile de desfășurare care sunt utilizate pentru a sincroniza contractele de proiect și proiectele direct de la Microsoft Dynamics 365 Project Service Automation la Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e4f11ec0bb88ed0971a3d082e7ca7823fcf8453
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082930"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizați contractele de proiect și proiectele direct din Project Service Automation la Finance and Operations

[!include[banner](../includes/banner.md)]

Acest subiect descrie șablonul și activitățile de desfășurare care sunt utilizate pentru a sincroniza contractele de proiect și proiectele direct de la Dynamics 365 Project Service Automation la Dynamics 365 Finance.

> [!NOTE] 
> Dacă utilizați Enterprise ediția 7.3.0, trebuie să instalați KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxul de date pentru Project Service Automation la Finanțe

> [!NOTE]
> Înainte de a putea utiliza soluția de integrare Project Service Automation la Finance, ar trebui să vă familiarizați cu caracteristica de integrare a datelor Dynamics 365.

Soluția de integrare Project Service Automation la Finance utilizează funcția de integrare a datelor pentru a sincroniza datele între instanțele Project Service Automation și Finance. Șablonul de integrare care este disponibil cu funcția de integrare a datelor permite fluxul de date despre contracte de proiecte, proiecte, linii de contracte de proiect și reperelor de linii de contracte de proiect, de la Project Service Automation până la Finance.

Următoarea ilustrație arată cum sunt sincronizate datele între Project Service Automation și Finance.

[![Fluxul de date pentru integrarea Project Service Automation cu Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Șabloane și activtăți

Pentru a accesa șabloanele disponibile, în centrul de administrare Microsoft Power Apps, selectați **Proiecte** , apoi, în colțul din dreapta sus, selectați **Proiect nou** pentru a selecta șabloanele publice.

Următoarele șabloane și activități în desfășurare sunt utilizate pentru a sincroniza contracte de proiect și proiecte de la Project Service Automation la Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrarea cu Dynamics 365 Project Service Automation v2.x
- **Numele șablonului în Integrarea datelor:** Proiecte și contracte (PSA la Fin și Ops)
- **Numele sarcinilor din proiect:**

    - Proiectul contractează PSA către Fin și Ops
    - Proiectele contractează PSA către Fin și Ops
    - Linii de contract de proiect PSA către Fin și Ops
    - Jaloane de linie de contract PSA la Fin și Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrarea cu Dynamics 365 Project Service Automation v3.x
Există o schimbare de schemă în Project Service Automation care afectează șablonul de referință al liniei de contract Project și este necesară utilizarea versiunii v2 a șablonului pentru a integra Project Service Automation v3.x cu Dynamics 365.

- **Numele șablonului în Integrarea datelor:** Proiecte și contracte (PSA 3.x la Fin și Ops) - v2
- **Numele sarcinilor din proiect:**

    - Proiectul contractează PSA către Fin și Ops
    - Proiectele contractează PSA către Fin și Ops
    - Linii de contract de proiect PSA către Fin și Ops
    - Jaloane de linie de contract PSA la Fin și Ops

Înainte să poată avea loc sincronizarea de contracte de proiecte și proiecte, trebuie să sincronizați conturile.

## <a name="entity-set"></a>Entitate setată

| Project Service Automation       | Finanțe                                                |
|----------------------------------|--------------------------------------------------------|
| Comenzi                           | Entitate de integrare pentru contract de proiect                |
| Proiecte                         | Entitate de integrare pentru proiect                         |
| Linii comandă                      | Entitate de integrare pentru linia de contract           |
| Jaloane linie contract de proiect | Entitate de integrare pentru jaloane linie de contract de proiect |

## <a name="entity-flow"></a>Fluxul de entități

Contractele de proiect sunt gestionate în Project Service Automation și sunt sincronizate cu Finance ca și contracte de proiect. Ca parte a șablonului de integrare, puteți seta sursa de integrare în Finance pentru contractul de proiect.

Proiectul de timp și material și proiectele cu preț fix sunt gestionate în Project Service Automation și sunt sincronizate la Finance ca proiecte. Ca parte a integrării de șablon, puteți seta sursa de integrare în Finance pentru proiect.

Liniile de contract de proiect sunt gestionate în Project Service Automation și sunt sincronizate cu Finance ca și reguli de facturare de contract. Dacă metoda de facturare diferă de tipul de proiect implicit, sincronizarea actualizează tipul de proiect pentru proiectul liniei de contract și grupul de proiecte.

Jaloanele de linii de contract de proiect sunt gestionate în Project Service Automation și sunt sincronizate cu Finance ca și jaloane de reguli de facturare de contract.

## <a name="project-service-automation-to-finance-integration-solution"></a>Soluție de integrare Project Service Automation la Finance

Câmpul **ID-ul contractului de proiect** este disponibil pe pagina **Contracte de proiect**. Acest câmp a devenit o cheie naturală și unică pentru a sprijini integrarea.

Când se creează un nou contract de proiect, dacă o valoare de **ID de contract de proiect** nu există deja, este generată automat utilizând o secvență numerică. Valoarea constă din **ORD** urmat de o secvență numerică incrementală și apoi de un sufix de șase caractere. Iată un exemplu: **ORD-01022-Z4M9Q0**.

Câmpul **Numărul de proiect** este disponibil pe pagina **Proiecte**. Acest câmp a devenit o cheie naturală și unică pentru a sprijini integrarea.

Când se creează un nou contract de proiect, dacă o valoare de **Număr de proiect** nu există deja, este generată automat utilizând o secvență numerică. Valoarea constă din **PRJ** urmat de o secvență numerică incrementală și apoi de un sufix de șase caractere. Iată un exemplu: **PRJ-01049-CCNID0**.

Când se aplică soluția de integrare Project Service Automation to Finance, un script de upgrade setează câmpul **ID-ul contractului de proiect** pentru contractele de proiect existente și **Numărul proiectului** pentru proiecte existente în Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Cerințe preliminare și configurare a mapării

- Înainte să poată avea loc sincronizarea de contracte de proiecte și proiecte, trebuie să sincronizați conturile.
- În setul de conexiuni, adăugați o mapare a câmpului cheii de integrare pentru **msdyn\_organizationalunits** la **msdyn\_name \[Name\]**. Este posibil să fie necesar mai întâi să adăugați un proiect la setul de conexiuni. Pentru mai multe informații, consultați [Integrați datele în Common Data Service pentru aplicații](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- În setul dvs. de conexiune, adăugați o mapare a câmpului cheii de integrare pentru **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**. Este posibil să fie necesar mai întâi să adăugați un proiect la setul de conexiuni. Pentru mai multe informații, consultați [Integrați datele în Common Data Service pentru aplicații](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** pentru contractele de proiecte și proiectele pot fi actualizate la o valoare diferită sau eliminate din mapare. Valoarea implicită a șablonului este **Project Service Automation**.
- Maparea **Termeni de plată** trebuie să fie actualizată astfel încât să reflecte condiții de plată valabile în Finance. De asemenea, puteți elimina maparea din sarcina proiectului. Harta valorilor implicite are valori implicite pentru datele demonstrative. Următorul tabel prezintă valorile din Project Service Automation.

    | Valoare | Descriere   |
    |-------|---------------|
    | 1     | Net 30        |
    | 2     | 2 % 10, Net 30 |
    | 3     | Net 45        |
    | 4     | Net 60        |

## <a name="power-query"></a>Power Query

Trebuie să utilizați Microsoft Power Query pentru Excel pentru a filtra datele dacă sunt îndeplinite următoarele condiții:

- Aveți comenzi de vânzări în Dynamics 365 Sales.
- Aveți mai multe unități organizaționale în Project Service Automation, iar aceste unități organizaționale vor fi mapate la mai multe entități juridice din Finance.

Dacă trebuie să utilizați Power Query, urmați aceste recomandări:

- Șablonul Proiecte și contracte (PSA to Fin și Ops) are un filtru implicit care include numai comenzile de vânzare ale tipului **Element de lucru (msdyn\_ordertype = 192350001)**. Acest filtru ajută la garantarea faptului că nu se creează contracte de proiect pentru comenzile de vânzare din Finance. Dacă vă creați propriul șablon, trebuie să adăugați acest filtru.
- Trebuie să creați un filtru Power Query care să includă numai organizațiile contractuale care ar trebui sincronizate cu entitatea juridică a setului de conexiuni de integrare. De exemplu, contractele de proiect pe care le aveți cu unitatea organizatorică contractuală a Contoso SUA ar trebui sincronizate cu entitatea juridică USSI, dar contractele de proiect pe care le aveți cu unitatea organizatorică contractuală a Contoso Global ar trebui sincronizate cu entitatea juridică USMF. Dacă nu adăugați acest filtru la maparea sarcinilor, toate contractele de proiect vor fi sincronizate cu entitatea juridică definită pentru setul de conexiuni, indiferent de unitatea organizațională a contractului.

## <a name="template-mapping-in-data-integration"></a>Maparea șabloanelor în integrarea datelor

> [!NOTE] 
> Câmpurile **CustomerReference** , **AddressCity** , **AddressCountryRegionID** , **AddressDescription** , **AddressLine1** , **AddressLine2** , **AddressState** și **AddressZipCode** nu sunt incluse în maparea implicită pentru contractele de proiect. Puteți adăuga mapările dacă doriți ca aceste date să fie sincronizate pentru contractele de proiect.
>
> Câmpurile **Descriere** , **ParentID** , **ProjectGroup** , **ProjectManagerPersonnelNumber** , and **ProjectType** nu sunt incluse în maparea implicită pentru proiecte. Puteți adăuga mapările dacă doriți ca aceste date să fie sincronizate pentru proiecte.

Următoarele ilustrații prezintă exemple de mapări ale sarcinilor șablon în Integrarea datelor. Maparea arată informațiile despre câmp care vor fi sincronizate de la Project Service Automation la Finance.

[![Maparea șablonului de contract de proiect](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Maparea șablonului de contract](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Maparea șablonului de linii contract de proiect](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Maparea șablonului de jalon de linie de contract de proiect](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Maparea jalonului de linie contract de proiect în proiectele și contractele (PSA 3.x la Dynamics) - șablonul v2:

[![Maparea șablonului de jalon de linie de contract de proiect cu versiunea a doua a șablonului](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
