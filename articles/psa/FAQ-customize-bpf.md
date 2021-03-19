---
title: Cum particularizez fluxul de business Fazele proiectului?
description: Generalități despre particularizarea fluxului de business Fazele proiectului.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 0f95677c56b745bf7900ad503596c93f1e722281
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286173"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Cum particularizez fluxul de business Fazele proiectului?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Există o limitare cunoscută în versiunile anterioare ale aplicației Project Service, și anume faptul că numele de faze în fluxul de business Fazele Proiectului trebuie să corespundă exact numele așteptate în engleză (**Quote**, **Plan**, **Close**). În caz contrar, logica de business, care se bazează pe numele de faze din limba engleză, nu funcționează conform așteptărilor. De aceea nu vedeți acțiuni familiare cum ar fi **Comutare proces** sau **Editare proces** disponibile pe formularul de proiect iar particularizarea fluxului de business nu este încurajată. 

Această limitare a fost tratată în versiunea 2.4.5.48 și ulterioară. Acest articol oferă soluții sugerate în cazul în care aveți nevoie să particularizați fluxul de business implicit pentru versiunile anterioare.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Logica de business cere o potrivire exactă cu numele de fază din limba engleză

Fluxul de business Fazele proiectului include logică de business care conduce la următoarele comportamente în aplicație:
- Atunci când proiectul este asociat cu o ofertă, codul setează fluxul de business la faza **Quote** (ofertă).
- Atunci când proiectul este asociat cu un contract, codul setează fluxul de business la faza **Plan** (planificare).
- Când fluxul de business avansează la faza **Close** (închidere), înregistrarea proiectului este dezactivată. Când proiectul este dezactivat, formularul de proiect și structura detaliată a proiectului (WBS) sunt setate la acces doar de citire, rezervările resurselor specifice sunt eliberate, iar orice liste de prețuri asociate sunt dezactivate.

Această logică de business se bazează pe numele în limba engleză pentru fazele de proiect. Această dependență de numele de fază din limba engleză este motivul principal pentru care nu este încurajată personalizarea fluxului de business Faze proiect, precum și motivul pentru care nu puteți vedea acțiunile comune de flux de business precum **Comutare proces** sau **Editare proces** pe entitatea proiectului.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Ce se întâmplă în cazul în care numele de fază nu corespund numelor din engleză?

În aplicația Project Service versiunea 1.x pe platforma 8.2, atunci numele de fază din fluxul de business nu corespund precis numelor de fază din limba engleză, se sare logica de business care stabilește faza corectă pentru oferte sau contracte sau cea care închide proiectul. Nu există se afișează mesaje de eroare. Prin urmare, se pare că aveți posibilitatea să particularizați fluxul de business Faze proiect. Cu toate acestea, veți vedea că nu va funcționa niciunul dintre procesele automate pentru oferte, contracte și închiderea proiectului.

În aplicația Project Service versiunea 2.4.4.30 sau mai veche pe platforma 9.0, a existat o schimbare arhitecturală semnificativă la fluxurile de business, care a necesitat o rescriere a logicii de business a fluxului de business. Ca urmare, în cazul în care numele de faze ale procesului nu corespund cu numele în engleză așteptate, primiți un mesaj de eroare. 

Prin urmare, în cazul în care doriți să particularizați fluxul de business Faze proiect pentru entitatea de proiect, puteți adăuga doar faze noi la fluxul de business implicit pentru entitatea proiectului, păstrând fazele **Quotes** (oferte), **Plan** (planificare) și **Close** (închidere) așa cum sunt. Această restricție asigură că nu veți primi erori de la logica de business, care se așteaptă la numele de faze în limba engleză fluxul de business.

În versiunea 2.4.5.48 sau ulterioară, logica de business descrisă în acest articol a fost eliminată din fluxul de business implicit pentru entitatea de proiect. Actualizarea la versiunea respectivă sau ulterioară vă va permite să personalizați sau să înlocuiți fluxul de business implicit cu unul propriu. 

## <a name="workarounds-for-earlier-versions"></a>Soluții pentru versiunile anterioare

Dacă actualizarea nu este posibilă, aveți posibilitatea să particularizați fluxul de business Faze proiect pentru entitatea de proiect într-unul dintre următoarele două moduri:

1. Adăugați faze suplimentare la configurația implicită, păstrând numele de fază în limba engleză pentru **Quote** (ofertă), **Plan** (planificare) și **Close** (închidere).


![Captură de ecran cu adăugarea de faze la configurația implicită](media/FAQ-Customize-BPF-1.png)
 
2. Creați-vă propriul flux de business și faceți din acesta fluxul de business principal pentru entitatea de proiect, lucru care vă permite să aveți orice nume de fază doriți. Cu toate acestea, dacă doriți să utilizați aceleași faze de proiect standard **Ofertă**, **Planificare** și **Închidere**, trebuie să faceți unele particularizări care sunt implicate de numele de fază personalizate. Logica mai complexă se află la închiderea proiectului, pe care îl puteți încă declanșa prin simpla dezactivare a înregistrării proiectului.

![Particularizare BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Considerente suplimentare pentru aplicația Project Service versiunea 2.4.4.30 sau mai veche pe platforma 9.0

În Project Service 2.4.4.30 sau mai timpuriu pe platforma 9.0, la un flux de business personalizat câmpul **Nume fază** din entitatea proiectului utilizată în diagrama **Proiect după fază** și vizualizările listă de proiecte de listă nu se actualizează, deoarece este cuplat la fluxul implicit de business Faze proiect. Puteți remedia această problemă cu etapele de mai jos:

- Adăugați un câmp personalizat pentru a capta faza de flux de business curentă care este actualizată pe măsură ce utilizatorul avansează prin fluxul de business.

- Modificați diagrama **Proiect după fază** pentru a lucra cu câmpul dumneavoastră particularizat în loc de configurația implicită.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Pași pentru a vă crea propriul flux de business pentru entitatea de proiect

Pentru a vă crea propriul flux de business pentru entitatea de proiect, faceți următoarele:

1. Accesați **Setări** > **Centru procese**. Nu copiați fluxul de business Faze proiect deoarece acest lucru copiază și logica de business a Project Service.

  ![Creare proces](media/FAQ-Customize-BPF-3.png)

2. Utilizați Proiectantul de procese pentru a crea numele de fază pe care le doriți. Dacă doriți aceeași funcționalitate cu fazele implicite pentru **Ofertă**, **Planificare** și **Închidere**, va trebui să creați acest lucru pe baza numelor de fază ale fluxului dvs. de business personalizat.

   ![Captură de ecran cu Proiectantul de Procese utilizat pentru personalizarea BPF](media/FAQ-Customize-BPF-4.png) 

3. În Proiectantul de procese, faceți clic pe **Ordonare fluxuri de proces** pentru a face ca fluxul de business personalizat să fie fluxul de business primar pentru entitatea proiectului, mutându-l deasupra fluxului de business Faze proiect în partea de sus a listei.


   [Captură de ecran cu utilizarea Ordonare fluxuri de proces](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Pașii de mai jos se aplică pentru aplicația Project Service 2.4.4.30 sau anterioară pe platforma 9.0

4. Adăugați un câmp nou personalizat la entitatea de proiect pentru a capta fazele personalizate în fluxul dvs. de business personalizat. Veți avea nevoie să adăugați logica de business (plugin/flux de lucru) pentru a actualiza acest câmp atunci când se actualizează faza pe fluxul de business personalizat.

   ![Captură de ecran cu personalizarea entității Proiect](media/FAQ-Customize-BPF-6-720.png)

5. Modificați diagrama **Proiect după fază** pentru a vă utiliza noul câmp personalizat pentru faze.

   ![Captură de ecran cu utilizarea diagramei Proiect după fază](media/FAQ-Customize-BPF-7-720.png)

6. Modificați orice vizualizări pentru entitatea de proiect, astfel încât să includă noul dumneavoastră câmp personalizat pentru faze.

   ![Captură de ecran cu modificarea vizualizărilor pe entitatea proiectului](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]