---
title: Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare
description: Acest subiect oferă informații și exemple pentru utilizarea API-urilor de Planificare.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116812"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

> [!IMPORTANT] 
> O parte sau toate funcționalitățile notate în acest subiect sunt disponibile ca parte a ediției de previzualizare. Conținutul și funcționalitățile pot fi modificate. 

## <a name="scheduling-entities"></a>Entități de planificare

API-urile de programare oferă posibilitatea de a efectua operațiuni de creare, actualizare și ștergere cu **Entități de planificare**. Aceste entități sunt gestionate prin intermediul motorului de planificare în Proiect pentru web. Creați, actualizați și ștergeți operațiuni cu **Entități de planificare** au fost restricționate în versiuni mai timpurii ale Dynamics 365 Project Operations.

Următorul tabel oferă o listă completă a **Entităților de planificare**.

| Nume de entitate  | Numele logic al entității |
| --- | --- |
| Project | msdyn_project |
| Activitate de proiect  | msdyn_projecttask  |
| Dependență de activitate proiect  | msdyn_projecttaskdependency  |
| Atribuire de resurse | msdyn_resourceassignment |
| Pachet de proiect  | msdyn_projectbucket |
| Membru echipă de proiect | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet este un model de unitate de lucru care poate fi utilizat atunci când mai multe cereri care afectează planificarea trebuie procesate în cadrul unei tranzacții.

## <a name="schedule-apis"></a>Planificați API-urile

Următoarea este o listă a API-urilor curente de planificare.

- **msdyn_CreateProjectV1**: Acest API poate fi folosit pentru a crea un proiect. Proiectul și pachetul de proiect implicit sunt create imediat.
- **msdyn_CreateTeamMemberV1**: Acest API poate fi utilizat pentru a crea un membru al echipei de proiect. Înregistrarea membrilor echipei este creată imediat.
- **msdyn_CreateOperationSetV1**: Acest API poate fi utilizat pentru a programa mai multe solicitări care trebuie efectuate în cadrul unei tranzacții.
- **msdyn_PSSCreateV1**: Acest API poate fi utilizat pentru a crea o entitate. Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de creare.
- **msdyn_PSSUpdateV1**: acest API poate fi utilizat pentru a actualiza o entitate. Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de actualizare.
- **msdyn_PSSDeleteV1**: acest API poate fi utilizat pentru a șterge o entitate. Entitatea poate fi oricare dintre entitățile de planificare care susțin operațiunea de ștergere.
- **msdyn_ExecuteOperationSetV1**: Acest API este utilizat pentru a executa toate operațiunile din cadrul setului de operații date.

## <a name="using-schedule-apis-with-operationset"></a>Utilizarea API-urilor de programare cu OperationSet

Pentru că înregistrează cu amândouă **CreateProjectV1** și **CreateTeamMemberV1** sunt create imediat, aceste API-uri nu pot fi utilizate în **OperationSet** direct. Cu toate acestea, puteți utiliza API-ul pentru a crea înregistrări necesare, pentru a crea un **OperationSet**, și apoi utilizați aceste înregistrări pre-create în **OperationSet**.

## <a name="supported-operations"></a>Operațiuni acceptate

| Entitate de planificare | Creați | Actualizați | Delete | Considerații importante |
| --- | --- | --- | --- | --- |
Activitate de proiect | Da | Da | Da | Fără |
| Dependență de activitate proiect | Da | Da | | Înregistrările de dependență ale sarcinii de proiect nu sunt actualizate. În schimb, o înregistrare veche poate fi ștearsă și o nouă înregistrare poate fi creată. |
| Atribuire de resurse | Da | Da | | Operațiile cu următoarele câmpuri nu sunt acceptate: **BookableResourceID**, **Efort**, **EfortCompletat**, **EfortRămânând**, și **PlannedWork**. Înregistrările de alocare a resurselor nu sunt actualizate. În schimb, înregistrarea veche poate fi ștearsă și o nouă înregistrare poate fi creată. |
| Pachet de proiect | Nedisponibil | Nedisponibil | Nedisponibil | Pachetul implicit este creat folosind API **CreateProjectV1**. |
| Membru echipă de proiect | Da | Da | Da | Pentru operația de creare, utilizați API **CreateTeamMemberV1**. |
| Project | Da | Da | Nedisponibil | Operațiunile cu următoarele câmpuri nu sunt acceptate: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Efort**, **EfortCompletat**, **EfortRămânând**, **Progres**, **Finalizare**, **TaskEarliestStart** și **Durată**. |

Aceste API-uri pot fi apelate cu obiecte de entitate care includ câmpuri personalizate.

Proprietatea ID este opțională. Dacă este furnizat, sistemul încearcă să-l folosească și aruncă o excepție dacă nu poate fi folosit. Dacă nu este furnizat, sistemul îl va genera.

## <a name="restricted-fields"></a>Câmpuri restricționate

Următoarele tabele definesc câmpurile care sunt restricționate din **Creare** și **Editare.**

### <a name="project-task"></a>Activitate de proiect

| **Nume logic**                       | **Poate crea** | **Poate edita**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | nu             | nu               |
| msdyn_actualcost_base                  | nu             | nu               |
| msdyn_actualend                        | nu             | nu               |
| msdyn_actualsales                      | nu             | nu               |
| msdyn_actualsales_base                 | nu             | nu               |
| msdyn_actualstart                      | nu             | nu               |
| msdyn_costatcompleteestimate           | nu             | nu               |
| msdyn_costatcompleteestimate_base      | nu             | nu               |
| msdyn_costconsumptionpercentage        | nu             | nu               |
| msdyn_effortcompleted                  | nu             | nu               |
| msdyn_effortestimateatcomplete         | nu             | nu               |
| msdyn_iscritical                       | nu             | nu               |
| msdyn_iscriticalname                   | nu             | nu               |
| msdyn_ismanual                         | nu             | nu               |
| msdyn_ismanualname                     | nu             | nu               |
| msdyn_ismilestone                      | nu             | nu               |
| msdyn_ismilestonename                  | nu             | nu               |
| msdyn_LinkStatus                       | nu             | nu               |
| msdyn_linkstatusname                   | nu             | nu               |
| msdyn_msprojectclientid                | nu             | nu               |
| msdyn_plannedcost                      | nu             | nu               |
| msdyn_plannedcost_base                 | nu             | nu               |
| msdyn_plannedsales                     | nu             | nu               |
| msdyn_plannedsales_base                | nu             | nu               |
| msdyn_pluginprocessingdata             | nu             | nu               |
| msdyn_progress                         | nu             | nu (da pentru P4W) |
| msdyn_remainingcost                    | nu             | nu               |
| msdyn_remainingcost_base               | nu             | nu               |
| msdyn_remainingsales                   | nu             | nu               |
| msdyn_remainingsales_base              | nu             | nu               |
| msdyn_requestedhours                   | nu             | nu               |
| msdyn_resourcecategory                 | nu             | nu               |
| msdyn_resourcecategoryname             | nu             | nu               |
| msdyn_resourceorganizationalunitid     | nu             | nu               |
| msdyn_resourceorganizationalunitidname | nu             | nu               |
| msdyn_salesconsumptionpercentage       | nu             | nu               |
| msdyn_salesestimateatcomplete          | nu             | nu               |
| msdyn_salesestimateatcomplete_base     | nu             | nu               |
| msdyn_salesvariance                    | nu             | nu               |
| msdyn_salesvariance_base               | nu             | nu               |
| msdyn_scheduleddurationminutes         | nu             | nu               |
| msdyn_scheduledend                     | nu             | nu               |
| msdyn_scheduledstart                   | nu             | nu               |
| msdyn_schedulevariance                 | nu             | nu               |
| msdyn_skipupdateestimateline           | nu             | nu               |
| msdyn_skipupdateestimatelinename       | nu             | nu               |
| msdyn_summary                          | nu             | nu               |
| msdyn_varianceofcost                   | nu             | nu               |
| msdyn_varianceofcost_base              | nu             | nu               |

### <a name="project-task-dependency"></a>Dependență de activitate proiect

| **Nume logic**              | **Poate crea** | **Poate edita** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | nu             | nu           |
| msdyn_linktypename            | nu             | nu           |
| msdyn_predecessortask         | da            | nu           |
| msdyn_predecessortaskname     | da            | nu           |
| msdyn_project                 | da            | nu           |
| msdyn_projectname             | da            | nu           |
| msdyn_projecttaskdependencyid | da            | nu           |
| msdyn_successortask           | da            | nu           |
| msdyn_successortaskname       | da            | nu           |

### <a name="resource-assignment"></a>Atribuire de resurse

| **Nume logic**             | **Poate crea** | **Poate edita** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | da            | nu           |
| msdyn_bookableresourceidname | da            | nu           |
| msdyn_bookingstatusid        | nu             | nu           |
| msdyn_bookingstatusidname    | nu             | nu           |
| msdyn_committype             | nu             | nu           |
| msdyn_committypename         | nu             | nu           |
| msdyn_effort                 | nu             | nu           |
| msdyn_effortcompleted        | nu             | nu           |
| msdyn_effortremaining        | nu             | nu           |
| msdyn_finish                 | nu             | nu           |
| msdyn_plannedcost            | nu             | nu           |
| msdyn_plannedcost_base       | nu             | nu           |
| msdyn_plannedcostcontour     | nu             | nu           |
| msdyn_plannedsales           | nu             | nu           |
| msdyn_plannedsales_base      | nu             | nu           |
| msdyn_plannedsalescontour    | nu             | nu           |
| msdyn_plannedwork            | nu             | nu           |
| msdyn_projectid              | da            | nu           |
| msdyn_projectidname          | nu             | nu           |
| msdyn_projectteamid          | nu             | nu           |
| msdyn_projectteamidname      | nu             | nu           |
| msdyn_start                  | nu             | nu           |
| msdyn_taskid                 | nu             | nu           |
| msdyn_taskidname             | nu             | nu           |
| msdyn_userresourceid         | nu             | nu           |

### <a name="project-team-member"></a>Membru echipă de proiect

| **Nume logic**                                 | **Poate crea** | **Poate edita** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | nu             | nu           |
| msdyn_creategenericteammemberwithrequirementname | nu             | nu           |
| msdyn_deletestatus                               | nu             | nu           |
| msdyn_deletestatusname                           | nu             | nu           |
| msdyn_effort                                     | nu             | nu           |
| msdyn_effortcompleted                            | nu             | nu           |
| msdyn_effortremaining                            | nu             | nu           |
| msdyn_finish                                     | nu             | nu           |
| msdyn_hardbookedhours                            | nu             | nu           |
| msdyn_hours                                      | nu             | nu           |
| msdyn_markedfordeletiontimer                     | nu             | nu           |
| msdyn_markedfordeletiontimestamp                 | nu             | nu           |
| msdyn_msprojectclientid                          | nu             | nu           |
| msdyn_percentage                                 | nu             | nu           |
| msdyn_requiredhours                              | nu             | nu           |
| msdyn_softbookedhours                            | nu             | nu           |
| msdyn_start                                      | nu             | nu           |

### <a name="project"></a>Project

| **Nume logic**                       | **Poate crea** | **Poate edita** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | nu             | nu           |
| msdyn_actualexpensecost_base           | nu             | nu           |
| msdyn_actuallaborcost                  | nu             | nu           |
| msdyn_actuallaborcost_base             | nu             | nu           |
| msdyn_actualsales                      | nu             | nu           |
| msdyn_actualsales_base                 | nu             | nu           |
| msdyn_contractlineproject              | da            | nu           |
| msdyn_contractorganizationalunitid     | da            | nu           |
| msdyn_contractorganizationalunitidname | da            | nu           |
| msdyn_costconsumption                  | nu             | nu           |
| msdyn_costestimateatcomplete           | nu             | nu           |
| msdyn_costestimateatcomplete_base      | nu             | nu           |
| msdyn_costvariance                     | nu             | nu           |
| msdyn_costvariance_base                | nu             | nu           |
| msdyn_duration                         | nu             | nu           |
| msdyn_effort                           | nu             | nu           |
| msdyn_effortcompleted                  | nu             | nu           |
| msdyn_effortestimateatcompleteeac      | nu             | nu           |
| msdyn_effortremaining                  | nu             | nu           |
| msdyn_finish                           | da            | da          |
| msdyn_globalrevisiontoken              | nu             | nu           |
| msdyn_islinkedtomsprojectclient        | nu             | nu           |
| msdyn_islinkedtomsprojectclientname    | nu             | nu           |
| msdyn_linkeddocumenturl                | nu             | nu           |
| msdyn_msprojectdocument                | nu             | nu           |
| msdyn_msprojectdocumentname            | nu             | nu           |
| msdyn_plannedexpensecost               | nu             | nu           |
| msdyn_plannedexpensecost_base          | nu             | nu           |
| msdyn_plannedlaborcost                 | nu             | nu           |
| msdyn_plannedlaborcost_base            | nu             | nu           |
| msdyn_plannedsales                     | nu             | nu           |
| msdyn_plannedsales_base                | nu             | nu           |
| msdyn_progress                         | nu             | nu           |
| msdyn_remainingcost                    | nu             | nu           |
| msdyn_remainingcost_base               | nu             | nu           |
| msdyn_remainingsales                   | nu             | nu           |
| msdyn_remainingsales_base              | nu             | nu           |
| msdyn_replaylogheader                  | nu             | nu           |
| msdyn_salesconsumption                 | nu             | nu           |
| msdyn_salesestimateatcompleteeac       | nu             | nu           |
| msdyn_salesestimateatcompleteeac_base  | nu             | nu           |
| msdyn_salesvariance                    | nu             | nu           |
| msdyn_salesvariance_base               | nu             | nu           |
| msdyn_scheduleperformance              | nu             | nu           |
| msdyn_scheduleperformancename          | nu             | nu           |
| msdyn_schedulevariance                 | nu             | nu           |
| msdyn_taskearlieststart                | nu             | nu           |
| msdyn_teamsize                         | nu             | nu           |
| msdyn_teamsize_date                    | nu             | nu           |
| msdyn_teamsize_state                   | nu             | nu           |
| msdyn_totalactualcost                  | nu             | nu           |
| msdyn_totalactualcost_base             | nu             | nu           |
| msdyn_totalplannedcost                 | nu             | nu           |
| msdyn_totalplannedcost_base            | nu             | nu           |


## <a name="limitations-and-known-issues"></a>Limitări și probleme cunoscute
Următoarea este o listă de limitări și probleme cunoscute:

- API-urile de programare pot fi utilizate numai de **Utilizatori cu licență Microsoft Project.** Nu pot fi utilizate de:
    - Utilizatori aplicație
    - Utilizatori de sistem
    - Utilizatori de integrare
    - Alți utilizatori care nu au licența necesară
- Fiecare **OperationSet** poate efectua doar maximum 100 de operații.
- Fiecare utilizator poate avea doar un maximum de 10 **OperationSets**.
- Project Operations acceptă în prezent maximum 500 de sarcini totale pe un proiect.
- **OperationSet** starea de eroare și jurnalele de erori nu sunt disponibile momentan.
- [Limite și restricții pentru proiecte și sarcini](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Eroare de tratare

   - Pentru a revizui erorile generate din seturile de operații, accesați **Setări** \> **Integrarea planificării** \> **Seturi de operații**.
   - Pentru a examina erorile generate de serviciul de planificare a proiectelor, accesați **Setări** \> **Integrarea planificării** \> **Jurnalele de erori PSS**.

## <a name="sample-scenario"></a>Eșantion de scenariu

În acest scenariu, veți crea un proiect, un membru al echipei, patru sarcini și două alocări de resurse. Apoi, veți actualiza o sarcină, actualizați proiectul, ștergeți o sarcină, ștergeți o atribuire de resurse și creați o dependență de sarcină.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Eșantioane suplimentare

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
