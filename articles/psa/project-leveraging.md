---
title: Estimări de vânzări și proiecte
description: Acest subiect furnizează informații despre cum să profitați de planificare și de estimări în procesul de vânzări.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: eafe60362003198a223026526f56261de414bb4a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082814"
---
# <a name="sales-estimates-and-projects"></a>Estimări de vânzări și proiecte

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

În timpul procesului de vânzare, aveți posibilitatea să creați estimări de vânzări prin legarea unui proiect la o ofertă de vânzare. În acest fel, estimarea deterministă poate apărea în timpul procesului de vânzări, pentru a profita de planificarea proiectelor și de capacitățile de estimare. În cazul în care vânzarea trece, planificarea care a fost utilizată în scopul estimării vânzărilor poate fi utilizată ca bază pentru rafinarea ulterioară a planului de proiect.

## <a name="linking-a-project-to-a-quote-line"></a>Legarea unui proiect la o linie de ofertă

Când creați o linie de ofertă bazată pe proiect, aveți posibilitatea să creați un proiect nou sau să asociați un proiect existent pe pagina **Linie ofertă**. 

> ![Formularul Linie ofertă](media/project-8.png)
 
Când creați un proiect nou din detaliile liniei de ofertă, puteți profita de șabloanele de proiect. Șabloanele de proiect sunt proiecte model care reprezintă planuri de proiect standard și estimări financiare care sunt tipice într-o organizație. Ele pot reprezenta, de asemenea, copii ale planurilor de proiect și estimările din proiectele anterioare.

> ![Detalii linie de ofertă](media/project-9.png)
  
Când creeați proiectul din ofertă, proiectul este asociat automat cu linia de ofertă.

## <a name="components-of-estimates-in-a-project"></a>Componentele estimărilor într-un proiect

O planificare vă permite să împărțiți activitatea în activități, să mențineți o ierarhie de activități, să determinați ce resurse sunt necesare pentru a finaliza o activitate și să atribuiți o estimare a efortului necesar pentru finalizarea unei activități.

Puteți defini efortul de lucru și estimările de planificare utilizând câmpurile din fila **Planificare** a paginii **Proiect**. Deoarece o listă de prețuri este asociată cu proiectul, estimările financiare sunt calculate utilizând costul și prețurile de vânzare care sunt definite în lista de prețuri.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importarea estimărilor dintr-un proiect într-o ofertă

După ce definiți estimările proiectului, aveți posibilitatea să le importați în linia de ofertă. În pagina **Detalii linie ofertă** , selectați **Importați din estimările** din panglică pentru a rezuma estimările de proiect după tipul de tranzacție, rol sau nivel de activitate.