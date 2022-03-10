---
title: Urmărirea efortului în proiecte
description: Acest subiect furnizează informații despre să urmăriți efortul proiectului și progresul lucrului.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 0df357eaf662816107fbc1777ebae030c93bd199756e78a1c3d59155dc64d38f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993976"
---
# <a name="project-effort-tracking"></a>Urmărirea efortului în proiecte

_**Se aplică la:** Project Operations pentru resurse/scenarii bazate pe stocuri, implementare Lite - tratarea facturării proforma_

Necesitatea de a urmări progresele în raport cu o planificare variază în funcție de industrie. Unele industrii urmăresc la un nivel granular, în timp ce alte industrii urmăresc la un nivel mai înalt. Acest subiect arată cum să planificați pentru a îndeplini cerințele organizației dvs.

## <a name="effort-tracking-view"></a>Vizualizarea Urmărire efort

Vizualizarea **Urmărirea efortului** urmărește progresul activităților din planificare prin compararea orelor de efort efective petrecute pe o activitate cu orele de efort planificate ale activității. Dynamics 365 Project Operations utilizează următoarele formule pentru a calcula măsurătorile de urmărire:

- **Procent progres**: efortul real petrecut până în prezent ÷ cost estimat la finalizare (EAC) 
- **Efort rămas**: efort estimat la realizare - efort real petrecut până în prezent 
- **EAC**: efortul rămas + efortul real depus până în prezent 
- **Varianța preconizată a efortului**: efort planificat – EAC

Project Operations prezintă o proiecție a varianței efortului pe activitate. În cazul în care EAC este mai mult decât efortul planificat, activitatea este proiectată să dureze mai mult timp decât a fost planificat inițial și este în urmă. În cazul în care EAC este mai puțin decât efortul planificat, activitatea este proiectată să dureze mai puțin timp decât a fost planificat inițial și este înainte.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reproiectarea efortului asupra sarcinilor nodului frunze

Adesea managerii de proiect revizuiesc estimările inițiale ale unei activități. Reproiectările proiectului reprezintă percepția estimativă a unui manager de proiect, dat fiind starea actuală a proiectului. Cu toate acestea, nu recomandăm ca managerii de proiect să schimbe numerele de efort planificate. Acest lucru se datorează faptului că efortul planificat al proiectului reprezintă sursa stabilită a adevărului pentru calendarul proiectului și estimarea costurilor, iar toate părțile interesate din proiect au fost de acord cu acesta.

Un manager de proiect poate reproiecta efortul asupra sarcinilor prin actualizarea valorii implicite **Efort rămas** cu o nouă estimare a sarcinii. Această actualizare cauzează o recalculare a estimării activității (EAC) la finalizare, procentajul de progres, precum și varianța de efort proiectată pentru o activitate. EAC, ETC, și procentul de progres cu privire la activitățile de sinteză sunt, de asemenea, recalculate, și produce o nouă proiecție a varianței efortului.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reproiectarea efortului asupra activităților rezumat

Efortul pe sarcini rezumat sau sarcini container poate fi reproiectat. Managerii de proiect pot actualiza efortul rămas cu privire la sarcinile de rezumat. Actualizarea efortului rămas declanșează următorul set de calcule din aplicație:

- Se calculează EAC și procentajul de progres al activității.
- Noul EAC este distribuit în jos, activităților secundare în aceeași proporție cum a fost EAC-ul original pe activitate.
- Se calculează noul EAC pe fiecare dintre activitățile individuale până la activitățile de nod frunză. 
- Activitățile secundare afectate până la nodurile frunză au efortul rămas și procentajul de progres recalculate pe baza valorii EAC. Acest lucru duce la o nouă proiecție pentru varianța efortului de activitate. 
- Sunt recalculate EAC-uri de sarcini rezumat până la nodul rădăcină.


## <a name="project-status-summary"></a>Rezumat stare de proiect

Urmărirea datelor din vizualizările de **Urmărire a efortului** și **Urmărirea costului** arată progresul și consumul de cost la nodul rădăcină de proiect, activități de sinteză și niveluri de activități nod frunză. Secțiunea **Stare** a paginii **Entitate de proiect** afișează un rezumat al stării nivelului de proiect.

## <a name="status-summary-fields"></a>Câmpuri rezumat stare

Câmpul **Stare generală proiect** este un câmp editabil care afișează starea generală a proiectului. Acesta utilizează codificare pe culori, precum verde, galben și roșu, pentru a indica riscul în creștere. Câmpul **Comentarii** permite managerului de proiect să introducă comentarii specifice despre statut. Câmpul **Stare actualizată pe** nu este editabil și valoarea este un marcaj temporal care indică când a fost actualizată starea ultima dată.

Câmpurile **Planificare performanță** și **Performanță de cost** sunt setate din data de urmărire. Atunci când varianța de planificare și cost pentru nodul rădăcină în vizualizarea de **Urmărire efort** sunt pozitive, puteți seta aceste câmpuri la **Avans.** Când programul și varianța costului pentru nodul rădăcină sunt negative, le puteți seta în **În urmă**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
