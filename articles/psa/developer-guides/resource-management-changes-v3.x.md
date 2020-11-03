---
title: Modificări în gestionarea resurselor (Project Service Automation) 3.x
description: Acest subiect furnizează informații despre modificările din zona de gestionare a resurselor.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082987"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Modificări în gestionarea resurselor (Project Service Automation) 3.x

Secțiunile acestui subiect furnizează informații despre modificările efectuate în zona de gestionare a resurselor din Dynamics 365 Project Service Automation versiunea 3. x.

## <a name="project-estimates"></a>Estimări de proiect

În loc să se bazeze pe entitatea **msdyn\_projecttask** ( **Activitate proiect** ), estimările proiectului se bazează pe entitatea **msdyn\_resourceassignment** ( **Atribuire resurse** ). Atribuirile de resurse au devenit „sursa adevărului" pentru programarea și prețul sarcinilor.

## <a name="line-tasks"></a>Activități de linie

În PSA 3. x, activitățile de linie sunt învechite (perimate). Atribuirile indică acum întreaga activitate în locul activităților de linie.

Următorul exemplu arată cum este atribuită o activitate denumită „Activitate test” membrilor echipei A și B în versiunile anterioare de PSA și în PSA 3.x.

- **Înainte de PSA 3.x:**

    - Activitate test

        - Activitate test – Activitate linie 1

            - Atribuire la A

        - Activitate test – Activitate linie 2

            - Atribuire la B

- **PSA 3.x:**

    - Activitate test

        - Atribuire la A
        - Atribuire la B

## <a name="unassigned-assignment"></a>Atribuire neatribuită

În PSA 3.x, o atribuire neatribuită este o atribuire care este atribuită unui membru de echipă **NULL** și unei resurse **NULL**. Atribuirile neatribuite pot apărea în câteva scenarii:

- Dacă s-a creat o activitate, dar nu a fost încă atribuită niciunui membru al echipei, se creează întotdeauna o atribuire neatribuită. 
- Dacă sunt eliminate toate persoanele alocate pe o activitate, o atribuire neatribuit este re-creată pentru această activitate.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Programarea câmpurilor din entitatea Activitate proiect

Câmpurile din entitatea **msdyn\_projecttask** au fost perimate sau mutate la entitatea **msdyn\_resourceassignment** , sau acum se face referire la ele din entitatea **msdyn\_projectteam** ( **Membru echipă proiect** ).

| Câmp perimat pe msdyn\_proiecttask (Activitate proiect) | Câmp nou pe msdyn\_resourarmistialocare (Atribuire resurse) | Comentariu |
|---|---|---|
| msdyn\_assignedresources | Niciunul | |
| msdyn\_assignedteammembers | Niciunul | |
| msdyn\_numberofresources | Niciunul | |
| msdyn\_scheduledhours | Niciunul | |
| msdyn\_effortcontour | msdyn\_plannedwork | Formatul de structură de date JavaScript Object Notation (JSON) care este stocat în câmp a fost modificat. |

## <a name="schedule-contour"></a>Contur planificare

Conturul de planificare este stocat în câmpul **Lucrări planificate** ( **msdyn\_plannedwork** ) din fiecare entitate de **Atribuire resurse** ( **msdyn\_resourceassignment** ).

### <a name="structure"></a>Structură

Noua structură a conturului planificării constă în felii de timp flexibile care sunt definite pentru fiecare zi a planificării. Fiecare felie de timp are următoarele proprietăți:

- **Start** - Începutul orelor de lucru pentru a ziua respectivă, în conformitate cu calendarul proiectului.
- **Sfârșit** - Finalul orelor de lucru pentru a ziua respectivă, în conformitate cu calendarul proiectului.
- **Ore** – Numărul de ore atribuite în ziua respectivă.

**Exemplu**

Acest exemplu utilizează un calendar de proiect în care ziua de lucru este de la 09:00 la 17:00 pe fusul orar UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Planificarea automată și planificarea manuală

Dacă o activitate este planificată automat, orele sunt încărcate frontal și durata activității poate fi redusă.

**Exemplu**

Următoarea sarcină este planificată automat timp de 18 ore pe trei zile (3 decembrie, 2018, până la 5 decembrie 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Dacă o activitate este planificată manual, orele sunt distribuite uniform la toate datele.

**Exemplu**

Următoarea sarcină este planificată manual timp de 18 ore pe trei zile (3 decembrie, 2018, până la 5 decembrie 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unitate de atribuire

Unitatea de atribuire a fost perimată în PSA 3.x. Orele de efort de activitate sunt acum împărțite în mod egal, pe zi, între toate resursele alocate.

**Exemplu**

În acest exemplu, pentru sarcină sunt atribuite două resurse și este planificată automat pentru 36 de ore pe trei zile (3 decembrie, 2018, la 5 decembrie 2018).

- Atribuire 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Atribuire 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensiuni de preț

În PSA 3.x, câmpurile de dimensiune a prețului specifice resurselor (cum ar fi **Rol** și **Unitate organizațională** ) au fost eliminate din entitatea **msdyn\_projecttask**. Aceste câmpuri pot fi preluate de la membrul echipei de proiect corespunzător ( **msdyn\_proiectteam** ) al atribuirii resursei **(msdyn\_resourceassignment** ) când sunt generate estimările de proiect. Un câmp nou, **msdyn\_organizationalunit** , a fost adăugat la entitatea **msdyn\_projectteam** .

| Câmp perimat pe msdyn\_proiecttask (Activitate proiect) | Câmp din msdyn\_projectteam (membru al echipei de proiect) care este utilizat în schimb |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Contururi

Câmpurile de contur de stabilire și de estimare a prețurilor au fost perimate pe entitatea **msdyn\_projecttask**. Acestea au fost mutate în entitatea **msdyn\_resourceassignment**.

| Câmp perimat pe msdyn\_proiecttask (Activitate proiect) | Câmp nou pe msdyn\_resourarmistialocare (Atribuire resurse) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Următoarele câmpuri au fost adăugate la entitatea **msdyn\_resourceassignment** :

* msdyn\_plannedcost
* msdyn\_plannedsales

Următoarele câmpuri pentru costurile și vânzările planificate, reale și rămase sunt neschimbate pe entitatea de **msdyn\_projecttask** :

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
