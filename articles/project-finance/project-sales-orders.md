---
title: Comenzi de vânzare pentru proiecte de timp și materiale
description: Acest subiect explică cum să creați comenzi de vânzare bazate pe proiecte pentru proiecte de timp și materiale.
author: KimANelson
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
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ro-RO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754700"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="5d873-103">Comenzi de vânzare pentru proiecte de timp și materiale</span><span class="sxs-lookup"><span data-stu-id="5d873-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="5d873-104">Acest subiect descrie cum să creați o comandă de vânzare pentru un proiect.</span><span class="sxs-lookup"><span data-stu-id="5d873-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="5d873-105">Comenzile de vânzare pot fi create numai pentru proiecte de tip **timp și material**.</span><span class="sxs-lookup"><span data-stu-id="5d873-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="5d873-106">Dacă un proiect de timp și materiale are mai multe surse de finanțare în contractul de proiect, trebuie să activați parametrul **Permiteți comenzi de vânzare pentru proiecte cu mai multe surse de finanțare** pe pagina **Managementul proiectului și parametrii contabili**.</span><span class="sxs-lookup"><span data-stu-id="5d873-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="5d873-107">Suportul pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare este disponibil începând cu versiunea aplicației 10.0.2 și mai nouă.</span><span class="sxs-lookup"><span data-stu-id="5d873-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="5d873-108">Parametrul pentru a permite asistența pentru comenzile de vânzare a proiectelor cu mai multe surse de finanțare va fi eliminat în valul de lansare din aprilie 2020, după care funcționalitatea va fi întotdeauna activată.</span><span class="sxs-lookup"><span data-stu-id="5d873-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="5d873-109">Puteți crea comenzi de vânzare bazate pe proiecte în două moduri:</span><span class="sxs-lookup"><span data-stu-id="5d873-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="5d873-110">Accesați proiectul în sine.</span><span class="sxs-lookup"><span data-stu-id="5d873-110">Go to the project itself.</span></span> <span data-ttu-id="5d873-111">În panoul de acțiuni, selectați **Gestionați > Sarcini articol > Comandă de vânzare**.</span><span class="sxs-lookup"><span data-stu-id="5d873-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="5d873-112">Informațiile despre proiect vor fi implicite pentru comanda de vânzare din proiect.</span><span class="sxs-lookup"><span data-stu-id="5d873-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="5d873-113">Dacă contractul de proiect are mai multe surse de finanțare, va trebui să selectați sursa de finanțare pentru a seta clientul pentru comanda de vânzare.</span><span class="sxs-lookup"><span data-stu-id="5d873-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="5d873-114">Dacă există o singură sursă de finanțare pentru proiect, clientul va fi setat automat.</span><span class="sxs-lookup"><span data-stu-id="5d873-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="5d873-115">Accesați pagina de listă **Comanda toate vânzările** și creați o nouă comandă de vânzări.</span><span class="sxs-lookup"><span data-stu-id="5d873-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="5d873-116">Va trebui să selectați proiectul pentru comanda de vânzare.</span><span class="sxs-lookup"><span data-stu-id="5d873-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="5d873-117">După selectarea proiectului, clientul va fi setat din sursa de finanțare sau va trebui să selectați sursa de finanțare dacă contractul de proiect are mai multe surse de finanțare.</span><span class="sxs-lookup"><span data-stu-id="5d873-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>
