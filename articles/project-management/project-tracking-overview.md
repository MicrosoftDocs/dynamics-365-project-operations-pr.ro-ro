---
title: Prezentare generală a urmăririi proiectelor
description: Acest subiect furnizează informații despre să urmăriți progresul proiectului și consumul de costuri.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082647"
---
# <a name="project-tracking-overview"></a>Prezentare generală a urmăririi proiectelor

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Necesitatea de a urmări progresele în raport cu o planificare variază în funcție de industrie. Unele industrii urmăresc la un nivel granular, în timp ce alte industrii urmăresc la un nivel mai înalt. Acest subiect arată cum să planificați pentru a îndeplini cerințele organizației dvs.

## <a name="effort-tracking-view"></a>Vizualizarea Urmărire efort

Vizualizarea **Urmărirea efortului** urmărește progresul activităților din planificare prin compararea orelor de efort efective petrecute pe o activitate cu orele de efort planificate ale activității. Dynamics 365 Project Operations utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

- **Procent progres** : efortul real petrecut până în prezent ÷ cost estimat la finalizare (EAC) 
- **Estimare pentru a finaliza (ETC)** : efort planificat – efortul real petrecut până în prezent 
- **EAC** : efortul rămas + efortul real depus până în prezent 
- **Varianța preconizată a efortului** : efort planificat – EAC

Project Operations prezintă o proiecție a varianței efortului pe activitate. În cazul în care EAC este mai mult decât efortul planificat, activitatea este proiectată să dureze mai mult timp decât a fost planificat inițial și este în urmă. În cazul în care EAC este mai puțin decât efortul planificat, activitatea este proiectată să dureze mai puțin timp decât a fost planificat inițial și este înainte.

## <a name="reprojecting-effort"></a>Reproiectarea efortului

Adesea managerii de proiect revizuiesc estimările inițiale ale unei activități. Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind starea actuală a proiectului. Cu toate acestea, nu recomandăm ca managerii de proiect să schimbe numerele de bază. Aceasta pentru că referința proiectului reprezintă sursa stabilită de adevăr pentru planificarea proiectului și estimarea de cost și toți participanții direct interesați ai proiectului s-au pus de acord în această privință.

Există două modalități prin care un manager de proiect poate reproiecta efortul asupra activităților:

- Suprascrie ETC-ul implicit cu o nouă estimare a efortului efectiv rămase pe activitate. 
- Suprascrie procentul progresului implicit cu o nouă estimare a progresului real asupra activității.

Fiecare dintre aceste abordări cauzează o recalculare a activității ETC, EAC și procentajul de progres și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reproiectarea efortului asupra activităților rezumat

Efortul pe sarcini rezumat sau sarcini container poate fi reproiectat. Indiferent dacă utilizatorul reproiectează utilizând efortul rămas sau procentul de progres pe activitățile rezumat, începe următorul set de calculări:

- Se calculează EAC, ETC. și procentajul de progres al activității.
- Noul EAC este distribuit în jos, activităților secundare în aceeași proporție cum a fost EAC-ul original pe activitate.
- Se calculează noul EAC pe fiecare dintre activitățile individuale până la activitățile de nod frunză. 
- Activitățile secundare afectate până la nodurile frunză au ETC și procentajul de progres recalculate pe baza valorii EAC. Acest lucru duce la o nouă proiecție pentru varianța efortului de activitate. 
- Sunt recalculate EAC-uri de sarcini rezumat până la nodul rădăcină.

### <a name="cost-tracking-view"></a>Vizualizare urmărire cost 

Vizualizarea **Urmărirea costurilor** compară costul real care a fost cheltuit pe o activitate cu costul planificat pentru o activitate. 

> [!NOTE]
> Această vizualizare afișează numai costurile cu munca și nu include costurile din estimările de cheltuieli. Project Operations utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

- **Procent din costul consumat** : ost real cheltuit până în prezent ÷ costul estimat la finalizare
- **Cost pentru a finaliza (CTC)** : cost planificat – cost real cheltuit până în prezent
- **EAC** : cost rămas + cost real cheltuit până acum
- **Varianța costurilor proiectate** : cost planificat – EAC

Pe activitate este afișată o proiecție a variației de cost. În cazul în care EAC este mai mult decât costul planificat, activitatea este proiectată să coste mai mult timp decât a fost planificat inițial. Prin urmare, este în tendință peste buget. În cazul în care EAC este mai puțin decât costul planificat, activitatea este proiectată să coste mai puțin decât a fost planificat inițial. Prin urmare, este în tendință sub buget.

## <a name="project-managers-reprojection-of-cost"></a>Reproiectarea costului pentru managerul de proiect

Când efortul este reproiectat, CTC, EAC, procentul de cost consumat și varianța costurilor proiectate sunt recalculate în vizualizarea **Urmărirea costurilor**.

## <a name="project-status-summary"></a>Rezumat stare de proiect

Urmărirea datelor din vizualizările de **Urmărire a efortului** și **Urmărirea costului** arată progresul și consumul de cost la nodul rădăcină de proiect, activități de sinteză și niveluri de activități nod frunză. Secțiunea **Stare** a paginii **Entitate de proiect** afișează un rezumat al stării nivelului de proiect.

## <a name="status-summary-fields"></a>Câmpuri rezumat stare

Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului. Acesta utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere. Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut. Câmpul **Stare actualizată pe** nu este editabil și valoarea este un marcaj temporal care indică când a fost actualizată starea ultima dată.

Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din data de urmărire. Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, puteți seta aceste câmpuri la **Avans.** Când programul și varianța costului pentru nodul rădăcină sunt negative, le puteți seta în **În urmă**.
