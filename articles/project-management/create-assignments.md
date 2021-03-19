---
title: Creați atribuiri de resurse
description: Acest subiect oferă informații despre crearea alocărilor de resurse generice și denumite.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a6f4f12a962cb570e8b83d8ee7a01fc0cc2c6155
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287118"
---
# <a name="create-resource-assignments"></a>Creați atribuiri de resurse

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_


O alocare a resurselor este asocierea directă a unui membru al echipei de proiect la o sarcină de nod frunză. Acest subiect furnizează informații despre moduri diferite de a atribui resurse.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Creați un membru al echipei prin atribuirea de sarcini


Când creați un membru al echipei generic prin atribuirea sarcinilor, creați un substituent sau o resursă generică. Această resursă generică descrie caracteristicile resursei numite care doriți să lucreze la final pe sarcini. Apoi generați o solicitare, sau transmiteți o cerere folosind solicitarea care este folosită pentru căutarea și rezervarea respectivei resurse.

1. Pe grila Planificare pentru o activitate, selectați pictograma resursă din celula **Resursă**.
2. Tastați un nume pentru a servi drept substituent pentru numele resursei. De exemplu „Manager de Program”.
3. Selectați **Creare**, iar în câmpul **Creare rapidă membru echipă**, setați rolul pentru resursa generică.
4. Atribuiți activități după cum este nevoie acestei resurse substituent prin selectarea resursei pe **Selectorul de resursă** pentru activitate. Resursele listate sub **Membrii echipei**.
5. Când ați finalizat alocarea resursei generice, selectați resursa generică pe fila **Echipă**, selectați resursa generică și apoi selectați **Generare cerință** pentru a crea o cerință de resurse pentru resursa generică.
6. Selectați **Rezervare** pentru resursa generică și apoi puteți folosi panoul de planificare pentru a găsi și rezerva o resursă reală. Puteți de asemenea remite solicitarea de realizare de către un manager de resurse.
7. Când resursa generică este pe deplin îndeplinită (îndeplinirea parțială a cerinței de resurse nu va avea ca rezultat o atribuire de resurse) cu o resursă numită, resursa generică este eliminată din echipă. Atribuțiile de sarcini pentru resursa generică sunt atribuite resursei denumite care a îndeplinit cerința resurselor generice.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuiți o resursă din lista tuturor resurselor care se pot rezerva.

Puteți utiliza caseta de căutare în **Selector de resurse** pentru a căuta toate resursele active care se pot rezerva și pentru a le atribui la orice activitate nod frunză. Resursele atribuite în acest mod sunt adăugate echipei fără rezervări. Acest lucru este similar cu adăugarea unui membru al echipei și selectarea **Niciuna** ca metodă de alocare. Resursa este afișată pe filele **Echipă**, **Atribuire resursă** și **Reconciliere** ca resurse cu singurele atribuiri și un deficit de rezervare. Rezervați-le dacă doriți să le utilizați disponibilitatea.

1. Din grila de activități, tablă sau cronologie, navigați la celula **Atribuit la**.
2. În caseta de căutare, începeți să tastați un nume. Rezultatele căutării sunt afișate în **Selectorul de resurse** în **Alte resurse**.
3. Selectați resursa pe care doriți să o alocați sarcinii sau selectați numele resursei de mai jos sub **Alte resurse ale echipei**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]