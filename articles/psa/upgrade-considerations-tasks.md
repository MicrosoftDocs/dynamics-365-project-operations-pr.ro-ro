---
title: Considerente de actualizare pentru structura detaliată a proiectului
description: Acest subiect oferă informații despre actualizarea structurii detaliate a proiectului de la Project Service Automation 2.x la 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951359"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Considerente de actualizare pentru structura detaliată a proiectului

[!include [banner](../includes/psa-now-project-operations.md)]

Acest subiect oferă informații despre actualizarea structurii detaliate a proiectului de la Project Service Automation 2.x la 3.x. Acest subiect definește starea de sănătate a unui proiect în Project Service Automation (PSA) care este necesar pentru o actualizare de succes. Există, de asemenea, informații despre condițiile comune de blocare care vor duce la eșuarea actualizării. Pentru mai multe informații despre definirea activităților de proiect și a funcțiilor lor în cadrul unei planificări de proiect, consultați [Planificări de proiect](project-creating.md).

## <a name="key-entities"></a>Entități-cheie
Pentru o structură detaliată a proiectului deja încărcată cu resurse, sunt necesare următoarele entități:

- [Proiect](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Echipă de proiect](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Sarcina proiectului](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Atribuiri de resurse](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependența sarcinii proiectului](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Resurse ce se pot rezerva](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Pentru a defini o resursă încărcată în structura detaliată a proiectului, trebuie să parcurgeți următorii pași:

1. Creați un nou proiect. Pentru mai multe informații despre modul de creare a unui proiect nou, consultați [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Creați una sau mai multe activități. Pentru mai multe informații despre modul de creare a unei activități, consultați [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definiți dependențele de activitate. Pentru informații suplimentare, consultați [Dependența sarcinilor de proiect](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Atribuiți membri de echipă de proiect la proiect. Pentru mai multe informații, consultați [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Atribuiți membri de echipă de proiect la activități. Pentru mai multe informații, consultați [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relații echipă de proiect

Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:
- Toți membrii echipei de proiect trebuie să fie asociați cu o resursă care se poate rezerva.
- Toți membrii echipei de proiect trebuie să fie asociați în cadrul aceluiași proiect. 

## <a name="project-task-relationships"></a>Relații activități de proiect
Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:

- Orice activități asociate trebuie să fie asociate cu același proiect.
- Fiecare activitate de linie trebuie să aibă o activitate părinte.
- Fiecare activitate trebuie să aibă un proiect părinte.

### <a name="valid-conditions"></a>Condiții valabile

- Toate duratele activităților trebuie să fie mai mari sau egale cu (>=) o oră și mai mici de 1.800.000 minute (1.250 de zile). *
- Toate activitățile trebuie să aibă o dată de începere nu mai devreme de 2000/01/01.*
- Toate activitățile trebuie să aibă o dată de începere nu mai târziu de 17 ani de la data curentă.*
- Toate activitățile trebuie să aibă o dată de începere anterioară sau egală cu data lor de încheiere.
- Toate tipurile de tranzacții pe clasificări (cheltuieli, materiale, taxe și timp) trebuie să aibă valori pentru **Unitatea implicită** și **Grup unități**.
- Formatele de dată cu litere trebuie evitate.

### <a name="potential-mitigation-steps"></a>Pași de atenuare potențiali
- Utilizați Căutare avansată pentru a identifica sarcinile de proiect care nu conțin un ID de proiect.
- Utilizați Căutare avansată pentru a identifica sarcinile proiectului în care durata programată este mai mare decât > 1.800.000.
- Înainte de a face orice schimbare de date, ar trebui să investigați orice personalizare asociată entității care ar fi putut duce la obținerea datelor într-o stare proastă. Aceste personalizări ar trebui abordate înainte de a continua cu actualizări legate de date.
- Pentru sarcinile identificate care au rămas orfane, luați în considerare ștergerea acestor sarcini dacă nu sunt necesare sau dacă ar trebui asociate cu proiectul părinte corect.
- Pentru orice sarcini în care durata este mai mare de 1.250 de zile, luați în considerare adăugarea mai multor sarcini pentru a reprezenta durata totală, dacă este posibil.

> [!NOTE]
> Elementele notate cu un asterisc (\*) au limite care se datorează faptului că managementul relațiilor cu clienții (CRM) suportă numai 7.320 extinderi de recurență. Trebuie să vă mențineți sub această limită.

## <a name="resource-assignment-relationships"></a>Relații atribuire de resurse
Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:

- Toate atribuirile de resurse într-o structură detaliată a proiectului trebuie să fie legate de același proiect.
- Toate atribuirile de resurse într-o structură detaliată a proiectului trebuie să fie asociate cu membri ai echipei de proiect din același proiect.

### <a name="potential-mitigation-steps"></a>Pași de atenuare potențiali
- Identificați toate activitățile care nu se încadrează în condițiile descrise mai sus.  
- Orice alocări de resurse care nu mai sunt valabile ar trebui să fie șterse.

## <a name="project-task-dependency-relationships"></a>Relațiile dependenței de activitate de proiect
Pentru a asigura o actualizare de succes, următoarele relații trebuie să fie menținute corect:

- Toate dependențele de activitate de proiect trebuie să fie corelate cu același proiect.
- O activitate nu poate avea aceeași dependență la care se face referire de mai multe ori.


[!INCLUDE[footer-include](../includes/footer-banner.md)]