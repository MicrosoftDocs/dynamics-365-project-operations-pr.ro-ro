---
title: Estimarea costurilor pentru atribuirile de resurse subcontractate
description: Acest articol explică cum Microsoft Dynamics 365 Project Operations calculează estimarea costurilor alocărilor de resurse subcontractate.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 40603c1d2dfdd49909d9a4bf5085f43201e8f6bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932357"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimarea costurilor pentru atribuirile de resurse subcontractate

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Atribuțiile de sarcini ale membrilor echipei de proiect subcontractați sunt calculate folosind **Cumpărare** lista de prețuri atașată subcontractului în evidența membrilor echipei aferente. Acest lucru este diferit de modul în care sunt calculate alocările de resurse ale angajaților în cazul în care atribuirile de sarcini ale resurselor angajaților sunt calculate folosind **Cost** lista de preturi care se ataseaza unitatii contractante a proiectului. 

Pentru membrii echipei de proiect generice care sunt subcontractați, sarcinile sunt calculate utilizând o configurație de preț bazată pe rol în lista de prețuri de achiziție atașată subcontractului. Prețurile de achiziție pot fi, de asemenea, setate special pentru fiecare resursă. Aceste prețuri specifice resurselor li se va acorda prioritate atunci când se calculează costurile atribuirilor de sarcini ale membrilor echipei de proiect numiți sunt lucrători contractuali. 

Prioritatea utilizării prețului de achiziție specific rolului față de specificul resursei este determinată de configurarea priorității dimensiunii de preț în **Parametri > Dimensiuni de preț bazate pe sumă**.

Această funcționalitate de derivare dinamică a prețurilor pe baza configurației dimensiunilor pentru prețurile de achiziție ale subcontractanților este similară cu modul în care sunt derivate costurile și ratele de facturare pentru angajații cu normă întreagă. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Crearea de sarcini pentru obținerea estimărilor de cost ale resurselor subcontractantului

Atribuțiile de sarcini pentru subcontractanți pot fi create în două moduri: 
- Folosind **Sarcini** fila.
- Folosind **Echipă** fila.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Crearea de atribuiri de resurse utilizând fila Sarcini
Folosind **Resurse** lista în **Sarcini** pentru o anumită sarcină, puteți crea o atribuire a sarcinii pentru o resursă numită sau o resursă generică. Dacă selectați o resursă numită din **Resurse Alocate** meniul drop-down pe sarcină și această resursă este un lucrător contractual, resursa numită este atribuită sarcinii și o înregistrare corespunzătoare a membrului echipei de proiect este creată cu tipul de lucrător setat la **Muncitor Contractual** și **Valabilitate** setat la **Invalid**. Ca pas următor, va trebui să deschideți înregistrarea membrilor echipei de proiect și să selectați o linie de subcontractare și subcontractare. Aceasta va actualiza atribuirea sarcinilor pentru a avea o referință la subcontractul și linia de subcontractare și va actualiza, de asemenea, statutul de membru al echipei la **Valabil**.

Dacă alegeți să creați un membru generic al echipei din **Resurse Alocate** meniu derulant pe sarcină, **Crearea generală a membrilor echipei** dialog vă va permite să selectați o linie de subcontractare și de subcontractare. Când resursa generică este atribuită sarcinii și este creată înregistrarea corespunzătoare a membrului echipei de proiect, veți observa că înregistrarea membrului echipei de proiect este creată cu tipul de lucrător setat la **Muncitor Contractual** și **Valabilitate** setat la **Valabil**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Crearea membrilor echipei de proiect folosind fila Echipă
Folosind fila Echipa din proiect, puteți crea un membru al echipei generic sau numit. Când creați membrul echipei, puteți selecta subcontractul și linia de subcontractare. După ce membrul echipei este creat, va trebui să îl atribuiți unui membru al echipei la o sarcină folosind **Resurse Alocate** meniu derulant pe sarcină. 

## <a name="updating-estimates"></a>Actualizarea estimărilor
După ce ați atribuit sarcinilor membrilor echipei de proiect, va trebui să navigați la **Estimări** fila pe proiect și selectați **Actualizați prețurile** pentru a se asigura că ratele de cost ale alocărilor de resurse ale subcontractanților sunt actualizate pe baza listei de prețuri de achiziție anexată la subcontract. Estimările nu sunt generate pentru sarcinile nealocate în Microsoft Dynamics 365 Project Operations. Ca rezultat, va trebui să creați sarcini pentru a stabili prețul și costul diferitelor sarcini din proiectul dvs. 

> [NOTĂ!] Membrii echipei de proiect care au **Tip muncitor** la fel de **Muncitor contractual** dar nu au o referință de subcontract sunt marcate ca **Invalid** pe **Membrii echipei de proiect** grilă. Dacă există membri ai echipei de proiect cu acest statut, deschideți înregistrarea membrilor echipei de proiect și actualizați manual câmpurile de subcontractare și subcontractare, astfel încât estimarea costurilor financiare să reflecte cu acuratețe costul subcontractantului pe **Estimări** fila. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
