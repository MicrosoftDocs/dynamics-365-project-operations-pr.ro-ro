---
title: Metode pentru costul de finalizare
description: Acest articol oferă informații despre metodele utilizate pentru a calcula costul pentru finalizarea unui proiect.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920305"
---
# <a name="cost-to-complete-methods"></a>Metode pentru costul de finalizare

_**Se aplică la:** Project Operations pentru scenarii bazate pe resurse/fără stoc_

Acest articol oferă informații despre metodele utilizate pentru a calcula costul pentru finalizarea unui proiect. Există mai multe metode pe care le puteți utiliza pentru a calcula costul pentru finalizarea unui proiect. 

Când creați o estimare pentru un proiect, pe pagina **Creați o estimare**, în câmpul **Metoda costului de finalizare**, puteți selecta unul dintre următoarele costuri pentru a finaliza metodele.

| Metodă pentru costul de finalizare    | Descriere                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cost real total            | Introduceți costurile estimate manual în **Cost total** sau câmpurile **Cantitate totală** folosind butonul **Cost estimat** de pe **Pagină de estimare**. Sistemul scade costurile reale din totalurile pe care le-ați introdus. Totalul este costul finalizării proiectului. Această metodă nu utilizează estimările cheltuielilor și alocările de resurse introduse în Project Operations încorporate în cadrul Microsoft Dataverse. Costul total sau cantitatea totală pot fi actualizate manual, după cum este necesar.  |
| Total prognoză reală        | Alocările de resurse și estimările cheltuielilor sunt utilizate pentru a determina suma totală estimată a proiectului. Costurile reale sunt comparate cu această prognoză pentru a calcula costul de finalizat.                                                                                                                                                                                                                                                                          |
| Ca estimare anterioară         | Aceleași metode de estimare care au fost utilizate în perioada anterioară sunt folosite aici. Această metodă necesită un model de prognoză dacă perioada anterioară necesită un model de prognoză.                                                                                                                                                                                                                                                                                                                           |
| Setați costul de finalizare la zero | Utilizată în mod obișnuit înainte de eliminarea proiectului estimativ, această metodă corespunde estimărilor totale cu tranzacțiile efective înregistrate și elimină coloana **Cost de finalizare**. Când este complet, rezultatul este întotdeauna de 100%. Pentru fiecare linie de cost pe care o creați, caseta de selectare **Prognoza** este debifată și estimarea totală este copiată din estimarea de cost anterioară. Consumul real pentru perioada estimată este dedus din costul finalizării proiectului.              |
| Din șablonul de cost           | Metoda de cost pentru finalizare care este configurată în șablonul de costuri asociat proiectului de estimare selectat.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]