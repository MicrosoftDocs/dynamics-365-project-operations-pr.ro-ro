---
title: Modificări de caracteristici de la Project Service Automation la Project Operations
description: Acest articol oferă o prezentare generală a modificărilor caracteristicilor de la Project Service Automation la Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459942"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Modificări de caracteristici de la Project Service Automation la Project Operations

Upgrade-ul de la Dynamics 365 Project Service Automation la Dynamics 365 Project Operations Lite va fi livrat în trei etape. Acest articol oferă informații despre modificările majore pe care vă puteți aștepta să le vedeți când actualizarea este finalizată.

| Livrare upgrade | Faza 1 <br>(Ianuarie 2022) | Faza 2 <br>(Noiembrie 2022) | Faza 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Nicio dependență de structura de defalcare a lucrărilor (WBS) pentru proiecte. | :bifă solidă: | :bifă solidă: | :bifă solidă: |
| WBS este inclus în limitele suportate în prezent de Project Operations. | &nbsp; | :bifă solidă: | :bifă solidă: |
| WBS în afara limitelor suportate în prezent de Project Operations, inclusiv suport pentru Project desktop client. | &nbsp; | &nbsp; | :bifă solidă: |

## <a name="project-management"></a>Gestionarea proiectelor

Cele mai semnificative schimbări în experiența utilizatorului vor fi în zona de planificare a proiectelor. Project Operations adoptă o nouă experiență modernă pentru gestionarea unei structuri de defalcare a lucrărilor (WBS) prin valorificarea capabilităților de programare oferite de [Project for the Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Diferențe în experiența de planificare

Următorul tabel rezumă diferențele de planificare dintre Project Service Automation și Project Operations.

|  Planificare     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Șabloane de proiect – Abilitatea de a defini și aplica șabloane de proiect atunci când este creat un proiect  |  &nbsp;    | :bifă solidă: |
| Integrarea structurii de defalcare a lucrărilor de proiect (WBS) cu clientul desktop   |    &nbsp;  | :bifă solidă: |
| Constrângeri – Începere nu mai devreme de, finalizare nu mai târziu de  | :bifă solidă: |   &nbsp;  |
| Jaloane – Sarcini cu durată zero   | :bifă solidă:  |  &nbsp;  |
| Sarcinile bazate pe resurse vor respecta disponibilitatea resurselor alocate   | :bifă solidă: |  &nbsp;    |
| Editare în etape de timp – Editați planurile și lucrați zi de zi   |   &nbsp;  | :bifă solidă: |
| Programare automată/manuală – Utilizați motorul de planificare a proiectului pentru a programa automat sau manual sarcini |  &nbsp; | :bifă solidă:  |
| Editați proiecte mari direct în interfața cu utilizatorul: nu există nicio limită pentru dimensiunea planurilor care sunt editabile  | Limită de sarcini 500  | :bifă solidă:       |
| Procent finalizat – Marcați progresul sarcinii   | :bifă solidă:  |  &nbsp;  |
| [Moduri de planificare a proiectului](../project-management/scheduling-modes.md) – Definiți proiectul ca unități fixe, efort fix sau durată fixă | :bifă solidă: | &nbsp; |
| Cronologie – Creați și personalizați vizualizarea cronologiei pentru a vizualiza detaliile programului și pentru a comunica cu părțile interesate. | :bifă solidă:  | &nbsp; |
| Sarcini bazate pe efort – Suportul motorului de programare pentru programarea unei sarcini ca bazată pe efort  | :bifă solidă:  | &nbsp; |
| Caseta de dialog **Informații despre sarcină** – Salvați detaliile sarcinii utilizând o casetă de dialog | :bifă solidă:  |  &nbsp;  |
| Trageți și plasați – Selectați sarcini multiple și modificați poziția lor pe WBS | :bifă solidă: | &nbsp;  |
| Vizualizări persistente flexibile – Definiți vizualizări mai granulare ale atributelor sarcinii   | :bifă solidă:  | &nbsp; |
| Sortare și filtrare WBS  | :bifă solidă:  | &nbsp; |
| Vizualizare panouri pentru livrarea proiectului non-cascadă  | :bifă solidă:   | &nbsp; |
| Vizualizare cronologie – Diagramă Gantt interactivă utilizată pentru a vizualiza și edita WBS   | :bifă solidă:  | &nbsp; |
| Comenzi rapide de la tastatură – Utilizați comenzile rapide de la tastatură pentru operațiuni obișnuite, cum ar fi indentarea sau inserarea  | :bifă solidă:  |  &nbsp; |
| Anulare pe mai multe niveluri – Efectuați o analiză de tip „ce ar fi dacă” pentru a înțelege pe deplin impactul modificărilor prin inversarea și reaplicarea unui întreg set de operațiuni | :bifă solidă: | &nbsp; |
| Decupare/Copiere/Lipire – Colaborați la dezvoltarea programului prin copierea și lipirea detaliilor programului între aplicații  | :bifă solidă: | &nbsp; |
| Liste de verificare pentru sarcini – Adăugați până la 20 de elemente din lista de verificare la o sarcină   | :bifă solidă: | &nbsp; |

## <a name="project-planning"></a>Planificarea unui proiect

Pagina **Proiect** din Project Operations are un număr semnificativ de diferențe în comparație cu pagina **Proiect** din Project Service Automation.

Următoarele acțiuni au fost eliminate de pe pagina **Proiecte** ca parte a actualizării Fazei 1:

  - **Deschideți în MS Project**
  - **Creare șablon**
  - **Anulați legătura cu MS Project**

Pagina **Proiect** din Project Operations include următoarele file noi.

- **Estimări materiale**
- **Configurare facturare activități**

Dila **Stare** a fost eliminată și câmpul **Stare** se află acum pe fila **Rezumat** cu modul de programare al proiectului.

   ![Actualizări la pagina Proiect.](media/projectform.png)

Fila **Planificare** a fost redenumită în fila **Sarcină** și prezintă noua experiență de planificare a proiectelor cu Project for the Web.

   ![Filă nouă Sarcini de proiect.](media/tasktab.png)

## <a name="scheduling-modes"></a>Moduri de planificare

Project Operations a introdus o nouă caracteristică, [Moduri de planificare](../project-management/scheduling-modes.md). Toate proiectele existente Project Service Automation vor setate în mod implicit la **Durată fixă** în Project Operations. Cu toate acestea, valoarea implicită pentru proiecte noi poate fi gestionată accesând **Setări** > **Parametri** > **Parametru** > **Mod planificare**.

   ![Setări ale parametrilor proiectului pentru modul Planificare.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limite de planificare a proiectelor

Project Operations se bazează pe Project for the Web pentru toate operațiunile de planificare a proiectelor. Project for the Web gestionează structura de defalcare a lucrărilor utilizând limitele din tabelul următor.

| **Câmp**                                          | **Limită**             |
|----------------------------------------------------|-----------------------|
| Total maxim activități pentru un proiect                  | 500                   |
| Total maxim durată pentru un proiect               | 3650 de zile (10 ani)  |
| Total maxim resurse pentru un proiect              | 300                   |
| Numărul maxim de legături (numai succesoare) pentru un proiect | 600                   |
| Total maxim de câmpuri particularizate pentru un proiect          | 10                    |
| Nivelul ierarhic maxim                            | 10 niveluri             |
| Legături maxime (succesor + predecesor)            | 20                    |
| Durata maximă a sarcinii frunzelor                      | 1250 de zile             |
| Durata maximă a unei sarcini rezumative                 | 3650 de zile (10 ani)  |
| Maximul de resurse atribuit unei activități               | 20 de resurse          |
| Interval de date acceptat pentru o activitate                    | 1/1/2000 - 12/31/2149 |
| Elemente listă de verificare                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Extensibilitatea și dezvoltarea planificării proiectelor

După ce faceți upgrade la Project Operations, trebuie să utilizați API-urile Project Scheduling pentru a executa operațiuni de creare, actualizare și ștergere pe următoarele entități:

|   Nume de entitate           |   Numele logic al entității       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Activitate proiect            | msdyn_projecttask           |
| Dependență de activitate proiect | msdyn_projecttaskdependency |
| Atribuire de resurse     | msdyn_resourceassignment    |
| Pachet de proiect          | msdyn_projectbucket         |
| Membru echipă de proiect     | msdyn_projectteam           |

Dacă în prezent aveți personalizări care implică aceste entități, consultați [Utilizarea API-urilor de planificare a proiectului pentru a efectua operațiuni cu entitățile de planificare](../project-management/schedule-api-preview.md) pentru îndrumări de implementare.

## <a name="data-model-changes"></a>Modificări model de date

Ca parte a Fazei 1 de Upgrade, au loc modificări ale modelului de date. Aceste modificări sunt în primul rând modificări de câmp ale entităților existente. În Faza 1, entitățile **msydn_project** și **msdyn_projectteam** sunt o refactorizare a personalizărilor. 

> [!IMPORTANT]
> Această secțiune va fi actualizată cu entități suplimentare pe măsură ce fazele viitoare de actualizare sunt finalizate.

Următoarele câmpuri au fost înlocuite cu câmpuri noi.

|   Entity          |   Nume logic vechi   |   Nume logic nou    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Următoarele câmpuri au fost adăugate.

|   Entity          |   Nume logic                               |   Descriere |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Afișează totalul vânzărilor cu taxe reale pentru proiect. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Afișează costul total al materialului real al proiectului. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Afișează totalul vânzărilor reale de materiale din proiect. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Linia de contract asociată acestui proiect. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Acesta este un câmp intern de sistem care este utilizat pentru identificatorul de corelare legat de **Copiere proiect**. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Acesta este un câmp intern al sistemului, utilizat pentru **Copiere proiect** legat de Identificatorul de sesiune. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Ultima sincronizare xRM Global Revision Token din Serviciul de planificare a proiectului. |
| msdyn_project     | msdyn_msprojectdocument                      | Documentul Microsoft Project care aparține proiectului. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Totalul costului pentru materiale planificat pentru proiect. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Totalul vânzărilor de materiale planificat pentru proiect. Numai pentru utilizare în Project Service Automation. |
| msdyn_project     | msdyn_program                                | Programul cu care este corelat acest proiect. |
| msdyn_project     | msdyn_quotelineproject                       | Linia de ofertă asociată cu acest proiect. |
| msdyn_project     | msdyn_replaylogheader                        | Antetul pentru jurnalele de reluare a redării. |
| msdyn_project     | msdyn_schedulemode                           | Modul de programare implicit, utilizat pentru toate sarcinile din proiect.  |
| msdyn_project     | msdyn_taskearlieststart                      | Cea mai timpurie dată de începere a oricărei activități din proiect.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Membrul echipei de proiect din care a fost copiat acest membru al echipei de proiect. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Indică dacă se creează cerința de resurse pentru un membru de echipă generic creat recent.  |
| msdyn_projectteam | msdyn_deletestatus                           | Starea de ștergere a membrului de echipă pentru a urmări dacă există o solicitare de ștergere trimisă către Project scheduling service și dacă acesta trimite un răspuns înapoi cu succes în fereastra de timp preconizată. |
| msdyn_projectteam | msdyn_effortcompleted                        | Urmărește efortul realizat de membrul echipei în atribuirile sale. |
| msdyn_projectteam | msdyn_effortremaining                        | Urmărește efortul care urmează a fi finalizat de membrul echipei în atribuirile sale. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Perioada de așteptare de la momentul în care membrul echipei trimite o solicitare de ștergere către Project scheduling service până când membrul echipei este șters efectiv în Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Marca de timp pentru înregistrarea momentului în care solicitarea de ștergere a membrului de echipă este trimisă către Project scheduling service. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Arată membrul echipei de proiect din care a fost copiat acest membru al echipei de proiect.  |

## <a name="project-templates"></a>Șabloane de proiect

Project Operations nu oferă suport pentru șabloanele de proiect. Cu toate acestea, puteți reproduce o mare parte din funcționalitatea de bază cu utilizarea [API-ului Copiere proiect](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Suport pentru programe de completare desktop

Suportul pentru programul de completare Microsoft Project Desktop nu va fi disponibil în primele 2 faze ale upgrade-ului. În Faza 3, clienții care au proiecte mai mari decât limitele acceptate în prezent de Project for the Web vor putea folosi programul de completare pentru desktop.

## <a name="editing-resource-assignment-contours"></a>Editare contururi de atribuire a resurselor

Capacitatea de a edita contururile de atribuire a resurselor va fi disponibilă atunci când Faza 2 de actualizare este disponibilă.

## <a name="billing-and-pricing"></a>Facturarea și stabilirea prețurilor

Următoarele caracteristici noi au fost adăugate în Project Operations. Aceste caracteristici sunt de natură aditivă și nu afectează modelul de date Project Service Automation.

- [Înregistrarea utilizării de materiale pentru proiecte și activitățile proiectului](../material/material-usage-log.md)
- [Gestionarea subcontractării](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansuri și contracte bazate pe garanții](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statutul contractului de a nu depăși și validările](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Facturare pe bază de activități](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Componente depreciate

Următoarele tabele documentează toate câmpurile depreciate care sunt mutate în soluția de componente depreciate după actualizare. Pentru mai multe informații și un link către soluție, consultați [Componente depreciate Dynamics 365 Project Service Automation 3x la Project Operations 4x](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>detaliufactură

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>detaliucomandăvânzare

| Câmpuri                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

