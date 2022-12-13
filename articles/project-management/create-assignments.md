---
title: Creați atribuiri de resurse
description: Acest articol oferă informații despre crearea alocărilor de resurse generice și numite.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812009"
---
# <a name="create-resource-assignments"></a>Creați atribuiri de resurse

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


O alocare a resurselor este asocierea directă a unui membru al echipei de proiect la o sarcină de nod frunză. Acest articol furnizează informații despre moduri diferite de a atribui resurse.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Creați un membru al echipei prin atribuirea de sarcini


Când creați un membru al echipei generic prin atribuirea sarcinilor, creați un substituent sau o resursă generică. Această resursă generică descrie caracteristicile resursei numite pe care doriți să le lucrați în cele din urmă la sarcini. Apoi generați o cerință sau trimiteți o solicitare utilizând cerința care este utilizată pentru a căuta și rezerva resursa numită.

1. Pe grila Planificare pentru o activitate, selectați pictograma resursă din celula **Resursă**.
2. Introduceți un nume care să servească drept nume pentru resursa substituent. De exemplu „Manager de Program”.
3. Selectați **Creare**, iar în câmpul **Creare rapidă membru echipă**, setați rolul pentru resursa generică.
4. Atribuiți activități după cum este nevoie acestei resurse substituent prin selectarea resursei pe **Selectorul de resursă** pentru activitate. Resursele listate sub **Membrii echipei**.
5. Când ați terminat de alocat resursa generică, în fila **Echipă**, selectați resursa generică, apoi selectați **Generare cerință** pentru a crea o cerință de resursă pentru resursa generică.
6. Selectați **Rezervare** pentru resursa generică și apoi puteți folosi panoul de planificare pentru a găsi și rezerva o resursă reală. Puteți de asemenea remite solicitarea de realizare de către un manager de resurse.
7. Când resursa generică este complet îndeplinită cu o resursă numită, resursa generică este eliminată din echipă. (Îndeplinirea parțială a cerinței de resurse nu va avea ca rezultat o alocare de resurse.) Atribuțiile de sarcini pentru resursa generică sunt atribuite resursei numite care a îndeplinit cerința de resurse a resursei generice.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuiți o resursă din lista tuturor resurselor care se pot rezerva.

Puteți utiliza caseta de căutare în **Selector de resurse** pentru a căuta toate resursele active care se pot rezerva și pentru a le atribui la orice activitate nod frunză. Resursele atribuite în acest mod sunt adăugate echipei fără rezervări. Acest lucru este similar cu adăugarea unui membru al echipei și selectarea **Niciuna** ca metodă de alocare. Resursa este afișată pe filele **Echipă**, **Atribuire resursă** și **Reconciliere** ca resurse cu singurele atribuiri și un deficit de rezervare. Rezervați-le dacă doriți să le utilizați disponibilitatea.

1. Din grila de activități, tablă sau cronologie, navigați la celula **Atribuit la**.
2. În caseta de căutare, începeți să tastați un nume. Rezultatele căutării sunt afișate în **Selectorul de resurse** în **Alte resurse**.
3. Selectați resursa pe care doriți să o alocați sarcinii sau selectați numele resursei de mai jos sub **Alte resurse ale echipei**.

## <a name="editing-resource-assignment-contours"></a>Editare contururi de atribuire a resurselor

În mod implicit, atunci când resursele sunt alocate unei sarcini din program, efortul lor este distribuit liniar fiecărei resursă, pe baza orelor de lucru ale acelei resurse și a modului de planificare al proiectului. Un manager de proiect poate folosi grila de alocare a resurselor pentru a rafina estimările de efort pentru fiecare resursă care este atribuită uneia sau mai multor sarcini pe diferite scale de timp. Această caracteristică îi ajută pe managerii de proiect să producă estimări mai precise ale costurilor și vânzărilor, care sunt determinate de contururile de alocare a resurselor care sunt generate atunci când o resursă este atribuită unei sarcini. În plus, managerii de proiect pot reflecta mai ușor cererea de resurse care este necesară pentru a construi cererea într-o cerință de resurse.

### <a name="navigation"></a>Navigare

Pentru a accesa grila de editare a conturului, managerul de proiect selectează mai întâi fila **Sarcini** de pe pagina principală a proiectului, apoi selectează **Atribuții** tab.

![Fila Atribuții din fila Sarcini din pagina principală a proiectului.](media/AssignmentGrid.png)

Grila acceptă două metode de grupare: **grupare după resursă** și **grupare după sarcină**. Spre deosebire de vizualizarea grilă, coloanele nu sunt configurabile. Singurele coloane vizibile sunt **Assigned To**, **Task Name**, **Assignment Start**,** Încheierea sarcinii **și** Efortul sarcinii **.

Când grila este redată inițial, aceasta începe la cel mai devreme contur de atribuire. Dacă programul dvs. nu conține sarcini care necesită efort, grila va fi goală și nu va afișa nimic.

![Grilă de atribuire goală.](media/emptyassignmentgrid.png)

Dacă doriți să vizualizați contururile și diferitele scale de timp, sunt disponibile și grila de alocare a resurselor doar în citire și grila de reconciliere a resurselor.

### <a name="resource-calendars"></a>Calendare de resurse

Capacitatea de a edita un contur pentru o anumită zi este guvernată de zilele lucrătoare ale resursei, așa cum se reflectă în calendarul acestora. Dacă o celulă este dezactivată pentru o anumită resursă, resursa respectivă nu are zile lucrătoare în acea perioadă.

Contururile unei resurse se pot extinde dincolo de datele curente de început și de sfârșit ale sarcinii atribuite. Dacă un contur este actualizat astfel încât să fie după cea mai recentă dată de încheiere a unei sarcini sau cea mai devreme dată de începere a unei sarcini, data de încheiere a sarcinii sau data de începere va fi modificată după caz. Cu toate acestea, dacă un contur este actualizat astfel încât să fie mai devreme decât data de începere a unei sarcini care este legată de un predecesor, actualizarea va eșua, deoarece atribuirea va declanșa sarcina să înceapă înainte ca predecesorul său să fie finalizat, iar comportamentul respectiv nu este în prezent. sprijinit.

### <a name="co-authoring"></a>Co-autorare

Modificările aduse grilei de alocare a resurselor sunt reflectate automat în toate vizualizările asociate, inclusiv în vizualizările diagramă, cronologie, panou și grilă. Dacă mai mulți utilizatori examinează proiectul în același timp, orice modificări pe care le face un utilizator vor fi reflectate în grilă. În schimb, orice modificări care sunt făcute în grila de alocare a resurselor vor fi afișate tuturor celorlalți utilizatori care vizualizează proiectul în aceeași sesiune.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
