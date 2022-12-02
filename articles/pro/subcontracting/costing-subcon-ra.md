---
title: Estimarea costurilor pentru atribuirile de resurse subcontractate
description: Acest articol explică cum Microsoft Dynamics 365 Project Operations calculează estimarea costurilor alocărilor de resurse subcontractate.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522671"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimarea costurilor pentru atribuirile de resurse subcontractate

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Atribuțiile de sarcini ale membrilor echipei de proiect subcontractați sunt calculate folosind lista de prețuri **Cumpărare** atașată subcontractului în înregistrarea membrilor echipei aferente. Acest lucru este diferit de modul în care sunt calculate alocările de resurse ale angajaților în cazul în care atribuirile de sarcini ale resurselor angajaților sunt calculate folosind lista de prețuri **Cost** care se atașează unității contractante a proiectului. 

Pentru membrii echipei de proiect de tip generic care sunt subcontractați, atribuțiile sunt calculate folosind o configurație de preț bazată pe roluri în lista de prețuri atașată subcontractului. Prețurile de achiziție pot fi, de asemenea, setate special pentru fiecare resursă. Aceste prețuri specifice resurselor vor avea prioritate atunci atribuirile de sarcini pentru evaluarea costurilor membrilor echipei de proiect numiți sunt pentru lucrători contractuali. 

Prioritatea utilizării prețului de achiziție specific rolului față de specificul resursei este determinată de configurarea priorității dimensiunii de preț în **Parametri > Dimensiuni de preț bazate pe sumă**.

Această funcționalitate de derivare dinamică a prețurilor pe baza configurației dimensiunilor pentru prețurile de achiziție ale subcontractanților este similară cu modul în care sunt derivate costurile și ratele de facturare pentru angajații cu normă întreagă. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Crearea de atribuiri de sarcini pentru obținerea estimărilor de cost ale resurselor subcontractantului

Atribuirile de sarcini pentru subcontractanți pot fi create în două moduri: 
- Utilizând fila **Sarcini**.
- Utilizând fila **Echipă**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Crearea de atribuiri de resurse utilizând fila Sarcini
Utilizând lista **Resurse** în fila **Sarcini** pentru o anumită sarcină, puteți crea o atribuire a sarcinii pentru o resursă numită sau o resursă generică. Dacă selectați o resursă numită din meniul vertical **Resurse Alocate** pe sarcină și această resursă este un lucrător contractual, resursa numită este atribuită sarcinii și o înregistrare corespunzătoare a membrului echipei de proiect este creată cu tipul de lucrător setat la **Lucrător Contractual** și **Valabilitate** setat la **Nevalid**. Ca pas următor, va trebui să deschideți înregistrarea membrilor echipei de proiect și să selectați un subcontract și o linie de subcontractare. Aceasta va actualiza atribuirea sarcinilor pentru a avea o referință la subcontractul și linia de subcontractare și va actualiza, de asemenea, starea de membru al echipei la **Valid**.

Dacă alegeți să creați un membru generic al echipei din meniul vertical **Resurse Alocate** pe sarcină, caseta de dialog **Crearea membrilor generici ai echipei** vă va permite să selectați un subcontract și o linie de subcontractare. Când resursa generică este atribuită sarcinii și este creată înregistrarea corespunzătoare a membrului echipei de proiect, veți observa că înregistrarea membrului echipei de proiect este creată cu tipul de lucrător setat la **Lucrător contractual** și **Validitatea** setată la **Valid**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Crearea membrilor echipei de proiect folosind fila Echipă
Utilizând fila Echipă pe proiect, puteți crea un membru al echipei generic sau numit. Când creați membrul echipei, puteți selecta subcontractul și linia de subcontractare. După ce membrul echipei este creat, va trebui să atribuiți membrul echipei la o sarcină folosind meniul vertical **Resurse alocate** de pe sarcină. 

## <a name="updating-estimates"></a>Actualizarea estimărilor
După ce ați atribuit sarcinile membrilor echipei de proiect, va trebui să navigați la fila **Estimări** de pe proiect și să selectați **Actualizare prețuri** pentru a vă asigura că ratele de cost ale alocărilor de resurse ale subcontractanților sunt actualizate pe baza listei de prețuri de achiziție anexată la subcontract. Estimările nu sunt generate pentru sarcinile nealocate în Microsoft Dynamics 365 Project Operations. Ca rezultat, va trebui să creați sarcini pentru a stabili prețul și costul diferitelor sarcini din proiectul dvs. 

> [NOTĂ!] Membrii echipei de proiect care au **Tipul de lucrător** ca **Lucrător contractual** dar nu au o referință de subcontract sunt marcați ca **Nevalizi** pe grila **Membrii echipei de proiect**. Dacă există membri ai echipei de proiect cu această stare, deschideți înregistrarea membrilor echipei de proiect și actualizați manual câmpurile de subcontract și linie de subcontractare, astfel încât estimarea costurilor să reflecte cu acuratețe costul subcontractantului pe fila **Estimări**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
