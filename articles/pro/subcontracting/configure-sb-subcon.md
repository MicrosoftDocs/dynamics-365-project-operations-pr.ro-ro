---
title: Configurarea Tabloului de planificare pentru a afișa lucrătorii contractuali și capacitatea subcontractată
description: Acest articol descrie cum să configurați Schedule Board în Microsoft Dynamics 365 Project Operations pentru a arăta capacitatea de resurse subcontractate atunci când personalul este necesar pentru resursele proiectului.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919845"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurarea Tabloului de planificare pentru a afișa lucrătorii contractuali și capacitatea subcontractată 

[!include [banner](../../includes/dataverse-preview.md)]

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

Tabloul de planificare în Microsoft Dynamics 365 Project Operations poate fi folosit pentru căutarea resurselor în două moduri:

- Căutare generală de resurse fără contextul vreunei cerințe specifice de resurse bazate pe proiect.
- Căutare de resurse specifice cerințelor, în care cerința proiectului va oferi contextul resurselor sugerate.

Pentru a notifica consiliul de planificare a capacității de resurse subcontractate și a lucrătorilor contractați, trebuie să faceți actualizări ale setărilor panoului de planificare. Aceste actualizări includ: 
- Actualizați setările Schedule Board pentru căutarea generală a resurselor.
- Actualizați setările Schedule Board pentru căutarea de resurse bazată pe cerințe.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Actualizați setările Schedule Board pentru căutarea generală a resurselor
### <a name="update-filters-for-general-resource-search"></a>Actualizați filtrele pentru căutarea generală a resurselor
Când căutați o resursă, filtrele disponibile pe panoul de planificare ar trebui să fie actualizate, astfel încât să puteți căuta și resurse externe, specificând oricare dintre următoarele sau toate:
  - Tipul lucrătorului, dacă resursele afișate ar trebui să fie lucrători contractuali sau angajați.
  - Firma furnizor căreia ar trebui să aparțină o resursă.
  - Resurse care aparțin unui anumit subcontract sau linie de subcontractare.
    
### <a name="update-retrieve-resource-query"></a>Actualizați interogarea de recuperare a resurselor
Interogarea utilizată pentru căutare ar trebui, de asemenea, actualizată pentru a utiliza aceste atribute suplimentare de filtru. Utilizați următorii pași pentru a actualiza configurația Schedule Board pentru căutarea generală a resurselor:  
1. Deschis **Programează setările tabloului** pentru un anumit tablou de orar.
2. Deschide **Setari generale** filă și derulați la **Alte setari**.
3. În lista de setări din această secțiune, actualizați **Aspect filtru** la **Aspect implicit al filtrului pentru Project Operations Lite**.
4. Actualizați **Preluați interogarea resurselor** la **Interogare implicită Recuperare resurse pentru Project Operations Lite**.

![Actualizați setările Schedule Board pentru căutarea generală a resurselor](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Actualizați setările Schedule Board pentru căutarea de resurse bazată pe cerințe
### <a name="update-filters-for-requirement-specific-resource-search"></a>Actualizați filtrele pentru căutarea resurselor specifice cerințelor 
Când căutați o resursă, filtrele disponibile pe panoul de planificare ar trebui să fie actualizate, astfel încât să puteți căuta și resurse externe, specificând oricare dintre următoarele sau toate:
 - Tipul lucrătorului, dacă resursele afișate ar trebui să fie lucrători contractuali sau angajați.
 - Firma furnizor căreia ar trebui să aparțină o resursă.
 - Resurse care aparțin unui anumit subcontract sau linie de subcontractare.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Actualizați interogarea de recuperare a resurselor pentru căutarea resurselor specifice cerințelor 
Interogarea utilizată pentru căutare ar trebui, de asemenea, actualizată pentru a utiliza aceste atribute suplimentare de filtru. Utilizați următorii pași pentru a actualiza configurația Schedule Board pentru căutarea de resurse bazată pe cerințe:

1. Deschis **Programează setările tabloului** pentru un anumit tablou de program și apoi selectați **Deschide Setări implicite** pentru a deschide setările pentru căutarea specifică cerințelor.
2. Deschide **Setari generale** filă și derulați la **Alte setari**.
3. În lista de setări din această secțiune, actualizați **Aspect filtru** la **Aspect implicit al filtrului pentru Project Operations Lite**.
4. Actualizați **Preluați interogarea resurselor** la **Interogare implicită Recuperare resurse pentru Project Operations Lite**.
5. Deschide **Tipuri de program** filă și accesați **Proiect**.
6. Sub setările pentru **Proiect**, Actualizați **Asistentul de programare Recuperare Resurse Interogare** la **Interogare implicită Recuperare resurse pentru Project Operations Lite** și actualizați **Asistentul de programare Recuperare interogare de constrângeri** la **Interogare implicită de constrângeri de recuperare pentru Project Operations Lite**.

![Actualizați setările Schedule Board pentru căutarea de resurse bazată pe cerințe](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
