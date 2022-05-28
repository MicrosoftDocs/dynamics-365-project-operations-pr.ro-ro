---
title: Utilizați API-urile de planificare a proiectului cu Power Automate
description: Acest subiect oferă un eșantion de flux care utilizează interfețele de programare a aplicației (API-uri) pentru planificarea proiectului.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597721"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Utilizați API-urile de planificare a proiectului cu Power Automate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Acest subiect descrie un exemplu de flux care arată cum să creați un plan complet de proiect utilizând Microsoft Power Automate, cum să creați un set de operații și cum să actualizați o entitate. Exemplul demonstrează cum să creați un proiect, un membru al echipei de proiect, seturi de operații, sarcini de proiect și alocații de resurse. Acest subiect explică, de asemenea, cum să actualizați o entitate și să executați un set de operații.

Următoarea este o listă completă a pașilor care sunt documentați în fluxul de probă din acest subiect:

1. [Creeaza o PowerApps declanșatorul](#1)
2. [Creați un proiect](#2)
3. [Inițializați o variabilă pentru membrul echipei](#3)
4. [Creați un membru generic al echipei](#4)
5. [Creați un set de operații](#5)
6. [Creați o găleată de proiect](#6)
7. [Inițializați o variabilă pentru starea conexiunii](#7)
8. [Inițializați o variabilă pentru numărul de sarcini](#8)
9. [Inițializați o variabilă pentru ID-ul sarcinii de proiect](#9)
10. [Faceți până când](#10)
11. [Stabiliți o sarcină de proiect](#11)
12. [Creați o sarcină de proiect](#12)
13. [Creați o atribuire de resurse](#13)
14. [Decrementează o variabilă](#14)
15. [Redenumiți o sarcină de proiect](#15)
16. [Rulați un set de operații](#16)

## <a name="assumptions"></a>Ipoteze

Acest subiect presupune că aveți cunoștințe de bază despre Dataverse platforma, fluxurile de cloud și interfața de programare a aplicației (API) pentru planificarea proiectului. Pentru mai multe informații, consultați [Referințe](#references) secțiunea mai târziu în acest subiect.

## <a name="create-a-flow"></a>Creați un flux

### <a name="select-an-environment"></a>Selectați un mediu

Puteți crea Power Automate curge în mediul dumneavoastră.

1. Mergi la<https://flow.microsoft.com> și utilizați acreditările de administrator pentru a vă conecta.
2. În colțul din dreapta sus, selectați **Medii**.
3. În listă, selectați mediul în care Dynamics 365 Project Operations este instalat.

### <a name="create-a-solution"></a>Creați o soluție

Urmați acești pași pentru a crea un [flux conștient de soluție](/power-automate/overview-solution-flows). Prin crearea unui flux conștient de soluție, puteți exporta mai ușor fluxul pentru a-l utiliza mai târziu.

1. În panoul de navigare, selectați **Soluții**.
2. Pe **Soluții** pagina, selectați **Soluție nouă**.
3. În **Soluție nouă** caseta de dialog, setați câmpurile necesare, apoi selectați **Crea**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Pasul 1: Creați un PowerApps declanșatorul

1. Pe **Soluții** pagina, selectați soluția pe care ați creat-o, apoi selectați **Nou**.
2. În panoul din stânga, selectați **Norii curg** \> **Automatizare** \> **Fluxul de nor** \> **instant**.
3. În **Nume flux** câmp, introduceți **Programați fluxul demonstrativ API**.
4. În **Alegeți cum să declanșați acest flux** listă, selectați **Power Apps**. Când creați un Power Apps declanșatorul, logica depinde de tine în calitate de autor. În acest subiect, lăsați parametrii de intrare necompleți în scopuri de testare.
5. Selectați **Creare**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Pasul 2: Creați un proiect

Urmați acești pași pentru a crea un proiect exemplu.

1. În fluxul pe care l-ați creat, selectați **Pas nou**.

    ![Adăugarea unui nou pas.](media/newstep.png)

2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.

    ![Selectarea unei operații.](media/chooseactiontab.png)

3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.

![Redenumirea unui pas.](media/renamestep.png)

4. Redenumiți pasul **Creați proiect**.
5. În **Numele acțiunii** câmp, selectați **msdyn\_ CreateProjectV1**.
6. Sub **msdyn\_ subiect** câmp, selectați **Adăugați conținut dinamic**.
7. Pe **Expresie** fila, în câmpul funcție, introduceți **Numele proiectului - utcNow()**.
8. Selectați **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Pasul 3: Inițializați o variabilă pentru membrul echipei

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **inițializați variabila**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Membru al echipei Init**.
5. În **Nume** câmp, introduceți **TeamMemberAction**.
6. În **Tip** câmp, selectați **Şir**.
7. În **Valoare** câmp, introduceți **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Pasul 4: Creați un membru generic al echipei

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creați membru al echipei**.
5. Pentru **Numele acțiunii** câmp, selectați **TeamMemberAction** în **Conținut dinamic** căsuță de dialog.
6. În **Parametrii de acțiune** câmp, introduceți următoarele informații despre parametri.

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

    - **\@\@ odata.type** – Numele entității. De exemplu, introduceți **„Microsoft.Dynamics.CRM.msdyn\_ echipă de proiect"**.
    - **msdyn\_ projectteamid** – Cheia primară a ID-ului echipei de proiect. Valoarea este o expresie de identificare unică globală (GUID).   ID-ul este generat din fila expresie.

    - **msdyn\_ proiect\@ odata.bind** – ID-ul proiectului al proiectului proprietar. Valoarea va fi conținutul dinamic care provine din răspunsul pasului „Creează proiect”. Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Sunt necesare ghilimele. De exemplu, introduceți **„/msdyn\_ proiecte(ADĂUGAȚI CONȚINUT DINAMIC)"**.
    - **msdyn\_ Nume** – Numele membrului echipei. De exemplu, introduceți **„ScheduleAPIDemoTM1”**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Pasul 5: Creați un set de operații

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creați un set de operații**.
5. În **Numele acțiunii** câmp, selectați **msdyn\_ CreateOperationSetV1** Dataverse acțiune personalizată.
6. În **Descriere** câmp, introduceți **ScheduleAPIDemoOperationSet**.
7. În **Proiect** câmp, introduceți **/msdyn\_ proiecte(**.
8. În **Conținut dinamic** caseta de dialog, selectați **msdyn\_ CreateProjectV1Response ProjectId**.
9. În **Proiect** câmp, introduceți **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Pasul 6: Creați o găleată de proiect

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **adăugați un rând nou**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creați o găleată**.
5. În **Nume tabel** câmp, selectați **Găleți de proiect**.
6. În **Nume** câmp, introduceți **ScheduleAPIDemoBucket1**.
7. Pentru **Proiect** câmp, selectați **msdyn\_ CreateProjectV1Response ProjectId** în **Conținut dinamic** căsuță de dialog.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Pasul 7: Inițializați o variabilă pentru starea conexiunii

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **inițializați variabila**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Inițiază starea linkului**.
5. În **Nume** câmp, introduceți **linkstatus**.
6. În **Tip** câmp, selectați **Întreg**.
7. În **Valoare** câmp, introduceți **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Pasul 8: Inițializați o variabilă pentru numărul de sarcini

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **inițializați variabila**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Init Număr de sarcini**.
5. În **Nume** câmp, introduceți **număr de sarcini**.
6. În **Tip** câmp, selectați **Întreg**.
7. În **Valoare** câmp, introduceți **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Pasul 9: Inițializați o variabilă pentru ID-ul sarcinii de proiect

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **inițializați variabila**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Init ProjectTaskID**.
5. În **Nume** câmp, introduceți **număr de sarcini**.
6. În **Tip** câmp, selectați **Şir**.
7. Pentru **Valoare** câmp, introduceți **ghid()** în constructorul de expresii.

## <a name="step-10-do-until"></a><a id="10"></a> Pasul 10: Faceți până când

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **face până când**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. Setați prima valoare din instrucțiunea condiționată la **număr de sarcini** variabilă din **Conținut dinamic** căsuță de dialog.
4. Setați condiția la **mai mic decât egal cu**.
5. Setați a doua valoare din instrucțiunea condiționată la **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Pasul 11: Setați o sarcină de proiect

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **setați variabila**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Setați sarcina proiectului**.
5. În **Nume** câmp, selectați **msdyn\_ projecttaskid**.
6. Pentru **Valoare** câmp, introduceți **ghid()** în constructorul de expresii.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Pasul 12: Creați o sarcină de proiect

Urmați acești pași pentru a crea o sarcină de proiect care are un ID unic care aparține proiectului curent și compartimentului de proiect pe care l-ați creat.

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creați sarcină de proiect**.
5. În **Numele acțiunii** câmp, selectați **msdyn\_ PssCreateV1**.
6. În **Entitate** câmp, introduceți următoarele informații despre parametri.

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

    - **\@\@ odata.type** – Numele entității. De exemplu, introduceți **„Microsoft.Dynamics.CRM.msdyn\_ sarcina proiectului"**.
    - **msdyn\_ projecttaskid** – ID-ul unic al sarcinii. Valoarea ar trebui să fie setată la o variabilă dinamică de la **msdyn\_ projecttaskid**.
    - **msdyn\_ proiect\@ odata.bind** – ID-ul proiectului al proiectului proprietar. Valoarea va fi conținutul dinamic care provine din răspunsul pasului „Creează proiect”. Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Sunt necesare ghilimele. De exemplu, introduceți **„/msdyn\_ proiecte(ADĂUGAȚI CONȚINUT DINAMIC)"**.
    - **msdyn\_ subiect** – Orice nume de sarcină.
    - **msdyn\_ projectbucket\@ odata.bind** – Bucket-ul de proiect care conține sarcinile. Valoarea va fi conținutul dinamic care provine din răspunsul la pasul „Creare bucket”. Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Sunt necesare ghilimele. De exemplu, introduceți **„/msdyn\_ projectbuckets(ADĂUGAȚI CONȚINUT DINAMIC)"**.
    - **msdyn\_ start** – Conținut dinamic pentru data de începere. De exemplu, mâine va fi reprezentat ca **„addDays(utcNow(), 1)”**.
    - **msdyn\_ pornire programată** – Data de începere programată. De exemplu, mâine va fi reprezentat ca **„addDays(utcNow(), 1)”**.
    - **msdyn\_ sfârşitul programului** – Data de încheiere programată. Selectați o dată în viitor. De exemplu, specificați **„addDays(utcNow(), 5)”**.
    - **msdyn\_ LinkStatus** – Starea legăturii. De exemplu, introduceți **„192350000”**.

7. Pentru **OperationSetId** câmp, selectați **msdyn\_ CreateOperationSetV1Response** în **Conținut dinamic** căsuță de dialog.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Pasul 13: Creați o atribuire de resurse

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creați o sarcină**.
5. În **Numele acțiunii** câmp, selectați **msdyn\_ PssCreateV1**.
6. În **Entitate** câmp, introduceți următoarele informații despre parametri.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Pentru **OperationSetId** câmp, selectați **msdyn\_ CreateOperationSetV1Response** în **Conținut dinamic** căsuță de dialog.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Pasul 14: Decrementați o variabilă

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **variabila de decrementare**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În **Nume** câmp, selectați **număr de sarcini**.
4. În **Valoare** câmp, introduceți **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Pasul 15: Redenumiți o sarcină de proiect

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Redenumiți sarcina proiectului**.
5. În **Numele acțiunii** câmp, selectați **msdyn\_ PssUpdateV1**.
6. În **Entitate** câmp, introduceți următoarele informații despre parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Pentru **OperationSetId** câmp, selectați **msdyn\_ CreateOperationSetV1Response** în **Conținut dinamic** căsuță de dialog.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Pasul 16: Rulați un set de operații

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Executați setul de operații**.
5. În **Numele acțiunii** câmp, selectați **msdyn\_ ExecuteOperationSetV1**.
6. Pentru **OperationSetId** câmp, selectați **msdyn\_ CreateOperationSetV1Response OperationSetId** în **Conținut dinamic** căsuță de dialog.

## <a name="references"></a>Referințe

- [Prezentare generală a modului de integrare a fluxurilor cu Dataverse -Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare](schedule-api-preview.md)
- [Privire de ansamblu asupra fluxurilor de nor -Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Prezentare generală a fluxurilor conștiente de soluții -Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
