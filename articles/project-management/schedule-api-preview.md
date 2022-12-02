---
title: Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare
description: Acest articol oferă informații și exemple pentru utilizarea API-urilor de planificare a proiectului.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541140"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


**Entități de planificare**

API-urile de planificare a proiectului oferă posibilitatea de a efectua operațiuni de creare, actualizare și ștergere pentru **Planificarea entităților**. Aceste entități sunt gestionate prin intermediul motorului de planificare în Proiect pentru web. Creați, actualizați și ștergeți operațiuni cu **Entități de planificare** au fost restricționate în versiuni mai timpurii ale Dynamics 365 Project Operations.

Următorul tabel oferă o listă completă a entităților de planificare a proiectului.

| **Nume de entitate**         | **Numele logic al entității**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Activitate de proiect            | msdyn_projecttask           |
| Dependență de activitate proiect | msdyn_projecttaskdependency |
| Atribuire de resurse     | msdyn_resourceassignment    |
| Pachet de proiect          | msdyn_projectbucket         |
| Membru echipă de proiect     | msdyn_projectteam           |
| Liste de verificare proiect      | msdyn_projectchecklist      |
| Etichetă proiect           | msdyn_projectlabel          |
| Sarcină de proiect de etichetat   | msdyn_projecttasktolabel    |
| Sprint proiect          | msdyn_projectsprint         |

**OperationSet**

OperationSet este un model de unitate de lucru care poate fi utilizat atunci când mai multe cereri care afectează planificarea trebuie procesate în cadrul unei tranzacții.

**API planificări de proiect**

În continuare este o listă a API-urilor curente de planificare a proiectului.

| **API**                                 | Descriere                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Acest API este folosit pentru a crea un proiect. Proiectul și pachetul de proiect implicit sunt create imediat.                         |
| **msdyn_CreateTeamMemberV1**            | Acest API este folosit pentru a crea un membru al echipei de proiect. Înregistrarea membrilor echipei este creată imediat.                                  |
| **msdyn_CreateOperationSetV1**          | Acest API este folosit pentru a programa mai multe solicitări care trebuie efectuate în cadrul unei tranzacții.                                        |
| **msdyn_PssCreateV1**                   | Acest API este folosit pentru a crea o entitate. Entitatea poate fi oricare dintre entitățile de planificare a proiectului care susțin operațiunea de creare. |
| **msdyn_PssUpdateV1**                   | Acest API este folosit pentru a actualiza o entitate. Entitatea poate fi oricare dintre entitățile de planificare a proiectului care susțin operațiunea de actualizare  |
| **msdyn_PssDeleteV1**                   | Acest API este folosit pentru a șterge o entitate. Entitatea poate fi oricare dintre entitățile de planificare a proiectului care susțin operațiunea de ștergere. |
| **msdyn_ExecuteOperationSetV1**         | Acest API este utilizat pentru a executa toate operațiunile din cadrul setului de operații date.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Acest API este utilizat pentru a actualiza un contur de lucru planificat al Atribuirii resurselor.                                                        |



**Utilizarea API-urilor de planificare a proiectelor cu OperationSet**

Pentru că înregistrează cu amândouă **CreateProjectV1** și **CreateTeamMemberV1** sunt create imediat, aceste API-uri nu pot fi utilizate în **OperationSet** direct. Cu toate acestea, puteți utiliza API-ul pentru a crea înregistrări necesare, pentru a crea un **OperationSet**, și apoi utilizați aceste înregistrări pre-create în **OperationSet**.

**Operațiuni acceptate**

| **Entitate de planificare**   | **Creați** | **Actualizați** | **Delete** | **Considerații importante**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Activitate de proiect            | Da        | Da        | Da        | Câmpurile **Progres**, **EffortCompleted** și **EffortRemaining** pot fi editate în Project for the Web, dar nu pot fi editate în Project Operations.                                                                                                                                                                                             |
| Dependență de activitate proiect | Da        | No         | Da        | Înregistrările de dependență ale sarcinii de proiect nu sunt actualizate. În schimb, o înregistrare veche poate fi ștearsă și o nouă înregistrare poate fi creată.                                                                                                                                                                                                                                 |
| Atribuire de resurse     | Da        | Da\*      | Da        | Operațiile cu următoarele câmpuri nu sunt acceptate: **BookableResourceID**, **Efort**, **EfortCompletat**, **EfortRămânând**, și **PlannedWork**. Înregistrările de alocare a resurselor nu sunt actualizate. În schimb, înregistrarea veche poate fi ștearsă și o nouă înregistrare poate fi creată. A fost furnizat un API separat pentru a actualiza contururile de atribuire a resurselor. |
| Pachet de proiect          | Da        | Da        | Da        | Pachetul implicit este creat prin utilizarea API-ului **CreateProjectV1**. Asistența pentru crearea și ștergerea pachetelor de proiecte a fost adăugată în Actualizarea Versiunea 16.                                                                                                                                                                                                   |
| Membru echipă de proiect     | Da        | Da        | Da        | Pentru operația de creare, utilizați API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Da        | Da        |            | Operațiunile cu următoarele câmpuri nu sunt acceptate: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Efort**, **EfortCompletat**, **EfortRămânând**, **Progres**, **Finalizare**, **TaskEarliestStart** și **Durată**.                                                                                       |
| Liste de verificare proiect      | Da        | Da        | Da        |                                                                                                                                                                                                                                                                                                                                                         |
| Etichetă proiect           | No         | Da        | No         | Numele etichetelor pot fi schimbate. Această caracteristică este disponibilă numai pentru Project for the Web                                                                                                                                                                                                                                                                      |
| Sarcină de proiect de etichetat   | Da        | No         | Da        | Această caracteristică este disponibilă numai pentru Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint proiect          | Da        | Da        | Da        | Câmpul **Începere** trebuie să aibă o dată anterioară celei din câmpul **Finalizare**. Etapele rapide pentru același proiect nu se pot suprapune. Această caracteristică este disponibilă numai pentru Project for the Web                                                                                                                                                                    |




Proprietatea ID este opțională. Dacă este furnizat, sistemul încearcă să-l folosească și aruncă o excepție dacă nu poate fi folosit. Dacă nu este furnizat, sistemul îl va genera.

**Limitări și probleme cunoscute**

Următoarea este o listă de limitări și probleme cunoscute:

-   API-urile de planificare a proiectelor pot fi utilizate numai de **Utilizatori cu licență Microsoft Project**. Nu pot fi utilizate de:
    -   Utilizatori aplicație
    -   Utilizatori de sistem
    -   Utilizatori de integrare
    -   Alți utilizatori care nu au licența necesară
-   Fiecare **OperationSet** poate efectua doar maximum 100 de operații.
-   Fiecare utilizator poate avea doar un maximum de 10 **OperationSets**.
-   Project Operations acceptă în prezent maximum 500 de sarcini totale pe un proiect.
-   Fiecare operațiune de actualizare a conturului alocării resurselor se consideră ca o singură operațiune.
-   Fiecare listă de contururi actualizate poate conține maximum 100 de secțiuni de timp.
-   **OperationSet** starea de eroare și jurnalele de erori nu sunt disponibile momentan.
-   Există maximum 400 de etape rapide per proiect.
-   [Limite și restricții pentru proiecte și sarcini](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   În prezent, etichetele sunt disponibile numai pentru Project for the Web.

**Eroare de tratare**

-   Pentru a revizui erorile generate din seturile de operații, accesați **Setări** \> **Integrarea planificării** \> **Seturi de operații**.
-   Pentru a examina erorile generate de serviciul de planificare a proiectului, accesați **Setări** \> **Integrarea programului** \> **Jurnalele de erori PSS**.

**Editarea contururilor de atribuire a resurselor**

Spre deosebire de toate celelalte API-uri de planificare a proiectelor care actualizează o entitate, API-ul de contur de alocare a resurselor este singurul responsabil pentru actualizările unui singur câmp, msdyn_plannedwork, pe o singură entitate, msydn_resourceassignment.

Modul de programare dat este:

-   **unități fixe**
-   Calendarul proiectului este 9-5p este 9-5pst, Luni, Marți, Joi, Vineri (Fără LUCRU MIERCURI)
-   iar calendarul de resurse este 9-1p PST de Luni până Vineri

Această sarcină este de o săptămână, patru ore pe zi. Acest lucru se datorează faptului că calendarul de resurse este de la 9-1 PST, sau patru ore pe zi.

| &nbsp;     | Activitate | Data inițială | Data de sfârșit  | Cantitate | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 muncitor |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

De exemplu, dacă doriți ca lucrătorul să lucreze doar trei ore în fiecare zi în această săptămână și să acorde o oră pentru alte sarcini.

#### <a name="updatedcontours-sample-payload"></a>Eșantion de sarcină UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Aceasta este atribuirea după rularea API-ului Update Contour Schedule.

| &nbsp;     | Activitate | Data inițială | Data de sfârșit  | Cantitate | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 muncitor | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Eșantion de scenariu**

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

** Eșantioane suplimentare

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
