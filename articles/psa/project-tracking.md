---
title: Progresul și costurile în curs ale proiectului
description: Acest subiect furnizează informații despre urmărirea progresului proiectului și consumul de costuri.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 0793ee0c75bcbdde0fd92a16634457f73f872b5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120648"
---
# <a name="project-progress-and-cost-consumption"></a>Progresul și costurile în curs ale proiectului

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Necesitatea de a urmări progresele în raport cu o planificare variază în funcție de industrie. Unele industrii urmăresc la un nivel granular, în timp ce alte industrii urmăresc la un nivel mai înalt. Acest subiect arată cum să planificați pentru a îndeplini cerințele organizației dvs.

## <a name="effort-tracking-view"></a>Vizualizarea Urmărire efort

Vizualizarea **Urmărire efort** urmărește progresul activităților în planificare. Aceasta compară orele de efort real petrecute cu o activitate cu orele de efort planificate ale activității. Project Service Automation utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

Inițial la crearea activității: Costul planificat va fi setat la Costul estimat la final. Odată ce sunt înregistrate valorile reale în activitate, următoarele vor fi calculate în vizualizarea Urmărire pentru Efort

- Procent progres = efortul real petrecut până în prezent + cost estimat la finalizare 
- Estimare până la finalizare (ETC) = Estimare la finalizare (EAC) - Efort real depus până în prezent 
- EAC = efortul rămas + efortul real petrecut până în prezent 
- Varianța preconizată a efortului = efortul planificat – EAC

Project Service Automation prezintă o proiecție a varianței efortului pe activitate. În cazul în care EAC este mai mult decât efortul planificat, activitatea este proiectată să dureze mai mult timp decât a fost planificat inițial. Prin urmare, este în urma planificării. În cazul în care EAC este mai puțin decât efortul planificat, activitatea este proiectată să dureze mai puțin timp decât a fost planificat inițial. Prin urmare, este înaintea planificării.

## <a name="reprojecting-effort"></a>Reproiectarea efortului

Este un lucru obișnuit ca un manager de proiect să revizuiască estimările inițiale ale unei activități. Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind starea actuală a proiectului. Cu toate acestea, nu recomandăm ca managerii de proiect să modifice numerele de referință, pentru că referința proiectului reprezintă sursa stabilită de adevăr pentru planificarea proiectului și estimarea de cost și toți participanții direct interesați ai proiectului s-au pus de acord în această privință.

Există două modalități prin care un manager de proiect poate reproiecta efortul asupra activităților:

- Suprascrie ETC-ul implicit cu o nouă estimare a efortului efectiv rămase pe activitate. 
- Suprascrie procentul progresului implicit cu o nouă estimare a progresului real asupra activității.

Fiecare dintre aceste abordări cauzează o recalculare a activității ETC, EAC și procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reproiectarea efortului asupra activităților rezumat

Efortul pe sarcini rezumat sau sarcini container poate fi reproiectat. Indiferent dacă utilizatorul reproiectează utilizând efortul rămas sau procentul de progres pe activitățile rezumat, începe următorul set de calculări:

- Se calculează EAC, ETC. și procentajul de progres al activității.
- Noul EAC este distribuit în jos, activităților secundare în aceeași proporție cum a fost EAC-ul original pe activitate.
- Se calculează noul EAC pe fiecare dintre activitățile individuale până la activitățile de nod frunză. 
- Activitățile secundare afectate până la nodurile frunză au ETC și procentajul de progres recalculate pe baza valorii EAC. Acest lucru duce la o nouă proiecție pentru varianța efortului de activitate. 
- Sunt recalculate EAC-uri de sarcini rezumat până la nodul rădăcină.

### <a name="cost-tracking-view"></a>Vizualizare urmărire cost 

Vizualizarea **Urmărirea costurilor** compară costul real care a fost cheltuit pe o activitate cu costul planificat. 

> [!NOTE]
> Această vizualizare afișează numai costurile cu munca și nu include costurile din estimările de cheltuieli. 

Project Service Automation utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

Când se creează o activitate, costul planificat este egal cu costul estimat la final. După ce sunt înregistrate valorile reale în activitate, următoarele se calculează în vizualizarea **Urmărire** pentru cost:

 - Procent din costul consumat = cost real cheltuit până în prezent ÷ costul estimat la finalizare pentru activitate
 - Cost pentru a finaliza (CTC) = cost estimat la finalizare - cost real cheltuit până în prezent
 - Cost estimat la finalizare = CTC - cost real cheltuit până în prezent
 - Varianța costului proiectat = Cost planificat - Cost estimat la final

Pe activitate este afișată o proiecție a variației de cost. În cazul în care costul estimat la finalizare este mai mult decât costul planificat, activitatea este proiectată să coste mai mult timp decât a fost planificat inițial. Prin urmare, este în tendință peste buget. În cazul în care costul estimat la finalizare e mai mic decât costul planificat, activitatea este proiectată să coste mai puțin timp decât a fost planificat inițial și tendința e sub buget.

## <a name="project-managers-reprojection-of-cost"></a>Reproiectarea costului pentru managerul de proiect

Când efortul este reproiectat, CTC, cost estimat la finalizare, procentul de cost consumat și varianța costurilor proiectate sunt recalculate în vizualizarea de **Urmărirea costurilor**.

## <a name="project-status-summary"></a>Rezumat stare de proiect

Urmărirea datelor din vizualizările de **Urmărire a efortului** și **Urmărirea costului** arată progresul și consumul de cost la nodul rădăcină de proiect, activități de sinteză și niveluri de activități nod frunză. Secțiunea **Stare** a paginii **Entitate de proiect** afișează un rezumat al stării nivelului de proiect.

## <a name="status-summary-fields"></a>Câmpuri rezumat stare

Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului. Acesta utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere. Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut. Câmpul **Stare actualizată pe** nu este editabil și valoarea este un marcaj temporal care indică când a fost actualizată starea ultima dată.

Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din data de urmărire. Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, puteți seta aceste câmpuri la **Avans.** Când programul și varianța costului pentru nodul rădăcină sunt negative, le puteți seta în **În urmă**.
