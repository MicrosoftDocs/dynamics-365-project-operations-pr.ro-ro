---
title: Versiuni de hartă Project Operations cu scriere duală
description: Acest subiect oferă lista hărților cu dublă scriere necesare pentru Dynamics 365 Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939031"
---
# <a name="project-operations-dual-write-map-versions"></a>Versiuni de hartă Project Operations cu scriere duală

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Folosind Dynamics 365 Project Operations pentru resurse/scenarii fără stoc necesită un set de hărți cu scriere duală care să fie rulate în mediu. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Hărți preliminare: soluție de orchestrare cu scriere duală

Următoarele hărți sunt condiții preliminare necesare pentru soluția Project Operations. Asigurați-vă că rulați hărțile listate în tabelul următor și orice hărți de tabel aferente din mediul dvs.

| Mapare de tabele | Sincronizare inițială |
| --- | --- |
| Registru (msdyn_ledgers) | Necesită sincronizare inițială pentru harta tabelului și toate condițiile preliminare. Coordonatorul pentru sincronizarea inițială este aplicația Finance and Operations. |
| Entități legale (cdm_companies) | Nu este necesar. Sistemul populează această entitate automat atunci când mediile sunt conectate utilizând scrierea duală. |
| Clienți V3 (conturi) | Nu este necesar pentru pregătire. |
| Furnizori V2 (msdyn_vendors) | Nu este necesar pentru pregătire. |

1. Din lista de hărți, selectați harta Registru **(msdyn\_ledgers)** cu toate premisele si selectați caseta de bifare **Sincronizare inițială**. În câmpul **Coordonator pentru sincronizarea inițială**, selectați **aplicații Finance and Operations** atât pentru harta contabilă, cât și pentru toate hărțile preliminare necesare. Selectare rând **Rulare**.

![Sincronizarea hărții registrului](media/DW6.png)

1. Urmați aceiași pași pentru toate hărțile de tabel rămase enumerate în tabelul de mai sus. Nu selectați caseta de selectare **Sincronizare inițială** atunci când rulați acele hărți.

## <a name="project-operations-dual-write-maps"></a>Hărți de scriere duală pentru Project Operations

Următoarele hărți sunt necesare pentru o soluție Project Operations.

| **Maparea entității** | **Cea mai recentă versiune** | **Sincronizare inițială** |
| --- | --- | --- |
| Entitate de integrare pentru relațiile de tranzacție ale proiectului (msdyn\_transactionconnections) | 1.0.0.0 | Nu este necesar pentru pregătire. |
| Anteturile contractului de proiect (comenzi de vânzări) | 1.0.0.1 | Nu este necesar pentru pregătire. |
| Linii de contract de proiect (salesorderdetails) | 1.0.0.0 | Nu este necesar pentru pregătire. |
| Sursa de finanțare a proiectului (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Nu este necesar pentru pregătire. |
| Tabel de integrare a Project Operations pentru estimări de materiale (msdyn\_estimatelines) | 1.0.0.0 | Nu este necesar pentru pregătire. |
| Propuneri de facturi de proiect V2 (facturi) | 1.0.0.2 | Nu este necesar pentru pregătire. |
| Integrare valori reale Project Operations (msdyn_actuals) | 1.0.0.14 | Nu este necesar pentru pregătire. |
| Integrare Project Operations de jaloane linie de contract (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Nu este necesar pentru pregătire. |
| Entitate de integrare a Project Operations pentru estimări de cheltuieli (msdyn_estimateslines) | 1.0.0.2 | Nu este necesar pentru pregătire. |
| Entitate de integrare a Project Operations pentru estimări orare (msdyn_resourceassignments) | 1.0.0.5 | Nu este necesar pentru pregătire. |
| Entitate de integrare de export Project Operations pentru categorii de cheltuieli (msdyn_expensecategories) | 1.0.0.2 | Nu este necesar pentru pregătire. |
| Entitate de integrare a Project Operations pentru cheltuieli de export (msdyn_expenses) | 1.0.0.2 | Nu este necesar pentru pregătire. |
| Entitatea privind exportul facturilor de la furnizori în proiectul de integrare Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Nu este necesar pentru pregătire. |
| Entitatea privind exportul liniilor de factură de la furnizori în proiectul de integrare Project operations (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Nu este necesar pentru pregătire. |
| Roluri de resurse de proiect pentru toate companiile (bookableresourcecategories) | 1.0.0.1 | Necesită o sincronizare inițială pentru harta tabelului pentru a sincroniza rolurile de resurse ale managerului de proiect și ale membrilor echipei care sunt populate în mediul Dynamics 365 Dataverse în timpul aprovizionării. Dataverse este sursa principală pentru sincronizarea inițială. |
| Sarcini de proiect (msdyn_projecttasks) | 1.0.0.4 | Nu este necesar pentru pregătire. |
| Categorii de tranzacții de proiect (msdyn_transactioncategories) | 1.0.0.0 | Nu este necesar pentru pregătire. |
| Proiecte V2 (msdyn_projects) | 1.0.0.1 | Nu este necesar pentru pregătire. |

Parcurgeți următorii pași pentru a rula hărțile listate.

1. Activați rolurile de resurse ale proiectului pentru harta tabelului **toate companiile (bookableresourcecategories)** deoarece această hartă necesită sincronizarea inițială. În câmpul **Coordonator pentru sincronizarea inițială** selectați **Common Data Service**. 

 ![Sincronizarea hărții tabelului de rol de resursă](media/6ResourceInitialSync.jpg)

 Așteptați până când starea hărții este **Rulare** înainte de a trece la pasul următor.

2. Selectați toate celelalte hărți necesare. Le puteți filtra în lista de hărți cu scriere duală folosind cuvântul cheie **Proiect** în căutare, în colțul din dreapta sus. Puteți selecta mai multe hărți și apoi le puteți rula. Pentru mai multe informații, consultați: [Gestionați mai multe hărți de tabel](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Asigurați-vă activați și rulați de asemenea și hărți de entități conexe.

### <a name="project-operations-dual-write-map-versions"></a>Versiuni de hartă Project Operations cu scriere duală

Rulați întotdeauna cea mai recentă versiune a hărții în mediul dvs. Este posibil ca anumite caracteristici și capacități să nu funcționeze corect dacă există oricare dintre următoarele condiții:

- O hartă nu este activată.
- Cea mai recentă versiune a hărții nu este activată. 
- Hărțile de tabel aferente nu sunt activate.

Puteți vizualiza versiunea activă a hărții în coloana **Versiune** de pe pagina **Scriere duală**. Puteți activa o nouă versiune a hărții selectând **Versiuni de hărții cu tabele**, selectând cea mai recentă versiune și apoi salvând versiunea selectată. Dacă ați personalizat o hartă a tabelului predefinită, va trebui să aplicați din nou modificările. Pentru mai multe informații, consultați: [Gestionarea ciclului de viață al aplicațiilor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).