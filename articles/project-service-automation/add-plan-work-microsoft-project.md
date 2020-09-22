---
title: Utilizarea programului de completare Project Service pentru a vă planifica munca în Microsoft Project | MicrosoftDocs
description: Acest subiect furnizează informații despre cum se adaugă, se configurează și se utilizează programul de completare Microsoft Project pentru Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754709"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Utilizarea programului de completare Project Service Automation pentru a vă planifica munca în Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vă ajută să vă planificați proiectele, inclusiv să realizați estimări. Puteți defini lucrarea astfel încât costurile, efortul și valoarea vânzărilor să fie clare la momentul când se trimite propunerea finală.  

 Acum puteți instala [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] și puteți planifica în mediul familiar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilizați capacitățile robuste de planificare și management din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], apoi actualizați-vă planul de proiect în Project Service Automation.  

> [!IMPORTANT]
> - Pentru a utiliza gestionarea documentelor SharePoint pentru a vă stoca filierele [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pentru proiectele [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], administratorul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] va trebui să pornească gestionare documente. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Activați gestionarea documentelor SharePoint pentru entități specifice](../admin/enable-sharepoint-document-management-specific-entities.md)  
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] este compatibil numai cu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descărcați și instalați programul de completare  
 Țineți informațiile de conectare [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] la îndemână. Veți avea nevoie de aceste informații pentru a vă conecta de la [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  De la Centrul de descărcare puteți descărca programul de completare pentru versiunea acceptată de Project Service, fie [v2. X](https://go.microsoft.com/fwlink/?linkid=828268), fie [v 3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Faceți clic pe linkul de descărcare.  

3.  Odată ce descărcarea s-a finalizat, faceți clic pe **Da** pentru a instala programul de completare.  

## <a name="configure-the-add-in"></a>Configurați programul de completare  

1. Deschideți [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și faceți clic pe fila **Project Service**.  

2. Faceți clic pe **Conectare**.  

3. Introduceți informațiile de conectare și faceți clic pe **Conectare**.  

   Acum puteți începe să folosiți programul de completare.  

## <a name="read-from-a-template"></a>Citirea de pe un șablon  
 Citiți dintr-un șablon creat în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] și copiat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pentru a începe să vă planificați proiectul. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crearea unui șablon de proiect (Project Service Automation)](../project-service/create-project-template.md)  

1.  De pe fila **Project Service**, faceți clic pe **Citire** > **Șablon de proiect Project Service Automation**.  

2.  Alegeți un șablon de proiect din listă și faceți clic pe **Deschidere**.  

    > [!NOTE]
    >  În mod implicit, activitățile copiate din șablon în Project sunt setate drept planificate manual.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Atribuiți roluri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] resurselor proiectului  

1.  Deschideți un proiect și faceți clic pe panglica **Activitate**.  

2.  Faceți clic pe meniul **Diagramă Gantt** și alegeți **Foaie de resurse**.  

3.  Pe foaia de resurse, faceți clic pe meniul vertical **Rol de resursă Project Service** și alegeți un rol Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Găsiți resurse pentru proiectul dvs.  

1.  Din fila Project Service, selectați un rând și faceți clic pe **Găsiți resurse**.  

2.  Pe ecranul **Rezervați resursa**, selectați resursa pe care doriți s-o utilizați pentru proiect.  

3.  Faceți clic pe **Rezervare**, apoi pe **OK**.  

## <a name="publish-your-project"></a>Publicarea proiectului  
Atunci când terminați de planificat proiectul, următorul pas este să importați și să publicați proiectul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Proiectul se va importa în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Se aplică procesul de generare a echipelor și a prețurilor. Deschideți proiectul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pentru a vedea că echipa, estimările de proiect și structura detaliată a proiectului au fost generate. Următorul tabel arată unde să găsiți rezultatele:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Diagramă Gantt**   | Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Structura detaliată a proiectului**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Foaie de resurse** |   Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membrii echipei de proiect**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Folosirea utilizării**    |    Importurile în ecranul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimări de proiect**.     |

**Pentru a vă importa și a vă publica proiectul**  
1. De pe fila **Project Service**, faceți clic pe **Publicare** > **Proiect nou Project Service Automation**.  

2. În caseta de dialog **Publicați într-un nou proiect din Project Service**, introduceți **Numele proiectului** și selectați **Clientul**.  

3. Opțional, bifați **Legați planul de proiect la Project Service Automation** pentru a lega planul fișierului Project la Project Service Automation.  

4. Faceți clic pe **Publicare**.  

   Legarea fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] face fișierul Project coordonator și stabilește structura detaliată a proiectului din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] drept doar în citire.  Pentru a face modificări în planul de proiect, trebuie să le efectuați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să le publicați ca actualizări la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editarea unui proiect care a fost importat  
 Pentru a modifica un plan de proiect care a fost importat în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], aveți două opțiuni:  

- Deschideți fișierul principal și editați-l în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Anulați legarea fișierului și editați-l direct în Project Service. În mod implicit, un proiect care a fost încărcat din [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] este blocat și poate fi editat numai în Project. Pentru a edita fișierul în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], legarea fișierului trebuie anulată.  

### <a name="edit-in-pn_microsoft_project"></a>Editarea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Din meniul principal, faceți clic pe **Project Service** > **Proiecte**.  

2. Din lista de proiecte, deschideți-l pe cel creat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Faceți clic pe **Deschideți în MS Project** din panglică. Acest lucru va deschide fișierul coordonator legat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Anulați legarea unui fișier și editați-l în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Din meniul principal, faceți clic pe **Project Service** > **Proiecte**.  

2. Din lista de proiecte, deschideți-l pe cel creat în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Faceți clic pe **Anulați legarea în MS Project** din panglică.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Încărcarea unui fișier Project în SharePoint sau în Grupurile Office  
 Puteți încărca fișierul Project în SharePoint și îl puteți găsi sub Documentele asociate pentru proiectul dvs. [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Trebuie ca administratorul dvs. să configureze gestionarea de documente SharePoint și să o activeze pentru entitatea Project. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurați integrarea SharePoint](../admin/set-up-sharepoint-integration.md)  

 De asemenea, puteți încărca fișierul Project în [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] dacă aveți grupurile Office configurate. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Colaborați cu colegii dvs. utilizând grupuri Office 365](../basics/collaborate-with-colleagues-using-office-365-groups.md)  

### <a name="upload-a-file-for-sharepoint"></a>Încărcarea unui fișier pentru SharePoint  

1. Din meniul principal, faceți clic pe **Project Service** > **Încărcare**.  

2. Selectați **În documentele Project din Project Service Automation**.  

3. În caseta de dialog **Activați deschiderea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selectați **Da** sau **Nu**.  

   - Dacă faceți clic pe **Da**, veți putea selecta butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** din Project Service Automation, veți putea lansa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și încărca fișierul Project din biblioteca de documente SharePoint.  

   - Dacă faceți clic pe **Nu**, linkul pentru butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nu va funcționa.  

4. Fișierul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] poate fi găsit în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sub **Documente** pentru respectivul proiect [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Încărcarea unui fișier pentru grupurile Office  

1. Din meniul principal, faceți clic pe **Project Service** > **Încărcare**.  

2. Selectați **În documentele Project din Project Service Automation**.  

3. În caseta de dialog **Activați deschiderea în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selectați **Da** sau **Nu**.  

   - Dacă faceți clic pe **Da**, veți putea selecta butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** în Project Service Automation, veți putea lansa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și încărca fișierul Project din biblioteca de documente SharePoint.  

   - Dacă faceți clic pe **Nu**, linkul pentru butonul **Deschideți în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nu va funcționa.  

4. Fișierul [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] poate fi găsit în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sub **Documente** pentru respectivul proiect [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publicarea proiectului ca șablon  
 Puteți să vă salvați proiectul și să-l refolosiți dacă îl salvați ca șablon de proiect în [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Șabloanele de proiect sunt planuri de proiect reutilizabile din [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crearea unui șablon de proiect (Project Service Automation)](../project-service/create-project-template.md)  

1. De pe fila **Project Service**, faceți clic pe **Publicare** > **Șablon proiect nou Project Service Automation**.  

2. În caseta de dialog **Publicați într-un nou proiect din șablonul Project Service**, introduceți **Numele șablonului de proiect**.  

3. Opțional, bifați **Legați planul de proiect la Project Service Automation** pentru a lega fișierul Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Faceți clic pe **Publicare**.  

Legarea fișierului Project la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] face fișierul Project coordonator și stabilește structura detaliată a proiectului din șablonul [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] drept doar în citire.  Pentru a face modificări în planul de proiect, trebuie să le efectuați în [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] și să le publicați ca actualizări la [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Consultați și  
 [Ghidul Managerului de proiect](../project-service/project-manager-guide.md)
