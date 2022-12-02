---
title: Utilizarea API-urilor de planificare a proiectelor cu Power Automate
description: Acest articol oferă un exemplu de flux care utilizează interfețele de programare a aplicației (API-uri) pentru planificarea proiectului.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404462"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Utilizarea API-urilor de planificare a proiectelor cu Power Automate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest articol descrie un exemplu de flux care arată cum să creați un plan complet de proiect utilizând Microsoft Power Automate, cum să creați un Set de operațiuni și cum să actualizați o entitate. Exemplul demonstrează cum să creați un proiect, un membru al echipei de proiect, Seturi de operații, sarcini de proiect și alocări de resurse. Acest articol explică, de asemenea, cum să actualizați o entitate și să executați un Set de operațiuni.

Următoarea este o listă completă a pașilor care sunt documentați în fluxul de exemple din acest articol:

1. [Creați un declanșator PowerApps](#1)
2. [Creați un proiect](#2)
3. [Inițializați o variabilă pentru membrul echipei](#3)
4. [Creați un membru de echipă generic](#4)
5. [Creați un Set de operațiuni](#5)
6. [Creați unei pachet de proiect](#6)
7. [Inițializați o variabilă pentru starea linkului](#7)
8. [Inițializați o variabilă pentru numărul de sarcini](#8)
9. [Inițializați o variabilă pentru ID-ul sarcinii de proiect](#9)
10. [Faceți până când](#10)
11. [Stabiliți o sarcină de proiect](#11)
12. [Creați o sarcină de proiect](#12)
13. [Creați o atribuire de resurse](#13)
14. [Decrementați o variabilă](#14)
15. [Redenumiți o sarcină](#15)
16. [Rulați un Set de operațiuni](#16)

## <a name="assumptions"></a>Ipoteze

Acest articol presupune că aveți cunoștințe de bază despre platforma Dataverse, fluxurile de cloud și interfața de programare a aplicației (API) Project Schedule. Pentru mai multe informații, consultați secțiunea [Referințe](#references) care va urma în acest articol.

## <a name="create-a-flow"></a>Creați un flux

### <a name="select-an-environment"></a>Selectați un mediu

Puteți crea fluxul Power Automate în mediul dvs.

1. Accesați <https://flow.microsoft.com> și utilizați-vă acreditările de administrator pentru a vă conecta.
2. În colțul din dreapta sus, selectați **Medii.**.
3. În listă, selectați mediul unde este instalat Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Creați o soluție

Urmați acești pași pentru a crea un [un flux receptiv la soluție](/power-automate/overview-solution-flows). Prin crearea unui flux receptiv la soluție, puteți exporta mai ușor fluxul pentru a-l utiliza mai târziu.

1. În panoul de navigare, selectați **Soluții**.
2. Pe pagina **Soluții**, selectați **Soluție nouă**.
3. În caseta de dialog **Soluție nouă**, setați câmpurile necesare, apoi selectați **Creare**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Etapa 1: Creați un declanșator PowerApps

1. Pe pagina **Soluție nouă**, selectați soluția pe care ați creat-o și apoi selectați **Nou**.
2. În panoul din stânga, selectați **Fluxuri Cloud** \> **Automatizare** \> **Flux Cloud** \> **Instantaneu**.
3. În câmpul **Nume flux**, introduceți **Programare flux demonstrativ API**.
4. În lista **Alegeți cum să declanșați acest flux**, selectați **Power Apps**. Când creați un declanșator Power Apps, logica depinde de dvs. în calitate de autor. În acest articol, lăsați necompleți parametrii de intrare în scopuri de testare.
5. Selectați **Creare**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Pasul 2: Creați un proiect

Urmați acești pași pentru a crea un exemplu de proiect.

1. În fluxul pe care l-ați creat, selectați **Etapă nouă**.

    ![Adăugarea unei noi etape.](media/newstep.png)

2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.

    ![Selectarea unei operațiuni.](media/chooseactiontab.png)

3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.

![Redenumirea unei etape.](media/renamestep.png)

4. Redenumiți etapa **Creare proiect**.
5. În câmpul **Nume acțiune**, selectați **msdyn\_CreateProjectV1**.
6. Sub câmpul **msdyn\_subject**, selectațiu **Adăugare conținut dinamic**.
7. Pe fila **Expresie**, în câmpul funcție, introduceți **Numele proiectului - utcNow()**.
8. Selectați **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Etapa 3: Inițializați o variabilă pentru membrul echipei

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **inițializare variabilă**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Iniț membru echipă**.
5. În câmpul **Nume**, introduceți **TeamMemberAction**.
6. În câmpul **Tip**, selectați **Șir**.
7. În câmpul **Valoare**, introduceți **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Etapa 4: Creați un membru generic al echipei de proiect

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Creare membru echipă**.
5. Pentru câmpul **Nume acțiunie**, selectați **TeamMemberAction** în caseta de dialog **Conținut dinamic**.
6. În câmpul **Parametri acțiune**, introduceți următoarele informații despre parametri.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Iată o explicație a parametrilor:

    - **\@\@odata.type** – Numele entității. De exemplu, introduceți **„Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – Cheia primară a ID-ului echipei de proiect. Valoarea este o expresie de identificare unică globală (GUID).   ID-ul este generat din fila expresie.

    - **msdyn\_project\@odata.bind** – ID-ul de proiect al proiectului proprietar. Valoarea va fi conținutul dinamic care provine din răspunsul etapei „Creare proiect”. Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Sunt necesare ghilimele. De exemplu, introduceți **„/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – Numele membrului echipei. De exemplu, introduceți **„ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Etapa 5: Creați un Set de operațiuni

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Creare Set de operațiuni**.
5. În câmpul **Nume acțiune**, selectați acțiunea personalizată **msdyn\_CreateOperationSetV1** Dataverse.
6. În câmpul **Descriere** introduceți **ScheduleAPIDemoOperationSet**.
7. În câmpul **Proiect**, introduceți **/msdyn\_projects(**.
8. În caseta de dialog **Conținut dinamic**, selectați **msdyn\_CreateProjectV1Response ProjectId**.
9. În câmpul **Proiect**, introduceți **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Etapa 6: Creați un pachet de proiect

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **adăugare câmp nou**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Creare Pachet**.
5. În câmpul **Nume tabel**, selectați **Pachete de proiect**
6. În câmpul **Nume**, introduceți **ProgramarePachetDemoAPI1**.
7. Pentru câmpul **Proiect**, selectați **msdyn\_CreateProjectV1Response ProjectId** în caseta de dialog **Conținut dinamic**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Etapa 7: Inițializați o variabilă pentru starea linkului

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **inițializare variabilă**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Iniț starelink**.
5. În câmpul **Nume**, introduceți **starelink**.
6. În câmpul **Tip**, selectați **Integer**.
7. În câmpul **Valoare**, introduceți **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Etapa 8: Inițializați o variabilă pentru numărul de sarcini

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **inițializare variabilă**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Iniț Număr de sarcini**.
5. În câmpul **Nume**, introduceți **număr de sarcini**.
6. În câmpul **Tip**, selectați **Integer**.
7. În câmpul **Valoare**, introduceți **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Etapa 9: Inițializați o variabilă pentru ID-ul sarcinii de proiect

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **inițializare variabilă**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Iniț ProjectTaskID**.
5. În câmpul **Nume**, introduceți **număr de sarcini**.
6. În câmpul **Tip**, selectați **Șir**.
7. Pentru câmpul **Valoare**, introduceți **ghid()** în generatorul de expresii.

## <a name="step-10-do-until"></a><a id="10"></a>Etapa 10: Repetare până la

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **repetare până la**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. Setați prima valoare din instrucțiunea condiționată la variabila **număr de sarcini** din caseta de dialog **Conținut dinamic**.
4. Setați condiția la **mai mic decât, egal cu**.
5. Setați a doua valoare din instrucțiunea condiționată la **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Etapa 11: Stabiliți o sarcină de proiect

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **stabilire variabilă**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În noua etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Stabilire Sarcină Proiect**.
5. În câmpul **Nume**, selectați **msdyn\_projecttaskid**.
6. Pentru câmpul **Valoare**, introduceți **ghid()** în generatorul de expresii.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Etapa 12: Creați o sarcină de proiect

Urmați acești pași pentru a crea o sarcină de proiect care are un ID unic care aparține proiectului curent și pachetului de proiect pe care l-ați creat.

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Creare Sarcină Proiect**.
5. În câmpul **Nume acțiune**, selectați **msdyn\_PssCreateV1**.
6. În câmpul **Entitate**, introduceți următoarele informații despre parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Iată o explicație a parametrilor:

    - **\@\@odata.type** – Numele entității. De exemplu, introduceți **„Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – ID-ul unic al sarcinii. Valoarea ar trebui să fie setată la o variabilă dinamică de la **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID-ul de proiect al proiectului proprietar. Valoarea va fi conținutul dinamic care provine din răspunsul etapei „Creare proiect”. Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Sunt necesare ghilimele. De exemplu, introduceți **„/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Orice nume de sarcină.
    - **msdyn\_projectbucket\@odata.bind** – Pachetul de proiect care conține sarcinile. Valoarea va fi conținutul dinamic care provine din răspunsul etapei „Creare pachet”. Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Sunt necesare ghilimele. De exemplu, introduceți **„/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Conținut dinamic pentru data de începere. De exemplu, mâine va fi reprezentat ca **„addDays(utcNow(), 1)”**.
    - **msdyn\_scheduledstart** – Data de începere planificată pentru operațiune. De exemplu, mâine va fi reprezentat ca **„addDays(utcNow(), 1)”**.
    - **msdyn\_scheduleend** – Data de încheiere programată. Selectați o dată în viitor. De exemplu, specificați **„addDays(utcNow(), 5)”**.
    - **msdyn\_LinkStatus** – Stare link. De exemplu, introduceți **„192350000"**.

7. Pentru câmpul **OperationSetId**, selectați **msdyn\_CreateOperationSetV1Response** în caseta de dialog **Conținut dinamic**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Pasul 13: Creați o atribuire de resurse

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Creare Atribuire**.
5. În câmpul **Nume acțiune**, selectați **msdyn\_PssCreateV1**.
6. În câmpul **Entitate**, introduceți următoarele informații despre parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Pentru câmpul **OperationSetId**, selectați **msdyn\_CreateOperationSetV1Response** în caseta de dialog **Conținut dinamic**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Etapa 14: Decrementați o variabilă

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **decrementare variabilă**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În câmpul **Nume**, selectați **număr de sarcini**.
4. În câmpul **Valoare**, introduceți **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Etapa 15: Redenumiți o sarcină de proiect

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Redenumire Sarcină Proiect**.
5. În câmpul **Nume acțiune**, selectați **msdyn\_PssUpdateV1**.
6. În câmpul **Entitate**, introduceți următoarele informații despre parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Pentru câmpul **OperationSetId**, selectați **msdyn\_CreateOperationSetV1Response** în caseta de dialog **Conținut dinamic**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Etapa 16: Rulați un Set de operațiuni

1. În flux, selectați **Etapă nouă**.
2. În caseta de dialog **Alegeți o operațiune**, în câmpul de căutare, introduceți **efectuare acțiune nelegată**. Apoi, pe fila **Acțiuni**, selectați operațiunea din lista de rezultate.
3. În etapă, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți etapa **Executare Set de operațiuni**.
5. În câmpul **Nume acțiune**, selectați **msdyn\_ExecuteOperationSetV1**.
6. Pentru câmpul **OperationSetId**, selectați **msdyn\_CreateOperationSetV1Response OperationSetId** în caseta de dialog **Conținut dinamic**.

## <a name="references"></a>Referințe

- [Prezentare generală a modului de integrare a fluxurilor cu Dataverse – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare](schedule-api-preview.md)
- [Privire de ansamblu asupra fluxurilor cloud – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Prezentare generală a fluxurilor receptive la soluții – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
