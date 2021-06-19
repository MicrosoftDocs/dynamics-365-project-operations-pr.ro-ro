---
title: Considerații privind upgrade-ul - Microsoft Dynamics 365 Project Service Automation versiunea 2.x or 1.x la versiunea 3
description: Acest subiect oferă informații despre lucrurile pe care trebuie să le luați în calcul atunci când faceți upgrade de la Project Service Automation versiunea 2. x sau 1. x la versiunea 3.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 04ae6aa3ef6a14a6f85dce3eaa5af01e0adce9ba
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014903"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Considerente legate de upgrade - PSA versiunea 2.x sau 1.x la versiunea 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation și Field Service
Atât Dynamics 365 Project Service Automation, cât și Dynamics 365 Field Service utilizați soluția URS (Universal Resourcing Scheduling Scheduling) pentru planificarea resurselor. Dacă aveți Project Service Automation și Field Service în instanța dvs., actualizați ambele soluțiile pentru a avea ultima versiune. Pentru Project Service Automation, aceasta este versiunea 3.x. Pentru Field Service, este versiunea 8.x. Actualizarea Project Service Automation sau Field Service va instala cea mai recentă versiune a URS. Dacă atât soluția Project Service Automation, cât și soluțiile Field Service din aceeași instanță nu sunt actualizate la cea mai recentă versiune, s-ar putea genera un comportament inconsecvent.

## <a name="resource-assignments"></a>Atribuiri de resurse
În Project Service Automation versiunea 2 și versiunea 1, atribuirile de activități au fost stocate ca activități fiu (denumite și activități de linie) în **Entitatea activitate** și legate indirect de entitatea de **Atribuire resurse** . Activitatea de linie a fost vizibilă în fereastra pop-up de atribuire pe structura detaliată a proiectului (WBS).

![Sarcini linie pe WBS în Project Service Automation versiunea 2 și versiunea 1](media/upgrade-line-task-01.png)

În versiunea 3 a Project Service Automation, schema de bază de atribuire a resurselor care pot fi rezervate la activități s-a modificat. Activitatea liniei a fost învechit și există o relație directă 1:1 între activitatea din **Entitatea activitate** și membrul echipei din entitatea de **Atribuire resurse**. Activitățile care sunt atribuite unui membru al echipei de proiect sunt acum stocate direct în entitatea Atribuire resurse.  

Aceste modificări au impact asupra actualizării oricăror proiecte existente care au atribuiri de resurse pentru resurse care pot fi rezervate și resurse generice într-o echipă de proiect. Acest subiect oferă considerentele pe care va trebui să le luați în considerare pentru proiectele dumneavoastră atunci când faceți upgrade la versiunea 3. 

### <a name="tasks-assigned-to-named-resources"></a>Sarcini atribuite la resursele numite.
Utilizarea entității de activitate subordonată în versiunea 2 și versiunea 1 le-au permis membrilor echipei să portretizeze un alt rol decât rolul implicit definit. De exemplu, Vera Cuza, căreia îi este atribuit implicit rolul de manager de program, ar putea fi atribuită la o sarcină cu rolul de Dezvoltator. În versiunea 3, rolul unui membru numit al echipei este întotdeauna implicit, astfel încât orice sarcină care îi este atribuită Verei Cuza utilizează rolul implicit de manager de program al Verei.

Dacă ați atribuit o resursă unei activități în afara rolului său implicit în versiunea 2 și versiunea 1, atunci când faceți upgrade, resursei denumite îi va fi atribuit rolul implicit pentru toate atribuirile de activități, indiferent de atribuirea rolului în versiunea 2. Alocarea va genera diferențe în estimările calculate de la versiunea 2 sau versiunea 1 la versiunea 3, deoarece estimările sunt calculate pe baza rolului resursei și nu a atribuirii activității de linie. De exemplu, în versiunea 2, două sarcini au fost atribuite la Maria Bușcan. Rolul de pe activitatea de linie pentru activitatea 1 este Dezvoltator și pentru sarcina 2, Manager de program. Maria Bușcan are rolul implicit de manager de program.

![Roluri multiple atribuite unei resurse](media/upgrade-multiple-roles-02.png)

Deoarece rolurile de dezvoltator și manager de programe diferă, estimările costurilor și vânzărilor sunt după urmează:

![Estimările de cost pentru rolurile de resurse](media/upggrade-cost-estimates-03.png)

![Estimările de vânzări pentru rolurile de resurse](media/upgrade-sales-estimates-04.png)

Când faceți upgrade la versiunea 3, activitățile de linie sunt înlocuite cu atribuirile de resurse pe sarcina membrului de echipă de resurse care se poate rezerva. Atribuirea va utiliza rolul implicit al resursei care se poate rezerva. În graficul următor, Maria Bușcan, care are un rol de manager de program, este resursa.

![Atribuiri de resurse](media/resource-assignment-v2-05.png)

Deoarece estimările se bazează pe rolul implicit pentru resursă, estimările de vânzări și costuri se pot modifica. În graficul următor, nu mai vedeți rolul de **Dezvoltator**, deoarece rolul este acum luat din rolul implicit al resursei care poate fi rezervată.

![Estimările costurilor pentru rolurile implicite](media/resource-assignment-cost-estimate-06.png)
![Estimare vânzări pentru rolurile implicite](media/resource-assignment-sales-estimate-07.png)

După finalizarea actualizării, aveți posibilitatea să editați rolul unui membru al echipei pentru a fi altceva decât cel atribuit implicit. Cu toate acestea, dacă modificați rolul unui membru al echipei, acesta va fi modificat pe toate sarcinile atribuite, deoarece membrilor echipei nu li se mai pot atribui mai multe roluri în versiunea 3.

![Actualizarea unui rol de resursă](media/resource-role-assignment-08.png)

Acest lucru este valabil și pentru activitățile de linie care au fost atribuite la resurse denumite atunci când modificați unitatea de organizație a resursei de la cea implicită la o altă unitate de organizație. După terminarea actualizării la versiunea 3, atribuirea va utiliza unitatea de organizație implicită a resursei în loc de cea setată pe linia de activitate.

### <a name="tasks-assigned-to-generic-resources"></a>Sarcini atribuite la resursele generice.
În versiunea 2 și versiunea 1, puteți seta rolul și unitatea de organizație pe o activitate și apoi utilizați caracteristica **Generare echipă** pentru a genera resurse generice bazate pe atributele setate pe activitate. În versiunea 3, creați membrii echipei generice cu rol și unitate de unitate de organizație și apoi atribuiți membrii echipei la activități.

În versiunea 2 și versiunea 1, proiectele cu resurse generice pot avea două stări sau un amestec al ambelor la nivel de activitate. De exemplu, puteți avea următoarele scenarii:

- Activități cu roluri și unități de organizație setate, dar nu s-a generat nicio atribuire de resurse afiliate.
- Activități cu atribuiri de resurse generice de membri ai echipei care au fost atribuite prin crearea de resurse generice utilizând caracteristica **Generare echipă**.

Înainte de a începe upgrade-ul, vă recomandăm să generați din nou echipa pentru fiecare proiect care are sarcini atribuite la resurse generice sau pentru care nu s-a rulat încă procesul de generare echipa.

Pentru activități care sunt atribuite membrilor generici de echipă care au fost generate cu **Generare echipă**, actualizarea va lăsa resursa generică pe echipă și va lăsa atribuirea la acel membru generic de echipă. Vă recomandăm să generați cerința de resurse pentru membrul generic de echipă după actualizare, dar înainte de a rezerva sau remite o solicitare de resurse. Acest lucru va păstra toate atribuirile de unitate de organizație pe membrii generici ai echipei care sunt diferite de unitatea de organizație contractantă a proiectului.

De exemplu, în proiectul Proiect Z, unitatea de organizație contractantă este Contoso SUA. În planul de proiect, pentru sarcinile de testare în faza de implementare a fost atribuit rolul consultant tehnic și unitatea de organizație atribuită este Contoso India.

![Alocarea organizației, faza de implementare](media/org-unit-assignment-09.png)

După faza de implementare, sarcina de testare a integrării este atribuită rolului de consultant tehnic, dar organizația este setată la Contoso SUA.  

![Test integrare alocare sarcini organizație](media/org-unit-generate-team-10.png)

Când generați o echipă pentru proiect, sunt creați doi membri generici de echipă din cauza diferitelor unități de organizație de pe activități. Consultantului tehnic 1 îi vor fi atribuite sarcinile Contoso India iar consultantul tehnic 2 va avea sarcinile Contoso SUA.  

![Membri de echipă generici generați](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> În Project Service Automation versiunea 2 și versiunea 1, membrul echipei nu deține unitatea de organizație, care este menținută pe linia de activitate.

![Activități de linie versiunea 2 și versiunea 1 în Project Service Automation](media/line-tasks-12.png)

Puteți vedea unitatea de organizație în vizualizarea estimări. 

![Estimări ale unităților de organizație](media/org-unit-estimates-view-13.png)
 
Când upgrade-ul este complet, unitatea de organizație de pe linia de activitate care corespunde cu membrul de echipă generic este adăugată la membrul de echipă generic și activitatea de linie este eliminată. Din acest motiv, vă recomandăm ca, înainte de actualizare, să generați sau să generați din nou echipa pe fiecare proiect care conține resurse generice.

Pentru activitățile care sunt atribuite unui rol cu o unitate de organizație care diferă de unitatea de organizație a proiectului contractant și o echipă nu a fost generată, actualizarea va crea un membru de echipă generic pentru rol, dar va utiliza unitatea contractantă a proiectului pentru unitatea de organizație a membrului echipei. Referindu-ne la exemplul cu Proiect Z, unitatea de organizație contractantă Contoso SUA, precum și pentru sarcinile de testare a planului de proiect în faza de implementare au fost atribuite rolul de consultant tehnic cu unitatea de organizație atribuită Contoso India. Sarcinii de testare a integrării încheiată după faza de Implementare i se atribuie rolul de consultant tehnic. Unitatea de organizație Contoso SUA și o echipă nu a fost generată. ctualizarea va crea un membru generic de echipă, un consultant tehnic care are orele atribuite pe toate cele trei sarcini, și o unitate de organizație Contoso SUA, unitatea de organizație contractantă a proiectului.   
 
Modificarea valorii implicite a diverselor unități organizaționale de resurse pe membrii echipei non-generați este motivul pentru care vă recomandăm să generați sau să generați din nou echipa pe fiecare proiect care conține resurse generice înainte de actualizare, astfel încât atribuirile unității organizaționale să nu se piardă.



[!INCLUDE[footer-include](../includes/footer-banner.md)]