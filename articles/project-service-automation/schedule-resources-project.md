---
title: Planificați resurse pentru un proiect
description: Cum se planifică resurse pentru un proiect în Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4935567d-9318-4f7c-9c02-c584a78b7841
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d9767e324b3caec4b5f9723347537dbe97ea34fb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754819"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planificați resurse pentru un proiect (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Puteți verifica disponibilitatea resurselor pentru a obține o imagine de ansamblu a rezervării resurselor dvs., sau puteți filtra vizualizarea după competențe, echipă, locație și alte opțiuni.  
  
Tabloul de planificare arată lista de resurse și disponibilitatea acestora. Selectați un mod de vizualizare pentru a arăta disponibilitatea după **Ore**, **Zile**, **Săptămâni** sau **Luni**.  
  
Înainte de a utiliza panoul de planificare, este important să-l configurați. Pentru informații suplimentare, consultați [Configurați tabloul de planificare (Field Service sau Project Service Automation)](../field-service/configure-schedule-board.md).
  
Dacă utilizați o versiune mai veche, pentru a vedea disponibilitatea resurselor, consultați [Vedeți disponibilitatea resurselor](../project-service/view-resource-availability.md).  

> [!IMPORTANT]
>  Pentru a utiliza funcția de rezervare a panoului de planificare, codificarea geografică și serviciile de localizare, trebuie să activați hărțile.  
> 
> 1. În meniul principal, selectați **Planificarea resurselor** > **Administrare**.  
> 2. Faceți clic pe **Parametri de planificare**.  
> 3. Deschideți înregistrarea și navigați i în jos la secțiunea **Resource Scheduling Optimization**.  
> 4. În câmpul **Conectare la Hărți**, alegeți **Da**.  
> 5. Acceptați condițiile și salvați înregistrarea.  
> 6. În meniul principal, selectați **Project Service** > **Panou de planificare**. De aici, există mai multe moduri de a planifica manual o cerință de rezervare. Alegeți metoda care funcționează pentru dvs.
  
## <a name="find-available-resources"></a>Găsiți resurse disponibile

1.  Din lista **Cerință de rezervare**, faceți clic dreapta pe o rezervare neprogramată și alegeți una dintre următoarele:  
  
- Alegeți **Găsiți disponibilitatea - Resurse curente** pentru a găsi o resursă disponibilă din lista de pe panoul de planificare.  
- Alegeți **Găsiți disponibilitatea - Toate resursele** pentru a găsi o resursă disponibilă din cele din sistem  
   > [!NOTE]
   >  Când faceți acest lucru, filtrele vor arăta opțiuni pentru cerința de rezervare selectată.  
  
2. Atunci când vedeți un slot disponibil, faceți clic dreapta pe intervalul de timp de pe tabloul de planificare și alegeți **Rezervați aici**. Sau glisați și fixați cerința de rezervare în slotul de timp disponibil.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervați o resursă utilizând vizualizarea zilnică și vedeți cine nu este rezervat
  
1.  Pe panoul de planificare, selectați **Modul de vizualizare** și selectați **Zile**.  
  
    Acest lucru arată o vizualizare grilă a numărului de ore rezervate pentru o resursă pe zi și prezintă zilele libere.  
  
2.  Faceți clic pe numele resursei pe care doriți s-o rezervați, apoi selectați **Rezervare**.  
  
3.  În caseta de dialog **Rezervare de resurse (creare)**, alege proiectul pentru care doriți să rezervați resursa, metoda de rezervare și timpii de începere sau de încheiere.  
  
4.  Când ați terminat, selectați **Rezervare**.  
  
## <a name="view-to-the-schedule-board"></a>Vizualizați tabloul de planificare
  
1.  Selectați o cerință de rezervare neplanificată din lista din partea de jos.  
  
2.  Glisați cerința de rezervare într-un slot de resurse/timp din panoul de planificare.  
  
3.  Când ați terminat, selectați **Rezervare**.  
  
### <a name="additional-resources"></a>Resurse suplimentare  
 [Ghidul managerului de resurse](../project-service/resource-manager-guide.md)
