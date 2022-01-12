---
title: Angajarea unui proiect cu lucrători contractuali și capacitate subcontractată
description: Acest subiect explică modul în care cerințele proiectului pot fi îndeplinite folosind lucrători contractuali sau capacitatea subcontractată în Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903077"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Angajarea unui proiect cu lucrători contractuali și capacitate subcontractată

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Membrii echipei de proiect generice pot avea angajați sau lucrători contractuali. Când angajați un proiect cu lucrători contractuali, vă puteți limita opțiunile de angajare la anumiți lucrători contractuali care sunt alocați unei linii de subcontractare. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Căutați cerințele de resurse de personal cu lucrători contractuali care aparțin unei anumite linii de subcontractare

Pentru a căuta și cerințe de resurse de personal cu lucrătorii contractuali care aparțin unei anumite linii de subcontractare, urmați acești pași:

1. Creați un membru generic al echipei de proiect care face referire la o linie de subcontractare și subcontractare.
2. Generați o cerință de resurse pentru acest membru generic al echipei de proiect utilizând **Generați cerință** butonul din subgrila membrilor echipei de proiect.
3. Selectați rândul membru al echipei și apoi selectați **Carte** butonul de pe subgrilă. 
4. Aceasta deschide panoul de orar cu contextul cerințelor. Împreună cu alte atribute, cum ar fi câmpurile date, rol și unități organizaționale, filtrele Schedule Board sunt, de asemenea, populate automat cu câmpurile furnizor, subcontract și subcontract din cerința de resurse.
5. Sistemul caută resurse care îndeplinesc criteriile de filtrare și le listează. 
6. Selectați una dintre resursele filtrate și rezervați resursa pentru cerință. 
7. Un membru al echipei de proiect este creat și actualizat cu referințe de subcontractare și subcontractare. Mergi la **Estimări de proiect** și selectați **Actualizați prețurile** pentru a vedea costul actualizat al alocării resurselor. 

> [!NOTE]
> Actualizarea membrului echipei de proiect cu o referință de subcontract și linie de subcontract nu poate fi întotdeauna posibilă în timpul rezervării dacă resursa este alocată mai multor linii de subcontract. Dacă sistemul nu poate actualiza membrul echipei de proiect cu o linie de subcontractare și subcontractare, atunci deschideți înregistrarea membrului echipei de proiect și actualizați manual aceste câmpuri, astfel încât estimarea costului financiar să reflecte cu acuratețe costul subcontractantului.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Căutați și cerințele de resurse de personal cu orice lucrător contractual

Pentru a căuta și cerințe de resurse de personal cu orice lucrător contractual, urmați acești pași:

1. Creați un membru generic al echipei de proiect.
2. Generați o cerință de resurse pentru acest membru generic al echipei de proiect utilizând **Generați cerință** butonul din subgrila membrilor echipei de proiect.
3. Selectați rândul membru al echipei și apoi selectați **Carte** butonul de pe subgrilă. 
4. Aceasta deschide panoul de orar cu contextul cerințelor. Împreună cu alte atribute, cum ar fi câmpurile date, rol și unități organizaționale, filtrele Schedule Board sunt, de asemenea, populate automat cu câmpurile furnizor, subcontract și subcontract din cerința de resurse. Deoarece cerința nu a avut nicio valoare de subcontractare sau linie de subcontractare completată, aceste atribute vor fi goale în panoul de filtrare.
5. Sistemul caută resurse care îndeplinesc criteriile de filtrare și le listează.
6. Actualizați **Tip muncitor** câmpul din panoul de filtrare la **Muncitor Contractual** pentru a limita căutarea la lucrătorii contractuali. Actualizați **Furnizor** pe panoul de filtrare pentru a selecta un furnizor pentru a limita căutarea pentru a afișa numai lucrătorii contractuali care aparțin unei anumite companii de furnizor.
7. Selectați un lucrător contractual din listă și rezervați resursa pentru cerință.
8. Este creat un membru al echipei de proiect. Cu toate acestea, membrul echipei de proiect nu este actualizat cu nicio linie de subcontract sau subcontract și, prin urmare, alocarea resurselor nu va fi calculată folosind prețul subcontractului. Actualizați manual membrul echipei de proiect cu o linie de subcontractare și accesați **Estimări de proiect** și selectați **Actualizați prețurile** pentru a vedea costul actualizat al alocării resurselor.

> [!NOTE]
> Membrii echipei de proiect care au **Tip muncitor** la fel de **Muncitor contractual** dar nu au o referință de subcontract sunt marcate ca **Invalid** pe **Membrii echipei de proiect** grilă. Dacă există membri ai echipei de proiect cu acest statut, deschideți înregistrarea membrilor echipei de proiect și actualizați manual câmpurile de subcontractare și subcontractare, astfel încât estimarea costurilor financiare să reflecte cu acuratețe costul subcontractantului pe **Estimări** fila. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
