---
title: Jurnalele de planificare a proiectelor
description: Acest articol oferă informații și exemple care vă vor ajuta să utilizați jurnalele de planificare a proiectelor pentru a urmări eșecurile legate de serviciul de planificare a proiectelor și API-urile de planificare a proiectelor.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923710"
---
# <a name="project-scheduling-logs"></a>Jurnalele de planificare a proiectelor

_**Se aplică la:** Operațiuni de proiect pentru scenarii bazate pe resurse/non-stoc, implementare simplă - acord cu facturarea proforma_, _pentru web_

Microsoft Dynamics 365 Project Operations utilizări [Proiect pentru web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) ca motor principal de planificare. În loc să folosești standardul Microsoft Dataverse Interfețe de programare a aplicațiilor web (API), Project Operations utilizează noile API-uri de planificare a proiectelor pentru a crea, actualiza și șterge sarcini de proiect, alocații de resurse, dependențe de sarcini, compartimente de proiect și membri ai echipelor de proiect. Cu toate acestea, atunci când operațiunile de creare, actualizare sau ștergere sunt executate în mod programatic pe entități WBS (work breakdown structure), pot apărea erori. Pentru a urmări aceste erori și istoricul operațiunilor, au fost implementate două noi jurnale administrative: **Set de operații** și **Serviciul de planificare a proiectelor (PSS)**. Pentru a accesa aceste jurnale, accesați **Setări** \> **Integrarea programului**.

Următoarea ilustrație arată modelul de date pentru jurnalele de planificare a proiectului.

![Model de date pentru jurnalele de planificare a proiectului.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Jurnalul de setări operațiuni

Jurnalul setului de operații urmărește execuția unui set de operațiuni care este utilizat pentru a rula una sau mai multe operațiuni de creare, actualizare sau ștergere într-un lot pentru proiecte, sarcini de proiect, alocații de resurse, dependențe de sarcini, compartimente de proiect sau membri ai echipei de proiect. The **Operațiune în stare** câmpul arată starea generală a setului de operațiuni. Detaliile privind sarcina utilă a setului de operații sunt capturate în înregistrările aferente setului de operațiuni.

### <a name="operation-set"></a>Set de operații

Următorul tabel prezintă câmpurile care sunt legate de **Set de operații** entitate.

| SchemaName            | Descriere                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Data/ora la care setarea operațiunii a fost finalizată sau a eșuat.                                                | CompletedOn            |
| msdyn_corelationid   | The **corelationId** valoarea cererii.                                                                  | ID corelare          |
| msdyn_description     | Descrierea setului de operațiuni.                                                                        | Descriere            |
| msdyn_executedon      | Data/ora la care a fost efectuată înregistrarea.                                                                       | Executată pe            |
| msdyn_operationsetId  | Identificatorul unic al instanțelor de entitate.                                                                   | OperationSet           |
| msdyn_Project         | Proiectul care are legătură cu setul de operațiuni.                                                            | Project                |
| msdyn_projectid       | The **projectId** valoarea cererii.                                                                      | ProjectId (perimat) |
| msdyn_projectName     | Nu se aplică.                                                                                              | Nu se aplică         |
| msdyn_PSSErrorLog     | Identificatorul unic al jurnalului de erori Project Scheduling Service care este asociat cu setul de operațiuni. | Jurnal de erori PSS          |
| msdyn_PSSErrorLogName | Nu se aplică.                                                                                              | Nu se aplică         |
| msdyn_status          | Starea setului de operațiuni.                                                                             | Status                 |
| msdyn_statusName      | Nu se aplică.                                                                                              | Nu se aplică         |
| msdyn_useraadid       | The Azure Active Directory (Azure AD) ID-ul obiectului utilizatorului căruia îi aparține cererea.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detaliu set de operațiuni

Următorul tabel prezintă câmpurile care sunt legate de **Detaliu set de operațiuni** entitate.

| SchemaName                 | Descriere                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializat Dataverse câmpurile pentru cerere.                                            | CdsPayload            |
| msdyn_entityname           | Numele entității pentru cerere.                                                     | EntityName            |
| msdyn_httpverb             | Metoda de solicitare.                                                                         | HTTPVerb (perimat) |
| msdyn_httpverbName         | Nu se aplică.                                                                             | Nu se aplică        |
| msdyn_operationset         | Identificatorul unic al setului de operații căruia îi aparține înregistrarea.                      | OperationSet          |
| msdyn_operationsetdetailId | Identificatorul unic al instanțelor de entitate.                                                  | Detaliu OperationSet   |
| msdyn_operationsetName     | Nu se aplică.                                                                             | Nu se aplică        |
| msdyn_operationtype        | Tipul de operație al setului de operațiuni.                                             | Tipul operațiunii         |
| msdyn_operationtypeName    | Nu se aplică.                                                                             | Nu se aplică        |
| msdyn_psspayload           | Câmpurile serializate ale serviciului de planificare a proiectelor pentru cerere.                           | PssPayload            |
| msdyn_recordid             | Identificatorul înregistrării cererii.                                                       | ID înregistrare             |
| msdyn_requestnumber        | Un număr generat automat care identifică ordinea în care au fost primite cererile. | Număr solicitare        |

## <a name="project-scheduling-service-error-logs"></a>Jurnalele de erori ale Serviciului de planificare a proiectelor

Jurnalele de eroare ale Serviciului de planificare a proiectelor captează eșecurile care apar atunci când Serviciul de planificare a proiectelor încearcă a **Salvați** sau **Deschis** Operațiune. Există trei scenarii acceptate în care aceste jurnale sunt generate:

- Acțiunile inițiate de utilizator eșuează critic (de exemplu, o atribuire nu poate fi creată din cauza privilegiilor lipsă).
- Serviciul de planificare a proiectelor nu poate crea, actualiza, șterge sau efectua orice altă operațiune în cascadă pe o entitate în mod programatic.
- Utilizatorul se confruntă cu erori atunci când o înregistrare nu se deschide (de exemplu, când un proiect este deschis sau informațiile unui membru al echipei sunt actualizate).

### <a name="project-scheduling-service-log"></a>Jurnalul serviciului de planificare a proiectelor

Următorul tabel arată câmpurile care sunt incluse în jurnalul Serviciului de planificare a proiectelor.

| SchemaName          | Descriere                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stiva de apeluri a excepției.                                               | Stivă de apeluri     |
| msdyn_corelationid | ID-ul de corelare al erorii.                                               | ID corelare  |
| msdyn_errorcode     | Un câmp care este folosit pentru a stoca Dataverse codul de eroare sau codul de eroare HTTP. | Cod de eroare     |
| msdyn_HelpLink      | Un link către documentația publică de ajutor.                                       | Link de ajutor      |
| msdyn_log           | Jurnalul de la Serviciul de planificare a proiectelor.                                   | Jurnal            |
| msdyn_project       | Proiectul care este asociat cu jurnalul de erori.                             | Project        |
| msdyn_projectName   | Numele proiectului dacă sarcina utilă a setului de operațiuni va fi persistată. | Nu se aplică |
| msdyn_psserrorlogId | Identificatorul unic al instanțelor de entitate.                                     | Jurnal de erori PSS  |
| msdyn_SessionId     | ID-ul sesiunii de proiect.                                                        | ID-ul sesiunii     |

## <a name="error-log-cleanup"></a>Curățarea jurnalului de erori

În mod implicit, atât jurnalele de eroare ale serviciului de planificare a proiectelor, cât și jurnalul setului de operațiuni pot fi curățate la fiecare 90 de zile. Orice înregistrări care sunt mai vechi de 90 de zile vor fi șterse. Cu toate acestea, prin modificarea valorii **msdyn_StateOperationSetAge** câmp de pe **Parametrii proiectului** pagina, administratorii pot ajusta intervalul de curățare astfel încât să fie între 1 și 120 de zile. Sunt disponibile mai multe metode pentru modificarea acestei valori:

- Personalizați **Parametrul proiectului** entitate prin crearea unei pagini personalizate și adăugarea **Stale Operations Set Age** camp.
- Utilizați codul client care utilizează [Kit de dezvoltare software WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Utilizați codul Service SDK care utilizează Xrm SDK **updateRecord** metoda (referință API client) în aplicațiile bazate pe model. Power Apps include o descriere și parametrii acceptați pentru **updateRecord** metodă.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
