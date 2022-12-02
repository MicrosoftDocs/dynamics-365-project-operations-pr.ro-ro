---
title: Implementați Project Operations - simplificat
description: Acest articol oferă informații despre cum se instalează implementarea Project Operations lite - gestionarea facturării proforme.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930333"
---
# <a name="deploy-project-operations---lite"></a>Implementați Project Operations - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_



Operațiunile de proiect acceptă mai multe modele de implementare. Pentru a determina cel mai bun model de implementare, consultați [Tipuri de implementare](determine-deployment-type.md).


> [!IMPORTANT]
> Această implementare, implementare simplificată - se ocupă de facturarea proforma, are ca rezultat o **Dataverse-desfășurarea doar a Project Operations**.

- [Instalare Project Operations într-un nou mediu Dataverse](#new)
- [Instalare într-un mediu Dataverse existent](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instalare Project Operations într-un mediu Dataverse nou

1. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență de Project Operations, creați un mediu Dataverse nou în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com). Asigurați-vă că **Crearea unei baze de date pentru acest mediu** și **Aplicații Dynamics 365** sunt activate. Pentru informații suplimentare, consultați [Creați și gestionați medii în centrul de administrare Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selectați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalați Project Operations într-un mediu Dataverse existent
1. Asigurați-vă că mediul nu a fost configurat cu [scriere duală](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) deoarece instalarea va instala mai apoi capabilități [Project Operations pentru scenarii bazate pe resurse/non-aprovizionate](project-operations-integrated-deployment-overview.md).
2. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență Project Operations, localizați mediul în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com) unde puteți instala Project Operations.
3. Instalați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365. Pentru informații suplimentare, consultați [aplicații Gestionați Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
