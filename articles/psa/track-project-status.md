---
title: Urmărirea stării unui proiect
description: Cum să urmăriți starea unui proiect în Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082882"
---
# <a name="track-a-projects-status-project-service"></a>Urmărirea stării unui proiect (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilizați [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] pentru a urmări progresul proiectului unui client.  

Pe măsură ce angajamentul progreseaz, etapele proiectului se actualizează pentru a reflecta etapa angajamentului:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nou**    | Când creați un proiect, faza este setată la **Nou**. Dacă ați creat proiectul dintr-un șablon, în această fază, proiectul ar putea avea o planificare, estimări și date de echipă. În caz contrar, aceasta va fi schița proiectului și va trebui să introduceți manual restul de componente ale proiectului. |
|  **Ofertă**   |      Când asociați un proiect la o ofertă sau creați unul de la o ofertă, faza proiectului este setată la **Ofertă** și datele de început și de sfârșit estimate sunt actualizate, de asemenea. Atunci proiectul este în faza de ofertă, detaliile ofertei se afișează pe fila **Vânzări** din pagina **Proiect**.      |
|   **Plan**   |                                     Atunci când câștigați o ofertă asociată cu un proiect și atunci când angajamentul progresează la faza de contractul, faza proiectului se actualizează la **Plan**. Detaliile contractului se afișează în fila **Vânzări** din pagina **Proiect**.                                      |
| **Terminată** |                    Când proiectul este terminat, puteți comuta faza la **Terminată**. Când faza de proiect este setată la Terminată, se înțelege că munca este 100% completă, dar proiectul este menținut deschis pentru orice timp de așteptare sau intrări de cheltuieli ce se vor înregistra.                     |
|  **Închidere**   |           Atunci când au fost înregistrate toate tranzacțiile pentru proiect și nu vă așteptați să mai fie și altele înregistrate, puteți seta manual etapa la **Închidere**. Când proiectul este setat la **Închidere** , nu mai puteți înregistra tranzacții în proiect și proiectul va fi doar în citire.           |

## <a name="to-track-a-projects-status"></a>Pentru a urmări starea unui proiect  

1.  Accesați **Project Service > Proiecte**.  

2.  Faceți clic pe proiectul la care doriți să lucrați.  

3.  În bara din partea de sus a ecranului, selectați săgeata în jos de lângă numele proiectului, apoi faceți clic pe **Monitorizare proiect**.  

4.  Selectați **Urmărire efort** sau **Urmărire costuri** în lista verticală de deasupra listei de activități.  

5.  Faceți dublu clic pe orice activitate pentru a o edita. De asemenea, puteți să mutați sau să redimensionați barele în diagrama Gantt pentru a modifica timpul și progresul unei activități.  

### <a name="see-also"></a>Consultați și  
 [Ghidul Managerului de proiect](../psa/project-manager-guide.md)