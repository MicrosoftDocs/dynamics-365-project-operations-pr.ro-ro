---
title: Configurarea Tabloului de planificare pentru a afișa lucrătorii contractuali și capacitatea subcontractată
description: Acest articol descrie cum să configurați Tabloul de planificare în Microsoft Dynamics 365 Project Operations pentru a arăta capacitatea de resurse subcontractate atunci când personalul este necesar pentru resursele proiectului.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262232"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurarea Tabloului de planificare pentru a afișa lucrătorii contractuali și capacitatea subcontractată 

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Tabloul de planificare în Microsoft Dynamics 365 Project Operations poate fi folosit pentru căutarea resurselor în două moduri:

- Căutare generală de resurse fără contextul vreunei cerințe specifice de resurse bazate pe proiect.
- Căutare de resurse specifice cerinței, în care cerința proiectului va oferi contextul pentru resursele sugerate.

Pentru a notifica tabloul de planificare a capacității de resurse subcontractate și a lucrătorilor contractați, trebuie să faceți actualizări ale setărilor Tabloului de planificare. Aceste actualizări includ: 
- Actualizarea setărilor Tabloului de planificare pentru căutarea generală a resurselor.
- Actualizarea setărilor Tabloului de planificare pentru căutarea de resurse bazată pe cerințe.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualizarea setărilor Tabloului de planificare pentru căutarea generală a resurselor
### <a name="update-filters-for-general-resource-search"></a>Actualizarea filtrelor pentru căutarea generală a resurselor
Când căutați o resursă, filtrele disponibile pe tabloul de planificare ar trebui să fie actualizate, astfel încât să puteți căuta și resurse externe, specificând oricare dintre următoarele sau toate:
  - Tipul lucrătorului, dacă resursele afișate ar trebui să fie lucrători contractuali sau angajați.
  - Compania furnizoare căreia o resursă ar trebui să-i aparțină.
  - Resurse care aparțin unui anumit subcontract sau linie de subcontractare.
    
### <a name="update-retrieve-resource-query"></a>Actualizare interogare de regăsire resurse
Interogarea utilizată pentru căutare ar trebui, de asemenea, actualizată pentru a utiliza aceste atribute suplimentare de filtru. Utilizați următorii pași pentru a actualiza configurația Tabloului de planificare pentru căutarea generală a resurselor:  
1. Deschideți **Setările tabloului de planificare** pentru un anumit Tablou de planificare.
2. Deschideți fila **Setări generale** și derulați la **Alte setări**.
3. În lista de setări din această secțiune, actualizați **Aspect filtru** la **Aspect implicit al filtrului pentru Project Operations Lite**.
4. Actualizați **Interogare de regăsire resurse** la **Interogare implicită regăsire resurse pentru Project Operations Lite**.

![Actualizarea setărilor Tabloului de planificare pentru căutarea generală a resurselor](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualizarea setărilor Tabloului de planificare pentru căutarea de resurse bazată pe cerințe
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualizarea filtrelor pentru căutarea de resurse specifice cerințelor 
Când căutați o resursă, filtrele disponibile pe tabloul de planificare ar trebui să fie actualizate, astfel încât să puteți căuta și resurse externe, specificând oricare dintre următoarele sau toate:
 - Tipul lucrătorului, dacă resursele afișate ar trebui să fie lucrători contractuali sau angajați.
 - Compania furnizoare căreia o resursă ar trebui să-i aparțină.
 - Resurse care aparțin unui anumit subcontract sau linie de subcontractare.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualizarea interogării de regăsire a resurselor pentru căutarea resurselor specifice cerințelor 
Interogarea utilizată pentru căutare ar trebui, de asemenea, actualizată pentru a utiliza aceste atribute suplimentare de filtru. Utilizați acești pași pentru a actualiza configurația Tabloului de planificare pentru căutarea de resurse bazată pe cerințe:

1. Deschideți **Setările tabloului de planificare** pentru un anumit Tablou de planificare și apoi selectați **Deschideți setările implicite** pentru a deschide setările pentru căutarea specifică cerințelor.
2. Deschideți fila **Setări generale** și derulați la **Alte setări**.
3. În lista de setări din această secțiune, actualizați **Aspect filtru** la **Aspect implicit al filtrului pentru Project Operations Lite**.
4. Actualizați **Interogare de regăsire resurse** la **Interogare implicită regăsire resurse pentru Project Operations Lite**.
5. Deschideți fila **Tipuri de planificare** și accesați **Proiect**.
6. Sub setările pentru **Proiect**, actualizați **Interogare de regăsire resurse pentru asistentul de planificare** la **Interogare implicită de regăsire resurse pentru Project Operations Lite** și actualizați **Interogare de regăsire constrângeri pentru asistentul de planificare** la **Interogare implicită de regăsire constrângeri pentru Project Operations Lite**.

![Actualizarea setărilor Tabloului de planificare pentru căutarea de resurse bazată pe cerințe](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
