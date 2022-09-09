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

Acest articol descrie un exemplu de flux care arată cum să creați un plan complet de proiect utilizând Microsoft Power Automate, cum să creați un set de operații și cum să actualizați o entitate. Exemplul demonstrează cum să creați un proiect, un membru al echipei de proiect, seturi de operații, sarcini de proiect și alocări de resurse. Acest articol explică, de asemenea, cum să actualizați o entitate și să executați un set de operații.

Următoarea este o listă completă a pașilor care sunt documentați în fluxul de probă din acest articol:

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

Acest articol presupune că aveți cunoștințe de bază despre Dataverse platforma, fluxurile de cloud și interfața de programare a aplicației (API) Project Schedule. Pentru mai multe informații, consultați [Referințe](#references) secțiunea mai târziu în acest articol.

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
2. În panoul din stânga, selectați **Norul curge** \> **Automatizare** \> **Fluxul de nor** \> **instant**.
3. În **Numele fluxului** câmp, introduceți **Programați fluxul demonstrativ API**.
4. În **Alegeți cum să declanșați acest flux** listă, selectați **Power Apps**. Când creați un Power Apps declanșatorul, logica depinde de tine în calitate de autor. În acest articol, lăsați necompleți parametrii de intrare în scopuri de testare.
5. Selectați **Creare**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Pasul 2: Creați un proiect

Urmați acești pași pentru a crea un proiect exemplu.

1. În fluxul pe care l-ați creat, selectați **Pas nou**.

    ![Adăugarea unui nou pas.](media/newstep.png)

2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.

    ![Selectarea unei operații.](media/chooseactiontab.png)

3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.

![Redenumirea unui pas.](media/renamestep.png)

4. Redenumiți pasul **Creare proiect**.
5. În câmpul **Nume** acțiune, selectați **msdyn\_ CreateProjectV1**.
6. Sub câmpul **subiect\_ msdyn**, selectați **Adăugare conținut** dinamic.
7. Pe fila **Expresie**, în câmpul funcție, introduceți **Nume proiect - utcNow()**.
8. Selectați **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Pasul 3: Inițializarea unei variabile pentru membrul echipei

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **variabila** inițializare. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Membru al** echipei Init.
5. În câmpul **Nume**, introduceți **TeamMemberAction**.
6. În câmpul **Tip**, selectați **Șir**.
7. În câmpul **Valoare**, introduceți **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Pasul 4: Creați un membru generic al echipei

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creare membru al** echipei.
5. Pentru câmpul **Nume** acțiune, selectați **TeamMemberAction** în caseta de **dialog Conținut** dinamic.
6. În câmpul Parametri **de** acțiune, introduceți următoarele informații despre parametru.

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

    - **\@\@ odata.type** – Numele entității. De exemplu, introduceți **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – Cheia principală a ID-ului echipei de proiect. Valoarea este o expresie identificator unic global (GUID).   ID-ul este generat din fila expresie.

    - **msdyn\_ project\@ odata.bind** – ID-ul proiectului care detine proiectul. Valoarea va fi conținutul dinamic care provine din răspunsul pasului "Creare proiect". Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Ghilimelele sunt necesare. De exemplu, introduceți **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ nume** – Numele membrului echipei. De exemplu, introduceți **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Pasul 5: Creați un set de operațiuni

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creare set de operațiuni**.
5. În câmpul **Nume acțiune, selectați** acțiunea particularizată msdyn **CreateOperationSetV1\_**.Dataverse
6. În câmpul **Descriere**, introduceți **ScheduleAPIDemoOperationSet**.
7. În câmpul **Proiect**, introduceți **/msdyn\_ projects(**.
8. În caseta de **dialog Conținut** dinamic, selectați **msdyn\_ CreateProjectV1Response ProjectId**.
9. În câmpul **Proiect**, introduceți **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Pasul 6: Creați o găleată de proiect

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **adăugare rând** nou. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Creare găleată**.
5. În câmpul **Nume** tabel, selectați **Găleți** proiect.
6. În câmpul **Nume**, introduceți **ScheduleAPIDemoBucket1**.
7. Pentru câmpul **Proiect**, selectați **msdyn\_ CreateProjectV1Response ProjectId** în caseta **de dialog Conținut** dinamic.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Pasul 7: Inițializarea unei variabile pentru starea link-ului

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **variabila** inițializare. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Init linkstatus**.
5. În câmpul **Nume**, introduceți **linkstatus**.
6. În câmpul **Tip**, selectați **Număr întreg**.
7. În câmpul **Valoare**, introduceți **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Pasul 8: Inițializarea unei variabile pentru numărul de activități

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **variabila** inițializare. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Init Număr de activități**.
5. În câmpul **Nume**, introduceți **numărul de activități**.
6. În câmpul **Tip**, selectați **Număr întreg**.
7. În câmpul **Valoare**, introduceți **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Pasul 9: Inițializarea unei variabile pentru ID-ul activității de proiect

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **variabila** inițializare. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Init ProjectTaskID**.
5. În câmpul **Nume**, introduceți **numărul de activități**.
6. În câmpul **Tip**, selectați **Șir**.
7. Pentru câmpul **Valoare**, introduceți **guid()** în generatorul de expresii.

## <a name="step-10-do-until"></a><a id="10"></a> Pasul 10: Faceți până când

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **do până când**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. Setați prima valoare din instrucțiunea condițională la variabila **număr de activități** din caseta **de dialog Conținut** dinamic.
4. Setați condiția la **mai puțin de egal cu**.
5. Setați a doua valoare din instrucțiunea condițională la **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Pasul 11: Setarea unei activități de proiect

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **variabila** set. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În noul pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumiți**.
4. Redenumiți pasul **Setați activitatea de proiect**.
5. În câmpul **Nume**, selectați **msdyn\_ projecttaskid**.
6. Pentru câmpul **Valoare**, introduceți **guid()** în generatorul de expresii.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Pasul 12: Crearea unei activități de proiect

Urmați acești pași pentru a crea o activitate de proiect care are un ID unic care aparține proiectului curent și găleata de proiect pe care ați creat-o.

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți pasul **Creare activitate proiect**.
5. În câmpul **Nume** acțiune, selectați **msdyn\_ PssCreateV1**.
6. În câmpul **Entitate**, introduceți următoarele informații despre parametru.

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

    - **\@\@ odata.type** – Numele entității. De exemplu, introduceți **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – ID-ul unic al sarcinii. Valoarea trebuie setată la o variabilă dinamică de la **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – ID-ul proiectului care detine proiectul. Valoarea va fi conținutul dinamic care provine din răspunsul pasului "Creare proiect". Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Ghilimelele sunt necesare. De exemplu, introduceți **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ subiect** - Orice nume de activitate.
    - **msdyn\_ projectbucket\@ odata.bind** – Găleata de proiect care conține sarcinile. Valoarea va fi conținutul dinamic care provine din răspunsul pasului "Creare găleată". Asigurați-vă că introduceți calea completă și adăugați conținut dinamic între paranteze. Ghilimelele sunt necesare. De exemplu, introduceți **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – Conținut dinamic pentru data de începere. De exemplu, mâine va fi reprezentat ca **"addDays(utcNow(), 1)".**"
    - **msdyn\_ scheduledstart** – Data programată de începere. De exemplu, mâine va fi reprezentat ca **"addDays(utcNow(), 1)".**"
    - **msdyn\_ scheduleend** – Data programată de încheiere. Selectați o dată în viitor. De exemplu, specificați **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** - starea link-ul. De exemplu, introduceți **"192350000".**

7. Pentru câmpul **OperationSetId**, selectați **msdyn\_ CreateOperationSetV1Response** în caseta **de dialog Conținut** dinamic.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Pasul 13: Crearea unei atribuiri de resurse

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți pasul **Creare atribuire**.
5. În câmpul **Nume** acțiune, selectați **msdyn\_ PssCreateV1**.
6. În câmpul **Entitate**, introduceți următoarele informații despre parametru.

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

7. Pentru câmpul **OperationSetId**, selectați **msdyn\_ CreateOperationSetV1Response** în caseta **de dialog Conținut** dinamic.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Pasul 14: Decrementarea unei variabile

1. În flux, selectați **Pas nou**.
2. În caseta de **dialog Alegeți o operațiune**, în câmpul de căutare, introduceți **variabila** decrement. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În câmpul **Nume**, selectați **numărul de activități**.
4. În câmpul **Valoare**, introduceți **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Pasul 15: Redenumirea unei activități de proiect

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți pasul **Redenumiți activitatea de proiect**.
5. În câmpul **Nume** acțiune, selectați **msdyn\_ PssUpdateV1**.
6. În câmpul **Entitate**, introduceți următoarele informații despre parametru.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Pentru câmpul **OperationSetId**, selectați **msdyn\_ CreateOperationSetV1Response** în caseta **de dialog Conținut** dinamic.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Pasul 16: Rulați un set de operațiuni

1. În flux, selectați **Pas nou**.
2. În **Alegeți o operație** caseta de dialog, în câmpul de căutare, introduceți **efectuează o acțiune nelegată**. Apoi, pe **Acțiuni** fila, selectați operația din lista de rezultate.
3. În pas, selectați punctele de suspensie (**...**), apoi selectați **Redenumire**.
4. Redenumiți pasul **Executare set de operațiuni**.
5. În câmpul **Nume** acțiune, selectați **msdyn\_ ExecuteOperationSetV1**.
6. Pentru câmpul **OperationSetId**, selectați **msdyn\_ CreateOperationSetV1Response OperationSetId** în caseta de **dialog Conținut** Dynamid.

## <a name="references"></a>Referințe

- [Prezentare generală a modului de integrare a fluxurilor cu Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilizați API-urile de planificare a proiectelor pentru a efectua operațiuni cu entități de planificare](schedule-api-preview.md)
- [Prezentare generală a fluxurilor de nori - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Prezentare generală a fluxurilor conștiente de soluții - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
