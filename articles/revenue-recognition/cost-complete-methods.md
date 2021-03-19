---
title: Metode pentru costul de finalizare
description: Acest subiect oferă informații despre metodele utilizate pentru a calcula costul pentru finalizarea unui proiect.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279063"
---
# <a name="cost-to-complete-methods"></a>Metode pentru costul de finalizare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest subiect oferă informații despre metodele utilizate pentru a calcula costul pentru finalizarea unui proiect. Există mai multe metode pe care le puteți utiliza pentru a calcula costul pentru finalizarea unui proiect. 

Când creați o estimare pentru un proiect, pe pagina **Creați o estimare**, în câmpul **Metoda costului de finalizare**, puteți selecta unul dintre următoarele costuri pentru a finaliza metodele.

| Metodă pentru costul de finalizare    | Descriere                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cost real total            | Introduceți costurile estimate manual în **Cost total** sau câmpurile **Cantitate totală** folosind butonul **Cost estimat** de pe **Pagină de estimare**. Sistemul scade costurile reale din totalurile pe care le-ați introdus. Totalul este costul finalizării proiectului. Această metodă nu utilizează estimările cheltuielilor și alocările de resurse introduse în Project Operations încorporate în cadrul Microsoft Dataverse. Costul total sau cantitatea totală pot fi actualizate manual, după cum este necesar.  |
| Total prognoză reală        | Alocările de resurse și estimările cheltuielilor sunt utilizate pentru a determina suma totală estimată a proiectului. Costurile reale sunt comparate cu această prognoză pentru a calcula costul de finalizat.                                                                                                                                                                                                                                                                          |
| Ca estimare anterioară         | Aceleași metode de estimare care au fost utilizate în perioada anterioară sunt folosite aici. Această metodă necesită un model de prognoză dacă perioada anterioară necesită un model de prognoză.                                                                                                                                                                                                                                                                                                                           |
| Setați costul de finalizare la zero | Utilizată în mod obișnuit înainte de eliminarea proiectului estimativ, această metodă corespunde estimărilor totale cu tranzacțiile efective înregistrate și elimină coloana **Cost de finalizare**. Când este complet, rezultatul este întotdeauna de 100%. Pentru fiecare linie de cost pe care o creați, caseta de selectare **Prognoza** este debifată și estimarea totală este copiată din estimarea de cost anterioară. Consumul real pentru perioada estimată este dedus din costul finalizării proiectului.              |
| Din șablonul de cost           | Metoda de cost pentru finalizare care este configurată în șablonul de costuri asociat proiectului de estimare selectat.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]