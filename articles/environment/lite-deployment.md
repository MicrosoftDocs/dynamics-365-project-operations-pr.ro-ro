---
title: Implementați Project Operations - simplificat
description: Acest articol oferă informații despre cum să instalați implementarea Project Operations lite - acord cu facturarea proforma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930333"
---
# <a name="deploy-project-operations---lite"></a>Implementați Project Operations - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_



Operațiunile de proiect acceptă mai multe modele de implementare. Pentru a determina cel mai bun model de implementare, consultați [Tipuri de implementare](determine-deployment-type.md).


> [!IMPORTANT]
> Această implementare, implementare simplificată - se ocupă de facturarea proforma, are ca rezultat o **Dataverse-desfășurarea doar a Project Operations**.

- [Instalați Project Operations într-un nou Dataverse mediu inconjurator](#new)
- [Instalați într-un existent Dataverse mediu inconjurator](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Instalați Project Operations pe un nou Dataverse mediu inconjurator

1. Dupa cum [Global sau Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență de operațiuni de proiect, creați o licență nouă Dataverse mediu în [Centru de administrare PowerPlatform](https://admin.powerplatform.com). Asigura-te ca **Creați o bază de date pentru acest mediu** și **Aplicații Dynamics 365** sunt activate. Pentru informații suplimentare, consultați [Creați și gestionați medii în centrul de administrare Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selectați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instalați Project Operations pe un existent Dataverse mediu inconjurator
1. Asigurați-vă că mediul nu a fost configurat cu [scriere duală](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) deoarece instalarea va instala apoi [Operațiuni de proiect pentru scenarii bazate pe resurse/neaprovizionate](project-operations-integrated-deployment-overview.md) capabilități.
2. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență Project Operations, localizați mediul în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com) unde puteți instala Project Operations.
3. Instalați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365. Pentru informații suplimentare, consultați [aplicații Gestionați Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
