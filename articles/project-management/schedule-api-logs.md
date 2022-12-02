---
title: Jurnalele de planificare a proiectelor
description: Acest articol oferă informații și exemple care vă vor ajuta să utilizați Jurnalele de planificare a proiectelor pentru a urmări eșecurile care sunt legate de Serviciul de planificare a proiectelor și API-urile de planificare a proiectelor.
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

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stoc, implementare Lite – de la ofertă până la factura proformă_, _Project for the web_

Microsoft Dynamics 365 Project Operations utilizează [Project for the web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) ca motor principal de planificare. În loc să utilizați interfețele de programare a aplicațiilor web (API) standard Microsoft Dataverse, Project Operations utilizează noile API-uri de planificare a proiectelor pentru a crea, a actualiza și a șterge sarcini de proiect, alocări de resurse, dependențe de sarcini, tranșe de proiect și membri ai echipelor de proiect. Cu toate acestea, atunci când operațiunile de creare, actualizare sau ștergere sunt executate în mod programatic pe entități WBS (work breakdown structure), pot apărea erori. Pentru a urmări aceste erori și istoricul operațiunilor, au fost implementate două noi jurnale administrative: **Set de operațunii** și **Serviciul de planificare a proiectelor (PSS)**. Pentru a accesa aceste jurnale, accesați **Setări** \> **Integrare program**.

Următoarea ilustrație prezintă modelul de date pentru Jurnalele de planificare a proiectului.

![Model de date pentru Jurnalele de planificare a proiectului.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Configurare Set de operațiuni

Jurnalul setului de operațiuni urmărește execuția unui set de operațiuni care este utilizat pentru a rula una sau mai multe operațiuni de creare, actualizare sau ștergere într-un lot pe proiecte, sarcini de proiect, alocări de resurse, dependențe de sarcini, compartimente de proiect sau membri ai echipei de proiect. Câmpul **Operațiune în stare** arată starea generală a setului de operațiuni. Detaliile încărcăturii utile setului de operațiuni sunt capturate în înregistrările aferente setului de operațiuni.

### <a name="operation-set"></a>Set de operațiuni

Următorul tabel arată câmpurile care sunt legate de entitatea **Set de operațiuni**.

| Nume schemă            | Descriere                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Data/ora la care setarea operațiunii a fost finalizată sau a eșuat.                                                | CompletedOn            |
| msdyn_correlationid   | Valoarea **correlationId** a solicitării.                                                                  | ID corelare          |
| msdyn_description     | Descrierea setului de operațiuni.                                                                        | Descriere            |
| msdyn_executedon      | Data/ora la care a fost rulată înregistrarea.                                                                       | Executată pe            |
| msdyn_operationsetId  | Identificatorul unic al instanțelor de entitate.                                                                   | OperationSet           |
| msdyn_Project         | Proiectul care are legătură cu setul de operațiuni.                                                            | Project                |
| msdyn_projectid       | Valoarea **projectId** a solicitării.                                                                      | ProjectId (perimat) |
| msdyn_projectName     | Nu se aplică.                                                                                              | Nu se aplică         |
| msdyn_PSSErrorLog     | Identificatorul unic al jurnalului de erori al Serviciului de planificare a proiectelor asociat setului de operațiuni. | Jurnal de erori PSS          |
| msdyn_PSSErrorLogName | Nu se aplică.                                                                                              | Nu se aplică         |
| msdyn_status          | Starea setului de operațiuni.                                                                             | Status                 |
| msdyn_statusName      | Nu se aplică.                                                                                              | Nu se aplică         |
| msdyn_useraadid       | ID-ul obiectului Azure Active Directory (Azure AD) al utilizatorului căruia îi aparține această solicitare.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detaliul setului de operațiuni

Următorul tabel arată câmpurile care sunt legate de entitatea **Detaliu set de operațiuni**.

| Nume schemă                 | Descriere                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Câmpurile serializate Dataverse pentru solicitare.                                            | CdsPayload            |
| msdyn_entityname           | Numele entității pentru solicitare.                                                     | EntityName            |
| msdyn_httpverb             | Metoda solicitării.                                                                         | HTTPVerb (perimat) |
| msdyn_httpverbName         | Nu se aplică.                                                                             | Nu se aplică        |
| msdyn_operationset         | Identificatorul unic al setului de operațiuni căruia îi aparține înregistrarea.                      | OperationSet          |
| msdyn_operationsetdetailId | Identificatorul unic al instanțelor de entitate.                                                  | Detaliu OperationSet   |
| msdyn_operationsetName     | Nu se aplică.                                                                             | Nu se aplică        |
| msdyn_operationtype        | Tipul de operațiune al setului de operațiuni.                                             | Tipul operațiunii         |
| msdyn_operationtypeName    | Nu se aplică.                                                                             | Nu se aplică        |
| msdyn_psspayload           | Câmpurile serializate ale Serviciului de planificare a proiectelor pentru solicitare.                           | PssPayload            |
| msdyn_recordid             | Identificatorul principal al înregistrării de solicitare.                                                       | ID înregistrare             |
| msdyn_requestnumber        | Un număr generat automat care identifică ordinea în care au fost primite solicitările. | Număr solicitare        |

## <a name="project-scheduling-service-error-logs"></a>Jurnalele de erori ale Serviciului de planificare a proiectelor

Jurnalele de erori ale Serviciului de planificare a proiectelor captează eșecurile care apar atunci când Serviciul de planificare a proiectelor încearcă o operațiune de **Salvare** sau **Deschidere**. Există trei scenarii acceptate în care sunt generate aceste jurnale:

- Acțiunile inițiate de utilizator eșuează critic (de exemplu, o atribuire nu poate fi creată din cauza privilegiilor lipsă).
- Serviciul de planificare a proiectelor nu poate crea, actualiza, șterge sau efectua orice altă operațiune în cascadă pe o entitate în mod programatic.
- Utilizatorul întâmpină erori atunci când o înregistrare nu se deschide (de exemplu, când un proiect este deschis sau informațiile unui membru al echipei sunt actualizate).

### <a name="project-scheduling-service-log"></a>Jurnalul Serviciului de planificare a proiectului

Următorul tabel arată câmpurile care sunt inclusse în secțiunea Jurnalul Serviciului de planificare a proiectului.

| Nume schemă          | Descriere                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Stiva de apeluri a excepției.                                               | Stivă de apeluri     |
| msdyn_correlationid | ID-ul de corelare a erorii.                                               | ID corelare  |
| msdyn_errorcode     | Un câmp care este folosit pentru a stoca codul de eroare Dataverse sau codul de eroare HTTP. | Cod de eroare     |
| msdyn_HelpLink      | Un link către documentația publică de ajutor.                                       | Link de ajutor      |
| msdyn_log           | Jurnalul de la Serviciul de planificare a proiectelor.                                   | Jurnal            |
| msdyn_project       | Un proiect care este asociat jurnalului de erori.                             | Project        |
| msdyn_projectName   | Numele proiectului dacă sarcina utilă a setului de operațiuni va fi menținută. | Nu se aplică |
| msdyn_psserrorlogId | Identificatorul unic al instanțelor de entitate.                                     | Jurnal de erori PSS  |
| msdyn_SessionId     | ID-ul sesiunii de proiect.                                                        | ID-ul sesiunii     |

## <a name="error-log-cleanup"></a>Curățarea jurnalului de erori

În mod implicit, atât jurnalele de eroare ale Serviciului de planificare a proiectelor, cât și jurnalul Setului de operațiuni pot fi curățate la fiecare 90 de zile. Orice înregistrări care sunt mai vechi de 90 de zile vor fi șterse. Cu toate acestea, prin modificarea valorii câmpului **msdyn_StateOperationSetAge** de pe pagina **Parametri proiect**, administratorii pot ajusta intervalul de curățare astfel încât să fie între 1 și 120 de zile. Sunt disponibile mai multe metode pentru modificarea acestei valori:

- Personalizați entitatea **Parametru proiect** prin crearea unei pagini personalizate și adăugarea câmpului **Setare vechime operațiuni vechi**.
- Utilizați codul client care utilizează [Kitul de dezvoltare software WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Utilizați codul Service SDK care utilizează metoda Xrm SDK **updateRecord** (referință API client) în aplicațiile bazate pe model. Power Apps include o descriere și parametrii acceptați pentru metoda **updateRecord**.

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
