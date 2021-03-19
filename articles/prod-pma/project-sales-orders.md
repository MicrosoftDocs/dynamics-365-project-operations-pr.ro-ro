---
title: Comenzi de vânzare pentru proiecte de timp și materiale
description: Acest subiect explică cum să creați comenzi de vânzare bazate pe proiecte pentru proiecte de timp și materiale.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289069"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="3d46d-103">Comenzi de vânzare pentru proiecte de timp și materiale</span><span class="sxs-lookup"><span data-stu-id="3d46d-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3d46d-104">Acest subiect descrie cum să creați o comandă de vânzare pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="3d46d-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="3d46d-105">Comenzile de vânzare pot fi create numai pentru proiecte de tip **timp și material**.</span><span class="sxs-lookup"><span data-stu-id="3d46d-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="3d46d-106">Dacă un proiect de timp și materiale are mai multe surse de finanțare în contractul de proiect, trebuie să activați parametrul **Permiteți comenzi de vânzare pentru proiecte cu mai multe surse de finanțare** pe pagina **Managementul proiectului și parametrii contabili**.</span><span class="sxs-lookup"><span data-stu-id="3d46d-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="3d46d-107">Suportul pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare este disponibil începând cu versiunea aplicației 10.0.2 și mai nouă.</span><span class="sxs-lookup"><span data-stu-id="3d46d-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="3d46d-108">Parametrul pentru a permite asistența pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare va fi eliminat în valul de lansare din aprilie 2020, după care funcționalitatea va fi întotdeauna activată.</span><span class="sxs-lookup"><span data-stu-id="3d46d-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="3d46d-109">Puteți crea comenzi de vânzare bazate pe proiecte în două moduri:</span><span class="sxs-lookup"><span data-stu-id="3d46d-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="3d46d-110">Accesați proiectul în sine.</span><span class="sxs-lookup"><span data-stu-id="3d46d-110">Go to the project itself.</span></span> <span data-ttu-id="3d46d-111">În panoul de acțiuni, selectați **Gestionați > Sarcini articol > Comandă de vânzare**.</span><span class="sxs-lookup"><span data-stu-id="3d46d-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="3d46d-112">Informațiile despre proiect vor fi implicite pentru comanda de vânzare din proiect.</span><span class="sxs-lookup"><span data-stu-id="3d46d-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="3d46d-113">Dacă contractul de proiect are mai multe surse de finanțare, va trebui să selectați sursa de finanțare pentru a seta clientul pentru comanda de vânzare.</span><span class="sxs-lookup"><span data-stu-id="3d46d-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="3d46d-114">Dacă există o singură sursă de finanțare pentru proiect, clientul va fi setat automat.</span><span class="sxs-lookup"><span data-stu-id="3d46d-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="3d46d-115">Accesați pagina de listă **Comanda toate vânzările** și creați o nouă comandă de vânzări.</span><span class="sxs-lookup"><span data-stu-id="3d46d-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="3d46d-116">Va trebui să selectați proiectul pentru comanda de vânzare.</span><span class="sxs-lookup"><span data-stu-id="3d46d-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="3d46d-117">După selectarea proiectului, clientul va fi setat din sursa de finanțare sau va trebui să selectați sursa de finanțare dacă contractul de proiect are mai multe surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="3d46d-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]