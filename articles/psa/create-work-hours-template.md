---
title: Crearea unui șablon de ore de lucru
description: Acest subiect descrie cum să creați un șablon de ore de lucru în Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981270"
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
3. Selectați fila **Ore de lucru** a resursei și completați instrucțiunile din [Setarea orelor de lucru pentru o resursă](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) pentru a configura regulile calendarului.

**Creați un șablon nou de calendar**

1. Accesați **Setări** \> **Șabloane de calendar**.
2. Selectați **Nou** și introduceți un nume, o descriere și o resursă șablon.


> [!NOTE]
> Când se face referire la o resursă într-un șablon de calendar, o copie a calendarului resursei este asociată cu șablonul de calendar. Dacă modificați orele de lucru ale șablonului copiat, aceste modificări nu se propagă în șablonul de calendar.


### <a name="see-also"></a>Consultați și  
 [Configurarea resurselor](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
