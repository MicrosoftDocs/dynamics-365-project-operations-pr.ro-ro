---
title: Remiterea unei solicitări de resurse
description: Acest subiect furnizează informații despre remiterea unei solicitări pentru o resursă de proiect.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082889"
---
# <a name="submitting-a-resource-request"></a>Remiterea unei solicitări de resurse

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aveți posibilitatea să trimiteți o cerință de resursă generată ca o solicitare de resursă. Solicitarea este apoi trimisă către un manager de resurse pentru îndeplinire.

1. În Project Service Automation (PSA), pe pagina **Proiecte** , faceți clic pe fila **Echipă** pentru a vizualiza o listă de resurse care pot fi rezervate. 
2. Selectați resursa generică care are o cerință de resurse din listă și apoi faceți clic pe **Remitere cerere**.

![Remiterea unei solicitări de resurse](media/RM-how-to-18.png)

Statutul de cerere al membrului generic de echipă se va schimba la **Remis**.

După ce solicitarea este îndeplinită de managerul de resurse, resursa generică va fi înlocuită de o resursă numită dacă managerul de resurse îndeplinește solicitarea cu rezervarea unei resurse numite. În caz contrar, resursa generică va rămâne în echipă și starea solicitării se va modifica la **Necesită revizuire** , dacă managerul de resurse a propus o resursă numită.
