---
title: Implementați Project Operations - simplificat
description: Acest subiect oferă informații despre cum se instalează implementarea Project Operations lite - gestionați facturarea proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950279"
---
# <a name="deploy-project-operations---lite"></a>Implementați Project Operations - simplificat

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Operațiunile de proiect acceptă mai multe modele de implementare. Pentru a determina cel mai bun model de implementare, consultați [Tipuri de implementare](determine-deployment-type.md).


> [!IMPORTANT]
> Această implementare, implementare simplificată - se ocupă de facturarea proforma, are ca rezultat o **Common Data Service-desfășurarea doar a Project Operations**.

- [Instalați Project Operations într-un nou mediu CDS](#new)
- [Instalați într-un mediu CDS existent](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a>Instalați Project Operations într-un mediu CDS nou

1. Drept [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu un permis de Project Operations, creați un mediu CDS nou în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com). Asigurați-vă că sunt activate **Baza de date CDS** și **Aplicații Dynamics 365**. Pentru informații suplimentare, consultați [Creați și gestionați medii în centrul de administrare Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selectați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365.


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a>Instalați Project Operations într-un mediu CDS existent

1. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență Project Operations, localizați mediul în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com) unde puteți instala Project Operations.
2. Instalați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365. Pentru informații suplimentare, consultați [aplicații Gestionați Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]