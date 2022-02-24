---
title: Atribuiți o resursă la o activitate
description: Acest subiect furnizează informații despre modul de atribuire a resurselor la activități.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
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
ms.openlocfilehash: a348130ee5760196b2f008ea811e7a81758dd73e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993251"
---
# <a name="assign-a-resource-to-a-task"></a>Atribuirea unei resurse la o activitate

[!include [banner](../includes/psa-now-project-operations.md)]

Există trei moduri de atribui o resursă la o activitate în Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervați o resursă ca un membru al echipei și apoi atribuiți resursa la o sarcină

Puteți adăuga o resursă la echipa proiectului și apoi puteți atribui resursa la sarcini în planificarea proiectului.

1. În fila **Membru echipă** adăugați un nou membru al echipei selectând **Nou**. 

2. Panoul **Creare rapidă membru echipă** se deschide, unde puteți selecta numele resursei care se poate rezerva puteți seta un rol. 

    Selectați una dintre următoarele metode de alocare pentru a rezerva resursa:

    - **Capacitate completă** rezervă întreaga capacitate a resursei pentru datele de pornire și finalizare indicate.
    - **Capacitate procentaj** rezervă resursa pentru un procent din capacitatea resursei pentru datele de pornire și finalizare indicate.
    - **După ore - Distribuiți uniform** rezervă resursa pentru un anumit număr de ore, distribuindu-le uniform pe zi între datele de început și de sfârșit indicate.
    - **După ore - Încărcare frontală** rezervă resursa pentru un anumit număr de ore, încărcând frontal timpul pe zi între datele de început și sfârșit indicate.
    - **Niciuna** adaugă resursa la echipă, dar nu creează rezervări care să le absoarbă capacitatea.

3. Pe grila **Planificare** pentru o activitate, faceți clic pe pictograma **Resursă** în celula resursei, apoi selectați **Membrii echipei**, pe care tocmai i-ați adăugat. 

> [!NOTE]
> În filele **Membru echipă** și **Reconciliere**, resursa afișează orele rezervate și atribuite. Orele ar trebui să fie aceleași, dar nu neapărat, deoarece rezervările și atribuirile nu sunt strâns cuplate. Fila **Reconciliere** vă oferă detalii atunci când acestea sunt diferite, cum ar fi când atribuiți unei resurse mai multe ore decât ați rezervat. Dacă este necesar, puteți corecta informațiile prin extinderea rezervărilor resursei sau prin modificarea atribuirii.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Creați un membru al echipei prin atribuirea de sarcini

Când creați un membru al echipei prin atribuirea de sarcini, creați un substituent sau o resursă generică care descrie caracteristicile resursei care doriți să lucreze la final pe sarcini. Apoi generați o solicitare (sau transmiteți o cerere folosind solicitarea) care este folosită pentru căutarea și rezervarea respectivei resurse.

1. Pe grila **Planificare** pentru o activitate, faceți clic pe pictograma **Resursă** în celula resursei.

2. Tastați un nume pentru a servi drept substituent pentru numele resursei. De exemplu „Manager de Program”.

3. Selectați **Creare**, iar în câmpul **Creare rapidă membru echipă**, setați rolul pentru resursa generică.

4. Puteți continua să atribuiți sarcini acestei resurse substituent prin selectarea resursei pe **Selectorul de resurse** pentru sarcină. Acestea sunt listate la **Membrii echipei**.

5. Când ați terminat alocarea resursei generice, selectați resursa generică pe fila **Echipă** și selectați **Generare cerință** pentru a crea o cerință de resurse pentru resursa generică.

6. Selectați **Rezervare** pentru resursa generică. Puteți utiliza Tabloul de planificare pentru a găsi și a rezerva o resursă reală. Puteți de asemenea remite solicitarea de realizare de către un manager de resurse.

7. Când resursa generică este îndeplinită cu o anumită resursă, resursa generică este scoasă din echipă și atribuirile de sarcini pentru resursa generică sunt atribuite resursei indicate care a îndeplinit cerința de resurse a resursei generice.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuiți o resursă din lista tuturor resurselor care se pot rezerva.

Puteți utiliza caseta de căutare în **Selectorul de resurse** pentru a căuta toate resursele care se pot rezerva și pentru a le atribui la o sarcină.

Resursele atribuite în acest mod sunt adăugate echipei fără rezervări. Acest lucru este similar cu adăugarea unui membru al echipei și selectarea Niciunul ca metodă de alocare. Resursa este afișată în filele **Echipă** și **Reconciliere** ca resurse care au numai atribuiri și un deficit de rezervare. Rezervați-le dacă doriți să le utilizați disponibilitatea.

1. Pe grila **Planificare** pentru o activitate, faceți clic pe pictograma **Resursă** în celula resursei.

2. Începeți să tastați un nume. Rezultatele căutării sunt afișate în **Selectorul de resurse** în **Alte resurse**.

3. Selectați resursa pe care doriți să o atribuiți activității.



[!INCLUDE[footer-include](../includes/footer-banner.md)]