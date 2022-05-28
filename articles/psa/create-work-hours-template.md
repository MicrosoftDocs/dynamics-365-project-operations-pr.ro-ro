---
title: Crearea unui șablon de ore de lucru
description: Acest subiect descrie cum să creați un șablon de ore de lucru în Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598963"
---
# <a name="create-a-work-hours-template-project-service"></a>Creați un șablon de ore de lucru (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Pentru a crea și gestiona un proiect, trebuie să aplicați un șablon de calendar de proiect. Șablonul de calendar definește următoarele atribute de proiect:

- Programul de lucru, inclusiv ora de început și sfârșit
- Zile de lucru
- Excepții din calendar, cum ar fi zilele nelucrătoare

Șablonul de calendar aplicat unui proiect este o copie a șablonului calendarului definit în setările organizației dvs.

> [!NOTE]
> Dacă modificați șablonul de calendar, aceste modificări nu se propagă la planificarea de lucru a proiectului. Pentru a schimba planificarea de lucru a proiectului, trebuie aplicat un nou șablon.

Pentru a crea un șablon de calendar pentru organizația dvs., există două cerințe principale:

- Definiți orele de lucru dorite ale șablonului utilizând o resursă rezervabilă nouă sau existentă.
- Creați un nou șablon de calendar și asociați șablonul cu resursa rezervabilă.

**Definiți orele de lucru ale șablonului**

1. Accesați **Resurse** \> **Resurse**.
2. Creați o nouă resursă pentru a face referință în șablonul calendarului sau selectați o resursă existentă.
3. Selectați fila **Ore de lucru** a resursei și completați instrucțiunile din [Setarea orelor de lucru pentru o resursă](/dynamics365/field-service/set-work-hours-resource) pentru a configura regulile calendarului.

**Creați un șablon nou de calendar**

1. Accesați **Setări** \> **Șabloane de calendar**.
2. Selectați **Nou** și introduceți un nume, o descriere și o resursă șablon.


> [!NOTE]
> Când se face referire la o resursă într-un șablon de calendar, o copie a calendarului resursei este asociată cu șablonul de calendar. Dacă modificați orele de lucru ale șablonului copiat, aceste modificări nu se propagă în șablonul de calendar.


### <a name="see-also"></a>Consultați și  
 [Configurarea resurselor](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
