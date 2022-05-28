---
title: Urmărirea stării unui proiect
description: Cum să urmăriți starea unui proiect în Project Service
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593397"
---
# <a name="track-a-projects-status-project-service"></a>Urmărirea stării unui proiect (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilizați [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] pentru a urmări progresul proiectului unui client.  

Pe măsură ce angajamentul progreseaz, etapele proiectului se actualizează pentru a reflecta etapa angajamentului:  

| Activitate | Descriere | 
|------------|----------|
| **New** | Când creați un proiect, faza este setată la **Nou**. Dacă ați creat proiectul dintr-un șablon, în această fază, proiectul ar putea avea o planificare, estimări și date de echipă. În caz contrar, aceasta va fi schița proiectului și va trebui să introduceți manual restul de componente ale proiectului. |
| **Ofertă** |  Când asociați un proiect la o ofertă sau îl creați dintr-o ofertă, etapa de proiect este setată la **Citat**, iar datele estimate de început și de încheiere sunt de asemenea actualizate. Atunci proiectul este în faza de ofertă, detaliile ofertei se afișează pe fila **Vânzări** din pagina **Proiect**. |
| **Plan** |  Atunci când câștigați o ofertă asociată cu un proiect și atunci când angajamentul progresează la faza de contractul, faza proiectului se actualizează la **Plan**. Detaliile contractului se afișează în fila **Vânzări** din pagina **Proiect**. |
| **Terminată** | Când proiectul este terminat, puteți comuta faza la **Terminată**. Când faza de proiect este setată la Terminată, se înțelege că munca este 100% completă, dar proiectul este menținut deschis pentru orice timp de așteptare sau intrări de cheltuieli ce se vor înregistra. |
| **Închidere** | Atunci când au fost înregistrate toate tranzacțiile pentru proiect și nu vă așteptați să mai fie și altele înregistrate, puteți seta manual etapa la **Închidere**. Când proiectul este setat la **Închidere**, nu mai puteți înregistra tranzacții în proiect și proiectul va fi doar în citire. |

## <a name="to-track-a-projects-status"></a>Pentru a urmări starea unui proiect  

1.  Accesați **Project Service > Proiecte**.  

2.  Faceți clic pe proiectul la care doriți să lucrați.  

3.  În bara din partea de sus a ecranului, selectați săgeata în jos de lângă numele proiectului, apoi faceți clic pe **Monitorizare proiect**.  

4.  Selectați **Urmărire efort** sau **Urmărire costuri** în lista verticală de deasupra listei de activități.  

5.  Faceți dublu clic pe orice activitate pentru a o edita. De asemenea, puteți să mutați sau să redimensionați barele în diagrama Gantt pentru a modifica timpul și progresul unei activități.  

### <a name="see-also"></a>Consultați și  
 [Ghidul Managerului de proiect](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
