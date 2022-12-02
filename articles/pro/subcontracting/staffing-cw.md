---
title: Atribuirea de personal pentru un proiect cu lucrători contractuali și capacitate subcontractată
description: Acest articol explică modul în care cerințele proiectului pot fi îndeplinite folosind lucrători contractuali sau capacitatea subcontractată în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522451"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Atribuirea de personal pentru un proiect cu lucrători contractuali și capacitate subcontractată

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Membrii generici ai echipei de proiect pot fi angajați sau lucrători contractuali. Când angajați un proiect cu lucrători contractuali, vă puteți limita opțiunile de angajare la anumiți lucrători contractuali care sunt alocați unei linii de subcontractare. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Căutați cerințele de resurse de personal cu lucrători contractuali care aparțin unei anumite linii de subcontractare

Pentru a căuta și pentru a asigura cerințele de resurse de personal cu lucrători contractuali care aparțin unei anumite linii de subcontractare, urmați acești pași:

1. Creați un membru generic al echipei de proiect care face referire la un subcontract sau o linie de subcontractare.
2. Generați o cerință de resurse pentru acest membru generic al echipei de proiect utilizând butonul **Generați cerință** din subgrila membrilor echipei de proiect.
3. Selectați rândul pentru membru al echipei și apoi selectați butonul **Rezervare** de pe subgrilă. 
4. Acesta deschide Tabloul de planificare cu contextul cerințelor. Alături de alte atribute, cum ar fi câmpurile date, rol și unități organizaționale, filtrele Tabloului de planificare sunt, de asemenea, populate automat cu câmpurile de furnizor, subcontract și linie de subcontract din cerința de resurse.
5. Sistemul caută resurse care îndeplinesc criteriile de filtrare și le listează. 
6. Selectați una dintre resursele filtrate și rezervați resursa pentru cerință. 
7. Un membru generic al echipei de proiect este creat și actualizat cu referințe pentru un subcontract sau o linie de subcontractare. Accesați **Estimări de proiect** și selectați **Actualizare prețuri** pentru a vedea costul actualizat al alocării resurselor. 

> [!NOTE]
> Actualizarea membrului echipei de proiect cu o referință de subcontract și linie de subcontractare poate să nu fie întotdeauna posibilă în timpul rezervării dacă resursa este alocată mai multor linii de subcontractare. Dacă sistemul nu reușește să actualizeze membrul echipei de proiect cu un subcontract sau linie de subcontractare, atunci deschideți înregistrarea membrului echipei de proiect și actualizați manual aceste câmpuri, astfel încât estimarea costului financiar să reflecte cu acuratețe costul subcontractantului.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Căutați și asigurați cerințele de resurse de personal cu orice lucrător contractual

Pentru a căuta și a asigura cerințele de resurse de personal cu orice lucrător contractual, urmați acești pași:

1. Creați un membru generic al echipei de proiect.
2. Generați o cerință de resurse pentru acest membru generic al echipei de proiect utilizând butonul **Generați cerință** din subgrila membrilor echipei de proiect.
3. Selectați rândul pentru membru al echipei și apoi selectați butonul **Rezervare** de pe subgrilă. 
4. Acesta deschide Tabloul de planificare cu contextul cerințelor. Alături de alte atribute, cum ar fi câmpurile date, rol și unități organizaționale, filtrele Tabloului de planificare sunt, de asemenea, populate automat cu câmpurile de furnizor, subcontract și linie de subcontract din cerința de resurse. Întrucât cerința nu a avut nicio valoare de subcontract sau linie de subcontractare completată, aceste atribute vor fi goale în panoul de filtrare.
5. Sistemul caută resurse care îndeplinesc criteriile de filtrare și le listează.
6. Actualizați câmpul **Tip lucrător** din panoul de filtrare la **Lucrător Contractual** pentru a limita căutarea la lucrătorii contractuali. Actualizați câmpul **Furnizor** în panoul de filtrare pentru a selecta un furnizor și a limita căutarea cu scopul de a afișa numai lucrătorii contractuali care aparțin unei anumite companii de furnizor.
7. Selectați un lucrător contractual din listă și rezervați resursa pentru cerință.
8. Un membru generic al echipei de proiect este creat. Cu toate acestea, membrul echipei de proiect nu este actualizat cu niciun subcontract sau linie de subcontract și, prin urmare, alocarea resurselor nu va fi calculată folosind prețul subcontractului. Actualizați manual membrul echipei de proiect cu o linie de subcontractare și accesați **Estimări de proiect** și selectați **Actualizare prețuri** pentru a vedea costul actualizat al alocării resurselor.

> [!NOTE]
> Membrii echipei de proiect care au **Tipul de lucrător** ca **Lucrător contractual**, dar nu au o referință de subcontract, sunt marcați ca **Nevalizi** pe grila **Membrii echipei de proiect**. Dacă există membri ai echipei de proiect cu această stare, deschideți înregistrarea membrilor echipei de proiect și actualizați manual câmpurile de subcontract și linie de subcontractare, astfel încât estimarea costurilor să reflecte cu acuratețe costul subcontractantului pe fila **Estimări**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
