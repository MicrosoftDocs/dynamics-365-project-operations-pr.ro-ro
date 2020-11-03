---
title: Actualizare pagină de pornire
description: Acest subiect arată unde se găsesc informații importante despre caracteristicile noi și modificate din Dynamics 365 Project Service Automation, precum și procesul de upgrade la cea mai nouă versiune.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 29e7b519b61e8709c025e9906d04aed0156f65eb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082877"
---
# <a name="upgrade-home-page"></a>Actualizare pagină de pornire

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Faceți upgrade de la PSA versiunea 2.x sau 1.x la versiunea 3.x

### <a name="new-instances"></a>Instanțe noi

Începând cu 17 mai 2019, la selectarea Project Service Automation în timpul asigurării accesului unei instanțe noi, versiunea 3.x este instalată în mod implicit.

### <a name="existing-instances"></a>Instanțe existente

Anterior, clienții care au o instanță de PSA versiunea 2.x și trebuiau să facă upgrade la versiunea 3.x, care este versiunea unificată bazată pe interfață client (UCI) de PSA, trebuiau să contacteze Asistența Microsoft și să furnizeze detaliile instanței lor astfel încât serviciul de asistență să poată activa instanța pentru upgrade la versiunea 3.x. Începând cu 1 martie 2020, clienții care au o instanță a PSA versiunea 2.x și au nevoie să facă upgrade la versiunea 3.x, vor putea să își actualizeze instanțele direct din portalul de administrare, fără să fie nevoiți să contacteze Asistența Microsoft.  

> [!NOTE]
> PSA versiunea 3.x include modificări semnificative. Acesta a fost construit pe cadrul de Interfață unificată pentru a ajuta la furnizarea unei experiențe de utilizator îmbunătățite. Aplicația reproiectată oferă o interfață de utilizator (UI) consecventă, uniformă și respectă principiile de proiectare adaptabile pentru vizualizarea optimă pe orice dimensiune de ecran sau dispozitiv. Au existat și alte modificări în cadrul aplicației. Unele dintre zonele care au fost schimbate includ stabilirea prețurilor, rezervarea și alocarea resurselor, a timpului, a cheltuielilor și a aprobărilor.

Înainte de a începe procesul de actualizare, vă recomandăm să completați următoarele activități:

- Verificați dacă pe instanța identificată sunt instalate atât Dynamics 365 Field Service, cât și Project Service Automation. Dacă ambele soluții sunt instalate, trebuie să planificați să le actualizați pe amândouă înainte de a relua utilizarea regulată a instanței.
- Examinați cu atenție următoarele subiecte. Conștientizarea și înțelegerea modificărilor dintre versiuni vă vor ajuta cu procesul de actualizare. Aceste subiecte oferă informații despre schimbările majore în PSA, împreună cu considerente și recomandări pentru planificarea actualizării la versiunea 3.x.

    - [Ce este nou sau modificat în Project Service Automation versiunea 3](whats-new-changed-v3.md)
    - [Considerente legate de upgrade - Project Service Automation versiunea 2.x sau 1.x până la versiunea 3](upgrade-v3.md)

- Actualizați-vă instanța sandbox pentru a evalua modificările din implementare înainte de a vă actualiza instanța de producție.

După ce ați revizuit subiectele care au fost menționate mai sus și sunteți gata să actualizați la PSA versiunea 3.x sau versiunea bazată pe UCI, trimiteți o solicitare de asistență Microsoft pentru a face actualizarea disponibilă din centrul de administrare. În cererea dumneavoastră, furnizați detaliile instanței dvs.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versiuni mai vechi de PSA (PSA versiunea 2.x) într-o instanță nou creată

De la 17 mai 2019, toate instanțele noi vor avea UCI ca client implicit. Pentru alinierea cu această modificare, se va furniza implicit accesul pentru PSA versiunea 3.x și Field Service versiunea 8.x, deoarece aceste versiuni sunt proiectate să funcționeze cu clientul UCI.

Începând cu 1 martie 2020, clienții Dynamics PSA nu vor mai putea crea medii noi cu versiuni mai vechi de PSA, de exemplu versiunea PSA 2.x sau mai veche. Orice nou mediu va avea doar versiunea 3.x a PSA.

> [!NOTE]
> Pentru cea mai bună experiență când utilizați versiunile mai vechi ale Field Service și ale aplicațiilor PSA, accesați pagina **Setări sistem** și, la câmpul **Utilizați numai noua Interfață unificată (recomandat)** , selectați **Nu** , deoarece aceste versiuni nu sunt proiectate să se încarce corect în UCI. După ce ați dezactivat UCI, aveți posibilitatea să deschideți și să executați aceste versiuni de Field Service și PSA utilizând vechiul client web. 
