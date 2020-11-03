---
title: Activați caracteristicile din aplicația Project Finder Mobile
description: Cum să activați caracteristicile aplicației Project Finder Mobile pentru Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082803"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Activați caracteristicile aplicației Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Resursele dvs. pot folosi aplicația Project Finder Mobile pe telefon cu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pentru a găsi noi proiecte la care să lucreze și a-și actualiza seturile de abilități.  
  
 Aplicația este disponibilă pentru [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], telefoanele [!INCLUDE[tn_android](../includes/tn-android.md)] și [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Trebuie să setați două opțiuni în setarea de parametri pentru ca unitatea dvs. organizațională să le permită utilizatorilor să vadă necesarul de resurse al proiectelor și să-și actualizeze abilitățile.  
  
> [!NOTE]
>  Aplicația Project Finder Mobile funcționează numai cu [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], nu cu instalații locale.  
  
1. Accesați **Project Service > Parametri**.  
  
2. Faceți clic pe setarea de parametri pe care doriți s-o utilizați pentru a permite caracteristicile aplicației Project Finder Mobile.  
  
3. În zona **General** , setați **Cerințele de resurse vizibile resurselor** la **Da**.  
  
4. Setați **Permiteți actualizarea abilităților de către resursă** la **Da**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Aceasta este o setare globală. Managerii de proiect pot seta dacă un proiect individual va fi vizibile pe pagina **Echipa de proiect** a acelui proiect.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificări prin e-mail  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trimite e-mailuri cu privire la cererile de resurse către următorii destinatari, la următoarele ore:  
  
|Destinatar|Eveniment|  
|---------------|-----------|  
|Manager de proiect|-   Când o resursă se înscrie pentru un proiect cu aplicația Project Finder Mobile.|  
|Resursă|-   Când munca pentru care s-a înscris resursa a fost deja efectuată de o altă resursă.<br />-   Când cererea de aprobare a abilităților a fost aprobată sau respinsă.<br />-   Când cererea de înscriere a proiectului a fost aprobată sau respinsă.|  
  
## <a name="privacy-notice"></a>Notificare privind confidențialitatea  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Consultați și  
 [Configurați resursele](../psa/set-up-resources.md)
