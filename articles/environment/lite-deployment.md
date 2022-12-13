---
title: Implementați Project Operations Lite
description: Acest articol oferă informații despre cum se instalează implementarea Project Operations lite - gestionarea facturării proforme.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: ro-RO
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810994"
---
# <a name="deploy-project-operations-lite"></a>Implementați Project Operations Lite

_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_



Operațiunile de proiect acceptă mai multe modele de implementare. Pentru a determina cel mai bun model de implementare, consultați [Tipuri de implementare](determine-deployment-type.md).


> [!IMPORTANT]
> Această implementare, implementare simplificată - se ocupă de facturarea proforma, are ca rezultat o **Dataverse-desfășurarea doar a Project Operations**.

- [Instalare Project Operations într-un nou mediu Dataverse](#new)
- [Instalare într-un mediu Dataverse existent](#existing)
- [Instalați într-un mediu Dataverse existent care are componente de scriere duală](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Instalați Project Operations Lite într-un nou Dataverse mediu

1. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență de Project Operations, creați un mediu Dataverse nou în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com). Asigurați-vă că **Crearea unei baze de date pentru acest mediu** și **Aplicații Dynamics 365** sunt activate. Pentru informații suplimentare, consultați [Creați și gestionați medii în centrul de administrare Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Selectați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instalați Project Operations Lite într-un mediu Dataverse existent 
1. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență Project Operations, localizați mediul în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com) unde puteți instala Project Operations.
1. Instalați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365. Pentru informații suplimentare, consultați [aplicații Gestionați Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instalați Project Operations Lite într-un mediu Dataverse existent în care sunt deja prezente soluții de scriere duală

Dacă doriți să continuați să rulați Project Operations în modul Lite Deployment, ar trebui să urmați acești pași:

1. În calitate de [Administrator global sau de Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență Project Operations, localizați mediul în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com) unde puteți instala Project Operations.
1. Instalați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365. Pentru informații suplimentare, consultați [aplicații Gestionați Dynamics 365](/power-platform/admin/manage-apps).
1. Deoarece mediul dvs. are componente de scriere dublă care ajută la integrarea în aplicațiile de finanțare și operațiuni instalate, instalarea Project Operations va instala și capabilitățile și extensiile necesare pentru a integra datele legate de proiect în aplicațiile de finanțare și operațiuni. Deoarece doriți să rulați Operațiuni de proiect în implementarea Lite, aceste componente de integrare ar trebui eliminate, deoarece vor crea restricții și cheltuieli generale pentru scenariile de implementare Lite. Dezinstalați manual soluțiile **Dynamics 365 Project Operations Dual Write** și **Dynamics 365 Project Operations Dual Write Entity Maps** pentru a elimina aceste componente.
1. Accesați **Operațiuni de proiect -> Setări -> Parametri**. Deschideți pagina de detalii **Parametrul proiectului** și setați câmpul **Comportament de actualizare a soluției** la **Lite Numai**. Acest lucru asigură că orice actualizări ulterioare ale Operațiunilor de proiect nu vor aduce înapoi componentele de integrare în Operațiunile de proiect.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
