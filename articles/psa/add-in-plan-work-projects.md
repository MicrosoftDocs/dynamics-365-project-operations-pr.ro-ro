---
title: Planificați-vă munca în Microsoft Project cu programul de completare Project Service
description: Acest subiect furnizează informații despre cum se utilizează programul de completare Microsoft Project pentru Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: c9628fcaf40f33d75f70ae15e37f422e65337d2c51d0d803178f8bcdfe10c7bd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993886"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planificați-vă munca în Microsoft Project cu programul de completare Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vă ajută să vă planificați proiectele, inclusiv să realizați estimări. Puteți defini lucrarea astfel încât costurile, efortul și valoarea vânzărilor să fie clare la momentul când se trimite propunerea finală.  

Puteți instala [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] și puteți planifica munca în mediul familiar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilizați capacitățile robuste de planificare și management din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], apoi actualizați-vă planul de proiect în Project Service Automation.  

> [!IMPORTANT]
> - Pentru a utiliza gestionarea documentelor SharePoint pentru a vă stoca filierele [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pentru proiectele [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], administratorul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] va trebui să pornească gestionare documente. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] este compatibil numai cu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descărcați și instalați programul de completare  
 Țineți informațiile de conectare [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la îndemână. Veți avea nevoie de aceste informații pentru a vă conecta de la [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  De la Centrul de descărcare puteți descărca programul de completare pentru versiunea acceptată de Project Service, fie [v2. X](https://go.microsoft.com/fwlink/?linkid=828268), fie [v 3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Selectați linkul de descărcare.  

3.  Odată ce descărcarea s-a finalizat, selectați **Da** pentru a instala programul de completare.  

## <a name="configure-the-add-in"></a>Configurați programul de completare  

1. Deschideți [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și selectați fila **Project Service**.  

2. Selectați **Conectare**.  

3. Introduceți informațiile de conectare și selectați **Conectare**.  

   Acum puteți începe să folosiți programul de completare.  

## <a name="read-from-a-template"></a>Citirea de pe un șablon  
 Citiți dintr-un șablon creat în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] și copiat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pentru a începe să vă planificați proiectul. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crearea unui șablon de proiect (Project Service Automation)](../psa/create-project-template.md)  

1.  De pe fila **Project Service**, selectați **Citire** > **Șablon de proiect Project Service Automation**.  

2.  Alegeți un șablon de proiect din listă și selectați **Deschidere**.  

    > [!NOTE]
    >  În mod implicit, activitățile copiate din șablon în Project sunt setate drept planificate manual.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Atribuiți roluri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] resurselor proiectului  

1.  Deschideți un proiect și selectați panglica **Activitate**.  

2. Selectați meniul **Diagramă Gantt** și alegeți **Foaie de resurse**.  

3. Pe foaia de resurse, selectați meniul vertical **Rol de resursă Project Service** și alegeți un rol Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Găsiți resurse pentru proiectul dvs.  

1.  Din fila Project Service, selectați un rând și selectați **Găsiți resurse**.  

2.  Pe ecranul **Rezervați resursa**, selectați resursa pe care doriți s-o utilizați pentru proiect.  

3.  Selectați **Rezervare** și apoi selectați **OK**.  

## <a name="publish-your-project"></a>Publicarea proiectului  
Atunci când terminați de planificat proiectul, următorul pas este să importați și să publicați proiectul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Proiectul se va importa în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Se aplică procesul de generare a echipelor și a prețurilor. Deschideți proiectul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pentru a vedea că echipa, estimările de proiect și structura detaliată a proiectului au fost generate. Următorul tabel arată unde să găsiți rezultatele.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagramă Gantt**   | Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Structura detaliată a proiectului**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Foaie de resurse** |   Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membrii echipei de proiect**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Folosirea utilizării**    |    Importă în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimări de proiect**.     |

**Pentru a vă importa și a vă publica proiectul**  
1. Pe fila **Project Service**, accesați **Publicare** > **Proiect nou Project Service Automation**.  

2. În caseta de dialog **Publicați într-un nou proiect din Project Service**, introduceți **Numele proiectului** și selectați **Clientul**.  

3. Opțional, selectați **Legați planul de proiect la Project Service Automation** pentru a lega planul fișierului Proiect la Project Service Automation.  

4. Selectați **Publicare**.  

   Legarea fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] face fișierul Project coordonator și stabilește structura detaliată a proiectului din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] drept doar în citire.  Pentru a face modificări în planul de proiect, trebuie să le efectuați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să le publicați ca actualizări la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editarea unui proiect care a fost importat  
 Pentru a modifica un plan de proiect care a fost importat în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aveți două opțiuni:  

- Deschideți fișierul principal și editați-l în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Anulați legarea fișierului și editați-l direct în Project Service. În mod implicit, un proiect care a fost încărcat din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] este blocat și poate fi editat numai în Project. Pentru a edita fișierul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], legarea fișierului trebuie anulată.  

### <a name="edit-in-pn_microsoft_project"></a>Editați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. În meniul principal, mergeți la **Project Service** > **Proiecte**.  

2. Din lista de proiecte, deschideți-l pe cel pe care l-ați creat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selectați **Deschideți în MS Project** din panglică. Acest lucru va deschide fișierul coordonator legat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Anulați legarea unui fișier și editați-l în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. În meniul principal, mergeți la **Project Service** > **Proiecte**.  

2. Din lista de proiecte, deschideți-l pe cel pe care l-ați creat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selectați **Anulați legarea în MS Project** din panglică.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Încărcarea unui fișier Project în SharePoint sau în Grupurile Office  
 Puteți încărca fișierul Project în SharePoint și îl puteți găsi sub Documentele asociate pentru proiectul dvs. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Trebuie ca administratorul dvs. să configureze gestionarea de documente SharePoint și să o activeze pentru entitatea Project. 

 De asemenea, puteți încărca fișierul Project în [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] dacă aveți grupurile Office configurate.

### <a name="upload-a-file-for-sharepoint"></a>Încărcarea unui fișier pentru SharePoint  

1. În meniul principal, mergeți la **Project Service** > **Încărcare**.  

2. Selectați **În documentele Project din Project Service Automation**.  

3. În caseta de dialog **Activați deschiderea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selectați **Da** sau **Nu**.  

   - Dacă selectați **Da**, veți putea selecta butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** din Project Service Automation, veți putea să lansați [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să încărcați fișierul Proiect din biblioteca de documente SharePoint.  

   - Dacă selectați **Nu**, linkul pentru **Deschidere în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nu va funcționa.  

4. Fișierul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] poate fi găsit în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sub **Documente** pentru respectivul proiect [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Încărcarea unui fișier pentru grupurile Office  

1. În meniul principal, mergeți la **Project Service** > **Încărcare**.  

2. Selectați **În documentele Project din Project Service Automation**.  

3. În caseta de dialog **Activați deschiderea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selectați **Da** sau **Nu**.  

   - Dacă selectați **Da**, veți putea să selectați butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** din Project Service Automation, veți putea să lansați [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să încărcați fișierul Proiect din biblioteca de documente SharePoint.  

   - Dacă selectați **Nu**, linkul pentru **Deschidere în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nu va funcționa.  

4. Fișierul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] poate fi găsit în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sub **Documente** pentru respectivul proiect [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publicarea proiectului ca șablon  
 Puteți să vă salvați proiectul și să-l refolosiți dacă îl salvați ca șablon de proiect în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Șabloanele de proiect sunt planuri de proiect reutilizabile din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Pentru mai multe informații, consultați [Creați un șablon de proiect (Project Service Automation)](../psa/create-project-template.md). 

1. Pe fila **Project Service**, accesați **Publicare** > **Șablon proiect nou Project Service Automation**.  

2. În caseta de dialog **Publicați într-un nou proiect din șablonul Project Service**, introduceți **Numele șablonului de proiect**.  

3. Opțional, selectați **Legați planul de proiect la Project Service Automation** pentru a lega planul fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Selectați **Publicare**.  

Legarea fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] face fișierul Project coordonator și stabilește structura detaliată a proiectului din șablonul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] drept doar în citire.  Pentru a face modificări în planul de proiect, trebuie să le efectuați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să le publicați ca actualizări la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Citiți o planificare încărcată de resurse

Când citiți un proiect din Project Service Automation, calendarul resursei nu este sincronizat cu clientul desktop. Dacă există diferențe în duratele sarcinii, efortul sau sfârșitul, probabil că resursele și clientul desktop nu au același calendar de șablon de oră de lucru aplicat proiectului.


## <a name="data-synchronization"></a>Sincronizarea datelor
Tabelele din această secțiune oferă informații despre sincronizarea datelor entității între Project Service Automation și programul de completare pentru desktop Microsoft Project.

### <a name="project-task-entity-table"></a>Tabelul entității de Sarcini de proiect
Următorul tabel prezintă modul în care datele din entitatea Sarcină de Proiect sunt sincronizate între Project Service Automation și programul de completare pentru desktop Microsoft Project.

| **Entitate** | **Câmp** | **Microsoft Project la Project Service Automation** | **Project Service Automation la Microsoft Project** |
| --- | --- | --- | --- |
| Activitate de proiect | Data scadentă | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Efort estimat | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | ID Client MS Project | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Activitate părinte | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Project | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Activitate de proiect | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Nume activitate de proiect | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Unitate de resursă (perimat în v3.0) | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Durată planificată | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | Data de început | Synchronized | Nu sunt sincronizate |
| Activitate de proiect | ID WBS | Synchronized | Nu sunt sincronizate |

### <a name="team-member-entity-table"></a>Tabelul entității Membru al echipei
Următorul tabel prezintă modul în care datele din entitatea Membru al echipei sunt sincronizate între Project Service Automation și Micros

| **Entitate** | **Câmp** | **Microsoft Project la Project Service Automation** | **Project Service Automation la Microsoft Project** |
| --- | --- | --- | --- |
| Membru echipă | ID Client MS Project | Synchronized | Nu sunt sincronizate |
| Membru echipă | Nume poziție | Synchronized | Nu sunt sincronizate |
| Membru echipă | proiect | Synchronized | Synchronized |
| Membru echipă | Echipă de proiect | Synchronized | Synchronized |
| Membru echipă | Unitate de resurse | Nu sunt sincronizate | Synchronized |
| Membru echipă | Rol | Nu sunt sincronizate | Synchronized |
| Membru echipă | Program de lucru | Nu sunt sincronizate | Nu sunt sincronizate |

### <a name="resource-assignment-entity-table"></a>Tabelul entității de Atribuire a resurselor
Următorul tabel prezintă modul în care datele din entitatea de Atribuire a resurselor sunt sincronizate între Project Service Automation și Micros

| **Entitate** | **Câmp** | **Microsoft Project la Project Service Automation** | **Project Service Automation la Microsoft Project** |
| --- | --- | --- | --- |
| Atribuire de resurse | De la data | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Ore | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | ID Client MS Project | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Lucru planificat | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Project | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Echipă de proiect | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Atribuire de resurse | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Activitate | Synchronized | Nu sunt sincronizate |
| Atribuire de resurse | Până în prezent | Synchronized | Nu sunt sincronizate |

### <a name="project-task-dependencies-entity-table"></a>Tabelul entității de Dependențe sarcini de proiect
Următorul tabel prezintă modul în care datele din entitatea de Dependențe sarcini de proiect sunt sincronizate între Project Service Automation și Micros

| **Entitate** | **Câmp** | **Microsoft Project la Project Service Automation** | **Project Service Automation la Microsoft Project** |
| --- | --- | --- | --- |
| Dependențe de activitate proiect | Dependență de activitate proiect | Synchronized | Nu sunt sincronizate |
| Dependențe de activitate proiect | Tip link | Synchronized | Nu sunt sincronizate |
| Dependențe de activitate proiect | Activitate predecesoare | Synchronized | Nu sunt sincronizate |
| Dependențe de activitate proiect | Project | Synchronized | Nu sunt sincronizate |
| Dependențe de activitate proiect | Activitate succesoare | Synchronized | Nu sunt sincronizate |

### <a name="additional-resources"></a>Resurse suplimentare
 [Ghidul Managerului de proiect](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]