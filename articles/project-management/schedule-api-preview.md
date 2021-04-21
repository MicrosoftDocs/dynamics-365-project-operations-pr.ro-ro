---
title: Utilizați API-uri de Planificare pentru a realiza operațiuni cu entități de Planificare
description: Acest subiect oferă informații și exemple pentru utilizarea API-urilor de Planificare.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868144"
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
- Planificarea API-urilor sunt în versiune preliminară publică. Utilizarea acestor API-uri într-un mediu de producție nu este acceptată de Microsoft.

## <a name="sample-scenario"></a>Eșantion de scenariu

În acest scenariu, veți crea un proiect, un membru al echipei, patru sarcini și două alocări de resurse. Apoi, veți actualiza o sarcină, actualizați proiectul, ștergeți o sarcină, ștergeți o atribuire de resurse și creați o dependență de sarcină.

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Eșantioane suplimentare

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
