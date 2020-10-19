---
title: Implementare Project Operations Lite - facturare de la ofertă și până la proforma
description: Acest subiect oferă informații despre cum se instalează implementarea Project Operations lite - gestionați facturarea proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949026"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="4224f-103">Implementare Project Operations Lite - facturare de la ofertă și până la proforma</span><span class="sxs-lookup"><span data-stu-id="4224f-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="4224f-104">_**Se aplică la:** implementare simplificată - facturare de la tranzacție la proforma_</span><span class="sxs-lookup"><span data-stu-id="4224f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4224f-105">Operațiunile de proiect acceptă mai multe modele de implementare.</span><span class="sxs-lookup"><span data-stu-id="4224f-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="4224f-106">Pentru a determina cel mai bun model de implementare, consultați [Tipuri de implementare](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="4224f-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="4224f-107">Această implementare, implementare simplificată - se ocupă de facturarea proforma, are ca rezultat o **Common Data Service-desfășurarea doar a Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="4224f-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="4224f-108">Instalați Project Operations într-un nou mediu CDS</span><span class="sxs-lookup"><span data-stu-id="4224f-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="4224f-109">Instalați într-un mediu CDS existent</span><span class="sxs-lookup"><span data-stu-id="4224f-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="4224f-110">Instalați Project Operations într-un mediu CDS nou</span><span class="sxs-lookup"><span data-stu-id="4224f-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="4224f-111">Drept [Administrator global sau de Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) cu un permis de Project Operations, creați un mediu CDS nou în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="4224f-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="4224f-112">Asigurați-vă că sunt activate **Baza de date CDS** și **Aplicații Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="4224f-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="4224f-113">Pentru informații suplimentare, consultați [Creați și gestionați medii în centrul de administrare Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="4224f-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="4224f-114">Selectați **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4224f-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="4224f-115">Instalați Project Operations într-un mediu CDS existent</span><span class="sxs-lookup"><span data-stu-id="4224f-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="4224f-116">În calitate de [Administrator global sau de Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) cu o licență Project Operations, localizați mediul în [Centrul de administrare PowerPlatform](https://admin.powerplatform.com) unde puteți instala Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4224f-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="4224f-117">Instalași **Microsoft Dynamics 365 Project Operations** din lista de implementare a aplicațiilor Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4224f-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="4224f-118">Pentru informații suplimentare, consultați [aplicații Gestionați Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="4224f-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


