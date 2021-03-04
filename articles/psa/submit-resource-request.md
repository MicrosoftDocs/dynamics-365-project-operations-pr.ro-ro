---
title: Remiterea unei solicitări de resurse
description: Acest subiect furnizează informații despre remiterea unei solicitări pentru o resursă de proiect.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 173572be43149aea253bf7beddb993f8c50ab337
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149738"
---
# <a name="submitting-a-resource-request"></a>Remiterea unei solicitări de resurse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Aveți posibilitatea să trimiteți o cerință de resursă generată ca o solicitare de resursă. Solicitarea este apoi trimisă către un manager de resurse pentru îndeplinire.

1. În Project Service Automation (PSA), pe pagina **Proiecte**, faceți clic pe fila **Echipă** pentru a vizualiza o listă de resurse care pot fi rezervate. 
2. Selectați resursa generică care are o cerință de resurse din listă și apoi faceți clic pe **Remitere cerere**.

![Remiterea unei solicitări de resurse](media/RM-how-to-18.png)

Statutul de cerere al membrului generic de echipă se va schimba la **Remis**.

După ce solicitarea este îndeplinită de managerul de resurse, resursa generică va fi înlocuită de o resursă numită dacă managerul de resurse îndeplinește solicitarea cu rezervarea unei resurse numite. În caz contrar, resursa generică va rămâne în echipă și starea solicitării se va modifica la **Necesită revizuire**, dacă managerul de resurse a propus o resursă numită.


[!INCLUDE[footer-include](../includes/footer-banner.md)]