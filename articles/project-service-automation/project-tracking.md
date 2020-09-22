---
title: Progresul și costurile în curs ale proiectului
description: Acest subiect furnizează informații despre să urmăriți progresul proiectului și consumul de costuri.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754804"
---
# <a name="project-progress-and-cost-consumption"></a>Progresul și costurile în curs ale proiectului

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Necesitatea de a urmări progresele în raport cu o planificare variază în funcție de industrie. Unele industrii urmăresc la un nivel granular, în timp ce alte industrii urmăresc la un nivel mai înalt. Acest subiect arată cum să planificați pentru a îndeplini cerințele organizației dvs.

## <a name="effort-tracking-view"></a>Vizualizarea Urmărire efort

Vizualizarea **Urmărire efort** urmărește progresul activităților în planificare. Aceasta compară orele de efort real care au fost petrecute pe o activitate cu orele de efort planificate pentru acea activitate. PSA utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

- Procentaj de progres = efort efectiv cheltuit până în prezent ÷ efortul planificat pentru activitate 
- Estimare pentru a finaliza (ETC) = efortul planificat - efortul real petrecut până în prezent 
- Estimare la (EAC) finalizat = efortul rămas + efortul real petrecut până în prezent 
- Varianța preconizată a efortului = efortul planificat – EAC

PSA prezintă o proiecție a varianței efortului pe activitate. În cazul în care EAC este mai mult decât efortul planificat, activitatea este proiectată să dureze mai mult timp decât a fost planificat inițial. Prin urmare, este în urma planificării. În cazul în care EAC este mai puțin decât efortul planificat, activitatea este proiectată să dureze mai puțin timp decât a fost planificat inițial. Prin urmare, este înaintea planificării.

## <a name="re-projecting-effort"></a>Reproiectarea efortului

Este un lucru obișnuit ca un manager de proiect să revizuiască estimările inițiale ale unei activități. Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind stadiul actual al proiectului. Cu toate acestea, nu recomandăm ca managerii de proiect să modifice numerele de referință, pentru că referința proiectului reprezintă sursa stabilită de adevăr pentru planificarea proiectului și estimarea de cost și toți participanții direct interesați ai proiectului s-au pus de acord în această privință.

Există două modalități prin care un manager de proiect poate reproiecta efortul asupra activităților:

- Suprascrie ETC-ul implicit cu o nouă estimare a efortului efectiv rămase pe activitate. 
- Suprascrie procentul progresului implicit cu o nouă estimare a progresului real asupra activității.

Fiecare dintre aceste abordări cauzează o recalculare a activității ETC, EAC și procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Reproiectarea efortului asupra activităților rezumat

Efortul pe sarcini rezumat sau sarcini container poate fi reproiectat. Indiferent dacă utilizatorul reproiectează utilizând efortul rămas sau procentul de progres pe activitățile rezumat, începe următorul set de calcule:

- Se calculează EAC, ETC. și procentajul de progres al activității.
- Noul EAC este distribuit în jos, activităților secundare în aceeași proporție cum a fost EAC-ul original pe activitate.
- Se calculează noul EAC pe fiecare dintre sarcinile individuale până la activitățile de nod frunză. 
- Activitățile secundare afectate până la nodurile frunză au ETC și procentajul de progres recalculate pe baza valorii EAC. Acest lucru duce la o nouă proiecție pentru varianța efortului de activitate. 
- Sunt recalculate EAC-uri de sarcini rezumat până la nodul rădăcină.

### <a name="cost-tracking-view"></a>Vizualizare urmărire cost 

Vizualizarea **Urmărirea costurilor** compară costul real care a fost cheltuit pe o activitate cu costul planificat pentru o activitate. 

> [!NOTE]
> Această vizualizare afișează numai costurile cu munca și nu include costurile din estimările de cheltuieli. 

PSA utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

- Procent din costul consumat = cost real cheltuit până în prezent ÷ costul planificat pentru activitate
- Cost pentru a finaliza (CTC) = cost planificat - cost real cheltuit până în prezent
- EAC = CTC + costul real cheltuit până în prezent
- Varianța costurilor proiectate = cost planificat – EAC

Pe activitate este afișată o proiecție a variației de cost. În cazul în care EAC este mai mult decât costul planificat, activitatea este proiectată să coste mai mult timp decât a fost planificat inițial. Prin urmare, este în tendință peste buget. În cazul în care EAC este mai puțin decât costul planificat, activitatea este proiectată să coste mai puțin decât a fost planificat inițial. Prin urmare, este în tendință sub buget.

## <a name="project-managers-re-projection-of-cost"></a>Reproiectarea costului a managerului de proiect

Când efortul este reproiectat, CTC, EAC, procentul de cost consumat și varianța costurilor proiectate sunt recalculate în vizualizarea de **Urmărirea costurilor**.

## <a name="project-status-summary"></a>Rezumat stare de proiect

Urmărirea datelor din vizualizările de **Urmărire a efortului** și **Urmărirea costului** arată progresul și consumul de cost la nodul rădăcină de proiect, activități de sinteză și niveluri de activități nod frunză. Secțiunea **Stare** a paginii **Entitate de proiect** afișează un rezumat al stării nivelului de proiect.

## <a name="status-summary-fields"></a>Câmpuri rezumat stare

Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului. Acesta utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere. Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut. Câmpul **Stare actualizată pe** nu este editabil și valoarea este un marcaj temporal care indică când a fost actualizată starea ultima dată.

Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din data de urmărire. Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, puteți seta aceste câmpuri la **Avans.** Când programul și varianța costului pentru nodul rădăcină sunt negative, le puteți seta în **În urmă**.
